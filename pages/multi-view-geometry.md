---
layout: post
title: Multi-view-geometry
description: Notes on multi-view geometry
tags: ["Geometric vision", "Multi-view Geometry"]
---

### Introduction to Multi-view Geometry

#### How does scaling an image affect the intrinsic matrix? 

To go from a 3d point $P=(x,y,z,1)$ in homogenous world coordinates, to $(u,v)$ in camera coordinates, the following equation holds true:

$$
(u,v,S) = \begin{pmatrix}\alpha_{x} & 0 & u_0 & \\
0 & \alpha_{y} & v_0\\
0 & 0 & 1 \\
\end{pmatrix}
\begin{pmatrix}R_{11} & R_{12} & R_{13} & T_{x}\\
R_{21} & R_{22} & R_{23} & T_{y}\\
R_{31} & R_{32} & R_{33} & T_{z}\\
0 & 0 & 0 & 1\\
\end{pmatrix}
\begin{pmatrix}
x\\  
y\\  
z\\ 
1\\
\end{pmatrix}
$$

We can write $(u,v,S)$ as $(u/S,v/S,1)$ as these are homogeneous coordinates. $u$ then can be written as $\frac{m_1 P}{m_3P}$. $v$ then can be written as $\frac{m_2 P}{m_3 P}$, where if $M$ is the project of the intrinsic and transformation matices, then $m_1$ is the 1st row of $M$.

Assuming we rescale the matrix as

$$
u' = \frac{u}{2} = \frac{1}{2}\frac{m_1 P}{m_3 P},  v'= \frac{v}{2} =  \frac{1}{2}\frac{m_2 P}{m_3 P}
$$

Rewritten in matrix form this is:


$$
(u',v',S) = \begin{pmatrix}\alpha_{x} & 0 & u_0 & \\
0 & \alpha_{y} & v_0\\
0 & 0 & 1 \\
\end{pmatrix}
\begin{pmatrix}0.5 & 0 & 0.5 & \\
0 & 0.5 & 0.5\\
0 & 0 & 1 \\
\end{pmatrix}
\begin{pmatrix}R_{11} & R_{12} & R_{13} & T_{x}\\
R_{21} & R_{22} & R_{23} & T_{y}\\
R_{31} & R_{32} & R_{33} & T_{z}\\
0 & 0 & 0 & 1\\
\end{pmatrix}
\begin{pmatrix}
x\\  
y\\  
z\\ 
1\\
\end{pmatrix}
$$
