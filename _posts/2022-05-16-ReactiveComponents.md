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
2. Step two is to replace the capacitor with a voltage source and connect the power source (or disconnect the power source). Now, solve for the unknown quantity you wish to solve for. Copy this down as ![equation2](https://latex.codecogs.com/png.image?\dpi{110}X(0^{&plus;})) 
3. Step three is to analyze the circuit a long time after the power has been connected (or disconnected). Replace the capacitor with an open circuit. Solve for unknown quantity again, labelling it as ![equation3](https://latex.codecogs.com/png.image?\dpi{110}X(\infty)) 
4. Step Four is to turn off all sources, remove the capacitor, and find the resistance across the terminals. Copy this down as "R". Now, multiply "R" by the capacitor's capacitance. Write that down as ![equation5](https://latex.codecogs.com/png.image?\dpi{110}\tau)
5. Step five is to plug everything into the equation: ![equation4](https://latex.codecogs.com/png.image?\dpi{110}X(t)=X(\infty)&plus;[X(0^{-})-X(\infty)]e^{\frac{-t}{\tau}}) 

Here's an example:
![RCsolve](/assets/img/RCsolve.jpg)
We will say that the switch will close at t=0. So, first step, determine voltage of the capacitor before the switch is moved. This is 0 volts. 
Step two is to replace the capacitor with a voltage source equal to zero volts. This will be a straight wire. For our unknown quantity, which is the voltage across the capacitor, the voltage will be zero. 
Step three is to replace the capacitor with an open circuit and solve for the voltage across. This will be 10 volts.
Step four is to find resistance across the capacitor terminals after turning eveything off. This is 100 ohms. Multiplying 100 by 0.05 we get 5. So the time constant for this circuit is 5 seconds. 
Step five, we get the equation: ![equation6](https://latex.codecogs.com/png.image?\dpi{110}V_{c}(t)=10-10e^{\frac{-t}{5}}) 
Which when we graph, we get something that looks like:
![RCgraph](/assets/img/RCgraph.PNG)

We can replicate these steps for any quantity we wish to know. 

**Inductors**

Comprised of a toroid of wire around a ferrite core, inductors 
