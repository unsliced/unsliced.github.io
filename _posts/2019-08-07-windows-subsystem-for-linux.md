---
layout: post
title: Windows Subsystem for Linux 
tags: windows admin
---

The [WSL](https://docs.microsoft.com/en-us/windows/wsl/about) allows you to run most of the command line tools directory on Windows. This is a **good thing**. 

Run the PowerShell as Admin, then reboot. 

Install a suitable distro from the Windows Store. 

Run it, setting a new UNIX username and password (hint: [/tags/passwords/](LastPass)). 

Then update the distro: 

```bash
sudo apt update && sudo apt upgrade
```


