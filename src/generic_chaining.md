# Generic chaining

## ステートメント

### 準備

$(T, d)$ を距離空間とする．

$T$ の部分集合 $A$ の直径を $\mathrm{diam}(A) = \sup\_{s, t \in A} d(s, t)$ と表す．

$T$ の分割 $\mathcal{A}$ とは，互いに交わらない $T$ の有限個の部分集合の族 $\mathcal{A} = \\{ A\_1, \ldots, A\_m \\}$ で，$\bigcup\_i A\_i = T$ となるものである．$T$ の分割 $\mathcal{A}$ および点 $t \in T$ に対して，$\mathcal{A}(t)$ によって $t$ を含む $\mathcal{A}$ の唯一の要素を表すとする．

$T$ の分割からなる列 $\mathcal{A}_0, \mathcal{A}\_1, \ldots$ がネストしているとは，任意の $k \geq 1$ に対して $\mathcal{A}\_{k}$ が $\mathcal{A}\_{k-1}$ の細分になっていることをいう．
分割の列 $\mathcal{A}\_{0}, \mathcal{A}\_{1}, \ldots$ がTalagrand列 (または許容列) であるとは，任意の $k \geq 1$ に対して，

$$
1 \leq |\mathcal{A}\_{k}| \leq 2^{2^k}
$$

が成り立つこととする．

以上の用語のもとで，$\gamma\_2(T, d)$ を

$$
\inf \sup\_{t \in T} \sum\_{k = 0}^\infty 2^{k/2} \mathrm{diam}(\mathcal{A}\_{k}(t))
$$

によって定義する．ただし，infはすべてのTalagrand列の全体にわたってとる．

### 定理の主張

$(T, d)$ を距離空間として，確率過程 $\\{ X\_t: t \in T \\}$ を距離 $d$ に関するsub-Gaussian processとする．つまり，任意の $s, t \in T$ と $u > 0$ に対して
$$
\mathbb{P}(|X\_s - X\_t| \geq u)
\leq 2 \exp \left( - \frac{u^2}{2 d(s, t)^2} \right)
$$
が成り立つものとする．

このとき，
$$
C\_1 \gamma_2(T, d) \leq
\mathbb{E} \sup\_{t \in T} X\_t
\leq C\_2 \gamma\_2(T, d)
$$
が成り立つ．ただし，$C\_1, C\_2 > 0$ は普遍的な定数である．


## コメント

- (劣)ガウス過程の最大値の期待値について，定数倍を許してタイトな上下界を与えた定理．Majorizing measure theoremともいう (Talagrand (2014), Theorem 2.4.1).
- これに対して，[Dudleyのエントロピーバウンド](chaining.md) および [Sudakov minoration](sudakov_minoration.md) によって得られる上下界はタイトでない例が存在する．例えば，$T$ が $\mathbb{R}^m$ の楕円体であるとき，Dudleyのバウンドよりも本質的によい上界が存在する (Talagrand (2014), Section 2.5).$T$ が $\mathbb{R}^m$ の部分集合のとき，Dudleyのバウンドによる上界は，最適なものと比較すると高々 $O(\log (m + 1))$ のギャップを生じうる．


## 出典

- Talagrand. Upper and Lower bound for Stochastic Processes. Springer, 2014.
- Dudley. Uniform Central Limit Theorems. 2nd edition (2014).
