# Smart Gardening - Using NodeMCU ESP8266 and Blynk

This Arduino project utilizes an ESP8266 microcontroller and various sensors to create an Internet of Things (IoT) system. The system includes the monitoring of soil moisture, temperature, and humidity, as well as the control of a relay to manage connected devices. The project integrates with the Blynk IoT platform for remote monitoring and control.

## Components

- ESP8266 microcontroller
- DHT11 Temperature and Humidity Sensor
- Soil Moisture Sensor
- Relay
- Push Button
- I2C-enabled LCD Display

## Setup

### Wiring

Connect the components according to the specified pin configurations in the code.

```c++
/* Connections
Relay. D3
Btn.   D7
Soil.  A0
SDA.   D2
SCL.   D1
Temp.  D4
*/
```

### Blynk Setup

1. Install the Blynk app on your mobile device.
2. Create a new project on the Blynk app.
3. Note the authentication token generated for your project.

### Arduino IDE Setup

1. Install the required libraries:
   - LiquidCrystal_I2C
   - ESP8266WiFi
   - Blynk
   - DHT

2. Open the Arduino sketch.
3. Replace the placeholders with your Blynk authentication token, Wi-Fi SSID, and Wi-Fi password:

   ```cpp
   char auth[] = "BLYNK_AUTH_TOKEN";
   char ssid[] = "WIFI_SSID";
   char pass[] = "WIFI_PASSWORD";
   ```

4. Upload the sketch to your ESP8266.

## Functionality

- Monitor temperature and humidity using the DHT11 sensor.
- Measure soil moisture and send data to the Blynk app.
- Control a relay to switch connected devices on/off.
- Physical button control to toggle the relay state.
- Display sensor data on an I2C-enabled LCD display.
- Blynk integration for remote monitoring and control.