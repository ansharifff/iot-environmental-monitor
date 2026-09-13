# IoT Environmental Monitor

Real-time environmental monitoring system using Arduino, dual DHT22 sensors, a BH1750 light sensor, and an OLED display, with persistent SD card data logging.

**Skills demonstrated:** Sensor interfacing (I2C + analog), embedded C, data logging, systems integration

## Components
- Arduino Uno R3
- DHT22 Temperature/Humidity Sensor (2×)
- BH1750 Light Sensor
- 1.3" OLED Display (128×64)
- Micro SD Card Module + 16GB card
- Breadboard + jumper wires

## How It Works
- Sensors are polled every [3 seconds] and readings are displayed live on the OLED
- Data is logged to the SD card in [CSV / plain text] format with a timestamp per entry

## Status
Completed — wiring, sensor reads, OLED display, and SD logging are all functional and tested.

## What I Learned
- Managing multiple I2C devices on one bus without address conflicts
- Handling sensor read timing/noise on the DHT22
- Structuring reliable data logging on embedded storage
