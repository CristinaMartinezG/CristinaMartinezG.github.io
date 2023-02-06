---
layout: project
type: project
image: img/micromouse/micromouse-square.jpg
title: "Micromouse"
date: 2015
published: True
labels:
  - Robotics
  - Arduino
  - C++
summary: "My team developed the so called Qing Qube which is meant to be used as a quick and easy way of setting up an automated assembly line."
---

<div class="text-center p-4">
  <img width="200px" src="../img/micromouse/micromouse-robot.png" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-robot-2.jpg" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-circuit.png" class="img-thumbnail" >
</div>

This project was given and sponsored by QING group.
The Qube project involves improving a robotic arm used to simulate an automation line. There is already a Qube, and the goal is to build another with a similar shape but slightly different specifications. The reasoning behind this is that they may be able to be linked together in the future. The new Qube must have better-organized cables and be able to recognize and grab various shapes and colors. 

For the new Qube, we follow the original drawings and make some changes based on the client's new specifications. This include, among other things, using a larger electric box, modifying the legs, and providing more room for movement. Furthermore, a new mechanical gripper capable of grabbing the specified items was developed. 

The finished product will be a robotic arm that can rearrange a board with various colors of shape cylinders and donuts according to a given color pattern. The whole hole process must be automated. 

Here is some code that illustrates how we read values from the line sensors:

```cpp
byte ADCRead(byte ch)
{
    word value;
    ADC1SC1 = ch;
    while (ADC1SC1_COCO != 1)
    {   // wait until ADC conversion is completed   
    }
    return ADC1RL;  // lower 8-bit value out of 10-bit data from the ADC
}
```

You can learn more at the [UH Micromouse News Announcement](https://manoa.hawaii.edu/news/article.php?aId=2857).
