# BJT N-channel MOSFET Gate Driver

## Description

A simple gate driver for a N-Channel MOSFET that is to be used for switching 
applications where the input signal is low in current and voltage.

A common usage would be driving a mosfet tor the correct voltage to the gate
from a micro-controller.

## Ratings

**Bypass Capacitors:** C1/C2

Capacitors should be chosen depending on the expected layout and input 
frequencies.

If unsure the default values of 0.1uF and 10uF are good starting points.

## Design Recommendations

Choose components for the transistors that can handle the needed gate voltage
while also working at the expected switching frequency.

## Layout Recommendations

N/A
