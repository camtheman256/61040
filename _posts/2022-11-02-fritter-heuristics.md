---
title: Fritter Heuristics Evaluation
subtitle: Revisiting my wireframes to talk about UX
description: 6.1040 Assignment 6a, wireframes heuristic evaluation
layout: post
categories: assignment
assignment: 6
---

This post takes a look at my wireframes from [Assignment 3][A3] under the [heuristics for evaluation][heuristics] in the assignment prompt. A work-in-progress version of my Fritter application is currently deployed at [fritter.61040.camk.co](https://fritter.61040.camk.co). Feel free to give it a try while I work on it!

1. TOC
{:toc}

## Usability Heuristics

### Learnability

- I'm a little concerned with how easy the Briefing aspect will be to learn. Right now, it might be a surprise if the Briefing pops up and users aren't already aware of its purpose. It might be useful to modify the briefing and tuck it away in the app somewhere in case users want to come back to an older Briefing or accidentally close it.
- Additionally, the community concept might be unfamiliar to users, so having a clear method of explaining it and showing them what communities they're a part of might be a good idea.

### Pleasantness

- I intentionally tried to design for simplicity for Fritter and tried to reduce the chaos on social media, and I think the paginated Feed really succeeds in this area.
- I like how the communities seamlessly integrate into the feed, which relates to the goal of respecting the user's time and interests. I'm going to try to retain this in the final Frontend design.

## Physical heuristics

### Situational context

- My wireframes only showcase a mobile device but my development platform is a desktop computer. I'll need to be careful to make sure that my Fritter app makes sense across platforms.
- Related to the previous point, a briefing that slides up might make less sense on a desktop platform, so I might want to consider some kind of dismissible pop-up instead.

### Fitt's law

- A key piece of my interface is the pagination, so I might want to focus on making really big and obvious previous and next page buttons.
- Another idea is enabling swiping between pages, though this might be more complicated given how some platforms handle a swipe from the edge as a back action.

## Linguistic level

### Consistency

- I really like how the "community" aspect of Fritter is just laid on top of the existing single-user style of posting Freets. It's very transparent when a Freet is posted to a community, and it fits well into the existing design.
- I also like how, copying from Twitter, the **@** symbol is clearly used to identify users, while the **&** symbol identifies communities. It may be worth calling this out more explicitly in my frontend design.

### Information Scent

- Right now, my wireframes in my [assignment 3 pitch][A3] are pretty disconnected. It's not clear how you get from one place to another. This ought to be changed in my frontend with more clear navigation from one screen to the next.
  - However, relating to the [Situational context](#situational-context) bullet point, it's worth making sure that these connections between pages make sense given the context of the platform they're designed on. More advanced navigation might be appropriate on desktop platforms, for example.



[A3]: {% link _posts/2022-10-02-fritter-converge.md %}
[heuristics]: https://61040-fa22.github.io/assignments/assignment-6#heuristics-for-evaluation