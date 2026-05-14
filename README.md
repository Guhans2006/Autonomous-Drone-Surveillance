# DISHTI – Drone Intelligence Surveillance & Threat Identification System

## Overview

DISHTI is an AI-powered drone surveillance and threat analysis system designed to detect, track, and assess potential threats from aerial video footage.

The system processes drone surveillance data using computer vision and artificial intelligence to identify objects, assign threat levels, estimate target coordinates, and generate structured intelligence reports.

This project demonstrates the practical application of AI in autonomous surveillance, defense monitoring, and intelligence-based decision support systems.

---

## Features

### Intelligent Object Detection
- Detects objects from aerial footage using YOLOv8
- Supports multiple target categories
- High-speed frame-by-frame analysis

### Multi-Object Tracking
- Assigns unique tracking IDs
- Maintains object continuity across frames
- Tracks target movement dynamically

### Threat Assessment Engine
Analyzes detected objects using:
- Object type
- Detection confidence
- Position relevance
- Motion characteristics

Threat levels:
- High
- Medium
- Low

### Coordinate Estimation
- Estimates target location
- Simulates geo-referenced positioning
- Supports mission-based coordinate projection

### Automated Intelligence Report Generation
Generates professional reports containing:
- Mission summary
- Detection details
- Threat prioritization
- Analytical insights
- Operational recommendations

### Configurable Analysis Pipeline
Supports customization of:
- Detection thresholds
- Tracking parameters
- Threat scoring logic
- Output settings

---

## Working Principle

The system follows this processing pipeline:

Drone Video Input  
↓  
Frame Extraction  
↓  
Object Detection using YOLOv8  
↓  
Target Tracking  
↓  
Threat Scoring  
↓  
Coordinate Estimation  
↓  
Report Generation  

---

## Threat Scoring Logic

Threat score is calculated based on:

- Object classification priority
- Detection confidence
- Proximity to mission center
- Motion velocity

Threat classification:

| Score Range | Threat Level |
|------------|-------------|
| ≥ 0.70 | High |
| 0.45 – 0.69 | Medium |
| < 0.45 | Low |

---

## Project Structure

```bash
DISHTI/
│
├── main.py
├── demo.py
├── config/
├── modules/
│   ├── detector.py
│   ├── tracker.py
│   ├── threat_scorer.py
│   ├── report_generator.py
│   ├── logger.py
│   └── video_reader.py
│
├── models/
├── outputs/
└── tests/
