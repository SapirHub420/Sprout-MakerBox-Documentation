# SprouT Buzzer

## Overview

<p align="center">
  <img src="images/LED Blue.png" alt="LED Blue" width="200">
  <img src="images/LED Green.png" alt="LED Green" width="200">
  <img src="images/LED Red.png" alt="LED Red" width="200">
  <img src="images/LED White.png" alt="LED White" width="200">
  <img src="images/LED Yellow.png" alt="LED Yellow" width="200">
</p>

The **SprouT Buzzer** is an output module that makes sound. It is often used to give a warning, confirm a button press, or show that a system is running.

It is a very common component in beginner electronics projects because it is simple to connect and easy to control.

Common project examples include:

- Alarm system
- Button press alert
- Timer warning
- Robot warning sound
- Smart home notification
- Fun sound effect project

---

## Description

A buzzer turns electrical signals into sound. When the microcontroller sends a signal, the buzzer produces a beep or buzzing sound.

There are two common types:

| Type | Description |
|---|---|
| Active buzzer | Makes sound with a steady power signal |
| Passive buzzer | Needs a changing signal to make different tones |

For beginner projects, an active buzzer is usually easier to use.

---

## Important Note

This buzzer is suitable for learning, prototyping, and simple alert systems.

It is not meant to replace a loud industrial alarm or a certified warning device.

---

## Main Features

- Makes sound for alerts and notifications
- Easy to connect with SprouT baseboard
- Works with Arduino and ESP32
- Can be controlled with a digital pin
- Useful for alarms, timers, and feedback

---

## Typical Specifications

| Item | Description |
|---|---|
| Module Type | Sound output module |
| Output | Beep or buzzing sound |
| Operating Voltage | Usually 3.3V or 5V |
| Control Type | Digital signal |
| Common Use | Alarms, warnings, sound feedback |
| Compatible Boards | Arduino, ESP32, SprouT MakerBox baseboard |

---

## Pinout

A typical buzzer module may have 2 or 3 pins.

### 2-Pin Version

| Pin | Function | Description |
|---|---|---|
| + | Power | Connect to VCC |
| - | Ground | Connect to GND |

### 3-Pin Version

| Pin | Function | Description |
|---|---|---|
| VCC | Power | Connect to 3.3V or 5V |
| GND | Ground | Connect to GND |
| I/O / SIG | Signal | Connect to a digital output pin |

---

## Plug and Play with SprouT Baseboard

The SprouT MakerBox baseboard makes it easy to connect this module.

### Step 1: Turn off the power

Before connecting the buzzer, turn off the baseboard power.

This helps prevent wiring mistakes.

---

### Step 2: Locate the output port

Find the output port on the SprouT baseboard.

Use a digital output pin for the buzzer signal.

---

### Step 3: Connect the buzzer

Connect the buzzer to the baseboard.

Typical connection:

| Buzzer | SprouT Baseboard |
|---|---|
| VCC / + | VCC / + |
| GND / - | GND / - |
| I/O / SIG | Digital output pin |

---

### Step 4: Power on the baseboard

After checking the wires, turn the power back on.

---

### Step 5: Control the buzzer

The microcontroller can turn the buzzer on or off with code.

You can also make simple tones using the buzzer.

---

## How It Works

The buzzer works by receiving an electrical signal from the microcontroller.

When the signal is HIGH, the buzzer turns on. When the signal is LOW, it turns off.

For simple projects:

```text
HIGH = buzzer ON
LOW  = buzzer OFF
```

For sound effects or melodies, you can use different frequencies.

---

## Arduino Example

```cpp
/*
  SprouT Buzzer Test
  Board: Arduino Uno / Nano

  Connection:
  Buzzer VCC -> 5V
  Buzzer GND -> GND
  Buzzer SIG -> D8
*/

#define BUZZER_PIN 8

void setup() {
  pinMode(BUZZER_PIN, OUTPUT);
}

void loop() {
  digitalWrite(BUZZER_PIN, HIGH);
  delay(500);
  digitalWrite(BUZZER_PIN, LOW);
  delay(500);
}
```

---

## Example Application: Button Alert

This example makes the buzzer sound when a button is pressed.

```cpp
#define BUZZER_PIN 8
#define BUTTON_PIN 7

void setup() {
  pinMode(BUZZER_PIN, OUTPUT);
  pinMode(BUTTON_PIN, INPUT_PULLUP);
}

void loop() {
  if (digitalRead(BUTTON_PIN) == LOW) {
    digitalWrite(BUZZER_PIN, HIGH);
  } else {
    digitalWrite(BUZZER_PIN, LOW);
  }
}
```

---

## Troubleshooting

### Problem: No sound

Possible causes:

- Wrong pin selected
- No power connection
- Loose wire
- Buzzer connected to the wrong side

Solution:

- Check VCC and GND
- Make sure the signal pin is correct
- Try a different digital pin

---

### Problem: Buzzer is always on

Possible causes:

- The code keeps the pin HIGH
- The pin is set as OUTPUT but not controlled properly

Solution:

- Check the code
- Make sure the buzzer pin is switched off after the delay

---

### Problem: Sound is weak

Possible causes:

- Low voltage supply
- Weak power source
- Buzzer type is not suitable for the project

Solution:

- Use a stable power supply
- Try a different buzzer module
- Check the wiring again

---

## FAQ

### Can I use it with ESP32?

Yes. Connect the buzzer to any digital output pin.

---

### Can I make different tones?

Yes. Passive buzzers can make different tones, and active buzzers usually make a simple beep.

---

### Do I need a resistor?

Usually no. Most buzzer modules can be connected directly to a digital pin and power supply.

---

### Can I use it as an alarm?

Yes. It is great for simple warning sounds and beginner alarm projects.

---

## See Also

- [SprouT LED](led.md)
- [SprouT Relay](../Power/relay.md)
- [SprouT Liquid Crystal Display](liquidcystaldisplay.md)

---

*Last Updated: July 2026*
*Status: Wiki-style component documentation*
