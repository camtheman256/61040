---
title: Fritter Backend Data Models
description: 6.1040 Assignment 5a, abstract data models for Fritter concepts
layout: post
categories: assignment
assignment: 5
---

Fritter abstract data models for my [Fritter Backend][Assignment] assignment. To learn more about the API for this project, check out the README.md in the [GitHub repository for my backend][GitHub]. The live backend for this application can be found at [fritter-backend.61040.camk.co](https://fritter-backend.61040.camk.co).

[Assignment]: https://61040-fa22.github.io/assignments/assignment-5
[GitHub]: https://github.com/camtheman256/61040-fritter-backend

1. TOC
{:toc}

## User

### State

- Username: User &rarr; **one** Username
- Password: User &rarr; **one** Password
- Session: User &rarr; **lone** Session
- Following: User &rarr; **set** Users
- Followers: User &rarr; **set** Users

### Actions

- create(u: Username, p: Password): User
- delete(u: User)
- modify(u: Username, p: Password)
- follow(u: User, f: User)
- unfollow(u: User, f: User)

## Freet

### State

- Author: Freet &rarr; **one** User
- Likes: Freet &rarr; **set** Users
- Replies: Freet &rarr; **set** Freets
- Community: Freet &rarr; **lone** Community
- Content: Freet &rarr; **one** String

### Actions

- create(u: User, c: String): Freet
- delete(f: Freet)
- modify(f: Freet, c: String)
- attach(f: Freet, c: Community)
- detach(f: Freet)

## Community \[Item\]

### State

- Name: Community &rarr; **one** Name
- Members: Community &rarr; **set** Users
- Moderators: Community &rarr; **set** Users
- Banned: Community &rarr; **set** Users
- Content: Community &rarr; **set** Item

### Actions

- join(u: User, c: Community)
- leave(u: User, c: Community)
- create(u: User, n: Name): Community
- moderate(m: User, c: Community)
- unmoderate(m: User, c: Community)
- ban(u: User, c: Community)
- unban(u: User, c: Community)

## Briefing \[Item, App\]

### State

- Timeframe: Briefing &rarr; **one** Duration
- Content: Briefing &rarr; **set** Item
- LastVisited: App &rarr; **one** Date

### Actions

- visit(a: App, d: Date)
- create(c: Set\<Content\>): Briefing
- modify(b: Briefing, t: Duration)

## Feed \[Item\]

### State

- LastRefreshed: Feed &rarr; **one** Date
- Pages: Feed &rarr; **set** Pages
- Content: Page &rarr; **set** Items
- Settings: Feed &rarr; **one** FeedSettings

### Actions

- create(c: Content): Feed
- modify(f: Feed, s: FeedSettings)
- changePage(f: Feed, p: Page)

## Concept Map

<img class="img-fluid" src="{% link assets/img/a5_concept_map.png %}"/>