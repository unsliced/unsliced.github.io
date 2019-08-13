---
layout: post
title: Ring fudge on Sonos 
tags: ring sonos alexa
permalink: /posts/ring-sonos-fudge/
---

## Alexa 

The Ring doorbell should be able to fire an Alexa speaker to act as a doorbell, i.e. play a short chime. 

The trouble seems to be that the [Sonos implementation of the Alexa API doesn't react](https://en.community.sonos.com/smart-home-integrations-229108/ring-doorbell-with-sonos-one-6820732), so while the Ring doorbell event fires, Sonos does not react. 

In the short term, I've created an [IFTTT](https://ifttt.com/applets/103096864d-if-new-ring-detected-at-front-door-then-play-doorbell-sounds-in-kitchen) trigger which plays a Spotify playlist of a doorbell. It's not a great solution, e.g. you have to tell the Sonos to stop the track, but it will do for now. 

 