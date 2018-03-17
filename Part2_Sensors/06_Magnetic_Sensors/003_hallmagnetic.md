# 6.1 Hall Magnetic Sensor

## Hardware Wiring
![Image](../../Examples/sensor-kit-for-arduino/003_Hall.jpg)

## Sketch
```
int Led=13;   // Define LDE Pin
int SENSOR=3; // Define 霍尔磁力传感器接口
int val;      // Define variable val
void setup()
{
  pinMode(Led,OUTPUT);  // Define LED as output
  pinMode(SENSOR,INPUT);// Define Hall Magnetic Sensor as input
}

void loop()
{
  val=digitalRead(SENSOR);//将数字接口3 的值读取赋给val
  if(val==HIGH)//当震动传感器检测有信号时,LED 亮
  {
    digitalWrite(Led, HIGH);
  }
  {
    digitalWrite(Led, LOW);
  }
}
```