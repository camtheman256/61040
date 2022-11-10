---
title: An Introduction to Fritter 
subtitle: A brief user guide to my Fritter app
description: 6.1040 Assignment 6, a blog post about how to use my Fritter application
layout: post
categories: assignment
assignment: 6
---

This post introduces [my Fritter app][app], which is available on the web at [fritter.61040.camk.co][app].

1. TOC
{:toc}

## Design

The design of my Fritter app was intended to be clean and refined. The serif font, Lora, helps the app look legitimate while still being playful.
The thin black outlines for the buttons and use of emoji as icons are to help the app feel lightweight but still fun and inviting.

The padding on the sides also adjusts to smaller screen sizes, so the app should be usable on mobile as well.

## Homepage

Loading up Fritter brings up the homepage, which has been cleaned up and some links are available to check out communities.
The starter Freets page has been moved to centralize the user experience around the user's interests.

![home]({% link assets/img/a6/home.png %}){:class="img-fluid"}

Signing in brings up an opportunity to post Freets, as well as view the user's feed.

![home signed in]({% link assets/img/a6/home2.png %}){:class="img-fluid"}

### Briefing

Right underneath is the user's Briefing, with the most recent Freets from the user's follows and communities from the last 12 hours.

![Briefing]({% link assets/img/a6/briefing.png %}){:class="img-fluid"}

## The Feed

Clicking to view the feed brings up the feed with the same state as the _last_ time the user refreshed it.
This gives the feed a more consistent user experience, as well as supports the pagination capability.

![Feed]({% link assets/img/a6/feed.png %}){:class="img-fluid"}

Refreshing the feed lets the user specify how many new Freets they want to see, as well as how many Freets they want to see at a time.

![Refresh]({% link assets/img/a6/refresh.png %}){:class="img-fluid"}

Then, the new Freets will be displayed after a feed refresh.

![Feed after refresh]({% link assets/img/a6/feed_refresh.png %}){:class="img-fluid"}

## All Freets

The "View all freets" page has been moved into its own page, which users can use to browse the network and follow new users.

![All Freets]({% link assets/img/a6/allfreets.png %}){:class="img-fluid"}

If you're signed in, searching up an individual user also gives the option to follow or unfollow.

![Follow]({% link assets/img/a6/follow.png %}){:class="img-fluid"}

## Communities

The Communities page lets users create, join, and view communities that exist on Fritter.

![Communities]({% link assets/img/a6/communities.png %}){:class="img-fluid"}

Searching up a community allows you to see its moderators and how many members it has. If you're signed in, you can join or leave the community.

![Join community]({% link assets/img/a6/mit_community.png %}){:class="img-fluid"}


[app]: https://fritter.61040.camk.co