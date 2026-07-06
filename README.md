# SpraySense: An-Arduino-Based Sensor-Driven Automatic Alcohol Sprayer
**SpraySense** is developed in partial fulfillment of the final project for **DCIT 26A - Application Development and Emerging Technologies**. SpraySense is designed to provide a contactless and hygienic solution for hand sanitation by automatically dispensing alcohol when a user's hand is detected within a 10cm range. 

An ultrasonic sensor is used to detect the presence of a hand within a 10 cm range. Once a hand is detected, the system activates a servo motor that presses the dispenser mechanism to release alcohol. To prevent excessive dispensing, a cooldown period of two seconds is implemented between activations.

The system also incorporates a liquid level sensor to monitor the availability of alcohol. When alcohol is present, a green LED is illuminated to indicate normal operation. If the alcohol level is low or empty, a red LED is activated to alert users that refilling is required. An audible buzzer provides feedback during dispensing to confirm system activation. The system is enclosed inside a plywood case, securely installed and assembled to ensure protection and stability. The automatic sprayer maintains the provenance of hygiene by allowing users to sanitize their hands effortlessly.

To ensure safe and reliable operation, the program includes distance validation, sensor signal inversion handling, and timed control logic using the Arduino millis() function for cooldown management. Overall, the project demonstrates an effective integration of sensors, actuators, and feedback devices to create an automated, user-friendly sanitation system suitable for schools, offices, and public areas.

## MATERIALS AND COMPONENTS 
## Hardware Components:
- Arduino Uno
- Ultrasonic Sensor
- High-Torque 180 Degrees Servo Motor Metal Gear
- 4.8v 2000mAh NI-MH Battery
- Red LED
- Green LED
- Jumper Wires
- Breadboard
- 5V Battery
- Passive Buzzer

## Plywood Case (Enclosure/Box) 
- Plywood
- Screws
- Cordless Drill Driver (used to drill and mount the screws) 
- Crosscut Saw

## Circuit Design / Schematic

The project uses an Arduino Uno as the **main controller**, selected for its reliability and ease of use. An **ultrasonic sensor** is connected to the Arduino’s digital pins to accurately measure the distance between the system and the user’s hand. A high-torque servo motor is connected to a PWM pin to allow precise angular movement required to press the alcohol pump.

A **liquid level sensor** is used to detect the presence of alcohol in the container. This sensor provides digital input to the Arduino using inverted logic for accurate detection. A green LED and red LED are connected to digital output pins to indicate alcohol availability, while a buzzer provides audio feedback during dispensing.

All electronic components are properly wired using jumper wires and a breadboard, powered by a 5V battery or external power supply, and safely enclosed inside a plywood case to ensure protection and stability of the circuit.


## How It Works
The project functions as intended through the following process:

1. The **Arduino** continuously reads distance data from the **ultrasonic sensor**.
2. The system checks the **liquid level sensor** to confirm alcohol availability.
3. When a hand is detected within **10 cm** and alcohol is present, the Arduino activates the servo motor.
4. The servo rotates to a preset angle, pressing the alcohol pump and dispensing liquid.
5. The buzzer sounds during dispensing to confirm activation.
6. The servo returns to its original position after spraying.
7. A two-second cooldown period prevents immediate reactivation.
8. The green LED indicates normal operation, while the red LED signals the need for refilling.
