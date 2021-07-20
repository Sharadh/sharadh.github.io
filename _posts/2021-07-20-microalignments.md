---
layout: post
title:  Microalignments
date:   2021-07-20 06:50:00 -0700
tags: technical collaboration
---
A key part of [Staff+][staffeng] engineering roles is to build alignment. I call my approach to doing this "microalignment". Many people have recently said it's a great word for what we do, so I'm going to write about it here.

## tl;dr
* Alignment is the _integration_ of two teams' ideas
* Like any integration, [waterfall] is a terribly inefficient way to do it; be intentional and add structure to align early and often
* When this works well, you won't even notice how useful this is

## Microalignments
As an engineer on a platform team, there's consistent engagement required with other teams for actual value to be delivered to a user. When I work on these cross-team projects, I use this formula:

1. Establish an async medium for the project. My favorite is a shared Slack channel.
2. Establish a stream of updates to that medium, and encourage my team to do the same.
3. When my team wonders if this is spammy, I encourage them to make the updates more succinct and to include links to more context. I guide them away from their comfort zone of less frequent larger updates, and towards more frequent smaller ones.

Digging into what those updates really look like:

* _"Re: ticket JIRA-123, just wanted to let you know we're on track and a draft PR is up. You can see it [here][example]."_
* _"Heads up: we just merged [this change][example] that addresses the problems we discussed in our last sync. Please let me know how it works!"_
* _"I just realized when working on JIRA-123 that we haven't agreed on the cadence of data updates. I don't know if this is important, but [here's][example] what I've assumed - let me know if anyone has comments."_

In all cases, there's a fairly informal _and short_ update which is easily parsed. Folks who need more info have a way to get it, and the message itself is a good place for any more discussion.

## Why do I need this?
Many teams today use some version of Agile methodologies, and that's supposed to make sure the right stuff gets built. However, there isn't a great story (that I've heard) about _how_ it gets built.

Scrum's general answer to needing different skills to build something is to have a cross-functional team. That works when organizations are small; as they grow, it starts to break down once "horizontal" teams evolve. These are teams like DevOps (or more generally, Infrastructure), Data Engineering, various backend Platform teams, etc. It's tempting to look at horizontals as the problem because they don't fit the Scrum process, but they're not - they're _really_ useful for a host of things, like shared best practices, a team engineers identify with, a manager that gets them and their career aspirations, etc. Scattering the engineers across customer-facing teams may work for the project but often doesn't for the codebase, nor for the individuals.

So, assuming we have different teams that need to work together, the standard process goes something like this:

1. We brainstorm and figure out dependencies; we then work with different teams, get capacity, and table the work each team needs to get done.
2. We go away and do the work. Every now and then, we get status updates (typically via a technical program manager, or TPM) about how the work is going.
3. When the Jira tickets align, combinations of teams integrate the work with each other.

This seems completely reasonable at first glance, and time and again I've seen teams drift apart in step (2) when they go away and do the work. In theory, having two-week sprints for all the teams means they only drift for that period of time before they get into a room and re-align. In practice, it takes longer.

_Note: I was going to write a whole lot of reasons why it takes longer, but it detracts from the point of this post. I'll write a follow up after._

## Why do I do it this way?
The key insight behind microalignment is to [lower the cost][value-of-docs] of collaboration, and we do that with two techniques: _overcommunication_, and _doing it async._

**Overcommunication** ensures that we keep people in the loop even when there's nothing contentious. Just like regular Scrum, there's steady stream of seemingly minor updates: _"We thought we could use the shared library, but not quite, so we're building our own client."_, _"Had some trouble testing, so it'll be a day delayed."_ The idea is to create enough ambient feedback loops so that we increase the chances of catching something we didn't think was important, or that when something does come up the larger team can _easily_ raise and examine it.

**Doing it async** is a necessary corollary to overcommunication to prevent burnout. We engineers just won't communicate if the cost of doing it is high - we'd rather wait for something to _"become an issue that deserves that level of communication"_. What we're actually saying, of course, is: _"It's painful to schedule a meeting to deal with this small thing. I'll note my assumptions and keep moving on."_. This is why _any_ async medium will do: email, wiki pages, Slack, etc.

## Is this my job?
So, let's say I'm a tech lead on a project. I've got a Product Manager (PM), an Engineering Manager (EM), and perhaps a Technical Program Manager (TPM) as part of my support system. Is this whole alignment stuff my job?

Yes. In fact, I believe that as a tech lead or _any_ engineering leader, my _primary_ job is to ship (technical) alignment. That takes on many forms, and in a cross-functional project, it means making sure my team and my partner teams are on the same page at all times.

I could leverage this support system around me to do this and focus on the _serious_ technical stuff, but I think that's a false economy. They'll need my help with the details, and I'll either be switching contexts too often or be a bottleneck. Especially as I've grown to be involved in many projects at the same time, I think a far more scalable approach is to provide my team(s) the tools to align.

## Does it work?
Measuring success for micro-alignment - like with all good process - is difficult. It tends to solve problems before they become large; this means it's not visible in same way a late-project-all-nighter to integrate two systems is. The success will be at a macro level: complex cross-team projects will ship more on time, and the people involved will be happier working on them.

This long payoff means it can be hard to convince my team that this is useful. Most folks on an engineering team need to be focused on the tactics, the weeds and the warts, and it's hard for them to grok a payoff longer than a two weeks. So while I myself focus on the result, I try and get my team to focus on the process wins by drawing attention to:

* Minor issues that _do_ get raised - and solved - via nimble self-organizing communications.
* Implementation details that in the end deviated from the plan, but still got done on time.

_Note: There are other approaches that evolve to try and achieve this; I'll cover these alternatives in a follow up post._

## Alternatives
There are two other approaches I've seen that evolve to try and achieve the same result:

* Some teams try and get more detail into their tickets. They try and minimize drift by removing the ambiguity. I've seen this result in less nimble execution, as teams take longer to break down the work and incur a higher psychological cost of changing track afterwards.
* Some organizations try a [Scrum of Scrums][scrum-scrums] approach with virtual teams. This seems to work to a point, but after that the burden of collaboration for the horizontal teams is overwhelming. There are too many scrum meetings for them to get any work done.

I've included it here for intellectual rigor and completeness - I'll likely address these in more detail in a follow up post.

## Summary
In this post, I wrote about my approach to building alignment, which is perhaps the most important part of my job. I like to apply Agile techniques in collaboration, and this has led me to "microalignments". By setting up a structure and providing guidance for my teams to communicate early and often, I've found success with minimizing the burden and chaos on cross-team projects.

<!-- References -->
[staffeng]: https://staffeng.com/
[waterfall]: https://en.wikipedia.org/wiki/Waterfall_model
[example]: https://www.example.com
[value-of-docs]: {% post_url 2021-04-02-value-of-documentation %}#cost
[scrum-scrums]: https://www.atlassian.com/agile/scrum/scrum-of-scrums
