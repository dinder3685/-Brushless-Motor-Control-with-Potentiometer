# -Brushless-Motor-Control-with-Potentiometer






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


