---
title: "Automatically Managed Files"
date: 2012-05-16 16:02:00-0400
tags: [Productivity]
---

I'm moving back to the desktop for a while to do some iOS programming. Many of the files on my laptop are auto-managing, so as I am moving the process, I thought I'd share how they are automatically managed using [Hazel](http://www.noodlesoft.com/hazel.php) from NoodleSoft.

Hazel is a background process that monitors folders and executes automated actions on matched files. Once a rule is created in Hazel, I can forget about what I have to do and Hazel takes care of things for me.

The first rule is simple, clean desktop. I drop all my temporary files and stuff on the desktop while I am working, then either file it later, delete it or more often than not, forget about it. Before this rule, my desktop was always a complete mess. My "Clean Desktop" macro monitors the desktop folder, and if I have not touched a file in 1 hour, it moves that file off the desktop into a working folder. Which means I always have a clean desktop.

{{< figure src="images/hazel-clean-desktop.png" width=640 height=260 >}}

But that does mean I have a messy Working folder. So I have Hazel monitor that as well. The first rule colors all files that are more than a day old in gray so at a glance I can see the old files.

{{< figure src="images/hazel-working-color-gray.png" width=640 height=230 >}}

The second rule clears the gray color if I do access the file.

{{< figure src="images/hazel-working-clear-color.png" width=640 height=205 >}}

And the third rule deletes any files I leave in working (which is most of them) after a while.

{{< figure src="images/hazel-empty-working-folder.png" width=640 height=230 >}}

Another use I have for Hazel is to archive my old nvAlt documents. In order for this to work, I had to install [openmeta](http://code.google.com/p/openmeta/) to enable tagging and enable super-secret openmeta mode in Hazel

```
defaults write com.noodlesoft.Hazel OMToolPath /usr/local/bin/openmeta
```

Now, when I tag an article in [nvAlt](http://brettterpstra.com/project/nvalt/) as `archive`, Hazel moves it to an archive folder and clears it out of nvAlt.

{{< figure src="images/hazel-archive-tag.png" width=640 height=205 >}}

The other folder I leave in a mess is handled by default by Hazel. All trashed files that are there for more than a week are deleted. I apply the same rule to the downloads folder. I also use the App Sweep feature whereby when I delete an application, Hazel looks for and deletes all the matching hidden files as well, such as preferences and local data, keeping my system much cleaner.

{{< figure src="images/hazel-trash.png" width=640 height=330 >}}

But the real reason I love Hazel is the next thing I am doing with it, using an Actions folder to have Hazel do all my filing for me. I am at the point where I am switching to a more paperless workflow so I download bank statements and other bills and I'd like them to be renamed and filed for me. This is what Hazel excels at and I'll write about it once I get it fully working.
