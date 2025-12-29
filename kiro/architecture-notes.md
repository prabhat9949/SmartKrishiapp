# Architecture Notes – SmartKrishi

## System Overview
SmartKrishi follows a mobile-first architecture with cloud-backed services.

## High-Level Architecture

User (Farmer)
   ↓
Android App (Jetpack Compose)
   ↓
Firebase Backend
   ↓
AI Services (TFLite Model)
   ↓
Weather API

## Components

### Frontend (Android App)
- Built using Jetpack Compose
- Simple UI optimized for readability
- Offline-friendly screens where possible

### Backend
- Firebase Authentication for user login
- Firebase Firestore for storing data
- Firebase Storage for image uploads

### AI Layer
- TensorFlow Lite model
- Runs on-device for faster inference
- Returns disease name + confidence

### External APIs
- Weather API for real-time climate data

## Data Flow Example (Disease Detection)
1. User captures leaf image
2. Image resized to 224x224
3. Image passed to TFLite model
4. Model predicts disease
5. Result displayed to user

## Security & Privacy
- No unnecessary personal data stored
- Images processed securely
- Firebase rules applied for data access

## Kiro’s Role
Architecture diagrams and flow discussions were planned inside Kiro
before implementation, reducing integration issues.
