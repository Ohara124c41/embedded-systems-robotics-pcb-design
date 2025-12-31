# watchdog_tpl5010

Low-power watchdog timer circuit based on the TI TPL5010. It periodically
asserts WAKE to a host system and expects a DONE pulse in return. If DONE is
missing within the programmed interval, the circuit drives RESET_OUT to recover
the host. This provides an independent supervision path for hung or deadlocked
MCUs; the interval is set by the DELAY/M_RST resistor and a pushbutton allows
manual reset.

Use cases include:
- Robotics controllers and real-time embedded nodes
- Fielded industrial devices in harsh conditions
- Small satellite subsystems needing autonomous recovery
- Remote sensors that must survive software lockups

Connector exposes VCC, RESET_OUT, DONE, WAKE, and GND for easy integration.
