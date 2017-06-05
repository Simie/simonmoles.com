---
title: "SRDebugger"
thumbnail: "/assets/images/thumbnails/srdebugger.png"
permalink: "/projects/srdebugger/"
frontpage: true
date: 2015-02-07
description: "Runtime console & tools for Unity games."
order: 0
---

Console & Tools On-Device for Unity Games
===

SRDebugger is a runtime console and tool system for the Unity game engine.

![Banner][banner]

Motivation
===========

One of Unity's primary advantages is fast iteration. Unfortunately, this advantage doesn't apply when deploying and testing on mobile platforms. The long export and deployment times can make tweaking values on mobile excruciatingly slow. While working on Unity games for iPad at Tigerface Games I encountered issues like this nearly every day:
- Bugs or errors while demoing the game and no debug log available.
- Wanting to demonstrate some feature, but the feature is behind a locked level.
- Tweaking parameters would take ages due to slow export + deploy.

I created SRDebugger as an attempt to fix all of these issues.

Development
===========

SRDebugger began as the debug panel for my own [iPad game][nova]. As I added more features, I began to realise this would be a useful product for other developers. My time working with Tigerface Games on their projects solidified this belief. I started to refactor the code to make it suitable for importing into other projects, and created a new game-agnostic UI.

SRDebugger was released on the Unity Asset Store in February 2015. It received favourable reviews from customers and continues to sell well to this day. I continue to improve and add features based on user feedback.

Features
==========

SRDebugger is structured so that the monitoring systems can execute without the UI being loaded. This loose coupling enables SRDebugger to have a minimal performance footprint when not in use, but it can be brought up at a moments notice when required. This was an essential requirement for including SRDebugger in all builds of a product.

The Options panel is my personal favourite feature. It makes it incredibly easy to tweak the _look and feel_ of a game by pinning a property to the screen and adjusting it on the fly. I've used it for calibrating touch control sensitivities and animation speeds. It can also trigger methods, in my case I have commands like "Win Battle", "Reset Battle", "Give Money", to quickly reach the part of the game I need to test.

![Options Panel Example][options_usage]
*The options panel can tweak gameplay parameters and execute methods.*

Another major aim for SRDebugger was for it to be "plug and play". I wanted the user to be able to import the plugin and be up and running in minutes. On the first import, a quick guide will appear telling the user how to access SRDebugger in their game. The next time they run their game, SRDebugger is ready to go. The runtime console uses the built in Unity log callback to retrieve the debug logs output by the standard Unity `Debug.Log()` method. The user doesn't have to change any of their logging code to start using SRDebugger.

![Welcome Screen Example][welcome_screen]
*The welcome screen greets new users and explains how to get started.*

The built-in bug reporter component communicates with my API server to forward the console log, (anonymised) system info, user email, message, and a screenshot of game to the developers email address. The reporter can be accessed from the panel or brought up with the SRDebugger API. This way the developer does not have to grant access to the entire debug panel to allow their users to report bugs. As browsing long logs on a touch device can be tedious, I use this service internally to send the console log to my PC where I can search and filter it as required.

Reception
==========

I was very fortunate to have a few very enthusiastic customers on my first day of release. Their great feedback and bug reports really helped the product get some momentum. A few months after release I was asked by Unity to include SRDebugger in their second "Level11" sale for Unity Pro subscribers. This steep discount propelled SRDebugger onto the front page for a number of weeks and led to a great number of positive reviews and purchases by non-Level 11 users.

Since then there has been a steady stream of sales, usually keeping SRDebugger on the first page of the _Scripting/Other_ category on the Asset Store. Further sales and promotions by Unity have led to a few very good months for SRDebugger.

As of May 2017, SRDebugger has sold over one thousand copies and has over one hundred reviews on the Asset Store.

Challenges
==========

The design aspect of the project was challenging for me. Creating a design for the panel, marketing materials, documentation, and website was significantly more time consuming that I had expected. The actual development of the debug panel turned out to be the easiest part of the project. However, I am pleased with the end result and subsequent updates to the product have been much faster now I have an established design style and company website. I am especially happy with the SRDebugger [product pages][product_page] with the auto-play video in the header demonstrating each main feature of the panel.

SRDebugger uses the new Unity UI system that was introduced in Unity 4.6 and Unity 5.0. Supporting older versions of Unity has made it hard to adopt the latest features, and workarounds have been required for changes in the API in later versions.

Links
==========
- [Product Page][product_page]
- [Asset Store Page](https://www.assetstore.unity3d.com/en/#!/content/27688)

[product_page]: https://www.stompyrobot.uk/tools/srdebugger
[banner]: {{"/assets/images/project_srdebugger/banner.png" | relative_url }}
[options_usage]: {{"/assets/images/project_srdebugger/options_usage.gif" | relative_url }}
[welcome_screen]: {{"/assets/images/project_srdebugger/welcome_screen.gif" | relative_url }}
[nova]: {{ site.baseurl }}{% link _posts/projects/2017-06-04-nova.md %}