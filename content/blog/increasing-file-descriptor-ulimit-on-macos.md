---
title: "Increasing File Descriptor Ulimit on MacOs"
date: 2023-01-01T11:17:10-05:00
author: Hilton Lipschitz
tags: [ Development, Macintosh, "Tips and Tricks", "OS X" ]
---

> **Warning:** This post is only for developers who are having issues when coding against `file descriptors` in the form of C-style file handles or sockets on MacOS. For everyone else, this does not apply.

### Running out of Resources

Right now I am developing an application that uses sockets (underneath a stack of other software) for inter-process communication. The problem is that after a few debug runs or crashes (I did say developing), the application will not start again from resource starvation. And the error message is no help at all.

Creating a socket connection internally asks for and uses up a system file descriptor. If the socket is closed properly, that file descriptor is returned back to the system. But when developing or debugging, because of crashes or hard kills, the socket may still close but the file descriptor is not released back. If the number of file descriptors for a process are exceeded, no new ones can be created. And no new runs can happen. It happens to me several times a day, and the only solution is to reboot.

On MacOS, the maximum number of file descriptors is set to a quite low 256. To see yours, run `ulimit -n`. *Once again I must remind you, this is plenty for 99.9% of all use cases on a Mac and should not be changed!*

### Increasing file descriptors

In order to permanently change the file descriptor limit, you need to run a script at boot to setup the system limits you prefer. This has been tested on MacOS Ventura, Monterey and Big Sur.

In `/Library/LaunchDaemons`, create a file called `limit.maxfiles.plist` and fill it with this:

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple/DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
  <plist version="1.0">
    <dict>
      <key>Label</key>
        <string>limit.maxfiles</string>
      <key>ProgramArguments</key>
        <array>
          <string>launchctl</string>
          <string>limit</string>
          <string>maxfiles</string>
          <string>8192</string>
          <string>81920</string>
        </array>
      <key>RunAtLoad</key>
        <true />
      <key>ServiceIPC</key>
        <false />
    </dict>
  </plist>
```

This increases open files (soft) from 256 to 8192, and system-wide (hard) from 8192 to 81920.

To ensure this runs successfully, run the following commands to set ownership, permissions and add it to the boot flow:

```
sudo chown root:wheel limit.maxfiles.plist
sudo chmod 0644 limit.maxfiles.plist
sudo launchctl load -w /Library/LaunchDaemons/limit.maxfiles.plist
```

Then reboot your Mac. After a restart, you should see the new numbers:

```
~ ❯ ulimit -Sn
8192
~ ❯ ulimit -Hn
81920
```

And you are good to go.

### Yes, I tried

- The Linux solution:
```
echo "* hard nofile 81920" >> /etc/security/limits.conf
echo "* soft nofile 8192" >> /etc/security/limits.conf
sysctl -w fs.file-max=8192
sysctl -p
```

- Editing `/etc/systctl.conf` manually
- Adding `ulimit -n 8192` to the shell startup

They work on Linux (and you should use those there) but not on MacOs.

