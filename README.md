# G0X Core

G0X Core is a consent-based Android remote device management and screen-sharing application. It allows users to view and manage their own or explicitly authorized Android devices through a secure web dashboard.

## Features

* Live Android screen sharing
* User-approved remote device management
* Android Accessibility Service integration
* MediaProjection-based screen capture
* Secure WebSocket communication
* Foreground service notification
* Session-based device connection
* Permission-based access control

## Architecture

```text
Android App
    ↓
MediaProjection / Accessibility Service
    ↓
Secure WebSocket Server
    ↓
G0X Web Dashboard
```

## Requirements

* Android 8.0 or higher
* Android Studio
* JDK 17 or compatible version
* A running G0X web dashboard
* HTTPS/WSS-enabled server

## Android Setup

1. Clone this repository.
2. Open the project in Android Studio.
3. Make sure the application ID is:

```text
com.g0x.network
```

4. Build and install the application on your Android device.
5. Open the app and grant the required permissions manually.
6. Approve screen-sharing permission when Android displays the system dialog.
7. Connect the device to the G0X web dashboard.

## Required Permissions

The app may request permissions for:

* Screen capture through MediaProjection
* Accessibility-based device interaction
* Foreground screen-sharing service
* Internet communication

Permissions must be granted by the device owner. The app does not bypass Android security restrictions.

## Security

* Use only your own devices or devices for which you have clear permission.
* Never share authentication tokens or private keys.
* Always use HTTPS and secure WebSocket connections.
* Keep the foreground notification visible during screen sharing.
* Stop the session when remote access is no longer needed.

## Project Structure

```text
G0X-Core/
├── app/
│   └── src/
├── AndroidManifest.xml
├── README.md
└── build.gradle
```

## Disclaimer

G0X Core is intended for legitimate remote support, testing, education, and management of authorized devices only. Do not use this project for unauthorized monitoring, hidden access, credential collection, or privacy-invasive activities.

## License

This project is provided for educational and authorized-use purposes.
