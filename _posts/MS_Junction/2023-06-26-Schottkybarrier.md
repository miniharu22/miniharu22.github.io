---
layout : single
title: "[MS Junction] Non-Ideal Effects : Schottky Barrier Lowering Effect"
categories: Junction
tag: 
    - [MS Junction]
toc: true
toc_sticky: true
comments: true
use_math: true
---

Image Charge, Schottky Barrier Lowering

## 1. Image Charge

&nbsp;

<p align="center"><img src="/assets/images/msjunction/18.png" width="30%" height="30%"  title="" alt=""/></p>

Before explaning the Schottky Barrier Lowering Effect, we should first know about **Image Charge**.  

Assuming that a metal wire having an infinite length exists in a grounded state, if one charge is located as far away as $$d$$ from the wire, this charge creates a potential in the wire.  

However, since this wire is grounded, the potential must always be zero, resulting in a contradiction.  

&nbsp;

<p align="center"><img src="/assets/images/msjunction/19.png" width="30%" height="30%"  title="" alt=""/></p>

To resolve this contradiction, it is assumed that virtual charges with opposite polarity to conventional charges exist in a state seperated by the same distance ($$d$$), and these virtual charges are called **Image Charge**.  

&nbsp;

## 2. Schottky Barrier Lowering

Up until now, We have knowed that Schottky Barrier height is invariant because it is a unique property of material, but it is not. To explain this, the concept of Image charge is necessary as learned above.  

&nbsp;

<p align="center"><img src="/assets/images/msjunction/20.png" width="50%" height="50%"  title="" alt=""/></p>

When metal and silicon are bonded, if electrons are located in the silicon, a positive image charge is formed in the metal. At this time, each charge generates an E-field, and the synthesis direction of each E-field becomes Metal -> Silicon.  

&nbsp;

<p align="center"><img src="/assets/images/msjunction/21.png" width="50%" height="50%"  title="" alt=""/></p>

If Reverse bias is applied to the MS Junction, an E-field is formed in the direction of Silicon -> Metal due to the fixed charge present in the depletion region.  

However, as fixed charge is formed by electrons located in silicon, an E-field is generated in the opposite direction of the existing E-field as above. And the E-field due to fixed charge and E-field due to image charge are offset, reducing Schottky Barrier Height.  

This phenomenon is called the **Schottky Barrier Lowering Effect**.  

In other words, there are various factors when calculating the current in the reverse bias statem but it should be noted that the Schottky Barrier Lowering Effect must be considered.  

