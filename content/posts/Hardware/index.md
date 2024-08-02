+++
title = 'Hardware development process'
summary = "Hardware selection and design"
draft = false
weight = 3
+++

## Hardware selection
Materials used in this project:

| Seeed XIAO ESP32C3 | LEDs | Buzzer |
|:-:|:-:|:-:|
| {{< figure src="images/esp.png" width="400" class="center" >}} | {{< figure src="images/led.png" width="400" class="center" >}} | {{< figure src="images/buzzer.png" width="400" class="center" >}} |

|Switches | LED strips | Water pump |
|:-:|:-:|:-:|
| {{< figure src="images/switch.jpg" width="400" class="center" >}} | {{< figure src="images/led_strip.png" width="400" class="center" >}} | {{< figure src="images/water_pump.jpg" width="400" class="center" >}} |

> **Note:** These peripherals are used in our system for illustration, and they may be replaced by other device/appliance.

| Features | ESP32C3 | ESP 8266 | STM32 with Wi-Fi Module |
|:-:|:-:|:-:|:-:|
| **ESP-NOW Protocol Support** | Native support | No native support | Typically unsupported |
| **Power Efficiency** | High, supports deep sleep modes | Moderate, less efficient | Varies, generally less efficient |
| **Performance and Features** | High, RISC-V architecture | Moderate, Tensilica Xtensa | Varies, depends on configuration |
| **Development Ecosystem and Community Support** | Extensive, strong community | Good, less advanced | Strong for STM32, complex configuration |
| **Cost and Availability** | Cost-effective | Cheaper, fewer features | More expensive, complex integration |

For this project we have chosen to work with the ESP32C3. The ESP32C3 is better suited for wireless switch module due to its native support for the ESP-NOW protocol, improved power efficiency, better performance, and more robust development ecosystem compared to the ESP8266 and STM32 with a Wi-Fi module.

## Hardware design

|Transmitter| Receiver |
|:-:|:-:|
| {{< figure src="images/receiver.jpg" width="300" class="center" >}} | {{< figure src="images/transmitter.jpg" width="300" class="center" >}} |


The ESP-NOW protocol requires two ESP32C3 boards, one to act as a transmitter and another as a receiver. Each board was connected to their out-of-the-box antennae to increase SNR.

The transmitter is wired to accept input from 3 switches. Each button when pressed would toggle the associated pins on the receiver sides.

The receiver is wired to 3 LEDs and when data is received from the transmitter, it would toggle the associated pins either from (HIGH to LOW) or (LOW to HIGH). The 3 LEDS, are just to indicate switching.

In the indoor farm application, one of the receiver output pins is wired to a buzzer. All output pins were then wired to the signal side of a relay board.
