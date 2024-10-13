Weather Station using Raspberry Pi and Arduino
This project presents a comprehensive weather station system utilizing Raspberry Pi and Arduino to monitor environmental parameters like rain intensity, air quality, light intensity, temperature, humidity, and wind speed. The integration of analog and digital sensors ensures accurate data acquisition, processed locally and backed up in the cloud.

Features
Arduino for reading analog sensors:

Rain Drop Sensor
MQ135 Air Quality Sensor
LDR Light Intensity Sensor
Raspberry Pi for handling digital sensors and system operations:

DHT11 Temperature and Humidity Sensor
Wind Sensor (Ultrasonic Sensors)
Pi Camera (for weather prediction using ML in future)
Data Storage and Visualization:

SQLite3 for local data storage
Google Firebase for real-time cloud backup
Flask Web App to display real-time and historical weather data
System Architecture
Arduino collects analog sensor data and communicates it to Raspberry Pi via serial communication.
Raspberry Pi processes data from both analog and digital sensors, stores it locally, and syncs with Firebase for real-time availability.
Flask Web Application provides a front-end interface to visualize the data and interact with historical weather logs.
Error Handling: A buzzer system triggers notifications for system or sensor failures.
Hardware Components
Arduino Microcontroller: Handles analog sensors.
Raspberry Pi: Manages digital sensors and web server tasks.
Pi Camera: Captures sky images for ML-based weather prediction (future enhancement).
Sensors Used
Rain Drop Sensor: Detects rainfall presence and intensity.
MQ135 Air Quality Sensor: Measures air quality based on gas concentration.
LDR Sensor: Tracks ambient light intensity to distinguish between day and night.
DHT11 Sensor: Records temperature (°C) and humidity (%).
Ultrasonic Sensors: Calculate wind speed based on travel time of ultrasonic waves.
Software Components
Flask Web App: Displays real-time data from Firebase and local logs.
SQLite3: Local database for offline data storage.
Firebase API: Syncs weather data with cloud storage for remote access.
Buzzer System: Notifies in case of sensor or communication errors.
Future Work
Implement machine learning algorithms using the Pi Camera to predict weather conditions based on cloud patterns and sky visuals.
