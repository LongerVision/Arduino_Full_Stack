# 5.3 Microphone Big Sound

## Hardware Wiring

![Microphone Big Sound](../../Examples/sensor-kit-for-arduino/033_microphone_bigsound.jpg)


## Sketch

The code can be found at [Examples_Arduino - sensor-kit-for-arduino - _033_Microphone_BigSound - _033_Microphone_BigSound.ino](https://github.com/LongerVisionRobot/Examples_Arduino/blob/master/sensor-kit-for-arduino/_033_Microphone_BigSound/_033_Microphone_BigSound.ino).
```
int sensorPin = A5;   // select the input pin for the potentiometer
int ledPin = 13;      // select the pin for the LED
int sensorValue = 0;  // variable to store the value coming from the sensor
int delaytime = 50;

void setup() {
  pinMode(ledPin, OUTPUT); 
  Serial.begin(9600); 
}
void loop() {
  sensorValue = analogRead(sensorPin);    
  analogWrite(ledPin, HIGH);  
  delay(delaytime);          
  analogWrite(ledPin, LOW);   
  delay(delaytime);
  Serial.println(sensorValue, DEC);  
}
```