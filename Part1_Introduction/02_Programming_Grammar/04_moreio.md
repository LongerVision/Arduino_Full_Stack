# 2.4 More about Arduino IO

## 2.4.1 PulseIn(pin, state, timeout);
* **brief**: read pulse length in **ms**.
* **param**:
    - **pin**: analog IO pin index, must be a value between 0 and 5, corresponding to analog pin A0 ~ A5.
    - **value**: **HIGH** or **LOW**. **HIGH** refers to a high level pulse, entering and leaving at a high level voltage; **LOW** refers to a low level pulse, entering and leaving at a low level voltage.
    - **timeout (optional)**: **ms** to wait for the pulse to be completed.
* **return**: unsigned long.