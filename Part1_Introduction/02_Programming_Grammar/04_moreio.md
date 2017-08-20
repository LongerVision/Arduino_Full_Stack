# 2.4 More about Arduino IO

## 2.4.1 void tone(pin, frequency, duration);
* **brief**: read pulse length in **ms**.
* **param**:
    - **pin**: analog IO pin index, must be a value between 0 and 5, corresponding to analog pin A0 ~ A5.
    - **frequency**: **HIGH** or **LOW**. **HIGH** refers to a high level pulse, entering and leaving at a high level voltage; **LOW** refers to a low level pulse, entering and leaving at a low level voltage.
    - **duration (optional)**: **ms** to wait for the pulse to be completed.
* **return**: void.

## 2.4.2 void noTone(pin);
* **brief**: read pulse length in **ms**.
* **param**:
    - **pin**: analog IO pin index, must be a value between 0 and 5, corresponding to analog pin A0 ~ A5.
* **return**: void.

## 2.4.3 void shiftOut(dataPin, clockPin, bitOrder, value);
* **brief**: read pulse length in **ms**.
* **param**:
    - **dataPin**: analog IO pin index, must be a value between 0 and 5, corresponding to analog pin A0 ~ A5.
    - **clockPin**: analog IO pin index, must be a value between 0 and 5, corresponding to analog pin A0 ~ A5.
    - **bitOrder**: analog IO pin index, must be a value between 0 and 5, corresponding to analog pin A0 ~ A5.
    - **value**: analog IO pin index, must be a value between 0 and 5, corresponding to analog pin A0 ~ A5.
* **return**: void.

## 2.4.4 byte shiftIn(dataPin, clockPin, bitOrder);
* **brief**: read pulse length in **ms**.
* **param**:
    - **dataPin**: analog IO pin index, must be a value between 0 and 5, corresponding to analog pin A0 ~ A5.
    - **clockPin**: analog IO pin index, must be a value between 0 and 5, corresponding to analog pin A0 ~ A5.
    - **bitOrder**: analog IO pin index, must be a value between 0 and 5, corresponding to analog pin A0 ~ A5.
* **return**: byte.

## 2.4.5 unsigned long PulseIn(pin, state, timeout);
* **brief**: read pulse length in **ms**.
* **param**:
    - **pin**: analog IO pin index, must be a value between 0 and 5, corresponding to analog pin A0 ~ A5.
    - **value**: **HIGH** or **LOW**. **HIGH** refers to a high level pulse, entering and leaving at a high level voltage; **LOW** refers to a low level pulse, entering and leaving at a low level voltage.
    - **timeout (optional)**: **ms** to wait for the pulse to be completed.
* **return**: unsigned long.