---
title: "Go to Where the Puck Is Going"
date: 2022-10-12T13:57:16-04:00
author: Hilton Lipschitz
tags: [ Thoughts, Writing ]
---

> "Go to where the puck is going, not where it has been". - Walter Gretzky (Wayne Gretzky's father)

Should we be building *new* product on existing, proven software stacks, or taking the challenge to start using the newer tools?  In this post, I take a high-level look at the technology landscape for commercial software development to aid in a thought exercise on how I would want to create new software products.

## Background

I have just left a role I spent 9 years in, building an asset management platform, using new — at the time — technologies, and that decision paid off. I have chosen to revisit and analyze my own technical skills and knowledge-bases to help decide what I would to do next given the choice, and with what?

That got me to thinking and questioning whether *I want* to build new product on proven, existing technologies, or take the challenge and use newer, but also proven, stacks.

Let's look at some of the landscape in 2022.

## Operating Systems

Ten, fifteen, twenty years ago, Microsoft's Windows was completely dominant. It owned the desktop market (and is still lead-dog there), and larger commercial organizations relied on it heavily for security, file sharing, applications and database servers (and many still do). If you wanted an audience for a product, Windows was the only platform to build for, everything else was niche.

These days, it's all different. Linus Torvalds' Linux is ubiquitous in server rooms and in the cloud, and has made significant gains on the desktop. And Apple's niche MacOs has taken a massive bite out of the user-chosen laptop and desktop space.

**It is where our users *are* that the most change has happened.**

Our users are nowadays on Mobile Phones, Tablets, Smart TVs, Personal Assistants, *personal* Laptops, and even car screens. Our users are comfortable and happy using these devices, actually prefer to use them, and, from a product maker's perspective, need to be just as productive away from their company supplied Windows desktop boat-anchors.

In servers, clearly the puck is on Linux and it seems to have slowed there. In user space, the puck is moving further away from the Windows Desktop towards a multi-device, ubiquitous anywhere native feeling front-end model. And I think this is where the opportunities abound, moving product functionality off the desktop and onto these devices to be used wherever, whenever and however the user wishes it.

## The Cloud

The cloud is no longer a mysterious thing in technology. The costs and benefits of the cloud are well known and understood, and the competitive landscape is tremendous. As evidence, just look at Azure and how Microsoft (the Windows everywhere company and will never change) has pivoted.

For big data, scaleable and reliable server work, the puck is showing that the cloud is best for smaller to larger sized installations, but at a certain massive scale or at high performance, it becomes cheaper to run your own goodies. The cloud vendors know this, and so encourage the use of their unique APIs to "lock" customers in. 

But the puck has moved beyond that and so should we. Containers and their management platforms are where the puck has moved towards, rendering the cloud as nothing more than a distributed data center to host these containers, and a service provider to these containers (for example data storage, database and redundancy). The container model has freed platforms from lock-in, maintained the simplicity of native application development, while still gaining the benefits of scalability and distribution.

Clearly the puck has bounced back to making new application's "plain old Linux" and hosting them in streamlined containers.  And when the product hits the performance limits of a container, the same code will happily run on a brace of containers, or on a rack of bare metal boxes.

## The Web as User Interface

The web is everywhere and on everything. Having a web interface to your product, a web site to market and support it, and a web-based community to discuss it are where the puck is today.

But that is not where the puck is going. Users want a new application to work natively on all their devices, delivering a touch interface on phones and tablets, voice interface on assistants, and native interface on laptops. And most importantly, they want it to work seamlessly with the features of the operating system and application ecosystem on those devices for sharing, automation and integration. Web interfaces do not have this capability and it holds users back.

It certainly is more work to build, service and support native front-ends for a new application, but that is where the users are, that is where the puck is going, and that is where new product needs to be.

## The Web as Integration

If your product is standalone and has no need to work with anything else on the internet, I am happy for you. But these days, a modern business uses a suite of online software products to manage and run their business, from source code control, to support tickets, finance and accounting, customer relations and other — non-core — needs. Critically, their core products need to integrate with this suite as well.

If you started a new company a decade ago, you would have to find a bunch of vendors to license software to you and then had to integrate them all yourself to run your business. Been there, done that, it was difficult and costly. These days, new companies simply sign up for a suite of independent cloud services and *expect* them to be seamlessly integrated, either natively or through a cloud-based integration service that they can add to their suite.

This is clearly where the puck is orbiting. A new product needs a web-based integration layer, with APIs for client and partner access and tooling or pre-built integrations to popular online services to make the integration invisible and easy for users to discover and implement.

## Open Source as Core

"Nobody gets fired for buying IBM". Not any more!

"Nobody gets fired for buying Microsoft". Not any more!

The choice between vendor product and *supported* open source product has been made by the puck. I am referring to the large, stable, open source projects that offer a paid-for support or are backed by very large organizations, not the hobbyist stuff. The cloud providers went with supported open source products, and in many cases, extended them. Sure, the decision was cost-based, but they have proven the reliability and stability of these technologies.

The traditional vendors have not sat back against this competition, ensuring their products run on Linux and cloud, even moving their core technology over (Microsoft and .Net Core is no longer Windows centric). But I believe that is more for existing customers to ease forced change and to try to stay relevant.

The puck is firmly sailing through the *supported* open source model and the plethora of products available is both unimaginable and leads to a difficult paradox of choice for users.

## Programming Languages

This may be the biggest decision yet. Do you build your product  using a vendor supplied language where there are plenty of affordable people that have the skills (C#, Java), but has a slower evolutionary path, or do you build it using the newer, smarter languages where only the passionate programmers reside and where much of the innovation is?

I believe this is where the puck experiences the most resistance. And in my experience, it's "much ado about nothing". Because the resistance is in resourcing, and the affordable programmers quickly follow where the work is.

If you have an *existing* product and the tooling you use is evolving to support Linux, the cloud, native interfaces, integration and open source access, then upgrade to the latest tooling and move forward. It offers short term gain and low implementation risk, but expect longer term to fall far behind where the puck is going and to be constrained in what you can create in the future. If the tooling is not evolving, best to get out now and kick off a rewrite (or even redesign).

But this thought exercise is about *new* product. For this, the newer languages are amazing and it is clear the puck is blasting towards them. Stable new-ish languages like Rust, Swift and even Go or TypeScript are where the innovation is, and where the failures and issues of other languages have been dealt with. Risen stars like Python, Haskell and JavaScript have peaked — even though they seem to be massively popular right now. New kids on the block like Kotlin and Dart are looking very promising (and are very well supported).

I would not choose tooling based on popularity. History has shown that only a few popular tools survive a decade or more without being eclipsed by something new and shiny. Look for languages that have strong ongoing support and a solid computer-science background, such as Rust with support from the Linux community, Swift from Apple, Kotlin from Google, and maybe TypeScript from Microsoft instead of .Net.

And if we choose these tools to build our new products, history has shown that the resources needed will follow.

## So what would I do?

Well, if I could, I would create *new* product:

- That runs on plain old Linux, the puck stopped here
- Can run locally on a development laptop, in a container on the cloud or on bare metal servers
- Has native user experiences for all our user's devices (using native platform tooling, design, conventions and integrations)
- Has APIs on the web to enable cheap integration and to partner with popular online products to pre-build and certify these integrations
- Is built using — and on top of - supported open source components
- And is written using several modern supported languages to ensure server ubiquity, future growth and native user interfaces

Based on this thought exercise, I would want to build new product where the puck is going, to take the challenge knowing that the industry will follow (and catch up).

If you could attack a new product development from scratch, what would you do?
