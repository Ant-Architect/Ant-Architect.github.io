---
layout: post
read_time: true
show_date: true
title:  EVO vs. MIQP vs. ChatGPT
date:   2023-11-24
description: Today we'd like to compare the two AI solutions we have implemented for floor plan generation, and also discuss the possibility of integrating ChatGPT with AntArchitect.
img: posts/20231124/miqp_1_25x25.png
tags: [ai, miqp, chatgpt, antarchitect, update, editor]
author: Jonatan Stenlund
github:
mathjax: no
---
Hi, and welcome to yet another blog post! Today we’d like to talk a bit about the AI solutions and algorithms we are working with to generate floor plans. Our goal is to make AntArchitect able to provide multiple solutions for floor plan generation, and have already implemented two completely different ones, which we’d like to discuss and compare. We would also like to discuss already existing AI solutions that could benefit AntArchitect, such as the popular ChatGPT.

## The Evolutionary Algorithm

In a previous post we presented the hybrid evolutionary and greedy algorithm, which takes a list of rooms as an input and arranges them according to size and neighbor constraints as an output. Since this approach tries multiple solutions and greedily chooses the best one in an iterative manner, it results in the algorithm being quite slow. A floor plan with five rooms, such as the one below, can take around half a minute to produce, and it gets slower the more rooms are added. Apart from the computation time, the algorithm produces nice results that respect size and neighbor constraints while also attempting to stay in a rectangular shape.

![EVO](/assets/img/posts/20231124/evo.png)

## MIQP

This is the other solution we have implemented, and our implementation is based on [this paper](https://lbfan.oss-cn-hangzhou.aliyuncs.com/personal_webpage/publications/2018-eg-iplayout.lres.pdf). MIQP stands for Mixed-Integer Quadratic Programming. It is a type of optimization problem that combines elements of both linear programming and quadratic programming with the additional constraint that some of the variables must take on integer values. Solving MIQP problems can be computationally challenging due to the discrete nature of the integer variables, and various optimization algorithms and solvers are employed to find optimal solutions. One such solver is offered by Gurobi, which is the one we have been using.

The main difference between the MIQP and EVO approaches in regards to the floor plan generation is that MIQP specifies a bounding box that should be filled by the rooms while EVO arranges the rooms without considering this constraint. This means that a correct implementation of MIQP should lead to all floor plans being completely filled rectangles, as long as the maximum individual room sizes aren’t too small. As shown in the images below, we haven’t managed to make this work perfectly yet, but we’re getting there. The first image shows a case where the bounding box is much larger than the individual room sizes, while the second and third images have bounding boxes that are closer to the total area of all individual rooms.

![MIQP 1](/assets/img/posts/20231124/miqp_1_25x25.png)

![MIQP 2](/assets/img/posts/20231124/miqp_2_10x5.png)

![MIQP 3](/assets/img/posts/20231124/miqp_3_20x10.png)

A major benefit of using the MIQP-based approach is that it’s much faster than the evolutionary and greedy hybrid, since it computes the optimal solution to a mathematical problem instead of iterating over a number of solutions. This is something that matters a lot to our users who shouldn’t have to wait long for a result to be displayed after pressing the button.

## ChatGPT

ChatGPT is a tool that can handle natural language interaction and generate well written and often accurate responses based on the user input, and it is one of the most powerful AI tools out there. It can of course also handle floor plan generation by, for example, the user specifying how many rooms they want and what their sizes should be, which results in a proposed solution from ChatGPT. GPT-4 even offers generated images with furniture and measurements included. This is very interesting to us, and we are thus looking for ways to integrate a sort of ChatGPT API with our application, so that users can utilize the power of ChatGPT’s generative abilities while having the results displayed and saved in AntArchitect. If we can make this API accept our input parameters, while returning output parameters in a fixed format, then we will have achieved this goal.

We will post any updates regarding this matter to this blog, so stay tuned for future updates.

Best regards,

*The AntArchitect Team*

