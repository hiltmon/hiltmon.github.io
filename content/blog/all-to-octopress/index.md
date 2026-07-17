---
title: "All to Octopress"
date: 2012-02-16T19:51:00-04:00
tags: [ Octopress ]
---

I have moved all of my sites over to [Octopress](https://github.com/octopress/octopress) by [Brandin Mathis](https://github.com/imathis). This means [hiltmon.com](https://hiltmon.com), [noverse.com](https://noverse.com) and shukaico.com are all on the same platform.

Why?

<!--more-->

* **Markdown everywhere:** I pretty much use [markdown](https://daringfireball.net/projects/markdown/), or really the [multi-markdown](http://fletcherpenney.net/multimarkdown/) variant, format for everything these days. I just love it. All files are just plain text so I never have to worry about vendor lock in (I still have some old Lotus Smartsuite files I cannot read), they are searchable and easy to maintain. All posts in [Octopress](https://github.com/octopress/octopress) are just plain markdown files.
* **Baked:** Unlike most other blogging systems, Octopress has no database, no server software to install, no dynamic caching needed and no need to configure the server. The web site is generated as plain old HTML files with a bit of Javascript. This means that user requests are just plain old HTML requests, requiring no processing on the server to serve, and leveraging the servers built in caches. It's the fastest way to serve a blog, and it can handle being *fireballed* (when you get linked to by [Daring Fireball](https://daringfireball.net/) and millions of geeks try to load your web at the same time).
* **It's ruby:** I do all my web work in [Ruby on Rails](https://rubyonrails.org/) or [Sinatra](http://www.sinatrarb.com/), so using the [mojombo/jekyll](https://github.com/mojombo/jekyll)
engine on my local machine just fits the bill. Tools like `rake` and formats like markdown just work for me.
* **I can hack it:** A few tweaks to the `rake` file and I have the `new_post` action logging to [DayOne](http://dayoneapp.com/) and opening [Byword](http://bywordapp.com/) with the new post.
* **Great, simple design:** I think [Brandin Mathis](https://github.com/imathis) did a great job on the default layout, fonts and color schemes. A lot of influential bloggers ([Matt Legend Gemmell](https://mattgemmell.com/), I'm looking at you) feel the same way. So I have pretty much left it alone.
* **Easy to set up:** Clone it from [GitHub](https://github.com/imathis/octopress), fill in a few fields, create a few files and generate. You have a site. Set up a few more fields and you can `rsync` it to the server without a hassle.

But I do miss a one thing though, I miss editing and maintaining my blog in MarsEdit. Oh, I know there are hacks and workarounds to manage an [Octopress](https://github.com/octopress/octopress) blog with it, but they are messy and leave my system feeling all dirty.

So thank you, [Brandin Mathis](https://github.com/imathis) and the [Octopress](https://github.com/octopress/octopress) team for a wonderful platform for us all to enjoy.
