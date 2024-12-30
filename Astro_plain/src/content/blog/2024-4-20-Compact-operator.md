---
title: 'Compact Operator converts weak convergence into convergence.'
description: ''
pubDate: 2024-4-20
tags: ['数学']
---

This is a conclusion I coincidentally discovered when I was working my homework for the functional analysis course. It is so nice and impressive that I'm going to inscribe it here: the compact operator converts weak convergence into convergence.

Before proving, I'm going to give some Lemmas for the convenience.

# Lemma 1:

 ## Statement:

$\mathcal{H}$ is a Hilbert space, $(x_n)_{n\ge1},x_0,x \in \mathcal{H}$, $x_n\rightharpoonup x_0$ and $x_n\rightharpoonup x$ as $n\rightarrow \infty$, then $x_0=x$. That is to say, the weak limit is unique.

## Proof:

Suppose $x_n\rightharpoonup x_0$ and $x_n\rightharpoonup x$ as $n\rightarrow \infty$, then for any $y\in\mathcal{H}$, $(x_n,y)\rightarrow(x_0,y)$ and $(x_n,y)\rightarrow(x,y)$ as $n\rightarrow \infty$.

By the uniqueness of limits, $(x_0,y)=(x,y)$ for all $y\in\mathcal{H}$.

Then, $(x_0-x,y)=0$ for all $y\in\mathcal{H}$. Let $y=x_0-x$, then $\|x_0-x\|=\sqrt{(x_0-x,x_0-x)}=0$. This implies $x_0 -x=0$, i.e. $x_0=x$.

# Lemma 2:

 ## Statement:

$\mathcal{H}$ is a Hilbert space, $(x_n)_{n\ge1},x_0 \in \mathcal{H}$, $x_n\rightharpoonup x_0$ as $n\rightarrow \infty$, then $(x_n)_{n\ge1}$ is bounded.

## Proof:

Let $T_n(\cdot)=(x_n,\cdot)$. It is clear that $T_n$ is continuous linear operators from  $\mathcal{H}$ to $\mathcal{H}$ and $\|T_n\|=\|x_n\|$ for each $n$.

$x_n\rightharpoonup x_0 \Leftrightarrow (x_n,y)\rightarrow (x_0,y)$ for all $y\in\mathcal{H}$ . So $(x_n,y)$ is bounded for all $y\in \mathcal{H}$.

Then $\sup\|T_ny\|=\sup(x_n,y)<\infty$ for all $y\in \mathcal{H}$.

By the Banach-Steinhaus uniform boundedness principle, $\sup\|T_n\|<\infty$, thus $\sup\|x_n\|<\infty$, i.e. $(x_n)_{n\ge1}$ is bounded.

# Proposition:

Now, I'm going to state the proposition and prove it.

## Statement: 

$\mathcal{H}$ is a Hilbert space, $(x_n)_{n\ge1},x_0 \in \mathcal{H}$. $x_n\rightharpoonup x_0$ as $n\rightarrow \infty$ and $K$ is a compact operator from  $\mathcal{H}$ to $\mathcal{H}$, then $Kx_n\rightarrow x_0$. 

## Proof:

Suppose that $Kx_n$ doesn't converge to $Kx_0$, then there will be an $\varepsilon>0$ such that $(Kx_n)\setminus B(x_0,\varepsilon)$ has infinitely many entries, denoted  $(Kx_n)\setminus B(x_0,\varepsilon)$ as $(Kx_{n_j})$. Since $x_n \rightharpoonup x_0$, by lemma2, $(x_n)$ is bounded. Since $K$ is compact, $(Kx_n)$ must be precompact, then $(Kx_{n_j})$ would has a subsequence $(Kx_{n_{j_k}})$ converges to some point $x\in\mathcal{H}$. Moreover, $\|x-Kx_0\|\ge \varepsilon$.

Since $Kx_{n_{j_k}}\rightarrow x$ as $k\rightarrow\infty$, $Kx_{n_{j_k}}\rightharpoonup x$ as $k\rightarrow\infty$. 

For any $x\in\mathcal{H}$,
$$
\begin{align*}
(x,Kx_{n_{j_k}}-Kx_0)&=(x,K(x_{n_{j_k}}-x_0))\\
&=(K^*x,x_{n_{j_k}}-x_0)\\
&=0
\end{align*}
$$
as $k\rightarrow \infty$ by the weak convergence of $x_n$. Then, $Kx_{n_{j_k}}\rightharpoonup Kx_0$.

By the uniqueness of weak limit, $Kx_0 =x$, which is contradictory to $\|x-Kx_0\|\ge \varepsilon$.

Therefore, what we supposed is wrong, i.e. $Kx_n$ doesn't converge to $Kx_0$.

# Consequences

This proposition is so beautiful! So what? I'm going to provide an example of an application here.

## Statement:

$\mathcal{H}$ is a Hilbert space, $(x_n)_{n\ge1},x_0,(y_n)_{n\ge1},y_0 \in \mathcal{H}$. $x_n\rightharpoonup x_0$ as $n\rightarrow \infty$ and $K$ is a compact operator from  $\mathcal{H}$ to $\mathcal{H}$, then $(x_n,Ky_n)\rightarrow(x_0,Ky_0)$ as $n\rightarrow\infty$. 

## Proof:

By the proposition above, $Ky_n$ converges to $Ky_0$, then
$$
\begin{align*}
\left|(x_n,Ky_n)-(x_0,Ky_0)\right|&=\left|(x_n,Ky_n-Ky_0)+(x_n,Ky_0)-(x_0-x_n,Ky_0)-(x_n,Ky_0)\right|\\
&=\left|(x_n,Ky_n-Ky_0)-(x_0-x_n,Ky_0)\right|\\
&\le\left|(x_n,Ky_n-Ky_0)\right|+\left|(x_0-x_n,Ky_0)\right|\\
&\le\|x_n\|\|Ky_n-Ky_0\|+\left|(x_0-x_n,Ky_0)\right|\\
&\rightarrow0
\end{align*}
$$
as $n\rightarrow\infty$. This implies $(x_n,Ky_n)\rightarrow(x_0,Ky_0)$ as $n\rightarrow\infty$. 
