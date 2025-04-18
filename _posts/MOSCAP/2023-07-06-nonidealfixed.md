---
layout : single
title: "[MOS] Non-Ideal Effects : Oxide Fixed Charge"
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

Various Oxide Charge, Oxide Fixed charge, C-V Plot with Oxide fixed charge

## 1. Various Oxide Charge

When we learn about the capacitance, it is assumed that there is no charge inside the oxide, but in reality, there is charge in Oxide.  

&nbsp;

<p align="center"><img src="/assets/images/MOSCAP/65.png" width="50%" height="50%"  title="" alt=""/></p>

There are four main types of Oxide charge.  

First, **Mobile ionic charge ($$Q_m$$)** is a charge caused by the penetration of ions inside Oxide, which is usually caused by impurities from outside, such as human sweat. Recently, however, $$Q_m$$ is negligible because the process is carried out iun an environment such as clean rooms where impurities are shielded.  

Second, **Oxide trapped charge ($$Q_{ot}$$)**, the charge formed by carrier trapped in crystal structure of oxide. Oxide is formed by thermal process with supplying oxygen gas to the Si substrate. But sometimes oxide such as $$SiO_x$$ is formed in the process, not $$SiO_2$$.  

These oxides form Traps because they have unstable molecular structures. The charge that occurs when the mobile carrier is trapped in these traps is **Oxide fixed charge ($$Q_f$$)**.  

&nbsp;

<p align="center"><img src="/assets/images/MOSCAP/66.png" width="50%" height="50%"  title="" alt=""/></p>

In the interface of silicon and oxide, the Dangling bond is formed due to the difference in Lattice structure. This defect forms a kind of Trap. The charge that occurs by trapping mobile carrier is called **Interface Trap charge ($$Q_{it}$$)**.  

&nbsp;

## 2. Oxide Fixed charge

The first thing that affects the C-V properties is Oxide fixed charge.  

&nbsp;

<p align="center"><img src="/assets/images/MOSCAP/67.png" width="50%" height="50%"  title="" alt=""/></p>

When checking the ideal C-V characteristics, it was confirmed that $$V_{fb0}$$ = $$\phi_{ms}, but in this case, that was solved by assuming that there is no charge corresponding to $$Q_m$$ inside silicon.  

&nbsp;

<p align="center"><img src="/assets/images/MOSCAP/68.png" width="50%" height="50%"  title="" alt=""/></p>

<p align="center"><img src="/assets/images/MOSCAP/69.png" width="40%" height="40%"  title="" alt=""/></p>

However, in fact, there is a charge inside the oxide, so if we consider this, the equation is expressed as above.  

&nbsp;

## 3. C-V Plot with Oxide fixed charge

&nbsp;

<p align="center"><img src="/assets/images/MOSCAP/70.png" width="50%" height="50%"  title="" alt=""/></p>

Eventually, Oxide fixed charge creates band bending and consequently affects $$V_{fb}$$, so the C-V plot shifts to the left as $$Q_{ss}$$ increases.  

In other words, due to the additional oxide charge, the point at which the capacitance decreases by enetering the depletion mode changes.  

&nbsp;

<p align="center"><img src="/assets/images/MOSCAP/71.png" width="50%" height="50%"  title="" alt=""/></p>

Looking at the above C-V plot, we can check that $$V_{fb}$$, that is, the point of decrease in capacitance has shifted to the left.  

&nbsp;

<p align="center"><img src="/assets/images/MOSCAP/72.png" width="50%" height="50%"  title="" alt=""/></p>

Furthermore, the formula about $$V_T$$ shows that as $$V_{fb}$$ changes, the Threshold point also shifts to the left. In other words, the point where the capacitance component increases is also shifted to the left.  

