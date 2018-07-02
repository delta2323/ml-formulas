# エントロピーの劣加法性

## ステートメント

$\mathcal{X}$を測度空間，$X_1, \ldots, X_N$を$\mathcal{X}$に値をとる独立な確率分布，$f\colon \mathcal{X}^N \to [0, 1]$を可測関数とする．$Z = f(X_1, 
\ldots, X_N)$とする．

$Z$のエントロピー$\mathrm{Ent}(Z)$を$\mathrm{Ent}(Z)\colon = \mathbb{E}\left[\Phi(Z)\right] - \Phi(\mathbb{E}Z)$，$X_1, \ldots, X_{i-1}, X_{i+1}, \ldots, X_{N}$で条件づけたエントロピー$\mathrm{Ent}^{(i)}(Z)$を$\mathrm{Ent}^{(i)}(Z)\colon = \mathbb{E}^{(i)}\left[\Phi(Z)\right] - \Phi(\mathbb{E}^{(i)}Z)$と定義する．ここで，$\mathbb{E}^(i)$は，$X_1, \ldots, X_{i-1}, X_{i+1}, \ldots, X_{N}$で条件づけた期待値である（すなわち，$X_i$についてのみ期待値を取る）．
この時，

$$
\mathrm{Ent}(Z) \leq \sum_{i=1}^N \mathbb{E}\left[ \mathrm{Ent}^{(i)} Z\right]
$$
が成立する．

## コメント

* 

## 出典
Boucheron et al. Concentration inequalities: A Nonasymptotic Theory of Independence (2013)
