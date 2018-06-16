# Slepianの不等式

## ステートメント

$X = (X_1, \ldots, X_n)$ と $Y = (Y_1, \ldots, Y_n)$ はそれぞれ平均 $0$ の正規分布を同時分布としてもつ確率変数列とする．$i, j \in \{ 1, \ldots, n \}$ について
$$
\mathbb{E}[X_i^2] = \mathbb{E}[Y_i^2]
$$
および
$$
\mathbb{E}[X_i X_j] \leq  \mathbb{E}[Y_i Y_j]
$$
が成り立つとする．

このとき，
$$
\mathbb{E} \max_{1 \leq i \leq n} Y_i \leq \mathbb{E} \max_{1 \leq i \leq n} X_i
$$
が成り立つ．

## コメント

平均 $0$ のガウス過程 $X_i$ ($i = 1, \ldots, n$) について，分散 $\mathbb{E}X_i^2$ の値が各時刻で同じなら，異なる時刻間の相関が小さいほど最大値の期待値は大きい．

ガウス過程の最大値の期待値どうしを比較したり，下から抑えたいときに役立つ．[Sudakov minoration](sudakov_minoration.md)も参照．
