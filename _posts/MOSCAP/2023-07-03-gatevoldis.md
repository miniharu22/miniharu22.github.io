---
layout : single
title: "[MOS] Gate Voltage Distribution"
categories: MOS
tag: 
    - [MOSCAP]
    - [MOSFET]
toc: true
toc_sticky: true
comments: true
use_math: true
---

Gate Voltage Distribution, Oxide Voltage

## 1. Gate Voltage Distribution

&nbsp;

<p align="center"><img src="/assets/images/MOSCAP/28.png" width="50%" height="50%"  title="" alt=""/></p>

Earlier, we learned that -$$\phi_{ms}$$ = $$V_{ox0}$$ + $$\phi_{s0}$$.  

So what happens if we apply an additional Gate voltage here?  

&nbsp;

<p align="center"><img src="/assets/images/MOSCAP/29.png" width="50%" height="50%"  title="" alt=""/></p>

The figure above is a schemativ diagram of the band diagram of MOS when $$V_G$$ is applied to the Gate.  

As the voltage is applied, additional band bending is formed on the existing oxide and surface, which is expressed in terms of $$V_G$$ = $$\Delta V_{ox}$$ + $$\Delta \phi_s$$.  

&nbsp;

<p align="center"><img src="/assets/images/MOSCAP/30.png" width="30%" height="30%"  title="" alt=""/></p>

Here, the increases of $$\Delta V_{ox}$$ and $$\Delta \phi_s$$ correspond to the difference between the potentials $$V_{ox}$$ and $$\phi_s$$ in the Thermal Equailibrium state.  

We know that in the Thermal Equailibrium state, -$$\phi_{ms}$$ = $$V_{ox0}$$ + $$\phi_{s0}$$, the above equation is summarized as follows.  

&nbsp;

<p align="center"><img src="/assets/images/MOSCAP/31.png" width="30%" height="30%"  title="" alt=""/></p>

Therefore, it can be seen that the voltage applied form the outside is distributed and applied to $$V_{ox}$$, $$\phi_{ms}$$, and $$\phi_{ms}$$.  

So, When a voltage is applied to the Gate, it first makes the energy band of Silicon flat by $$\phi_{ms}$$, increases the Surface potential to Threshold, and then applies the rest to Oxide.  

&nbsp;

## 2. Oxide Voltage

&nbsp;

<p align="center"><img src="/assets/images/MOSCAP/32.png" width="50%" height="50%"  title="" alt=""/></p>

As we learned before, MOS Structrue is Capacitor.  

When a voltage is applied to the gate, a charge of +$$Q_m$$ is formed in the metal area (which exists only on the surface of metal), and -$$Q_m$$ charge with same amount is formed in the silicon.  

&nbsp;

<p align="center"><img src="/assets/images/MOSCAP/33.png" width="40%" height="40%"  title="" alt=""/></p>

In other words, if charge is formed on the metal by changing the gate voltage, charge of the same amount must be formed on silicon.  

At this time, the value that determines how much charges will be collected in the Capacitor is **Oxide Capacitance**.  

In MOS, since oxide acts as a dielectric, it can be expressed in $$\frac{dielectric constant}{thickness}$$.  

&nbsp;

<p align="center"><img src="/assets/images/MOSCAP/34.png" width="30%" height="30%"  title="" alt=""/></p>

Since we know the formula $$Q$$ = $$CV$$ here, substituting $$C_{ox}$$ and $$V_{ox}$$ values into the formula yields values of $$Q_m$$ or $$Q_s$$.  

Thus, the formula of $$V_{ox}$$ that we wanted to obtain can be expressed as $$V_{ox}$$ = -$$\frac{Q_s}{C_{ox}}$$.  

**※ The (-) sign is used in this expression because $$V_{ox}$$ has a positive sign and $$Q_s$$ has a negative sign.  

