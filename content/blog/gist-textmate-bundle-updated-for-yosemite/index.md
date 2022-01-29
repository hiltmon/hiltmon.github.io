---
title: "Gist TextMate Bundle updated for Yosemite"
date: 2014-10-18 12:44:44 -0400
tags: textmate
---

{{< figure src="images/textmate.png" width=128 height=128 class="image-right" >}}

Thanks to Michael Sheets, the Gist TextMate bundle now works in [TextMate 2](http://macromates.com) on Yosemite. The issue was that the UI code in TextMate 2 relied on Ruby 1.8, and Ruby 1.8 is deprecated and no longer installed in OS X 10.10. 

Michael created a shim to fake Ruby 1.8 until such time as the code base moves to Ruby 2.0, implemented the change in the Gist bundle and it's working now.

You can get the source at [GitHub](https://github.com/hiltmon/Gist.tmbundle) or just wait until it gets propagates via TextMate 2's bundle update process.

*Follow the author as [@hiltmon](https://twitter.com/hiltmon) on Twitter.*
