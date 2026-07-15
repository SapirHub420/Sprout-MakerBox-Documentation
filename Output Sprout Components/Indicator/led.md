# SprouT LED

## Overview

<p align="center">
  <img src="images/LED Blue.png" alt="LED Blue" width="190">
  <img src="images/LED Green.png" alt="LED Green" width="190">
  <img src="images/LED Red.png" alt="LED Red" width="190">
  <img src="images/LED White.png" alt="LED White" width="190">
  <img src="images/LED Yellow.png" alt="LED Yellow" width="190">
</p>

The **SprouT LED** is a simple output component used to show status, create light effects, or indicate activity in a project. It is one of the easiest components to learn in electronics because it can be controlled directly by a microcontroller.

It is commonly used in beginner projects such as blinking lights, alarms, indicators, and visual feedback systems.

---

## Description
The LED (Light Emitting Diode) emits light when current flows through it. It is often used to show whether a device is ON, OFF, or performing a certain action.

LEDs can be used in many ways, including:
- Power indicators
- Warning lights
- Button feedback
- Animation effects
- Smart device status signals

---

## Features
- Simple and easy to use
- Low power consumption
- Bright visual output
- Works well with Arduino and ESP32
- Can be used for blinking, timing, and alert systems

---

## Specifications
| Item | Description |
|---|---|
| Component Type | Light output module |
| Operating Voltage | Usually 3.3V or 5V depending on the module |
| Control Type | Digital signal |
| Common Use | Indicators, alerts, lighting effects |
| Compatible Boards | Arduino, ESP32, SprouT MakerBox baseboard |

---

## Pinout
A typical LED module may have 2 or 3 pins.

| Pin | Function | Description |
|---|---|---|
| VCC | Power | Connect to 3.3V or 5V |
| GND | Ground | Connect to GND |
| SIG / I/O | Signal | Connect to a digital output pin |

---

## Plug and Play with SprouT Baseboard
The SprouT MakerBox baseboard makes it easy to connect the LED module.

### Step 1: Turn off the power
Before connecting the LED, switch off the baseboard power to avoid wiring mistakes.

### Step 2: Locate the output port
Find an available digital output pin on the baseboard.

### Step 3: Connect the module
Connect the LED module to the baseboard:

| LED Module | SprouT Baseboard |
|---|---|
| VCC / + | VCC / + |
| GND / - | GND / - |
| SIG / I/O | Digital output pin |

### Step 4: Power on the baseboard
Turn the power back on after confirming the connections.

### Step 5: Control the LED
The microcontroller can turn the LED ON or OFF using code.

---

## How It Works
The LED lights up when the microcontroller sends a HIGH signal to the output pin. When the signal becomes LOW, the LED turns off.

In simple terms:

```text
HIGH = LED ON
LOW = LED OFF
```

This makes the LED useful for blinking, status display, and warning notifications.

---

## Arduino Example

### Hardware Setup
Required components:
- Arduino board
- LED module
- Jumper wires

Wiring:
- LED VCC -> 5V
- LED GND -> GND
- LED SIG -> D8

### Arduino Code
```cpp
#define LED_PIN 8

void setup() {
  pinMode(LED_PIN, OUTPUT);
}

void loop() {
  digitalWrite(LED_PIN, HIGH);
  delay(500);
  digitalWrite(LED_PIN, LOW);
  delay(500);
}
```

### Results
The LED will blink ON and OFF every half second.

---

## ESP32 Example

### Hardware Setup
Required components:
- ESP32 board
- LED module
- Jumper wires

Wiring:
- LED VCC -> 3.3V
- LED GND -> GND
- LED SIG -> GPIO2

### ESP32 Code
```cpp
#define LED_PIN 2

void setup() {
  pinMode(LED_PIN, OUTPUT);
}

void loop() {
  digitalWrite(LED_PIN, HIGH);
  delay(500);
  digitalWrite(LED_PIN, LOW);
  delay(500);
}
```

### Results
The LED will blink repeatedly, showing that the ESP32 is controlling the output correctly.

---

## Applications
- Status indicators
- Alarm systems
- Button press feedback
- Visual notifications
- Simple animations
- Learning digital output control

---

## Troubleshooting
- If the LED does not light up, check the power and ground connections.
- If the LED stays off, confirm that the correct digital pin is used in the code.
- If the LED is very dim, make sure the wiring is secure and the module is powered properly.

---

## FAQ
### Frequently Asked Questions

**Can I use the LED with Arduino?**
Yes. The LED can be connected to any digital output pin on Arduino.

**Can I use the LED with ESP32?**
Yes. It works well with ESP32 digital pins.

**Do I need a resistor?**
Some LED modules already include a resistor. If you are using a bare LED, a resistor is usually needed.

**Can I make the LED blink?**
Yes. You can control blinking with simple delay commands in the code.

---

*Last Updated: July 2026*
*Status: Wiki-style component documentation*
