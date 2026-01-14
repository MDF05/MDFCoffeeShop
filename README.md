# CoffeShop - Mobile Application

**CoffeShop** is a modern, cross-platform mobile application built with **React Native** and **Expo**, designed to provide a seamless coffee ordering experience.

![Project Status](https://img.shields.io/badge/status-active-success.svg)
![License](https://img.shields.io/badge/license-Proprietary-blue.svg)
![Platform](https://img.shields.io/badge/platform-iOS%20%7C%20Android-lightgrey.svg)

## 📖 Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Usage](#usage)
- [Environment Variables](#environment-variables)
- [Folder Structure](#folder-structure)
- [📚 Documentation](#-documentation)
- [Contributing](#contributing)
- [Security](#security)
- [License](#license)
- [Author](#author)

## 🚀 Project Overview

CoffeShop aims to revolutionize the way customers interact with their favorite coffee spots. Built for both iOS and Android, it leverages the power of Expo to deliver a high-performance, native-like experience.

## ✨ Features

- **Cross-Platform**: Runs smoothly on both iOS and Android devices.
- **Intuitive UI**: Designed with a focus on user experience and ease of use.
- **Fast Performance**: Optimized for speed and responsiveness.
- **File-Based Routing**: Utilizes Expo Router for simplified navigation logic.

## 🛠 Tech Stack

- **Framework**: [React Native](https://reactnative.dev/) (v0.76.2)
- **Platform**: [Expo](https://expo.dev/) (~52.0.9)
- **Routing**: [Expo Router](https://docs.expo.dev/router/introduction/) (~4.0.7)
- **Language**: TypeScript / JavaScript
- **Testing**: Jest, Jest-Expo

## 📥 Installation

Follow these steps to set up the project locally.

### Prerequisites

- Node.js (LTS recommended)
- npm or yarn
- Expo CLI (`npm install -g expo-cli`)

### Steps

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/MDF05/coffeshop.git
    cd coffeshop
    ```

2.  **Install dependencies:**
    ```bash
    npm install
    ```

3.  **Start the development server:**
    ```bash
    npx expo start
    ```

## 📱 Usage

After starting the server:
- **Android**: Press `a` in the terminal to open in Android Emulator.
- **iOS**: Press `i` in the terminal to open in iOS Simulator (macOS only).
- **Web**: Press `w` in the terminal to run in the browser.

## 🔑 Environment Variables

Create a `.env` file in the root directory to configure the application. See [ENVIRONMENT.md](ENVIRONMENT.md) for details.

## 📂 Folder Structure

```
CoffeShop/
├── app/                 # Expo Router application code
├── assets/              # Static assets (images, fonts)
├── components/          # Reusable React components
├── constants/           # Global constants and config
├── hooks/               # Custom React hooks
├── scripts/             # Utility scripts
├── src/                 # Source code
├── .env                 # Environment variables
├── app.json             # Expo configuration
├── package.json         # Dependencies and scripts,
└── README.md            # Project documentation
```

## 📚 Documentation

For detailed information, please refer to the specific documentation files below:

- [Architecture](ARCHITECTURE.md)
- [API Documentation](API_DOCUMENTATION.md)
- [Database Schema](DATABASE_SCHEMA.md)
- [Deployment Guide](DEPLOYMENT.md)
- [Environment Configuration](ENVIRONMENT.md)
- [Testing Guide](TESTING.md)
- [Style Guide](STYLE_GUIDE.md)
- [Contributing Guide](CONTRIBUTING.md)
- [Code of Conduct](CODE_OF_CONDUCT.md)
- [Security Policy](SECURITY.md)
- [Governance](GOVERNANCE.md)
- [Support](SUPPORT.md)
- [Roadmap](ROADMAP.md)
- [Changelog](CHANGELOG.md)
- [Disclaimer](DISCLAIMER.md)
- [License](LICENSE)

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guide](CONTRIBUTING.md) for details on how to get started.

## 🔒 Security

For security vulnerabilities and reporting, please verify our [Security Policy](SECURITY.md).

## 📄 License

This project is proprietary software. See the [LICENSE](LICENSE) file for details.

## ✍️ Author

**mdavafahreza**
- Owner of CoffeShop
