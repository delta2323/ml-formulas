# Sudakov minoration

## ステートメント (a)

$T$ を可算集合として，$\\{ X_t: t \in T \\}$ を $T$ で添字づけられた平均0のガウス過程とする．つまり，それぞれの $X_t$ は同じ確率空間で定義された正規確率変数で，$\mathbb{E} X_t = 0$ を満たすものとする．$T$ に $X_t$ から誘導される擬距離 $d_X$ を
$$
d_X(s, t) = \sqrt{\mathbb{E} (X_s - X_t)^2}
$$
のように定める．任意の $\epsilon > 0$ に対して，$M(\epsilon, T, d_X)$ を擬距離 $d_X$ による $T$ の $\epsilon$-パッキングナンバーとする．

このとき，
$$
\mathbb{E} \sup_{t \in T} X_t \geq C \epsilon \sqrt{\log M(\epsilon, T, d_X)}
$$
が成り立つ．ただし，$C > 0$ は普遍的な定数である．

## ステートメント (b)

$\mathbb{R}^d$ の任意の部分集合 $T$ に対して，$T$ のガウス幅 (Gaussian width) を
$$
w(T) := \mathbb{E} \sup_{t \in T} \langle t, Z \rangle
$$
によって定義する．ただし，$Z$ は $d$ 次元の標準正規分布にしたがう確率変数とする．また，$\sup_t$ による可測性の問題はここでは考えないとする．

このとき，任意の $\epsilon > 0$ に対して
$$
w(T) \geq C \epsilon \sqrt{\log M(\epsilon, T, \lVert \cdot \rVert_2)}
$$
が成り立つ．ただし，$C > 0$ は普遍的な定数である．

## コメント

ガウス過程のsupの期待値を，距離エントロピーを使って下からおさえる不等式である．特に，[Dudleyのエントロピーバウンド](dudley_entropy_bound.md)と合わせると，ガウス過程の最大値の期待値は
$$
C_1 \epsilon \sqrt{\log M(\epsilon, T, d_X)} \leq
\mathbb{E} \sup_{t \in T} X_t \leq
C_2 \int_0^\infty \sqrt{\log M(\epsilon, T, d_X)} d \epsilon
$$
のように上下からバウンドできると主張している．直感的には，Dudley積分を，「幅 $\epsilon$」「高さ $\sqrt{\log M(\epsilon, T, d_X)}$」の長方形の面積で近似した形になっている．

Sudakov minorationによる下界はオーダーの意味でタイトではない場合がある．このギャップは[generic chaining](generic_chaining.md)と呼ばれる方法を利用することで埋まる．

ステートメント(b)のように，ガウス幅のオーダーを下から見積もることに役にたつ．

## 出典

- Dudley. Uniform Central Limit Theorems. 2nd edition (2014).
- Gine and Nickl. Mathematical Foundations of Infinite-Dimensional Statistical Models (2015).
