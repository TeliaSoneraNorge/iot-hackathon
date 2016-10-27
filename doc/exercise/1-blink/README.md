# Blink the LED

## Parts needed
- NodeMCU
- 220ohm resistor
- Any colored LED
- Two wires

## How to connect
Connect one wire from the long leg (+) to the digital pin D0.
Connect one wire from the short leg (-) to one of the pins named GND.

## Code
```Arduino
// the setup function runs once when you press reset or power the board
void setup() {
  // initialize digital pin D0 as an output.
  pinMode(D0, OUTPUT);
}

// the loop function runs over and over again forever
void loop() {
  digitalWrite(D0, HIGH);   // turn the LED on
  delay(1000);              // wait for a second
  digitalWrite(D0, LOW);    // turn the LED off
  delay(1000);              // wait for a second
}
```
