# 14.1 Bluetooth

## Example 1:

## Hardware Wiring
![Image](../../Examples/geek-workshop/studynotes/006_nixielightLG5011BSR.jpg)

## Sketch
Please refer to [https://howtomechatronics.com/tutorials/arduino/arduino-and-hc-05-bluetooth-module-tutorial/](https://howtomechatronics.com/tutorials/arduino/arduino-and-hc-05-bluetooth-module-tutorial/).
```
#define ledPin 7
int state = 0;
void setup() {
  pinMode(ledPin, OUTPUT);
  digitalWrite(ledPin, LOW);
  Serial.begin(38400); // Default communication rate of the Bluetooth module
}
void loop() {
  if(Serial.available() > 0){ // Checks whether data is comming from the serial port
    state = Serial.read(); // Reads the data from the serial port
 }
 if (state == '0') {
  digitalWrite(ledPin, LOW); // Turn LED OFF
  Serial.println("LED: OFF"); // Send back, to the phone, the String "LED: ON"
  state = 0;
 }
 else if (state == '1') {
  digitalWrite(ledPin, HIGH);
  Serial.println("LED: ON");;
  state = 0;
 } 
}
```


## Example 2:

## Hardware Wiring
![Image](../../Examples/geek-workshop/studynotes/006_nixielightLG5011BSR.jpg)

## Sketch
Please refer to [https://create.arduino.cc/projecthub/user206876468/arduino-bluetooth-basic-tutorial-d8b737](https://create.arduino.cc/projecthub/user206876468/arduino-bluetooth-basic-tutorial-d8b737).
