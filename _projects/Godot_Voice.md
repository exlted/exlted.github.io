---
layout: post
title: Godot Voice
description: Text Animation and Audio Generation in Godot
---
Godot Voice is an attempt I made at writing library code for Godot. It wraps Godot's Text Box for rendering, and provides animation and sound generation for letter-by-letter text boxes. This project has a particular focus on being able to characterize speaking styles for different characters, meaning you can define per-character 'beep intervals' so that some letters are spoken faster or slower than others. 

However, this project showed me frustrating limitations with Godot that turned me off of using the engine altogether. Specifically, C# for Godot does not support compiling for web, and cross-compatability between C# and GDScript leaves a lot wanting. Since the creators of Godot severely push GDScript, and I personally don't enjoy writing in GDScript, this was my last project that I chose to do in Godot.

Overall, I'm proud of the design I generated for this utility. I really like the ability to automate generation of something that would often need to be hand keyframed, or given up on entirely. I think it's likely that I'll port this code to work in another engine when I work on a game that could benefit from the provided behavior.

Technologies Used
=================

* Godot
* C#

Credits
=======

* Ben King

[Source](https://github.com/exlted/GodotVoice)