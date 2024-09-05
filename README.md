# Traffic Light Simulator

## Description

This project simulates a traffic light system using multiple LEDs connected to an Arduino. The simulation cycles through various traffic light patterns, turning different combinations of LEDs on and off to represent different traffic light states.

## Components

- Arduino (e.g., Arduino Uno)
- 12 LEDs
- Resistors (220Ω or similar)
- Jumper wires
- Breadboard

## Pin Configuration

| LED Name | Pin Number |
| -------- | ---------- |
| H1       | 2          |
| K1       | 3          |
| M1       | 4          |
| H2       | 5          |
| K2       | 6          |
| M2       | 7          |
| H3       | 8          |
| K3       | 9          |
| M3       | 10         |
| H4       | 11         |
| K4       | 12         |
| M4       | 13         |

## Code

```cpp
// Code Traffic_Light_Simulator
#define H1 2
#define K1 3
#define M1 4
#define H2 5
#define K2 6
#define M2 7
#define H3 8
#define K3 9
#define M3 10
#define H4 11
#define K4 12
#define M4 13

void setup(){
   pinMode(2,OUTPUT);
   pinMode(3,OUTPUT);
   pinMode(4,OUTPUT);
   pinMode(5,OUTPUT);
   pinMode(6,OUTPUT);
   pinMode(7,OUTPUT);
   pinMode(8,OUTPUT);
   pinMode(9,OUTPUT);
   pinMode(10,OUTPUT);
   pinMode(11,OUTPUT);
   pinMode(12,OUTPUT);
   pinMode(13,OUTPUT);
}

void loop(){
   // Lamp H1, M2, M3, M4 ON
   digitalWrite(H1,HIGH);
   digitalWrite(M2,HIGH);
   digitalWrite(M3,HIGH);
   digitalWrite(M4,HIGH);
   delay(3000);

   // Lamp K1, M2, M3, M4 ON
   digitalWrite(H1,LOW);
   digitalWrite(K1,HIGH);
   delay(2000);

   // Lamp M1, H2, M3, M4 ON
   digitalWrite(K1,LOW);
   digitalWrite(M2,LOW);
   digitalWrite(M1,HIGH);
   digitalWrite(H2,HIGH);
   delay(3000);

   // Lamp M1, K2, M3, M4 ON
   digitalWrite(H2,LOW);
   digitalWrite(K2,HIGH);
   delay(2000);

   // Lamp M1, M2, H3, M4 ON
   digitalWrite(K2,LOW);
   digitalWrite(M2,HIGH);
   digitalWrite(M3,LOW);
   digitalWrite(H3,HIGH);
   delay(3000);

   // Lamp M1, M2, K3, M4 ON
   digitalWrite(H3,LOW);
   digitalWrite(K3,HIGH);
   delay(2000);

   // Lamp M1, M2, M3, H4 ON
   digitalWrite(K3,LOW);
   digitalWrite(M3,HIGH);
   digitalWrite(M4,LOW);
   digitalWrite(H4,HIGH);
   delay(3000);

   // Lamp M1, M2, M3, K4 ON
   digitalWrite(H4,LOW);
   digitalWrite(K4,HIGH);
   delay(2000);

   digitalWrite(K4,LOW);
   digitalWrite(M1,LOW);
}
```

## How It Works

1. Initialization: The setup() function sets all the specified pins as output.
2. Traffic Light Simulation: The loop() function cycles through various traffic light patterns:
   - Turns on specific LEDs for a set duration.
   - Each state represents a different traffic light configuration.
   - The sequence repeats indefinitely.

## Usage

1. Connect the LEDs to the specified pins on the Arduino.
2. Upload the code to your Arduino board.
3. Observe the simulated traffic light patterns as the LEDs turn on and off in the sequence defined.

## Notes

- Ensure that you use appropriate resistors for the LEDs to prevent damage.
- Modify the delay() durations to adjust the timing of the traffic light simulation.
