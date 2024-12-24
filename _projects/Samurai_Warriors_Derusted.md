---
layout: post
title: Samurai Warriors Derusted
description: Remake of an Old Project to learn Bevy
---
Over the past year or so, I've been trying to find a game engine/toolkit that I want to learn more to start working on games again. At some point during that time, I got really interested in Bevy, especially since I was using Rust for StreamCore and wanted to use the language more. In trying to learn Bevy, though, I went down a few paths that probably made things more difficult for me, and ended up causing me to take a break and look at other options I had available to myself.

However, there are 2 things that I am proud of from the development of this rewrite of Samurai Warriors.
1. I significantly upgraded the random dungeon generation.
2. I wrote a system for generically loading assets without ever referencing any filenames.

The original random dungeon generation in Samurai Warriors was simple. We would generate X rooms that did NOT overlap in any way, then generate corridors from room 1 to room X, ensuring that every room that got generated would be reachable by the player. However, one of the things I always had dreamed of when writing the original Samurai Warriors, was to support rooms overlapping. The room generation process for Derusted allows for overlapping rooms, which makes for significantly more interesting dungeon layouts.

The asset loading, while I'm proud of it in theory, is probably the thing that I should've just done normally. It uses built in Bevy functionality to mark a Folder as something that needs assets loaded from, then it searches for an index.json file, which then gives pairs of json & asset files. It then loads in each one of those pairs into a Map which allows you to look up files based on the JSON definition. A good example of this is in [tile_data.rs](https://github.com/exlted/Samurai_Warriors_Derusted/blob/main/samurai_warriors_derusted/src/tile_data.rs) where we have an enum that provides all the different bits of data used to write these textures to the map. Because of Rust Enums, you're able to provide additional data inside of the enum, which makes this particular way of accessing tile data work really slick in the code once it's up and running. However, it took me multiple days, and a significant amount of work to get it to a working state at all. 

Overall, I'm happy with what got done in this project, but I'm not happy with the project overall as I never got around to finishing it. I learned a lot about Rust and Bevy while writing this code, and I think some day I may choose to go back and try to finish it off, but for now it's going to stay incomplete.

Technologies Used
=================

* Rust
* Bevy

Credits
=======

* Ben King

[Source](https://github.com/exlted/Samurai_Warriors_Derusted)