# Project-YL-69
TugasMengupload kode ke github

void setup() {
  Serial.begin(9600);
  pinMode(2, OUTPUT);
  pinMode(3, OUTPUT);
  pinMode(4, OUTPUT);
}

void loop() {
  int yellow = 2;
  int blue = 3;
  int red = 4;
  int sensorValue = analogRead(A1);

  digitalWrite(2, LOW);
  digitalWrite(3, LOW);
  digitalWrite(4, LOW);
  
  if (sensorValue >= 1000) (digitalWrite(yellow, HIGH));
  else if ((sensorValue <= 999) && (sensorValue >=901)) (digitalWrite(blue, HIGH));
  else if (sensorValue <= 900) (digitalWrite(red, HIGH));
  else ;

  if (sensorValue >= 1000) (Serial.print("SOIL IS TOO DRY!!!!!"));
  else if ((sensorValue <= 999) && (sensorValue >=901)) (Serial.print("SOIL IS PERFECT!!!!!"));
  else if (sensorValue <= 900) (Serial.print("SOIL IS TOO WET!!!!!"));
  else;
  
  Serial.print("Soil Humidity is: ");
  Serial.println(sensorValue);
  delay(500);



}
