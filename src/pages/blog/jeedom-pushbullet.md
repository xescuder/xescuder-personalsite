---
templateKey: 'blog-post'
title: 'Jeedom - Alerts by Pushbullet'
date: 2017-01-04T15:04:10.000Z
featuredpost: false
description: >-
  Alerts by Pushbullet
tags:
  - domotics
---

This tutorial explains how to setup Pushbullet for Jeedom communication (for example if we want to receive a message when an intrusion is detected).

## Create account in Pushbullet

1. Go to [https://www.pushbullet.com/](https://www.pushbullet.com/) and create a new account
1. Setup your devices to be notified, like your phone or your computer.
1. Go to **Settings > Account** and go to **Access tokens**
1. Click **Create Access Token** button
1. Copy the content of created token

## Install plugin

First install Pushbullet plugin from **Plugins** menu.

## Add equipment

From plugin click **Ajouter**

1. Press ‘Ajouter’ and set the name of the equipment (‘Pushbullet Xavier’)
1. Paste the previous token in field **Token pushbullet**
1. Select a name for Jeedom be visible at Pushbullet account
1. Press **Sauveguarder**