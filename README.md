# 2-Servo-motor-system
#include <Servo.h>
Servo servo1;
Servo servo2;
int angle=0; 



void setup()
{
 servo1.attach(8);
 servo1.write(angle);

 servo2.attach(13);
 servo2.write(angle);
 delay(1000);}


void loop()
{
  // scan from 0 to 180 degrees
  for(angle = 10; angle < 180; angle++)  
  {                                  
    servo1.write(angle);  
    servo2.write(angle); 
    delay(15);                   
  } 
  // now scan back from 180 to 0 degrees
  for(angle = 180; angle > 10; angle--)    
  {                                
    servo1.write(angle); 
    servo2.write(angle); 
    delay(15);       
  } 
}
