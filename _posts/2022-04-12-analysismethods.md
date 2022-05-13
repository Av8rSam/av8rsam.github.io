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

![KCLcircuit](/assets/img/KCLcircuitpic.PNG)

The two resistors on the right can be combined into an equivalent resistance of 100 ohms. Now we have two 100 ohm resistors in parallel as such:
![KCLcircuit2](/assets/img/KCLcircuit2pic.PNG)
If we wanted to find the current going through the first 100 ohm resistor we could re-arrange ohms law to get 
![equation3](https://latex.codecogs.com/svg.image?I&space;=&space;\frac{V}{R})
So 10 volts divided by 100 ohms is 0.1 amps. Since the second resistor is also 100 ohms, we can say that the current through that resistor is also 0.1 amps. According to KCL we can say that the total current going into the resistor system is 0.2 amps. We can check that by finding the total equivalent resistance and using ohm's law. So ![equation4](https://latex.codecogs.com/svg.image?\frac{1}{\frac{1}{100}&plus;\frac{1}{100}}&space;=&space;50) 
And 10 volts divided by 50 ohms is 0.2 amps. This checks out and we can see how KCL works. In summary, 0.2 amps goes in and 0.1 amps goes down each branch to each resistor. One thing to understand here is that the voltage sources I use in my examples are ideal, meaning they keep their positive output however many volts above the negative at all times. They can also provide a wide range of voltages without sagging. 

**Node Voltage**

Node voltage is my favorite circuit analysis technique. Based off of KCL, we pick a "node" and find the voltage in reference to ground through the understanding that all the current coming in and out of the node is equal to zero. First, lets start by practicing identifying nodes. Nodes connect two components in an electrical circuit. Think of them as a piece of wire in a circuit where you can stick the probe from a multimeter and measure voltage. Lets use the below circuit:

![NodeVoltage](/assets/img/NodeExamplePic.PNG)

First, we need to establish a reference or ground node. Typically, we chose the node connected to the negative side of the battery but a good rule of thumb is to chose a reference node by the node that has the most connections. For this circui, the reference node will be:

![referencenode](/assets/img/groundnode.jpg)

Now that we have a reference node, we can label our other nodes. 

![othernodes](/assets/img/othernodes.jpg)

I labeled them as N1 and N2. Ok, lets use node voltage to analyze these circuits. Rememeber how all the current entering a node has to equal all the current exiting the node? We can apply this to each node to solve for the voltage at that node. Using Ohm's law, we can solve for the currents entering the node. If we assume that all the currents are exiting the node, then one will be "negative" and balance out the "positive" current. Basically, all we need to do is sum all the currents exiting the node and set it equal to zero. Lets just look at one node for now, N1.

![analysisv1](/assets/img/analysisv1.jpg)

We can determine current I1 by finding the voltage across R1. 
![equation4](https://latex.codecogs.com/png.image?\dpi{110}I_1&space;=&space;\frac{N_1-V_1}{R_1})
As you can see, the current I1 is equal to the voltage drop across R1 divided by the resistance R1. We can find the currents I2 and I3 the same way. For I2, the voltage drop is the difference between N1 and N2.  
![equation5](https://latex.codecogs.com/png.image?\dpi{110}I_2&space;=&space;\frac{N_1-N_2}{R_2})
For I3, the voltage drop is just equal to N1. Thus, 
![equation6](https://latex.codecogs.com/png.image?\dpi{110}I_3&space;=&space;\frac{N_1}{R_3})
Now that we have all of our equations for the currents, we can combine them by summing them to equal zero. 
![equation7](https://latex.codecogs.com/png.image?\dpi{110}\frac{N_1-V_1}{R_1}&plus;\frac{N_1-N_2}{R_2}&plus;\frac{N_1}{R_3}=0)
This equation would have two unknowns so we need to make a similar equation for N2 now. First, draw the current leaving N2:

![analysisv2](/assets/img/analysisv2.jpg)

Now, repeat the process done before. The current I4 is going to be equal to 
![equation8](https://latex.codecogs.com/png.image?\dpi{110}I_4&space;=&space;\frac{N_2&space;-&space;N_1}{R_2})
I am going to skip the step by step and list out all of the currents leaving N2 as one equation.
![equation9](https://latex.codecogs.com/png.image?\dpi{110}\frac{N_2-N_1}{R_2}&plus;\frac{N_2}{R_4}&plus;\frac{N_2}{R_5&plus;R_6}=0)
Now, we have two equations and two unknowns. Via some algebra and maybe a computer solver we can solve for the voltages at N1 and N2.

**Mesh Current**

Now, I will explain mesh current analysis. Mesh current analysis relies on Kirchoff's Voltage Law (KVL) rather than KCL from nodal analysis. Here is a circuit you can analyze with Mesh Current Analysis:

![meshv1](/assets/img/meshexamplepic.PNG)

This circuit is relatively simple for a mesh current analysis example and it could be analyzed with nodal analysis but it is a good way to describe mesh current analysis. You may run into circuits which are very messy and nodal analysis won't work. That's when you'll need to use mesh current analysis. 

What is a mesh? a mesh is a loop within a circuit. According to KVL, all of the voltages in a loop will sum to zero. We can use this to determine the current in any single loop in a circuit. I will draw the loops in our circuit above:

![meshanalysisv1](/assets/img/meshanalysisv1.jpg)

Beginning in the loop labelled X we will start in the bottom left corner and move clockwise starting at resistor R7. Since we are trying to add up the voltages, we need to find the voltage across R7. The voltage across R7 is equal to 
![equation10](https://latex.codecogs.com/png.image?\dpi{110}I_x*R_7)
Which was found using ohm's law. Now, we can write an equation for loop X.
![equation11](https://latex.codecogs.com/png.image?\dpi{110}I_x(R_7)&plus;I_x(R_8)&plus;R_4(I_x-I_z)&plus;R_1(I_x-I_Y)=0)
One thing to note here is when a resistor connects two meshes like R4, we multiply the resistance R4 by the net difference between current X and current Y. Always assume the current you are working with is the larger current and subtract the other from it. So for current X, subtract currents z and y rather than subtract current x. Now, for loop Y, the equation will look like:
![equation12](https://latex.codecogs.com/png.image?\dpi{110}-V_1&plus;R_1(I_Y-I_X)&plus;R_6(I_Y-I_W)=0)
Here, notice for voltage sources, we just put their voltage value into the circuit. The reason it is negative is because we are going clockwise around the loop and enter its negative terminal first. For loop Z the equation will be:
![equation13](https://latex.codecogs.com/png.image?\dpi{110}R_4(I_z-I_X)&plus;R_5(I_Z)&plus;R_2(I_Z)&plus;R_3(I_Z-I_W)=0)
And for loop W the equation will be:
![equation14](https://latex.codecogs.com/png.image?\dpi{110}R_6(I_W-I_Y)&plus;R_3(I_W-I_Z)&plus;V_3=0)
Again, there is a voltage source (just noticed it's named V3 even though there are only 2, oops) and this voltage source, when going clockwise, is positive. 
Now, we have 4 equations and 4 unknowns so we can plug it into a computer to solve or do some algebra. 

What happens when there is a current source in a mesh? Say V1 from the example above was a current source. Current sources make mesh analysis easier! If V1 was a current source, ay I1, it would mean that the loop current IY would be equal to I1. Therefore, everywhere in the equations where you see IY you can replace that with current I1. 

**Special Cases** 

There occasionally are a few special cases with these analysis methods which I will discuss.

The first is the super node. A super node is when two nodes are connected via a voltage source. Here is an example:

![supernodepic](/assets/img/supernodepic.PNG)

When you try to do nodal analysis on this circuit you run into a problem because V2 separates two of the nodes. How do we work around this? We turn it into a supernode. I will draw the nodes on the circuit:

![superanalysisv2](/assets/img/superanalysisv2.jpg)

When making our equations for each node, on the super node labelled NS, we will need to write the equations for N1 and N2 as one. We will, in a sense, be looking at the current leaving the entire super node.

Here's the equation for NS:
![equation15](https://latex.codecogs.com/png.image?\dpi{110}\frac{N_1-V_1}{R_1}&plus;\frac{N_1}{R_3}&plus;\frac{N_2}{R_4}&plus;\frac{N_2-N_3}{R_6}=0)
So, we never use the label NS in the equation, we use the individual node labels but the terms for N1 and N2 are in the same equation. Now, for N3:
![equation16](https://latex.codecogs.com/png.image?\dpi{110}\frac{N_3-N_2}{R_6}&plus;\frac{N_3}{R_5}=0)
And after that we have one final equation to connect the supernode. Since V2 separates N1 and N2, we know that those two nodes will have a voltage difference of V2. Therefore we can write the equation: 
![equation17](https://latex.codecogs.com/png.image?\dpi{110}N_1-N_2=V_2)
And again with some algebra, we can solve for each voltage.

The next Special case is the super mesh. Here is an example:

![supermeshpic](/assets/img/supermeshpic.PNG)

A current source is in between two meshes. We will have to make a super mesh like this:

![smanalysisv1](/assets/img/smanalysisv1.jpg)

Where we will analyze the purple loop as one rather than two. Similarly to supernode analysis, we will solve for the purple loop and then use a connecting equation to solve for each individual loop. Our first equation for the supermesh will look like:
![equation18](https://latex.codecogs.com/png.image?\dpi{110}-V_1&plus;R_1(I_x)&plus;R_3(I_Y-I_Z)&plus;R_5(I_Y)&plus;R_4(I_Y)&plus;R_2(I_X)=0)
And for Mesh Z:
![equation19](https://latex.codecogs.com/png.image?\dpi{110}R_6(I_Z)&plus;R_8(I_Z)&plus;R_7(I_Z)&plus;R_3(I_Z-I_Y)=0)
And finally, our connecting equation. Since the current source is pointing down, we will assume that current X will be greater than current Y.
![equation20](https://latex.codecogs.com/png.image?\dpi{110}I_X-I_Y=I_1)
And once again for the last time just algebra to solve for the current loops.

That's all for this tutorial. These methods will be used in just about everycircuit from here on out.
