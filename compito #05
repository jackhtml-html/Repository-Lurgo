#define GPIO_LED 4
#define GPIO_LED2 5
#define GPIO_LED3 6
#define pulsante 2

volatile byte led_stato = LOW;

void setup() {
  
Serial.begin(9600);
pinMode(pulsante, INPUT_PULLUP);
pinMode(GPIO_LED, OUTPUT);
pinMode(GPIO_LED2, OUTPUT);
pinMode(GPIO_LED3, OUTPUT);

attachInterrupt(digitalPinToInterrupt(pulsante),
ISR_lampeggia, CHANGE);
}
void loop() {
Serial.println(digitalRead(pulsante));
digitalWrite(GPIO_LED, led_stato);
digitalWrite(GPIO_LED2, led_stato);
digitalWrite(GPIO_LED3, led_stato);
}
void ISR_lampeggia() {
led_stato = !led_stato;
}
