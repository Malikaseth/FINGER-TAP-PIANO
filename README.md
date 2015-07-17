# FINGER-TAP-PIANO
I developed this project in my first year at a workshop at NSIT Delhi. 
This is the code i used on Engeria Software.


#include <CapTouch.h>
#define BUTTON1 P2_3
#define BUTTON2 P2_4
#define BUTTON3 P2_5
#define BUTTON4 P2_2
#define BUTTON5 P2_1
#define BUTTON6 P2_0
#define LED1 P1_0
#define LED2 P1_1
#define LED3 P1_2
#define LED4 P1_3
#define LED5 P1_4
#define LED6 P1_5
uint8_t state = false;
CapTouch testbutton1 = CapTouch(BUTTON1, TOUCH_BUTTON);
CapTouch testbutton2 = CapTouch(BUTTON2, TOUCH_BUTTON);
CapTouch testbutton3 = CapTouch(BUTTON3, TOUCH_BUTTON);
CapTouch testbutton4 = CapTouch(BUTTON4, TOUCH_BUTTON);
CapTouch testbutton5 = CapTouch(BUTTON5, TOUCH_BUTTON);
CapTouch testbutton6 = CapTouch(BUTTON6, TOUCH_BUTTON);
boolean buttonState1 = false;
boolean buttonState2 = false;
boolean buttonState3 = false;
boolean buttonState4 = false;
boolean buttonState5 = false;
boolean buttonState6 = false;
boolean State1 = false;
boolean State2 = false;
boolean State3 = false;
boolean State4 = false;
boolean State5 = false;
boolean State6 = false;

void setup() {
 pinMode(LED1,OUTPUT);
 pinMode(LED2, OUTPUT);
 pinMode(LED3, OUTPUT);
 pinMode(LED4, OUTPUT);
 pinMode(LED5, OUTPUT);
 pinMode(LED6, OUTPUT);
}
void loop() {
 if (testbutton1.isTouched() > 0) {
 if (buttonState1 == false && State1==false) {
 buttonState1 = true;
 State1=true;
 tone(P1_6, 523, 1000);
 digitalWrite(LED1,State1);
 delay(500);
 State1=false;
 digitalWrite(LED1,State1);
   }
   
 } 
 else if (testbutton2.isTouched() > 0) {
 if (buttonState2 == false && State2== false) {
 buttonState2 = true;
 State2 = true;
 tone(P1_6, 587, 1000);
 digitalWrite(LED2,State2);
 delay(500);
 State2 =false;
 digitalWrite(LED2,State2);
 }
 
 }
 else if (testbutton3.isTouched() > 0) {
 if (buttonState3 == false && State3== false) {
 buttonState3 = true;
 State3 = true;
 tone(P1_6, 639, 1000);
 digitalWrite(LED3,State3);
 delay(500);
 State3 =false;
 digitalWrite(LED3,State3);
 }
 
 }
 else if (testbutton4.isTouched() > 0) {
 if (buttonState4 == false && State4== false) {
 buttonState4 = true;
 State4 = true;
 tone(P1_6, 698, 1000);
 digitalWrite(LED4,State4);
 delay(500);
 State4 =false;
 digitalWrite(LED4,State4);
 }
 }
 else if (testbutton5.isTouched() > 0) {
 if (buttonState5 == false && State5== false) {
 buttonState5 = true;
 State5 = true;
 tone(P1_6, 783, 1000);
 digitalWrite(LED5,State5);
 delay(500);
 State5 =false;
 digitalWrite(LED5,State5);
 }
 }
 else if (testbutton6.isTouched() > 0) {
 if (buttonState6 == false && State6== false) {
 buttonState6 = true;
 State6 = true;
 tone(P1_6, 880, 1000);
 digitalWrite(LED6,State6);
 delay(500);
 State6 =false;
 digitalWrite(LED6,State6);
 }
 }
 
 else {
 buttonState1 = false;
 buttonState2 = false;
 buttonState3 = false;
 buttonState4 = false;
 buttonState5 = false;
 buttonState6 = false;
 State1=false;
 State2=false;
 State3=false;
 State4=false;
 State5=false;
 State6=false;
 }
}                                                     

