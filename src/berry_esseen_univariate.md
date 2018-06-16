# Berry--Esseenの定理

## ステートメント

$X_1, \ldots, X_n$ は独立同分布にしたがう確率変数であって，$\mathbb{E} X_1 = 0$, $\mathbb{E} X_1^2 = \sigma^2 < \infty$, $\mathbb{E} |X_1|^3 = \rho < \infty$ を満たすものとする．
$$
S_n = \frac{\sum_{i=1}^n X_i}{\sigma \sqrt{n}}
$$
として，$F_n: \mathbb{R} \to [0, 1]$ を $S_n$ の累積分布関数とする．また，$\Phi: \mathbb{R} \to [0, 1]$ を標準正規分布の累積分布関数とする．

このとき，
$$
\sup_{x \in \mathbb{R}} |F_n(x) - \Phi(x)| \leq \frac{C \rho}{\sigma^3 \sqrt{n}}
$$
が成り立つ．ここで，$C > 0$ は普遍的な定数である．

## コメント

1次元確率変数の中心極限定理がKolmogoriv距離に関して成り立つ，という主張を有限のサンプルサイズで定量化したものである．
