---
layout: post
title:  "How to make your WiFi Magilights even more magical"
date:   2017-03-23 02:49:29 +0000
---


Recently I purchased [MagicLight WiFi Smart LED RGB Light Bulbs](http://a.co/56MsesY) to brighten up my room. After installing them and playing with the android app I noticed there was no Web Gui or portal to control them. So I decided to take action and create one myself [here](https://github.com/mystycs/magiclight-web). I wanted to do this because I was annoyed of always pulling my phone out to change the lights. This way I could run it on a local server and just pull up a local page to control them.

The first action step was to figure out how to communicate with them. Having prior networking experience I assumed it was going to be over some TCP protocol so I decided to install a packet collector on my phone. Doing so I collected a bunch of data and started to dechiper the data that was collected.

![](http://i.imgur.com/vuFC3rV.jpg)

![](http://i.imgur.com/mB5C5qo.jpg)

After looking it over i quickly noticed the following below:

The lights communicate by TCP packets over port 5577.

To turn on youll send `71230fa3` 
To turn off youll send `71240fa4`

To change a color its `31 + (HEX Color Code) + 00F00F(magic hex) + checksum(sum of all bytes % 256)` ei: `3100FF0000F00F2E`

I used the socket class that came with rails to communicate with the lights via TCP.

![](http://i.imgur.com/Da8lp21.jpg)

The app i created below contains much of the same functionality as the MagicHome Pro app via Android. I am still adding more everyday.

![](http://i.imgur.com/dp0238i.jpg)


Now my life has become much easier as I dont always have to pull out my phone to control my lights.
