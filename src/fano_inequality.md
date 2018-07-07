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

### (a) 情報理論における応用

直感的には，次のように解釈できる．ある通信路を通して，$\mathcal{X}$ に値をとる情報 $X$ を送信したいとする．通信路には $\mathcal{Y}$ に値をとる「符号」$Y$ を流すことができるが，通信には確率的なノイズが乗ってしまう．条件付き分布は $p(Y \mid X)$ によって与えられるとする．通信路から出力された $Y$ から，もとの情報 $X$ を (確率的に) 復元することを試みて，$\hat{X}$ を作るとする．

誤りの確率 $\mathbb{P}(X \neq \hat{X})$ はなるべく小さくしたい．しかし，通信路の乱雑度 $H(X \mid Y)$ や $H(X \mid \hat{X})$ が大きいほど，正確な復元は難しくなると思われる．これを定量化したのがFanoの不等式である．実際，Fanoの不等式から，$|\mathcal{X}| \geq 2$ のとき，次の下界が成り立つ．
$$
\mathbb{P}(X \neq \hat{X}) \geq \frac{H(X \mid Y) - 1}{\log_2 |\mathcal{X}|}
$$

具体的な応用としては，Shannonの通信路符号化定理 (channel coding theorem) の証明に利用できる．

有限集合 $\mathcal{W}$ を伝達したいメッセージの集合とする．$w$ は次のようなプロセスを経て伝達されるとする．

1. 長さ $n$ の文字列 $x^n = x^n(w) \in \mathcal{X}^n$ に符号化する．
1. 通信路 $P(y^n \mid x^n)$ を通して伝達し，$y^n \in \mathcal{Y}^n$ を得る．
1. $y^n$ から $\hat{w} \in \mathcal{W}$ を復号する．

このとき，上の1と3で利用した符号化 / 復号化におけるレート $R$ を $R = (\log_2 |\mathcal{W}|) / n$ によって定義する．

2では，無記憶通信路 $p(y \mid x)$ を利用して1文字ずつ独立に送ることを考える．この通信路の容量 (capacity) を
$$
C := \max_{p(x)} I(X; Y)
$$
によって定義する．通信路符号化定理の主張を簡単に述べると，達成可能なレート $R$ の上界が通信路容量によって与えられるということである：

1. もし $R < C$ であれば，レートが $R$ である符号化方式が存在して，ワーストケースの誤り確率 $\max_{w} \mathbb{P}(\hat{w} \neq w)$ を $n \to \infty$ において漸近的に0にすることができる．
1. 逆に，レートが $R$ の符号化方式 (の列) が漸近的に誤り確率を0にするのであれば，$R \leq C$ でなければならない．

2の主張の証明にFanoの不等式が利用できる．詳細はCover and Thomas, Chapter 7を参照．

### (b) 学習理論における応用

数理統計や統計的学習理論では，Fanoの不等式はミニマックス下界を導出するための基本的なツールである．

ミニマックス理論で下からバウンドしたいのは次のような量である：

$\mathcal{P}$ を確率分布の集合とする．データ $X$ は，未知の確率分布 $P \in \mathcal{P}$ に従っているとする．このとき，データから計算できる推定量 $\hat{\theta}(X)$ を使って，$P$ に関係するなんらかのパラメータ $\theta(P)$ を推定したい．推定の良さの尺度としては，距離 (のようなもの) $d$ の期待値

$$
\mathbb{E}_P d(\hat{\theta}(X), \theta(P))
$$

ができるだけ小さくなるような推定量 $\hat{\theta}$ が良い，と考えるものとする (慣例にならってリスクと呼ぶ)．ミニマックスリスクとは，「想定している分布の集合 $\mathcal{P}$ の中での最悪の場合のリスクの値」を最小にするような $\hat{\theta}$ のリスクとして定義される:

$$
\mathcal{M} = \inf_{\hat{\theta}} \sup_{P \in \mathcal{P}} \mathbb{E}_P d(\hat{\theta}(X), \theta(P)).
$$

ミニマックスリスク $\mathcal{M}$ を下から抑えたい．もし $\mathcal{P}$ が有限集合であったとすると，$\theta(P)$ を推定する問題は，有限のメッセージの候補 $P_1, \ldots, P_m$ から正しい $P_j$ を復元することと似ているから，問題の難しさはFanoの不等式で記述できそうである．

そこで，一般の $\mathcal{P}$ に対しては，次のように都合のよい離散化がとれるものする．

1. 有限個の $P_1, \ldots, P_m \in \mathcal{P}$ をとる．
1. (距離 $d$ のパッキング条件) すべての $i \neq j$ に対して，$d(\theta(P_i), \theta(P_j)) \geq \alpha$.
1. (分布どうしの見分けにくさ) すべての $i \neq j$ に対して，$D_{\mathrm{KL}}(P_i, P_j) \leq \beta$．

このとき，Fanoの不等式の帰結として，次のような下界が得られる．

$$
\sup_{P \in \mathcal{P}} \mathbb{E}_P d(\hat{\theta}(X), \theta(P))
\geq \max_{j} \mathbb{E}_{P_j} d(\hat{\theta}(X), \theta(P))
\geq \frac{\alpha}{2} ( 1 - \frac{\beta + \log 2}{\log m} ).
$$

詳細については Yu (1997) および Tsybakov (2009), Chepter 2を参照．

## 出典

* T. M. Cover and J. A. Thomas. Elements of Information Theory. 2nd edition. Wiley, (2006).
* A. B. Tsybakov. Introduction to Nonparametric Estimation. Springer, (2009).
* B. Yu. Assouad, Fano, and Le Cam. In Festschrift for Lucien Le Cam, Springer, 1997.
