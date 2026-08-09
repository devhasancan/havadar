# Havadar ☁️

A robust, location-aware iOS weather application demonstrating advanced networking, concurrent threading, and strictly decoupled MVC architecture.

## 📌 Executive Summary
Havadar is a production-ready weather application that fetches real-time meteorological data via the OpenWeatherMap API. The core engineering focus of this project is secure network requests, asynchronous data parsing, and native device hardware integration (GPS) using Apple's Core Location framework. 

## 🛠 Technical Architecture & Core Competencies

*   **Protocol-Oriented Programming (Delegation):** Engineered custom protocols (`WeatherManagerDelegate`, `UITextFieldDelegate`) to establish secure, decoupled, one-way communication between the networking layer and the user interface.
*   **Asynchronous Networking & Concurrency:** Utilized native `URLSession` to execute non-blocking HTTP requests. Implemented strict thread safety by pushing all UI state updates to the Main Thread via `DispatchQueue.main.async`.
*   **Data Parsing (Codable):** Leveraged Swift's `Codable` protocol and `JSONDecoder` to safely and efficiently map complex JSON payloads into strongly typed structural models (`WeatherData`).
*   **Core Location Integration:** Interfaced with device GPS hardware via `CLLocationManager` to dynamically fetch localized weather data based on the user's real-time geographic coordinates.
*   **Dynamic UI & Computed Properties:** Utilized computed properties within `WeatherModel` to dynamically evaluate API weather condition codes and assign matching vector assets (SF Symbols) for a polished user interface.
*   **Security & Version Control:** Strictly isolated API keys from the public repository using `.gitignore` and local environment structs to prevent secret leakage and ensure industry-standard security.

## 👨‍💻 Developer Insight
This project represents a deep dive into dynamic, data-driven iOS software. The primary architectural challenge was managing the asynchronous nature of web requests while ensuring the UI remained highly responsive. By isolating the API configuration and employing the Delegate Design Pattern, the View Controller acts purely as a UI lifecycle manager. This results in a highly maintainable, scalable, and secure codebase.
