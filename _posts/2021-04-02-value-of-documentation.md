---
layout: post
title:  "The Value of Documentation"
date:   2021-04-02 22:00:00 -0700
tags: culture documentation collaboration
---
A group of us were talking about the value of technical writing, and there was an excellent question: _What happens if my colleagues just don't believe writing documentation is worth it?_.

I personally believe that documentation _is_ useful in a vast majority of cases, and I also know that being able to empathize and work with those who don't is a major part of being a successful engineer. So, let's see why this disagreement happens and what we can do about it.

## Scenario
Let's take an example: you join a new team, and are enthusiastic to make a contribution - to make a mark! You realize there's a simple way: the team has built a lot of things recently and the documentation is patchy. So as you ramp up you write down your learnings and share it with the team. Instead of an equally enthusiastic reception, a senior colleague - maybe even your tech lead! - is lukewarm.

At this point, it's easy and perhaps even reasonable to conclude that your colleague is a philistine who has no appreciation for the craft of Software Engineering. But that doesn't really get us anywhere. Like Fred Kofman says in _[Conscious Business]_, we need to take the attitude of a _player_ who can affect the game, not a _spectator_  who takes it for what it is.

## The Problem
At a high level we can approach this like any other engineering issue - with a dispassionate analysis of the pros and cons, a simple cost/benefit analysis. But if we do, we'll quickly realize that with documentation _both_ the cost and the benefit are subjective. We may believe that we get great value from documentation - that a well written comment, a module overview, or a project readme make us tangibly more productive. We may also think that it's not that much effort for us to add the documentation while we're around the work.

But our colleagues may disagree about both sides of this equation.

This is why conversations about the value of documentation can be exceedingly frustrating: often, the two parties are operating with different _axioms_ about the domain.

## Cost
We all agree there's effort required to write and maintain documentation. Here's the catch, though - folks who think docs are useful are more likely to write them, and with practice it becomes easier; their perceived cost is lower than average. On the other hand, writing - and _especially_ maintaining - comes across as onerous to folks who aren't used to doing it.

It's an interesting phenomenon, and I think many "soft-skills" are like this: over time, the difficulty of the skill polarizes those who pick it up and those who don't into camps that can't really understand each other.

## Benefit
On the other side of the equation, we come to the _benefit_ of writing documentation. We'd assume that this one is more straightforward, right? Turns out no, because statistics.

Truth be told, there's a _lot_ of average (or even plain bad) technical writing out there. So, there's a high probability that when a colleague thinks of the average document, their immediate response is to say: _"Meh, I'll pass."_

It's not that there isn't _any_ good writing that they've read, it's just that the state of our industry means it's entirely reasonable that their instincts tell them it's not worth the effort.

## Evidence Based Reasoning
To summarize: folks don't just agree that writing documentation is good because it's _"just good craftsmanship."_ We all extrapolate off our own varied experiences, so this is entirely reasonable and common. That said, I'd wager that a majority of engineers agree that good documentation makes their job easier. How do we work with the smart, valued colleagues who don't agree?

Of the two parts of the equation, I believe the more effective way is to focus on the benefits. If we offer to do the work, and we believe it's not much effort, the only thing left is to convince our team it's a worthwhile investment. To do this, I suggest trying a simple technique - evidence based reasoning: ask them for specific examples where docs have helped them.

Most people will point to an example, and then immediately point out why that isn't something we can emulate. This is a start, and engaging with them on _why_ we can't emulate it is already halfway to where we want to go. It's no longer a question of "is it useful?", but a question of "how can it be done?"

On the other hand, if they say they've _never_ found useful documentation then they are either an extreme case of a certain style of learning, or just plain unaware. With their permission, ask others in your pod, team, guild, or org. I'm fairly certain that seeing widespread appreciation of the benefits will help them understand that _many others_ find it useful even if they don't. At this point, most reasonable people will cede.

### Myth: "I'd rather just read the code"
One notable objection to writing documentation is that engineers say the documentation often goes out of date, the code is the only source of truth, and therefore we should just write good code and point everyone to it.

This is partially true - essentially, for one segment of documentation, we should prefer to let the code speak. If we're writing stand-alone documentation about the nitty-gritties of a function, class, or algorithm, we're probably doing it wrong. This sort of stuff changes often and it's most effective to keep the comments inline with the code.

However, a vast majority of documentation is not function docstrings. It's stuff at a higher level of zoom - what the module does, or the project, or even the platform. Reading the code is an extremely ineffective way of transmitting this valuable information.

## Caution: Confirmation Bias
I'll throw in a note of caution before we end: beware [confirmation bias]. If we're super-enthusiastic believers in writing documentation, it's totally normal that we can take it too far. Put bluntly: sometimes writing docs **is not** the right thing to do, but we might do it because we think it's generally a good thing.

I like to check myself when I get push-back from a colleague, and try to honestly answer: am I doing it intentionally because it's useful, or automatically because it scratches an itch?

The latter is totally okay, as long as we don't ask someone else to follow suit.

## Mental Note: Types of Leadership
My reasoned guess is that this specific situation my colleague was in was difficult because the technical leader in question was leading by authority, which left little room for perspectives different from theirs. It's the latest reminder that I need to consciously practice different styles of leadership. If I'm truly committed to making diversity work in tech, I need to cultivate a style that can allow different opinions - even ones that I don't personally resonate with or have seen to work!

## Summary
This post was about the value of documentation: how can I have a productive conversation with a rational colleague who just doesn't see the point of it?

1. Many times, these conversations are frustrating because of axiomatic differences. It's easy to assign wildly different values to both the cost and the benefit of documentation, which leads to polarized opinions.
3. Connecting with specific instances where it has helped our colleague might help break the axiomatic gridlock.
4. If all else fails, agreeing to ask for more people's opinions will help identify if either of you have a significantly extreme view of the issue.

<!-- References -->
[Conscious Business]: https://www.amazon.com/Conscious-Business-Build-through-Values/dp/1622032020
[confirmation bias]: https://en.wikipedia.org/wiki/Confirmation_bias
