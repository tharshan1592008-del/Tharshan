// Define the pins for the water level sensor probes (inputs)
const int lowLevelPin = 2;    // Probe at the bottom/low level
const int medLevelPin = 3;    // Probe at the middle level
const int highLevelPin = 4;   // Probe at the top/high level

// Define the pins for the indicator LEDs (outputs)
const int lowLED = 8;         // Red LED
const int medLED = 9;         // Yellow LED
const int highLED = 10;       // Green LED
const int buzzer = 11;        // Optional buzzer for full tank alert

void setup() {
  // Set sensor pins as inputs with internal pull-up resistors
  // This keeps the pins HIGH until they touch water (which connects them to GND)
  pinMode(lowLevelPin, INPUT_PULLUP);
  pinMode(medLevelPin, INPUT_PULLUP);
  pinMode(highLevelPin, INPUT_PULLUP);

  // Set LED and buzzer pins as outputs
  pinMode(lowLED, OUTPUT);
  pinMode(medLED, OUTPUT);
  pinMode(highLED, OUTPUT);
  pinMode(buzzer, OUTPUT);
}

void loop() {
