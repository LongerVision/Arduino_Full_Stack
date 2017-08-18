# 2.3 Arduino Analog IO

## 2.3.1 analogReference(type);

## 2.3.2 analogRead(pin);

## 2.3.3 analogWrite(pin, value);
* **pin**: digital IO pin index, must be a value between 0 and 19, but 2 ~ 13 is preferred. Normally, pin number should be 0 ~ 13. Analog pins A0 ~ A5 can also be adopted, which is according to number 14 ~ 19.
* **value**: **HIGH** or **LOW**, where **HIGH** is for high level voltage, **LOW** is for low level voltage.