# DC Motor

## Overview
- The DC motor is a small electric motor used to create movement in projects.
- It is commonly used for wheels, fans, pumps, and rotating parts.
- The motor is suitable for beginner electronics and simple robotics projects.

## Description
- A DC motor converts electrical energy into mechanical rotation.
- When power is supplied, the motor spins in one direction.
- By changing the polarity or using a motor driver, the direction can be controlled.

## Features
- Simple and easy to use
- Low cost and widely available
- Useful for motion and automation projects
- Can be controlled with a microcontroller

## Specifications
- Type: DC brushed motor
- Voltage: typically 3V to 6V depending on the model
- Current: varies by load and motor size
- Rotation: continuous rotation when powered
- Control method: direct power or motor driver

## Pinout
- **VCC**: Power input
- **GND**: Ground connection
- **Signal / Control**: Connected through a motor driver or controller pin

## Plug and Play with Sprout Baseboard
- The DC motor can be connected to the Sprout baseboard through the appropriate output port.
- Make sure the motor power supply is suitable for the motor rating.
- Use a motor driver if the motor needs more current than the controller can provide.

## How It Works
- The motor receives electrical current from the power source.
- The current creates a magnetic field inside the motor.
- The interaction of magnetic fields causes the shaft to rotate.
- The speed and direction of rotation depend on voltage and control method.

## Arduino Example

### Hardware Setup
- 1 x DC motor
- 1 x motor driver module
- Arduino board
- Jumper wires
- Power supply

### Arduino Code
```cpp
int motorPin = 9;

void setup() {
  pinMode(motorPin, OUTPUT);
}

void loop() {
  analogWrite(motorPin, 128);
  delay(2000);
  analogWrite(motorPin, 0);
  delay(2000);
}
```

### Results
- The motor runs at medium speed for 2 seconds.
- Then it stops for 2 seconds.
- This repeats continuously.

## ESP32 Example

### Hardware Setup
- 1 x DC motor
- 1 x motor driver board
- ESP32 development board
- Jumper wires
- Power supply

### ESP32 Code
```cpp
int motorPin = 18;

void setup() {
  pinMode(motorPin, OUTPUT);
}

void loop() {
  analogWrite(motorPin, 150);
  delay(2000);
  analogWrite(motorPin, 0);
  delay(2000);
}
```

### Results
- The motor turns on and off in cycles.
- This helps test basic motor control.

## Applications
- Robot wheels
- Small fans
- Pumps
- Toy projects
- Automated moving parts

## Troubleshooting
- If the motor does not spin, check the power supply.
- If the motor is weak, verify the voltage rating.
- If the motor is noisy, make sure the wiring is secure.
- If using a motor driver, confirm the driver is connected correctly.

## FAQ

### Frequently Asked Questions
- **Can the motor run directly from the microcontroller?**
  - Usually no. A motor driver is safer and more reliable.

- **Can the motor change direction?**
  - Yes, with a motor driver or by reversing polarity.

- **What happens if the motor draws too much current?**
  - The board may reset or the driver may shut down. Use a suitable power source.
