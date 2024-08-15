# Smart Classroom

This project implements a smart classroom system using an Arduino, a fingerprint sensor, and an LCD display. The system counts the number of students entering and exiting a room and controls various devices (fans and lights) based on the count.

## Components Required

- Arduino (e.g., Arduino Uno)
- Fingerprint sensor (e.g., Adafruit Fingerprint Sensor)
- I2C LCD display (16x2)
- Relay modules for controlling devices (fans and lights)
- Infrared (IR) sensors for detecting entry and exit

## Libraries Used

- `Wire.h`: For I2C communication.
- `LiquidCrystal_I2C.h`: For controlling the I2C LCD display.
- `Adafruit_Fingerprint.h`: For interfacing with the fingerprint sensor.
- `SoftwareSerial.h`: For creating a software serial connection.


## Functionality

1. **Fingerprint Authentication**: 
   - The system prompts the user to scan their fingerprint.
   - If the fingerprint is recognized, access is granted, and a lock is unlocked for a brief period.

2. **Student Counting**:
   - The system uses two IR sensors to detect students entering and exiting.
   - The count of students is displayed on the LCD.

3. **Device Control**:
   - Based on the number of students, the system controls fans and lights:
     - No students: All devices off.
     - 1-6 students: Some devices turned on.
     - More than 6 students: All devices turned on.

## Usage

1. Connect all components as per the pin definitions.
2. Upload the code to the Arduino.
3. Scan your fingerprint to gain access.
4. Enter and exit the room to see the student count update on the LCD.

## Notes

- Ensure that the fingerprint sensor is properly calibrated and enrolled with fingerprints before use.
- Adjust the relay connections according to your hardware setup.
- Modify the access delay and other parameters as needed for your specific application.

## License

This project is open-source. Feel free to modify and use it for your own applications!
