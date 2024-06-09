---
layout: post
title: AC Sources
date: 2022-05-15
subtitle: Intro to Alternating Current Sources
gh-repo: Av8rSam/av8rsam.github.io
gh-badge: [star, fork, follow]
tags: [AC, Alternating Current, Sine Waves]
comments: true
---

**AC Sources**

An AC source, or alternating current source, supplys a constantly reversing voltage or current. We have been working with DC current which is just one polarity, plus and minus. AC sources still have a polarity but most often it doesn't matter because current is reversing in and out of each terminal. The power in US homes comes in the form of a 170 volt sine wave oscillating at 60 Hz. If you hear 120 volts rms that is the same thing I will talk about that later.

AC sources can be modelled by a sine or cosine function. Most electrical engineers use the cosine function. A cosine voltage source will have the equation:
![equation1](https://latex.codecogs.com/png.image?\dpi{110}V(t)=Acos(\omega&space;t&space;\pm&space;\theta))
Where the source is changing with time. The "A" represents the amplitude of the source, the greek letter omega which looks like a fancy "w" represents the frequency of the source in radians per second. The greek letter theta which looks like a fancy zero represents the phase shift of the source. 

What does this all mean? Well, say we had a 170 volt 60 Hz cosine wave, our function would look like:
![equation2](https://latex.codecogs.com/png.image?\dpi{110}V(t)=170cos(120\pi&space;t))
To get from 60 Hz to radians per second, you simply just multiply by 
![equation3](https://latex.codecogs.com/png.image?\dpi{110}2\pi)
The peaks of the graph would reach 170. 
![graph](/assets/img/cosinegraph.PNG)

Theta is written in the equation as degrees but in order to use the cosine function you must conver to radians before calculating. to convert from degrees to radians use the following: 
![equation4](https://latex.codecogs.com/png.image?\dpi{110}\theta_{radians}=\theta_{degrees}*\frac{\pi}{180})
and from radians to degrees use the following:
![equation5](https://latex.codecogs.com/png.image?\dpi{110}\theta_{degrees}=\theta_{radians}*\frac{180}{\pi)
Luckily, for most circuits, we will use the degrees number and don't need to convert to radians. 

To convert from cosine waves to sine waves, use the following:
![equation6](https://latex.codecogs.com/png.image?\dpi{110}Acos(\omega&space;t&plus;\theta)=Asin(\omega&space;t&plus;(\theta&space;&plus;90)))

**RMS Values**

There are some AC Sources which will be labelled as RMS or "Root Mean Square." Since an AC source is alternating, the average of it would be zero. Obviously, the source is not equal to zero. In order to find the average then, an integral was used and the signal was squared, then the average was found, then the root was found. Squaring makes the negative peaks positive which allows for a non-zero mean to be found. Luckily, we don't need to find the integral of every AC source we come across. If we simplify the integral, it comes out to be:
![equation7](https://latex.codecogs.com/png.image?\dpi{110}V_{rms}=\frac{V_{peak}}{\sqrt{2}})

Back to the American home. 170 divided by the square root of 2 is 120. Therefore, you typically hear the voltage of a home as 120 Volts RMS. The RMS value is the equivalent DC value of the sine wave. Therefore, if you had 120 volts DC, you would need 170 volts AC to have the same average value. Additionally, the RMS value is what your multimeter will read.

A cosine or sine function will never have an RMS value in front of it. It is an equation of the wave and therefore will have the peak value. 
