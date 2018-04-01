# 15.2 Arduino UNO and Longer Vision Robot Arduino Extension Board


## Step 1: Arduino UNO R3

Find a suitable place and fix Arduino UNO R3 onto the top Acrylic plate:

![Image](../../Examples/longervisionrobot/assemble_lvrarduino_01.jpg)


## Step 2:  Arduino Extension Board

Just directly plugin Longer Vision Robot Arduino Extension Board onto the Arduino UNO R3:

![Image](../../Examples/longervisionrobot/assemble_lvrarduino_02.jpg)


## Step 3: Batteries

And then, find a suitable place on the top Acrylic plate and fix the given black battery box, and put two batteries into the box. And it's NOT hard to connect two battery cables onto Arduino Extension Board's power:
* **<span style="color:red">red cable</span>**: power +
* **<span style="color:black">black cable</span>**: power -, namely, ground.

You now can simply test if the battery and power button on Arduino Extension Board is properly first:

![Image](../../Examples/longervisionrobot/assemble_lvrarduino_03.jpg)

As we can see, the battery and the power switch on Arduino Extension Board works fine.


## Step 4: Test 4 Wheels

We now connect Arduino UNO R3 on the vehicle to our laptop, and download the following sketch onto Arduino UNO. 

### Sketch

```
int rightMotor1 = 14;
int rightMotor2 = 15;
int leftMotor1 = 16;
int leftMotor2 = 17;

int leftPWM = 5;
int rightPWM = 6;

void setup() {
  // put your setup code here, to run once:
  pinMode(leftMotor1, OUTPUT);
  pinMode(leftMotor2, OUTPUT);
  pinMode(rightMotor1, OUTPUT);
  pinMode(rightMotor2, OUTPUT);
  pinMode(leftPWM, OUTPUT);
  pinMode(rightPWM, OUTPUT);
}

void loop() {
  // put your main code here, to run repeatedly:
  analogWrite(leftPWM, 250);  //设置PWM输出，即设置速度
  analogWrite(rightPWM, 250);

  digitalWrite(leftMotor1, LOW);
  digitalWrite(leftMotor2, HIGH);
  digitalWrite(rightMotor1, LOW);
  digitalWrite(rightMotor2, HIGH);
}
```