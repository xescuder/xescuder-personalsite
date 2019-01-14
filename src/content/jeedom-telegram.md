---
layout: post
title: Jeedom - Telegram
author: xescuder
tags:
  - domotics
date: '2019-01-12T12:11:55.000Z'
---

This tutorial explains how to setup Telegram for Jeedom communication (for example if we want to receive a message when an intrusion is detected).

## Telegram bot creation

1. Go to your telegram app and search 'botfather'
1. Enter into botfather and enter /newbot
1. Create bot with a name (for example 'Jeedom') and your username
1. The bot will answer with a token that you need to copy


## Jeedom setup

1. Go to your jeedom web console and add plugin ‘Telegram’
1. Press ‘Ajouter’ and set the name of the equipment (‘Telegram’)
1. Copy the previous token in field 'Bot token'
1. Checkbox 'Active' and 'Visible'
1. From tab 'Commandes' press button 'Tester' on second line, and check that you've received a message on Telegram