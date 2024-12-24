---
layout: post
title: JustAnotherWebsocketServer
description: Learning Rust Libraries & Websockets
---
JustAnotherWebsocketServer (JAWS) is a tool I developed during the process of building StreamCore for "UI customization". The exciting thing that it does is that custom source files are able to be served to provide a "full" website beyond the bootstrapping that's done by default. 

The customizations work using a json file which allows the person developing the customization to effectively add HTML tags that will be added to the bootstrap page. This means you're able to provide custom CSS, JavaScript, HTML, or even JSON to load Javascript Variables. 

There are probably better ways to have implemented this functionality, but I believe that this shows my skills at bodging in functionality into systems that aren't necessarily designed to do what I'm asking them to do. 

Technologies Used
=================

* JavaScript
* HTML
* CSS
* Docker
* Rust

Credits
=======

* Ben King

[Source](https://github.com/exlted/JustAnotherWebsocketServer/tree/main)