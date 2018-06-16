# Dudleyのエントロピーバウンド

## ステートメント

Dudley's entropy boundや，chainingと呼ばれている不等式は，(sub)-Gaussian processの最大値の期待値を，カバリングナンバーまたはパッキングナンバーの積分によって上から抑える形の不等式である．

$T$ を可算集合として，$\{ X_t: t \in T \}$ を $T$ で添字づけられた平均0のガウス過程とする．つまり，それぞれの $X_t$ は同じ確率空間で定義された正規確率変数で，$\mathbb{E} X_t = 0$ を満たすものとする．$T$ に $X_t$ から誘導される擬距離 $d_X$ を
$$
d_X(s, t) = (\mathbb{E} (X_s - X_t)^2)^{1/2}
$$
のように定める．任意の $\epsilon > 0$ に対して，$M(\epsilon, T, d_X)$ を擬距離 $d_X$ による $T$ の $\epsilon$-パッキングナンバーとする．

このとき，
$$
\mathbb{E} \sup_{t \in T} X_t \leq C \int_{0}^\infty \sqrt{\log M(\epsilon, T, d_X)} d \epsilon
$$
が成り立つ．ただし，$C > 0$ は普遍的な定数である．

## コメント

上のステートメントは Talagrand (2014), (2.38) 式から取った．

[最大不等式](maximal_inequality.md)を無限集合に拡張したもの．(sub-)Gaussian processの最大値を上から抑えたいときに，添字集合の距離エントロピー (カバリングナンバーやパッキングナンバー) の評価に帰着させることができる．

(sub-Gaussian processの最大値の期待値) $\leq$ (metric entropyの積分) という形の不等式を指して，総称的にDudley's entropy boundと呼ぶことがある．

- $T$ を非可算集合にすることもできる．この場合，厳密には $\sup_{t \in T} X_t$ の部分の可測性を気にする必要がある．
- $X_t$ をsub-Gaussian processにすることもできる．
- Modulus of continuity $\mathbb{E} \sup_{d(s, t) \leq \delta} |X_s - X_t|$ を上からおさえる形のステートメントもある．

下から抑えたいときは[Sudakov minoration](sudakov_minoration.md)がある．

よりタイトな不等式として，[Generic chaining](generic_chaining.md)と呼ばれるものが知られている．

## 出典

- Talagrand. Upper and Lower bound for Stochastic Processes. Springer, 2014.
- van der Vaart and Wellner. Weak Convergence and Empirical Processes. Springer, 1996.
- Gine and Nickl. Mathematical Foundations of Infinite-Dimensional Statistical Models. Cambridge University Press, 2015.
