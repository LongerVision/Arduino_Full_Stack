# 4.4 IR Obstacle Avoidance

## Hardware Wiring
![Image](../../Examples/sensor-kit-for-arduino/028_ir_obstacleavoidance.jpg)

## Sketch
```
int Led=13;       // Define LED Pin
int buttonpin=3;  // Define the obstacle avoidance sensor's pin
int val;          // Define a variable val
void setup()
{
  pinMode(Led,OUTPUT);      // Define LED as output
  pinMode(buttonpin,INPUT); // Define obstacle avoidance sensor as input
  Serial.begin(9600);
}
void loop()
{
  val=digitalRead(buttonpin); // Assign digital pin 3 to val
  Serial.println(val);
  if(val==HIGH)   //当避障传感器检测有信号时，LED 闪烁
  {
    digitalWrite(Led,HIGH);
  }
  else
  {
    digitalWrite(Led,LOW);
  }
}
```