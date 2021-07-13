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
First, a point about alignment.

We've been reading Will Larson's [Staff Engineer][staffeng] book at work, and there's a specific line that captures my role as a Staff+ engineer perfectly:
> Staff-plus roles are leadership roles, and in leadership roles, the support system that got you here will fade away. **Often abruptly, you're now expected to align the pieces around you for your own success.**
> - [Staying aligned with Authority][staffeng-aligned]

So, here's how alignment works for an engineer:
* **<=Staff**: there isn't much alignment to worry about. My manager, product manager (PM), or technical program manager (TPM) - what do they _all_ do the entire day, anyway? - need to know when something isn't quite what we expected during Planning.
* **>=Staff**: I'm 99% sure the team can get the work done. How do I make sure I'm not wasting their time, and we work on the right things and have things to work on? I better talk to my manager, PM, or TPM (they're probably thinking about the same thing.)

Here's the rub: as (often) the most senior Engineer, I'm expected to (a) understand the key details of what the team is doing; (b) understand the implications of these on the context<sup>*</sup> we operate in; and (c) escalate appropriately when _something is off._ 

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

## Summary
In this post, I wrote about my approach to building alignment, which is perhaps the most important part of my job. I like to apply Agile techniques in collaboration, and this leads to recurring "microalignments". This technique helps me scale, and also helps the organization build [connective tissue][updates].

### Notes
* Building alignment is key part of Sr. engineering roles
* Like any integration, waterfall is a terrible way to do this and expensive
    * also, high psychological cost
* Agile works way better
    * microalignments
    * keep people in the loop even when there's nothing contentious
    * usually, _something_ will come up. It'll be so minor you won't realize - but this is _important_ so look for it and draw focus to it.
* Your job is to help the org build [connective tissue]()

<!-- References -->
[staffeng]: https://staffeng.com/
[waterfall]: https://en.wikipedia.org/wiki/Waterfall_model
[staffeng-aligned]: https://staffeng.com/guides/staying-aligned-with-authority
[updates]: https://lethain.com/weekly-updates/
