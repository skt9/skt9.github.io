---
layout: post
title: Stochastic Differential Equations for Diffusion
description: Overview of the use of SDEs in Diffusion Models
---

### Introduction to SDEs


A stochastic differential equation (SDE) is a differential equation 
in which one or more of the terms is a stochastic process,[1] resulting in 
a solution which is also a stochastic process. SDEs have many applications throughout 
pure mathematics and are used to model various behaviours of stochastic models such as stock 
prices,[2] random growth models[3] or physical systems that are subjected to thermal fluctuations.


SDEs have a random differential that is in the most basic case random white noise calculated 
as the derivative of a Brownian motion or more generally a semimartingale. However, other types 
of random behaviour are possible, such as jump processes like Lévy processes[4] or semimartingales 
with jumps. Random differential equations are conjugate to stochastic differential equations. 
Stochastic differential equations can also be extended to differential manifolds.[5][6][7][8]


### Brownian Motion

Brownian motion is the random motion of particles suspended in a medium (a liquid or a gas).[2]

This motion pattern typically consists of random fluctuations in a particle's position inside a 
fluid sub-domain, followed by a relocation to another sub-domain. Each relocation is followed by 
more fluctuations within the new closed volume. This pattern describes a fluid at thermal equilibrium, 
defined by a given temperature. Within such a fluid, there exists no preferential direction of flow 
(as in transport phenomena). More specifically, the fluid's overall linear and angular momenta remain 
null over time. The kinetic energies of the molecular Brownian motions, together with those of molecular 
rotations and vibrations, sum up to the caloric component of a fluid's internal energy 
(the equipartition theorem).


