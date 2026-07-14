#define YELLOWLED 7
#define REDLED 6
#define GREENLED 5
#define YELLOWLED2 8


void setup() {

  pinMode(YELLOWLED, OUTPUT);
  pinMode(REDLED, OUTPUT);
  pinMode(GREENLED, OUTPUT);
  pinMode(YELLOWLED2, OUTPUT);
}

void loop() {
  for (int i = 0; i < 3; i++) {
    allof_them();
  }
  for (int j = 0; j < 3; j++) {
    oneby_one();
  }
}
void allof_them() {
  digitalWrite(YELLOWLED, HIGH);
  digitalWrite(REDLED, HIGH);
  digitalWrite(GREENLED, HIGH);
  digitalWrite(YELLOWLED2, HIGH);
  delay(1000);
  digitalWrite(YELLOWLED, LOW);
  digitalWrite(REDLED, LOW);
  digitalWrite(GREENLED, LOW);
  digitalWrite(YELLOWLED2, LOW);
  delay(1000);
}

void oneby_one() {
  digitalWrite(YELLOWLED, HIGH);
  delay(1000);
  digitalWrite(YELLOWLED, LOW);
  digitalWrite(REDLED, HIGH);
  delay(1000);
  digitalWrite(REDLED, LOW);
  digitalWrite(GREENLED, HIGH);
  delay(1000);
  digitalWrite(GREENLED, LOW);
  digitalWrite(YELLOWLED2, HIGH);
  delay(1000);
  digitalWrite(YELLOWLED2, LOW);
}
