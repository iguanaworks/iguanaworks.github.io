---
title: "Serial Transceiver"
date: 2017-05-23
coverImage: "images/Serial-Transceiver-310x310.jpg"
---

We’ve designed a small board that acts as an IR receiver and a high-powered transmitter. It’s small and light enough to hang off of a serial port, doesn’t need batteries, and has a transmit range on the order of 10 meters.

## How does it work?

Instead of using an external power supply or battery, we use a large capacitor that charges slowly off one of the serial port’s signal lines. Since IR transmissions have a fairly low duty cycle, enough charge accumulates over time to transmit at high power.

Here’s the [schematic](images/serial-schematic.pdf). No, the value of C1 is not a typo. It’s 0.33F, one-third of a Farad, sort of like a small battery. We use the Panasonic EEC-S0HD334V, which you can buy for about $1.50. Note: if you substitute a TSAL 6100 for the 6400 shown, you get a longer range but a narrower transmit angle.

When you plug in the board, the receiver works immediately. The transmitter takes about 15 minutes to reach a minimum charge level before you can use it. You only have to wait the first time; the capacitor holds its charge for a long time after it’s unplugged. The capacitor will reach maximum charge in about an hour, and once it’s charged up, the transmit range is about 10 meters. If you hold the transmit command on continuously for ten minutes or so, the range will gradually reduce to about 5 meters and then level off (the charge and discharge rates are about even at that point). As soon as you stop transmitting, the capacitor will recharge and bring the range back up. If you only transmit occasionally (once every few seconds, say), the range should stay near the maximum.

This circuit requires an input voltage of only 5.5V, so it works fine with laptop serial ports that don’t put out the full 12V. It has a peak current draw of about 3mA to 4mA. That’s actually less than the continuous draw of the simple receive-only circuit described on the [LIRC](http://www.lirc.org/) page, since we used a voltage regulator that’s more efficient than the 78L05 at low currents.

To get things a bit smaller, we printed up some PCBs for this circuit. Here’s the [Layout](images/serial-layout.pdf). The board is 1.3 inches long and the same width as a 9-pin serial connector.
