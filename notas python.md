# Python Notes

This repo part will have some generic things that might be helpfull to others.

## 2025-04 - PyVISA issues

### Agilent(HP) 34420A multimeters

When using PyVISA and old multimeters (Agilent, HP) it turns out that some commands will work and others will not:

* does not work in python: ' "MEAS:VOLT:DC? AUTO,MIN,(@1)" ', but works in National Instruments MAX (using interactive communication)
* it works in python: 'READ?', also in MAX

SOLUTIONS:

In my case the use of a specific terminator solved the problem, so when calling the instrument make sure to include a terminator:

'''python
    def connect(self):
        rm = pyvisa.ResourceManager()
        self.instrument = rm.open_resource(self.resource_name)
        self.instrument.read_termination = '\n'
        self.instrument.write_termination = '\n'
        self.instrument.timeout = 5000
        print(f"Connected to Multimeter 3458A: {self.instrument.query('*IDN?')}")
'''

## Python issues

2024-04

An issue started happening a month ago on CONDA. Both in my work and home pc: I could not install packages using CONDA, I was able to do it on PIP,
but that means that if I create a new ENV I could not install PIP either.

The error was:
_Conda SSL Error: OpenSSL appears to be unavailable on this machine. OpenSSL is required to download and install packages_

The solution I followed was:
https://github.com/conda/conda/issues/11982#issuecomment-1285538983
