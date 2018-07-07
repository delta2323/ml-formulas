# Hypercontractive不等式

## ステートメント

関数$f\colon\{-1,1\}^n \to \mathbb{R}$と実数$\rho \in [-1,1]$に対し，
$$
T_\rho f(x)=\mathbb{E}_{y∼N_\rho(x)}[f(y)]
$$
と定義する．
ここで$y∼N_\rho(x)$とは，各$i \in \{1,\ldots,n\}$について独立に
$$
y_i = \begin{cases}
x_i & \text{確率 } \frac{1+\rho}{2}\\
-x_i & \text{確率 } \frac{1-\rho}{2} \\
\end{cases}
$$
と選ぶことを指す．

このとき関数$f: \{-1,1\}^n \to \mathbb{R}$と，$0 \leq \rho \leq \sqrt{\frac{p-1}{q-1}}$なる実数$1 \leq p \leq q \leq \infty$に対して，
$$
\|T_\rho f\|_q \leq \|f\|_p 
$$
が成り立つ．

## 出典

* R. O'Donnell. Analysis of Boolean Functions (2014).
