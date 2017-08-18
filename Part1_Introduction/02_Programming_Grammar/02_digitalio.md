# 2.2 Arduino Digital IO

## 2.2.1 pinMode(pin, mode);
* **pin**: digital IO pin index, must be a value between 0 and 19, but 2 ~ 13 is preferred. Normally, pin number should be 0 ~ 13. Analog pins A0 ~ A5 can also be adopted, which is according to number 14 ~ 19.
* **mode**: **INPUT** or **OUTPUT**, where **INPUT** is for reading, **OUTPUT** is for writing.

## 2.2.2 digitalWrite(pin, value);
* **pin**: digital IO pin index, must be a value between 0 and 19, but 2 ~ 13 is preferred. Normally, pin number should be 0 ~ 13. Analog pins A0 ~ A5 can also be adopted, which is according to number 14 ~ 19.
* **value**: **HIGH** or **LOW**, where **HIGH** is for high level voltage, **LOW** is for low level voltage.

## 2.2.3 digitalRead(pin);
* **pin**: digital IO pin index, must be a value between 0 and 19, but 2 ~ 13 is preferred. Normally, pin number should be 0 ~ 13. Analog pins A0 ~ A5 can also be adopted, which is according to number 14 ~ 19.