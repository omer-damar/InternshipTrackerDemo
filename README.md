# Internship Tracker

> An iOS application for organizing internship applications, browsing remote jobs and viewing company locations on a map.

![Swift](https://img.shields.io/badge/Swift-5.9-orange?logo=swift)
![iOS](https://img.shields.io/badge/iOS-17%2B-blue?logo=apple)
![SwiftUI](https://img.shields.io/badge/UI-SwiftUI-purple)
![SwiftData](https://img.shields.io/badge/Storage-SwiftData-green)

## Screenshots

<p align="center">
  <img width="250" alt="Internship Tracker screen 1" src="https://github.com/user-attachments/assets/85ecb31e-17c3-4024-a0c0-36f4f48a79e2" />
  <img width="250" alt="Internship Tracker screen 2" src="https://github.com/user-attachments/assets/f0ca28b3-fb04-4821-8000-ec81543868f4" />
  <img width="250" alt="Internship Tracker screen 3" src="https://github.com/user-attachments/assets/40846d68-b0b8-493f-8d88-75b221dc37c2" />
</p>

<p align="center">
  <img width="250" alt="Internship Tracker screen 4" src="https://github.com/user-attachments/assets/484a9cb3-8771-40e4-bf12-d6e2ec5d42a8" />
  <img width="250" alt="Internship Tracker screen 5" src="https://github.com/user-attachments/assets/1476f5b9-6158-4177-b1bd-400c095f648c" />
  <img width="250" alt="Internship Tracker screen 6" src="https://github.com/user-attachments/assets/9200152f-8f15-47fd-92d7-c50b0ba49b77" />
</p>

## Features

| Feature | Description |
|---|---|
| Application tracking | Organize applications by pending, interview, offer and rejected states |
| Remote job board | Fetch current listings from the Remotive public API |
| Notifications | Trigger local notifications when newly observed jobs are detected |
| Company map | Display company locations and open directions with Apple Maps |
| Local persistence | Store application data on-device with SwiftData |
| Analytics | Review application progress and status distribution |

## Tech Stack

- Swift and SwiftUI
- SwiftData
- URLSession
- MapKit and Core Location
- UserNotifications
- XCTest

## Getting Started

### Prerequisites

- Xcode 15+
- iOS 17+ simulator or device
- macOS Ventura or newer

### Installation

```bash
git clone https://github.com/omer-damar/InternshipTrackerDemo.git
cd InternshipTrackerDemo
open "Internship Tracker.xcodeproj"
```

### Location Permission

In Xcode, open the app target's Info settings and add:

| Key | Suggested value |
|---|---|
| `NSLocationWhenInUseUsageDescription` | We use your location to show company locations and provide directions. |

## Remote Jobs

The job board consumes the [Remotive public API](https://remotive.com/api/remote-jobs):

```http
GET https://remotive.com/api/remote-jobs
```

On the first successful fetch, existing job IDs are marked as seen. On later refreshes, newly observed IDs can trigger a local notification.

## Project Structure

```text
Internship Tracker/
├── App/             # App entry point, assets and onboarding
├── Helpers/         # Shared helpers
├── Models/          # SwiftData and remote API models
├── Services/        # Networking, location and notifications
└── Views/
    ├── Analytics/
    ├── Applications/
    ├── Calendar/
    ├── Jobs/
    ├── Map/
    ├── Settings/
    └── Tools/
```

## Contributors

- [Berat Zengin](https://github.com/devberatzengin)
- [Ömer Faruk Damar](https://github.com/omer-damar)

This repository is a fork of the original collaborative project and keeps both contributors visible.

