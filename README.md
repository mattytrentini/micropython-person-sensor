# MicroPython Person Sensor

This is a [MicroPython](https://micropython.org/) driver for the [usefulsensors Person Sensor](https://usfl.ink/ps).

This is a port of [dupontgu's person-sensor-circuitpython repo](https://github.com/dupontgu/person-sensor-circuitpython).

## Installation

```bash
mpremote mip install github:org/mattytrentini/micropython-person-sensor
```

## Usage

```python
from machine import I2C
from person_sensor import PersonSensor

i2c = I2C(1)  # Will need an I2C instantiation that matches your device
ps = PersonSensor(i2c)  # Configure person sensor
# There are many methods, but retrieving a list of detected faces will be the main one
faces = ps.get_faces()
for face in faces:
    print(face)
```
