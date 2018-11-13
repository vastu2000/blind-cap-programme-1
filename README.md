//const int trigPin=9;
//const int echoPin=10;
long duration;
int distance;
void setup() {
  pinMode(9,OUTPUT);
  pinMode(10,INPUT);
  pinMode(11,OUTPUT);
  Serial.begin(9600);

}

void loop() {
digitalWrite(9,LOW);
delayMicroseconds(2);
digitalWrite(9,HIGH);
delayMicroseconds(10);
digitalWrite(9,LOW);
duration = pulseIn(10,HIGH);
distance=duration*0.0332/2;
Serial.print("Distances");
Serial.println(distance);
if(distance<=300)
{
digitalWrite(11,HIGH);


}
else
{
digitalWrite(11,LOW);
} 
}
