===============================
MinimalModbus
===============================

Easy-to-use Modbus RTU, Modbus ASCII, and Modbus TCP implementation for Python.

**Documentation**: https://minimalmodbus.readthedocs.io

Features
--------
MinimalModbus is an easy-to-use Python module for talking to instruments (slaves)
from a computer (master) using the Modbus protocol, and is intended to be running on the master.
The only dependence is the pySerial module (also pure Python).

There are convenience functions to handle floats, strings and long integers
(in different byte orders).

This software supports the 'Modbus RTU' and 'Modbus ASCII' serial communication and 'Modbus TCP' over a socket connection (e.g. Ethernet).

This package is intended for use on Linux, macOS and Windows platforms.
It is open source, and released under the Apache License, Version 2.0.

For Python 3.8 and later. Tested with Python 3.8, 3.9, 3.10, 3.11 and 3.12.

This package uses semantic versioning.

## Modbus TCP support

You can communicate with TCP-enabled devices by passing a socket URL as the port address.

.. code-block:: python

    import minimalmodbus
    instrument = minimalmodbus.Instrument(
        port="socket://192.168.20.200:502",
        slaveaddress=1,
    )
