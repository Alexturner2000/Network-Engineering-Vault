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
2018 - 802.3bt (ammended) - Type 4 - 90 Watts - PoE++

### PoE Injector
A wall outlet device that inject the DC current into the ethernet cable

### PoE Splitter
If your equiptement has different power compatibility, you can use a PoE Splitter. This allows you to manually configure the output voltage.

---

Center Trapped Transformers

Lets say your transfering data at a rate of 125MHz or 1,250,000Hz. This input is applied to two transformers. Additionally, 48V is applied between the two transformers. 

[Illistration](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAsCmC0YCYQDYCcA6AzJSZMFYwAGSbMZfEfIqqJfOMMAKADcRZMEaFIbPu4AOzIQNCImpFp02jXnp8zPqIS8oADhAINWxFoUyCY9KjMn8AHQAORRQC4ImDk0ipCpoqhwUNmIkIuYG4e7kI++H4BHPjoyBqkuLrIRBqpRAiMkCDKRKrqYCLautr4oobSxnZmqBY2dviOIM6wdhka+KhpQkKYmLp8-SZEYN4jqGrIyP4jIoHwcWO+3tQaKQFwCBC5ogI0kFqwCGXgOmLDlZTV5mD2DfWKzRwIM2Aapn0aqMg4OEiu7jAnm8kF8-kCANC+HCoMi-i0Ow4XHERSOJ2O5QuRCqphud0UD0oLTaXm4AWhBE6iHc5XQ7U63V6-QS2KElFadNGfFGk2m0kKyECbCRgiYSD2mnOEmOMhkpyksvOCiUAHdnicxSBvuBEGJmGq0aIDiA0pKiPqOKaBdoCkVzQbtbweOonXrrMUtMadHpdRB5Mx3d7hKoSq6-Xr2LA+DwTlHZFwlVB9gYlYoLXGY7sMaVyuns9nDdpUnqDdnTYWE-b1aIExnmkhzQBzDjRnMt2QIIQNks27KmtTZSsWgf15oJUdVkfcLRTk6Tl0nfrZbPmgBOY8HSCXbfEMgt2s1I81VdNXvUxqrsCtqOz1svjr41e0j-NAHtaD8pWpUOJeDVdAg6DEEQ1DxFi4bOES4D+u+NCfr+CA-lAuI1PgOh8NwnYNnS-LgE8NDOEwervmoKDZPsXhaN8OGylsbIHJ04HaMxpGYMwQA)














