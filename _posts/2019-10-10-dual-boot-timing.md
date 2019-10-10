
---
layout: post
title: Dual boot timing issue  
tags: linux windows  
permalink: /posts/dual-boot-time-issue/
---

The problem was that after having booted into Linux, the next time Windows loaded it would show the incorrect time (generally an hour earlier). [Apparently](https://www.maketecheasier.com/fix-windows-linux-show-different-times/) this is because Linux assumes the motherboard time to be UTC, while Windows assumes it to be local. 

(So I could either wait until the clocks change, or fix it - the laptop is right for half the year.)

The solution is to either change the way Linux behaves, or Windows. It is generally  considered easier to do the former. 

```bash
timedatectl set-local-rtc 1 --adjust-system-clock
```

This will tell the system to interpret your motherboard’s stored time as local time. Linux will no longer apply time zone adjustments to the time stored on the motherboard. As a result, your clocks will sync.

(A 0 would reverse and be considered as UTC.)