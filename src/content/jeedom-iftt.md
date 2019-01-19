---
layout: post
title: Jeedom - Control plugs with IFTT (if this then that)
author: xescuder
tags:
  - domotics
date: '2019-01-18T15:11:55.000Z'
---

You want to control from Jeedom some WIFI devices, as plug, you can use IFTT.

Used devices:

- [TECKIN WIFI Plug](https://www.amazon.es/gp/product/B07D5V139R/ref=ppx_yo_dt_b_asin_title_o00__o00_s00?ie=UTF8&psc=1)

## Setup device using Smart Life app

1. Install **Smart Life** in App Mobile
1. Search and add devices from **Smart Life**

## Setup IFTT account and create service

1. Go to [https://ifttt.com](https://ifttt.com) and create an account
1. Go to [webhooks url](https://ifttt.com/services/maker_webhooks/)
1. Press **Settings**, and copy last content after /use/ URL

## Setup Jeedom IFTT plugin

1. Des de **Gestion des plugins** cercar el plugin **IFTT** i instal·lar-lo
1. Go to plugin **IFTT** and press **Ajouter**
1. Create an equipment and set **Clef** value to the copied code from IFTT webhooks settings
1. Check **Activate** and press **Sauveguarder**


## Create communication with your plug in IFTT

1. Go to IFTT web and press **My Applets** and **New Applet**
1. Push + button in if **+** this then that
1. Choose service **Smart Life**
1. At **Search services** field look and select **Webhooks**
1. Select **Receive a web request**
1. Use a name to remember from jeedom (like 'Open plug living room')
1. Press **Create trigger**
1. Now we can define the that portion clicking on '+' before 'that' label
1. Now select service **Smartlife**
1. Select action to use, for example *Turn on*
![jeedom_iftt_smartlife_on](/img/jeedom_iftt_smartlife_on.png)
1. Now we'll see all devices we've detected and configured in **Smartlife** mobile app
1. Select the device
1. Disable **Receive notifications when this Applet runs** if you don't want to be annoyed each time action is performed
1. Press **Finish**