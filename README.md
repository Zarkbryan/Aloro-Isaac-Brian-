# Aloro Systems Lighting Dashboard

This project is a web-based lighting control system built with an ESP32 using WiFi. It provides a dashboard to manually control three LEDs and switch between automatic or manual control modes. The system automatically adjusts the LED lights based on the ambient light level using a Light Dependent Resistor (LDR).

## Features

- **Manual Mode**: Control LEDs individually through a web interface.
- **Automatic Mode**: LEDs will automatically turn ON when the ambient light level is low (LDR value < 1500) and turn OFF when the light level is high.
- **Web Dashboard**: A simple and styled HTML interface to control the system.
- **Switch Between Modes**: You can toggle between "Auto" and "Manual" modes.
- **Real-time Light Level**: View the ambient light level read by the LDR in real-time.

## Hardware Required

- **ESP32** Development Board
- **3 LEDs** (with resistors)
- **1 Light Dependent Resistor (LDR)**
- **Breadboard and Jumper Wires**
- **A WiFi network** for the ESP32 to connect to.

## Circuit Diagram

- Connect the **LDR** to pin **34**.
- Connect the **LEDs** to pins **33**, **32**, and **27**, with appropriate resistors.

## Software Requirements

- **Arduino IDE** with ESP32 board package installed.
- **WiFi** library (comes pre-installed with ESP32 board package in Arduino IDE).

## Installation

1. Clone this repository or download the source code.

2. Open the Arduino IDE and load the code into your ESP32 board.

3. Set the WiFi credentials in the code by updating the following lines:
    ```cpp
    const char* ssid     = "YourWiFiNetworkName";
    const char* password = "YourWiFiPassword";
    ```

4. Select the correct ESP32 board and port in the Arduino IDE.

5. Upload the code to your ESP32.

6. Open the Serial Monitor to view the ESP32's IP address after it connects to the WiFi.

7. Open a web browser and enter the ESP32 IP address (e.g., `http://192.168.1.100`).

## Web Interface

### Modes
- **Switch to Manual Mode**: Control the LEDs individually.
- **Switch to Automatic Mode**: LEDs automatically adjust based on ambient light.

### LED Control in Manual Mode
- Turn **LED 1** on/off.
- Turn **LED 2** on/off.
- Turn **LED 3** on/off.

### Light Level Display
The current ambient light level read by the LDR will be displayed on the dashboard.

## Example Web Dashboard

![Dashboard Example](images/dashboard_example.png)

## Troubleshooting

- Ensure that your ESP32 is properly connected to the WiFi network.
- If the IP address is not showing up in the Serial Monitor, ensure the ESP32 has successfully connected to the network.
- Verify the LDR and LED connections if the manual control doesn’t work.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Credits

- **Author**: Aloro Isaac Brian
- **Team**: Innovators
