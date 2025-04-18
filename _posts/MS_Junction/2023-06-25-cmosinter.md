---
layout : single
title: "[MS Junction] Non-Ideal Effects : CMOS Interconnection"
categories: Junction
tag: 
    - [MS Junction]
    - [Tunneling]
    - [CMOS]
toc: true
toc_sticky: true
comments: true
---

CMOS Interconnection, Ohmic contact with Highly Doping

## 1. CMOS Interconnection

As, previously learned, Ohmic Contact can be used as an interconnection vecause current can flow smootly due to low potential barrier.  

So what exactly is Interconnection?  

&nbsp;

<p align="center"><img src="/assets/images/msjunction/14.png" width="50%" height="50%"  title="" alt=""/></p>

The figure above is a cross-sectional view of CMOS. We can see that nmos and pmos are connected. In order to apply an electrical signal (=current) to each semiconductor, a metal (gray part in the figure) must be connected. 

In this way, **Interconnection* is the connection of metal to the semiconductor to transmit the signal. This is formed through Ohmic contact.  

Then, is Ohmic contact formed by connecting only metals to semiconductors like that as above?  

&nbsp;

## 2. Ohmic contact with Highly Doping

&nbsp;

<p align="center"><img src="/assets/images/msjunction/15.png" width="50%" height="50%"  title="" alt=""/></p>

In order to form Ohmic contact, the relation of greater and less between metal and silicon's work function is important as shown in the figure above.

This is also divided according to wheter silicon is n-type or p-type.  

&nbsp;

<p align="center"><img src="/assets/images/msjunction/16.png" width="50%" height="50%"  title="" alt=""/></p>

In actual semiconductor processes, various metals cannot be used in a complex manner while considering the relation of greater and less of the each work function.  

Also, if we look at both ends of the above cross-sectional view, different types of semiconductors are bonded to one metal at the same time. In this case, it is difficult to form Ohmic contact because there is a contradiction that $$Φ_s$$ < $$Φ_m$$ and $$Φ_s$$ > $$Φ_m$$ at the same time.  

&nbsp;

<p align="center"><img src="/assets/images/msjunction/17.png" width="50%" height="50%"  title="" alt=""/></p>

To solve this problem, a method using doping concentration is used, not changing the type of metal.  

In the existing Schottky Contact, rectifying properties appear, but when silicon is doped with high concentration, the difference between $$E_F$$ and $$E_C$$ is reduced as shown in the above picture.  

In addition, the depletion width of the MS Junction is inversely proportional to the doping concentration, so highly doping rapidly reduces the thickness of potential barrier.  

At this time, since electrons of the metal can pass through the potential barrier through **Tunneling**, and move to the silicon, an interconnection is formed using this.  

For example, if the type of metal is fixed as one, in the p-type, Ohmic contact can be formed using the difference in work function, and in the n-type, Tunneling can be used to make it similar to Ohmic contact.  

