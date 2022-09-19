---
layout: post
assignment: 1
categories: assignment
title: Twitter Critique
subtitle: Let's talk about tweets
description: Assignment 1 for 6.1040, a critique of Twitter and its design based on a Value Sensitive Design framework.
---

For more details on this assignment, [check out the assignment post][post]{:target="_blank"}.

1. TOC
{:toc}

# Introduction

The purpose of this assignment is to offer a design critique of Twitter, so we can highlight some of its strengths and flaws as we develop our Twitter clone, Fritter.
To do this, we'll take a look at Twitter from two perspectives: [**Value Sensitive Design**][VSD]{:target="_blank"} and [**Need-finding interviews**][NFI]{:target="_blank"}.

**Value Sensitive Design** (VSD) will help us take a look at how Twitter is designed to explore the long-term effects of its design on its users and the world. 
**Need-finding interviews** let us put these values into context with observations of how real users are using Twitter today.

# Looking at Twitter's Design with VSD

To study Twitter's design, we'll break them down based on the VSD framework into **stakeholders**, **time**, **pervasiveness**, and **values**.

## Stakeholders

Stakeholders with respect to a piece of software include everyone who is impacted, directly or indirectly, by that software's use.
In this case, we're going to look at *who* Twitter's existence impacts and *how* it impacts them with two examples: Russian bots and Presidential account handovers.

### Non-Targeted Use

During the lead-up to the 2018 midterm election, Twitter was facing pressure from the government to disclose information about the large number of Russian bots on its platform.[^1] 
Just like with Facebook, peddling of disinformation was a significant issue on Twitter before the 2016 election of Donald Trump. Many of these bots tweeted incendiary right-wing content, trying to stir up support for extreme causes and destabilize the American political sphere.[^2]

Twitter has spent the time since addressing these bots and has added [labels for government affiliates and state media][labels], but these processes aren't perfect. Tools like [Botometer] have sprung up to try to spot "authentic" users of Twitter and distinguish them from malicious bots. Even verified accounts can't be trusted, as they are even more prone to hacking than the average Twitter user for their valuable blue check.[^3] More work needs to be done by Twitter to try to promote authenticity in its platform and stop nefarious actors flooding the platform with spam and disinformation.

### Changing Hands

