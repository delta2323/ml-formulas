# Brunn--Minkowskiの不等式

## ステートメント

$\mu$ を $\mathbb{R}^n$ のLebesgue測度とする．$A, B \subseteq \mathbb{R}^n$ を空でないコンパクト集合とし，$\lambda \in [0, 1]$ とする．このとき
$$
\mu( (1 - \lambda) A + \lambda B)^{1/n} \geq (1 - \lambda) \mu(A)^{1/n} + \lambda \mu(B)^{1/n}
$$
が成り立つ．ただし，集合 $A, B \subseteq \mathbb{R}^n$ に対して，$A + B$ はMinkowski和を表し，$\lambda A = \\{ \lambda x: x \in A \\}$ とする．

## コメント

凸幾何における基本的な不等式のひとつ．(TODO: 応用例)

## 証明の概要

$\lambda = 1/2$，$n = 1$ とした不等式 $\mu(A + B) \geq \mu(A) + \mu(B)$ は容易に示すことができる．多次元の場合は，[Prekopa--Leindlerの不等式](prekopa_leindler.md)を経由する方法が知られている (Boucheron, Lugosi and Massart (2013)).

## 出典

Boucheron et al. Concentration inequalities: A Nonasymptotic Theory of Independence (2013)
