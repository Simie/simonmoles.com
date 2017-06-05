---
title: "Precision Engineering"
thumbnail: "/assets/images/thumbnails/pe.jpg"
permalink: "/projects/precision-engineering/"
frontpage: true
description: "Popular mod for Cities: Skylines. Adds angle snapping, guidelines when building roads."
---

![Banner][banner]

Precision Engineering is a mod for [Cities: Skylines][cities_skylines]{:target="_blank"} that adds snapping and measuring tools when placing roads, power lines, pipes, etc.

# Development

Cities: Skylines is created with the Unity game engine. This makes it relatively straightforward to decompile the C# assemblies and investigate how things work. The game's developers, Colossal Order, also provided a powerful mod API that allowed loading any C# DLL.

I was able to dig deep into the road placement code to discover where I can hook in to display information to the user and enable angle snapping. Using a snippet of code provided by [cope][cope] I was able to override the built-in methods used for road placement to implement custom snapping behaviour without modifying the game's DLLs.

<div style='position:relative;padding-bottom:57%; margin-bottom: 10px;'><iframe src='https://gfycat.com/ifr/DifferentIgnorantAplomadofalcon' frameborder='0' scrolling='no' width='100%' height='100%' style='position:absolute;top:0;left:0;' allowfullscreen></iframe></div>

# Reception

Precision Engineering released in May 2015 and sat at #1 most popular on the Workshop front page for almost a year. It currently sits at the #3 most subscribed mod of all time for Cities Skylines with over 500,000 subscribers, and continues to gain more each day.

I created a [series of gifs][gifs] to show off the mod to potential users. This proved very popular, and inspired a trend that other popular mods followed.

Colossal Order implemented a very similar set of features into the base game in May 2017. This has slowed the flow of new users. However, since it does not implement the entire feature set of Precision Engineering, there are still over 1000 new users each day.

<div style='position:relative;padding-bottom:57%; margin-bottom: 10px;'><iframe src='https://gfycat.com/ifr/FrighteningGlitteringAustralianfreshwatercrocodile' frameborder='0' scrolling='no' width='100%' height='100%' style='position:absolute;top:0;left:0;' allowfullscreen></iframe></div>

### Links
- [Steam Workshop Page][steamcommunity]
- [Reddit Release Thread][reddit_thread]
- [Github Repo][github_repo]

[banner]: {{"/assets/images/pe/header.jpg" | relative_url }}

[cities_skylines]: http://store.steampowered.com/app/255710/Cities_Skylines/
[steamcommunity]: http://steamcommunity.com/sharedfiles/filedetails/?id=445589127
[reddit_thread]: https://www.reddit.com/r/CitiesSkylines/comments/37i4ls/release_precision_engineering_updated_guide_lines/
[github_repo]: https://github.com/Simie/PrecisionEngineering
[cope]: https://github.com/sschoener/cities-skylines-detour
[gifs]: http://imgur.com/voLHeOi