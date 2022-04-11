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
