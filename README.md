# Night Lamp with Motion Detector and Timer

Developed as part of the EC1091E Practical Electronics course at the National Institute of Technology, Calicut (Monsoon 2024).

## Project Objective
The goal of this project was to design an energy-efficient lighting solution that automatically activates upon detecting human motion and remains on for a user-defined duration before turning off.

## Images
![prototype](https://github.com/user-attachments/assets/97b34e5d-0cc3-4bd6-ade5-dc7621be742b)

## How It Works
The system is divided into three functional stages:
1. Motion Sensing:
   An HC-SR501 PIR sensor detects infrared radiation from moving objects. When motion is detected, it biases a 2N3904 transistor to trigger the timing circuit.
2. Timing (Monostable Multivibrator):
   An NE555 Timer IC is configured in monostable mode. It produces a high output pulse at Pin 3 for a specific duration defined by the RC network.
3. Relay Driving:
   The output pulse switches a BC547 transistor, which energizes a 12V SPDT relay to turn on the lamp (LED).

### Timing Calculation
The duration (t) the lamp remains ON is determined by the formula:
t=ln(3)×R×C
Where R is the resistance of the 1MΩ potentiometer and C is the 470µF capacitor.

## Circuit Diagram
<img width="1362" height="720" alt="circuit_diagram" src="https://github.com/user-attachments/assets/5b25bf61-477b-44bd-807e-8c34c0401256" />

## Components Used
- IC	555 Timer
- PIR Sensor	HC-SR501
- Relay	12V SPDT
- Transistors	BC547 & 2N3904
- Capacitors	470µF (Elec), 0.01µF (Ceramic)
- Resistors	10KΩ, 1KΩ (x2)
- 1MΩ Potentiometer
- LED	5mm Yellow

## Key Features
- Energy Efficient: Operates only when movement is sensed, reducing electricity costs.
- Adjustable Timer: The duration can be modified by tuning the onboard potentiometer.
- Safety & Security: Ideal for hands-free illumination in dark hallways or as a deterrent for intruders.

##  Limitations

- False Triggers: May be activated by pets or environmental factors like wind.
- Detection Range: Limited by the PIR sensor's specific viewing angle.

## Contributors

Rashid Rahman TP (B241108EC) 
Richu Mathew Shaji (B241119EC) 
Rishal Mohammad (B240090EC) 

For more detailed technical analysis, please refer to the MotionDetectionNightLamp_Report.pdf uploaded in this repository.
