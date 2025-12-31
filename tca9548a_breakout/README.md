# tca9548a_breakout

Breakout for the TI TCA9548A 8-channel I2C switch/multiplexer. It lets a single
I2C master select one of eight downstream buses to integrate multiple identical
I2C sensors with fixed addresses. Address jumpers (A0-A2) set the mux address,
on-board pullups support SDA/SCL, and a RESET header allows recovery from bus
lockups.

Use cases include:
- Ring-mounted time-of-flight modules
- Redundant IMUs and navigation stacks
- Distributed environmental sensors
- Multi-sensor robotics or payload testbeds

Headers expose VCC/GND, upstream SDA/SCL, and the eight switched channels.
