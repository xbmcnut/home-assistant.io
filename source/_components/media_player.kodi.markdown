---
layout: page
title: "Kodi"
description: "Instructions how to integrate Kodi into Home Assistant."
date: 2015-06-22 11:00
sidebar: true
comments: false
sharing: true
footer: true
logo: kodi.png
ha_category: Media Player
featured: true
ha_release: pre 0.7
---


The `kodi` platform allows you to control a [Kodi](http://kodi.tv/) multimedia system from Home Assistant.

To add Kodi to your installation, add the following to your `configuration.yaml` file:

```yaml
# Example configuration.yaml entry
media_player:
  platform: kodi
  host: http://192.168.0.123
  port: 8080
  name: Kodi
  username: USERNAME
  password: PASSWORD
  turn_off_action: shutdown
```

Configuration variables:

- **host** (*Required*): The host name or address of the device that is running XBMC/Kodi
- **port** (*Optional*): The port number. Defaults to 8080.
- **name** (*Optional*): The name of the device used in the frontend.
- **username** (*Optional*): The XBMC/Kodi HTTP username.
- **password** (*Optional*): The XBMC/Kodi HTTP password. You cannot leave the password field blank. Use 'None' if you do not use a password.
- **turn_off_action** (*Optional*): The desired turn off action. Options are `none`, `quit`, `hibernate`, `suspend`, `reboot`, or `shutdown`. Default `none`.
