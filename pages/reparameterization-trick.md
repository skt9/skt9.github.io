---
layout: page
title: Reparameterization Trick
description: Explaining the reparameterization trick
tags: ["generative-models", "maths"]
---

# The Reparameterization Trick
So why is taking the gradient w.r.t $\theta$ of the expectation non-differentiable? 

Let's understand the first case where the expectation is not a function $\theta$, $E_{p(z)}[f_\theta(z)]$. $p$ being the probability density.
Assuming $f(\theta,z)$ is differentiable, we compute the gradient as follows:

$$
\begin{aligned}
\nabla_\theta E_{p(z)}[f_{\theta}(z)] &= \nabla_\theta[\int_{z}p(z)f_{\theta}(z)dz]\\
&= [\int_{z}p(z)\nabla_\theta f_{\theta}(z)dz]\\
&= E_{p(z)}[\nabla_\theta f_{\theta}(z)]\\
\end{aligned}
$$

In this case, computing the gradient is straightforward. 

### When $p$ depdends on $\theta$
$$
\begin{aligned}
\nabla_\theta E_{p_{\theta}(z)}[f_{\theta}(z)] &= \nabla_\theta[\int_{z}p_\theta(z)f_{\theta}(z)dz]\\
&= [\int_{z} \nabla_\theta(p_\theta(z)f_{\theta}(z))dz]\\
&=\int_{z} \nabla_\theta(p_\theta(z))]f_{\theta}(z))dz + \int_{z}p_\theta(z) \nabla_\theta f_{\theta}(z))dz\\
&= \underbrace{\int_{z} \nabla_\theta(p_\theta(z))f_{\theta}(z))dz} + E_{p_\theta(z)}[\nabla_\theta f_{\theta}(z)]dz
\end{aligned}
$$

The underbraced part of the equation is where the issue of differentiability comes. The first term of the last equation is not guaranteed to be an expectation. Monte Carlo methods require that we can sample from $p_\theta(z)$, but not that we can take its gradient. This is not a problem if we have an analytic solution to  $\nabla_\theta p_\theta(z)$, but this is not true in general.


### 
Now that we have a better understanding of the problem, let’s see what happens when we apply the reparameterization trick to our simple example. To be consistent with Kingma, I’ll switch to bold text for vectors and denote the 

