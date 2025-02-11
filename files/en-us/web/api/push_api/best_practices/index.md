---
title: Web Push API Notifications best practices
slug: Web/API/Push_API/Best_Practices
tags:
  - Apps
  - Beginner
  - Best practices
  - Guide
  - Notifications
  - Push
  - Push API
  - Usability
---


This article provides a useful summary of best practices to keep in mind when developing web sites and applications that use Push Notifications for user engagement.

> “If done well, it's nice to have, but if not done well, it's really annoying.” — Overheard conversation between two browser developers discussing the ethics of push notifications.

## Overview of web push notifications

Web Push Notifications (created using a combination of the [Notifications](/en-US/docs/Web/API/Notifications_API), [Push](/en-US/docs/Web/API/Push_API), and [Service Worker](/en-US/docs/Web/API/Service_Worker_API) APIs) are part of the rising noise that product developers and marketers are using to get attention for their sites. Searching the web for "web push notifications," you'll find articles from marketing experts who believe you should use push to re-engage people who have left your site so they can complete a purchase, or be sent the latest news, or receive links to recommended products.

### The dark side

Their novelty provides a new and unexploited opportunity for enterprising sites to reach potential customers. Has the customer switched tabs to answer an email? Win them back with an expiring offer of free shipping that they can’t ignore!

But really, is this the best use of push notifications? Or is it a new iteration on the old and tired pop-up ad?

> “Web push doesn’t risk ending up in the spam folder. Nor can it be blocked by ad blockers. It shows right up on your desktop even when the website is shut. In mobile, it shows up in the notification tray, just like app push notifications, even when the browser is not running.” — an unnamed marketing site

### Positive uses of push

But there’s a bright and useful side to push notifications, too. Let’s say you and your team commonly use a chat program to communicate, but today you’re happily working somewhere, and problem comes up. Say your program manager found a hiccup in the approvals and wants to get your feedback on something before she proceeds.

After a few failed attempts to get your attention, they send you an email, and your email app produces a push notification that successfully alerts you, even though your mail web app is not open.

In this document, we’ll talk about the ethical use of web push notifications. Sometimes they can eliminate frustration and annoyance, and sometimes they can cause them, and it’s up to you as a developer to make wise recommendations (and decisions) about the use of push notifications.

## What are you hoping to achieve with this push notification?

As with everything, with great power comes great responsibility. Every push notification should be useful and time-sensitive, and the user should always be asked for permission before sending the first one, and be offered an easy way to opt out of getting more in the future.

There are some basic questions you can answer to determine if a push notification is needed:

- Is there someone waiting in real-time for a response? In our above example, the program manager is awaiting your response and so a push notification is appropriate.
- Is up-to-the minute updating necessary? I use a service that aggregates different social media news sources. When a story I’m interested in is trending, I’d like to get a notification!
- Is there breaking news that is timely? This is where it gets a little tricky. Sometimes news sites request push notifications so they can essentially say "Look at me! Look at me!" It all comes down to what the user wants, and you can use behavior to determine intent. For example, if the user views more than one article, or lingers on your page for several minutes, they may be interested in receiving updates.

In addition to the question of whether a push notification is required at all, there are many different types of push notifications, ranging from casual-and-disappearing to persistent-and-requiring-interaction.

We caution you to use the interaction-requiring ones very sparingly, since they can be the most annoying. Your notifications should be assistive, not disruptive.

## Building trust

Some studies have shown that as many as 60% of push notifications are blocked. Allowing your site to push notifications in realtime requires trust. You can build trust by having a well-designed website that provides good content that shows respect for the user, and a clear value to accepting push notifications.

## Browser mitigations

Because of abuses of push notifications in the past, web browser developers have begun to implement strategies to help mitigate this problem. For example, Safari 12.1 now requires—and other browsers either already do, or are planning to do so—that the user interact with the page in some way before the page can request permission to perform push notifications. This at least prevents the user from getting spontaneously asked this question on web pages thaty've only glanced at once may rarely if ever look at again.

In the case of Firefox, see {{bug(1524619)}}, in which we find that Firefox 68 implements this, disabled by default, behind the preference `dom.webnotifications.requireuserinteraction`.

## See also

- [Notifications API](/en-US/docs/Web/API/Notifications_API)
- [Using the Notifications API](/en-US/docs/Web/API/Notifications_API/Using_the_Notifications_API)
- [Push API](/en-US/docs/Web/API/Push_API)
