# 9.4 Relay

## Hardware Wiring
![Image](../../Examples/sensor-kit-for-arduino/016_relay.jpg)

## Sketch
```
int relay = 10; // Define relay pin
void setup()
{
  pinMode(relay,OUTPUT); // Define relay pin as output
}
void loop()
{
  digitalWrite(relay,HIGH); // Relay open
  delay(1000);
  digitalWrite(relay,LOW);  // Relay close
  delay(1000);
}
```