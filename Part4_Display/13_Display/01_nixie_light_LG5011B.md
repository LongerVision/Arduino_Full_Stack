# 13.1 Nixie Light LG5011B

## Hardware Wiring
![Image](../../Examples/geek-workshop/studynotes/006_nixielightLG5011BSR.jpg)

## Sketch
```
//set IO to control each piece. Please refer to the official definition of LG5011B.
int a=7;
int b=6;
int c=5;
int d=11;
int e=10;
int f=8;
int g=9;
int dp=4;

//Display digit 1
void digital_1(void)
{
  unsigned char j;
  digitalWrite(c,LOW);  //light up c
  digitalWrite(b,LOW);  //light up b
  for(j=7;j<=11;j++)    //turn down others
    digitalWrite(j,HIGH);
  digitalWrite(dp,HIGH);//turn down dot point
}
//Display digit 2
void digital_2(void)
{
  unsigned char j;
  digitalWrite(b,LOW);
  digitalWrite(a,LOW);
  for(j=9;j<=11;j++)
    digitalWrite(j,LOW);
  digitalWrite(dp,HIGH);
  digitalWrite(c,HIGH);
  digitalWrite(f,HIGH);
}
//Display digit 3
void digital_3(void)
{
  unsigned char j;
  digitalWrite(g,LOW);
  digitalWrite(d,LOW);
  for(j=5;j<=7;j++)
    digitalWrite(j,LOW);
  digitalWrite(dp,HIGH);
  digitalWrite(f,HIGH);
  digitalWrite(e,HIGH);
}
//Display digit 4
void digital_4(void)
{
  digitalWrite(c,LOW);
  digitalWrite(b,LOW);
  digitalWrite(f,LOW);
  digitalWrite(g,LOW);
  digitalWrite(dp,HIGH);
  digitalWrite(a,HIGH);
  digitalWrite(e,HIGH);
  digitalWrite(d,HIGH);   
}
//Display digit 5
void digital_5(void)
{
  unsigned char j;
  for(j=7;j<=9;j++)
    digitalWrite(j,LOW);
  digitalWrite(c,LOW);
  digitalWrite(d,LOW);
  digitalWrite(dp,HIGH);
  digitalWrite(b,HIGH);
  digitalWrite(e,HIGH); 
}
//Display digit 6
void digital_6(void)
{
  unsigned char j;
  for(j=7;j<=11;j++)
    digitalWrite(j,LOW);
  digitalWrite(c,LOW);
  digitalWrite(dp,HIGH);
  digitalWrite(b,HIGH);   
}
//Display digit 7
void digital_7(void)
{
  unsigned char j;
  for(j=5;j<=7;j++)
    digitalWrite(j,LOW);
  digitalWrite(dp,HIGH);
  for(j=8;j<=11;j++)
    digitalWrite(j,HIGH);
}
//Display digit 8
void digital_8(void)
{
  unsigned char j;
  for(j=5;j<=11;j++)
    digitalWrite(j,LOW);
  digitalWrite(dp,HIGH);
}
void setup()
{
  int i;    //Define variable i
  for(i=4;i<=11;i++)
    pinMode(i,OUTPUT);  //set pins 4~11 as output
}
void loop()
{  
  while(1)
  {
    digital_1();    //digit 1
    delay(2000);    //delay 2 seconds
    digital_2();
    delay(2000);
    digital_3();
    delay(2000);
    digital_4();
    delay(2000);
    digital_5();
    delay(2000);
    digital_6();
    delay(2000);
    digital_7();
    delay(2000);
    digital_8();
    delay(2000);   
  }
}
```


## Assignments
How to display digits **9** and **0** on **LG5011B**?
