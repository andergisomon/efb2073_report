+++
title = 'Software development process'
summary = "Further discussion, technical challenges, and how we had overcome them"
draft = false
weight = 4
+++

## Flowchart
| Receiver | Transmitter |
|:-:|:-:|
| {{< figure src="images/Receiver.svg" width="400" class="center" >}} | {{< figure src="images/Transmitter.svg" width="400" class="center" >}} |

## Discussion


## Technical challenges faced
**1. No Arduino code requirement**
> Since Arduino itself is a framework that relies on ESP IDF, the technical requirement of a codebase that does not use the Arduino framework is a major obstacle. ESP IDF in comparison is a low-level framework with a level of documentation and support that is orders of magnitude lower than that of Arduino.

**2. Lack of convenient APIs**
> ESP IDF also has a steeper learning curve as it comprises of low-level APIs specific to Espressif SoCs. Many functionalities will need to be written from scratch, compared to Arduino that enjoys an ecosystem of diverse libraries that make it easy to develop for.

**3. Limited Community Support**
> Oftentimes we are the first to implement something in pure ESP IDF. The technical documentation provided by ESP IDF is sometimes scarce, outdated, or available only in Chinese. Example implementations are often irrelevant, uncommented and supplied with no README.

## Overcoming the challenges

We worked from afternoon to the early morning multiple times; reading through documentation and ESP IDF source code to debug our code. Since it seemed like an impossible requirement, we initially implemented our project using Arduino, and translated the code into pure ESP IDF once we figured out the base code.