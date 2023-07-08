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


