# Introduction
This a project in Udacity Advanced Embedded Systems provided by EgFwd.

In the automotive industry, ECUs are communicating together to provide safety and driver's comfort.

ECUs are microcontrollers connected with input and output devices. input devices to sense the surrounding environments, and output devices to perform actions according to readings that came from input devices.

## Project Requirements

Provide a fully static design and a fully dynamic design for two ECUs communicating together to control car lights according to door state, light switch state, and car speed state.

### Hardware requirements:

Two microcontrollers connected via CAN bus
- One Door sensor (D)
- One Light switch (L)
- One Speed sensor (S)
- ECU 1 connected to D, S, and L, all input devices
- Two lights, right (RL) and left (LL)
- One buzzer (B)
- ECU 2 connected to RL, LL, and B, all output devices
### Software requirements:

- ECU 1 will send status messages periodically to ECU 2 through the CAN protocol
- Status messages will be sent using Basic Communication Module (BCM)
- Door state message will be sent every 10ms to ECU 2
- Light switch state message will be sent every 20ms to ECU 2
- Speed state message will be sent every 5ms to ECU 2
- Each ECU will have an OS and application SW components
- If the door is opened while the car is moving → Buzzer ON, Lights OFF
- If the door is opened while the car is stopped → Buzzer OFF, Lights ON
- If the door is closed while the lights were ON → Lights are OFF after 3 seconds
- If the car is moving and the light switch is pressed → Buzzer OFF, Lights ON
- If the car is stopped and the light switch is pressed → Buzzer ON, Lights ON
