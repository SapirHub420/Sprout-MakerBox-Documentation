# Sprout Potentiometer

## Overview

<div style="display: flex; gap: 15px; justify-content: center;">
<img src="images/Potentionmeter.png" alt="Potentiometer" width="200">
</div>

The Sprout Potentiometer is a user-friendly variable resistor used to provide an adjustable analog voltage. Turn the knob to change the output voltage, which can be read by any analog input on the Sprout MakerBox baseboard.

---

## Description

A potentiometer is essentially a three-terminal device that acts as a voltage divider. As you rotate the shaft, the wiper moves along a resistive track, changing the ratio of resistance and therefore the voltage at the middle (wiper) pin.

Key points:
- Provides a continuous analog signal (not digital)
- Commonly used for user input: brightness, volume, position, or as a simple sensor
- Typical unit is 10 kΩ (check your module label for exact value)

---

## Pinout

- **VCC**: Connect to 3.3V or 5V (match your baseboard voltage)
- **GND**: Ground
- **OUT/WIPER**: Analog output that varies between 0V and VCC

---

## How it works (simple)

1. The potentiometer forms a voltage divider between VCC and GND.
2. The wiper outputs a voltage proportional to its position.
3. Your microcontroller reads that voltage on an analog input and converts it to a numeric value.

Formula: output voltage is between 0 and VCC proportionally to knob position.

---

## Reading values (example Arduino/Analog)

```cpp
// Example: read potentiometer on analog pin A0
int potPin = A0;

void setup() {
	Serial.begin(9600);
}

void loop() {
	int raw = analogRead(potPin);        // 0 - 1023 on 5V AVR boards
	float percent = raw / 1023.0 * 100;  // convert to 0 - 100%
	Serial.println(percent);
	delay(200);
}
```

Note: On a 3.3V board, analog range may be 0–4095 depending on ADC resolution; adapt the scaling accordingly.

---

## Applications

- User input (knobs for settings)
- Adjusting brightness, volume, or motor speed
- Manual calibration and tuning for prototypes

---

## Tips

- Use stable power (VCC) for consistent readings
- Add a small software low-pass filter or moving average to smooth jitter
- If you need a wide end-to-end range, choose the correct resistance value (10 kΩ is common)
- Protect the wiper from mechanical stress; avoid heavy sideways force

---

## Connection Guide

```
Potentiometer pins:
┌ VCC  (to 3.3V/5V)
├ WIPER (to analog input)
└ GND  (to ground)
```

---

## See Also

- [Sprout MakerBox Baseboard Documentation](../../flow.md)
- Other input components: [Button](Basic Input/button.md)

---

*Last Updated: July 2026*  
*Status: Simple wiki-style entry* 
