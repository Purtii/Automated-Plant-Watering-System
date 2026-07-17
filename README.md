**# Automated Plant Watering System**

## Project Overview

The Automated Plant Watering System is an IoT-based embedded system designed to monitor soil moisture and control plant irrigation remotely.

The project combines a NodeMCU ESP8266 microcontroller, a resistive soil moisture sensor, a 16x2 I2C LCD, a relay module, a mini water pump and the Blynk IoT platform.

Its purpose is to reduce incorrect watering caused by lack of time, frequent travel or manual estimation. The system provides real-time information about the condition of the soil and allows the user to control the irrigation pump from a mobile device.

## Project Objectives

The main objectives of the project were:

- To measure soil moisture in real time
- To convert raw sensor values into understandable percentages
- To display the moisture level locally on an LCD
- To send sensor data to a cloud-based mobile dashboard
- To control a water pump remotely
- To create a low-cost and energy-efficient prototype
- To maintain stable operation without blocking the microcontroller

## System Architecture

The system is divided into three main levels:

### 1. Data Acquisition

A resistive soil moisture sensor is inserted into the soil and produces an analog value based on electrical conductivity.

Dry soil produces a higher analog value, while wet soil produces a lower value.

### 2. Processing and Communication

The NodeMCU ESP8266 reads the analog sensor value and converts it into a percentage between 0% and 100%.

The ESP8266 also provides Wi-Fi connectivity, allowing the device to communicate with the Blynk Cloud platform.

### 3. Display and Execution

The calculated moisture level is displayed on a 16x2 LCD using the I2C communication protocol.

A relay module controls the water pump and provides electrical separation between the low-power microcontroller circuit and the pump’s external power circuit.

The pump can be activated or deactivated remotely through the Blynk mobile application.

## Hardware Components

- NodeMCU ESP8266
- Resistive soil moisture sensor
- 16x2 LCD with PCF8574 I2C adapter
- 5V relay module with optocoupler
- Mini water pump
- External power supply
- Water container and tubing
- Breadboard and jumper wires

## Software Implementation

The software was developed in C++ using the Arduino IDE.

The program uses asynchronous execution through `BlynkTimer`, allowing the sensor to be read periodically without blocking the main program.

The main software responsibilities are:

- Reading the analog soil moisture value
- Mapping the raw value to a moisture percentage
- Updating the LCD display
- Sending data to Blynk through virtual pin `V0`
- Receiving pump commands through virtual pin `V1`
- Controlling the relay using active-low logic
- Keeping the pump turned off during system startup

The project uses the following technologies and protocols:

- C++
- Arduino framework
- ESP8266 Wi-Fi communication
- Blynk IoT Cloud
- I2C communication
- Analog-to-digital conversion
- Relay-based actuator control


## Future Improvements

Possible future developments include:

- Automatic watering based on a moisture threshold
- Maximum pump runtime for flood prevention
- Temperature and air-humidity monitoring
- Water tank level detection
- Mobile notifications for dry soil
- Historical moisture charts
- Support for multiple plants
- Use of a capacitive moisture sensor
- Offline operation without internet access
- Battery or solar-powered operation

## Conclusion

The project demonstrates how IoT technology can be used to improve plant care and water-resource management.

By combining sensor data acquisition, embedded processing, Wi-Fi communication, cloud monitoring and actuator control, the system provides a practical example of a complete IoT application.

The prototype also helped develop knowledge in embedded programming, analog sensor processing, I2C communication, cloud integration, asynchronous software execution and hardware control.

## Project Team

- **Purtan Rareș Ionuț** — Team Leader
- Mîțu Daria-Andreea
- Livitchi Vlad
- Pungă Tudor-Cristian
- Popa Mihnea-Alexandru
- Dragoș Patrik

**Coordinator:** Petru Papazian

## Academic Context

This project was developed as a Year III Development Project at the Politehnica University of Timișoara.
