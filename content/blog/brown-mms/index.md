---
title: "Brown M&Ms: A Quick Way to Determine Code Quality"
date: 2015-10-14 19:31:20 -0400
tags: 
---

{{< figure src="images/vanhalenmm.png" width=320 height=320 class="image-right" >}}

My business runs on code. Every day, my team and I deploy new systems, patches and add new features to our mission-critical code base. And we rarely have a problem.

That's because we have a quick way to determine if the programmer attended to the details of the product and code, and whether we then need to hold the deploy for a deeper check and test or can run a lighter test and confidently push it out.

We run a quick quality check.

We look for the presence of *brown M&Ms*.

{{< figure src="images/vanhalen.png" width=320 height=196 class="image-right" >}}

Back in the day, the legendary band [Van Halen](http://www.van-halen.com) put on complex live shows involving lots of equipment, lighting and expensive sensitive sound equipment. The setup for the show was documented in great detail in their standard concert contract which dictated what the venue needed to do to set up and run a Van Halen Concert.

{{< figure src="images/vanhalenrider.jpg" width=477 height=144 class="image-right" >}}

One of the more unusual requests, under the "Munchies" section hidden in the middle of the contract, was a line requesting a bowl of M&M's with the brown ones removed.

One would assume that they were just being prima-donna rock stars in requiring each venue to task a person to remove the brown M&Ms from the bowl.

But that was not the intent.

This requirement served a very practical purpose: **to provide a simple way of determining whether the technical specifications of the contract had been thoroughly read and complied with**.

In short, if there was a bowl of M&Ms with the brown ones removed, chances are the venue had read all the details of the contract, followed them all and had set up the concert properly and correctly. If not, Van Halen knew to run a detailed check, line by line, to find out what the venue had failed to set up properly and could put the concert at risk. Empirically, they usually found problems when the M&Ms requirement was not met, and rarely found problems when the bowl was properly prepared.

In our case, we don't ask programmers to provide bowls of chocolate <span class="light">(although that would make me a lot happier)</span>. Instead, one of their requirements is to code to our quite *capricious* coding standards, where tech arguments on spacing, naming and formatting have been, in many cases, arbitrarily decided. You may not like our standards. *Heck, even I don't agree with parts of them and I designed them.* They are there to help the team read each-others' code, and also there as our [coal-mine canary](https://en.wiktionary.org/wiki/canary_in_a_coal_mine).

When new code is delivered to us, the first thing we do is scan it for standards compliance. We can see, at a glance, if the code is to standard or not: are the headers present, are the files named correctly, is the spacing and layout right and does the code look 'clean'. So, if the programmer has *not* followed the coding standards, we know to drill further. If they have followed the standards to the letter, chances are the code is better.

**The programmer who takes the time to code to all our needs (the standards being just one) is more likely to have thought through the code, structured and tested it properly and produced a more reliable and maintainable product.** If a programmer has been lazy, copy/pasted code and ignored the coding standard, its more likely that they have not fully examined the problem space, designed an elegant solution, tested it and made it maintainable.

*Its all about attention to detail.* If the code layout detail has been adhered to, so too have all the other details.

We've seen this time and time again. Code to standard is usually more reliable and correct. And because of that, adherence to standards has become our bowl of M&Ms test.

To be clear, we do not just take the pretty code and push it out. Code still gets reviewed, tested, challenged and examined before it goes out to run the business. If the attention to detail was applied to standardizing the code, then the likelihood of the same level of attention being paid to the functionality and feature set of the code is very high. 

{{< figure src="images/vanhalenbrown.png" width=270 height=192 class="image-right" >}}

Empirically, we see fewer bugs and problems, have an easier time in review, better tests run with better coverage, and maintenance by the team is easier.

Code written to our standards is our brown M&M check, our way to get a quick feel for the quality of work we're dealing with.

Ironically, I am one of the few people who actually likes the brown M&Ms. Feel free to remove the blue ones from my bowl.

*Follow the author as [@hiltmon](https://twitter.com/hiltmon) on Twitter.*
