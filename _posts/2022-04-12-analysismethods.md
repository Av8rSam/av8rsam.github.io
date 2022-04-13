---
layout: post
title: Kirchoff, Node, and Mesh
date: 2022-04-03
subtitle: A guide to circuit analysis tools
gh-repo: Av8rSam/av8rsam.github.io
gh-badge: [star, fork, follow]
tags: [Resistors, Kirchoffs voltage law, kirchoffs current law, nodal voltage analysis, mesh current analysis]
comments: true
---

Welcome to one of the longer electrical engineering basics post. In this post, I will describe how to use Kirchoff's Voltage law, Kirchoff's Current law, Node Voltage analysis, and mesh current analysis. These are all very strong and important tools you can use to analye any ciruit. 

**Kirchoff's Voltage Law**

Kirchoff's voltage law states that the voltage drops around a loop in a circuit must sum to equal zero. This is like my analogy from the previous post about resisitors, I talked about voltage being a person running an obstacle course. Each time the person does the obstacle course, they are going to use all the energy they have and if there are multiple obstacles, then the person will allocate their energy accordingly. 
For an example of KVL with resistors look at the below circuit:

![kvlcircuit](/assets/img/KVLcircuitpic.PNG)

Using voltage divider to solve for the voltage across R1 we do 
![equation1](https://latex.codecogs.com/png.image?\dpi{110}10*\frac{25}{100}&space;=&space;2.5&space;). Now that we know how many volts are across R1, we can use KVL to determine the voltage across R2. We start at the bottom left corner and work our way around the circuit in a clockwise motion. Going into the voltage source, there is a negative sign first so the first term we write down is -10. Then we get to R1, we will make the sign of its voltage drop positive since it has a positive voltage drop across it. So we add to our string +2.5. Finally, we arrive at R2 and since it is another resistor, it will have a positive sign in front.
Lastly, we end the equation by setting it equal to zero. What we have so far is: 
![equation2](https://latex.codecogs.com/png.image?\dpi{110}-10&space;&plus;&space;2.5&space;&plus;&space;R_2&space;=&space;0)
All we have to do is solve for R2, which is going to be 7.5 volts. This is because of KVL which means all of the voltage drops around a circuit sum to zero. More practically, all of the voltage drops across the resistors add to equal the voltage of the battery. 

**Kirchoff's Current Law**

Kirchoff's current law (KCL) states that the current entering a node must equal the current leaving a node. This is easy to see. Imagine a large river splits into two smaller rivers, all the water coming through the larger river must equal the water leaving in the smaller rivers. This is all that KCL is saying and it is a powerful analysis tool. Lets look at the next circuit below:

![KCLcircuit](/assets/img/KCLciruitpic.PNG)

The two resistors on the right can be combined into an equivalent resistance of 100 ohms. Now we have two 100 ohm resistors in parallel as such:
![KCLcircuit2](/assets/img/KCLcircuit2pic.PNG)
If we wanted to find the current going through the first 100 ohm resistor we could re-arrange ohms law to get 
![equation3](https://latex.codecogs.com/svg.image?I&space;=&space;\frac{V}{R})
So 10 volts divided by 100 is 0.1 amps. Since the second resistor is also 100 ohms, we can say that the current through that resistor is also 0.1 amps. According to KCL we can say that the total current going into the resistor system is 0.2 amps. We can check that by finding the total equivalent resistance and using ohm's law. So ![equation4](https://latex.codecogs.com/svg.image?\frac{1}{\frac{1}{100}&plus;\frac{1}{100}}&space;=&space;50) 
And 10 volts divided by 50 ohms is 0.2 amps. This checks out and we can see how KCL works. In summary, 0.2 amps goes in and 0.1 amps goes down each branch to each resistor. 
