---
layout : single
title: "Charge Density"
categories: PN_Junction
tag: PN_Junction
toc: true
toc_sticky: true
comments: true
---

## 1. Charge Density

&nbsp;

<p align="center"><img src="/assets/images/pnjunction/Gauss-Law.jpg" width="50%" height="50%"  title="" alt=""/></p>

When there is one charge on an arbitrary closed surface, The elecrtic flux(Φ) through this surface can represent the electric field($$E$$) as an Integral over the surface.  

In addition, Φ can be expressed as Total charge in a closed surface and Dielectric constant of the transmission medium constituting the surface.  

&nbsp;

<p align="center"><img src="/assets/images/pnjunction/1.png" width="50%" height="50%"  title="" alt=""/></p>

We assume that all charges are concentrated in a single point in a closed surface, But Gauss's Law can be applied even if all charges are evenly distributed in the surface.  
  
At this time, The value obtained by dividing all charges in the surface by the volume is called **Charge Density(ρ,$$C/{cm}^3$$)**.  

If Charge Density is integrated in triplicate with respect to the volume, it is equal to the total amount of charge.   

In addition, the divergence theorem can be used to obtain the Equation in the form of ∇ as above.  

&nbsp;

<p align="center"><img src="/assets/images/pnjunction/2.png" width="10%" height="10%"  title="" alt=""/></p>

If we summarize this equation again for one dimension, We can find the relation expression for Electric Field($$E$$) and Charge Density(ρ).  

&nbsp;

## 2. Poisson’s Equation(ρ-E-V relation)

&nbsp;

<p align="center"><img src="/assets/images/pnjunction/3.png" width="50%" height="50%"  title="" alt=""/></p>

Ealier, The expressions for $$E$$ and ρ were opbtained through Gauss's Law, and since we know the relational expressions for electric fields and voltages, By combine them We obtain the relational expressions for Voltage($$V$$) and Charge Density(ρ) as above. We call it **Poisson Equation**.  

So, if we know the charge density, We can also get the electric field and voltage.
That is why we will now calculate the charge density first to obtain the electric field and voltage from semiconductor.  

&nbsp;

<p align="center"><img src="/assets/images/pnjunction/4.png" width="30%" height="30%"  title="" alt=""/></p>

So what materials are charged in a semiconductor?  

It is **Carrier** and **Fixed Charge**.  

Therfore, in order to calculate the charge density, the concentration of Carrier and Fixed charge must be considered.  