---
layout: post
title: Live Lower Third to Zoom/Meet with OBS  
tags: bad21 obs zoom video meet ubuntu
permalink: /posts/obs-lower-third/
---

Obs-Studio is a great tool for mixing video sources, editing (including audio) tracks, overlays and so on.  It's great. 

You can set up a virtual camera, output the mixed signal and then hook it up to a video consuming app, e.g. Zoom or Google Meet, so as to be able to create a live lower third to put new information onto the screen. 

On Ubuntu using [CatxFish](https://github.com/CatxFish/obs-v4l2sink) which will also need the [v4l2 loopback](https://github.com/umlaeute/v4l2loopback#run) enabled. 

One thing to note, `catxfish` needs `obslib-dev` which itself needs `libobs0`, the issue here is that the latest obs-studio is (at the time of writing) `26.1.1-0obsproject1~groovy` - but `libobs0` needs this to be downgraded to `26.0.2+dfsg1-1`. 

No biggie. 