---
layout: post
title: Unreal RTS Toolkit
description: Developing Reusable Unreal Code
---
My aptly named Unreal RTS Toolkit is actually my first major project done in Unreal and as such I have been using this as a way to learn the engine while streching my game development chops. 

I am working towards making a Wintermaul style tower defense game, but in my wish to learn Unreal more than I wanted to rush through getting this game developed, I decided to develop a somewhat generic set of RTS plugins which I would make open source for anyone to use.
![Screenshot of the plugin explorer in the Unreal Editor](https://exlted.github.io/assets/images/RTSToolkit_Plugins.PNG)

From what I've seen in researching other open source projects in Unreal, my significant use of Interfaces seems to be uncommon. One of the primary tools I like to use in making my code reusable is dependency injection. I'm sure that there are places that I've not allowed for it where I could have, but it is the main reason I've created so much infrastructure around using Interfaces in this codebase.

A hack/workaround I found was methods to handle Delegates being declared in an Interface. One [bad example](https://github.com/exlted/unreal-rts-toolkit/blob/master/Plugins/RTSUnitSystem/Source/RTSUnitSystem/Public/Interfaces/Targetable.h) includes #defines and templated functions in the Interface. This code allows for a largely transparent usage of the underlying Delegate by the end user, though it is limited by not being usable by Blueprints. So, the [next method](https://github.com/exlted/unreal-rts-toolkit/blob/master/Plugins/RTSToolkitInterfaces/Source/RTSToolkitInterfaces/Public/Interfaces/StatUpdater.h) I found does support use in Blueprints. By declaring a non-multicast delegate which matches your multicast delegate, you're able to accept the non-multicast version as a parameter which can then be registered directly into the multicast delegate. 

![Screenshot of the structure of my example game's Cursor](https://exlted.github.io/assets/images/RTSToolkit_Cursor.PNG)
![Screenshot of my example game's Cursor having a Ghost Cube attached to it](https://exlted.github.io/assets/images/RTSToolkit_CursorInGame.PNG)

Probably the plugin I'm most proud of in this project is the [Simple Attachment System](https://github.com/exlted/unreal-rts-toolkit/tree/master/Plugins/SimpleAttachmentSystem/Source/SimpleAttachmentSystem) which provides a system where by placing only two Actor Components on an Actor, you're able to have a named slot where you can easily attach any item to. While I'm currently only using this to attach a Ghost Actor to the player's cursor to show where they're going to build a building, this could be used in any game with visible equipment 

![Screenshot of my example game's Layout in Unreal's Widget Editor](https://exlted.github.io/assets/images/RTSToolkit_Layout.PNG)

Another interesting thing I've developed would be my UI Layout system. I have a widget which only has Named Slots in it which through an Interface I've developed are accessible by any other Blueprint that knows about it. It's not the most useful thing, but it was an answer for my question of "how do I place all of these disparate widgets I'm developing onto one screen while allowing multiple widgets to share the same space?"

![Screenshot of the Stat Settings page in the Unreal Project Settings Editor](https://exlted.github.io/assets/images/RTSToolkit_StatSettings.PNG)

The final thing I want to point out would have to be my [RTS Economy System](https://github.com/exlted/unreal-rts-toolkit/tree/master/Plugins/RTSEconomySystem/Source/RTSEconomySystem) which provides a Project Settings menu to allow the end user of this plugin to define as many types of resources as they want in their game. The defined items show up as a dropdown wherever anything references a Resource in any of my plugin code. There is a similar behavior in the over-broad [RTS Toolkit Interfaces](https://github.com/exlted/unreal-rts-toolkit/tree/master/Plugins/RTSToolkitInterfaces/Source/RTSToolkitInterfaces/Public) which handles Stats, but also provides a position to define what those stat names mean for any of my related plugins. So, you could use this to rename Health to Stamina or Vitality if you so wanted.

Do I think any of this is revolutionary, no, but I do think that you can see how much I've learned in just a couple of months of focused development. I'm looking forward to completing my first project and applying this knowledge to make future projects go even better! Thank you for your time in reading this!

Technologies Used
=================

* C++
* Unreal Engine
* Blueprints

Credits
=======

* Ben King (Development)

[Source](https://github.com/exlted/unreal-rts-toolkit)
