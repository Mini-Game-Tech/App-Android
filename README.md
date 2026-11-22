# 🕹️ Minigame Tech

> A cross-platform web platform for classic arcades, hosted on GitHub Pages and packaged in an Android app via WebView.

[![GitHub Pages](https://img.shields.io/badge/status-live-success.svg)](https://cipriano-salvatore.github.io/minigame-tech/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Platform](https://img.shields.io/badge/platform-Web%20|%20Android-blue.svg)](https://github.com/cipriano-salvatore/minigame-tech)
[![Android](https://img.shields.io/badge/Android-WebView%20Wrapper-green.svg)](https://github.com/cipriano-salvatore/minigame-tech/blob/main/app/)

---

## 📖 About The Project

**Minigame Tech** is an open-source project dedicated to recreating legendary retro arcade games. The platform combines:

- **Game logic** written in Python (with 'g2d', Pygame) and C#
- **Frontend interface** in modern and responsive HTML5/CSS3
- **Android wrapper** that encapsulates the website in a WebView for distribution on the Google Play Store

Whether you're dodging traffic in Frogger, clearing aliens in Space Invaders, or navigating mazes in Pac-Man, Minigame Tech delivers a nostalgic experience optimized for both desktop and mobile touch screens.

---

## 🎮 Features

- **Classic Arcade Remakes:** Faithfully recreated mechanics of timeless titles.
- **Cross-Platform Play:** Fully responsive design optimized for desktop browsers and mobile touchscreens.
- **Android App Support:** Published on the Google Play Store as a WebView-wrapper application for friction-free mobile deployment.
- **Zero-Dependency Web Core:** The web heart is built with efficient core scripts and modern web standards for fast loading times.

> **Note:** The Android app acts as a WebView container for the web platform. Native features are currently limited to fullscreen and offline pull-to-refresh modes.

---

## 🚀 Built With

- **Basic Logic and Game Cycles:** Python ('g2d', Pygame) / C#
- **Frontend:** HTML5, CSS3, Responsive Design
- **Hosting and CI/CD:** GitHub Pages
- **Mobile wrapper:** Android Studio (Java, WebView API)

---

## 🌐 Live Demo & Access

You can play minigames directly through the web platform:

🔗 **[https://mini-game-tech.github.io/](https://cipriano-salvatore.github.io/mini-game-tech/)**

**Service Status:** The GitHub Pages site is actively maintained and the badge above reflects its current status. If the link doesn't work, open an issue on the repository.

---

## 📱 Android Application

Minigame Tech is also available as an Android application, bringing the full retro arcade experience to smartphones with optimized touch layouts and immersive fullscreen mode.

**Important:** The app is a WebView wrapper around the web platform. Contains no native game code: all games run inside the WebView by loading 'https://minigame-tech.github.io/`.

**Required permits:**
- 'INTERNET': For loading the web page.
- 'ACCESS_NETWORK_STATE': To detect the connection and display the appropriate offline page.

Network security is managed via 'network_security_config', which enforces HTTPS for the 'minigame-tech.github.io' domain and blocks clear-text traffic.

---

## 🛠️ Local Development & Setup

To run or modify the project locally:

1. **Clone the repository:**
   "'bash
   git clone https://github.com/cipriano-salvatore/minigame-tech.git
   "'

2. **Navigate to the project directory:**
   "'bash
   minigame-tech CD
   "'

3. **Open and test:** Open 'index.html' in your preferred browser or serves it via a local development server (e.g., Python's HTTP server):
   "'bash
   python3 -m http.server 8000
   "'

To test the Android app:
- Open the project in Android Studio.
- Make sure you have a recent version of the JDK (Java 17+ recommended).
- Run on a device or emulator with API level 24+.

---

## 🔒 Security & Privacy

- **Network Security:** The app imposes HTTPS for all web uploads. Free-to-air traffic (HTTP) is blocked at the Android configuration level.
- **Local Data:** No sensitive data is stored locally. Access to local files on the device is disabled in the WebView for security reasons.
- **Privacy:** There are no third-party trackers or analytics in the Android app. The web page may have its own privacy policy.

---

## 🤝 Contributing

Contributions, problem reports, and feature requests are welcome! Feel free to check out the [issues page](https://github.com/cipriano-salvatore/minigame-tech/issues).

1. Fork the Project
2. Create your feature branch ('git checkout -b feature/AmazingFeature')
3. Commit your changes ('git commit -m 'Add some AmazingFeature")
4. Push to branch ('git push origin feature/AmazingFeature')
5. Open a Pull Request

---

## 📄 License

Distributed under the MIT License. See [LICENSE](https://github.com/cipriano-salvatore/minigame-tech/blob/main/LICENSE.md) for more information.

---

## 🛠️ Internal Technical Stack (Developer Notes)

> This information is for technical contributors.

- **Web Core:** Static site generated with pure HTML/CSS/JS, hosted on GitHub Pages.
- **Android App:** 'app/' module on Android Studio, minimum SDK 24, target SDK 37.
- **Build System:** Gradle with Java 17 (compatible with compileSdk 37).
- **Resources added:** 'res/xml/network_security_config.xml' for configured network security.