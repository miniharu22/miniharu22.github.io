---
layout : single
title: "[MOS] Non-Ideal Effects : Oxide Interface Trap"
categories: MOS
tag: 
    - [MOSCAP]
    - [MOSFET]
    - [Capacitance]
    - [Trap]
toc: true
toc_sticky: true
comments: true
use_math: true
---

Density of Interface Trap, Extraction of $$D_{it}$$ from C-V Plot

## 1. Density of Interface Trap

&nbsp;

<p align="center"><img src="/assets/images/MOSCAP/73.png" width="50%" height="50%"  title="" alt=""/></p>

Interface Trap is distributed at a specific energy level as shown above.  

Distribution of Interface trap is interpreted in consideration of Energy level because the probability of electrons being trapped or escaping also changes depending on which energy level the trap is located at.  

&nbsp;

<p align="center"><img src="/assets/images/MOSCAP/74.png" width="50%" height="50%"  title="" alt=""/></p>

The indicator to figure this out is $$D_{it}$$, which means **Density of Interface trap per Energy level**.  

As shown in the graph above, we can check that $$D_{it}$$ changes with the energy level.  

&nbsp;

<p align="center"><img src="/assets/images/MOSCAP/75.png" width="40%" height="40%"  title="" alt=""/></p>

In addition, as $$\phi_s$$ changes, the change in charge, which is trapped in the interface trap, will also occur.  

This results in another Capacitance, which is called as **$$C_{it}$$**.  

&nbsp;

> **Why is $$D_{it}$$ the biggest in $$E_V$$ and $$E_C$$?**  

Most of interface traps result from the dangling bond at the interface.  

Dangling bond is a defect caused by unstable covalent bonds breaking. Since the energy state of these defective states stabilizes near $$E_C$$ and $$E_V$$ with high probability of presence of carriers, they are mainly distributed at both ends of the bandgap.  

Therefore, $$D_{it}$$ also has the largest value near $$E_C$$ and $$E_V$$.  

&nbsp;

## 2. Extraction of $$D_{it}$$ from C-V Plot

&nbsp;

<p align="center"><img src="/assets/images/MOSCAP/76.png" width="50%" height="50%"  title="" alt=""/></p>

The way to check $$D_{it}$$ is to use the CV Plot.  

If there is a difference between the theorectical and actual values as shown in the figure above when extracting CV characteristics by modeling MOS capacitor, the influence by Interface trap will be the cause.  

&nbsp;

<p align="center"><img src="/assets/images/MOSCAP/77.png" width="30%" height="30%"  title="" alt=""/></p>

Therefore, $$Q_{it}$$ can be extracted using $$\Delta V_G$$ as shown in the figure above.  

&nbsp;

<p align="center"><img src="/assets/images/MOSCAP/78.png" width="30%" height="30%"  title="" alt=""/></p>

Since we know $$Q_{it}$$, if we substitute it into the above formula, we can extract $$D_{it}$$ and $$C_{it}$$.   

&nbsp;

<p align="center"><img src="/assets/images/MOSCAP/79.png" width="50%" height="50%"  title="" alt=""/></p>

However, the method we learned can be used only in MOS Capacitor, not in MOSFET.  

This is because, as shown in the figure above, there are various parasitic capacitance components in MOSFET, so it is difficult to conclude that a change in CV characteristics occured simply due to the influence of only $$C_{it}$$.  

Therefore, to extract $$D_{it}$$ through CV Plot, we must thoroughly analyze other parasitic capacitances components in advance.  