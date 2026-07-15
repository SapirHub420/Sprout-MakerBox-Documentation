# SprouT LCD

## Overview
The **SprouT LCD** is an output display module used to show text, numbers, and simple messages in electronics projects. It is very useful when you want a project to display information such as temperature, status, time, or sensor values.

It is commonly used in beginner projects, learning boards, and small embedded systems because it gives a clear visual output.

---

## Description
The LCD (Liquid Crystal Display) shows information by controlling pixels on the screen. A typical module can display characters on one or more rows.

This display is often used to:
- Show sensor readings
- Display system status
- Create simple user interfaces
- Show messages and warnings
- Build educational electronics projects

---

## Features
- Shows text and numbers clearly
- Easy to use in beginner projects
- Works well with Arduino and ESP32
- Can display sensor values and messages
- Useful for monitoring and feedback systems

---

## Specifications
| Item | Description |
|---|---|
| Display Type | Character LCD |
| Common Size | 16x2 or 20x4 depending on module |
| Operating Voltage | Usually 5V |
| Control Type | Digital signal through controller pins |
| Common Use | Display text, values, and status |
| Compatible Boards | Arduino, ESP32, SprouT MakerBox baseboard |

---

## Pinout
A typical LCD module has several pins. The exact pin names may vary depending on the model.

| Pin | Function | Description |
|---|---|---|
| VSS | Ground | Connect to GND |
| VDD | Power | Connect to 5V |
| V0 | Contrast | Used to adjust screen contrast |
| RS | Register Select | Selects command or data mode |
| RW | Read/Write | Usually connected to GND for writing |
| E | Enable | Enables data transfer |
| D4-D7 | Data Pins | Used for sending data |
| A | Anode | Backlight positive |
| K | Cathode | Backlight negative |

---

## Plug and Play with SprouT Baseboard
The SprouT MakerBox baseboard can be used with an LCD module when connected properly.

### Step 1: Turn off the power
Before connecting the LCD, switch off the baseboard power.

### Step 2: Locate the control pins
Find the digital pins needed for RS, E, and data pins on the baseboard.

### Step 3: Connect the module
Connect the LCD to the board using the appropriate wiring:

| LCD Pin | Connection |
|---|---|
| VSS | GND |
| VDD | 5V |
| V0 | Potentiometer or contrast control |
| RS | Digital pin |
| RW | GND |
| E | Digital pin |
| D4-D7 | Digital pins |
| A | 5V |
| K | GND |

### Step 4: Power on the baseboard
Turn the power back on after checking all connections.

### Step 5: Load the display code
Use Arduino or ESP32 code to send text to the display.

---

## How It Works
The LCD receives commands and character data from the microcontroller. The controller inside the display processes the incoming signals and shows the correct text on the screen.

In simple terms:
- The microcontroller sends commands to control the display.
- The display shows letters, numbers, or symbols.
- The screen can be updated as the program runs.

---

## Arduino Example

### Hardware Setup
Required components:
- Arduino board
- LCD module
- Potentiometer for contrast
- Jumper wires

Wiring example:
- LCD RS -> D12
- LCD E -> D11
- LCD D4 -> D5
- LCD D5 -> D4
- LCD D6 -> D3
- LCD D7 -> D2

### Arduino Code
```cpp
#include <LiquidCrystal.h>

LiquidCrystal lcd(12, 11, 5, 4, 3, 2);

void setup() {
  lcd.begin(16, 2);
  lcd.print("SprouT LCD");
}

void loop() {
  lcd.setCursor(0, 1);
  lcd.print("Hello World");
  delay(1000);
  lcd.setCursor(0, 1);
  lcd.print("                ");
  delay(1000);
}
```

### Results
The LCD will show the message "SprouT LCD" on the first line and "Hello World" on the second line.

---

## ESP32 Example

### Hardware Setup
Required components:
- ESP32 board
- LCD module
- Potentiometer
- Jumper wires

Wiring example:
- LCD RS -> GPIO13
- LCD E -> GPIO14
- LCD D4 -> GPIO26
- LCD D5 -> GPIO27
- LCD D6 -> GPIO25
- LCD D7 -> GPIO33

### ESP32 Code
```cpp
#include <LiquidCrystal.h>

LiquidCrystal lcd(13, 14, 26, 27, 25, 33);

void setup() {
  lcd.begin(16, 2);
  lcd.print("ESP32 LCD");
}

void loop() {
  lcd.setCursor(0, 1);
  lcd.print("Hello ESP32");
  delay(1000);
  lcd.setCursor(0, 1);
  lcd.print("           ");
  delay(1000);
}
```

### Results
The LCD will display text on the screen and update it repeatedly.

---

## Applications
- Sensor display projects
- Stopwatch and timer systems
- Temperature and humidity monitors
- Smart home status panels
- Educational electronics demos
- Data display for small embedded systems

---

## Troubleshooting
- If nothing appears, check the power and ground connections.
- If the screen is blank, adjust the contrast using the potentiometer.
- If text looks incorrect, confirm that the data pins are connected properly.
- If the display flickers, use a stable power supply.

---

## FAQ
### Frequently Asked Questions

**Can I use the LCD with Arduino?**
Yes. The LCD works well with Arduino boards.

**Can I use the LCD with ESP32?**
Yes. ESP32 can also control the display.

**Do I need a library?**
Yes. The LiquidCrystal library is commonly used for Arduino-based LCD projects.

**Can I display sensor values?**
Yes. The LCD is often used to show sensor readings such as temperature or humidity.

---

*Last Updated: July 2026*
*Status: Wiki-style component documentation*
