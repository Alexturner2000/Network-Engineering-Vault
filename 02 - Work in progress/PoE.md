# Power Over Ethernet (PoE)
tags: [[Poe]], [[Ethernet]], [[Layer 1]], [[UTP]], [[Separate Signaling]]

Power over Ethernet protocols allow power to be sent over ethernet without hindering the maximum transfer rate of data. In order to understand the transfer of power, it is also crucial to understand how Unshielded Twitted Pair [[UTP]] works on [[Ethernet]]. PoE uses [[Separate Signaling]] to its advantage. Phantom Powering allows power to be sent over data wires if all four pairs are used. There are two modes, common mode, used for injecting power, and differential mode, which transfers data. In common mode, one wire in a pair is negative, and the other is positive. This makes the average voltage almost zero. PoE injects DC power equally into the pair, and because it is all injected equally, there is no affect with the data signals.

### Why is power invisible to data

Early versions of PoE only used the 2 unused data pairs, while later versions utilized all four

1 - Data
2 - Data
3 - Data
4 - Power
5 - Power
6 - Data
7 - Power
8 - Power

It runs using [[DC]] power (commonly 48V). 

### Active PoE
When connected to an end device, PoE determins the power compatibiltiy and comunitcate with the device to determin the correct amount of power to transmit.

### Passive PoE
Sends a constant power to the end device without any sort of negotiation

2003 - 802.3af - Type 1 - 15.4 Watts - PoE
2009 - 802.3at - Type 2 - 30 Watts - PoE+
2011- 802.3bt - Type 3 - 60 Watts - 4PPoE (4 pair power over ethernet)
2018 - 802.3bt (ammended) - 90 Watts
