---
layout: post
read_time: true
show_date: true
title:  Editor Update
date:   2023-11-02
description: This week we give you an update regarding our editor, and the first algorithm we have implemented.
img: posts/20231102/editor-banner.png
tags: [antarchitect, update, editor]
author: Jonatan Stenlund
github:
mathjax: no
---
Hello, and welcome to this long awaited status update! We have been quiet the last couple of weeks because of midterms, but rest assured that things are happening behind the scenes. This week we would like to give you an update regarding our editor, and the first algorithm we have implemented in our backend.

## A Greedy Evolutionary Algorithm

The algorithm we have chosen to implement initially is a hybrid greedy and evolutionary algorithm. What we mean by this is that there is a first part that chooses an initial sequence of rooms in a greedy way, and then a second part that works in an evolutionary fashion to find the optimal sequence by repeating the greedy step. This is illustrated in the figure below (see [this link](https://www.researchgate.net/publication/331718182_Hybrid_Evolutionary_Algorithm_applied_to_Automated_Floor_Plan_Generation) for reference).

![Greedy evolutionary algorithm](/assets/img/posts/20231102/algorithm-1.png)

For this algorithm to work, we need to feed some input parameters to the it in the form of a JSON object. The object contains a list of rooms, where each room has an id, label, min width, max width, min height, max height, min area, max area and a list of neighbors. In our editor, these parameters can be entered which allows the Generate button to be pressed, which sends the parameters to our API. In our backend, the algorithm does its thing, and a new JSON object is returned once it's done. This object contains a list of the same rooms from earlier, but instead of min/max constraints each room has a set height, width and bottom left corner coordinate. The data can be visualized in our editor, as shown below.

![Editor](/assets/img/posts/20231102/editor.png)

As one can see, this is from an early iteration, where there were some issues with room overlapping. This is an issue that has been fixed in later iterations.

Thanks for following our journey, and stay tuned for more updates!

Best regards,

*The AntArchitect Team*

