---
layout: post
title: Voltage, Current, and resistance
date: 2022-03-25
subtitle: First Part to Basic Electronics
gh-repo: Av8rSam/av8rsam.github.io
gh-badge: [star, fork, follow]
tags: [test]
comments: true
---

Welcome to the first part of my electrical engineering series. I plan to document and record here in posts everything I learn in my educational career. This first post is about the relationship between voltage, current, and resistance. Voltage and current are very common measurements within electronics and electricity. 

**Voltage**

It helps to think of voltage as an electrical pressure. In reality it is a potential difference between two points. It is also called EMF (electromotive force) sometimes. Imagine you carry some electrons up to the top of a hill and release them, they want to go back down the hill but on the way they have to go through a light bulb. Similarly, a voltage means there are electrons at a higher potential seeking lower potential and in order to achieve this potential balance, they have to go through a resistance. A voltage cannot exist unless there is a resistance, similarly, a resistance will always cause a voltage drop. 

The unit of voltage is the volt and it is more formally the energy per unit charge created by separation. The equation for voltage is: *V = (dw)/(dq)* where V is volts, w is unites of energy in joules, and q is charge in coulombs. A coulomb is 6.24 x 10^18 electrons (or protons). 

**Current** 

Current is the measurement of the rate of flow of electrons through a resistance or wire. The units are amperes or amps and one amp is equal to one coulomb per second. You can think of current as the amount of electrons you take to the top of the hill. Typically, one amp is a lot of current and circuits use milliamps or microamps. 

**Resistance** 

Resistance is what ties voltage and current together. Resistance is what it sounds like, it resists electricity. The units are Ohms and it is labelled with the greek symbol Omega. One volt across one ohm will result in one amp. This is a seemingly simple but complex relationship. If we look back at the hill analogy, the person carrying the electrons up the hill is equivalent to a battery which adds electrical potential to a system or circuit. The bulb on the down side of the hill is the reistance, the height of the hill is the voltage, and the amount of electrons going through the bulb is the current. 

**Bringing it all together** 

Voltage, current, and reistance can all be linked by Ohm's law: *V=I x R* which can be written as *I = V/R* 

In reality the hill analogy doesn't line up with what is actually happening. In a circuit, the electrons aren't all piled up at one end and going to the other side, electrons exist at every point in a circuit or wire even when off. Like a hose full of water, if the end of the hose is closed, there is no water running but the hose still has water in it. Voltage across a wire is a pressure causing all the electrons within the wire to begin moving at the same time. This is why electricity is instant, the pressure felt by the electrons is instant and they start flowing as soon as the switch is closed. That's why when you flip a swith your lights come on instantly. 

![Electrons](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT-93_4c-SCBAYig5ykzLTFMZF5qzZ0D3Y3ZA&usqp=CAU.jpg)

There are also some other unique situatiosn regarding these three parameters. You probably have seen some of these things happen in real life. The first is if you have a very low resistance and a voltage, for example say you have a car battery and a wire connecting the two terminals. The wire has close to zero resistance which, if you plug into the ohm's law equation: *12 / (Very Small) = (Very Big)*. There will be a huge current going through the wire, quickly heating the wire up to its melting point. This is why electrical shorts are hazardous in cars, they can cause high heat and the insulation around the wires can start on fire. Another situation is if you have an airgap between two points. Air is a good insulator which means it has a very high reisitance. Air can turn into a conductor however, at extremely high voltages the air ionizes (the electrons separate from the atoms and flow freely) and ionized gas is very conductive. When you bring a wire very close to making an electrical connection, you might see an arc for a very small moment. The arc doesnt last very long. Why it this? Well for an instant, when the gas is ionized, the resistance is very low causing high current. The supply which is providing this voltage starts supplying very high current but it cannot do this forever. Every supply has a limit on how much current it can provide. Once it reaches that limit, the voltage of the supply will drop because it cannot supply that much current anymore. Since the voltage drops due to the limit of the supply, the arc will cease because the voltage is no longer high enough to jump the gap.
