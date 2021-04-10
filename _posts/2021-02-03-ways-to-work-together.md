---
layout: post
title:  "Four Ways To Work Together"
date:   2021-02-03 21:30:00 -0800
tags: culture mental-models
---
As I've grown more senior, I've become more aware of the _leverage_ of things that I do. There's one flavor of this that I love: people leverage.

## People Leverage
People leverage helps us provide outsized gains to the organization by working with other people. This is a fundamental shift for us as engineers, since this is no longer about us and our work, or even how other people affect that work. It is about expanding the scope of our work to include other people, and about working _through_ them to achieve great things.

Don’t take my word for it - have a read through the [Staff Eng Stories][staff-eng] and notice how every story of more senior engineering roles involves working with, and through other people. Our bias for engineering means that the large technical problem jumps out at us; look closely though and you'll notice that across every technical problem the common thread is learning how to work with people.

There are two broad ways in which you can build people leverage - you can build up people directly, or you can build them up indirectly by making their job easier. This post is about the former.

## Direct Leverage
When working with people directly, my go-to resource is a mental model I learned from [High Output Management][high-output]. I’ve adapted it slightly, and call it _Pair/Direct/Delegate/Mentor_ (aside: my teammates will attest to my imaginative naming.)

**Pair** with a colleague to help them learn skills or best practices by osmosis. This is extremely useful when there’s a lot of stuff to communicate, and the colleague is new to an area we are quite familiar with. Instead of them doing the work and then providing bucket loads of feedback, we can do the work together<sup>*</sup>. Active pairing is when we’re doing the work and the colleague is observing and commenting; shadowing or passive pairing is when these roles are flipped.

> "Since you've not worked on that repo before, let's pair on that first ticket. It builds multiple images, so there are some uniquely tricky bits floating around."
> 
> "Could you let me ride along while you work on this task? I'd like to learn how you use snapshot versions of our libraries to test this out."

<sup>_*This notion of pairing is related to but different from [Pair Programming][pairprog]. This "Pair" could be considered a superset: while we're pairing up on the task, there is primarily one way that we expect learning to transfer._</sup>

**Direct** a colleague when they have the skills required to do a complex task, but may not have experience in navigating the complexity and understanding the pieces that go into it. This complexity may be in the task itself, or in the lifecycle of the task like requirement gathering, stakeholder management, release engineering, etc.

> "I've added a lot of detail to that ticket. Apart from the acceptance criteria we discussed, it includes link to code that needs to be altered and some things to watch out for."
> 
> "I've not released breaking changes to libraries too often. Do you mind adding exact steps detailing how you would release this new data model?"

**Delegate** to a colleague when they have the skills required to break down and complete a complex task, given only the requirements and constraints. Typically, this is 90% of the actual work that follows the initial 10% where we would work with stakeholders and the project itself to identify the boundaries of the solution, and a handful of considerations. Depending on the colleague, the boundaries and considerations can be firm, or just suggestions on what to consider.

> "I've worked with Alan to get the list of requirements that we discussed, especially around expected turnaround times for the uploads. Do you think you have enough to break this down and implement it?"
> 
> "I'd like to take on this story, but I would need some help understanding the first couple of use-cases better. If we can quickly sync on that, I can then drive this forward."

**Mentor** a colleague when they are able to see a task through the entire lifecycle, and may need some guidance at key points on what to focus on, or how to approach the problem. Here, the colleague reaches out for help when they need it. We make ourselves available, and at most observe the task non-judgmentally to know what questions to ask or provide perspective when they do reach out. In rare cases, we might pull them into a 1:1 to provide guidance.

> "How do you think that meeting with the vendor went?"
> 
> "Could we chat sometime tomorrow to debrief this meeting? I'm not sure I understand what we spoke about, or why the meeting took that direction."

## Degree of Leverage
The techniques clearly move from the most time investment (Pair) to the least (Mentor), so it's tempting to assume that we ought to jump to latter whenever possible. However, that would be a false economy: unless the technique is matched to our colleague's needs, the time invested isn't useful.

In other words, jumping to _mentor_ people all the time because that helps us scale better isn't effective. We'll need to be aware of all these possible techniques and deploy the right tool for the job for maximum impact. So, how do we know which of these techniques to use?

## Task Relevant Maturity: the missing piece
Despite the usual connotations of _Direct_ and _Delegate_, it isn’t organizational hierarchy that dictates which technique to use with a colleague. Instead, it is a concept called Task Relevant Maturity [1][trm-1] [2][trm-2]; this encourages us to use a colleague's _prior experience_ working on similar tasks as a heuristic for how self-driven they can be on a new one.

**tl;dr:** we need to be curious enough about our colleague to understand their ability as it pertains to a specific task: we don't rely on their title, seniority, or general excellence. This also necessarily means that we know enough about the task to understand what skills it requires and where the pitfalls lie, and how it maps to our colleague.

## Summary
As we grow into senior technical leaders, learning how high/low touch to work with people is key to building leverage. By matching our colleagues' capabilities and experience to the task at hand, we can choose the level of support we provide; this gives us better returns on our time investment, and gives them the space to learn and grow.

<!-- References -->
[staff-eng]: https://staffeng.com/stories/
[high-output]: https://www.amazon.com/High-Output-Management-Andrew-Grove/dp/0679762884
[pairprog]: http://www.extremeprogramming.org/rules/pair.html
[trm-1]: https://getlighthouse.com/blog/management-concept/
[trm-2]: https://medium.com/@ameet/task-relevant-maturity-aff122fb535f

