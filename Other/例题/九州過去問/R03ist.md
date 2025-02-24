---
tags:
  - 過去問
  - 例题
dlink:
  - "[[R03ist.pdf]]"
datetime: 2024-12-10 01:22:51
---
# 数学
## 線形代数
$n \times m$ 実行列 $A \in \mathbb{R}^{n \times m}$ の第 $j$ 列 ($j = 1, 2, \dots, m$) を $a_j \in \mathbb{R}^n$ とする。  
各部分集合 $J \subseteq \{1, 2, \dots, m\}$ について、その要素数を $|J|$ で表し、$a_j \ (j \in J)$ を $j$ に関する昇順で左から並べて得られる $A$ の部分行列を $A[J] \in \mathbb{R}^{n \times |J|}$ で表す。  
このとき、以下の問いに答えよ。
1. 以下の行列 $A$ に対し、$\{a_j | j \in J\}$ が線形独立であるような部分集合 $J \subseteq \{1, 2, 3, 4, 5, 6\}$ をすべて求めよ。
   $$
   A =
   \begin{pmatrix}
   1 & 0 & 0 & -2 & 0 & 0 \\
   0 & 1 & 0 & -2 & -3 & -5 \\
   -2 & -2 & 0 & 4 & 6 & 0
   \end{pmatrix}
   $$
2. (1) の行列 $A$ に対し、$rank(A[J]) < |J|$ を満たす部分集合 $J \subseteq \{1, 2, 3, 4, 5, 6\}$ であって、$J$ の任意の真部分集合 $I \subset J$ について $rank(A[I]) = |I|$ が成り立つものをすべて求めよ。ただし、空集合 $\emptyset$ に対しては $rank(A[\emptyset]) = 0$ と定義する。
3. 一般の $A \in \mathbb{R}^{n \times m}$ について、$I \subseteq J \subseteq \{1, 2, \dots, m\}$ かつ $rank(A[J]) = |J|$ のとき、$rank(A[I]) = |I|$ が成り立つことを示せ。

---
## 微分積分
$\mathbb{R}^2$ 上の関数
$$
f(x, y) = (x + y) \exp\left(-\frac{x^2 + y^2}{2}\right)
$$
について次の各問いに答えよ。
1. $f$ の停留点を全て求めよ。
2. $f$ の極大点と極小点を全て求めよ。
3. $f$ の最大値または最小値が存在する場合、それらを求めよ。

## 微分方程式
次の微分方程式の一般解を求めよ。
$$
\frac{dy}{dx} = \frac{x^2 + 6y^2}{4xy}
$$
$$
\frac{dy}{dx} = e^{2x + y + 1} - 1
$$

---
![[R03-数学-向量分析#ベクトル解析]]

---
![[R03-数学-复素数#複素関数論]]

---
![[R03-数学-概率统计#確率・統計]]


---
# 选修

## 情報理論

![[R03-B-問1#問1]]

![[R03-B-問2#問2]]

---
## オートマトンと言語
![[R03-C-問1#問1]]

![[R03-C-問2#問2]]