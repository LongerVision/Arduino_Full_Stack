# 6.3 Linear Hall

## Hardware Wiring

![Linear Hall](../../Examples/sensor-kit-for-arduino/021_linearhall.jpg)


## Sketch

The code can be found at [Examples_Arduino - sensor-kit-for-arduino - _021_LinearHall - _021_LinearHall.ino](https://github.com/LongerVisionRobot/Examples_Arduino/blob/master/sensor-kit-for-arduino/_021_LinearHall/_021_LinearHall.ino).
```
int Led=13;       // Define LDE Pin
int buttonpin=3;  // Define linear hall sensor's pin
int val;          // Define Variable val
void setup()
{
  pinMode(Led,OUTPUT);  // Define LED as output
  pinMode(buttonpin,INPUT); // Define linear hall sensor as input
  Serial.begin(9600);
}
void loop()
{
  val=digitalRead(buttonpin); // assign digital pin 3's reading to val
  Serial.println(val);
  if(val==HIGH) // anything detected by linear hall sensor, LED starts flashing
  {
    digitalWrite(Led,HIGH);
  }
  else
  {
    digitalWrite(Led,LOW);
  }
}
```