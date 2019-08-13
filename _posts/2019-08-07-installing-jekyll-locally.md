---
layout: post
title: Installing Jekyll 
tags: jekyll 
permalink: /posts/installing-jekyll/
---

Following [the instructions](https://jekyllrb.com/docs/installation/windows/) was pretty straightforward. 

I did then also have to install the `jekyll-sitemap` and `jekyll-feed` gems. 

It's not clear what it does but 
```bash
sudo jekyll build 
```

followed by the more obvious 

```bash
sudo jekyll serve --watch 
```

to produce a [live local version](http://127.0.0.1:4000). 