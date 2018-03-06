
# elo_trek
---

This was a standard led light my daughter Jordi bought me for my birthday. I later replaced the internal electronics and leds with my own.

I have it configured so that I can use it as any other ELO_LED light but when the ELO_DFMON sends state changes, the light will display low and critcally low indicators.

Here is mt elo_firmware ```custom.h```
```c++
#ifdef ELO_TREK
    #define ELO_LED
    #define ELO_MQTT
    #define ELO_INDICATOR
    #define NUM_LEDS 4
    #define DEVICE_NAME "elo_trek"
    #define MAX_INDICATORS 1
#endif
```

You can see it supports 4 leds and a single indicator. Using the ```elo_mobile``` app, you can choose what that indicator will display.