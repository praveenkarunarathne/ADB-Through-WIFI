# ADB Through WiFi

This repository provides a guide for connecting to Android devices through WiFi using ADB (Android Debug Bridge).

## Prerequisites

- Android Debug Bridge (ADB) installed on your computer
- Android device with USB debugging enabled
- Both computer and Android device connected to the same WiFi network

## Commands

Follow these commands in order to establish a WiFi connection with your Android device:

### 1. Check connected devices
```bash
adb devices
```
This command lists all connected Android devices. Make sure your device appears in the list before proceeding.

### 2. Enable TCP/IP mode
```bash
adb tcpip 5555
```
This command restarts the ADB daemon on the device in TCP/IP mode on port 5555.

### 3. Connect via WiFi
```bash
adb connect 192.168.49.1:5555
```
This command connects to the Android device using its IP address (192.168.49.1 in this example) on port 5555.

## Notes

- Replace `192.168.49.1` with your Android device's actual IP address
- You can find your device's IP address in Settings > About phone > Status > IP address
- After the initial setup, you can disconnect the USB cable and continue using ADB wirelessly
- To disconnect, use: `adb disconnect 192.168.49.1:5555`

## Troubleshooting

- Ensure both devices are on the same network
- Check that USB debugging is enabled on your Android device
- Verify the correct IP address of your Android device
- Make sure port 5555 is not blocked by firewall settings