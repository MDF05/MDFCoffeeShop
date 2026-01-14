# Deployment Guide

This document outlines the steps to build and deploy the **CoffeShop** application using **EAS (Expo Application Services)**.

## 📋 Prerequisites

1.  **EAS CLI**: Install via `npm install -g eas-cli`.
2.  **Expo Account**: You need to be logged in (`eas login`).
3.  **Project Configuration**: Ensure `app.json` and `eas.json` are correctly configured.

## 🚀 Building for Production

### Android (APK / AAB)

1.  **Configure Build Profile**:
    Ensure your `eas.json` has a production profile:
    ```json
    "build": {
      "production": {
        "android": {
          "buildType": "app-bundle"
        }
      }
    }
    ```

2.  **Run Build**:
    ```bash
    eas build --platform android --profile production
    ```

### iOS (IPA)

*Note: Requires an Apple Developer Account.*

1.  **Run Build**:
    ```bash
    eas build --platform ios --profile production
    ```

## 📲 Deployment to App Stores

### Google Play Store

1.  **Manual Upload**: Download the `.aab` file from the EAS build dashboard and upload it to the Google Play Console.
2.  **Automated**: Use EAS Submit.
    ```bash
    eas submit -p android
    ```

### Apple App Store

1.  **Automated**: Use EAS Submit to upload to TestFlight or the App Store.
    ```bash
    eas submit -p ios
    ```

## 🔄 OTA Updates (Over-The-Air)

You can push updates to your users without going through the store review process for JavaScript-only changes.

1.  **Publish Update**:
    ```bash
    eas update --branch production --message "Quick bug fix"
    ```

## 🛠 Internal Testing

### Preview Builds
To create a build for internal testing (not for store):

```bash
eas build --profile preview --platform all
```

This will generate an APK (Android) and an internal distribution build (iOS) that can be installed directly on devices.
