
# Sereno

A calm, minimalist air quality companion for your smart home.

Sereno connects to Home Assistant and visualizes indoor air quality with a design-first interface inspired by Dieter Rams. It prioritizes clarity over dashboards and uses AI to explain air quality trends in simple language.

---

## Core Ideas

Sereno is built around three principles:

- Calm interface
- Clear air quality insights
- Universal smart home compatibility

Instead of complex dashboards, Sereno answers one core question:

**Is the air in my home healthy right now?**

---

## Features

### Air Quality Dashboard

Displays:

- Air quality status
- PM2.5 primary metric
- Particle sensors
- Gas sensors
- Environment sensors

Example layout:

GOOD  
PM2.5 — 3.8 µg/m³

Particles  
PM1  
PM2.5  
PM10  

Gases  
CO2  
VOC  

Environment  
Temperature  
Humidity

---

### Home Assistant Integration

Sereno connects directly to a Home Assistant instance to access air quality sensors and purifier devices.

Supported sensors include:

- PM1
- PM2.5
- PM10
- CO2
- VOC
- Temperature
- Humidity

Sereno automatically discovers compatible sensors.

---

### AI Air Assistant

Users can ask:

- Why is air quality worse tonight?
- Should I open the windows?
- What caused this spike?

Sereno analyzes sensor data and provides simple explanations.

---

## Technology Stack

iOS App  
SwiftUI

Smart Home Integration  
Home Assistant REST API + WebSockets

AI Layer  
OpenAI API

Optional Backend  
Cloudflare Workers or Vercel Edge

---

## Project Structure

sereno/

    SerenoApp.swift
    Views/
        DashboardView.swift
        SensorSectionView.swift
        AirQualityStatusView.swift

    Models/
        Sensor.swift
        AirQualityStatus.swift

    Services/
        HomeAssistantClient.swift
        SensorDiscoveryService.swift
        AIExplanationService.swift

    ViewModels/
        DashboardViewModel.swift

---

## Development Setup

1. Install Xcode
2. Run Home Assistant locally
3. Generate a long-lived access token
4. Configure Sereno with your Home Assistant URL

Example:

http://homeassistant.local:8123

---

## Example Home Assistant API Request

GET /api/states

Authorization: Bearer TOKEN

---

## Roadmap

Phase 1 — MVP

- Home Assistant connection
- Sensor discovery
- Dashboard UI

Phase 2 — Intelligence

- AI explanations
- Historical graphs
- Alerts

Phase 3 — Smart Home Integration

- Automations
- Air purifier control
- Ventilation recommendations

---

## Name

Sereno

Meaning: calm, clear air.
