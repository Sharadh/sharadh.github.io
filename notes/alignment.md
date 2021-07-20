---
layout: page
title: Alignment
# only render this page when using `jekyll serve --unpublished`
published: false
---
We've been reading Will Larson's [Staff Engineer][staffeng] book at work, and there's a specific line that captures my role as a Staff+ engineer perfectly:
> Staff-plus roles are leadership roles, and in leadership roles, the support system that got you here will fade away. **Often abruptly, you're now expected to align the pieces around you for your own success.**
> 
> \- [Staying aligned with Authority][staffeng-aligned]

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

The more insidious part of escalation is that when it becomes the go-to approach, teams forget how to work without it. When _that_ happens, the senior engineers involved - and this is where you and I come in - just don't scale. Engineers usually outnumber the folks in the "management structure", so the management folks become a bottleneck for every decision. Consequently, senior ICs hit a wall and get incredibly frustrated that they just can't create the impact they want.

### Connective Tissue
This technique helps me scale, and also helps the organization build [connective tissue][updates].

<!-- References -->
[staffeng]: https://staffeng.com/
[staffeng-aligned]: https://staffeng.com/guides/staying-aligned-with-authority
[updates]: https://lethain.com/weekly-updates/
