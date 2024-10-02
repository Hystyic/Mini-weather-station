# Mini Weather Station

This project uses an Arduino and various sensors to monitor environmental conditions such as temperature, humidity, light, UV radiation, dust particles, air pressure, and rainfall. The system outputs real-time data to the serial monitor, providing information about the environment, which can be used for various applications like weather stations or air quality monitoring.

## Components Used:
- **DHT22 Sensor**: Measures temperature and humidity.
- **Adafruit BMP085 Sensor**: Measures barometric pressure and altitude.
- **Dust Sensor**: Monitors dust particle density in the air.
- **Light Sensor (Photoresistor)**: Detects light intensity.
- **UV Sensor**: Measures ultraviolet light levels.
- **Rain Sensor**: Detects the presence of rain.

## Libraries:
- `DHT.h`: Required for the DHT22 sensor to read temperature and humidity.
- `Adafruit_BMP085.h`: Required for the BMP085 sensor to read barometric pressure and altitude.

## Pin Configuration:

| **Component**          | **Pin Type**   | **Arduino Pin** |
|------------------------|----------------|-----------------|
| DHT22 Sensor (Temperature & Humidity) | Digital | 7               |
| Dust Sensor            | Analog Input   | A0              |
| UV Sensor              | Analog Input   | A1              |
| Rain Sensor            | Analog Input   | A3              |
| Light Sensor (Photoresistor) | Analog Input   | A0              |
| Adafruit BMP085 (Barometric Pressure & Altitude) | I2C (SDA, SCL)  | Connected via I2C (Wire library) |

## Code Functionality:
1. **Light Intensity**: The light sensor detects the brightness levels, categorizing the conditions as "Normal", "Too Bright", or "Dark" based on the sensor value.
2. **Temperature and Humidity**: The DHT22 sensor reads the temperature and humidity, displaying the values in the serial monitor.
3. **UV Detection**: The UV sensor monitors the UV radiation levels and provides feedback based on normal or high UV levels.
4. **Dust Particles**: The dust sensor measures the dust density in the air and displays the particle concentration in PPM (Parts Per Million).
5. **Barometric Pressure and Altitude**: The BMP085 sensor reads the atmospheric pressure and calculates the altitude above sea level.
6. **Rain Detection**: The rain sensor checks if rain is present and outputs whether rain is detected or not.

## How to Use:
1. Connect the sensors to the corresponding pins on the Arduino as per the pin configuration.
2. Install the necessary libraries (`DHT.h`, `Adafruit_BMP085.h`) through the Arduino Library Manager.
3. Upload the code to your Arduino.
4. Open the serial monitor to view the environmental data in real time.

## Notes:
- Ensure proper calibration for sensors if required for more accurate readings.
- Power the sensors appropriately (check sensor datasheets for voltage requirements).
- Modify sensor thresholds as needed based on your environmental conditions.
