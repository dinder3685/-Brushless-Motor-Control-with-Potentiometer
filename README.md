# -Brushless-Motor-Control-with-Potentiometer
/*
Components Used
Arduino Uno
Power Distribution Board
Breadboard
ESC (Electronic Speed Controller)
Brushless Motor
Fuse
Potentiometer
Circuit Diagram

Connections
ESC Signal Pin: Connect to Arduino pin 2
ESC Power Pins: Connect to the Power Distribution Board
Potentiometer Middle Pin: Connect to Arduino analog pin A0
Potentiometer Other Pins: Connect to 5V and GND


*/











#include <Servo.h>

#define ESC_PIN 2

Servo esc;

void setup() 
{
  esc.attach(ESC_PIN, 1000, 2000);
  esc.write(0);
  delay(2000);
}

void loop() 
{
  int potValue = analogRead(A0);
  potValue = constrain(potValue, 550, 1023);  // Read upper half of potentiometer value.
  int motorSpeed = map(potValue, 550, 1023, 0, 180);
  esc.write(motorSpeed);  
}


