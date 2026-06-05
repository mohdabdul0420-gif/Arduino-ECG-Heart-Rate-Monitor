# Arduino ECG Heart Rate Monitor Project Report

## 1. Introduction

Electrocardiography (ECG) is a technique used to measure the electrical activity of the heart. Monitoring heart signals helps in identifying various cardiac conditions and understanding heart performance. This project implements a low-cost ECG monitoring system using an Arduino microcontroller and an ECG sensor module.

## 2. Objective

* To acquire ECG signals from the human body.
* To monitor heart activity in real time.
* To visualize ECG waveforms using a computer.
* To develop a portable and affordable healthcare monitoring system.

## 3. Hardware Requirements

* Arduino Uno
* AD8232 ECG Sensor Module
* ECG Electrodes
* Jumper Wires
* USB Cable
* Personal Computer

## 4. Software Requirements

* Arduino IDE
* Serial Plotter
* Windows/Linux Operating System

## 5. System Architecture

The ECG electrodes collect electrical signals from the body and send them to the AD8232 ECG sensor. The sensor amplifies and filters the signals before forwarding them to the Arduino Uno. The Arduino reads the analog data and transmits it through serial communication to a computer where the ECG waveform is displayed.

## 6. Working Methodology

1. Electrodes are attached to the user's body.
2. The ECG sensor captures heart signals.
3. Analog signals are processed by the sensor module.
4. Arduino reads the ECG data through an analog input pin.
5. The data is transmitted to the computer through USB serial communication.
6. The ECG waveform is visualized using the Serial Plotter.

## 7. Circuit Connections

| AD8232 Pin | Arduino Uno |
| ---------- | ----------- |
| GND        | GND         |
| 3.3V       | 3.3V        |
| OUTPUT     | A0          |
| LO+        | D10         |
| LO-        | D11         |

## 8. Sample Arduino Code

```cpp
const int ECG_PIN = A0;

void setup() {
  Serial.begin(9600);
}

void loop() {
  int ecgValue = analogRead(ECG_PIN);
  Serial.println(ecgValue);
  delay(5);
}
```

## 9. Results

The developed system successfully captures and displays ECG signals in real time. The waveform generated on the Serial Plotter corresponds to the electrical activity of the heart and can be used for basic monitoring and analysis.

## 10. Advantages

* Low cost
* Portable design
* Easy implementation
* Real-time monitoring
* Educational value

## 11. Limitations

* Not intended for clinical diagnosis
* Susceptible to motion artifacts
* Limited signal processing capabilities

## 12. Applications

* Health monitoring
* Biomedical education
* Research and development
* Embedded systems projects
* IoT healthcare solutions

## 13. Future Scope

* Bluetooth connectivity
* Mobile application support
* Cloud data storage
* AI-based heart condition analysis
* Remote patient monitoring

## 14. Conclusion

The Arduino ECG Heart Rate Monitor demonstrates the effective integration of biomedical sensing technology with embedded systems. The project provides a simple and economical solution for monitoring heart activity and serves as an excellent platform for learning healthcare-oriented embedded system design.
