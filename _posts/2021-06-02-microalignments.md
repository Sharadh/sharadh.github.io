---
layout: post
title:  Microalignments
date:   2021-06-02 16:50:00 -0700
tags: technical collaboration
---
A key part of [Staff+][staffeng] engineering roles is to build alignment. I call my approach to doing this "microalignment"; enough people have recently said it's a great word for what we do, so I'm going to write about it here.

## tl;dr
* Alignment is the integration of two teams' ideas
* Like any integration, [waterfall] is a terribly inefficient way to do it; be intentional and add structure to align early and often
* When this works well, you won't even notice how useful this is

## Alignment
First, a note about alignment.

We've been reading Will Larson's [Staff Engineer][staffeng] book at work, and there's a specific line that captures my role as a Staff+ engineer perfectly:
> Staff-plus roles are leadership roles, and in leadership roles, the support system that got you here will fade away. **Often abruptly, you're now expected to align the pieces around you for your own success.**
> - [Staying aligned with Authority][staffeng-aligned]

So in essence, here's how alignment works for an engineer:
* **<=Staff**: there isn't much alignment to worry about. My manager, product manager (PM), or technical program manager (TPM) - what do they _all_ do the entire day, anyway? - need to know when something isn't quite what we expected during Planning.
* **>=Staff**: I'm 99% sure the team can get the work done. How do I make sure I'm not wasting their time, and we work on the right things and have things to work on? I better talk to my manager, PM, or TPM (they're probably thinking about the same thing.)

Here's the rub: as (often) the most senior Engineer, I'm expected to (a) understand the key details of what the team is doing; (b) understand the implications of these on **the context** we operate in; and (c) escalate appropriately when _something is off._ 

### The Context
The context is subjective, and can include any of the following:
* Architectural choices the organization is moving towards
* Recent site reliability issues in the domain of the team's work
* Roadmap or personnel changes on partner teams
* Staffing and morale on partner teams
* Concerns that don't quite fall neatly on any of the teams in question
* ...

In larger organizations, the context is narrower (e.g the Tech Lead only focuses on architectural choices and reliability), while in smaller organizations, the context is broader.

## Building Alignment
I lied a little in the previous section. My job, really, isn't as much about _escalating_ when something is misaligned as much as it is to _solve it_: escalation is one (usually expensive) strategy to do so.

Escalation is undesirable for two reasons:

1. It incurs management overhead: getting teams to align is meta-work, and is basically a cost of doing business. By engaging the management structure, we pull in folks away from the actual work, ramp them up, get them to make a decision, and then help them communicate their will out to the teams doing the work.
2. It is psychologically expensive: instead of having the feeling of "figuring it out", we end up having one winner at best, and often two losers who both feel incapable of owning their own fate.

The more insidious part of escalation is that when it becomes the go-to approach, teams forget how to work without it. When _that_ happens, the senior engineers involved - and this is where you and I come in - just don't scale. Engineers usually outnumber the folks in the "management structure", so every decision has a bottleneck. Consequently, senior ICs hit a wall and get incredibly frustrated that they just can't create the impact they want.

## What are we Aligning?
I want to take a step back at this point and examine this thing called "alignment". What is it that we're aligning?

Conventional answers to this include: we're aligning roadmaps, we're pointing in the same direction, we're agreeing on what to do next, etc. I think these are useful snapshots of what alignment looks like at different times, but are just artifacts of being aligned. I think what we're actually aligning is our ideas of what work looks like.

Any team is a team because of strong internal bonds; these same bonds that let the team work well together mean that information bubbles - and more importantly, **idea bubbles** - start to develop. Multiple teams working on the same project have their own idea of what the project is, what their scope is, and how to achieve it. Alignment is the _integration_ of these smaller idea bubbles into a larger idea bubble, the project.

## Waterfall doesn't work
Cross team projects typically follow a standard way of integrating these ideas:

1. We brainstorm and figure out dependencies; we then work with different teams, get capacity, and table the work each team needs to get done.
2. We go away and do the work. Every now and then, we get status updates (typically via TPM) about how the work is going.
3. When the Jira tickets align, combinations of teams integrate the work with each other.

This seems completely reasonable at first glance. However, my assertion is that this is essentially a waterfall approach to software development, and it isn't very effective.

The crux of it lies in Step (2), when we go away and do the work. When projects have ambiguity, it's easy for each team to make tiny assumptions as they solve their own piece. Over time the meaning of the tickets that were broken down changes subtly. Sure, you can have really detailed and strict _acceptance criteria_ - and at that point, you're removing doubt by doubling down on requirements gathering, which is more waterfall-y.

### Doesn't Scrum Solve this?
At this point you may be thinking, _"Man, this guy really doesn't get Agile! If they were doing it right, none of this would happen."_

Yes, and no.

[Agile says][agile-manifesto]:

* Working software over comprehensive documentation
* Customer collaboration over contract negotiation

Scrum commonly interprets this as:

* Ship working code at every milestone
* Have a cross functional team so there aren't large integrations

The wrinkle is when organizations grow large enough that there emerge specialized "horizontal" or "platform" teams. Good examples are DevOps (or, Production Engineering if you include the tools teams), Data Engineering, various Data Platform teams, etc. There's value in having them be horizontals - shared best practices, a manager that gets them and their career aspirations, etc. Scattering them across customer-facing teams may work for the project but often doesn't for the codebase, or the individuals.

### Doesn't Scrum of Scrums Solve this?
At this point you may be thinking, _"Man, this guy really doesn't get Agile at scale! If they were doing Scrum of Scrums, none of this would happen."_

Yes, and no.

Scrum of Scrums encourages these ["virtual teams"][scrum-scrums] to follow the same Scrum processes as development teams. That works for some cases, but especially when there are some smaller horizontal teams that have a small part to play but spread across many projects, the overhead becomes pretty intense. In my experience doing this (and watching others), there develops real frustration at being in various scrum ceremonies one after another for a small contribution or just to "be informed".

### Mindset Change
At these points, when I'm tempted to evolve the process to be more sophisticated to combat this, I remember another key part of the Agile manifesto:

* Individuals and interactions over processes and tools
...and the longer ones from [the principles][agile-principles]:

> Build projects around motivated individuals. Give them the environment and support they need, and trust them to get the job done.
> The most efficient and effective method of conveying information to and within a development team is face-to-face conversation.

I think there's a simpler way: instead of relying on stronger process, get cross team partners into a (slack) room together, tell them it's their responsibility to be on the same page as they work on things, and leave them to it. Instead of applying structure to developers, and in the process subtly absolving them of the responsibility to collaborate effectively, I think the more appropriate approach is to give them the responsibility but empower them with techniques that help.

That (finally) brings us to microalignment.

## How to Microalign
There are two key principles to enable microalignment: _overcommunicate_, and _async_

Overcommunication ensures that we keep people in the loop even when there's nothing contentious. Just like regular Scrum, there's steady stream of seemingly minor updates: _"We thought we could use the shared library, but not quite, so we're building our own."_, _"Had some trouble testing, so it'll be a day delayed."_ The idea is to create enough ambient feedback loops so that we increase the chances of catching something we didn't think was important, or that when something does come up the cross-functional team has enough muscle memory to raise it to each other in an easy way.

Async communication is a necessary corollary to overcommunication to prevent burnout. Engineers just won't communicate if the cost of doing it is high - they'd rather wait for something to "become an issue" that "deserves that level of communication". This is why _any_ async medium will do: email, wiki pages, Slack, etc. On top of that, there are a few templates to communicate through:

* Re: ticket JIRA-123, just wanted to let you know we're on track and a draft PR is up. You can see it [here][example]
* Heads up: we just merged [this change][example] that addresses the problems we discussed in our last sync. Please let me know how it works!
* I just realized when working on JIRA-123 that we haven't agreed on the cadence of data updates. I don't know if this is important, but [here's][example] what I've assumed - let me know if anyone has comments.

In all cases, there's a fairly informal _and short_ update which is easily parsed. Folks who need more info have a way to get it, and the message itself is a good place for any more discussion.

### Does it Work?
Measuring success for micro-alignment - like with all good process - is difficult. It tends to solve problems before they become large; this means it's not visible in the way of a late-project all-nighter to integrate two systems. The success will be at a macro level: complex cross-team projects will ship more on time, and the people involved will be happier working on them. This means that for technical leaders, part of implementing this change is to draw attention to the minor stuff that _do_ get raised - while focusing on long term actual outcomes.

## Summary
In this post, I wrote about my approach to building alignment, which is perhaps the most important part of my job. I like to apply Agile techniques in collaboration, and this leads to recurring "microalignments". This technique helps me scale, and also helps the organization build [connective tissue][updates].

<!-- References -->
[staffeng]: https://staffeng.com/
[waterfall]: https://en.wikipedia.org/wiki/Waterfall_model
[staffeng-aligned]: https://staffeng.com/guides/staying-aligned-with-authority
[updates]: https://lethain.com/weekly-updates/
[agile-manifesto]: https://agilemanifesto.org/
[scrum-scrums]: https://www.atlassian.com/agile/scrum/scrum-of-scrums
[agile-principles]: https://agilemanifesto.org/principles.html
[example]: https://www.example.com
