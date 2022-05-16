---
layout: post
title: Reactive Components
date: 2022-05-16
subtitle: Overview of Capacitors and Inductors
gh-repo: Av8rSam/av8rsam.github.io
gh-badge: [star, fork, follow]
tags: [Capacitors, Inductors, AC, Reactance, Capacitance, Inductance, Impedance]
comments: true
---

**Capacitors**

Capacitors are a component of electronics used to store electrical energy in the form of electric fields. They consist of two conductive plates separated by a non-conducting insulator. They store electrical energy by gathering charges on the conducting plates. For this reason, once they are full, capacitors behave like an open circuit because no more current can flow. 

![capacitors](/assets/img/capacitors.jpg)

Capacitors have the main equation: 
![equation1](https://latex.codecogs.com/png.image?\dpi{110}C=\frac{Q}{V})
Where C is capacitance in Farads, Q is charge in coulombs, and V is volts. The larger the capacitance, the larger the amount of charge a capacitor can store. Typically you will read the capacitance and voltage rating on a capacitor. The voltage rating is how many volts you can apply to the capacitor before it breaks down. 

**RC Circuits**

When a capacitor and resistor are connected in series, they behave in a way that is related to their capacitance and resistance values. If connected to a battery with an initially uncharged capacitor, the capacitor will charge up at a rate according to the resistance multiplied by the capacitance. 

One thing about capacitors is that they don't change voltage instantaniously. We can use this to analyze RC circuits. 
1. Step one is to determine the voltage of the capacitor before power is connected or disconnected. Because capacitors can't change instantaneously in voltage, we need to find what they are acting like before a change in the circuit happens. You can find the voltage of the capacitor by removing it from the circuit and finding the open circuit voltage at the terminals.
2. Step two is to replace the capacitor with a voltage source and connect the power source (or disconnect the power source). Now, solve for the unknown quantity you wish to solve for. Copy this down as ![equation 2](https://latex.codecogs.com/png.image?\dpi{110}X(0^{&plus;})) 
3. Step three is to analyze the circuit a long time after the power has been connected (or disconnected). Replace the capacitor with an open circuit. Solve for unknown quantity again, labelling it as 
