---
templateKey: 'blog-post'
title: 'Jeedom - Alarm scenario'
date: 2017-01-04T15:04:10.000Z
featuredpost: false
description: >-
  How to configure Jeedom with an alarm
tags:
  - domotics
---

I started to build my domotic center with Jeedom. This tutorial is to show how you can set an alarm with the next equipments:

* [Raspberry](https://www.amazon.es/gp/product/B07BDR5PDW/ref=ppx_yo_dt_b_asin_title_o01__o00_s01?ie=UTF8&psc=1)
* [Razberry](https://www.amazon.es/gp/product/B00BL9QFH6/ref=ppx_yo_dt_b_asin_title_o01__o00_s00?ie=UTF8&psc=1)
* [Fibaro Presence Sensor](https://www.amazon.es/gp/product/B01CPR7VX4/ref=ppx_yo_dt_b_asin_title_o01__o00_s01?ie=UTF8&psc=1) 
* [Neocoolcam Siren](https://es.aliexpress.com/item/NEO-COOLCAM-Z-wave-Wireless-Siren-Alarm-Sensor-Compatible-with-Z-wave-Plus-Sensor-Alarm-Home/32810518687.html). 
* [Xiaomi Gateway](https://es.aliexpress.com/item/Nuevo-Xiaomi-Mijia-Gateway-2th-versi-n-Smart-Home-multifuncional-Home-Kit-para-Xiaomi-Mijia-puerta/32853412923.html)
* [Xiaomi Door Window Sensors](https://es.aliexpress.com/item/Original-Xiaomi-Door-Window-Sensor-Pocket-Size-xiaomi-Smart-Home-Kits-Alarm-System-work-with-Gateway/32829391822.html)

We're going to use the plugin **Alarm**, very easy to setup. 

## Prerequisites

First configure Telegram using tutorial [Jeedom-Telegram](/jeedom-telegram)

## Plugin installation

1. First of all download **Siren** plugin from Jeedom. Gestion des plugins ![Plugins management](img/jeedom_plugins_management.png)
2. Activate it

## Setup Alarm

1. Go to plugins menu (fourth option from left) and select **Sécurité>Alarme**
2. Press **Ajouter** and choose the name for the alarm
3. Check options:
   * Activer
   * Visible
   * Armement visible (to enable or disable alarm from dashboard)
   * Status immédiat visible
4. Define a 'Mode' (at tab 'Modes') that will allow us to activate alarm or deactivate from dashboard when we leave from home
   * Press **Ajouter mode**
   * Create a name, for example 'TOTAL'

## Zone creation

1. From menu **Zones** define the zones that the alarm has to look out. I'm going to define a single zone 'TOTAL' for everything, but you can define any zones you need (perimeter, inside, ...):
   * Press **Ajouter zone**
   * Edit a name zone ('TOTAL', for example)
   * Click **Déclencheur** and select the equipment and the commande that defines trigger for presence or sensor
   For example if you've a Fibaro Sensor like me:
   ![Create fibaro link in zone](/img/jeedom_alarm_1.png)
   After creation we can define how much time we've to leave home before the condition is checked at 'Activation' field (in minutes) and in 'Declencher' what is the time the actions will be executed after condition is true (if for example a presence is detected and we set 1 minutes for Declencher the actions will be executed after 1 minute)
   You can set **Activation** to 3 minutes.
   Add as many equipments you need in Declencher (I've added after Fibaro Sensor other window sensors)
   * Press **Action immediate** to create for example a Telegram message when previous conditions are true
     ```
     	* Press second button and select equipment 'Telegram'
     	* In 'Message field' enter a message like 'Intruder in living home'
     ```
   * Press **Action** to define an action that will be launched after 'Activate' time. This is useful when we enter at home, so we need a time to disconnect alarm. For example, if I want to beep the siren: 
   * Select the mode we've created ('TOTAL')
   * On the second button select the commande to activate the alarm.
   ![Set siren on](/img/jeedom_alarm_action_immediate.png)
2. Return to **Mode** and add with button '+Zone' the new created zone ('TOTAL')

## Configure messages to receive when alarm is activated and deactivated

Finally we need to set if we need to receive some notification when we activate the alarm and when we deactivate. We're going to use Telegram:

1. Select **Activation OK** tab. Here we're going to set what to do when we activate the alarm
   * I want for example to receive a telegram message immediately when I activate the alarm, so I press "Ajouter action immediate lors de l'activation" and select 'Telegram' equipment and the message I want to receive to my bot
   * Also I want to receive a telegram message after the real activation (we've defined it in field 'Activation' at zone), so I press 'Ajouter action lors de l'activation'
   ![Alarm activated](/img/jeedom_alarm_activated.png)
2. Select **Deactivation OK** and define a telegram message when we deactivate the alarm

## Activate the alarm

1. Go to dashboard (we see the alarm plugin and the padlock open)
   ![Alarm on](/img/jeedom_alarm_off.png)
2. Press padlock to activate alarm (the padlock then is shown closed)

![Alarm off](/img/jeedom_alarm_on.png)

Remember you need to leave before the 'Activate' time field...
