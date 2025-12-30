# Tangent Cones in Constrained Optimization

In constrained optimization, the tangent cone at a feasible point describes the **feasible directions** in which you can move while still satisfying the constraints, at least locally.  
This repository contains a Python script that visualizes tangent cones of feasible sets from constrained optimization problems in $\\mathbb{R}^2\$. The goal is to see what “feasible directions” look like and how they relate to constraint geometry.

---

## 1. Background: tangent cones in optimization

Consider a constrained problem

$$\
\min f(x) \quad \text{s.t. } x \in M,
\$$

where M $\subset$ $\mathbb{R}^2\$ is the **feasible set** (defined by constraints).

At a feasible point **x**, the **tangent cone** $T(M,x)$ is the set of directions **d** such that, for very small step $t > 0$, we can move from x to $x + t d$ and remain in **M**. These are the **locally feasible directions** and they appear in first‑order optimality conditions.

**First‑order optimality condition:** At a local minimum $x^\star$, every feasible direction **d** has a non‑negative directional derivative:

$$\
Df(x^\star; d) \ge 0 \quad \text{for all feasible } d.
\$$


## 2. Example problem in this repository

The example in the code represents the problem
$$
\min_{x \in $\mathbb{R}^2}$ $\|x\|$ \quad \text{s.t. } x_2 \ge 0
$$

*Note:* Here \(x\) is a vector in $mathbb{R}^2\$, so it has two components ($x = (x_1, x_2)$).

**Feasible set**
  $$
  M = \{(u,v) \in $\mathbb{R}^2 \$ mid v \ge 0\},
  $$
  i.e. the upper half‑plane.

**Feasible point**
  $$
  x^\star = (0,0),
  $$
  which lies on the active constraint boundary \(x_2 = 0\).

**Tangent cone at \(x^\star\)**
  $$
  T(M, x^\star) = \{ d = (d_1,d_2) \in \mathbb{R}^2 \mid d_2 \ge 0 \}.
  $$

