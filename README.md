# Smart-Street-Light-System
A smart street light system is an IoT-based technology that uses sensors, wireless communication, and cloud computing to control and manage street lighting. It adjusts the intensity of lights based on various factors, detects faults, and notifies maintenance teams for repairs, resulting in energy savings and improved safety.


 const int ldrPin = A0;      // Connect the LDR to analog input A0
 
const int pirPin = 2;       // Connect the PIR sensor to digital input 2

const int ledPin = 13;      // Connect the LED to digital output 13

int ldrValue = 0;           // Variable to store the LDR value

int pirValue = 0;           // Variable to store the PIR value

void setup() {

pinMode(ledPin, OUTPUT); // Set the LED pin as an output

pinMode(pirPin, INPUT);   // Set the PIR pin as an input

Serial.begin(9600);       // Optional: Open a serial connection for debugging

}

void loop() {

ldrValue = analogRead(ldrPin);   // Read the analog value from the LDR

Serial.print("LDR: ");           // Optional: Print the LDR value to the serial monitor

Serial.print(ldrValue);

pirValue = digitalRead(pirPin);  // Read the digital value from the PIR sensor

Serial.print(" PIR: ");          // Optional: Print the PIR value to the serial monitor

Serial.println(pirValue);

if ((ldrValue < 400) &&  pirValue == LOW) {  // If it's dark and motion is detected,

digitalWrite(ledPin, HIGH);               // turn on the LED

}

if ( pirValue== HIGH)

{

digitalWrite(ledPin, LOW);             // turn on the LED

}

delay(1000);                               // Optional: Wait a short time before reading again

}









![WhatsApp Image 2023-04-02 at 15 46 57](https://github.com/Mahaveermandloi/Smart-Street-Light-System/assets/132800572/cdd9479c-336f-434c-a76d-ab7886a5e2ba)

![8](https://github.com/Mahaveermandloi/Smart-Street-Light-System/assets/132800572/6b0044da-e40d-45f5-b327-97804f06d32a)
![9](https://github.com/Mahaveermandloi/Smart-Street-Light-System/assets/132800572/9846365d-7115-4e3f-8aab-83bc089e72e9)
![10](https://github.com/Mahaveermandloi/Smart-Street-Light-System/assets/132800572/cc021bf1-04d1-4e1c-a6df-68785499286d)
