---
layout: post
title: Game of Life
description: Conways Game of Life... But Mine!
---
During my first collegiate project, the goal was to implement Conway's Game of Life, as well as add a few 'additional features' that weren't called for in the original design spec. Primarily, the features I decided to add were 'quality of life' features around the save/load system as well as in setting initial state of the cells. 

One of the required features was to be able to make the board size (in terms of cells) resizable. However, keeping state if you made the board bigger wasn't required. So, one of the most important features I added was that the cell state would remain across resizes, assuming that living cells wouldn't need to be cut off to handle the resize. Additionally, the program is able to pause the simulation and resize the board while the simulation is actively running.

This is largely the same as any other game of life written by a novice programmer. But, what it shows about me in particular is that when I'm doing design work, my goal is always to try and understand why something is being done the way it's being done, so that whatever I add through my designs is a feature that builds upon the same goals as the rest of the features, making a 'more complete' product. 

Technologies Used
=================

* C#

Credits
=======

* Full Sail University (Initial Template project)
* Ben King

[Source](https://github.com/exlted/PP1-Game-of-Life/tree/master/WindowsFormsApplication1/WindowsFormsApplication1)