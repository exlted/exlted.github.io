---
layout: post
title: Simple Menu System
description: Minimalist Unity UI Toolkit Menu System
---

![Gif of the SimpleMenuSystem's Example in Use](https://exlted.github.io/assets/images/SMS_MenuInUse.gif)

One of the 'rules of thumb' I always just assumed about Unity was that to have a decent menu, you needed a menu system to provide controller/keyboard support. Since I'm just working on some small projects, I didn't want to reinvent the wheel, so I did what anyone using Unity does and looked for assets that I could pull in to do it for me. 

I found many, most worked in ways that didn't jive with how I like to code, or looked good but cost money. I tried a few, and found them lacking, usually lacking mouse support, actually. 

A couple of days into my search, I resigned myself to writing a new one that would work how I wanted and support all input methods I cared about. As I start working on it, I notice that Unity by itself is doing a lot more than I expected. I place focus into a button, and use WASD and the focus moves around the buttons exactly how I expect it to. Even in unusual button layouts! 

Once I notice that, I might as well write the system I want right then and there if all the parts I was dreading would be taken care of already!

Enter the SimpleMenuSystem (great name, I know). A minimalist Menu tool that relies on Unity as much as it can, only extending the base functionality when I found it to be lacking. Oh yeah, and I decided to use UI Toolkit, because building something new on the 'old' tech felt bad.

- 1 MonoBehavior
- 2 SerializedFields
- 1 Serializable struct
- 2 public functions

For simple menuing, which to me means being able to navigate groups of button or button-like objects which can have actions associated with interacting with said buttons, that is all I needed.

![Picture of the Button Definitions in the Example Scene provided with SimpleMenuSystem](https://exlted.github.io/assets/images/SMS_ExampleButtonDefinition.PNG)

By setting up a struct to associate a Name with a UnityEvent, we are able to easily dynamically add Callbacks to any item defined in a UI Toolkit menu at runtime with no additional code!

We also use a Stack to keep track of the page we're on in the Menu so that you can have multiple paths to the same menu page without needing to have multiple copies of the same one.

This code also uses the UI Toolkit classnames to great effect. It Allows us to mark which item in a menu should get focus initially, as well as limiting the number of VisualElements we are querying through when displaying a new menu page. 

This project is in progress, and as my other games require more features, more will be added to the SimpleMenuSystem. I know I'll be implementing a good way to handle Settings menus at some point, so look forward to that! 

Technologies Used
=================

* Unity
* UI Toolkit
* C#

Credits
=======

* Ben King

[Source](https://github.com/exlted/SimpleMenuSystem)