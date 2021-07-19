---
layout: post
title:  Microalignments
date:   2021-07-17 08:50:00 -0700
tags: technical collaboration
---
A key part of [Staff+][staffeng] engineering roles is to build alignment. I call my approach to doing this "microalignment". Many people have recently said it's a great word for what we do, so I'm going to write about it here.

## tl;dr
* Alignment is the integration of two teams' ideas
* Like any integration, [waterfall] is a terribly inefficient way to do it; be intentional and add structure to align early and often
* When this works well, you won't even notice how useful this is

## What are we Aligning?
We hear this word "alignment" a whole lot as part of day to day work, so I want to take a step back and look at it. What is it that we're aligning?

Conventional answers to this include: we're aligning roadmaps, we're pointing in the same direction, we're agreeing on what to do next, etc. I think these are useful snapshots of what alignment looks like at different times, but are just artifacts of being aligned. What we're actually aligning is our **ideas** of what the work is.

Said differently: if we agree on our idea - our mental model - of the work, then these other things like the roadmap or various backlogs will follow. There's definitely effort required to pay attention, dot the i's, and cross the t's; that said, things mostly just work.

## Idea Drift
Any team is a team because of strong internal bonds; these same bonds that let the team work well together mean that information bubbles - and more importantly, **idea bubbles** - start to develop. It's _really difficult_ for folks within the team to realize that they've interpreted a little ambiguity in the plan in a way that's notably different! In the process of interpretation, they've all agreed on one thing, and now that thing is obvious to them.

So in this way, multiple teams working on the same project have their own idea of what the project is, what _their_ scope is, and how to achieve it. They may have had a shared understanding to begin with, and over time there's idea drift that happens.

When I think of alignment, I think of the _integration_ of these smaller idea bubbles into a larger one - a shared understanding of the project.

## Status Quo
On a generic team that follows an agile methodology, we tend try and ensure alignment on cross team projects with a standard process:

1. We brainstorm and figure out dependencies; we then work with different teams, get capacity, and table the work each team needs to get done.
2. We go away and do the work. Every now and then, we get status updates (typically via a technical program manager, or TPM) about how the work is going.
3. When the Jira tickets align, combinations of teams integrate the work with each other.

This seems completely reasonable at first glance. However, my assertion is that this is essentially a waterfall approach to software development, and that it isn't very effective.

The crux of it lies in Step (2), when we go away and do the work. That's when different teams drift apart.

If you're wondering, _"Wait, what? This isn't a problem for us at all!"_, it's possible your org is not at a size where this is a problem, or you're solving it with one of the alternatives below. [Have a look](#alternatives)! If it's the former, this article will be of little use to you. Also, I envy you a little bit: there's a lot of joy in a smaller and more nimble org. Enjoy it!

## How to Microalign
There are two key principles to enable microalignment: _overcommunicate_, and _do it async._

**Overcommunication** ensures that we keep people in the loop even when there's nothing contentious. Just like regular Scrum, there's steady stream of seemingly minor updates: _"We thought we could use the shared library, but not quite, so we're building our own client."_, _"Had some trouble testing, so it'll be a day delayed."_ The idea is to create enough ambient feedback loops so that we increase the chances of catching something we didn't think was important, or that when something does come up the larger team can _easily_ raise and examine it.

**Doing it async** is a necessary corollary to overcommunication to prevent burnout. Engineers just won't communicate if the cost of doing it is high - they'd rather wait for something to _"become an issue that deserves that level of communication"_. What they're actually saying, of course, is: _"It's painful to schedule a meeting to deal with this small thing. I'll note my assumptions and keep moving on."_. This is why _any_ async medium will do: email, wiki pages, Slack, etc.

These two principles lead to micro-communications; here are a few effective examples:

* _"Re: ticket JIRA-123, just wanted to let you know we're on track and a draft PR is up. You can see it [here][example]."_
* _"Heads up: we just merged [this change][example] that addresses the problems we discussed in our last sync. Please let me know how it works!"_
* _"I just realized when working on JIRA-123 that we haven't agreed on the cadence of data updates. I don't know if this is important, but [here's][example] what I've assumed - let me know if anyone has comments."_

In all cases, there's a fairly informal _and short_ update which is easily parsed. Folks who need more info have a way to get it, and the message itself is a good place for any more discussion. If you're a tech lead or senior IC who wants to try this out:

1. Establish an async medium for the project. My favorite is a shared Slack channel.
2. Establish a stream of updates to that medium, and encourage your team to do the same.
3. When your team wonders if this is spammy, encourage them to make the updates more succinct and to include links to more context. Guide them away from larger and less frequent updates, and towards smaller and more frequent ones.

