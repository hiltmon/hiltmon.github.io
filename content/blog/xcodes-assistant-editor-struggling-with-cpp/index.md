---
title: "Xcode's Assistant Editor struggling with C++"
date: 2023-03-03T09:36:12-05:00
author: Hilton Lipschitz
tags: [ Development, Programming, C++ ]
---

One of the best features of Xcode for C++ programmers is its Assistant Editor. This is an editor panel to the right of the main editor where you are working that automatically (and somewhat magically) displays the counterpart to the file you are editing. So for example if I am working on `service.cpp`, the assistant displays its header `service.h`.

{{< figure src="images/AssistantEditor.png" width=484 height=170 >}}

This is great for productivity. I can glance to the right to see the declarations that I am implementing, and can change both declaration and definition directly without opening or changing contexts. And when I switch to another code file, the assistant helpfully display's its header.  Even better, when I pick a header file to work on, the Assistant shows me it's matching implementation file.

But recently the Assistant has gone haywire.

> Yes, I tried it all, and nuking the derived data folders and reinstalling Xcode has not helped. And I am on the latest Ventura and Xcode on a new-ish M1 MacBook Pro

First, the Assistant scrolls to some random part of the file and jumps back to that point after a minute. So if I have a large header and pop the cursor on line 10 in the Assistant, after a minute, it randomly scrolls to another part of the file instead of, well, just sitting there where I left the cursor. And if I scroll back, it auto scrolls away again after half a minute. (Feedback: 12007103).

And second, it "loses" the mapping between header and implementation. After a short while editing multiple code files and the assistant keeping up, it gives up the ghost and either goes blank, or insists the wrong header file is the correct counterpart. The menu option Reset Assistant Selection does not work, it just beeps. Somehow the compiler can still find the header, but the Assistant cannot. I have to restart Xcode. (Feedback: FB12029686)

The Assistant Editor has been a great innovation and a reliable companion for years. And Xcode a solid IDE. If anyone else is having these issues, please let Apple know. C++ is a core component of Xcode and it needs to work correctly for all of us.