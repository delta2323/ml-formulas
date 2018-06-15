# ステートメント

$X_1, \ldots, X_N$が独立な確率変数であり，$X_i$はalmost sureで実数軸上の区間$[a_i, b_i] (a_i \leq b_i)$ に値を取ると仮定する．$S = \sum_{i=1}^{N} X_i$とすると，任意の$t\geq 0$に対し，

$$
\mathbb{P} \\{ S - \mathbb{E}S \geq t \\} \leq \exp\left( - \frac{2 t^2}{\sum_{i=1}^N(b_i - a_i)^2} \right)
$$

# コメント
この定理と「sub Gaussian性の必要十分条件」から，有界で独立な確率変数達の和はsub Gaussianであることがわかる．

# 出典
Boucheron et al. Concentration inequalities: A Nonasymptotic Theory of Independence (2013)
