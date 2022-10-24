---
title: Fritter Backend Design Reflection
subtitle: A wild API appeared!
description: 6.1040 Assignment 5b, reflecting on my Fritter API implementation
categories: assignment
assignment: 5
layout: post
---

This post reflects on my Fritter backend design. For the production Fritter backend, visit [fritter-backend.61040.camk.co][backend]. The GitHub repository is [camtheman256/61040-fritter-backend][github].

1. TOC
{:toc}

## Feed Implementation

Implementing the Feed proved to be pretty interesting! While most social media apps treat the "feed" as a structured view into the post concept, I implemented the feed by having separate endpoints for creating the feed and viewing its individual pages. The concept structure proved to be helpful for giving the feed a full-blown model, some collection helper functions, middleware, and endpoints.

### Light Briefing

In my design, I realized it made the most sense to treat the briefing as a simple (time-limited) query into the User's feed and decided to forego a model for Briefings. This is further supported by the idea that the Briefing is intended to be looked through once and then dismissed once the user comes back to the app. In the abstract data model, I had the Briefing concept interact with a generic "App" concept. Without more modifications to User to track their behavior, it's hard to determine whether to launch a Briefing. I will likely leave whether to launch the Briefing up to the frontend instead, which is where the "App" concept can come in.

## Modifications to User

I modified the User concept to have arrays holding lists of users for their followers and the users they follow. In theory, this could be reduced to just one list that the user follows, by having a virtual field to get the list of users that follow them. However, it made the most sense to me and seemed best for scalability to store both on the user model.

[backend]: https://fritter-backend.61040.camk.co
[github]: https://github.com/camtheman256/61040-fritter-backend