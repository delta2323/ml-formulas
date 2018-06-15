# ステートメント
$X_1, \ldots, X_N$を独立な確率変数であり，$\mathbb{E}X_i^2 < \infty$かつ，ある$b > 0$が存在して$X_i < b$ a.s. であると仮定する．
$S = \sum_{i=1}^{N} X_i$とすると，任意の$t>0$に対して，

$$
\mathbb{P}\left(S \geq t\right) \leq \exp\left( -\frac{t^2}{2(v + \frac{bt}{3})} \right)
$$

が成立する．ここで，$h(u) = (1+u)\log (1+u) - u (u>0)$である．

# 証明の概要

[Bennettの不等式](bennett_inequlity.md)と不等式
$$
h(u) \geq \frac{u^2}{2(1 + \frac{u}{3})}
$$
から導かれる．

# 出典

Boucheron et al. Concentration inequalities: A Nonasymptotic Theory of Independence (2013)
