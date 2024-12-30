---
layout: post
title: 一篇文章搞懂 Jordan 标准型！
categories: 数学
description: 用一篇文章搞明白 Jordan 标准型的核心思路。
keywords: Jordan标准型, 高等代数, 线性代数
---

Jordan 标准型是线性代数中的难点之一，且各种书中的论述往往都十分繁复而抽象，难以理解. 事实上，至今为止我都未能清晰深刻地理解我读过的任何一本数学教材中对此问题的全部逻辑. 本文梳理了一种思路，较为清晰，现分享如下.

注：本文阅读需要的基础有基本的矩阵知识、特征值的知识.

# 不变子空间

让我们从不变子空间讲起：

设线性空间 $$V$$ 上的线性变换 $\mathcal{A}$，若有 $W \subseteq V$ 使得 $\forall \alpha \in W$，有$\mathcal{A}(\alpha)\in W$，则称 $W$ 是 $\mathcal{A}$ 的一个不变子空间. 其中，若 $W = \{0\}$ 或 $W=V$，我们称 W 为**平凡不变子空间**，反之则称为**非平凡不变子空间**.

直观的理解不变子空间，就是将变换“框定”在内部的子空间. 特别的：特征子空间是 $1$ 维的不变子空间.

正因不变子空间“框住”了这个线性变换，我们可以将线性变换限制在这个不变子空间上，记作 $\mathcal{A}\mid_W$.

我们可以将任意一个线性空间分解为若干个不变子空间的直和

$$
\begin{eqnarray*}
V=W_1\oplus W_2\oplus\cdots\oplus W_s
\end{eqnarray*}.
$$

这也就是将线性空间上的一个变换“拆成”若干部分. 特别的，笔者单独约定：如果一个不变子空间不能再拆成两个不变子空间的直和，则称其为**极小不变子空间**.

如果我们把一个线性空间分解为了若干个不变子空间，就相当于我们对它的基做了一个划分。在这样的划分之下，我们应当可以单独操控每一个不变子空间，也就是说；我们能将这个线性变换的矩阵表示写成

$$
\begin{eqnarray*}
\begin{bmatrix}
A_1\\
&A_2\\
&&\ddots\\
&&&A_s
\end{bmatrix}
\begin{bmatrix}
M_1\\
M_2\\
\vdots\\
M_4
\end{bmatrix}
\end{eqnarray*}.
$$

​	其中 $A_i$ 是 $\mathcal{A}\mid_{W_i}$ 的矩阵， $M_i$ 表示以 $W_i$ 的基的向量坐标. 这样一种分块对角化称之为准对角化，这是多么美妙的形状！特别的，当 $W_i$ 都是 $1$ 维的不变子空间，也就是特征子空间时，$\mathcal{A}$ 是可以对角化的，其中 $A_i$ 是对应的特征值.

# 极小不变子空间

我们下面来研究一个极小不变子空间的结构，设 $W$ 是一个 $s$ 维极小不变子空间，限制在上面的线性变换为 $\mathcal{A}$，其矩阵为 $A$.

首先，对于限制在这个极小不变子空间的线性映射的矩阵，它的特征多项式在复数域上一定有解，因而它必然存在一个特征子空间。而每个特征值又有对应的特征子空间，假定它有若干个特征子空间，它就至少可以分解为两个不变子空间的直和，而这与它是极小不变子空间是矛盾的。这就告诉我们：它只有一个特征值 $\lambda_0$，且有且仅有一个特征子空间.

接着让我们观察 $\mathcal{A}$ ，因为 $\mid(\lambda \mathcal{I}-\mathcal{A})\mid=(x-\lambda_0)^s=0$，根据 Hamilton-Caylay 定理（证明可以详细参考《[哈密顿-凯莱定理的三种证明](https://blog.csdn.net/qq_35649707/article/details/104789846)》这篇博文），$(\mathcal{A}-\lambda_0\mathcal{I})^s=0$，也就是说 $(\mathcal{A}-\lambda_0\mathcal{I})$ 是一个幂零变换. 这样，根据 $\mathcal{A}=\lambda_0\mathcal{I}+(\mathcal{A}-\lambda_0\mathcal{I})$，限制在极小不变子空间上的线性变换就可以分解为一个纯粹的缩放变换和一个幂零变换的组合，这是多么的简洁！

我们将此幂零变换记作 $\mathcal{B}$，矩阵为 $B$. 假设其幂零指数为 $m\le s$，即 $\mathcal{B}^m=0$，$\mathcal{B}^{m-1}\not= 0$.  下面我们证明 $m$ 必然等于 $s$：

对于一个幂零变换，易证存在 $\alpha\in W$，使得 $\alpha,\mathcal{B}(\alpha),\cdots,\mathcal{B}^{m-1}(\alpha)$ 线性无关，这样它就成为 $\left\langle\alpha,\mathcal{B}(\alpha),\cdots,\mathcal{B}^{m-1}(\alpha)\right\rangle$ 的一个基，且 $\left\langle\alpha,\mathcal{B}(\alpha),\cdots,\mathcal{B}^{m-1}(\alpha)\right\rangle$ 是 $\mathcal{B}$ 的一个不变子空间，称其为循环子空间.

当 $s=0$ 时，$m=s$. 当 $m=0$ 时，$W=\{0\}$，$s=0$.因而 $m=0\Leftrightarrow s=m$.

当 $s=1$ 时，$m=1$，$s=m$.

当 $s\ge 2$ 时，下设 $1\le m<s$.

1. 当 $s=2$ 时，$m=1$，则取 $\alpha\in W$，有 $\langle\alpha\rangle$ 为一个循环子空间，取 $\beta\in W,\beta\notin\langle\alpha\rangle$，也是一个循环子空间. 因 $W=\langle\alpha\rangle\oplus\langle\beta\rangle$，$W$ 可以分解为两个不变子空间的直和.
2. 假设 $s = k$ 时 $W$ 可以分解为两个不变子空间的直和. 当 $s=k+1$ 时，$W$ 可以分解为 $W=W_1\oplus W'$，其中 $W_1$ 是 $m$ 维循环子空间. 而 $\dim(W')=k+1-m\le k$，因而 $W'$ 是不变子空间. 于是 $W$ 也能分解为两个不变子空间的直和.

