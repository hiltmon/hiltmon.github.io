---
title: "Optimizing Short Form Writing for Developers"
date: 2022-08-22T12:20:09-04:00
draft: false
author: Hilton Lipschitz
tags: [ Writing ]
---

The vast majority of non-code writing performed by software engineers is **short form standard format**, defined here as:

- **Short Form**: A small amount of headings and text up to 1000 words
- **Standard Format**: The same standard structure or pattern of document repeated over and over again

Yet even though its short form and standard format, it takes too much time and effort to produce these, so we developers conveniently "forget" to create these valuable documents (or mess up structure of them).

I have found *my* way to optimize the creation of these so I can spin them up quickly, deliver the information needed correctly, send them out and get back to coding.

<!--more-->

## Short Form Standard Format

As developers, we write the same standard documents over and over again:

- [Statements of Work](https://hiltmon.com/blog/2016/03/05/minimal-project-management)
- Test Results
- Release Notes
- Meeting Notes
- Code Reviews
- Etc.

These documents usually do not contain a lot of text, but the content is valuable for communications, remembering things and structuring conversations.

We often try to avoid creating these documents because it's a hassle to set them up, remember (or figure out) the structure and content needed, write the actual prose and deliver them in the required format. Putting it all together and formatting it just takes too much time. We're coders, not writers, after all! We have better things to do.

So I have optimized the process of creating these to remove these hassles.

To create a new standard format, I use a mix of [Markdown](https://hiltmon.com/blog/2012/02/20/the-markdown-mindset/) and Text Expansion as follows:

- Launch my Markdown editor (which is usually running anyway)
- Expand a text template
- Fill in the necessary paragraphs
- Export to PDF (which automatically uses the standard format)
- Email it out

## Writing Tool

For short form especially, you do not want a heavy, slow writing environment, like a word processor or even an online tool. Instead, you want to focus on the content and to ignore the performance and formatting so you can bash it out quickly and move on.

I write all short form in Markdown, good old fashioned plain text with almost no distractions. I can focus on what I need to write up and not worry about look, feel, page layouts and the rest.

I find in plain text I can focus on the content, stream thoughts and spin up documents quickly.

But what to write?

## Templates

Since these are all standard form, I use [TextExpander](https://textexpander.com) snippets to store the structure needed, from Markdown meta data to content and even placing the cursor where I usually want to start typing.

With a template document, creating the deliverable because as easy as filling in a form. The headings tell me what I need to write where and what content is needed in this standard form.

For example, this is my Release Notes snippet:

{{< figure src="images/short-form-release-note.png" width=366 height=395 >}}

In [iA Writer](https://ia.net/writer), I simple type `;tocrn` and it expands to set the boilerplate for the document:

```
Kind: Release Notes  
Title: Release Notes  
Project:    
Author: Hilton Lipschitz  
Affiliation: Maritime Capital LP  
Web: http://www.maritimelp.com  
Date: 2022-08-22  
Version: 0.1 

# Release Notes 2022-08-22

## Highlights

- 

## Details

```

## Writing the Content

Now that the template is set up, I know what and where I need to create the content. So I can get to it. It's taken me seconds to get here and the structure of the document guides me in what I need to write.

And when it's done, how do I make it pretty and distribute it?

## Formatting the content

I have created a custom CSS template for our markdown documents that formats the text using the styles and fonts needed. And then set that up as the default for iA Writer.

When writing the content, I can switch to the preview window to confirm how it looks, often using the changed look to help me review and edit the content. And when I am done creating the content, export to PDF for release.

For example, here is the final Release Note:

{{< figure src="images/short-form-output.png" width=476 height=219 >}}

## Email it out

Oh, I leave this step up to you.

## Why Optimize?

I found I was spending too much time re-inventing each standard form document each time I needed to create one, and in trying to figure out what the content needed to be. Finally, after creating the document, I would have to go back and format it.

With a small investment in

- Creating the template expansions
- Creating the standard CSS output format

I find I can get into a short form standard format document in seconds, "know" exactly what needs to be written and can get it out the way. I can get it setup and into it lot faster without too much context switching. And I am more likely to produce the document than not.

Try it, optimize for short form, it may work for you too.