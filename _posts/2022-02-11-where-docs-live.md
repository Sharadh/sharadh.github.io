---
layout: post
title:  Where documentation lives
date:   2022-02-11 08:30:00 -0700
tags: technical collaboration
published: true
---
There are many reasons why engineers don't write documentation. One that's come up in conversation many times recently is _"I don't know where to put this so it's useful!"_. This post attempts to address this question, with some specific guidance around the quintessential Software Engineering answer: _"It depends."_

# Zoom level
> **What Documentation is Required?**
>
> Different levels of documentation are required for the casual user of a program, for the user who must depend upon a program, and for the user who must adapt a program for changes in circumstance or purpose.
> 
> \- Frederick Brooks (1975). Chapter 15 - The Other Face. _[The Mythical Man Month][mmm]_

The single most important part of writing documentation is to understand we always need a zoom level: [the map is not the territory][map-territory]. It's nigh impossible to create a document that's both wide and deep and still useful. (The idea of [progressive summarization][PS] and - ironically - [this shorter summary][PS-2] both capture this well.)

Commonly, I've seen four zoom levels for tech docs:
1. Code
2. Project (service, library, etc; colloquially, _"GitHub Repo"_)
3. System
4. Project Plan

At the _Code_ level, documentation is concerned with how the component works. The component here can be a function, class, or module; it is some independent part of the program. It can (and probably should) contain references to related components but does not primarily concerns itself with things outside its immediate scope. Code level documentation should live inline, as code comments.

At the _Project_ level, documentation is concerned with how the components interconnect. This can be how different components connect with each other (`Reader`, `Parser`, `Transformer`) or how they represent variations of the same (`Parser`, `JSONParser`, `CSVParser`). Notably, it could also be about the project layout - a topic that's consumed many lunch hours. Project level documentation should live in a `docs/` folder in the project. This could also be called _Architecture_, but I find that to be confused easily with _System_ below.

At the _System_ level, documentation is concerned with how the system works to serve a business need. This marks a departure from the previous two levels: the same projects commonly appear in multiple system level documents. System level documentation has in turn varying levels - a project and its infrastructure, a suite of projects (~a platform), an end-user feature, or event the entire engineering architecture of your company. System level documentation should live in the company wiki<sup>1</sup><sup>2</sup>.

At the _Project Plan_ level, documentation is concerned with how a project runs<sup>3</sup>. It is firmly soft-technical: there are a lot of _references_ to the technical work, and the focus is on how the work is sequenced, funded, measured, and ~~marketed~~ presented. There are two variations of this: tech leads may draw up project plans to communicate planned work to their teams, or managers may draw up project proposals and reviews to communicate with executives. The former should live alongside whatever is used to track work (e.g Jira<>Confluence), while the latter should live in general documentation or the company wiki<sup>4</sup>.

# Who cares?
At both the code and project levels, the documentation is geared towards fellow contributors: _"the user who must adapt a program for changes in circumstance or purpose."_

At the system level, the documentation is geared towards both fellow contributors and clients: _"the casual user of a program, \[or\] for the user who must depend upon a program"_

At the project plan level, the documentation is geared towards the machinery of people that funds and runs the project. This doesn't have a direct mapping to Brooks' quote earlier.

# What changes together lives together
Most engineers struggle with disambiguating project and system level documentation. This is because until we were all forced to work remotely, the former wasn't a thing: we just didn't commonly write down project-level decisions, and relied on colocation to bridge the gap. >=COVID<sup>5</sup>, many of us have identified this problem and that's led to a glut of docs in wikis everywhere.

The problem is that even when they get the zoom level right, these docs are submoptimal because code changes in unexpected ways (and sometimes at high velocity), and project documentation in wikis quickly goes stale. Worse, it takes _a lot_ of effort to make it discoverable.

This is why I prefer project level docs to live _inside_ the project. I really like using regular change management (PRs/CRs/Issues) to discuss, and [ADR] to document these decisions in a structured way.

# tl;dr
* When writing docs, clearly identify what zoom level you're working at
* Choose the appropriate location: what changes together lives together
* Use regular PRs/Issues to discuss project-level changes, and [ADR] to document them

---
---
<sup>1</sup>In some uncommon cases, it may make sense to put system docs at the _Project_ level. This typically happens when the project contains infrastructure definitions inline (terraform/CloudFormation/etc).

<sup>2</sup>Here, "wiki" is any searchable document store that non-Engineers can access.

<sup>3</sup>It's easy to identify documentation at this level, since most engineers hate writing these.

<sup>4</sup>It is a best-practice to link to these documents that live outside the wiki (e.g Google Docs) from some central wiki home for the project that _also_ contains system level documentation.

<sup>5</sup>I use Post-COVID to mean _"once the pandemic began"_, but this sits uncomfortably with some, esp. parents like me who want to make it _very clear_ that the pandemic isn't over yet. >=COVID is clearer.

<!-- References -->
[mmm]: https://en.wikipedia.org/wiki/The_Mythical_Man-Month
[PS]: https://fortelabs.co/blog/progressive-summarization-a-practical-technique-for-designing-discoverable-notes/
[PS-2]: https://jamesstuber.com/progressive-summarization-a-waste/
[map-territory]: https://fs.blog/map-and-territory/
[ADR]: https://adr.github.io/