由 1、2，根据数学归纳法，当 $s\ge 2$ ， $1\le m<s$ 时，W 一定可以分解为两个不变子空间的直和.

此时，B 就能写成分块对角的形式，而 $A=\lambda_0 I+B$，这样 $A$ 也能写成分块对角的形式，但这和 $W$ 是 $A$ 的一个极小不变子空间是矛盾的，因此我们的假设“$1\le m<s$”是错误的，于是 $s=m$.

如是既证：$m=s$.

这样，限制在极小不变子空间上的线性变换 $\mathcal{A}$ 就分解为了一个纯粹的缩放变换 $\lambda_0\mathcal{I}$ 和一个幂零指数为阶数的幂零变换 $\mathcal{A}-\lambda_0\mathcal{I}$ 的组合. 至此，终点已经近在眼前！

# Jordan块和Jordan标准型

我们已经知道幂零变换 $\mathcal{B}=\mathcal{A}-\lambda_0\mathcal{I}$ 的幂零指数为阶数 $s$，则必然存在 $\alpha\in W$，使得 $\left\langle\alpha,\mathcal{B}(\alpha),\cdots,\mathcal{B}^{s-1}(\alpha)\right\rangle$ 是 $W$ 的一个基，容易看出，$\mathcal{B}$ 在这组基上的矩阵为

$$
\begin{eqnarray*}
\begin{bmatrix}
0&1\\
&0&1\\
&&\ddots&\ddots\\
&&&0&1\\
&&&&0
\end{bmatrix}

\end{eqnarray*}.
$$

而 $\lambda_0\mathcal{I}$ 在其上的矩阵为

$$
\begin{eqnarray*}
\begin{bmatrix}
\lambda_0\\
&\lambda_0\\
&&\ddots&\\
&&&\lambda_0\\
&&&&\lambda_0
\end{bmatrix}

\end{eqnarray*}.
$$

因而 $\mathcal{A}$ 在其上的矩阵为

$$
\begin{eqnarray*}
\begin{bmatrix}
\lambda_0&1\\
&\lambda_0&1\\
&&\ddots&\ddots\\
&&&\lambda_0&1\\
&&&&\lambda_0
\end{bmatrix}

\end{eqnarray*}.
$$

我们称之为一个 **Jordan 块**.

这样，我们就将一个极小不变子空间 $W$ 上的线性变换化为了一个 Jordan 块. 观察 Jordan 块右下角的 $k$ 阶方阵，发现它也是一个 Jordan 块，这就表明它对应了一个 $k$ 维的极小不变子空间. 特别的，右下角的 $\lambda_0$ 对应了 $W$ 的特征子空间，即 $1$ 维的子空间. 这样我们就发现：$m$ 维极小不变子空间中存在一个极小不变子空间的嵌套，使其每一个维数都有一个极小不变子空间，这是多么美妙的结构！（笔者本想通过先证明这一结构，再推出 Jordan 块的形式，结果失败了……）

我们将一个矩阵分块对角化，以使得其每一个分块对应一个极小不变子空间，即

$$
\begin{eqnarray*}
\begin{bmatrix}
A_1\\
&A_2\\
&&\ddots\\
&&&A_s
\end{bmatrix}

\end{eqnarray*},
$$

其每一个分块都可以化为一个 Jordan 分块，将其全部替换得到

$$
\begin{eqnarray*}
\begin{bmatrix}
J_1\\
&J_2\\
&&\ddots\\
&&&J_s
\end{bmatrix}

\end{eqnarray*},
$$

我们将其唤作 **Jordan 标准型**. 在不计 Jordan块排列次序的意义下，Jordan标准型是唯一的.

至此，我们就成功的将一个矩阵化为了 Jordan 标准型，总结如下：

1. 将线性空间划分为线性映射的极小不变子空间的直和，将线性映射写成分块对角矩阵.
2. 将每一分块的（唯一）特征值求出，特征值在主对角线上排列成为伸缩变换，主对角线上方是 1 成为幂零变换，两者之和为该分块的 Jordan 块.
3. 将 Jordan块回代，得到 Jordan 标准型.

# 几种求 Jordan 标准型的路径

不同的书中可能会介绍不同的求解 Jordan 标准型的路径，它们的做法更加抽象，也更具有实操性，但是其核心本质与本文的思路是一样的。常见的求法有**初等因子法**和**特征值法**，但本文不再赘述，详细的可以参考《[若尔当标准型求法](https://blog.csdn.net/Whitecedar/article/details/109703790)》这篇博文.






