加速*4
```C++
float a=millis();
int x=100;
void setup() {
  pinMode(5,OUTPUT); 
  pinMode(6,OUTPUT); 
}


void loop() {
  
float b=millis();

 if ((b-a)>=5000)
 {
  x = x+50;
  a=b;
  if (x>=255)x=99;
  Serial.print(x);
 }
 analogWrite(5,x);
 digitalWrite(6,0);
 }
 ```
 按鈕加速:
 ```C++
 float a=millis();
int x=100;
void setup() {
  pinMode(5,OUTPUT); 
  pinMode(6,OUTPUT); 
  pinMode(2,INPUT);
}
void mothor(int x)
{
  analogWrite(5,x);
  digitalWrite(6,0);
}


void loop() {
  

 if (digitalRead(2)==LOW)
 {
  while(digitalRead(2)==LOW )
  x = x+50;
 }
 if(x>=254)
 {
  x = 255;
 }
 if(x<=109)
 {
  x = 110;
 }
 mothor(x);
 }
 ```
 
