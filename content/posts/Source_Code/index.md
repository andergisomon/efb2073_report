+++
title = 'Source code'
summary = "View our code in detail"
draft = false
weight = 10
+++

> Some C code for your viewing pleasure. 

``` c
#include "freertos.h"
#include <drivers/gpio.h>

// I'm a comment. Everyone ignores me. I'm lonely. That makes me sad.

extern void init_gpio();
void app_main() {
    init_gpio();
}
```