---
layout : single
title: "[PN Junction] Depletion Capacitance"
categories: Junction
tag: 
    - [PN Junction]
    - [Capacitance]
toc: true
toc_sticky: true
comments: true
---

Capacitance, Depletion Capacitance, Expression of Depletion Capacitance, Built-in Voltage Check, Doping Concentration Check

## 1. Capacitance

&nbsp;

<p align="center"><img src="/assets/images/pnjunction/46.png" width="50%" height="50%"  title="" alt=""/></p>

In general, the structure of the capacitor we know is that an insulator or dielectric is filled between two plates.  

Due to the characteristics of this medium, an E-field is generated due to the fixed charge in a situation where the charge is located at both ends of the plate without moving.  

As such, the measure of how much charge can be stored in an E-field is **Capacitance**.  

&nbsp;

<p align="center"><img src="/assets/images/pnjunction/47.png" width="20%" height="20%"  title="" alt=""/></p>

This Capacitance is expressed as the dielectric constant ($$\epsilon$$) and the distance between the plate and the cross-sectional area of the plate($$A$$).  

If the capacitance per unit area is expressed, the unit can be expressed as [F/$$cm^3$$].  

&nbsp;

## 2. Depletion Capacitance

&nbsp;

<p align="center"><img src="/assets/images/pnjunction/48.png" width="50%" height="50%"  title="" alt=""/></p>

Then let's think of the charge density of PN Junction in Reverse Bias.  

In situations where Reverse bias is applied, the majority carrier on each side cannot move due to the increase in the potential barrier, and only Fixed charge exists in the Depletion region.  

At this time, an E-field is generated because only fixed charge exists inside the depletion region, which has a structure similar to Capacitor.  

When Reverse bias is applied in this way, a characteritic similar to the capacitor that occurs in PN Junction is called **Depletion Capacitance**.  

&nbsp;

<p align="center"><img src="/assets/images/pnjunction/49.png" width="50%" height="50%"  title="" alt=""/></p>

Then, how can Depletion capacitance be expressed mathematically?  

When Reverse bias is applied, the Depletion Width is extended.  As a result, the total charge in the Depletion region increases as above. 

&nbsp;

<p align="center"><img src="/assets/images/pnjunction/50.png" width="50%" height="50%"  title="" alt=""/></p>

Also, since Capacitance can be expressed as $$Q=CV$$, Depletion capacitance can be expressed as the amount of changee in Total charge according to the change in Reverse Bias Voltage.  

&nbsp;

## 3. Expression of Depletion Capacitance

&nbsp;

<p align="center"><img src="/assets/images/pnjunction/51.png" width="50%" height="50%"  title="" alt=""/></p>

Depletion capacitance is a differential form of Reverse bias voltage and Charge, and to summarize it, as above it can be expressed in a differential form of One-side Depletion Length and Depletion Width.  

&nbsp;

<p align="center"><img src="/assets/images/pnjunction/52.png" width="50%" height="50%"  title="" alt=""/></p>

If the Depletion capacitance formula is derived using the relational expressions obtained in this way, it is as follows.  

&nbsp;

<p align="center"><img src="/assets/images/pnjunction/53.png" width="50%" height="50%"  title="" alt=""/></p>

In the end, it can be quantitatively confirmed that Depletion capacitance is also in the same form as **Capacitance per unit area**.  

The Depletion Capacitance obtained in this way is an important parameter for interpreting the AC Characteristics of semiconductors later, so we must checked it carefully.  

&nbsp;

## 4. Built-in Voltage Check

&nbsp;

<p align="center"><img src="/assets/images/pnjunction/54.png" width="50%" height="50%"  title="" alt=""/></p>

Using the previously obtained Depletion Capacitance formula, a linear function for $$V_R$$ can be created as above.  

If we write a $$1/{C_{deep}}^2 - V_R$$ Plot, we can obtain a $$x$$ axis intercept, and use it to obtain a Built-in Potential because this value is $$V_{bi}$$.  

&nbsp;

## 5. Doping Concentration Check

&nbsp;

<p align="center"><img src="/assets/images/pnjunction/55.png" width="50%" height="50%"  title="" alt=""/></p>

Using the above $$1/{C_{dep}}^2 - V_R$$ formula, it is possible to extract the relationship between Dielectric constant and Doping concentration form this slope.  

In addition, two relational expressions for $$N_A,N_D$$ can be obtained by using $$V_{bi}$$ through the $$x$$ intercept. Using this, $$N_A,N_D$$ can be obtained.  