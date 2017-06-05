---
title: 'New Blog, Hello World'
---
### Hell, It's About Time

It's been a while since I updated my personal site. My old site was made during 2010 (!) and was really beginning to rot.
The tipping point was when I noticed my clever bracket design looked terrible if the user happened to have the Raleway font installed on their PC, rather than using the version served from my site. So, away with all that. 
Renovating this site also gave me an opportunity to brush up on all the latest web technologies. CSS is a joy to use now that all browsers support the features that were held back by Internet Explorer back when I last worked on this site. Rounded corners? Box sizing? Filters? Media queries? Calc!? Nice.

<!--more-->

### Enter SSG (Static Site Generator)

A blog rarely updates, so it makes no sense to have a CMS running when each request usually returns pretty much the same result. 
A static site generator takes the data source and generates a set of html files that can be served from any web host. 
This has a number of advantages:

- Reduced chance of site being compromised by vulnerabilities in e.g. Wordpress.
- No need to set up databases, PHP, etc on web host, or when moving.
- Easier to scale during times of increased traffic. Just copy the files to a CDN based host.
- Site loads __super fast__. It's just serving html!

I decided on using [Jekyll][jekyll] for this new site. I have used it before for my [company website][stompy_robot], so I was already familiar with how it all works. 
An alternative could have been [Hugo][hugo], but it seems to have less buzz around it, and I'm less familiar with Go than I am with Ruby.

### Open Source

I used a starter project called [Fresco][fresco] to get everything up and running. This saved me having to scour the documentation to find the best practices for each technology and get something working fast.
The source is available to view on [Github][repo]. I've set up Travis to automatically build and test the site. HTML-Proofer checks for missing links, broken images, that sort of thing. No more broken links.

This was also a good opportunity to try out the new WSL build in the latest Windows 10 update. This fixes the networking issues I had with Jekyll last time I tried using WSL.
The latest build works perfectly, so I'm able to run everything in a bash shell just as if I was working on a Mac or Linux. No more scrappy workarounds when using Ruby on Windows!

[jekyll]: https://jekyllrb.com/
[hugo]: https://gohugo.io/
[stompy_robot]: https://www.stompyrobot.uk/
[repo]: https://www.github.com/Simie/simonmoles.com/
[fresco]: https://github.com/ixkaito/frasco
*[WSL]: Windows Subsystem for Linux