---
layout : single
title: "[MOS] Non-Ideal Effects : Electrical Oxide Thickness"
categories: MOS
tag: 
    - [MOSCAP]
    - [MOSFET]
    - [Capacitance]
toc: true
toc_sticky: true
comments: true
use_math: true
---

Difference in Oxide Thickness, Poly-Si Gate Depletion, Quantum Confinement Effect, Effects on C-V

## 1. Difference in Oxide Thickness

&nbsp;

<p align="center"><img src="/assets/images/MOSCAP/80.png" width="50%" height="50%"  title="" alt=""/></p>

If the physical thickness of the Oxide is set to $$t_{ox}$$ in the degign, in fact, if we measure the oxide thickness using electrical method, such as C-V plot, it is measured to be greater than $$t_{ox}$$.  

This is because the entire oxide thickness is measured thicker by various mechanisms. The Oxide thickness at this time is defined as **Electrical Oxide Thickness ($$t_{oxe}$$)**.  

&nbsp;

## 2. Poly-Si Gate Depletion

&nbsp;

<p align="center"><img src="/assets/images/MOSCAP/81.png" width="50%" height="50%"  title="" alt=""/></p>

If the Gate of MOS is replaced with highly-doped Poly-Si instead of metal, a depletion region is formed.  

&nbsp;

<p align="center"><img src="/assets/images/MOSCAP/82.png" width="40%" height="40%"  title="" alt=""/></p>

Of course, since it is highly doped, the depletion width is small, but as a result, a additional capacitance is formed, which is defined as $$C_{poly}$$.  

&nbsp;

<p align="center"><img src="/assets/images/MOSCAP/83.png" width="50%" height="50%"  title="" alt=""/></p>

$$C_{poly}$$ is srially connected to $$C_{ox}$$, and the above equation shows that the Oxide thickness has been increased to $$t_{ox}$$ + $$\frac{W_{poly}}{3}$$. 

This phenomenon by Poly-Si is defined as **Poly Depletion Effect**. 

&nbsp;

<p align="center"><img src="/assets/images/MOSCAP/84.png" width="40%" height="40%"  title="" alt=""/></p>

In that case, Subthreshold Swing will increase, which reduces the performance of MOSFET. So, to solve this issue, we mainly use metal gate instead of Poly-Si, these days.  

&nbsp;

## 3. Quantum Confinement Effect

&nbsp;

<p align="center"><img src="/assets/images/MOSCAP/85.png" width="50%" height="50%"  title="" alt=""/></p>

We learned that electrons converge on the surface in Inversion mode as shown above.  

&nbsp;

<p align="center"><img src="/assets/images/MOSCAP/86.png" width="50%" height="50%"  title="" alt=""/></p>

However, the electrons are distributed at locations away from the surface by a certain distance ($$t_{inv}$$) by the Quantum-Mechanical effect, rather than being attached to the surface.  

This phenomenon is called  **Quantum Confinement Effect**.  

&nbsp;

<p align="center"><img src="/assets/images/MOSCAP/87.png" width="50%" height="50%"  title="" alt=""/></p>

Eventually, like Poly Depletion effect, the oxide thickness increases by $$\frac{t_{inv}}{3}$$ and $$C_{ox}$$ decreases.  

&nbsp;

## 4. Effects on C-V

&nbsp;

<p align="center"><img src="/assets/images/MOSCAP/88.png" width="50%" height="50%"  title="" alt=""/></p>

So, due to the Poly Depletion effect and Quantum confinement effect, the actual capacitance is reduced than $$C_{ox}$$.  

In addition, the above C-V Characteristics show that the capacitance decreases proportional to increase in $$V_G$$, because the depletion width increases as Gate voltage increases.  

As the depletion width increases, $$C_{poly}$$ decreases, which also reduces $$C_{oxe}$$.  

**※ However, the increase in Depletion width as $$V_G$$ increases is established only under the assumption that the poly-si gate is used.**  