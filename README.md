# ha-addressable-led-controller
Control addressable LED strips in Home Assistant like a normal light while keeping the LED logic on the ESP.
## Concept

Home Assistant can control addressable LED strips, but sometimes you want more flexibility than the standard integration provides.

This project uses a simple but powerful idea:

A **virtual light entity in Home Assistant** controls a **physical addressable LED strip running on an ESP device**.

This allows the strip to behave like a normal Home Assistant light while keeping the LED logic on the microcontroller.

Advantages:

- Works like a normal light inside Home Assistant
- Custom LED effects can run directly on the ESP
- The ESP keeps full control of the LED strip logic
- Easily extendable with new effects and behaviors


## Example

The included example implements a simple **wipe on/off effect**.

When the light turns on, the strip fills gradually.  
When it turns off, the strip fades out in reverse order.

This is only meant as a demonstration of the concept.


## Community Project

This repository is intended as a **starting point for experimentation**.

The architecture allows much more advanced features, such as:

- advanced LED effects
- segment-based control
- individual LED logic
- automation-triggered animations

Originally the project aimed to support configurable LED count and orientation from Home Assistant, but this could not be implemented cleanly with the current ESPHome limitations.

If someone finds a better solution, contributions are very welcome.


## Hardware used for testing

- ESP32-C6 DevKit
- WS2812 addressable LED strip
- ESPHome
- Home Assistant

Other ESP boards and addressable LED strips should work as well.
