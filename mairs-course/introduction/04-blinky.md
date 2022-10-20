# LED Blinking
Need to include the following header file
```c
#include "driver/gpio.h" // gpio means general purpose input output
```

Example
```c
#include <stdio.h>
#include "driver/gpio.h"
#include "freertos/FreeRTOS.h"
#include "freertos/task.h"

#define PIN 2 // in-built LED pin number (for most of the ESP32 boards)

void app_main(void)
{
  // Tell espidf which pin to use as GPIO
  esp_rom_gpio_pad_select_gpio(PIN); 

  // Tell espidf GPIO whether the pin is input or output
  gpio_set_direction(PIN, GPIO_MODE_OUTPUT);

  int isOn = 0; // whether on or off 
  while (true)
  {
    isOn = !isOn; // toggle 0/1
    gpio_set_level(PIN, isOn);

    //delay 
    vTaskDelay(1000 / portTICK_PERIOD_MS); //1000 ms 
  }
}
```