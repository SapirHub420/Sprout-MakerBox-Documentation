# Relay

## Overview
- A relay is an electrically controlled switch used to turn devices on and off.
- It is useful when a microcontroller needs to control a higher-power device.
- Relays are often used in home automation, safety systems, and simple control projects.

## Description
- A relay uses a small electromagnetic coil to move a switch.
- When current flows through the coil, the internal contacts change state.
- This allows a low-power signal to control a higher-power circuit.

## Features
- Electrically isolated control and load circuits
- Can switch higher-voltage devices safely
- Useful for turning on lamps, fans, or motors
- Works well with Arduino and ESP32 projects

## Specifications
- Type: Electromechanical relay
- Control voltage: typically 5V depending on module
- Contact type: normally open (NO) and normally closed (NC) options
- Load voltage: depends on the relay rating
- Switching current: depends on the relay model

## Pinout
- **VCC**: Power input for the relay coil
- **GND**: Ground connection
- **IN / SIG**: Control signal from the microcontroller
- **NO**: Normally open contact
- **NC**: Normally closed contact
- **COM**: Common contact

## Plug and Play with Sprout Baseboard
- The relay can be connected to the Sprout baseboard through the correct control and power pins.
- Make sure the external load voltage is within the relay rating.
- Always power the relay module correctly before connecting the load.
- For safety, do not connect mains voltage unless you are experienced and using proper isolation.

## How It Works
- The microcontroller sends a signal to the relay module.
- The relay coil becomes energized.
- The switch inside the relay moves from one contact to another.
- This opens or closes the load circuit.

## Arduino Example

### Hardware Setup
- 1 x relay module
- Arduino board
- LED or small lamp
- Jumper wires
- Power supply

### Arduino Code
```cpp
int relayPin = 8;

void setup() {
  pinMode(relayPin, OUTPUT);
}

void loop() {
  digitalWrite(relayPin, HIGH);
  delay(2000);
  digitalWrite(relayPin, LOW);
  delay(2000);
}
```

### Results
- The relay turns on for 2 seconds.
- Then it turns off for 2 seconds.
- This shows how a relay can control an external device.

## ESP32 Example

### Hardware Setup
- 1 x relay module
- ESP32 board
- LED or small lamp
- Jumper wires
- Power supply

### ESP32 Code
```cpp
int relayPin = 18;

void setup() {
  pinMode(relayPin, OUTPUT);
}

void loop() {
  digitalWrite(relayPin, HIGH);
  delay(2000);
  digitalWrite(relayPin, LOW);
  delay(2000);
}
```

### Results
- The relay toggles on and off automatically.
- This demonstrates basic relay control.

## Applications
- Home automation
- Lamp and fan switching
- Small appliances
- Alarm systems
- Educational electronics projects

## Troubleshooting
- If the relay does not switch, check the control signal and power supply.
- If the relay clicks but the load does not respond, verify the load wiring.
- If the relay becomes hot, reduce the load or check the contact rating.
- Always confirm that the connected device is within the relay's rated limits.

## FAQ

### Frequently Asked Questions
- **Can a relay control high-voltage devices?**
  - Yes, but only if the relay and wiring are rated for that voltage and used safely.

- **Is a relay the same as a transistor?**
  - No. A relay is an electromechanical switch, while a transistor is a semiconductor switch.

- **Can I use a relay with Arduino?**
  - Yes. A relay module can be controlled easily with a digital output pin.
