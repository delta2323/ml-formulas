# Fanoの不等式

## ステートメント

$\mathcal{X}$, $\mathcal{Y}$ を有限集合とする．$X, \hat{X}$ は $\mathcal{X}$ に値をとる確率変数，$Y$ は $\mathcal{Y}$ に値をとる確率変数であって，$X \to Y \to \hat{X}$ はマルコフ連鎖であるとする．

$H(X \mid \hat{X})$ は条件つきエントロピーとする．$p \in [0, 1]$ に対して $h(p) := -p \log p - (1 - p) \log (1 - p)$ とおく．

このとき，
$$
h(\mathbb{P}(X \neq \hat{X})) + \mathbb{P}(X \neq \hat{X}) \log_2 |\mathcal{X}|
\geq H(X \mid \hat{X}) \geq H(X \mid Y)
$$
が成り立つ．

## コメント

* $h(0) = h(1) = 0$ と定義する．
* 情報理論，学習理論における基本的な不等式のひとつである．

## 出典

* T. M. Cover and J. A. Thomas. Elements of Information Theory. 2nd edition. Wiley, (2006).
* A. B. Tsybakov. Introduction to Nonparametric Estimation. Springer, (2009).
* B. Yu. Assouad, Fano, and Le Cam. In Festschrift for Lucien Le Cam, Springer, 1997.
