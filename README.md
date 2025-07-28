# HealthcareAI - Exercise Tracking System

A comprehensive exercise tracking system using MediaPipe and OpenCV to count various exercises including push-ups, squats, bicep curls, and more. The main goal is to ensure proper form while exercising to achieve maximum effectiveness.

## Features
- Real-time pose detection and exercise counting
- Form validation and feedback
- Modular architecture supporting multiple exercise types
- Clean, organized codebase with proper separation of concerns

## Project Structure
```
src/
├── core/
│   └── pose_detector.py          # Unified pose detection module
├── exercises/
│   ├── __init__.py
│   ├── base_exercise.py          # Base class for all exercises
│   └── pushup_counter.py         # Push-up specific implementation
└── utils/
    ├── __init__.py
    └── camera_utils.py           # Camera setup utilities

tests/                            # Exercise test files
data/                            # Training/reference data
```

## Supported Exercises
- Push-ups
- Squats
- Bicep curls
- Jumping jacks
- Lunges
- Planks
- And more...

## Pose Detection Reference
The system uses MediaPipe's Pose module for body landmark detection. Refer to the image below for the different body joints detected:

![MediaPipe Pose Landmarks](https://google.github.io/mediapipe/images/mobile/pose_tracking_full_body_landmarks.png)

## Getting Started
1. Install required dependencies: `opencv-python`, `mediapipe`, `numpy`
2. Run any test file from the `tests/` directory to start exercise tracking
3. Follow on-screen feedback to maintain proper form

## Usage
The modular design allows easy extension for new exercise types by inheriting from the `BaseExercise` class and implementing exercise-specific logic.