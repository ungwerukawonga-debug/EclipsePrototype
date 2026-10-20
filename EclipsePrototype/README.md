# EclipsePrototype

This document explains how to run the EclipsePrototype application on Windows and Android.

## Project Overview

EclipsePrototype is a .NET MAUI Blazor Hybrid application. It combines a native MAUI shell with embedded Blazor web UI components, providing a cross-platform experience.

## Prerequisites

Before running the application, ensure you have the following installed:

*   **.NET SDK**: Install the latest .NET SDK (version 9.0 or later, as indicated in `EclipsePrototype.csproj`).
*   **.NET MAUI Workloads**: Install the necessary .NET MAUI workloads. You can do this by running:
    ```bash
    dotnet workload install maui
    ```

### For Android Development

To run the application on an Android device or emulator, you will also need:

*   **Android SDK**: Installed via Visual Studio or Android Studio.
*   **Android Device/Emulator**:
    *   **Emulator**: An Android Virtual Device (AVD) configured and running in Android Studio's Device Manager.
    *   **Physical Device**: An Android phone with USB Debugging enabled in Developer Options, connected to your computer via USB, and authorized for debugging.

## How to Run the Application

### 1. Navigate to the Project Directory

Open your terminal or command prompt and navigate to the root directory of the `EclipsePrototype` project:

```bash
cd C:\Users\kawon\Desktop\Prototype\EclipsePrototype\EclipsePrototype
```

### 2. Run on Windows

To run the application on your Windows machine:

```bash
dotnet run -f net9.0-windows10.0.19041.0
```

This command will build the application and launch it in a new window on your desktop.

### 3. Run on Android

To run the application on a connected Android device or running emulator:

**Ensure your Android device/emulator is ready before running this command.**

```bash
dotnet build -t:Run -f net9.0-android
```

This command will build the application for Android, deploy it to your active device/emulator, and launch it.

## Troubleshooting

*   **"No available device" error (Android)**: This means no Android emulator is running or no physical device is connected and recognized.
    *   Verify your device is connected and USB debugging is enabled.
    *   Check `adb devices` in your Android SDK `platform-tools` directory to ensure your device is listed.
    *   If using an emulator, ensure it's fully booted.
*   **Build Errors**: If you encounter build errors, ensure all .NET MAUI workloads are installed and your .NET SDK is up to date.

---
