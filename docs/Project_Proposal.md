# Circuit Intelligence
## Smart LED Control Using Real Time Hand Detection

University of Virginia  
Department of Electrical and Computer Engineering  
Course: ECE 4332 / ECE 6332 AI Hardware Design and Implementation  
Semester: Fall 2025  

Team Members  
Fares Elsherbiny  
Yasir Babiker  

## Project Summary
This project builds a fast and reliable system where simple hand gestures control LED behavior in real time. The goal is to combine lightweight AI based gesture recognition with embedded hardware control to achieve low latency interaction while keeping cost and power low. The system detects a hand using a camera, converts the gesture into a compact representation, sends it to an Arduino through serial communication, and the Arduino updates LEDs instantly.

## Motivation
Hand gestures are natural and intuitive, but many gesture systems rely on heavy computers or cloud processing, which increases cost, power use, and latency. Our goal is to show that smart interaction does not require big hardware. This matters for real time control, IoT devices, and small robots where every millisecond and every watt counts.

## Platform Selection
Embedded System Platform: Arduino  

Justification  
Arduino provides fast and reliable GPIO control for LEDs with low power usage and low latency. It has a straightforward development workflow and strong library support, which lets us focus on the AI hardware system design and integration.

## Team Responsibilities
Fares Elsherbiny  
Co Leader Hardware and Software  
Responsibilities include hardware integration, LED control logic, serial communication testing, and documentation.

Yasir Babiker  
Co Leader Algorithm and Software  
Responsibilities include gesture detection logic, model or rule based design, image processing, testing, and helping refine the final system.

Collaboration Plan  
Both members work across the full workflow including coding, testing, model design, hardware setup, debugging, and documentation. We compare approaches and merge the best features into one unified system.

## System Architecture
Pipeline  
Gesture Input from laptop camera  
Preprocessing and gesture inference on laptop  
Serial communication from laptop to Arduino over USB  
Arduino hardware control  
LED output actions  

Current Midterm Status  
Gesture Input: Laptop camera  
Processing and inference: Laptop  
Communication: Laptop to Arduino  
Hardware control: Arduino  
Output: LED actions  
Continuous loop and reliability testing

## Technical Objectives
Gesture Accuracy at least 90 percent  
Response Time at most 0.5 seconds  
Power Consumption at most 5 watts  
Reliability at least 2 hours continuous run  
Support at least 3 gestures such as on, off, and change

## Results
Midterm results in controlled lighting and short range testing  
Gesture accuracy about 90 percent  
Response time under 0.5 seconds and visually instant  
Stable continuous loop without freezing during testing  
Multiple gestures supported through finger state patterns

## Limitations
Gesture detection currently runs on the laptop rather than fully on device  
Performance can depend on lighting conditions  
Gesture set is limited at the current stage

## Future Work
Move inference fully on device using a microcontroller friendly model  
Quantize and optimize the model to reduce latency and memory  
Expand gesture set and map gestures to richer outputs such as colors, brightness, or patterns  
Improve robustness across lighting, distance, and different users  
Measure power more formally and optimize system level efficiency

## HowTo Run the System

### Requirements
Hardware  
Arduino board  
LEDs and resistors  
Breadboard and wires  
USB cable  

Software  
Arduino IDE  
Python 3  
OpenCV  
MediaPipe  
PySerial  

### Wiring
Connect LEDs to Arduino digital pins 8 through 12 with the correct series resistors. Connect grounds properly. Use the same pin mapping used in the Arduino sketch.

### Step by Step
1. Build the LED circuit on a breadboard and connect LEDs to Arduino pins 8 to 12.
2. Upload the Arduino LED control sketch to the board using the Arduino IDE.
3. Install Python dependencies and confirm the correct serial port for the Arduino.
4. Run the Python camera and gesture script on the laptop.
5. Show hand gestures in front of the camera.
6. The script sends finger states to the Arduino and the Arduino updates LEDs in real time.

### What You Should See
The laptop detects the hand and creates a five value finger state list. The Arduino receives those values and turns LEDs on or off based on the gesture input.

## Repository Structure
Recommend folders  
src for Python code  
arduino for Arduino sketch  
models for trained model files if used  
docs for images, wiring diagrams, and presentation material

## References
MediaPipe Hands Documentation  
Arduino IDE Documentation  
OpenCV Tutorials  
TensorFlow Lite resources and example gesture recognition repos
