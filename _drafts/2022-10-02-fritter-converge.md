---
title: Welcome to Fritter
subtitle: A new version of Twitter that respects your time and interests
description: 6.1040 Assignment 3, a product pitch for a version of Twitter
assignment: 3
layout: post
categories: assignment
---

This post lays out a pitch and design for Fritter, my Twitter clone.

1. Table of Contents
{:toc}

# Pitch

**Fritter is a new version of Twitter that's better at respecting your time and your interests.** Fritter aims to eliminate the endless doomscrolling of social media, while keeping you connected with your friends, communities, and public figures. 

Fritter respects your interests by only giving you content on topics you care about. It's centered around your favorite communities, and it keeps moderation in the hands of people you know and respect. Instead of having platform-wide rules that let bots and harassment fall through the cracks, Fritter has community moderation. Now, you can set your own rules and cut out the noise of spam and off-topic posts.

Fritter respects your time by giving you just what you need to know when you want to know it. It'll update you with a Briefing when you open the app. It's paginated, so you won't have to feel the FOMO of an infinite scroll if you only have limited time to check social media. The Briefing feature also means that you can easily fit Fritter into your morning routine without missing out on everything that's happening.

<div class="alert bg-danger">
TODO: Where does following/joining a community show up?
</div>

# Concepts

Some concepts in this assignment are implicitly referenced because they will be copied over from Twitter and similar platforms without much modification:

- Following users (for the purpose of generating Freets to be used in the Briefing and Feed)
- Liking Freets (for the purpose of ranking popular content in communities and the Feed)

## User

In order to post to Fritter, users must sign up for a **user account**.

**Purpose:** Identify the authors of Freets and aggregate all of their Freets together

**Operational Principle:** Users identify people or organizations using Fritter. When a person signs up for Fritter and selects a handle[^1], a user account is created for that handle. Handles in Fritter are prefixed with the **@** symbol. The person can also supply a photo, biography, and name that will show up on the profile of this user in Fritter. All of this information can be changed at any time, for any reason.

### State

- the user's name, photo, biography, and handle
- the user's followers list
- the user's following list
- the list of Freets posted by this user

### Actions

- people can create user accounts
- people can change their profile information and handle
- people can delete user accounts, removing their profile freets from Fritter
- users can follow other user accounts

## Freet

In Fritter, a **Freet** is a 300-character or fewer post created by a user.

**Purpose:** Freets allow for Fritter users to communicate on the platform and publish their thoughts 

**Operational Principle**: Freets can be posted by users at any time to their profile and can optionally be published to a community. Freets posted to a community are subject to moderation and community rules. Freets may also be posted in reply to existing Freets, where they will show up underneath.

### State

- number of likes received
- (in case of a reply) parent Freet
- community attached to a Freet

### Actions

- users can post Freets to their profile
- users can tag their Freets with a community when they post them
- users can reply to other Freets with new Freets

## Community

In Fritter, a **community** is a collectively created curation of Freets centered around a topic or idea.

**Purpose:** Communities allow for the aggregation and moderation of similar Freets on Fritter, and provide users with a central place to learn about a topic.

**Operation Principle:** Much like following a user, users can join a community on Fritter to see its Freets in their Briefing and Feed. Only members of a community can post Freets to that community. Moderators can take action to detach Freets from a community if they don't follow the rules. The number of likes on a Freet by community members helps rank the Freet in a user's Briefing and Feed and on the community page. Communities in Fritter are prefixed with the ampersand (**&**) symbol.

### State

- list of community members
- list of community moderators

### Actions

- users can join or leave a community
- users can become moderators
- users can create new communities

## Briefing

In Fritter, a **Briefing** is presented to users after they reopen the app after a longer duration.

**Purpose:** Freet Briefings help catch Fritter users up on the most popular content in their feed since their last visit.

**Operational Principle:** When a Fritter user reopens the app after a long duration, a Briefing panel is presented to them, with an adjustable timeframe for the recency of Freets. Only Freets from the user's follows and communities will be shown in a Briefing.

### State

- the timeframe of Freets to show
- the number of Freets to show

### Actions

- users can adjust the timeframe of tweets to show
- users can adjust how many tweets they want to be shown in their Briefing

## Feed

---

[^1]: In other platforms, this is often called a _username_.