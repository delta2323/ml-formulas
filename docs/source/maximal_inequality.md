# 最大不等式

## ステートメント (sub-Gaussian)

$X_1, \ldots, X_n$ は分散パラメータ $\sigma_i^2$ ($i = 1, \ldots, n$) をもつsub-Gaussian確率変数であるとする．このとき，
$$
\mathbb{E} \max_{1 \leq i \leq n} X_i \leq \sqrt{2 \log n} \max_{i} \sigma_i^2
$$
および
$$
\mathbb{E} \max_{1 \leq i \leq n} |X_i| \leq \sqrt{2 \log 2n} \max_{i} \sigma_i^2
$$
が成り立つ．

## ステートメント (chi-squared)

$X_1, \ldots, X_n$ は，互いに独立とは限らない自由度 $p$ のカイ二乗確率変数とする．このとき，
$$
\mathbb{E} \max_{1 \leq i \leq n} X_i \leq p + 2 \sqrt{p \log n} + 2\log n
$$
が成り立つ．

## コメント

- 有限個の確率変数の最大値に関するバウンドを最大不等式と呼ぶことがある．一般論については，Boucheron, et al. (2013) Section 2.5などを参照．
- $n$ 個のsub-Gaussian確率変数の最大値の期待値は，相関の有無にかかわらず $O(\sqrt{\log n})$ で上から抑えることができる．
- カイ二乗分布の最大不等式は，sub-Gamma確率変数に関する最大不等式の特別な場合である (Boucheron, et al. (2013) Corollary 2.6).
- 無限集合への拡張については[Dudleyのエントロピーバウンド](dudley_entropy_bound.md)を参照．
- 最大値の期待値どうしの大小比較は[Slepianの不等式](slepian_inequality.md)を参照．

## 出典

Boucheron et al. Concentration inequalities: A Nonasymptotic Theory of Independence (2013)
