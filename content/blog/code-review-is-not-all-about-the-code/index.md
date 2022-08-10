---
title: "Code Review is not all about the Code"
date: 2022-08-10T12:12:49-04:00
draft: false
author: Hilton Lipschitz
---

We all understand the benefits of the code review process in reducing the risk of software issues making it out into the wild, and in improving the skills of developers. Frequently though, the code review focusses wholly on the code and on an eyeball search for potential bugs and no more. There is a better way.

As developers, we read and write code all day, it's our superpower and wholly inside our comfort zone. So it's easy and convenient for us to jump straight into reading the code and poking around for bugs. As a result, we miss out on the true objectives of the review process, and on the true benefits that it should yield. In reality, a huge amount of time is wasted on reading, analyzing and understanding code that will likely be thrown away.

From my perspective, the code look is only the latter third of the process. The review process should always start with the business as first third, then look at the structure and architecture, and finally at the code itself.

{{< figure src="images/Code-Review-Percentages.png" width=505 height=257 >}}

## Business

Let's look at each part, starting with the business.

Code should be written to achieve certain business goals, to created needed functionality, or to solve a business problem. If the code under review does less (or more) than that, the review should stop there. There is no point spending reviewer hours on looking at code that will not be used because it does not match requirements.

So a reviewer always needs to start with the business context: Why was this code created? Who asked for it? Who approved it? Where are the requirements or designs (if any)? Where are the measures to be used to prove that the code is business correct? The reviewer should never go into a code review without having *and understanding* this big picture context. 

With this business knowledge, they can start to review whether or not the code is worth a more detailed look. In review, let the developer present what the code does at a business or functional level, what its inputs and outputs are (with evidence) and what the test case results look like. The reviewer should have enough context to understand whether the code meets or misses expected specifications, and could challenge the developer on requirements interpretations and missing functionality (or extra functionality - as in "why did they spend time working on code that was not even asked for?").

If the code does not meet the business requirements, there is no point in doing more work or spending more review time.

If it does, the first third is complete.

## Architecture

The next part of review is to look at the structure and architecture used.

Most applications have patterns and standards that need to be met to make the code more navigable, readable and maintainable. We're not yet looking at the content of the code files, we're looking at their existence, naming, locations and adherence to architectural decisions.

For example, your application may use libraries for plugins, so this code should do that. Or it could be architected in a certain folder structure, so this code should follow that (see Ruby on Rails for example). Or you may mandate a pattern of initialize, process and close down, which means this code should be the same.

If the code is structured and written to a different pattern or architecture, it's harder to read and maintain, and creates cognitive dissonance in users. Having multiple architectures in a system creates insurmountable tech debt and makes maintenance and extension more difficult.

There is only one case where a new architecture should pass a code review, and that is when you are refactoring an existing system to a new architecture.

So if the code does not match the architecture of the bigger system, even if it works from a business perspective, its best to stop there and have the developer migrate it to the correct patterns. That leads to readability and maintainability benefits downstream and makes it easier to drill into the actual code at the next review. If the reviewer had gone straight to the code, they would have reviewed code that needed to be thrown away.

And now the second third is complete.

## Code Review

Finally, when the business and architecture thirds are both completed and passed, its time to get to the bit we're all good at ... actual code review, the third where we spend the time and actually read the code itself.

This latter third is the when we reviewers get to test standards compliance, DRY, SOLID, patterns and other file content requirements. Now is the time to look for bad naming, odd structures, risky code, performance issues, etc. Now is the time to challenge the developer on why they wrote things a certain way.

As a mighty benefit, and given that the business needs are now well known to the reviewer, they can also focus the review on code and issues that are important (instead of just hammering everything). For example, finding slow code in an application that runs overnight without a deadline should not fail code review, but finding slow code in a real-time application should. Finding threading issues in single threaded code should not be a stopper. Finding unreadable code should. Finding cases where failures are not checked for should. Finding code that fails language or coding standards should. The business and architecture context ensures that the code review itself does not look for, nor spend time on, nor try to change, that which is unnecessary.

---

Code review is all about reducing software risks, improving programmer skills and delivering readable and maintainable code to specifications. By spending time on the business and architectural thirds, a lot of time that is wasted on looking at lines of code can be spared until the code its actually ready for it.

*Follow the author as [@hiltmon](https://twitter.com/hiltmon) on Twitter*
