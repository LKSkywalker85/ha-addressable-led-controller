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

The code so far after flashed it to an ESP via ESP Home Builder in HA:
- New lamp that you can control in HA
- effects will be covered by the ESP
- You will have a dropdown menu for the orientation of the stripe to adjust the wipe on/off effect
- you can choose the number of LED's your physical stripe is capable off -> all effects will adjust to this number
- create your own effects
  
