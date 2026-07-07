// Define Traffic Light Pins for Main Road
const int mainGreen  = 2;
const int mainYellow = 3;
const int mainRed    = 4;

// Define Traffic Light Pins for Side Road (Smart Sensor Road)
const int sideGreen  = 5;
const int sideYellow = 6;
const int sideRed    = 7;

// Define Ultrasonic Sensor Pins (HC-SR04)
const int trigPin = 8;
const int echoPin = 9;

// Distance threshold (in centimeters) to detect a waiting car
const int carDistanceThreshold = 20; 

void setup() {
  // Set Traffic Light pins as outputs
  pinMode(mainGreen, OUTPUT);
  pinMode(mainYellow, OUTPUT);
  pinMode(mainRed, OUTPUT);
  pinMode(sideGreen, OUTPUT);
  pinMode(sideYellow, OUTPUT);
  pinMode(sideRed, OUTPUT);
  
  // Set Ultrasonic Sensor pins
  pinMode(trigPin, OUTPUT);
  pinMode(echoPin, INPUT);

  // Initial State: Main road is Green
  
