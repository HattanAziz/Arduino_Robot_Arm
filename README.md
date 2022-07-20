# Arduino_Robot_Arm

1- The first step is to assemble the arm and merge it together correctly and connect the motors together , Majoring in electrical and mechanical engineering

![Screenshot 2022-07-20 155318](https://user-images.githubusercontent.com/109594520/179989796-91e9f74a-df79-4507-8431-6ac284b954a0.png)


After you finish assembling the arm, you start programming the robotic arm so that you can use it


2 - we open arduino ide 

3- Make sure you select the right board from tools > board > arduino avr board > arduino UNO


 ![image](https://user-images.githubusercontent.com/109594520/179990386-4fbc3b53-0988-4f8f-981b-beb92bff045a.png)
 
 4 -  Make sure you select the right port fome tools > port 
 
 ![image](https://user-images.githubusercontent.com/109594520/179991673-237eb7e4-434b-4198-8f40-69c3432a900e.png)


5 - go to file > exampels > servo > sweep  
now you can program

![image](https://user-images.githubusercontent.com/109594520/179992503-419ba6d1-21c0-4ca2-8e5b-e78ddef78bfc.png)

6 - And you can set the angle of the arm and the speed 

the code :

#include <Servo.h>

Servo myservo;  // create servo object to control a servo
// twelve servo objects can be created on most boards

int pos = 0;    // variable to store the servo position

void setup() {
  myservo.attach(9);  // attaches the servo on pin 9 to the servo object
}

void loop() {
  for (pos = 0; pos <= 180; pos += 1) { // goes from 0 degrees to 180 degrees
    // in steps of 1 degree
    myservo.write(pos);              // tell servo to go to position in variable 'pos'
    delay(15);                       // waits 15 ms for the servo to reach the position
  }
  for (pos = 180; pos >= 0; pos -= 1) { // goes from 180 degrees to 0 degrees
    myservo.write(pos);              // tell servo to go to position in variable 'pos'
    delay(15);                       // waits 15 ms for the servo to reach the position
  }
}



7-We use a piece called Uno to connect between the robotic arm and the computer, and we connect it in a correct way ,
note : Be careful if you don't connect the uno piece correctly, it can damage your device

![image](https://user-images.githubusercontent.com/109594520/179995584-bb3cd65c-3a6d-40ab-ade9-2f3ce02977a6.png)

![image](https://user-images.githubusercontent.com/109594520/179995960-1e81802a-797b-4f57-b808-70567a9fd0b8.png)




https://user-images.githubusercontent.com/109594520/179993612-69fb8aec-3395-44bc-bf66-d7e2bdd87122.mp4

![image](https://user-images.githubusercontent.com/109594520/179993785-8d02b473-81f1-4d20-8f07-0e5effaa2565.png)

