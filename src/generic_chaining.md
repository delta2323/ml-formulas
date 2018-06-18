# Generic chaining

## ステートメント

### 準備

$(T, d)$ を距離空間とする．

$T$ の部分集合 $A$ の直径を $\mathrm{diam}(A) = \sup_{s, t \in A} d(s, t)$ と表す．

$T$ の分割 $\mathcal{A}$ とは，互いに交わらない $T$ の有限個の部分集合の族 $\mathcal{A} = \\{ A_1, \ldots, A_m \\}$ で，$\bigcup_i A_i = T$ となるものである．$T$ の分割 $\mathcal{A}$ および点 $t \in T$ に対して，$\mathcal{A}(t)$ によって $t$ を含む $\mathcal{A}$ の唯一の要素を表すとする．

$T$ の分割からなる列 $\mathcal{A}_0, \mathcal{A}_1, \ldots$ がネストしているとは，任意の $k \geq 1$ に対して，$\mathcal{A}_k$ が $\mathcal{A}_{k - 1}$ の細分になっていることをいう．分割の列 $\mathcal{A}_0, \mathcal{A}_1, \ldots$ がTalagrand列 (または許容列) であるとは，任意の $k \geq 1$ に対して，$\mathcal{A}_k$ の要素数について
$$
1 \leq |\mathcal{A}_k| \leq 2^{2^k}
$$
が成り立つこととする．

以上の用語のもとで，$\gamma_2(T, d)$ を
$$
\inf_{\\{ \mathcal{A}_k \\}_{k \geq 0} }
\sup_{t \in T} \sum_{k = 0}^\infty 2^{k/2} \mathrm{diam}(\mathcal{A}_k(t))
$$
によって定義する．ただし，infはすべてのTalagrand列の全体にわたってとる．

### 定理の主張

$(T, d)$ を距離空間として，確率過程 $\\{ X_t: t \in T \\}$ を距離 $d$ に関するsub-Gaussian processとする．つまり，任意の $s, t \in T$ と $u > 0$ に対して
$$
\mathbb{P}(|X_s - X_t| \geq u)
\leq 2 \exp \left( - \frac{u^2}{2 d(s, t)^2} \right)
$$
が成り立つものとする．

このとき，
$$
C_1 \gamma_2(T, d) \leq
\mathbb{E} \sup_{t \in T} X_t
\leq C_2 \gamma_2(T, d)
$$
が成り立つ．ただし，$C_1, C_2 > 0$ は普遍的な定数である．


## コメント

- (劣)ガウス過程の最大値の期待値について，定数倍を許してタイトな上下界を与えた定理．Majorizing measure theoremともいう (Talagrand (2014), Theorem 2.4.1).
- これに対して，[Dudleyのエントロピーバウンド](chaining.md) および [Sudakov minoration](sudakov_minoration.md) によって得られる上下界はタイトでない例が存在する．例えば，$T$ が $\mathbb{R}^m$ の楕円体であるとき，Dudleyのバウンドよりも本質的によい上界が存在する (Talagrand (2014), Section 2.5).$T$ が $\mathbb{R}^m$ の部分集合のとき，Dudleyのバウンドによる上界は，最適なものと比較すると高々 $O(\log (m + 1))$ のギャップを生じうる．


## 出典

- Talagrand. Upper and Lower bound for Stochastic Processes. Springer, 2014.
- Dudley. Uniform Central Limit Theorems. 2nd edition (2014).
