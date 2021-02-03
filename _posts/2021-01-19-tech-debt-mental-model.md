---
layout: post
title:  "Useful Mental Models for Technical Debt"
date:   2021-01-15 21:41:40 -0800
categories: technical tech-debt mental-models
---
In a conversation with my new team, one issue that came up was avoiding technical debt. We were all excited (and nervous!) that we were working on a greenfield project, and the team felt that one main benefit was _not_ taking on a codebase saddled with tech-debt. As I reflected on this conversation, I realized that I'd learned and used a couple of really useful mental models about tech debt. In this post, I'll write down the mental models in my head so others can see, evaluate, and help me make them better.

## Why Talk About Tech Debt?
I think it's important to talk about tech debt because, at a very high level, it boils down to something very simple: tech debt bad, no tech debt good.

This is clearly _super_ reductive, so it's not going to scale well. But it's also super _simple_, which means it sticks! Most engineers have an "away" reaction to tech debt and would prefer to design the more elegant solution. If we don't talk about it - if we don't stop to question it - the default choice we may take is suboptimal.

One of my senior colleagues, Anurag, had this pithy little statement that has stuck with me:
> The \[Silicon\] Valley is filled with failed startups that have gold-plated plumbing.

Most of us do Software Engineering in pursuit of a larger product or business goal. Learning how to reason about tech debt is a critical part of doing this well.

## Debt and Capital
The first mental model comes from the name itself: Technical Debt is a form of debt. So let's zoom out into a little Economics 101: why does debt exist?

When I was younger, and brought up with a hyper-conservative attitude towards owing money to people, I thought all debt was bad. Turns out, this isn't necessarily true. Profitable companies - _highly_ profitable companies - frequently take on a little debt. It's considered a responsible way to run a business: companies (or individuals) believe the rate of interest they pay on the debt is lower than the benefits that it gives them. These benefits could be anything that matters: users, revenue, market share, etc.

This is exactly why taking on _appropriate_ technical debt is considered a responsible way to run an engineering team. When we take on tech debt, we're betting that the rate of interest we pay on that debt is lower than the benefits it gives us: time back to do other things, faster time-to-market, or unblocking a client team.

### Rate of Interest
What does the rate of interest on the debt mean, and why does it matter?

The rate of interest is the cost to _maintain_ that debt, or to _workaround_ it. For example, it could mean we have to laboriously copy-paste a change in 17 different places across 3 projects. Or it could mean we have to manually press 5 buttons in a specific order each time we want the product inventory to refresh on the live website.

### Tech Bankruptcy
Tech bankruptcy happens when a team's technical debt grows to such an extent that they can't continue to function. The debt has balooned beyond management, and the team is unable to keep up the consistent payments to service it. Left unchecked, the team _will_ fail, projects _will_ crumble, and everyone _will_ be fairly miserable.

The [Google Site Reliability Engineering (SRE) Book](https://sre.google/sre-book/table-of-contents/) has a neat way of semi-objectively judging a team's tech-debt budget using SLOs. In this scenario, when a team runs out of budget, all feature work stops and they have to service the debt _or_ lose SRE support.

### Aside: Your Currency is Time
_Feel free to skip this part, it's just me nerding out on exact abstractions._

Here's the interesting bit: although it's called technical debt, what we're actually dealing with is time. What we're borrowing is time - instead of doing the elegant solution, we're saving some time with a hackier one. What we're paying back is a little time every sprint to service this debt, but we think the net time we save is worth it.

Bankruptcy happens when we don't have any time left. All our time is spent servicing tech debt, and without outside investment (i.e more engineers) or asset stripping (i.e fewer projects) the team can't continue to function.

## Recap: Tech Debt is Debt
So that's the first mental model: tech debt is like any other debt, a tool for growth that ought to be used responsibly after considering the cost and benefits.

## Calculating the Rate of Interest
Let's assume there's some way to determine the benefits we get from taking on tech debt. (We'll just hand-wave and let our hypothetical all-action Product Manager, Alan, handle it. Thanks Alan!) The second mental model is around determining this rate of interest.

My favorite resource for this is a blogpost from Riot games about the _[Taxonomy of Technical Debt](riot)_. Under this model, there are a few different axes to consider any debt: Impact, Cost, and Contagion

* **Impact** is what we've seen already - the cost of maintaining or working around the debt.
* **Cost** is actually _Cost to fix_: the cost of biting the bullet, doing the more elegant thing, and ripping all the hacks out.
* **Contagion** is _very_ interesting. It's how quickly the debt spreads - in 2021 in the midst of a pandemic, one could say it's the replication factor of the debt.

### Contagion
TODO

## Summary
1. Tech debt is like any other debt - taking on a responsible amount will infuse your project with funds for growth.
2. Like other debt, learn to reason about the rate of interest and what you _can_ afford to pay back.

## Notes
* Why
* First: tech debt is debt
    * Why we take on debt
    * Interest rate
    * When does it make sense
    * Tech bankruptcy (xref Google SRE book)
* Second: Riot games
    * Impact/Cost/Contagion
    * Contagion is really key
    * Three of these play into the interest rate
* Examples of good tech debt and bad

[riot]: https://technology.riotgames.com/news/taxonomy-tech-debt

