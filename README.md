# ADB Through WiFi

This repository provides instructions on how to connect to your Android device over WiFi using ADB (Android Debug Bridge).

## Prerequisites

- Android device with USB debugging enabled
- ADB installed on your computer
- Device and computer connected to the same network

## Commands

### 1. Check connected devices

First, make sure your device is connected via USB and is recognized:

```bash
adb devices
```

### 2. Set device to TCP/IP mode

Enable TCP/IP mode on your device with port 5555:

```bash
adb tcpip 5555
```

### 3. Connect to device over WiFi

After enabling TCP/IP mode, connect to your device using its IP address:

```bash
adb connect 192.168.49.1:5555
```

### 4. Switch back to USB mode

When you're done, you can switch back to USB mode:

```bash
adb usb
```
