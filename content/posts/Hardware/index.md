+++
title = 'Hardware Development Process'
summary = "Hardware selection, Harware design"
draft = false
weight = 3
+++

## Hardware selection
> Materials used in this project:
|ESP32C3 | LEDs | Buzzer |
|:-:|:-:|:-:|
| {{< figure src="images/esp.png" width="400" class="center" >}} | {{< figure src="images/led.png" width="400" class="center" >}} | {{< figure src="images/buzzer.png" width="400" class="center" >}} |

> Note: LEDs and Buzzer are just for demonstration purposes, as we want to demonstrate how our module works, the LEDs and Buzzer may be replaced by any other industrial device or appliance.

| Features | ESP32C | ESP 8266 | STM32 with Wi-Fi Module |
|:-:|:-:|:-:|:-:|
| **ESP-NOW Protocol Support** | Native support | No native support | Typically unsupported |
| **Power Efficiency** | High, supports deep sleep modes | Moderate, less efficient | Varies, generally less efficient |
| **Performance and Features** | High, RISC-V architecture | Moderate, Tensilica Xtensa | Varies, depends on configuration |
| **Development Ecosystem and Community Support** | Extensive, strong community | Good, less advanced | Strong for STM32, complex configuration |
| **Cost and Availability** | Cost-effective | Cheaper, fewer features | More expensive, complex integration |

> For this project we have chosen to work with the ESP32C3. In summary, the ESP32C3 is better suited for wireless switch module due to its native support for the ESP-NOW protocol, improved power efficiency, better performance, and more robust development ecosystem compared to the ESP8266 and STM32 with a Wi-Fi module, and we already had an ESP32C3 boards in our possessions.

## Hardware design

|Transmitter| Receiver |
|:-:|:-:|
| {{< figure src="images/receiver.jpg" width="300" class="center" >}} | {{< figure src="images/transmitter.jpg" width="300" class="center" >}} |


> The ESP-NOW protocol requires that two ESP32C3, one to act as a transmitter and another as a receiver. To support the wireless module the ESP32C3 was also connected to an antennae extension.
The transmitter is wired to accept input from 3 switches, each button when pressed would toggle the associated pins on the receiver sides.
The receiver is wired to 3 LEDs and when data is received from the transmitter, it would toggle the associated pins either from (HIGH to LOW) or (LOW to HIGH). The 3 LEDS, are just to indicate switching.
