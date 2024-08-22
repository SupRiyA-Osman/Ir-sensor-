int irpin = 7;        // Define the pin connected to the IR sensor
int irvalue;          // Variable to store the value read from the IR sensor

void setup() {
  pinMode(irpin, INPUT);  // Set the IR pin as input
  Serial.begin(9600);     // Initialize serial communication at 9600 bps
}

void loop() {
    
  irvalue = digitalRead(irpin);   // Read the value from the IR sensor
  Serial.print("irvalue=");       // Print label for the IR value
  Serial.print(irvalue);        // Print the actual IR value and move to a new line
  delay(500);                     // Small delay to make the output readable
}
