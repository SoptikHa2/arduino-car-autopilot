# Joystick HW-504

[Aliexpress](https://www.aliexpress.com/item/4000282446081.html), ~0.7 USD

```
Range: 360deg (both x, y)
Extra: Button click
```

## Usage

```
VCC (+5V): +5V
GND: GND
VRx: ANALOG 0
VRy: ANALOG 1
SW: DIGITAL 2
```

```c
// Arduino pin numbers
const int SW_pin = 2; // digital pin connected to switch output
const int X_pin = 0; // analog pin connected to X output
const int Y_pin = 1; // analog pin connected to Y output

void setup() {
  pinMode(SW_pin, INPUT);
  digitalWrite(SW_pin, HIGH);
  Serial.begin(9600);
}

void loop() {
  Serial.print("Switch:  ");
  Serial.print(digitalRead(SW_pin));
  Serial.print("\n");
  Serial.print("X-axis: ");
  Serial.print(analogRead(X_pin));
  Serial.print("\n");
  Serial.print("Y-axis: ");
  Serial.println(analogRead(Y_pin));
  Serial.print("\n\n");
  delay(500);
}
```
