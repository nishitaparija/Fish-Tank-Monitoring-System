# 🐠 Fish Tank Monitoring System

A cross-platform IoT monitoring application built with **Flutter**, designed to track and visualise real-time fish tank environmental data. The app connects to IoT sensors over HTTP and presents live readings through an intuitive, chart-driven dashboard — available on Android, iOS, Web, Linux, macOS, and Windows.

---

## Features

- **Real-Time Sensor Monitoring** — Live data fetched from IoT sensors via HTTP
- **Data Visualisation** — Interactive charts displaying tank conditions over time using `fl_chart`
- **Cross-Platform** — Single codebase runs on Android, iOS, Web, Linux, macOS, and Windows
- **State Management** — Reactive UI powered by GetX
- **Clean UI** — Material Design with Google Fonts and smooth tap animations

---

## Tech Stack

| Layer | Technology |
|---|---|
| Framework | Flutter (Dart) |
| State Management | GetX (`get: ^4.6.6`) |
| Data Fetching | HTTP (`http: ^1.1.0`) |
| Charts | fl_chart (`^0.63.0`) |
| UI Extras | flutter_spinkit, zoom_tap_animation, flutter_expandable_fab |
| Fonts | Google Fonts |
| Native Layers | C / C++ (CMake) |

---

## Project Structure

```
Fish-Tank-Monitoring-System/
├── lib/                  # Dart source — screens, controllers, models
├── android/              # Android platform layer
├── ios/                  # iOS platform layer
├── web/                  # Web platform layer
├── linux/                # Linux desktop platform layer
├── macos/                # macOS desktop platform layer
├── windows/              # Windows desktop platform layer
├── assets/
│   └── images/           # App assets
├── pubspec.yaml          # Dependencies and configuration
└── README.md
```

---

## Getting Started

### Prerequisites

- [Flutter SDK](https://docs.flutter.dev/get-started/install) (Dart SDK `>=2.19.5 <3.0.0`)
- Android Studio / Xcode (for mobile builds)
- A running IoT sensor backend (e.g. ESP8266 / NodeMCU serving sensor data over HTTP)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/nishitaparija/Fish-Tank-Monitoring-System.git
   cd Fish-Tank-Monitoring-System
   ```

2. **Install dependencies**
   ```bash
   flutter pub get
   ```

3. **Configure the sensor endpoint**

   Update the API base URL in the relevant controller file to point to your IoT device:
   ```dart
   const String baseUrl = 'http://<your-sensor-ip>';
   ```

4. **Run the app**

   ```bash
   # Mobile
   flutter run

   # Web
   flutter run -d chrome

   # Desktop (e.g. Linux)
   flutter run -d linux
   ```

---

## Supported Platforms

| Platform | Supported |
|---|---|
| Android | ✅ |
| iOS | ✅ |
| Web | ✅ |
| Linux | ✅ |
| macOS | ✅ |
| Windows | ✅ |

---

## IoT Integration

The app is designed to work alongside an IoT sensor node (e.g. ESP8266 / NodeMCU) that exposes sensor readings over a local HTTP endpoint. The Flutter app polls this endpoint and renders the data in real time.

Typical monitored parameters may include:
- 🌡️ Water temperature
- 💧 Water level
- ⚗️ pH level
- 🌊 Turbidity / water clarity

---

## Contributing

Contributions are welcome. To contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m 'Add your feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

---

## Author

**Nishita Parija**
- GitHub: [@nishitaparija](https://github.com/nishitaparija)
- LinkedIn: [linkedin.com/in/nishitaparija](https://linkedin.com/in/nishitaparija)

---

## License

This project is open source and available under the [MIT License](LICENSE).
