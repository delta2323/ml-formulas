# Chernoff Bound

## ステートメント

$X$を確率変数とする，任意の$t>0$と$\lambda \in \mathbb{R}$に対して
$$
\mathbb{P}\\{ |X - \mathbb{E}X| \geq t\\}  \leq e^{\psi_{X}(\lambda)-\lambda t}.
$$
ここで，$\psi_{X}$は$X$の生成母関数の対数，$\psi_{X}(\lambda):=\log \mathbb{E}\left[e^{\lambda X} \right]$．

## 証明の概要
[Markovの不等式](markov_inequality.md)から証明できる

## コメント
この不等式により，期待値周りの確率集中は生成母関数の対数$\psi_X$を評価することに帰着される

## 出典
Boucheron et al. Concentration inequalities: A Nonasymptotic Theory of Independence (2013)
