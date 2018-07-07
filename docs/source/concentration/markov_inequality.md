# Markovの不等式

## ステートメント

$X$を非負の確率変数とする，任意の$t> 0$に対して

$$
\mathbb{P} (X \geq t) \leq \frac{\mathbb{E}\left[X\right]}{t}
$$
が成り立つ．

## 証明の概要
任意の$t\geq 0$に対して，

$$
X \geq t\mathbb{1}_{\\{X\geq t\\}}
$$
が成り立つので，期待値を取って，

$$
\mathbb{E}\left[X\right] \geq \mathbb{E}\left[t\mathbb{1}_{\\{X\geq t\\}} \right] = t \mathbb{P} (X\geq t).
$$

両辺を$t$で割れば不等式が得られる．

## コメント
* 集中不等式と呼ばれる類の一連の不等式の出発点となる．
* Markovの不等式からChebyshevの不等式やExponential版のChebyshevの不等式が示せる．
* 文献によっては，Chebyshevの不等式のことをMarkovの不等式と呼ぶこともある．

## 出典
Boucheron et al. Concentration inequalities: A Nonasymptotic Theory of Independence (2013)
