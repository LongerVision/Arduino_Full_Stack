# 14.1 Serial


## Hardware Wiring



## Sketch
The code can be found at [Examples_Arduino - arduinocc - _001_Serial - _001_Serial.ino](https://github.com/LongerVisionRobot/Examples_Arduino/blob/master/arduinocc/_001_Serial/_001_Serial.ino).
You can also refer to [https://www.arduino.cc/en/Tutorial/SoftwareSerialExample](https://www.arduino.cc/en/Tutorial/SoftwareSerialExample).
```
#include <SoftwareSerial.h>

SoftwareSerial mySerial(0,1);	// RX=0, TX=1

void setup() {
  // Open serial communications and wait for port to open:
  Serial.begin(115200);
  while(!Serial) {
    ;	// wait for serial port to connect. Needed for Leonardo only
  }

  // set the data rate for the SoftwareSerial port
  mySerial.begin(115200);
}

void loop() {
  if(mySerial.available())
    Serial.write(mySerial.read());
  if(Serial.available())
    mySerial.write(Serial.read());
}
```

