# Efron--Steinの不等式

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
\Delta_i := \mathbb{E}_i Z - \mathbb{E}_{i-1}Z
$$

によりDoobマルチンゲール列 $\\{\Delta_i \\}_{i=1}^N$を構成し，$Z$の分散が$\Delta_i$達の分散の和で書けることから証明している．
ここで$\mathbb{E}_i$は$X_1, \ldots, X_i$で条件づけた期待値である．

## コメント
* $f$の2乗可積分性の仮定は分散を定義するために課している．
* $\mathrm{Var}^{(i)}$を$X^{(i)} := (X_1, \ldots, X_i, X_{i+1}, \ldots X_N)$で条件づけた分散，すなわち，$\mathrm{Var}^{(i)}(Z) := \mathbb{E}^{(i)}\left[ (Z - \mathbb{E}^{(i)}Z)^2 \right]$とした時（ここで，$\mathbb{E}^{(i)}$は$X^{(i)}$で条件づけた期待値），ステートメントの右辺は$\sum_{i=1}^N \mathbb{E}\left[ \mathrm{Var}^{(i)} (Z) \right]$と書ける（元のステートメントと異なり，係数$1/2$がないことに注意）．従って，Efron--Steinの定理は一定の条件で分散が劣加法性を持つことを主張していると見ることもできる．
* 入力確率変数達に同分布性は仮定しないが独立性は仮定する．独立性は仮定せずに分散を評価する方法としてGauss--Poincare不等式があるが，これは同分布性より更に強く，入力確率変数達は標準正規分布であることを仮定している．
* Efron--Steinでは$Z$の分散を評価することはできるが，分布が指数的に減少することを示すことためのには使えない（Boucheron et al. (2013) 6章）．


## 出典
* Boucheron et al. Concentration inequalities: A Nonasymptotic Theory of Independence (2013)
