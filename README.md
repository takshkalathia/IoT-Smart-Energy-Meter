# IoT-Based Smart Energy Meter

An IoT-based smart energy monitoring system using **ESP32, ACS712, ZMPT101B, EmonLib, and Blynk IoT 2.0** to measure electrical parameters and visualize energy consumption remotely.

## Overview

Electricity consumption monitoring is an important part of smart homes and energy management. Traditional energy measurement methods provide limited accessibility for users who want to monitor consumption remotely.

This project implements a modular **IoT-based Smart Energy Meter** using an ESP32 development board. The system measures voltage and current from an electrical load, calculates electrical power and accumulated energy consumption, and sends the measured values to the **Blynk IoT platform** through Wi-Fi.

The measured parameters can be viewed in real time through a smartphone or web-based Blynk dashboard.

## Objectives

- Develop an IoT-based system for electrical energy monitoring.
- Measure **RMS voltage** and **RMS current** from an electrical load.
- Calculate electrical power and accumulated energy consumption.
- Transmit measurement data wirelessly using Wi-Fi.
- Visualize real-time measurements using the Blynk IoT platform.
- Demonstrate the application of IoT in smart-home energy monitoring.

## System Architecture

The system consists of voltage and current sensing circuits connected to an ESP32 development board. The ESP32 processes the sensor measurements and communicates with the Blynk IoT platform over Wi-Fi.

```text
        AC Mains
           │
           ▼
    ┌───────────────┐
    │ Electrical    │
    │     Load      │
    └───────┬───────┘
            │
      ┌─────┴─────┐
      │           │
      ▼           ▼
 ZMPT101B      ACS712
 Voltage       Current
  Sensor        Sensor
      │           │
      └─────┬─────┘
            ▼
     ┌─────────────┐
     │    ESP32    │
     │ Development │
     │    Board    │
     └──────┬──────┘
            │
          Wi-Fi
            │
            ▼
     ┌─────────────┐
     │ Blynk IoT   │
     │  Platform   │
     └──────┬──────┘
            │
            ▼
    Smartphone / Web
       Dashboard
