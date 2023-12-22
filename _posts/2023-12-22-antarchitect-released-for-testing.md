---
layout: post
read_time: true
show_date: true
title:  AntArchitect Released For Testing
date:   2023-12-22
description: Welcome to the final post for AntArchitect. Thank you for being a part of our journey.
img: posts/20231222/antarchitect-larger.png
tags: [antarchitect, update, release]
author: Jonatan Stenlund
github:
mathjax: no
---
Hello, and welcome to what will probably be the final post regarding the AntArchitect. The course, during which our task was to create AntArchitect, is nearing its end, and we had our final presentation and demonstration a couple of days ago. We thank you for joining us on this journey, and hope that it has been exciting and interesting.

## The Final Product

We’d like to discuss the features of AntArchitect, and also what could be some possible future improvements, in the case that work on the product should continue after the course is finished. As you know by now, AntArchitect is a tool for generating floor plans with the help of artificial intelligence and complex algorithms. The purpose is to give regular people, as well as architects, a way to simply create floor plans without having to specify exact constraints and measurements. AntArchitect aims to give inspiration to users by creating optimal solutions based on loose constraints as input.

The core functionality of AntArchitect lies in two different algorithms for floor plan generation. One of them we have chosen to call EVO, while the other we have chosen to call MIQP. EVO is a greedy evolutionary algorithm that takes a list of neighbors and measurement constraints as an input, and arranges the rooms in an optimal way. MIQP instead takes a bounding box and a list of rooms, and attempts to place these rooms in a way so that the bounding box is filled out. MIQP can also handle more advanced constraints such as desired room placement in the bounding box. For a more technical description of the algorithms, please check out our previous blog posts about them.

The frontend application is built in Next.js, and allows users to create an account to which they can save generated floor plans. We wanted the product to be intuitive and simple to use, so we have made the interface simple with clear buttons, sliders, help text and error messages. There is also a Documentation page for detailed instructions on how to use the tool. The image below shows how it can look when generating a floor plan using MIQP. Notice that MIQP has built-in presets which can be used to get started on a floor plan.

![Editor MIQP](/assets/img/posts/20231222/editor-miqp.png)

## Future Improvements

While we are really happy with how AntArchitect turned out, there are some things that we didn’t have time to implement that might be fun and interesting. First of all, we didn’t fully utilize the capabilities of Three.js to create an editor where rooms can be moved around and edited after the generation phase. This can be quite complex since it requires collision detection to avoid overlap, and it’s a bit out of scope for our purpose, but it could be a fun feature. We also didn’t connect our frontend with any generative AI solutions like we discussed in the last post, but this is also quite out of scope for us, and tools like ChatGPT already provide ways to display results as images. Finally, we didn’t make use of all features provided by the MIQP solver, such as supporting non-rectangular floor plans. The solver provided by Gurobi supports quite advanced constraints, and we only utilized a few of them. This could be interesting to expand upon in the future.

With that said, feel free to try AntArchitect for yourself in its current state, but note that work on the product has finished for now, and no further changes and improvements will be made: [https://ant-architect.azurewebsites.net/](https://ant-architect.azurewebsites.net/)

Thank you for having been a part of our project, and perhaps we’ll meet again in the future. We’d also like to take the opportunity to wish you a Merry Christmas! 

Until we meet again,

*The AntArchitect Team*


