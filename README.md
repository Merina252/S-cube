# S-cube
An approach for an smart home
char inputByte;
void setup() {
 Serial.begin(9600);
 pinMode(13,OUTPUT);
 pinMode(9, OUTPUT);

}

void loop() {
while(Serial.available()>0){
  inputByte= Serial.read();
  Serial.println(inputByte);
  if (inputByte=='1'){
  digitalWrite(13,HIGH);
  }
  else if(inputByte=='0'){
  digitalWrite(13, LOW);
  }
  
  if(inputByte=='2'){
    digitalWrite(9, HIGH);
  }
  else if (inputByte=='3'){
  digitalWrite(9, LOW);
  } 
  }
}
