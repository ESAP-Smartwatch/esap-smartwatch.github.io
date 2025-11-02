---
layout: home
navname: Home

# Cells at the bottom of the page
cellLinks:
  - cname: Documentation
    curl: map
    cimage: media/demo02.jpg

  - cname: Screenshots
    curl: screenshots
    cimage: media/demo03.jpg

  - cname: About
    curl: about
    cimage: media/demo04.jpg

  - cname: Support
    curl: donate
    cimage: media/demo02.jpg

  - cname: GitHub
    curl: https://github.com/ESAP-Smartwatch/app
    cnewtab: true
    cimage: media/demo03.jpg

  - cname: Releases
    curl: https://github.com/ESAP-Smartwatch/app/releases
    cnewtab: true
    cimage: media/demo04.jpg
---

## About the Project

The ESAP Smartwatch is an **open-source health tracking smartwatch** developed by the Embedded Systems @ Purdue team. This project combines hardware design, embedded systems programming, and mobile app development to create a fully functional fitness tracking solution.

The smartwatch syncs with a companion mobile app via Bluetooth Low Energy (BLE), transmitting heart rate and movement data for comprehensive health monitoring.

---

## Features {#features}

### Mobile App
- 📊 **Health Tracking**: Monitor calories burned, workout duration, and daily steps
- 🏃 **Workout Logging**: Add, view, and manage workout sessions with type, duration, and calories
- 📱 **Bluetooth Connectivity**: Pair with the smartwatch via BLE using custom device UUID
- 📈 **Statistics Dashboard**: View overall statistics, averages, and workout breakdowns
- 💡 **Fitness Tips**: Get daily fitness recommendations

### Hardware
- ⌚ **Custom PCB Design**: Open-source hardware design using KiCad
- 💓 **Heart Rate Monitoring**: Real-time heart rate tracking
- 🏃‍♂️ **Movement Detection**: Accelerometer-based activity tracking
- 🔋 **Battery Powered**: Optimized for extended usage
- 📡 **BLE Communication**: Wireless data sync with mobile devices

---

## Getting Started {#getting-started}

### Prerequisites
- Node.js (v14 or newer)
- npm or yarn
- Expo CLI
- iOS Simulator (for macOS) or Android Emulator

### Installation

1. Clone the repository:
```bash
git clone https://github.com/ESAP-Smartwatch/app.git
cd app
```

2. Install dependencies:
```bash
npm install
```

3. Run on iOS:
```bash
npx expo start
# Press 'i' for iOS Simulator
```

4. Run on Android:
```bash
npx expo start
# Press 'a' for Android Emulator
```

For detailed setup instructions, including platform-specific guides, visit the [Quick Start Guide](https://github.com/ESAP-Smartwatch/app/blob/main/QUICK_START.md).

---

## Tech Stack {#tech-stack}

### Mobile App
- **React Native**: Cross-platform mobile framework
- **Expo**: Development and build platform
- **JavaScript & TypeScript**: Primary languages
- **React Navigation**: Navigation library
- **Context API**: State management
- **Ionicons**: Icon library

### Hardware
- **Arduino**: Microcontroller platform
- **KiCad**: PCB design software
- **Bluetooth Low Energy (BLE)**: Wireless communication
- **Embedded C/C++**: Firmware development

---

## App Structure

```
app/
├── App.js                          # Main app entry point
├── src/
│   ├── components/                 # Reusable components
│   │   ├── Button.js
│   │   ├── StatCard.js
│   │   └── WorkoutItem.js
│   ├── screens/                    # Main screens
│   │   ├── HomeScreen.js
│   │   ├── WorkoutScreen.js
│   │   └── StatsScreen.js
│   └── context/                    # State management
│       └── WorkoutContext.js
├── package.json
└── app.json
```

---

## Contributing

This project is developed by the Embedded Systems @ Purdue team. Contributions are welcome!

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## Documentation

- [Quick Start Guide](https://github.com/ESAP-Smartwatch/app/blob/main/QUICK_START.md)
- [Arduino Setup](https://github.com/ESAP-Smartwatch/app/blob/main/ARDUINO_SETUP.md)
- [Design Standards](https://github.com/ESAP-Smartwatch/app/blob/main/DESIGN_STANDARDS.md)
- [Implementation Summary](https://github.com/ESAP-Smartwatch/app/blob/main/IMPLEMENTATION_SUMMARY.md)
- [App Store Submission](https://github.com/ESAP-Smartwatch/app/blob/main/APP_STORE_SUBMISSION.md)

---

## License

This project is licensed under the [Apache 2.0 License](https://www.apache.org/licenses/LICENSE-2.0).

Copyright © 2025 by William Zhang & Embedded Systems @ Purdue
