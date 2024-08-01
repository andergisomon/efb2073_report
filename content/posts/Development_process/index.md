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
**1. Development Environment**
> The biggest difficulty that we encountered while developing the module was utilizing ESP-IDF. The process includes setting it up which requires manual installation of dependencies such as Git. The framework is also strict in choosing specific versions as its components, which may induce build errors and compatibility issues caused by version conflicts.

**2. Framework Maturity**
> Despite being powerful and full of features to be explored, the ESP-IDF is more niche compared to the popular and widely used Arduino framework. ESP-IDF also has a steeper learning curve as it is highly complex and has a lower level of APIs. Having a deep understanding of its hardware and software architecture became a huge obstacle to configure the module.

**3. Limited Community Support**
> The ESP-IDF community is smaller when compared to the Arduino community. There are less examples, tutorials, and forums available to allow studying and troubleshooting specific problems encountered.  The repository of examples and libraries for ESP-IDF was also too little to be used as a learning tool on utilizing the framework. This made searching for relevant code or reference implementations difficult.

## Overcoming the challenges