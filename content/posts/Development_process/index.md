+++
title = 'Software development process'
summary = "Further discussion, technical challenges, and how we had overcome them"
draft = false
weight = 4
+++

## Flowchart
| Receiver | Transmitter |
|:-:|:-:|
| {{< figure src="images/Receiver.svg" width="600" class="center" >}} | {{< figure src="images/Transmitter.svg" width="600" class="center" >}} |

## Discussion

## Technical challenges faced
### 1. No Arduino code requirement
{style="color: red"}

> Arduino for ESP32 itself is a framework that [wraps around](https://github.com/espressif/arduino-esp32 "Title") ESP IDF. The technical requirement of an Arduino-free codebase is a major hurdle. ESP IDF in comparison is a low-level framework that interfaces more directly to Espressif hardware.

### 2. Lack of convenient APIs
> ESP IDF also has a steeper learning curve as it comprises of low-level APIs specific to Espressif SoCs. Many functionalities do not have convenient high-level abstractions, compared to Arduino that enjoys an ecosystem of diverse libraries that are easy to use.

### 3. Limited Community Support
> Oftentimes we were the first to implement something in **pure ESP IDF**. The technical documentation provided by ESP IDF is sometimes scarce, outdated, or available only in Chinese. Example implementations are often irrelevant, uncommented and supplied with no README.

## Overcoming the challenges
We worked from afternoon to the early morning multiple times; reading through documentation and ESP IDF source code to debug our code.

Since it seemed like an impossible requirement, we initially implemented our project using Arduino, and translated the code into pure ESP IDF once we figured out the base code.

## Web development
Using the [Hugo](https://gohugo.io "Title") framework, we used JavaScript, HTML, and CSS to develop this web report. For collaborative coding, we used [Git](https://git-scm.com "Title"), the industry standard for version control.

Additionally, we opted to use GitHub Pages to host this report for free without ads or background trackers which are permanently enabled for those who use [Wix](https://support.wix.com/en/article/wix-editor-wix-ads-on-mobile-site "Title"), Google Sites, [Weebly](https://www.sellercommunity.com/t5/Weebly-Getting-Started/Weebly-Ads/td-p/476754 "Title"), or other free web building sites.

The report reader can rest assured that no personal data is secretly used, as this website is a static site built by the team from the ground up. In fact, we used a software development philosophy called "build in public" (BIP), where anyone can independently [audit our website](https://github.com/andergisomon/efb2073_report "Title"). 