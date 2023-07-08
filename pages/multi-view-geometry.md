---
layout: post
title: Multi-view-geometry
description: Notes on multi-view geometry
tags: ["Geometric vision", "Multi-view Geometry"]
---

### Introduction to Multi-view Geometry

#### How does scaling an image affect the intrinsic matrix? 

To go from a 3d point $P =(x,y,z,1)$ in homogenous world coordinates, to (u,v) in camera coordinates, the following equation holds true:

$$
(u,v,S) = \begin{pmatrix}2 & 3 & 4 & 5\\
1 & 0 & 0 & 1}\\
2 & 3 & 4 & 5\\
\end{pmatrix}
$$


