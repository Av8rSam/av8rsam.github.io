---
layout: post
title: The Resistor
date: 2022-04-03
subtitle: Second Part to Series
gh-repo: Av8rSam/av8rsam.github.io
gh-badge: [star, fork, follow]
tags: [Resistors, Resistance, Series, Parallel, Equivalent Resistance]
comments: true
---
Welcome to part two of the basic electrical engineering series. This post will cover everything resisitors. Please read the previous post about voltage, current, and resistance if you don't understand those concepts yet. 

Resistors come in several different forms. The most common look like:
![Resistor](https://www.electronicsforu.com/wp-contents/uploads/2021/06/3-9.jpg)

Their resistance is measured in Ohms. Resisitors are used to provide a known load to a circuit. Combining resisitors, we can make things such as voltage dividers or current dividers. These can be used to provide a specific voltage to an IC. Lets analyze some circuits, starting with circuit A:
![circuits](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fd2vlcm61l7u1fs.cloudfront.net%2Fmedia%2F7c0%2F7c0faad2-c154-4b34-a07a-7fb3321435fe%2Fphpvd4VzE.png&f=1&nofb=1.jpg)
To find the total resistance of two resistors in series, we simply add their values together. Lets say R1 is 10 ohms and R2 is 25 ohms, the total or "Equivalent Resistance" would be 35 ohms. Simply enough. Thus, for resistors in series, the rule is:
![equation1](https://latex.codecogs.com/png.image?\dpi{110}R_{eq}&space;=&space;\sum{R_{1,&space;2,&space;3..n}})
Looking at circuit B now, to find the total resistance of two resistors in parallel, it gets a little more complicated. The total resistance is the inverse of the sum of the inverse resistances. So, take 1 divided by R1, add this to 1 divided by R2, and then take one over this. The equation for resistors in parallel is:
![equation2](https://latex.codecogs.com/png.image?\dpi{110}R_{eq}&space;=&space;(\sum{R_{n}^{-1}})^{-1})
Where did these equations come from? we can look at the current going through the circuit to find this out. For the series circuit, we can see that the current going through both resistors will be the same. Think of someone doing a long obstacle course with two main obstacles. They could do one obstacle very quickly but they will use all their energy and won't have any for the next obstacle. Therefore, they must conserve their energy and use half of their energy on the first obstacle and half on the second. You can kind of think of voltage as the energy in this analogy, half the voltage will be used on one and half on the other.  
Since current through a loop is equal everywhere, we can always assume the voltage will "conserve" its energy. Now, what if we have two different obstacles or two different resistors? The equivalent or total resistance will still be the sum but what will the voltage across each resistor be? Just like an obstacle course, the runner will conserve their energy for the largest obstacle. The same thing goes for voltage, the larger resistor will have the larger voltage drop across it. 
This is known as the voltage divider. The voltage divider circuit looks like:
![voltagedivider](https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2Fwww.abelectronics.co.uk%2Fdocs%2Ftools%2Fresistor%2Fvoltage-divider.gif&f=1&nofb=1.jpg)
Really, a voltage divider is two resistors in series and we take the reference voltage across one resistor. Based on the ratio between the resistors, we can find the voltage between them. The equation for this is: 
![equation3](https://latex.codecogs.com/png.image?\dpi{110}V_{out}=V_{in}*\frac{R_2}{R_1&space;&plus;&space;R_2})
This is a very powerful equation which will be used across many different applications and circuits. For example, lets say you have a sensor you want to connect to an Arduino microcontroller. The sensor measures wind speed and outputs a value between 0 and 15 volts. The Arduino can only measure between 0 and 5 volts. You can use a voltage divider to scale this range down to work with the arduino. So, we want to get 15 down to 5, using our equation we plug in and get:
![equation4](https://latex.codecogs.com/png.image?\dpi{110}5=15*\frac{R_2}{R_1&space;&plus;&space;R_2})
So we know that 
![equation5](https://latex.codecogs.com/png.image?\dpi{110}\frac{R_2}{R_1&space;&plus;&space;R_2}&space;=&space;\frac{1}{3})
And we can use some algebra to see that R1 needs to have twice the resistance of R2. We can then just pick some values, lets say 1k ohms and 2k ohms and take a lead from inbetween these two to our arduino. Now our 0-15v range has been scaled to 0-5v. 
One last topic to his is the current divider. In parallel, two resistors form a current divider. The current going through R1 is equal to 
![equation6](https://latex.codecogs.com/png.image?\dpi{110}I_{out}=I_{In}*\frac{R_1}{R_1&plus;R_2})
I will cover more of this kind of topic in the next post. 
