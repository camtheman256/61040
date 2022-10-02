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
- people can delete user accounts
  - removes their profile from Fritter
  - removes their Freets from Fritter
- users can follow other user accounts
  - updates their follower list

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
  - updates community members list
- users can become moderators
  - gives user the ability to remove Freets from a community and ban users
- users can create new communities
  - new community is created
  - user gets moderation ability in their new community

## Briefing

In Fritter, a **Briefing** is presented to users after they reopen the app after a longer duration.

**Purpose:** Freet Briefings help catch Fritter users up on the most popular content in their feed since their last visit.

**Operational Principle:** When a Fritter user reopens the app after a long duration, a Briefing panel is presented to them, with an adjustable timeframe for the recency of Freets. Only Freets from the user's follows and communities will be shown in a Briefing.

### State

- the timeframe of Freets to show
- the number of Freets to show
- the Freets to show in the Briefing

### Actions

- users can adjust the timeframe of tweets to show
- users can adjust how many tweets they want to be shown in their Briefing

## Feed

In Fritter, the **feed** is the primary way users can view Freets from their communities and the users they follow.

**Purpose:** Provide a way for users to browse Fritter in a way that respects their time.

**Operational Principle:** The most recent Freets in a user's communities and followed accounts are ranked according to their popularity and are displayed in a paginated view in the main page of the app. Many features of the feed are adjustable, such as how often to allow refreshing of the feed, the number of Freets to show per page, and the number of pages to show. 

### State

- when the feed was last refreshed
- the page the user is viewing
- the collection of Freets to show in the feed

### Actions

- users can browse through the pages of Freets in the feed
- users can adjust settings for:
  - how often to load new Freets into the feed[^2]
  - how many Freets to show per page
  - how many pages to show (can be infinite)

# Synchronizations

## Community-Freet synchronization

Users can only post **Freets** to **communities** that they are members of, so we need a synchronization rule that connects these two concepts:

```
when join c (Community), allow f (Freet) to be posted to c
when leave c (Community), disallow f (Freet) to be posted to c
```

## Feed and Briefing synchronizations

The **feed** and **briefing** need to get synchronized with both the **user's follows** and **joined communities**, in order to know which Freets to show a user.

```
when join c (Community), add c's freets to e (Feed) and b (Briefing)
when follow u (User), add u's freets to e (Feed) and b (Briefing)
```

## User-Freet synchronization

When **users** delete their account, we want to respect their wishes by also remove their **Freets** from the platform.

```
when delete u (User), delete all f (Freets) posted by u
```

# Wireframes

My Fritter wireframe prototype can be found [here][wireframe] on Figma. Click to close the briefing, visit the next page, and click on the community link to view an example community page. Some screenshots are embedded below.

## Briefing

<img src="{% link assets/img/a3_fritter/Briefing.png %}" class="post-image border" />

This view shows the Briefing page, which pops up in a panel. Tapping the **12h** text will let you adjust how recent you want the Freets to be in your Briefing. The Briefing is easy to dismiss with the close button or by sliding down the panel.

## Feed

<img src="{% link assets/img/a3_fritter/Feed 2.png %}" class="post-image border" />

This view shows the main Fritter feed. You can click through the pages of Freets with the pagination at the bottom. Like handles in Twitter, communities also get linked in Freets, if a Freet is posted to a community or if the name of a community is included in the text of a Freet.

## Community Page

<img src="{% link assets/img/a3_fritter/Community.png %}" class="post-image border" />

This is what a community page looks like in Fritter. It looks similar to profile page in Twitter, but it shows a list of members and moderators instead.

# Design Tradeoffs

## Who holds the gavel?

When designing the community feature, I had to decide whether communities should get to self-moderate, or whether this should be handled entirely on a platform-wide basis. While community moderation has worked well on other platforms like Reddit, it has led to a more hands-off approach that let hateful communities proliferate.

However, in this case, I think letting communities moderate themselves helps keep things "on-topic" and respects Fritter users' interests better, which is a fundamental goal of the platform.

## Slot Machine vs. The Newspaper

Multiple concepts in Fritter are directly counter to addictive engagement features existing on nearly every social media platform out there. However, in my interviews with Twitter users, they seemed to desire an interface more like a newspaper, so they could catch up on their favorite topics without being sucked into doomscrolling or rabbit holes.

The Briefing and feed present a return to a newspaper-like format. The Briefing is like skimming the front page, whereas the feed is like leafing through the pages.

## Sea of Settings

One potential issue with many features of my Fritter app is that it turns over a large amount of control over how the app behaves to the user. In this case, it'll be important to have good defaults and prompt users if they want different behavior, as most users won't dig into the settings to configure the app at first.

However, offering these settings to control Fritter's behavior is a key feature of how Fritter respects your time, so it's important to have them, even if it means that the app is less engaging for new users.

---

[^1]: In other platforms, this is often called a _username_.
[^2]: The intention behind this feature is to remove the gamified "slot machine" aspect of social media, where you can constantly refresh to get new content. Users that care about seeing recent Freets can set this to a low number.

[wireframe]: https://www.figma.com/proto/KvbunFX9WF1M2A3WBIhQXj/Fritter?node-id=1%3A2&scaling=scale-down&page-id=0%3A1&starting-point-node-id=1%3A2