---
layout: page
title: Reparameterization Trick
description: Explaining the reparameterization trick
tags: ["generative-models", "maths"]
---

# The Reparameterization Trick
So why is taking the gradient w.r.t $\theta$ of the expectation non-differentiable? 

Let's understand the first case where the expectation is not a function $\theta$: $E_{p(z)}[f_\theta(z)]$?

