# Attenuation
Tags: [[Attenuation Coefficient]], [[Electrical]], [[PoE]], [[Physics]] [[UTP]]

The reduction in signal strength over a distance
$$ Attenuation (dB) = A(f) × L$$
$A(f)$ is attenuation coefficient in $dB$ per meter at frequency $f$
$L$ is length in


**Cat5e**
We know frequency for Cat5e is 100MHz
$$Attenuation (dB) = A(f) × L = 24dB(for 100 MHz, Cat5e) × 1 = 24dB$$
---
## Attenuation Coefficient
Unless we are given the attenuation coefficient, well need to calculate it with the following equation
$$A(f)=\sqrt{(\frac{R}{2}+\frac{G}{2})×(\frac{L}{2}+\frac{C}{2})}$$
$R$ is the resistance per unit length in *[[Ohms]]*
$G$ is the conductance per unit length in *[[Siemens]]*
$L$ is the inductance per unit length in *[[Henries]]*
$C$ is the capacitance per unit length in *[[Farads]]*

$$A(f)=\sqrt{(\frac{R}{2}+\frac{G}{2})×(\frac{L}{2}+\frac{C}{2})}
=\sqrt{(\frac{0.188\ohm /m}{2}+\frac{0.001S}{2})×(\frac{50\mu H}{2}+\frac{5nF}{2})}
$$
$$
=\sqrt{(\frac{0.188\ohm}{2}+\frac{0.001S}{2})×(\frac{50\mu H}{2}+\frac{5nF}{2})}
$$