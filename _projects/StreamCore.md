---
layout: post
title: StreamCore
description: Mircroservice Stream Chat Visualizer
---
StreamCore is the project I started to learn Rust and Microservice Architecture. It is still in progress, but due to me no longer using it as much as I used to, the project has been backburnered for the forseeable future. It is a tool to support multi-platform streaming. If you know what tools like StreamLabs do, StreamCore's goal is to replace that, while being open source, and being easily extensible to be able to support new platforms with minimal effort.

The biggest sign of success for StreamCore to me, was the fact that I was able to implement support for a brand new streaming platform's chat within a couple of days. And since that success, I have attempted to simplify the design of StreamCore to make that process even faster.

Additionally, my second point of pride is the combination of using Docker and a Microservice architecture, so that the end user only needs to run the specific services they need to support the platforms they're streaming to. 

My final point of pride on this project was learning how to use Github significantly more. This project uses Github Actions to build and deploy the docker images. And it uses github pages to host JSON schemas which have ended up going unused in the project so far.

However, I do think I've bit off more than I can chew with this project, and to get it to the point that I dreamed of it getting to it will either need a major rework in how it's designed, or I will need significantly more understanding of multi-service communication, as it's relatively unstable in its current state.

This project shows my strengths as a programmer though, as I understood almost none of the tools I was using going into writing StreamCore, and I feel I learned a lot and grew significantly as a programer because of the work I did on it.

Technologies Used
=================

* Rust
* Javascript
* Docker
* Github Actions

Credits
=======

* Ben King

[Source](https://github.com/exlted/StreamCore)