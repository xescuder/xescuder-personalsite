---
templateKey: 'blog-post'
title: 'Jeedom - Control your TV'
date: 2017-01-04T15:04:10.000Z
featuredpost: false
description: >-
  Control your TV with Jeedom
tags:
  - domotics
---


Prerequisites:

- Buy a Broadlink remote control. I found it with a big discount at [https://www.efectoled.com/es/comprar-control-wifi/4467-mando-controlador-remoto-rm-pro.html](https://www.efectoled.com/es/comprar-control-wifi/4467-mando-controlador-remoto-rm-pro.html)

## Plugin installation

1. Go to menu **Plugins > Gestion des plugins** and press on **Market** icon
1. Search **Broadlink** and install it
	![Broadlink market](img/jeedom-broadlink-1.png)
1. Active it

## Add device

1. Go to **Plugins > Protocole domotique** and select **Broadlink**
1. Press **Mode inclusion**
1. After some seconds a screen will be shown with the found equipment where:
	- Select **Broadlink Universal Remote** in *Equipment* field
	- Select **Default** in *Modèle* field
	- Select the **Object parent**
	- Leave checked the fields **Activer** and **Visible**
	- Take not of IP 
1. Press **Sauvegarder**
1. Go to your router and configure this IP as static (DHCP Management). For example in my router is found at Configuration > LAN, DHCP estático (all in Expert Mode).


## Setup TV control
1. Go to tab **Commandes**
1. For each command (volume up, on, off, ...) we need to do the next actions:
	- Press **Apprendre une commande**
	- Use tv remote and press some button, for example volume up
	- Wait a moment and you'll see the command 
	![Broadlink command](img/jeedom-broadlink-2.png)
	- Sustitute the assigned command name (at column **Nom**) with a more easy name. Example: 1Commande26008c0095 to **Volume up**

1. Press **Sauvegarder**
