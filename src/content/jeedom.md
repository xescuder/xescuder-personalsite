---
layout: post
title: Jeedom - Alarm scenario
author: xescuder
tags:
  - domotics
date: '2012-08-20T15:11:55.000Z'
---
I've a Raspberry used for domotics (with a Razberry). One of my needs what's how to set an alarm using a Fibaro Presence Sensor and a Neocoolcam Siren. I'm going to explain how to do it!

## Plugin installation

1. First of all download 'Siren' plugin from Jeedom. Gestion des plugins ![](/img/jeedom_plugins_management.png)
2. Activate it

## Setup Alarm

1. Go to plugins menu (fourth option from left) and select 'Sécurité>Alarme'
1. Press 'Ajouter' and choose the name for the alarm
1. Check options:

	- Activer
	- Visible
	- Armement visible (to enable or disable alarm from dashboard)
	- Status immédiat visible

1. Define a 'Mode' (at tab 'Modes') that will allow us to activate alarm or deactivate from dashboard when we leave from home

	- Press 'Ajouter mode'
	- Create a name, for example 'Exit home'

1. From menu 'Zones' define the zones that the alarm has to look out. For each zone:
	
	- Press 'Ajouter zone'
	- Edit a name zone ('Living room zone', for example)
	- Click 'Déclencheur' and select the equipment and the commande that defines trigger for presence or sensor

	For example if you've a Fibaro Sensor like me:

	![Create fibaro link in zone](/img/jeedom_alarm_1.png)

	- Press 'Action immediate' to define an action that has to be launched if previous condition is true. For example, if I want to beep the siren: 

		* Select the mode we've created ('Exit home')
		* On the second button select the commande to activate the alarm.
		For example, for a Neocoolcam siren:
		![Set siren on](/img/jeedom_alarm_2.png)

		* Press second button and select equipment 'Telegram'
		* In message I set 'Alarm activated in 5 minutes'

	- Press tab 'Activation OK'
		* By default volume is shown, where we can set for example 15

