Arduino Brushless Motor Control with Potentiometer
This project demonstrates how to control a brushless motor using an Arduino, a potentiometer, and an ESC (Electronic Speed Controller). By adjusting the potentiometer, the Arduino changes the speed of the motor.

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


How It Works
Initialization: The ESC is initialized in the setup() function, with a 2-second delay to allow the ESC to initialize properly.
Potentiometer Reading: In the loop() function, the potentiometer's analog value is read from pin A0.
Value Constraint: The potentiometer value is constrained to the upper half (550-1023) to read only the forward movement.
Mapping: The constrained value is mapped to the ESC's input range (0-180 degrees).
Motor Control: The mapped value is then sent to the ESC to control the motor speed.
Safety Precautions
Ensure the fuse is appropriately rated to prevent overcurrent conditions.
Double-check all connections before powering the circuit.
Project Video



