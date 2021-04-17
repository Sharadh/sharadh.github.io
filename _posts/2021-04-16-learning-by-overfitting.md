---
layout: post
title:  "Learning by Overfitting"
date:   2021-04-16 19:22:00 -0700
tags: learning mental-models culture
---
I find the weirdness of learning something new fascinating, and I try to observe myself and others going through the process. One particular process I've realized recently is "learning by overfitting" - I'll explain what I mean by that, why I think it is helpful, and how to guard it against the forces of [Imposter Syndrome][imposter-syndrome].

_If you're interested, I wrote a [longer post][imposter-syndrome-me] about Imposter Syndrome previously._

## How Children Learn
The inspiration for this came from our toddler. Ever since he was able to move, he's had a curious habit: every time my wife or I give him something new to play with, he takes it on a tour of the house. He takes the new item to every single activity he does: he tries to put it inside a pot, he tries to balance it on his blocks, he tries to dunk it in water. He tries every single way of playing with it, and gradually - as he learns what it is good for - settles on a handful of things. Granted, children have a logic all their own, but there is _some_ logic at play here, and it's always puzzled us.

When my wife and I were talking about it, it suddenly hit me: I was a complete and utter hypocrite! I do exactly what my son does, except in the abstract domain of thought. Every time I have a new idea - or more accurately, a new mental model - I try using it _everywhere_. Over time I settle down but when starting out, that new mental model is the [Grand Unified Theory][GUT] of all knowledge.

## Learning by Overfitting
I call this "learning by overfitting": like data scientists sometimes stretch and strain their model to fit every data point, I stretch and strain my mental model to fit every observed event. In general, I realized I go through three phases when I learn a new thing:

1. **Try it everwhere** and see if it works. See all the things in terms of the new mental model.
2. **See it fail** and notice where the limits lie.
3. **Tune the model** to pare back and account for the failures.

...and repeat.

Let's take an example: I've just learned [Maslow's Heirarchy][maslow].

1. I see every incident of a colleague not collaborating well as _"some psychological needs haven't been met"_.
2. I observe that many colleagues feel very secure, and still seem to not collaborate well and are fairly curt.
3. I refine my understanding of Maslow's Heirarchy - it explains each person's actions in accordance with their own self-actualization, not mine.

Let's take another one: I've learned about microservices.

1. Everytime anyone has a problem of maintenance and things getting too complex, I think _"Oh, the service is too big. We should split it up."_
2. I try it out and realize that splitting it up would cause most operations to need coordination across two services, which makes things more complex.
3. I realize that microservices make sense as long as they have distinct data concerns, and that some services just deal with more complex data.

Over and over again, I observe myself doing the same thing. That's not half as interesting as the fact that I observe people around me doing it as well!

## Hammers and Nails
In many discussions, I've been tempted to repeat [the saying][hammer]:
> When all you have is a hammer, everything looks like a nail.

It's generally a valid thing to say, especially when I think my colleague is misdiagnosing the problem in order to apply a specific remedy. When I'm thinking this, I'm also implicitly assigning a "score" to their ability to critically analyze a situation at hand.

With the realization that overfitting is part of the learning process, my mindset has changed. Instead of judging my colleagues' ability to analyze the situation, I see it as them playing with a new concept: they're taking it for a spin, and seeing if it provides value.

## Imposter Syndrome
Learning that many of us learn by overfitting has helped me address my own imposter syndrome when starting with a new domain. Instead of questioning my own judgement and learning, I've learned to accept that I will overfit - that I will take the first few things I learn and oversimplify the domain in terms of these things. This has helped me bootstrap _faster_.

It has also helped me collaborate better in two key ways:

1. I qualify statements especially to junior colleagues with _"I learned this recently, and think it may apply here..."_; this helps them understand where I am in my domain learning instead of overweighting my words.
2. I am more gentle when pointing out others' overfitting: instead of dismissing the idea itself, I try and clarify where the model works - and at what point it breaks down.

## Summary
So to summarize: many of us learn by playing with a new idea and overfitting it to all situations. Accepting this as a part of learning can help us be more gentle with ourselves and others, and probably speed up the rate at which we all learn.

<!-- References -->
[imposter-syndrome]: https://en.wikipedia.org/wiki/Impostor_syndrome
[imposter-syndrome-me]: {% post_url 2021-01-15-imposter-syndrome %}
[GUT]: https://en.wikipedia.org/wiki/Grand_Unified_Theory
[maslow]: https://www.simplypsychology.org/maslow.html
[hammer]: https://en.wikipedia.org/wiki/Law_of_the_instrument