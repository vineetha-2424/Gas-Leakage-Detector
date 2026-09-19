int gas = A0;
int buzzer = 8;

void setup() {
  pinMode(buzzer, OUTPUT);
  Serial.begin(9600);
}

void loop() {
  int value = analogRead(gas);

  Serial.println(value);

  if (value > 400)
    digitalWrite(buzzer, HIGH);
  else
    digitalWrite(buzzer, LOW);

  delay(500);
}
# Gas-Leakage-Detector
