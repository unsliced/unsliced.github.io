---
layout: post
title: Wireless Networking Monitoring
tags: wifi network python linux pi 
permalink: /posts/network-monitoring/
---


## Python solutions 

Using [probemon](https://github.com/nikharris0/probemon)
	- [Logging probe packets with probemon](https://null-byte.wonderhowto.com/how-to/log-wi-fi-probe-requests-from-smartphones-laptops-with-probemon-0176303/)
	- [using probemon](https://www.jbrandsma.com/news/2018/01/02/catching-wifi-probes-using-a-raspberry-pi/)


# On Linux 

After installing `netaddr` and `scapy` it's time to play: 
	- sudo airmon-ng - to check what's attached 
	- sudo airmon-ng start *interfacename* - to start the monitoring from a particular antenna 
	- *it might suggest check kill - best not in my limited experience, it will probably kill the main wifi connection* 
	- sudo airmon-ng - to check what the new monitoring interface name is called 
	- sudo airodump-ng iname - a realtime view 
	- e.g. sudo python3 probemon.py -i wlan0mon -f -s -r -o ./2020-01-01-location.log
		- -l for stdout 
		- -r is for the strength of the signal which doesn't seem to work on Linux 

## WPA cracking
[Cracking WPA passwords](https://www.thepolyglotdeveloper.com/2018/06/crack-wireless-passwords-raspberry-pi-aircrack/) certainly gave some ideas (in particular using the [Aircrack-ng](https://www.aircrack-ng.org/doku.php?id=Main#documentation) suite, include [airmon](https://www.aircrack-ng.org/doku.php?id=airmon-ng)). 

## Pi and Linux projects
Interesting projects include: 
	- a [go based pi solution](https://github.com/meyersj/wifi). 
	- a [pi network scanner](https://makezine.com/projects/build-raspberry-pi-network-scanner/)
	- [Kismet](https://kismetwireless.net/) looks to be very useful. 



