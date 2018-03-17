# 5.4 Microphone

## Hardware Wiring
![Image](../../Examples/sensor-kit-for-arduino/034_microphone.jpg)

## Sketch
```
int Led=13;       // Define LDE Pin
int buttonpin=3;  // Define D0 sensor's pin
int val;          // Define Variable val
void setup()
{
  pinMode(Led,OUTPUT);      // Define LED as output
  pinMode(buttonpin,INPUT); // Define sensor D0 as output
  Serial.begin(9600);
}
void loop()
{
  val=digitalRead(buttonpin);//将数字接口3的值读取赋给val
  if(val==HIGH)//当声音检测模块检测有信号时，LED 闪烁
  {
    digitalWrite(Led,HIGH);
  }
  else
  {
    digitalWrite(Led,LOW);
  }
  Serial.println(val, DEC);
}
```