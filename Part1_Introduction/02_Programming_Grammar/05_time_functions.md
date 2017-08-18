# 2.5 Arduino Time Functions

## 2.5.1 delay(ms);
* **brief**: delay several milliseconds.
* **ms**: milliseconds.
* **return**: void.

## 2.5.2 delayMicroseconds(us);
* **brief**: delay several microseconds.
* **us**: microseconds.
* **return**: void.

## 2.5.3 millis();
* **brief**: return the time length in milliseconds since the most recent rebooting. Clearly, the longest time that can be recorded is 2^32-1 milliseconds. After that, the time length will starts from 0 again.
* **return**: an unsigned long.

## 2.5.4 micros();
* **brief**: return the time length in microseconds since the most recent rebooting. Clearly, the longest time that can be recorded is 2^32-1 microseconds. After that, the time length will starts from 0 again.
* **return**: an unsigned long.
