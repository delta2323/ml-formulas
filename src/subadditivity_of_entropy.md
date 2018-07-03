# エントロピーの劣加法性

## ステートメント

$\mathcal{X}$を測度空間，$X_1, \ldots, X_N$を$\mathcal{X}$に値をとる独立な確率分布，$f\colon \mathcal{X}^N \to [0, 1]$を可測関数とし，$Z = f(X_1, 
\ldots, X_N)$とする．

$Z$のエントロピー$\mathrm{Ent}(Z)$と$X_1, \ldots, X_{i-1}, X_{i+1}, \ldots, X_{N}$で条件づけたエントロピー$\mathrm{Ent}^{(i)}(Z)$をそれぞれ

$$
\mathrm{Ent}(Z)\colon = \mathbb{E}\left[\Phi(Z)\right] - \Phi(\mathbb{E}Z)\\\\
\mathrm{Ent}^{(i)}(Z)\colon = \mathbb{E}^{(i)}\left[\Phi(Z)\right] - \Phi(\mathbb{E}^{(i)}Z)
$$

と定義する．ここで，$\mathbb{E}^(i)$は，$X_1, \ldots, X_{i-1}, X_{i+1}, \ldots, X_{N}$で条件づけた期待値（すなわち，$X_i$についてのみ期待値を取る），$\Phi(x) \colon = x\log x (x\geq 0)$である（$0\log 0=0$と約束する）．
この時，

$$
\mathrm{Ent}(Z) \leq \sum_{i=1}^N \mathbb{E}\left[ \mathrm{Ent}^{(i)} Z\right]
$$

が成立する．

## 証明の方針

$\mathcal{X}$が有限集合の場合には，$(X_1, \ldots, X_N)$の分布関数$p$と$q\colon = fp$のKLダイバージェンスにHanの不等式を適用することで得られる．一般の場合には，エントロピーのvariational formulaを経由して示せる(Boucheron et al. 2013)4章．

## コメント

* 確率測度$P$と$P$に絶対連続な確率測度$Q$に対して，$Q$の$P$に関するKLダイバージェンス（相対エントロピー）$\mathrm{KL}(Q\|P)=\mathrm{Ent}\left(\frac{dP}{dQ} \right)$である．この意味で$$一般化
* エントロピーを定義するのに用いた$\Phi(x)=x\log x$を，「アファイン関数」または「$\Phi''>0$かつ$1/\Phi''$が凹」な2階微分な関数$\Phi$に一般化することで$\Phi$-エントロピーが定義でき，通常のエントロピーと同様に劣加法性が成立する（Rafał and Oleszkiewicz 2000）．

## 出典
* Boucheron et al. Concentration inequalities: A Nonasymptotic Theory of Independence (2013)
* Latała Rafał, and Krzysztof Oleszkiewicz. "Between sobolev and poincaré." Geometric aspects of functional analysis. Springer, Berlin, Heidelberg, 2000. 147-168.
