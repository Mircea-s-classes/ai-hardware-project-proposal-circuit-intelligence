# University of Virginia
## Department of Electrical and Computer Engineering

**Course:** ECE 4332 / ECE 6332 — AI Hardware Design and Implementation  
**Semester:** Fall 2025  
**Proposal Deadline:** November 5, 2025 — 11:59 PM  
**Submission:** Upload to Canvas (PDF) and to GitHub (`/docs` folder)

---

# AI Hardware Project Proposal Template

## 1. Project Title
Name of the Team:
Circuit Inteligence

List of students in the team:
Yasir Babiker and Fares Elsherbiny

Provide a clear and concise title for your project. 
Smart LED Control Using Real-Time Hand Detection
## 2. Platform Selection
Embedded System Platform – Arduino

Justification:

The Arduino platform is chosen because it provides an easy and efficient way to control LEDs and interface with sensors for hand gesture detection. Its low latency and real-time processing make it ideal for responsive hardware control. Arduino’s open-source libraries, affordability, and strong community support also make it perfect for building a simple yet effective hand gesture-controlled LED system.

## 3. Problem Definition
The main problem this project addresses is creating an efficient and responsive system that can recognize hand gestures and control LEDs in real time using low-power embedded hardware. Traditional gesture recognition systems often rely on high-performance computers or cloud processing, which increases latency and power consumption.

This project focuses on running gesture detection locally on an Arduino-based platform, minimizing delay between gesture input and LED response. The relevance to AI hardware lies in optimizing limited computational resources to achieve real-time interaction — improving efficiency, reducing latency, and demonstrating how AI concepts can be implemented on small, scalable embedded systems.
## 4. Technical Objectives
1. Gesture Detection Accuracy: Achieve at least 90% accuracy in recognizing hand gestures used to control the LEDs.

2. Response Time: Ensure the system responds to a recognized gesture within 0.5 seconds of detection.

3. Power Efficiency: Maintain total system power consumption below 5 watts during operation.

4. System Reliability: Operate continuously for at least 2 hours without errors or incorrect LED responses.

5. Scalability: Support at least 3 distinct hand gestures (e.g., turn on, turn off, change color) with potential to expand to more gestures in future versions.
## 5. Methodology
Hardware Setup:
The system uses an Arduino board to control LEDs and a camera or gesture sensor to detect hand movements. The Arduino handles real-time LED control, while the sensor captures and interprets gestures. Components include LEDs, resistors, power supply, and connecting wires.

Software Tools:
The project uses the Arduino IDE for programming, Python with TensorFlow Lite for training and optimizing a lightweight gesture recognition model, and OpenCV for image preprocessing.

Model Design:
A small convolutional neural network (CNN) is trained to recognize a few hand gestures (e.g., on, off, change color). The model is quantized and deployed on the hardware for fast, low-power inference.

Performance Metrics:
Key targets include ≥90% accuracy, ≤0.5 s response time, ≤5 W power use, and support for at least 3 gestures.

Validation Strategy:
Testing will measure accuracy, latency, and power consumption under different lighting and user conditions. The system will run for at least 2 hours continuously to verify reliability and real-time performance.
## 6. Expected Deliverables
Working Demo: A functional hand gesture-controlled LED system running on the Arduino platform.

GitHub Repository: Contains all source code, trained model files, wiring diagrams, and setup instructions.

Documentation: Step-by-step guide explaining hardware connections, software setup, and model deployment.

Presentation Slides: Summarize project goals, design approach, performance results, and future improvements.

Final Report: Detailed written report covering problem statement, methodology, testing results, and conclusions.

## 7. Team Responsibilities  

| Name | Role | Responsibilities |
|------|------|------------------|
| **Fares Elsherbiny** | **Co-Leader / Hardware & Software Engineer** | Collaborates on code development for hand detection and LED control, integrates the system with Arduino hardware, and assists with documentation. |
| **Yasir Babiker** | **Co-Leader / Hardware & Software Engineer** | Works jointly on coding and algorithm optimization, compares and refines both versions of the code with Fares, and helps test and troubleshoot the Arduino setup. |

**Collaboration Plan:**  
Both team members share equal leadership and responsibility. They will each write and test their own versions of the code for gesture detection and LED control. After comparing results, they will merge the best-performing features and test the final integrated system together on the Arduino hardware. Both will jointly handle debugging, performance evaluation, and final documentation.

---

## 8. Timeline and Milestones  

| Week / Date | Milestone | Deliverable |
|--------------|------------|-------------|
| **Week 2 – Nov. 5, 2025** | **Project Proposal** | PDF submission outlining problem, objectives, and design plan; GitHub repository initialized. |
| **Week 4 – Nov. 19, 2025** | **Midterm Presentation** | Presentation slides and preliminary results showing gesture detection controlling LEDs. |
| **Week 6 – Early Dec. 2025** | **Integration & Testing** | Fully working prototype tested on Arduino with both versions of code compared and merged. |
| **Final – Dec. 17, 2025** | **Final Presentation & Report** | Final report, live demo, and GitHub archive of completed system. |

**Collaboration Plan:**  
Fares and Yasir will work in parallel during each phase. Both will code, test, and evaluate independently, then combine their work for integration and testing. They will meet regularly to review progress, refine system performance, and prepare joint deliverables for each milestone.

## 9. Resources Required
Hardware Components: Arduino board, camera or gesture sensor, LEDs, resistors, jumper wires, and power supply.

Dataset: A custom hand gesture image dataset collected using the camera module, including multiple gestures under varied lighting conditions.

Compute Access: A standard laptop or desktop with Python and TensorFlow installed for training and converting the model to TensorFlow Lite format.
## 10. References
Include relevant papers, repositories, and documentation.
