# 4.5 IR Line Tracking

## Hardware Wiring
![Image](../../Examples/sensor-kit-for-arduino/029_ir_linetracking.jpg)

## Sketch
Please refer to [Examples_Arduino - sensor-kit-for-arduino - _029_IR_LineTracking - _029_IR_LineTracking.ino](https://github.com/LongerVisionRobot/Examples_Arduino/blob/master/sensor-kit-for-arduino/_029_IR_LineTracking/_029_IR_LineTracking.ino).
```
int Led=13;       // Define LED Pin
int buttonpin=3;  // Define the line tracking sensor's pin
int val;          // Define a variable val
void setup()
{
  pinMode(Led,OUTPUT);  // Define LED as Output
  pinMode(buttonpin,INPUT); // Define line tracking sensor as input
  Serial.begin(9600);
}
void loop()
{
  val=digitalRead(buttonpin);// Assign the value of digital pin 3 to val
  Serial.println(val);
  if(val==HIGH)   // if anything detected by line tracking sensor, LED starts flashing.
  {
    digitalWrite(Led,HIGH);
  }
  else
  {
    digitalWrite(Led,LOW);
  }
}
```