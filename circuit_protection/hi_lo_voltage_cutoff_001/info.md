# High/Low Voltage Cutoff

## Description

A window comparator for low-voltage DC systems. This circuit allows the output
to be at logic low outside the voltage window which is set by the two resistor
voltage dividers.

This circuit can be used for applications like low/high voltage protection of
battery packs, as well as for temperature protection.

One thing to keep in mind is that the input offset voltage of the IN+/- pins
for the standard LM393 is 5mV maximum.

## Ratings


*Input Voltage:* 2.0V ~ 36V
*Output Voltage:* 0.0V(LOW) ~ V-supply(HIGH)
*Input Bias Current(LM393):* 25nA
Minimum Current:
Maximum Current:

The error for this circuit assuming the worst case can be calculated taking the
following formula for each comparator channel.


Thevenin Resistance = Vin * (R2) / (R1 + R2)

Voltage Error Total = Input offset voltage + Input bias current * resistance


### Example 001

In this example assume it's a Li-Ion 2S1P pack where cell voltage can range 
from 2.0V~4.2V normally.

For this example we're trying to keep the pack voltage within 5.0v ~ 8.2v 
which under ideal circumstances should give a cell voltage range of 2.5V to 
4.1V on the upper end.

We're going to assume a reference voltage of 2.5V as we can get that by default
from many voltage references.

Given the error of:
Verr_Ib = R1+R2 * Ib = 10kOhm * 25nA = 0.25mV = 250uV
Verr_total = Vos + Verr_Ib * scale-factor
Verr_total = 5mV + 250uV * scale-factor.

I_div_high = 8.2V / 10kOhm = 820uA
Vr1hi = 5.7V
Vr2hi = 2.5V
R1 = 5.7V / 820uA = 6.9512kOhm
R2 = 2.5V / 820uA = 3.0487kOhm

I_div_low = 5.0V / 10kOhm = 500uA
Vr3lo = 2.5V 
Vr4lo = 2.5V
R3 = 5kOhm
R4 = 5kOhm


VIN:: Ranging from say 4.0V~8.4V
VREF:: 2.5V
R1:: Voltage divider 1, top resistor.
R2:: Voltage divider 1, bottom resistor.
R3:: Voltage divider 1, top resistor.
R4:: Voltage divider 1, bottom resistor.



R_total_high = R1 + R2
R_total_low = R3 + R4



## Design Recommendations

The resistor's used in the input voltage dividers should be at least 1% 
tolerance in order to make sure it's somewhat accurate.



## Layout Recommendations

N/A
