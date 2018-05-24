# 6-LED Water Lights


In our first class, a single LED example was given. Now, we'll discuss a bit more about LED control with 6 LED lights.

## Hardware Wiring

![LED Water Lights](../Examples/geek-workshop/studynotes/01_6ledwaterlights.jpg)


## Sketch
```
//define Led IO pin
int Led1 = 1;
int Led2 = 2;
int Led3 = 3;
int Led4 = 4;
int Led5 = 5;
int Led6 = 6;

//Led water light style 1 
void style_1(void)
{
  unsigned char j;
  for(j=1; j <= 6; j++)
  {
    digitalWrite(j, HIGH);
    delay(200);
  }
  for(j=6; j >= 1; j--)
  {
    digitalWrite(j, LOW);
    delay(200);
  }
}

void setup()
{
  unsigned char i;
  for(i=1; i<=6; i++)//set pin 1~6 as output mode in order
    pinMode(i, OUTPUT);//set pin i as output mode
}

void loop()
{
  style_1(); //style 1
}
```
