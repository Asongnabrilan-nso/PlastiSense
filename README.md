Video: `https://youtu.be/B_dy0DAJdtQ`

# PlastiSense

PlastiSense is a precise **filament diameter sensor** powered by the **Seeed Studio XIAO ESP32-C3**. It is designed to monitor filament quality in real-time, offering a web-based dashboard and API for data integration.

## 🚀 Features

-   **Real-time Measurement**: High-precision diameter readings in millimeters (mm).
-   **Web Dashboard**: Hosted on the device itself (`http://winfidel.local`), providing a visual interface for monitoring.
-   **REST API**: JSON endpoints for easy integration with other systems (e.g., OctoPrint, Home Assistant).
-   **WiFi Connectivity**: Connects to your home/office network.
-   **Captive Portal**: Easy initial setup via the `SK-WInFiDEL-Setup` access point.
-   **OTA Updates**: Support for Over-The-Air firmware updates.

## 🛠️ Hardware

The project is built around:
-   **Microcontroller**: [Seeed Studio XIAO ESP32-C3](https://www.seeedstudio.com/Seeed-XIAO-ESP32C3-p-5431.html)
-   **Custom PCB**: Files located in the `PlastiSense_PCB` dictionary.
-   **Stl Files**: 3D printable case files located in `stl` directory.

## 📁 Project Structure

-   `Firmware/`: Source code for the ESP32-C3 firmware (PlatformIO project).
-   `Hardware/`: Mechanical parts and diagrams.
-   `PlastiSense_PCB/`: KiCad PCB design files.
-   `stl/`: 3D printable STL files for the sensing unit.

## ⚡ Getting Started

### 1. Build & Flush Firmware
Detailed instructions for building and flashing the firmware can be found in the [Firmware Documentation](Firmware/README.md).

### 2. Connect to the Device
1.  Power on the PlastiSense device.
2.  Connect to the WiFi network named **SK-WInFiDEL-Setup**.
3.  A captive portal should open. If not, visit `http://192.168.4.1`.
4.  Configure your local WiFi credentials.

### 3. Access the Dashboard
Once connected to your network, access the device at:
-   **URL**: `http://winfidel.local`
-   **API Endpoint**: `http://winfidel.local/api/v0/diameter/read`

For more details on connection and API usage, see the [Connection Guide](Firmware/connection.md).