---
title: "Open Extension-less Files in your Favorite Editor on OS X"
date: 2015-09-04 09:40:47 -0400
tags: 
---

{{< figure src="images/less-1.png" width=263 height=453 class="image-right" >}}

Xcode does a horrible job of editing Makefiles (and other extension-less files like dot-files). If you right-click in Xcode on a Makefile and **Open with External Editor**, OS X opens it in TextEdit. *Which is worse.*

The issue is that TextEdit is associated with extension-less files. Usually to change how files are opened, you select the file in Finder, right-click and choose **Get Info** from the menu. You then choose the editor in the **Open with** dropdown and click **Change All...**. But this does not work for extension-less files, it throws the below error.

{{< figure src="images/less-2.png" width=466 height=195 >}}

The solution is to use [RCDefaultApp](http://www.rubicode.com/Software/RCDefaultApp/) to change this association.

Install it now, its free. I'll wait.

Once its installed, open **Default Apps** from **System Preferences**, go to **Apps** and select the application you prefer for extension-less files, I use trusty [BBEdit](http://www.barebones.com/products/bbedit/) if course. Scroll down to find the **public.data** UTI, check it and click **Set as Default**. Extension-less files should now open in BBEdit from Finder and from Xcode.

{{< figure src="images/less-3.png" width=666 height=417 >}}

<span class="light">I figured out the necessary UTI using the command `mdls Makefile` and seeing that the system had it as "public.data". Many other sites say using "public.text" is the correct mapping but that did *not* work for me on OS X 10.10 Yosemite.</span>

*Follow the author as [@hiltmon](https://twitter.com/hiltmon) on Twitter.*