### Does it Work?
Measuring success for micro-alignment - like with all good process - is difficult. It tends to solve problems before they become large; this means it's not visible in same way a late-project all-nighter to integrate two systems is. The success will be at a macro level: complex cross-team projects will ship more on time, and the people involved will be happier working on them. This means that for technical leaders, part of implementing this change is to draw attention to the minor issues that _do_ get raised - while focusing on long term actual outcomes.

## Alternatives

### Don't well detailed tickets solve this?
We identified that the root cause of idea drift is the ambiguity in the work, which means that over time the meaning of the tickets that were broken down changes subtly. One knee-jerk reaction to this is to insist on really detailed and strict acceptance criteria. Effectively, we could try and remove doubt by doubling down on requirements gathering or up-front breakdown.

In my experience, unless the breakdown involves actually zooming in and mapping out the work to be done in the context of the project it needs to be done in, there will always be ambiguity. As a colleague once put it:
> I feel like that level of rigor makes me implement the task twice - once in text when I write the ticket up, and once in code for realz.

This makes the development process a bit more waterfall-y: there's a lot more resistance to changes to the implementation plan because of the effort put into it already. It may look like less "extra stuff" for the team to do (that's engineer speak for "speaking to other people"), but the team's execution becomes less nimble.

### Doesn't Scrum Solve this?
At this point you may be thinking, _"Man, this guy really doesn't get Agile! If they were doing it right, none of this would happen."_

Yes, and no.

[Agile says][agile-manifesto]:

* Working software over comprehensive documentation
* Customer collaboration over contract negotiation

Scrum commonly interprets this as:

* Ship working code at every milestone
* Have a cross functional team so there aren't large integrations

The wrinkle is when organizations grow large enough that there emerge specialized "horizontal" or "platform" teams. Good examples are DevOps (or more generally, Infrastructure), Data Engineering, various Data Platform teams, etc. Before you say, _"There's your problem right there!"_ - there's value in having them be horizontals. This pattern keep evolving because it's useful for a host of things, like shared best practices, a team engineers identify with, a manager that gets them and their career aspirations, etc. Scattering the engineers across customer-facing teams may work for the project but often doesn't for the codebase, or the individuals.

### Doesn't Scrum of Scrums Solve this?
There is a popular evolution (or interpretation?) of Scrum, called [Scrum of Scrums][scrum-scrums]. It advocates for "virtual teams" that cross team boundaries, and encourages these to follow the same Scrum processes as development teams.

This works for some cases, but tends to break down when many _small_, horizontal teams are involved. These teams tend to have a small part to play across many projects, and the overhead becomes pretty intense. In my experience doing this (and watching others), engineers develop acute frustration at being in various scrum ceremonies one after another for a small contribution, or just to "be informed".

### Mindset Change
While it's tempting to evolve the Scrum process to be more sophisticated to combat this, I think there's a simpler way. Going back to another key part of the Agile manifesto:

* Individuals and interactions over processes and tools

...and the longer ones from [the principles][agile-principles]:

> Build projects around motivated individuals. Give them the environment and support they need, and trust them to get the job done.
> The most efficient and effective method of conveying information to and within a development team is face-to-face conversation.

Instead of relying on stronger process, let's get cross team partners into a (slack) room together, tell them it's their responsibility to be on the same page as they work on things, and leave them to it. When we apply too much structure to software development, we risk subtly absolving developers of the responsibility to collaborate effectively.  I think the more appropriate approach is to give them the responsibility but empower them with techniques that help.

Zooming out, I think this is a good example of one of my guiding principles: _put the pain where it belongs_. Who owns the scrum of scrums? Typically, the TPM does - and on that person falls the responsibility of knowing what every engineer is _actually_ doing, translating across teams, and aligning ideas. When the TPM owns collaboration, the engineers don't have skin in the game and don't feel the pain of a lack of collaboration muscle. They never need to get better at popping idea bubbles, and the organization compensates for this by investing even more resources.

## Summary
In this post, I wrote about my approach to building alignment, which is perhaps the most important part of my job. I like to apply Agile techniques in collaboration, and this leads to frequent microalignments. This technique helps me scale, and also helps the organization build [connective tissue][updates].

<!-- References -->
[staffeng]: https://staffeng.com/
[waterfall]: https://en.wikipedia.org/wiki/Waterfall_model
[updates]: https://lethain.com/weekly-updates/
[agile-manifesto]: https://agilemanifesto.org/
[scrum-scrums]: https://www.atlassian.com/agile/scrum/scrum-of-scrums
[agile-principles]: https://agilemanifesto.org/principles.html
[example]: https://www.example.com
