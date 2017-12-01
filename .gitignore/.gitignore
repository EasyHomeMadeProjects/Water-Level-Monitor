//Automatic Water Level control system by Easy HomeMade Projects.
//Arduino code written by Engr. Usman Ahmad.
//Use arduino UNO or Arduino NANO.
#include <LiquidCrystal.h>
int level1=A1;
int level2=A2;
int level3=A3;
int level4=A4;
int level5=A5;
int motor=6;
int a;
int b;
int c;
int d;
int e;
int r; //Water Pump status flag
int m=0; //water Pump flag
int z=111; // Adjust this value from 100 to 1023 if your circuit do not show correct value. 
  

LiquidCrystal lcd(12, 11, 5, 4, 3, 2);
void setup()
{
pinMode(level1,INPUT);
pinMode(level2,INPUT);
pinMode(level3,INPUT);
pinMode(level4,INPUT);
pinMode(level5,INPUT);
pinMode(motor,OUTPUT);
lcd.begin(20, 4); // if you are using 16x2 line LCD, then replace these values and also adjust all LCD text for 1st and 2nd line in the loop below. 
}

void loop()
{

r=digitalRead(motor);
a=analogRead(level1);
b=analogRead(level2);
c=analogRead(level3);
d=analogRead(level4);
e=analogRead(level5);
lcd.clear();
lcd.setCursor(2,0);              
lcd.print("Easy HM Projects");   
lcd.setCursor(0,1);              
lcd.print("Water Level Monitor.");

if(e>z && d>z && c>z && b>z && a>z )
{
  {
    digitalWrite(motor,LOW);
  }
lcd.setCursor(1,2);
lcd.print("Tank is 100% FULL");
}
else
{
  if(e<z && d>z && c>z && b>z && a>z )
{
lcd.setCursor(1,2);
lcd.print("Tank is 80% FULL");
}
else
{
  if(e<z && d<z && c>z && b>z && a>z )
{
lcd.setCursor(1,2);
lcd.print("Tank is 60% FULL");
}
else
{
if(e<z && d<z && c<z && b>z && a>z )
{

lcd.setCursor(1,2);
lcd.print("Tank is 40% FULL");
}
else
if(e<z && d<z && c<z && b<z && a>z )
{

lcd.setCursor(1,2);
lcd.print("Tank is 20% FULL");
}
else
{if(e<z && d<z && c<z && b<z && a<z )
{
 {
digitalWrite(motor,HIGH);
}

lcd.setCursor(3,2);
lcd.print("Tank is EMPTY");
}
}}}}
if(r==LOW)
{
lcd.setCursor(0,3);
lcd.print("Water Pump is (OFF)");
}
else
{
lcd.setCursor(0,3);
lcd.print("Water Pump is (ON)");
}
{
delay(100);
lcd.clear();

}}
