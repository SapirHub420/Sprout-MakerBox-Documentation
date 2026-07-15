# Motor Driver

## Overview

<p align="center">
  <img src="C:\Users\user\OneDrive - Universiti Teknologi MARA\Documents\Github\Sprout-MakerBox-Documentation\images\PNG - TOP - SprouT - SENANG - Motor Driver.png" alt="SprouT Infrared Sensor" width="350">
</p>

- The motor driver is a small control module used to operate motors safely and efficiently.
- It allows a microcontroller to control the speed and direction of one or more motors.
- It is commonly used in robotics, automation, and moving projects.

## Description
- A motor driver acts as an interface between the control board and the motor.
- It receives signals from the microcontroller and provides enough power to drive the motor.
- The module helps protect the controller from high current and noise from the motor.

## Features
- Controls motor direction
- Controls motor speed using PWM
- Supports low-power control signals from a microcontroller
- Protects the main board from motor current spikes
- Useful for DC motors and simple robotic systems

## Specifications
- Type: DC motor driver module
- Control signal: digital or PWM input
- Power supply: depends on motor voltage rating
- Output: drives one motor channel or multiple channels depending on model
- Compatibility: works with Arduino, ESP32, and other microcontrollers

## Pinout
- **VCC / VM**: Motor power input
- **GND**: Ground connection
- **IN1 / IN2**: Control inputs for direction
- **ENA / PWM**: Speed control input
- **OUT1 / OUT2**: Motor output terminals

## Plug and Play with Sprout Baseboard
- The motor driver can be connected to the Sprout baseboard through the correct power and control pins.
- Make sure the motor voltage matches the driver rating.
- Use a suitable external power supply if the motor needs more current.
- Connect the motor to the output terminals only after the driver is powered correctly.

## How It Works
- The microcontroller sends control signals to the motor driver.
- The driver switches the current to the motor in the correct direction.
- PWM signals are used to change the motor speed.
- The driver behaves like a bridge between low-power logic and high-power motor current.

## Arduino Example

### Hardware Setup
- 1 x motor driver module
- 1 x DC motor
- Arduino board
- Jumper wires
- External power supply

### Arduino Code
```cpp
int in1 = 8;
int in2 = 9;
int pwmPin = 10;

void setup() {
  pinMode(in1, OUTPUT);
  pinMode(in2, OUTPUT);
  pinMode(pwmPin, OUTPUT);
}

void loop() {
  digitalWrite(in1, HIGH);
  digitalWrite(in2, LOW);
  analogWrite(pwmPin, 150);
  delay(2000);

  digitalWrite(in1, LOW);
  digitalWrite(in2, HIGH);
  analogWrite(pwmPin, 150);
  delay(2000);
}
```

### Results
- The motor spins forward for 2 seconds.
- Then it spins backward for 2 seconds.
- This demonstrates basic direction control.

## ESP32 Example

### Hardware Setup
- 1 x motor driver module
- 1 x DC motor
- ESP32 board
- Jumper wires
- External power supply

### ESP32 Code
```cpp
int in1 = 18;
int in2 = 19;
int pwmPin = 21;

void setup() {
  pinMode(in1, OUTPUT);
  pinMode(in2, OUTPUT);
  pinMode(pwmPin, OUTPUT);
}

void loop() {
  digitalWrite(in1, HIGH);
  digitalWrite(in2, LOW);
  analogWrite(pwmPin, 150);
  delay(2000);

  digitalWrite(in1, LOW);
  digitalWrite(in2, HIGH);
  analogWrite(pwmPin, 150);
  delay(2000);
}
```

### Results
- The motor changes direction automatically.
- This helps test motor control logic.

## Applications
- Robot cars and wheeled robots
- Conveyor systems
- Fan and pump control
- Simple automation projects
- Educational electronics experiments

## Troubleshooting
- If the motor does not move, check the power supply and wiring.
- If the motor runs weakly, verify the voltage rating.
- If the motor gets hot, reduce the load or lower the duty cycle.
- If the driver overheats, use a better power supply and ensure proper cooling.

## FAQ

### Frequently Asked Questions
- **Can I connect the motor directly to the microcontroller?**
  - No. A motor driver is recommended because motors need more current.

- **Can I change motor speed?**
  - Yes. Use PWM signals from the microcontroller.

- **Can the motor run in both directions?**
  - Yes, by changing the control signals.
