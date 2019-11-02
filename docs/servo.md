# Servo SG90
[Aliexpress](https://www.aliexpress.com/item/32841541380.html), ~1 USD

```
Range 0-180 deg
Brown: GND
Red: +5V
Orange: digital output pin
```

## Usage
```c
#include <Servo.h>

Servo myservo;
int pos = 0;

void setup() {
  myservo.attach(9);
}

void loop() {
  if(pos > 180) pos = 0;
  myservo.write(pos);
  Serial.println(pos);
  delay(15);
  pos += 1;
}
```

## Dependencies:
- Servo
