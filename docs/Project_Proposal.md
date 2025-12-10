# University of Virginia
## Department of Electrical and Computer Engineering

**Course:** ECE 4332 / ECE 6332 — AI Hardware Design and Implementation  
**Semester:** Fall 2025  


---

# AI Hardware Project Proposal

## 1. Project Title
**Team Name:** Circuit Intelligence  
**Students:** Yasir Babiker and Fares Elsherbiny  

**Project Title:** Smart LED Control Using Real-Time Hand Detection

---

## 2. Platform Selection
**Embedded System Platform – Arduino**

**Justification:**  
Arduino gives us a simple and reliable way to control LEDs while staying fast enough for real-time gesture response. It does not need heavy compute or cloud processing and fits the goal of keeping the system small, low-power, and responsive. It is affordable, well supported, and easy to integrate with sensors, which lets us focus more on model design and hardware interaction.

---

## 3. Problem Definition
We want a system that recognizes hand gestures and controls LEDs on the spot without relying on a full computer. Most gesture systems use GPUs or stronger CPUs which create delay and increase power use. Our goal is to push gesture detection onto smaller hardware while still reacting smoothly in real time.

This connects directly to AI hardware design since we work with limited compute and memory and still try to deliver quick inference, low latency, and reliable behavior on a lightweight embedded platform.

---

## 4. Technical Objectives
1. Reach **90% or higher gesture recognition accuracy**.  
2. Keep response time **under 0.5 seconds**.  
3. Stay **under 5 watts** during operation.  
4. Run **at least 2 hours** with stable performance.  
5. Support **three or more gestures**, such as on, off, and color change.

---

## 5. Methodology

### Hardware Setup
We use an Arduino board to drive LED outputs while a camera collects hand images. The camera captures the gesture, the model interprets it, and the Arduino responds by changing the LED state. Components include LEDs, resistors, wires, and a power source.

### Software Tools
We use Python, TensorFlow Lite, and OpenCV to train and prepare a lightweight gesture model. The Arduino IDE is used to deploy the LED control logic and integrate the gesture output.

### Model Design
A small CNN is trained on a custom gesture dataset. After training, the model is quantized to run efficiently on low-power hardware. The goal is to keep inference fast and accurate while fitting the constraints of the system.

### Performance Metrics
We evaluate:  
- Accuracy (goal ≥ 90%)  
- Reaction time (goal ≤ 0.5 seconds)  
- Power usage (goal ≤ 5W)  
- Stability over long operation  
- Support for multiple gestures  

### Validation Strategy
We test gestures in different lighting conditions and distances. We measure accuracy, latency, and power consumption. A continuous two-hour test checks reliability and consistency.

---

## 6. Expected Deliverables
- A working demo where LEDs respond to hand gestures in real time.  
- A GitHub repository with all code, model files, and wiring diagrams.  
- Documentation explaining setup and deployment instructions.  
- Presentation slides covering results and system design.  
- A final written report with testing, findings, and conclusions.

---

## 7. Team Responsibilities

| Name | Role | Responsibilities |
|------|------|------------------|
| **Fares Elsherbiny** | Co-Leader / Hardware & Software | Builds and tests the LED control logic, handles hardware integration, writes gesture interface code, and supports documentation. |
| **Yasir Babiker** | Co-Leader / Algorithm & Software | Trains and optimizes the gesture model, works on image processing and detection logic, tests both versions of the code, and helps refine the final system. |

**Collaboration Plan:**  
Both members write their own code versions, compare results, and merge the strongest features into one unified system. Work is done in parallel with regular check-ins for testing, debugging, and preparing deliverables.

---

## 8. Timeline and Milestones

| Week / Date | Milestone | Deliverable |
|--------------|------------|-------------|
| **Week 2 – Nov. 5** | Project Proposal | Proposal PDF and GitHub repository setup. |
| **Week 4 – Nov. 19** | Midterm Presentation | Slides and first working demo of gesture-controlled LEDs. |
| **Week 6 – Early Dec.** | Integration & Testing | Full prototype tested and both code versions merged. |
| **Final – Dec. 17** | Final Presentation & Report | Live demo, final report, and full GitHub archive. |

**Collaboration Plan:**  
Both members work in parallel for coding and testing. Weekly check-ins ensure the model, hardware logic, and integration stay on track. Final merging and testing are done together.

---

## 9. Resources Required
**Hardware:** Arduino board, camera or gesture sensor, LEDs, resistors, wires, and a power supply.  
**Dataset:** Custom gesture images collected through the camera under different lighting conditions.  
**Compute:** A laptop or desktop running Python, OpenCV, and TensorFlow for training and converting the model.

---

## 10. References
1. TensorFlow Lite Micro Documentation  
2. MediaPipe Hands Documentation  
3. Arduino IDE Official Documentation  
4. OpenCV Image Processing Tutorials  
5. Example TFLite gesture recognition repos on GitHub  

