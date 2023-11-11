---
layout: post
read_time: true
show_date: true
title:  Making Progress!
date:   2023-11-11
description: This week we show you our minimum viable product, with a fully working editor and a simple algorithm for generating floor plans.
img: posts/20231111/floor-plan-2-banner.png
tags: [antarchitect, update, editor]
author: Jonatan Stenlund
github:
mathjax: no
---
Hello, and welcome to another update! This time, we'd like to show you a fully functional minimum viable product, with a working editor and a simple algorithm for generating floor plans. In the AntArchitect web application, we start by logging in, which redirects us to the dashboard.

![Dashboard](/assets/img/posts/20231111/dashboard.png)

From here we can choose to create a new floor plan, which takes us to the editor. In the editor we plan to support two types of algorithms, one of them which were showcased in our previous update. As shown in the image below, we have a simple form where we can enter the parameters for the algorithm (constraints for width, height, area and neighbors), and then press the Generate button to send the data to our API.

![Generate Floor Plan](/assets/img/posts/20231111/generator.png)

After the algorithm in the backend has done it's work, a new floor plan is returned and visualized in the editor. Initially, we only displayed the rooms as colored rectangles, but then we added labels as well to make it easier to distinguish between them.

![Initial Floor Plan](/assets/img/posts/20231111/floor-plan.png)

To make it even more clear, we then added labels for displaying width and height for the different rooms, as shown in the image below. This gives the resulting visualisation a more practical use, as it can be used to implement real world floor plans.

![Floor Plan With Labels](/assets/img/posts/20231111/floor-plan-2.png)

We are very happy with the progress we have made so far, and are looking forward to the next sprint where we will be adding more features to the editor. These features include implementing the second algorithm, adding support for moving and resizing rooms, adding support for saving and loading floor plans, and increasing the speed of the evolutionary algorithm.

Thank you for reading, and stay tuned for more updates!

Best regards,

*The AntArchitect Team*
