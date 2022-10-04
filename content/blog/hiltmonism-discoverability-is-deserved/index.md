---
layout: hiltmonism
title: "Discoverability Is Deserved"
date: 2022-10-04T10:17:50-04:00
author: Hilton Lipschitz
tags: [ Hiltmonism ]
---

Discoverability is the user's ability to find key information, features, services and capabilities in a software application. It enables users to locate, see, learn and understand what capabilities the software provides.

If users cannot discover a capability, how will they know it exists in the application in the first place?

Designers and developers need to keep this in mind when architecting and structuring applications. They need to not only focus on what is being provided, and how users can use it, but also on how users can find it.

> **Aside**: Bloomberg terminal  
> The Bloomberg terminal, the black and orange windows you see in any financial news segment or on desk, is renowned for its mystical incantation interface. Users use special short-codes to access functions on these screens, for example `BTMM` to see the fixed income market rates, or `IRSB` to see a swap curve. Traders pride themselves in knowing the right incantations to get the right data they need, but for newbies, it's impossible to guess unless you know the Bloomberg name for something. Recently they have been trying to expose short-codes with bright yellow popups and a status bar hint, but most folks ignore this. This lack of discoverability used to be a feature of the product and a competitive advantage to older users, but it's a huge hindrance to the new generation.

Vendors of products with non-discoverable interfaces do offer manuals, online documents and one-one-one training to compensate for the non-discoverability. But this predicates on the user wanting to read the manual (never), go online and search for features (google it and hope a blog answers the question) or remember what happened in the rushed training they had ages ago. This problem too has a solution, namely repeated, iterative training, but users have jobs to do and will not tolerate too many training interruptions.

> **Aside**: Sublime, Visual Studio Code, even Nova  
> At some point, it was "decided" that the Command Palette pattern was the way to go for GUI text and code editors. I first came across it in Sublime Text, but it seems to be everywhere now. I get the reason, these products are plugin based, and plugins need a place to expose their features. But discovering what's in there amongst the hundreds of other lines of features is a mean feat. GUIs have menus, and the discoverable solution of allowing plugin developers to add to the menu system (and toolbars) is a proven model, so why do they not use it?

When accessing an application for the first time, users create their own cognitive model of the product. To create this model, they will explore the application looking for that which they need (or have someone show it to them). ***And then stop looking and start using it to do their work***. In their internal model then, the product has a certain set of capabilities, which they will then use, and be unaware of the rest. Over time, they may be shown additional features by peers and may add it to their model, or forget about it after one use.

If a product does expose its capabilities in a discoverable way, it does encourage users to try them out. Telling their peers that "I just found feature X, did you know the applications did that? How cool is that!" give them status and improves their productivity at the same time. If they find it on first use, even better.

> **Aside**: Microsoft Word  
> For those who have dived into this application, you will realize just how big and capable it is. And how little of it people use because they could not discover the its powers. I cannot remember where I heard this anecdote, it was decades ago, but it goes something like this. In an interview once, a Microsoft person was asked about why the preferences were set they way they were in Word. This, the representative answered, was a question asked internally before. No one knew, but for version after version, they copied the same preferences. In one edition, they even instrumented the preferences to see which ones were being changed by users so they could update the defaults. And got almost no data back, no-one changed the preferences. Users assumed the defaults were set by those who knew more (and that smells true), and Microsoft assumed users would discover the settings and features in Word though the preferences pane, which we now know to be false. I suspect that is why the command-bar that exposes Word features was created, it's way more discoverable.

It is this first exploration of the product that discoverability is key. The easier and more exposed the feature is, the more likely the user will add it to their cognitive model and use it. Even if they do not need the feature at the start, seeing it will imprint on[^1] the user, and be remembered.

So, when you are designing the architecture and the experience,  take the time to create a discoverable product, and test it with real people to see whether they can find the treasure you have created.

[^1]: Imprint On: To cause (a very young animal) to recognize and be attracted to another animal or to an object identified as the parent.
