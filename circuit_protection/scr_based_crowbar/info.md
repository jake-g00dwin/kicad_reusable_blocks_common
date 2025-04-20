# SCR based crowbar

## Description

The crowbar circuit depends on the Zener diode's breakdown voltage to trigger
the SCR into shorting the Vin to ground, which in turn blows the fuse F1.


## Ratings

**Fuse:** F1
The selected fuse depends on your application, you may find that inrush current
for some applications rules out the use of a fast blow fuse of too low of a 
current rating.

**Zener Diode:** D1
Select a value for the Zener diode that approximately 1V above desired Vout 
voltage level.

**SCR:** D2
The SCR gate voltage should be lower than the Zener diode breakdown voltage
for it to correctly trigger.

**Snubber Cap:** C2
A commonly used value is 47uF, it's here to prevent false triggering and to 
soak up voltage spikes from switching.

**Filter Cap:** C1
This is optional, but common when taking power into a board/circuit from an
external source or power supply.

## Design Recommendations

I recommend first selecting the appropriate voltage and current for your 
application.

Once those values are known select the closest fuse and then use an SCR with 
an I^2t rating larger than the maximum expected fuse current AT MINIMUM!

Selecting a high value SCR is a good idea as you shouldn't depend on the SCR
failing shorted.

A value 20x greater than the fuse value is a more than reasonable rule of 
thumb.


## Layout Recommendations

N/A
