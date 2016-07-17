---
layout: page
title: "Flux Led/MagicLight"
description: "Instructions how to setup Flux led/MagicLight within Home Assistant."
date: 2015-07-17 20:09
sidebar: true
comments: false
sharing: true
footer: true
ha_category: Light
ha_iot_class: "Local Polling"
featured: true
ha_release: 0.25
---

Flux Led support is integrated into Home Assistant as a light platform. Several brands use the same protoco and they have the HF-LPB100 chipset in common.
Example of bulbs:
-
- []()
- []()
- []()

Configuration

```yaml
# Example configuration.yaml entry
light:
  platform: hue
  host: DEVICE_IP_ADDRESS
  allow_unreachable: true
  filename: my_hue_hub_token.conf
```

Configuration variables:

- **host** (*Required*): IP address of the device, eg. 192.168.1.10.
- **allow_unreachable** (*Optional*):  This will allow unreachable bulbs to report their state correctly. By default *name* from the device is used.
- **filename** (*Optional*): Make this unique if specifying multiple Hue hubs.

