# Efron-Steinの不等式

## ステートメント
$\mathcal{X}$を測度空間，$X_1, \ldots, X_N$を$\mathcal{X}$に値を取る独立な確率分布，$f: \mathcal{X}^N\to \mathbb{R}$を2乗可積分な関数とする．
$Z=f(X_1, \ldots, X_N)$ とすると，

$$
\mathrm{Var}(Z) \leq \frac{1}{2} \sum_{i=1}^N \mathbb{E}\left[(Z - Z_i)^2\right].
$$

ここで， $X_i'$を$X_i$の独立なコピーとし， $Z_i = f(X_1, \ldots, X_i', \ldots, X_N)$とした．

## 証明の概要
Boucheron et al. (2013)3章では，

$$
\Delta_i = \mathbb{E}\_i Z - \mathbb{E}\_{i-1}Z
$$

によりDoobマルチンゲール列を構成し，$Z$の分散が$\Delta_i$達の分散の和で書けることから証明している．
ここで$\mathbb{E}_i$は$X_1, \ldots, X_i$で条件づけた期待値である．

## コメント
* $f$の2乗可積分性の仮定は分散を定義するために課している．
* 入力に同分布性を仮定しない点が[Gauss集中不等式](gaussian_concentration_inequality.md)などと異なる．
* Efron-Steinでは$Z$の分散を評価することはできるが，Gauss不等式のように分布の裾が指数的に減少することを示すことためのには使えない（Boucheron et al. (2013)6章）． 
同分布性を仮定せずに分布の裾の指数的減少を評価する方法として，Bounded difference inequality,
Modified Log-Sobolev不等式を用いたEntropy methodから得られる種々の不等式や，関数$f$に凸性などのさらなる仮定を課す方法などが知られている．

## 出典
* Boucheron et al. Concentration inequalities: A Nonasymptotic Theory of Independence (2013)
