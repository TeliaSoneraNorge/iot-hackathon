# Blink the NodeMCU

## Parts needed
- NodeMCU

## Instructions

- In Atom, open the project folder for this exercise; ```exercises/1-blink```. If you have not cloned or downloaded the repository already, you need to do it now.
- Press the *build* button ![](img/build.png) at the top of the left menu to compile the project.
- Press the *upload* button ![](img/upload.png) below the build button to upload the code to the NodeMCU. The blue LED will flash during this process.
- After the upload is complete, the red LED should start blinking once per second!
- Have a look at the code in ```exercises/1-blink/src/main.ino``` and see if you can change the blinking behaviour, for example making it blink faster.

## Code

The red LED is connected internally to the pin named D0.

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

## Troubleshooting

- On Windows, you might have to add the following line to platformio.ini, replacing COMx with the correct port for your computer: ```upload_port = COMx```