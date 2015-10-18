## Eagle schematics and board files for Detectino hardware

These are design files for two piggy back boards used in the Detectino Alarm project.

### Detectino_nodcdc
This is an expansion board used to read analog and digital inputs from commercial
alarm sensors and provide readings over a shared CAN bus.

The core is an Arduino Nano. The board provides protection for analog
and digital signals, in order to harden Arduino inputs and a CAN bus
transceiver.

Each board can handle 8 analog sensors and 3 digital ones.

Multiple boards can be connected over a single CAN bus.

### Detectino_raspi
This is the "core" board, which is a piggy back for RaspberryPi B+,
which provides isolated CAN bus and isolated power supply using
a suitable DC-DC converter.

The board is completely isolated from the environment, in order
to protect the RaspberryPi where the core software runs and
avoid disruption of the service caused by external electrical factors.

This board is plugged in the same CAN bus and communicate with
the Detection expansion boards-

#### Warning!
I'm not an electronic expert at all, so I tried to understand
and do my best in designing these boards.
If someone finds any error or have suggestions, please tell!

##### Notes
The other folders are initial design of the Arduino piggy back board,
not realized in practice.

