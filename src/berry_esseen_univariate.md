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

中心極限定理の主張は，$S_n$ が標準正規分布に分布収束するというものである．一様中心極限定理とは，この収束がKolmogorov距離
$$
\sup_{x \in \mathbb{R}} |F_n(x) - \Phi(x)|
$$
に関して成り立つということを主張したものである．Berry--Esseenの定理は，一様中心極限定理がさらに有限サンプルで成り立つように定量化を行ったものである．