Twitter conveniently lets users change their handles, profiles, and names whenever they want, though this has led to much confusion and some hilarity when prominent Daily Show correspondent and comedian Jaboukie [used this feature to impersonate prominent accounts and got himself suspended from the platform](https://www.insider.com/jaboukie-giabuchi-twitter-suspended-blue-checkmark-verified-cnn-joe-biden-2020-3).
Famously, Twitter also orchestrates an official handover of a significant number of accounts for US Presidential administrations, archiving old accounts and copying over followers from the transitionary ones.[^4]

Every time an account changes hands or changes a profile presents an opportunity for spam or confusion.
In Fritter, this could be resolved by making the account usernames work a bit more like email. You can't change your email address once you make it, but you can add aliases or forward from one account to the other.
Fritter could still show your old alias on your old tweets but show them together in one "combined" account view with the most recent handle shown on the account. Under this model, @POTUS in Fritter might redirect to @POTUS46, so that one person or organization is always associated with one handle.

## Time

A VSD analysis of time considers how a piece of software will be used long into the future. Will generations of people come to rely on it only to have it fall apart? Will new unexpected uses of Twitter emerge and what will they look like?

My analysis will cover how Twitter is being reappropriated from more traditional uses, and how people who don't use Twitter might be affected in the long run.

### Reappropriation

With its short post format and easy-to-use API, Twitter lends itself to a lot of interesting use cases.

- One neat usage of Twitter is as an **alert engine**, with a good example being [MIT Alert](https://twitter.com/mitalert). Because Twitter supports push notifications for new tweets, I have Twitter send me a notification every time MIT Alert posts a Tweet. This can be a super effective way of keeping tabs on something or creating a community alert system. However, if Twitter does go down, the stakes are now much higher, as people won't be able to receive timely updates if they are in danger.
- Another way Twitter can be used is as a **repository for automated creativity**. Many interesting projects have emerged on the site. On the less creative end, there's [a progress bar that tracks how far into the year we are](https://twitter.com/year_progress). On the more creative end, there's a bot that [mashes up two emoji together to make a new emoji](https://twitter.com/EmojiMashupBot). While neither of these are particularly critical or interesting on their own, they go to show that a creative bot community is alive and well on Twitter, likely due to the platform being more permissive of automated accounts than elsewhere. This permissive attitude towards bots, however, requires Twitter to strike a delicate balance between what is and isn't an acceptable use case for automation.

### Choosing Not to Use

Twitter is such a pervasive platform now that it is difficult in some industries, especially news and politics, to not be on Twitter. In fact, Pew Research found that one-third of all tweets from U.S. adults are about politics, and that 78% of them are from people 50 and older.[^5]

If politicians are spending their time looking for feedback on their performance, they may be missing broad swaths of their constituents simply by checking Twitter. However, as many conversations and debates between journalists and politicians occur on Twitter nowadays, choosing not to use Twitter may take you out of the political conversation entirely. Also, it is getting harder to read Twitter without an account[^6], endangering people that would prefer to stay anonymous in their browsing.


## Pervasiveness

Pervasiveness analyses of software look at what happens when the software lands in the hands of nearly everyone in a group of people. How will people interact, and where might the design break down if everyone has it?

My analysis will cover how social media behaves in different political contexts and how Twitter might be different with widespread use.

### Political Contexts

**In the United States,** Twitter is broadly protected by [Section 230 of the Communications Decency Act][230], which gives it the freedom to set [its own rules][rules] around safety, harassment, and hate speech. Twitter can decide what it thinks belongs on its platform. Users in the U.S., for the most part, feel empowered to speak their opinions online, and Twitter will leave them up. Some right-wing copies of Twitter have sprung up recently, such as Parler and Truth Social, as some communities believe that Twitter's moderation of its platform impacts them disproportionately.

**In China**, platforms like Douyin, Weibo, and WeChat are highly moderated with automated tools and with government censors.[^7] Citizens do not have the freedom to speak out about their government, and if they do, they may face stiff penalties that would be foreign to Americans who are used to the anonymity provided by the internet.

This comparison goes to show that social media that perform well in one political context may face huge restrictions in another. If Twitter wanted to operate in China, it would need to give the Chinese government unfettered access to all of its tweets to determine which ones to censor, or it would need to block all outside tweets, severing the expectation of freedom that exists in the US on its platform.

### Widespread Use

While Twitter has greatly expanded the flexibility of its platform in recent years, with better quote tweets, a threaded tweet composer, and 280-character tweets, it still lacks many features that might be necessary for a global platform with billions of users. A couple notable ones are:

- **an edit button** - Twitter is rolling out the ability for users to edit their tweets with limitations, and only for paying customers.[^8] Critical features like this will need to be ironed out, with clear expectations on what an edited tweet looks like, before users can place their trust in Twitter.
- **longform posts** - Tweet threads are nice, but a cumbersome way to post long pieces of content. Twitter has acquired Revue to help tackle this problem,[^9] but it's aimed at writers more than an average user. More flexible posting styles may be needed before Twitter can become ubiquitous.

## Values

Finally, the last part of our analysis will look at what values Twitter inherently reflects with its design. A good piece of software should have values that align with what are important to its users and its stakeholders.

### Choosing Values for Twitter

Twitter has always tried to have a frictionless posting experience, from its early days when it was a texting service[^10] to it's simple "What's happening?" prompt. Many of Twitter's strengths and weaknesses come from it being the center of attention. With this in mind, Twitter should ideally reflect the following values:

- **expression**: Twitter is a very expressive platform, and some of the most viral content on the internet is either tweets or screenshots of tweets posted on other platforms. Twitter should do everything it can to keep its creators and thought-leaders, and it should listen their concerns on how to improve the platform.
- **self-efficacy**: Twitter users and their communities should feel empowered to take ownership of the platform for their own advocacy, without the fear of being harassed.
- **security**: As a smaller platform, Twitter has struggled with security in recent years. Most notably, a group of teenage hackers were able to steal credentials from inside the company that allowed them to make big changes on the platform, including posting tweets on behalf of unsuspecting users.[^11] This type of security posture is unacceptable, as it leaves users unsettled around the safety of their personal information and identity on the platform. Twitter should make a renewed push for security, as some of the world's most vulnerable activists rely on it for their work.

### User Experience of Values

A company's values aren't important unless they are actually represented in their software. Twitter has always had a unique ability to bring the most creative and thought-provoking content to their platform, and their platform continues to support this effort. Twitter's retweets and likes features allow popular content to go viral with ease, and many Twitter users remark on how the best jokes can always be found there. Additionally, new features are attempting to attack misinformation by encouraging users to read articles before they reshare them.[^12]

However, Twitter has also traditionally had a huge harassment problem, causing many of their users to feel unsafe speaking out against other users with large and passionate followings (e. g. Elon Musk). Twitter will need to make sure that their most vulnerable users are supported, and they will have to find more creative ways to defend against pile on attacks that are mounted on their platform.

# Looking at Twitter's Design through Interviews

To dig deeper into my analysis of Twitter, I wanted to find a couple people that would have differing use cases for the platform. So, I interviewed my grandpa, Steve, who checks Twitter a few times a day, and a friend at Caltech named, Eitan, who remarked to me that he was aspiring to get more into the platform.

## Interview with My Grandpa Steve

I wanted to talk to my grandpa about his Twitter usage because I thought it could provide an interesting parallel to the typical social media target audience of young tech-savvy users. My grandpa reads a variety of magazines with interests in politics, Catholicism, and social justice, and as a result, he wants to be able to follow his favorite authors outside of the specific magazine articles and get their thoughts on timely issues. He treats Twitter as a secondary news feed to his traditional news consumption, where he can get a broader set of opinions and ideas that are linked to current events.

Although he does worry about "becoming unbalanced" by only following his favorite authors and academics, he doesn't look to Twitter to discover new accounts to follow. He expressed a concern of falling into rabbit holes on social media, so he largely avoids reading replies. When asked about how he shares online, he said he doesn't feel a need to tweet, as he isn't running for office and would be worried about saying something ignorant or uninformed.

What surprised me most about my interview with my grandpa is that how uniformly Twitter is a positive experience in his life. He doesn't feel a need to discover other accounts or users on the platform or engage with viral trends. He follows a small set of accounts, reads his news feed daily, and gets value from hearing interesting thoughts from his favorite journalists. The simplicity of Twitter's feature set benefits him specifically, so adding more features for discovery, posting, or searching Twitter would not impact, or potentially even hurt, his user experience.

## Interview with Eitan

In comparison to my interview with my grandpa, my interview with Eitan was much more focused around comparing Twitter to other social networks that he and his friends might be using. I wanted to get a sense of where he thought Twitter fit in in the landscape of social media platforms and to hear his frustrations and excitement about it.

Eitan mostly compared Twitter to other social media that he is using, like Reddit and Instagram. He particularly liked Twitter because it felt like a platform where you can get substantial news from agencies, public figures, and celebrities that is lacking on Instagram and Reddit. He gave some examples of being able to read about the status of backroads into parks from CalTrans or announcements from his favorite bands. He also liked the speed at which information appeared on Twitter and that it was easy to look up a hashtag to use Twitter as a "crowdsourced" alert system for things happening in his area.

Eitan also talked a bit about why he particularly disliked other platforms such as Instagram, Snapchat, and TikTok for feeling more "predatory". He didn't like how unnaturally "fast" TikTok was or the spam-like push notifications that Instagram sends. He felt like posting pictures on Instagram was serving as a shortcut for social interaction, whereas he felt he could learn something meaningful by using Twitter or Reddit. At the end of our interview, he made an interesting remark about how social media is a "truly human" invention, but the tech in the loop can "hijack" our natural social tendencies.

My interview with Eitan produced some fascinating thoughts about social media in general. It was interesting how the focus of Instagram and Snapchat on online personalities made these platforms feel "icky," whereas the focus of Reddit and Twitter on sharing information publicly made them feel more honest and well-intentioned. Eitan appreciated the fact that Twitter didn't resort to growth-hacking, attention-grabbing behavior, like sending spammy notifications or implementing addictive full-screen video scrolling. As Twitter grows, it ought to look to its core base of users before copying features from other platforms that might drive these people away, as it might ruin its "authentic" feel.


[^1]: [*Twitter released 9 million tweets from one Russian troll farm. Here’s what we learned.*](https://www.vox.com/2018/10/19/17990946/twitter-russian-trolls-bots-election-tampering) (Vox)
[^2]: [*The Agency*](https://www.nytimes.com/2015/06/07/magazine/the-agency.html) (New York Times)
[^3]: [*Hacked verified Twitter accounts continue to spam Elon Musk*](https://www.teslarati.com/verified-twitter-spam-elon-musk/) (Teslarati)
[^4]: [*What to expect on Twitter on US Inauguration Day 2021*](https://blog.twitter.com/en_us/topics/company/2021/inauguration-2021.html) (Twitter Blog)
[^5]: [*Politics on Twitter: One-Third of Tweets From U.S. Adults Are Political*](https://www.pewresearch.org/politics/2022/06/16/politics-on-twitter-one-third-of-tweets-from-u-s-adults-are-political/) (Pew Research Center)
[^6]: [*Can't read Twitter at all without an account*](https://news.ycombinator.com/item?id=29947636) (Hacker News)
[^7]: [*The Communist Party thinks China's prolific censors are not censoring enough*](https://www.cnn.com/2021/12/15/tech/china-weibo-censorship-fine-mic-intl-hnk/index.html) (CNN)
[^8]: [*Twitter’s edit button is a big test for the platform’s future*](Twitter’s edit button is a big test for the platform’s future) (The Verge)
[^9]: [*Twitter acquires newsletter platform Revue*](https://techcrunch.com/2021/01/26/twitter-acquires-revue/) (TechCrunch)
[^10]: [*Twitter turns off its original SMS service in most countries*](https://www.theverge.com/2020/4/27/21238131/twitter-sms-notifications-disabled-jack-dorsey-hack) (The Verge)
[^11]: [*Teen ‘mastermind’ behind the great Twitter hack sentenced to three years in prison*](https://www.theverge.com/2021/3/16/22334421/twitter-hacker-bitcoin-plea-deal-agreement-graham-ivan-clark-three-years) (The Verge)
[^12]: [*Twitter is bringing its ‘read before you retweet’ prompt to all users*](https://www.theverge.com/2020/9/25/21455635/twitter-read-before-you-tweet-article-prompt-rolling-out-globally-soon) (The Verge)

[post]: https://61040-fa22.github.io/assignments/assignment-1
[VSD]: http://www.envisioningcards.com/?page_id=2
[NFI]: https://61040-fa22.github.io/assets/lecture-notes/L2.pdf
[labels]: https://help.twitter.com/en/rules-and-policies/state-affiliated
[Botometer]: https://botometer.osome.iu.edu/
[230]: https://www.eff.org/issues/cda230
[rules]: https://help.twitter.com/en/rules-and-policies/twitter-rules