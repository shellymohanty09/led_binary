void setup() {
// put your setup code here, to run once:

  Serial.begin(9600);
  pinMode(2,OUTPUT);
  pinMode(3,OUTPUT);
  pinMode(4,OUTPUT);
  pinMode(5,OUTPUT);
  pinMode(6,OUTPUT);
}

int x,i,res;
void loop() {
  // put your main code here, to run repeatedly:
  x = Serial.read();
  for(i=2;i<=6;i++)
  {
    res = x%2;
    x = x/2;

    if(res==1)
      digitalWrite(i,HIGH);
    else
      digitalWrite(i,LOW);    
  }
}
