# ミニマックス理論におけるLe Camの方法

## ステートメント

$\mathcal{P}$ を可測空間 $(\mathcal{X}, \mathcal{A})$ 上の確率測度の集合とする．任意の $P \in \mathcal{P}$ に対して，(擬) 距離空間 $(\Theta, d)$ の値 $\theta(P)$ が対応しているとする．$\hat{\theta}: \mathcal{X} \to \Theta$ を任意の可測写像とする．

2つの確率測度 $P_1, P_2 \in \mathcal{P}$ を，$d(\theta(P_1), \theta(P_2)) \geq 2\delta > 0$ を満たすようにとる．このとき，
$$
\sup_{P \in \mathcal{P}} \mathbb{E}_{P} d(\hat{\theta}, \theta(P)) \geq \delta (1 - d_{\mathrm{TV}}(P_1, P_2)).
$$


## コメント

* ミニマックスリスクを，「2つの仮説 $P_1$, $P_2$ の見分けにくさ」に基づいて下から抑える不等式である．

## 証明の方針

仮説検定の枠組みに基づいた解説はTsybakov (2009)を参照．ここでは，Yu (1997) にならって，より直接的な証明を与える．

$\theta_i := \theta(P_i)$ ($i = 1, 2$) と表す．また，$P_i$ による期待値を $\mathbb{E}_i$ などと書く．

三角不等式より，

$$
d(\hat{\theta}(X), \theta_1) + d(\hat{\theta}(X), \theta_2)
\geq d(\theta_1, \theta_2) \geq 2\delta
$$

である．よって，$i = 1, 2$ に対して

$$
f_i(X) := \frac{d(\hat{\theta}(X), \theta_i)}{2\delta}
$$

とおくと，$f_i$ は非負可測関数で $f_1 + f_2 \geq 1$ が成り立つ．したがって，

$$
\begin{align}
2 \sup_{P \in \mathcal{P}} \mathbb{E}_P d(\hat{\theta}, \theta(P))
& \geq \mathbb{E}_1 d(\hat{\theta}, \theta_1) +
\mathbb{E}_2 d(\hat{\theta}, \theta_2) \\\
& \geq 2 \delta \inf_{f_i \geq 0, f_1 + f_2 = 1}
(\mathbb{E}_1 f_1 + \mathbb{E}_2 f_2 ) \\\
& = 2 \delta (1 - d_{\mathrm{TV}}(P_1, P_2)).
\end{align}
$$


## 出典

* A. B. Tsybakov. Introduction to Nonparametric Estimation. Springer, (2009).
* B. Yu. Assouad, Fano, and Le Cam. In Festschrift for Lucien Le Cam, Springer, 1997.
