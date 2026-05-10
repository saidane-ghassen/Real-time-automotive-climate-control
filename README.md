# Autonomous Automotive Climate Control System – STM32F407

## Overview
This project is an embedded real-time prototype of an autonomous automotive climate control system based on the STM32F407 microcontroller.

The system reads temperature and humidity data, acquires a user speed command through an ADC potentiometer, and controls:
- BLDC motor 1 for ambient air ventilation
- BLDC motor 2 for air-conditioning gas flow
- DC radiator fan using an L298N driver
- LCD I2C display for system monitoring

## Key Features
- STM32F407-based embedded control unit
- FreeRTOS / CMSIS-RTOS2 task-based architecture
- ADC + DMA for potentiometer speed command
- PWM control for BLDC motors and DC radiator fan
- DHT22 temperature/humidity sensing
- LCD 16x2 I2C user interface
- ON/OFF operating mode
- Temperature-based radiator fan control

## Hardware Used
- STM32F407VGT6 board
- DHT22 temperature and humidity sensor
- 2x BLDC A2212 motors
- 2x ESC XXD 40A
- DC 12V radiator fan
- L298N motor driver
- LCD 16x2 with I2C module
- Potentiometer
- ON/OFF button
- LiPo / 12V power supply

## Software Architecture
The application is organized around three main RTOS tasks:
- Sensor task: reads button state and DHT22 data
- Motor task: computes and updates PWM commands
- Display task: updates the LCD interface

## System Architecture
![Block Diagram](images/block_diagram.png)

## Demo
[Prototype video](media/prototype_demo.mp4)

## Documentation
- [Project report](docs/RAPPORT_PS2_1.pdf)
- [Project presentation](docs/presentation.pdf)

## Future Improvements
- PID-based thermal regulation
- CAN communication for automotive integration
- Battery monitoring
- Dedicated PCB design
- Energy optimization

## Authors
- Alaa Chouchene
- Ghassen Saidane

## License
This project is shared for educational and portfolio purposes.
