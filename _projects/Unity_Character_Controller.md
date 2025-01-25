---
layout: post
title: Unity Character Controller
description: Developing a Low/No Code Unity Character Controller
---
With the advent of the new Unity Control system, I wanted to finally move forward with developing this low-code control system that I've been dreaming of writing for years. The final thing that pushed me over the edge to being able to get it done was learning about ScriptableObjects as compared to MonoBehaviors and exactly what all you're able to do with them. 

The most exciting prospect out of this project, is the use of ScriptableObjects to provide Composable behaviors, rather than needing to use Inheritance structures. With my prior, limited, understanding of what tools were available when doing development in Unity, I had always shied away from writing "long term library code" that I would intend on being able to reuse in future games I write. Why would I reuse a character controller I'd written previously, if I need to rewrite a bunch of it anyway to do the things I need to do differently in this game? That's where compositional development comes in clutch!

The structure of this system is as follows:
* Wrappers - Holds configuration for a 'control.'
* Handler - Hooks into Unity Control System to transform a user's input into useful data. It'll store a specific action's name to register for its callbacks.
* Transformer - Takes the input from the Handler to turn it into the actual change you're wanting to see on screen. 
* Applicator - Takes the output from the Transformer and applies it to the MonoBehavior that is calling into this wrapper

Overall, there is definitely room to expand upon this idea, but for now these 4 sets of ScriptableObjects allow you to use the Unity Editor to configure the controls rather than needing to necessarily write code to do it. At the time of writing, the exact controls that are supported are limited enough that new Handlers, Transformers, Applicators, and potentially even Wrappers will be needed to handle a new game's specific control schema. But, my goal is to continue adding to the built-in options with every game I write. If there's ever a control setup I find that I can't handle with what I've already write, I'll write it and add it.

Eventually, I plan on writing some Unity UI to automatically convert a defined control schema into a full-on "one click" basic set of controls. Obviously this will want additional configuration after the initial setup, but it will significantly speed up the initial time-to-use of this library.


Technologies Used
=================

* Unity
* C#

Credits
=======

* Ben King (Everything Else)

[Source](https://github.com/exlted/Character_Controller)