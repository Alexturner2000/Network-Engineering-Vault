# Attenuation
Tags: [[Attenuation Coefficient]], [[Electrical]], [[PoE]], [[Physics]], [[UTP]]

The reduction in signal strength over a distance

## Calculate using Input Output
$$Attenuation(dB) = 10 \cdot log_{10} (\frac{P_{in}}{P_{out}}) $$
$P_{in}$ is power-in in Watts
$P_{out}$ is power-out in Watts 

## Calculate using Attenuation Coefficients
$$ Attenuation (dB) = A(f) × (\frac{L}{100})$$
$A(f)$ is attenuation coefficient in $dB$ per 100 meters at frequency $f$
$L$ is length in meters

---
### Cat5e
**Given**
$f = 100MHz$ or $100,000,000Hz$
$A(f) = 24dB$ for 100MHz Cat5e

**Calculation**
$Attenuation = A(f) × L$ 
$Attenuation = 24dB × 1$ 
$Attenuation = 24dB$

The attenuation coefficient is already commonly known for Cat5e, but for a thorough explanation on how its calculated see [[Attenuation Coefficient]] tag.

