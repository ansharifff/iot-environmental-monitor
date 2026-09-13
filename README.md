# IoT Environmental Monitor

Real-time environmental monitoring system using Arduino, dual DHT22 sensors, a BH1750 light sensor, and an OLED display, with SD card data logging.

**Skills demonstrated:** Sensor interfacing (I2C + analog), embedded C, hardware debugging, systems integration

## Components
- Arduino Uno R3
- DHT22 Temperature/Humidity Sensor (2×)
- BH1750 Light Sensor
- 1.3" OLED Display (128×64)
- Micro SD Card Module + 16GB card
- Breadboard + jumper wires

## Status
- **DHT22 temperature/humidity sensors:** working, stable readings
- **SD card logging:** working
- **BH1750 light sensor:** intermittent/unreliable readings — suspect a faulty unit or a wiring/pull-up issue on the I2C bus; still debugging
- **OLED display:** faulty — not reliably initializing or displaying; suspect either a bad unit or an I2C address/wiring conflict with the BH1750 on the same bus

## What I Learned
- Diagnosing whether an I2C fault is a bad component vs. a bus/address conflict (two I2C devices sharing a bus need distinct addresses and can interfere if wiring or pull-ups aren't right)
- Isolating faults by testing sensors independently before assuming the whole system design is wrong
- The value of testing individual modules before full integration — would test each sensor standalone first on any future build

## Next Steps
- Swap in a new OLED and BH1750 to confirm whether the issue is the units themselves or the shared I2C bus
- If confirmed as a bus conflict, add proper pull-up resistors or move one device to a different interface
