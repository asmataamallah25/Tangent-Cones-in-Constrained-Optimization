# Tangent Cones in Constrained Optimization

In constrained optimization, the tangent cone at a feasible point describes the **feasible directions** in which you can move while still satisfying the constraints, at least locally.  
This repository contains a Python script that visualizes tangent cones of feasible sets from constrained optimization problems in $\\mathbb{R}^2\$. The goal is to see what “feasible directions” look like and how they relate to constraint geometry.

---

## 1. Background: tangent cones in optimization

Consider a constrained problem
$$\[
\min f(x) \quad \text{s.t. } x \in M,
\]$$
where $\(M \subset \mathbb{R}^2\)4 is the **feasible set** (defined by constraints such as $\(g_i(x) \le 0\))$.

At a feasible point \(x\), the **tangent cone** \(T(M,x)\) is the set of directions \(d\) such that, for very small step sizes \(t > 0\), one can move from \(x\) to \(x + t d\) and remain in \(M\). These are the **locally feasible directions** and they appear in first‑order optimality conditions.

**First‑order optimality condition:** At a local minimum \(x^\star\), every feasible direction \(d\) has a non‑negative directional derivative,
\[
Df(x^\star; d) \ge 0 \quad \text{for all feasible } d.
\]
This means there is no feasible direction in which an infinitesimally small step can decrease the objective.

For many simple sets, the tangent cone can be written explicitly and drawn geometrically.

---

## 2. Example problem in this repository

The first example in the code corresponds to the problem
\[
\begin{aligned}
\min_{x\in\mathbb{R}^2} \quad & f(x) = \tfrac12\|x\|^2 \\
\text{s.t.} \quad & x_2 \ge 0.
\end{aligned}
\]

- **Feasible set**
  \[
  M = \{(u,v) \in \mathbb{R}^2 \mid v \ge 0\},
  \]
  i.e. the upper half‑plane.

- **Feasible point**
  \[
  x^\star = (0,0),
  \]
  which lies on the active constraint boundary \(x_2 = 0\).

- **Tangent cone at \(x^\star\)**
  \[
  T(M,x^\star) = \{ d = (d_1,d_2) \in \mathbb{R}^2 \mid d_2 \ge 0\}.
  \]




