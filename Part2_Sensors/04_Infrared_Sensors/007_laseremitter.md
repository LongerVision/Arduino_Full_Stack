# 4.2 Laser Emitter

## Hardware Wiring
![Image](../../Examples/sensor-kit-for-arduino/007_laseremitter.jpg)

## Sketch
Please refer to [Examples_Arduino - sensor-kit-for-arduino - _007_LaserEmit - _007_LaserEmit.ino](https://github.com/LongerVisionRobot/Examples_Arduino/blob/master/sensor-kit-for-arduino/_007_LaserEmit/_007_LaserEmit.ino).
```
void setup()
{
  pinMode(13, OUTPUT); // Define Pin 13 as Digital Output
}
void loop() {
  digitalWrite(13, HIGH); // Open Laser Head
  delay(1000);
  // Delay 1 second
  digitalWrite(13, LOW); // Close Laser Head
  delay(1000);
  // Delay 1 second
}
```