加速*4
///C++
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
 ///
 按鈕加速:
 
