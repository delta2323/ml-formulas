# Dvoretzki--Kiefer--Wolfowitzの不等式 (DKW不等式)

## ステートメント

$X$ を $\mathbb{R}$ に値をとる任意の確率変数とし，$F: \mathbb{R} \to [0, 1]$ をその分布関数とする．$X_1, \ldots, X_n$ を $X$ の独立なコピーとして，$F_n$ をそれらの経験分布関数とする．このとき，ある定数 $0 < C < +\infty$ が存在して，任意の $t > 0$ に対して
$$
\mathbb{P}(\sqrt{n} \sup_{x \in \mathbb{R}} |F_n(x) - F(x)| > t) \leq C \exp( - 2 t^2)
$$
が成り立つ．

## コメント

Massart (1990) によると，DKW不等式は $C = 2$ で成り立つ (Dudley (2014))．

DKW不等式は，i.i.d.確率変数の分布関数に対する一様大数の法則 (Glivenko--Cantelliの定理) の有限サンプル版といえる．ちなみに，$x \in \mathbb{R}$ を固定すると，$|F_n(x) - F(x)|$ の集中不等式は[Hoeffdingの不等式](hoeffding_inequality.md)から示すことができる．

一様中心極限定理の有限サンプル版については，[Berry--Esseenの定理](berry_esseen_univariate.md)を参照．

## 出典

R. M. Dudley. Uniform Central Limit Theorems. 2nd edition (2014).
