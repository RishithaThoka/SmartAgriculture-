# Smart Agriculture with IoT

## Overview
This repository contains a presentation (`Smart_Agriculture.pdf`) detailing an IoT-based smart agriculture system. The project demonstrates the use of sensors (DHT11 for temperature and humidity, soil moisture sensor, and LDR module for light intensity) connected to an Arduino to monitor crop field conditions and automate irrigation. The system aims to enhance agricultural efficiency by enabling remote monitoring and resource management.

## Contents
- `Smart_Agriculture.pdf`: The main presentation file (converted from PowerPoint), covering the project’s objectives, circuit connections, working prototype, code, applications, and references.
- `LICENSE`: Creative Commons Attribution 4.0 International License (CC BY 4.0) file.
- `.gitignore`: File to exclude unnecessary files (e.g., temporary PowerPoint files, system files).

## Purpose
This project was developed as part of a course (CSE 130.101-1) by Ristha Thokayyear to showcase how IoT can revolutionize agriculture. It is intended for students, educators, and agricultural enthusiasts interested in smart farming solutions.

## Project Details
### Objectives
- Measure humidity and temperature using the DHT11 sensor.
- Detect light intensity using the LDR module.
- Monitor soil moisture levels using a soil moisture sensor.
- Automate irrigation based on sensor data displayed on a 16x2 LCD.

### Components
- **DHT11 Sensor**: Measures temperature and humidity.
- **Soil Moisture Sensor**: Detects soil moisture levels to determine irrigation needs.
- **LDR Module**: Measures light intensity.
- **16x2 LCD with I2C Adapter**: Displays sensor data (e.g., moisture levels, motor status).
- **Arduino**: Microcontroller to process sensor data and control irrigation.
- **Jumper Wires**: Connect components to the Arduino.

### Circuit Connections
- **DHT11**: Positive to pin 13, negative to GND, signal to 5V via breadboard.
- **Soil Moisture Sensor**: AO to A0 pin, VCC to 5V, GND to Arduino GND.
- **LDR Module**: DO to A1 pin, VCC to 5V, GND to Arduino GND.
- **16x2 LCD with I2C**: GND to Arduino GND, VCC to 5V, SDA to A4, SCL to A5.

### Working Prototype
The system uses an Arduino to read data from the DHT11, soil moisture sensor, and LDR module. The soil moisture sensor triggers the irrigation motor (ON if moisture < 950, OFF otherwise). Sensor data (moisture level, humidity, temperature) is displayed on the 16x2 LCD. The code includes logic to categorize moisture levels as HIGH (<300), MID (300–950), or LOW (>950).

### Applications
- Crop water management.
- Increased crop productivity.
- Efficient resource utilization.
- Reduced production costs.
- Smart monitoring of crop conditions.
- Improved quality of agricultural products.

## How to Use
1. Download `Smart_Agriculture.pdf` from this repository.
2. Open the PDF using any PDF viewer (e.g., Adobe Acrobat, Google Chrome).
3. Review the slides for details on the IoT smart agriculture system, including objectives, circuit setup, and code.
4. To replicate the project:
   - Gather the listed components (Arduino, DHT11, soil moisture sensor, LDR module, 16x2 LCD with I2C).
   - Follow the circuit connections outlined in the PDF.
   - Upload the provided Arduino code (see slide 11) to your Arduino board.
   - Test the system in a controlled environment.

## Code
The Arduino code snippet in the presentation controls the irrigation motor and displays sensor data on the LCD. Key logic:
- Reads soil moisture from analog pin A0.
- Activates the motor (pin 2) if moisture > 950.
- Displays moisture status (HIGH, MID, LOW) and humidity/temperature on the LCD.
For the full code, refer to slide 11 in `Smart_Agriculture.pdf`.

## License
This project is licensed under the [Creative Commons Attribution 4.0 International License (CC BY 4.0)](LICENSE). You are free to share and adapt the material, provided you give appropriate credit to the author.

## References
- [IoT based Smart Agriculture Monitoring System](https://electronics-project-hub.com)
- [Wikipedia](https://www.wikipedia.org)
- [ThingSpeak](https://www.thingspeak.com)
- [YouTube](https://www.youtube.com)

## Contact
For questions or feedback, contact [Ristha Thokayyear] via [GitHub profile or email, if available]. Contributions or suggestions to improve the project are welcome!

## Notes
- The PDF contains minor typos (e.g., "SWANT" instead of "SMART," "ardiuno" instead of "Arduino"), which have been clarified in this README.
- The code on slide 11 appears incomplete (repetitive "Humidity" prints). For a working implementation, ensure proper variable names (e.g., `temp = DHT.temperature`) and complete the loop logic.
- If you plan to share the Arduino code separately, consider adding a `.ino` file to the repository.
