# 4.4 IR Obstacle Avoidance

## Hardware Wiring
![Image](../../Examples/sensor-kit-for-arduino/028_ir_obstacleavoidance.jpg)

## Sketch
```
int Led=13;       // Define LED Pin
int buttonpin=3;  // Define the obstacle voidance pin
int val;          // Define a variable val
void setup()
{
  pinMode(Led,OUTPUT);//定义LED 为输出接口
  pinMode(buttonpin,INPUT);//定义避障传感器为输出接口
  Serial.begin(9600);
}
void loop()
{
  val=digitalRead(buttonpin);//将数字接口3的值读取赋给val
  Serial.println(val);
  if(val==HIGH)//当避障传感器检测有信号时，LED 闪烁
  {
    digitalWrite(Led,HIGH);
  }
  else
  {
    digitalWrite(Led,LOW);
  }
}
```