# Ambience
Ambience is a node-based smart lighting system built for ESP32 microcontrollers and designed to control individually-addressable ("neopixel") LEDs. Each device (Ambience "Node") running the Ambience software hosts a webserver over your local network which allows it to be controlled by any network-capable device through simple HTTP requests.  

This smart LED implementation aims to be **lightweight**, **flexible**, and **powerful** through *device/state composition*. What does that mean? It means each device is only concerned about its own state. The way these devices are controlled and how their states are composed in the real world is left up to the end user.

## Environment Setup
In order to build and flash Ambience onto an ESP32, you'll need to first install the required libraries and tools. Currently you must do the building and flashing of Ambience yourself using Arduino IDE.

1. Download and install the latest version of the [Arduino IDE](https://www.arduino.cc/en/Main/Software_).
2. Download and install the [ESP32fs plugin](https://github.com/me-no-dev/arduino-esp32fs-plugin/releases/tag/1.0).
3. Follow [Espressif's guide](https://docs.espressif.com/projects/arduino-esp32/en/latest/installing.html) for installing the ESP32 board into Arduino's board manager.
4. Install the required libraries using [Arduino's Library Manager](https://www.arduino.cc/en/guide/libraries).
    - **Adafruit NeoPixel** by Adafruit (Version 1.10.0+).
    - **ArduinoJson** by Benoit Blanchon (Version 6.18.4+).
    - **ArduinoOTA** by Juraj Andrassy (Version 1.0.7+).

## Firmware Installation
With the ESP32 connected to you computer via USB, the correct board selected, and the port set to the serial port associated with your ESP32, follow the instructions below to flash Ambience onto your ESP32. 
1. Clone or download the Ambience repository.
2. Open the Ambience.ino file in your Arduino IDE
3. Make any desired changes to the configuration macros in "Core.h" for this device.
    - Most noteably, esnure **NUM_LEDS**, **WIFI_SSID**, **WIFI_PASS**, and **DATA_PIN** are set correctly 
4. Upload content located in the "data" directory to the ESP32's interanl storage using the "ESP32 Sketch Data Upload" tool located in the "Tools" dropdown.
5. Build and Upload the sketch using the "Upload" button.
