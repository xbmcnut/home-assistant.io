---
layout: page
title: "Samsung Smart TV"
description: "Instructions on how to integrate a Samsung Smart TV into Home Assistant."
date: 2016-02-13 12:02
sidebar: true
comments: false
sharing: true
footer: true
logo: samsung.png
ha_category: Media Player
featured: false
ha_release: 0.13
---

The `samsungtv` platform allows you to control a [Samsung Smart TV](http://www.samsung.com/uk/consumer/tv-audio-video/televisions/).

When the TV is first connected, you will need to accept Home Assistant on the TV to allow communication.

To add a TV to your installation, add the following to your `configuration.yaml` file:

```yaml
# Example configuration.yaml entry
media_player:
  platform: samsungtv
  host: 192.168.0.10
  name: Living Room TV
```

Configuration variables:

- **host** (*Required*): The IP of the Samsung Smart TV, eg. 192.168.0.10
- **name** (*Optional*): The name you would like to give to the Samsung Smart TV.


Currently known supported models:

- C7700
- D7000
- D8000
- ES5500
- ES6800
- F6300
- F6500
- EH5600
- F6400AF
- LAC46C650
 
If your model is not on the list then give it a test, if everything works correctly then add it to the list on [GitHub](https://github.com/home-assistant/home-assistant.io).
The two letters at the beginning of the model number represent the region, UE is Europe, UN is North America and UA is Asia & Australia. The two numbers following that represent the screen size. If you add your model remember to remove these before adding them to the list.

There's currently a [known issue](https://github.com/home-assistant/home-assistant/issues/2098) with some TV's receiving a *Key press UP* that can interrupt certain applications. 

Currently tested but not working models:

- KU6300 - Shows in GUI but unable to control.
