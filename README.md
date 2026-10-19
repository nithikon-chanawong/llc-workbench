# LLC Resonant Converter Workbench

An interactive engineering tool for designing and analyzing full-bridge LLC resonant converters based on **Infineon Application Note AN 2012-09**.

🔗 **[Website](https://nithikon-chanawong.github.io/llc-workbench/)**

## Overview

This tool helps engineers explore LLC resonant converter parameters, analyze voltage gain, and examine analytical steady-state waveforms using the First Harmonic Approximation (FHA) and piecewise time-domain models.

## Features

- **Bidirectional Parameter Calculator** — Calculate resonant parameters from component values, or estimate component values from specified design targets.
- **Resonant Gain Analysis** — Plot the voltage gain against normalized switching frequency and explore the effects of quality factor and inductance ratio.
- **Interactive Gain Curve** — Adjust the operating point directly on the graph and examine different frequency operating regions.
- **Steady-State Waveforms** — Visualize primary bridge voltage, resonant tank current, magnetizing current, and secondary rectifier currents.
- **Formula Inspector** — View calculation equations and numerical substitutions for supported parameters.

## Mathematical Model

The calculator uses FHA-based equations for LLC resonant converter analysis, including:

**Resonant Frequency**

$$
f_r = \frac{1}{2\pi\sqrt{L_r C_r}}
$$

**Normalized Switching Frequency**

$$
F_x = \frac{f_s}{f_r}
$$

**Inductance Ratio**

$$
m = \frac{L_r + L_m}{L_r}
$$

**Quality Factor**

$$
Q = \frac{\sqrt{L_r/C_r}}{R_{ac}}
$$

**Voltage Gain**

$$
M(F_x)=
\frac{F_x^2(m-1)}
{\sqrt{
(mF_x^2-1)^2+
F_x^2(F_x^2-1)^2(m-1)^2Q^2
}}
$$


## Reference

Sam Abdel-Rahman, *Resonant LLC Converter: Operation and Design*, Infineon Technologies North America Corp., Application Note AN 2012-09, September 2012.

---

**Note:** This workbench provides analytical calculations and waveform representations. Results should be verified against circuit simulation or experimental measurements before being used for hardware design.
