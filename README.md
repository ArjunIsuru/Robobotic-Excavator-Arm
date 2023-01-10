# Robobotic-Excavator-Arm
Controlling the Arm using Joy stick
*Robotic Arm Joy Stick*

First I got the joy stick as a coordinate Plane...
Then I programmed Mini arm as X axis and the Major arm as Y  axis...

One gap has a 10 mm (1cm) space...

If I move the Joy stick as (±x,±y)
coordinates...That means the robotic arm is rotated with

©x =   ±x/10 × 180 = ±18 x

©y =   ±y/10 × 180 = ±18 y

_Code:-_

#include <Servo.h>

Servo myservo1; 
Servo myservo2;

int xPos = 0;
int yPos = 0;

void setup() {

pinMode(A0, INPUT);
pinMode(A1, INPUT);
myservo1.attach(5);
myservo2.attach(6);
}

void loop() {

xPos = map(analogRead(A0),0,1023,0,180);

yPos= map(analogRead(A1),0,1023,0,180);

myservo1.write(xPos);
myservo2.write(yPos);
}

*Arjun ( Isuru ) 🍁✨*
