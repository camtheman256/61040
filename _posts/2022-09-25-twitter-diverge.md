---
layout: post
assignment: 2
categories: assignment
title: Fritter Diverge
subtitle: Some ideas for Twitter
description: Assignment 2 for 6.1040, a series of sketches for new features for Twitter
---

In this post, I'll lay out a series of ideas for Fritter, 6.1040's Twitter clone through _adjusted_, _adopted_, and _invented_ concepts. For more info on this assignment, [check out the assignment page][assignment].

Although these concepts are intended to be used in our Fritter clone, I found it more helpful to write about them as they apply to a Twitter user, so much of the language in this article will refer to the concepts as if they were integrated into the Twitter app as a new feature.

1. TOC
{:toc}

# Communities

<img class="img-fluid" src="{% link assets/img/a2_community.png %}">

**Type:** Adoption (from Reddit primarily)

**Problem:** Content on Twitter feels too scattered. It’s hard for communities to exist on Twitter or for there to be a central place to post content on a topic.

**Purpose:** Provide a central, safe, moderated place to post about a common topic on Twitter.

**Operational Principle**: Users can "join" a community like they would follow any other user, and tweets from that community will appear in their feed. Communities have moderators and rules attached to them, and posts must be explicitly attached to a community in order to appear in its feed. Communities can be referenced from thor tweets using the ampersand (&) character, like you might reference a hashtag or another user.

# Briefing

<img class="img-fluid" src="{% link assets/img/a2_briefing.png %}">

**Type:** Invention

**Problem:** Users don't have a good way to "catch up" on tweets they've missed since they've opened the app, and the feed can feel like a bottomless pit of tweets.

**Purpose:** Provide users with a time-bound way to catch up on Twitter after some time away without sucking them into infinite scrolling.

**Operational Principle**: When the user opens Twitter after a longer duration, a "briefing" panel will be presented to them, with a choice of how long the tweets should go back. The default choice will catch the user up on the most relevant tweets they've missed since they closed the app. Users can dismiss the panel whenever they are done with it.

# Reading List

<img class="img-fluid" src="{% link assets/img/a2_reading_list.png %}">

**Type:** Adoption (from apps like Pocket)

**Problem:** Users might find interesting articles while browsing Twitter, but want to go back to read them later when they have more time or want to leave the feed.

**Purpose:** Provide users a helpful place to store and scroll through articles that they want to read later.

**Operational Principle**: Tweets that are identified as containing a link to a news article have a button attached to the link description to send this article to the reading list. When a user views their reading list, they can see a link to the article and how long the article will take to read. Once they've read the article, they can choose to engage with the tweet where the article originated from or mark it off their list.

# Alert System

<img class="img-fluid" src="{% link assets/img/a2_alert.png %}">

**Type:** Adjustment (from Twitter's existing post notification feature)

**Problem:** Many organizations use Twitter as a way to alert their followers of timely things happening in their community, including things that may put their followers at risk.

**Purpose:** Provide users with a way to surface tweet notifications at a higher priority through Time Sensitive notifications or text messages.

**Operational Principle**: Accounts can choose to "offer alerts" and users can choose to subscribe to them, with settings for sending higher priority notifications or sending texts with the alert. When an account marks a tweet as an alert, users will receive the tweet in the way they've configured.

# Profile Status

<img class="img-fluid" src="{% link assets/img/a2_status.png %}">

**Type:** Adoption (from apps like Slack)

**Problem:** Users can't show ephemeral information on their profile without editing their biographical information.

**Purpose:** Provide users with a casual and ephemeral way to show what they're up to.

**Operational Principle**: Users will see a button next to their name with the option to set a status. They can pick an emoji and a short piece of text that will get displayed next to their name atop their profile. There's more possibilities to enable automatic expiration of the status or themed ones for popular events.

# Thread Reader

<img class="img-fluid" src="{% link assets/img/a2_threads.png %}">

**Type:** Adjustment (of Twitter's existing thread features)

**Problem:** It's clunky to read a long string of threads, as they're separated by all the Tweet metadata and like/retweet/share buttons.

**Purpose:** Provide a cleaner way to read threads more akin to reading an article.

**Operational Principle**: Tweets that have a long set of replies posted together (commonly thought of as a thread) can get expanded in a view that leaves out much of the existing tweet metadata and reads more like an article. Replies to the top tweet are now bunched together at the bottom, and clicking on any of the individual tweets opens the existing tweet view with all of the like/retweet/share features.

[assignment]: https://61040-fa22.github.io/assignments/assignment-2