# ステートメント
$X$をパラメータ$v$のポアソン分布とする，$Y=X-v$の生成母関数の対数$\psi_{Y}(\lambda) :=  \mathbb{E} e^{\lambda (Y)}$は

$$
\psi_{Y} (\lambda) = v\phi(\lambda),
$$
ここで，$\phi(u) := e^u-u-1$である．さらに，$\psi_Y$のCramer変換，$\psi_Y^{\ast}(t) := \sup_{\lambda>0} e^{\psi_Y (\lambda) -\lambda t}$ は

$$
\psi_Y^{\ast}(t) = vh\left(\frac{t}{v}\right)
$$
である，ここで$h(u) := (1+u)\log (1+u) - u (u>0)$である．

# コメント
* [Bennetの不等式](bennett_inequality.md)の証明にこの事実を使える

# 出典
Boucheron et al. Concentration inequalities: A Nonasymptotic Theory of Independence (2013)
