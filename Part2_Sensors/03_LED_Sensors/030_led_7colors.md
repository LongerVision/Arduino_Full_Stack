# 3.8 LED 7 Colors

## Hardware Wiring

![LED 7 Colors](../../Examples/sensor-kit-for-arduino/030_led_7colors.jpg)


## Sketch

The code can be found at [Examples_Arduino - sensor-kit-for-arduino - _030_LED_7Colors - _030_LED_7Colors.ino](https://github.com/LongerVisionRobot/Examples_Arduino/blob/master/sensor-kit-for-arduino/_030_LED_7Colors/_030_LED_7Colors.ino).
```
/*
  Blink
  Turns on an LED on for two second, then off for two second, repeatedly.
 
  This example code is in the public domain.
 */

void setup() {                
  // initialize the digital pin as an output.
  // Pin 13 has an LED connected on most Arduino boards:
  pinMode(13, OUTPUT);     
}

void loop() {
  digitalWrite(13, HIGH);   // set the LED on
  delay(2000);              // wait for a second
  digitalWrite(13, LOW);    // set the LED off
  delay(2000);              // wait for a second
}
```