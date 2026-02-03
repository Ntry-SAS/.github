# Ntry: Smart Dorm Access System

EGR 302: Junior Design Project | Spring 2026 | California Baptist University

Ntry is a non-invasive, smart retrofit solution that transforms a resident's smartphone into a secure dorm key. By bridging legacy RFID infrastructure with modern mobile technology, Ntry eliminates the operational strain of lost keys and physical lockouts.

## The Problem
Physical keys and RFID cards are easily lost, damaged, or forgotten. This causes:

- Operational Strain: Admins must manually verify identities and issue temporary passes.
- Security Gaps: Lost credentials remain a threat until a card is manually deactivated or a lock is re-keyed.
- Resident Friction: Lockouts disrupt daily student life and create dependency on staff availability.

## The Solution
Our system utilizes a "mechanical air-gap" approach. A Raspberry Pi-controlled servo motor physically lowers a cloned ID card to the existing reader, allowing for digital control without modifying university hardware or voiding warranties.

## Key Features
- Walk-Up Entry: Bluetooth Low Energy (BLE) proximity detection for hands-free unlocking.
- Guest Passes: Secure, time-bound QR codes for trusted visitors.
- Admin Dashboard: Real-time access logging and remote emergency override.
- 2FA Security: Biometric/PIN authentication required for manual unlock commands.

## Tech Stack
- Frontend: Flutter (Dart) — Cross-platform iOS/Android mobile application.
- IoT Controller: Python (Flask/OpenCV) — Raspberry Pi edge device for hardware control and QR processing.
- Cloud Infrastructure: AWS (Cognito for Auth, DynamoDB for NoSQL data storage).
- Hardware: Raspberry Pi 4, Servo Motors, and a Flipper Zero (used for initial credential cloning).

## The Team
- Eli Manning - Team Leader
- Elliott Willer - Team Member
- Josue Hernandez - Team Member
- Johnathan Fierro - Team Member
- Instructor: Dr. Dan Grissom

## Repository Structure
- ntry-mobile - The Flutter application source code.
- ntry-edge - Python logic for the Raspberry Pi and servo control.
- ntry-backend - AWS configuration and cloud functions.
