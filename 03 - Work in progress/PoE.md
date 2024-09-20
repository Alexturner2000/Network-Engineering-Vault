# Power Over Ethernet (PoE)
tags: [[PoE]], [[Ethernet]], [[Layer 1]], [[UTP]], [[Separate Signaling]], [[Electrical]]

Power over Ethernet allows a power and data to be transferred simultaneously over an ethernet cable. It has two methods of sending power. **Phantom Powering** is the term used when power and data pulses can be sent over the same copper cable pair. There is also **Spare Pair Powering**, which sends power strictly over one pair, without data pulses. The data pulses will have their own individual cable pairs 

There are two modes, 
1. common mode - used for injecting power
2. differential mode - which transfers data. 
Power in the ethernet cable is DC, whereas the data is being transferred in AC. The DC is injected into the coper cable with the use of Center Tapped Transformers, which allows both data and current to reach their destination. 



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
When connected to an end device, PoE determines the power compatibility and communicate with the device to determine the correct amount of power to transmit.

### Passive PoE
Sends a constant power to the end device without any sort of negotiation

## IEEE Standards

| Type   | IEEE Standard     | Year | Name  | Capacity   | Modes     |
| ------ | ----------------- | ---- | ----- | ---------- | --------- |
| Type 1 | 802.3af           | 2003 | PoE   | 15.4 Watts | All, A, B |
| Type 2 | 802.3at           | 2009 | PoE+  | 30 Watts   | All, A, B |
| Type 3 | 802.3bt           | 2011 | 4PPoE | 60 Watts   | All       |
| Type 4 | 802.3bt (amended) | 2018 | PoE++ | 90 Watts   | All       |

## Other 
### PoE Injector
A wall outlet device that inject the DC current into the ethernet cable
### PoE Splitter
If your equipment has different power compatibility, you can use a PoE Splitter. This allows you to manually configure the output voltage.

---

Center Trapped Transformers



Explanation of the illustration:
For power transmission to work, there needs to be a copper pair. In the top right, we have a data transfer rate of 125MHz AC with a Vmax of 125MV and current of -230kA. This runs into the center Trapped Transformer, as well as our PoE power source, which is 48V and 48mA. 

[Illistration](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAsCmC0YCYQDYCcA6AzJSZMFYwAGSbMZfEfIqqJfOMMAKADcRZMEaFIbPu4AOzIQNCImpFp02jXnp8zPqIS8oADhAINWxFoUyCY9KjMn8AHQAORRQC4ImDk0ipCpoqhwUNmIkIuYG4e7kI++H4BHPjoyBqkuLrIRBqpRAiMkCDKRKrqYCLautr4oobSxnZmqBY2dviOIM6wdhka+KhpQkKYmLp8-SZEYN4jqGrIyP4jIoHwcWO+3tQaKQFwCBC5ogI0kFqwCGXgOmLDlZTV5mD2DfWKzRwIM2Aapn0aqMg4OEiu7jAnm8kF8-kCANC+HCoMi-i0Ow4XHERSOJ2O5QuRCqphud0UD0oLTaXm4AWhBE6iHc5XQ7U63V6-QS2KElFadNGfFGk2m0kKyECbCRgiYSD2mnOEmOMhkpyksvOCiUAHdnicxSBvuBEGJmGq0aIDiA0pKiPqOKaBdoCkVzQbtbweOonXrrMUtMadHpdRB5Mx3d7hKoSq6-Xr2LA+DwTlHZFwlVB9gYlYoLXGY7sMaVyuns9nDdpUnqDdnTYWE-b1aIExnmkhzQBzDjRnMt2QIIQNks27KmtTZSsWgf15oJUdVkfcLRTk6Tl0nfrZbPmgBOY8HSCXbfEMgt2s1I81VdNXvUxqrsCtqOz1svjr41e0j-NAHtaD8pWpUOJeDVdAg6DEEQ1DxFi4bOES4D+u+NCfr+CA-lAuI1PgOh8NwnYNnS-LgE8NDOEwervmoKDZPsXhaN8OGylsbIHJ04HaMxpGYMwQA)














