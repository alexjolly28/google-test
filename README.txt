# google-test

#include <Servo.h>

Servo right_motor;
Servo left_motor;



int left_motor_fs = 180; //left motor inte forward speed
int left_motor_rs = 0; //left motor nte revers speed


int right_motor_fs = 0; //right motor nte forward speed
int right_motor_rs = 180; //right motor nte revers speed



void setup()
{
  Serial.begin(9600);

  right_motor.attach(10);
  left_motor.attach(11);
}



void forward()
{

  right_motor.write(right_motor_fs);
  left_motor.write(left_motor_fs);

}

void backward()
{
  right_motor.write(right_motor_rs);
  left_motor.write(left_motor_rs);
}

void left()
{
  right_motor.write(right_motor_fs);
  left_motor.write(left_motor_rs);
}

void right()
{
  right_motor.write(right_motor_rs);
  left_motor.write(left_motor_fs);
}


void stp()
{
  right_motor.write(90);
  left_motor.write(90);
}




void loop()
{


}
