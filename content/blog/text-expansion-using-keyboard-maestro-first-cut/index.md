---
title: "Text Expansion using Keyboard Maestro (First Cut)"
date: 2016-04-08 08:43:08 -0400

---

This post presents how I have set up [Keyboard Maestro](http://www.keyboardmaestro.com/main/) to replace basic text expansion from [TextExpander](https://smilesoftware.com/textexpander) ... so far. This post covers <span class="light">(More to follow at some point.)</span>:

* Basic text expansion
* When to use copy vs typing
* Limiting to applications
* Basic variables


{{< figure src="images/te-to-km-1.png" width=333 height=305 class="image-right" >}}

## Basic Text Expansion

The basic text expansion macro looks like the macro on the right.

* It is triggered when a string is typed, in this case `;gma`
* It has a single action, **Insert text by Typing**, containing the text to be typed, in this case `git pull; make clean; make -j 8`.

Thats all there is to it. Nice and simple.

Type `;gma` anywhere and Keyboard Maestro makes the replacement.

## Insert text by typing vs pasting

{{< figure src="images/te-to-km-8.png" width=333 height=341 class="image-right" >}}

Almost all the time, **Insert text by typing** is the right way to go. Its fast enough and does not affect the system clipboard. However, for long strings, typing may be too slow.

{{< figure src="images/te-to-km-2.gif" width=320 height=175 >}}

In these rare cases, **Insert text by pasting** is way faster. But you need to add another step to the macro. Add a **Set Clipboard to Past Clipboard** step after the paste to reset the clipboard back by 1 in Keyboard Maestro's history. <span class="light">(Thanks to [@TheBaronHimSelf](https://twitter.com/TheBaronHimself) for this tip.)</span>

{{< figure src="images/te-to-km-3.gif" width=320 height=83 >}}

## Limit To Application

Many of my snippets apply only to specific applications. To limit snippets to an application (or set of them), I create a new Group and make it available in a selected list of applications.

{{< figure src="images/te-to-km-4.png" width=617 height=250 >}}

The snippets in this group only expand in Xcode.

## Basic Variables

Keyboard Maestro has many of the same variables and abilities as TextExpander (and a whole bunch more, of course), including

{{< figure src="images/te-to-km-5.png" width=444 height=195 class="image-right" >}}

* Position Cursor after typing `%|%`
* The current clipboard `%CurrentClipboard%`

So, for example, to create a Markdown Link using a URL on the clipboard and place the caret (the text insertion cursor) in the description area, I can use my `;mml` macro.

```
[**CARET**]
(http://localhost:4000/blog/2016/04/08/text-expansion-using-keyboard-maestro-first-cut/)
```


{{< figure src="images/te-to-km-6.png" width=381 height=304 class="image-right" >}}


Or to create a date heading in an Assembly Note, I can use my `;mmd` macro.

This types:

	---
	
	**2016-04-08**
soul
	
You can format the date any way you like, of course.

{{< figure src="images/te-to-km-7.png" width=247 height=262 class="image-right" >}}

To see what variables are available, click the **Insert Token** dropdown on the right of the action panel. As you can see, there is a huge number available.

I have managed to replace the majority of my TextExpander snippets using the basic text expansion macro described here, and it's working great.

<span class="light">Next to do these with sounds and with more advanced abilities.</span>

Hope this helps.

*Follow the author as [@hiltmon](https://twitter.com/hiltmon) on Twitter.*
