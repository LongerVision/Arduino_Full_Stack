# 3.5 Photoresistor

## Hardware Wiring
![Image](../../Examples/sensor-kit-for-arduino/015_photoresistor.jpg)

## Sketch
Please refer to [Examples_Arduino - sensor-kit-for-arduino - _015_PhotoResistor - _015_PhotoResistor.ino](https://github.com/LongerVisionRobot/Examples_Arduino/blob/master/sensor-kit-for-arduino/_015_PhotoResistor/_015_PhotoResistor.ino).
```
int sensorPin = 2;
int value = 0;
void setup() {
  pinMode(sensorPin, INPUT);
  Serial.begin(9600);
}
void loop() {
  value = analogRead(sensorPin);
  Serial.println(value, DEC);
  delay(50);
}
```