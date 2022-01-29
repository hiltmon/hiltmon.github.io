---
title: "Eliminating Google Analytics Referral Spam"
date: 2015-01-18 10:42:51 -0500
tags: 
---

{{< figure src="images/google-analytics.png" width=100 height=101 class="image-right" >}}

It seems that the [Google Analytics](http://www.google.com/analytics/) use of a public tracking code was a mistake. Anyone can use your tracking code on their site, which adds to your traffic, or they can create ghost visits and spam referrals by hammering Google Analytics with your code *while never visiting your site*. Oh, and the codes are easy to guess, so they do not even need to know about your site.

In most cases, this is perfectly harmless (<abbr title="In Mu Humble Opinion">IMHO</abbr>) as only Google Analytics data is affected and your reports look funny. Your ad stats, *if not Google*, remain the same as they are independent.

The only reason I am talking about this is because I was up early this morning and noticed that a page with the title of "Luck" was trending in my analytics[^1].

{{< figure src="images/google-analytics-luck.png" width=300 height=153 class="left-right" >}}

Except for one problem.

**There is no post entitled "Luck"**.

I never wrote one.

Ever!

{{< figure src="images/google-analytics-hostname.png" width=310 height=230 class="image-right" >}}

Which led me down the rabbit hole.

You can spot these fake referrals pretty easily. Go to **Reporting** / **Acquisition** / **Referrals** on the Google Analytics site. Then, next to **Primary Dimension**, select **Other** / **Behavior** / **Hostname**:

My site is **hiltmon.com**, who the blazes is that?

<span class="light">*Whatever you do, please do **not** visit that URL.*</span>

Michael Sullivan ([@AnalyticsEdge](http://twitter.com/AnalyticsEdge)) from Analytics Edge wrote two excellent posts recently on what these are and how to deal with this referral spam:

* [Removing Referral Spam from Google Analytics](http://www.analyticsedge.com/2014/12/removing-referral-spam-google-analytics/)
* [Advanced Segment to Eliminate Spam Referrals](http://www.analyticsedge.com/2015/01/advanced-segment-eliminate-spam-referrals/)

Go ahead, read them.

I have updated my Google Analytics filters and am waiting to see if the changes work. I have also created the segment as directed and that seems to work great, but only for some reports.

*Follow the author as [@hiltmon](https://twitter.com/hiltmon) on Twitter.*

[^1]: Still running [Status Board](https://panic.com/statusboard/) by the seriously handsome folks at [Panic](https://panic.com) on the original iPad.
