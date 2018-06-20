# ML Formulas
理論計算科学・機械学習・統計学などに出てくる等式・不等式を集めていきます

# 運用方法

GitHubのIssueで管理しています．1つのトピック（不等式・等式・定理など）に対して1つのMarkdownファイルを用意し，そこに「ステートメント」「証明の概要」「コメント」「出典」などを簡潔にまとめます．

# How to contribute

* ほしいエントリがある場合は「Issues」から新たなIssueから希望を挙げてください（エントリのドラフトもあるとベターです）
* 既にあるエントリで誤植を見つけた場合にはIssueとして登録するか，Pull Requestで修正を送ってください．


# 今後やりたいこと

* Twitter Bot化

# 今後登録を検討している数式リスト

Contribution welcome!

* 機械学習・統計的学習理論
  * 集中不等式
    * [Markovの不等式](src/markov_inequality.md)
    * [Chebyshevの不等式](src/chebyshev_inequality.md)
    * [Chernoff bound](src/chernoff_bound.md)
    * [Hoeffdingの不等式](src/hoeffding_inequality.md)
    * [Bennetの不等式](src/bennett_inequality.md)
    * [Bernsteinの不等式](src/bernstein_inequality.md)
    * Azuma's inequality
    * Talagrand's inequality
    * Gaussian concentration inequality
    * [Dudleyのエントロピーバウンド](src/dudley_entropy_bound.md)
    * [Sudakov minoration](src/sudakov_minoration.md)
    * Symmetrization
    * [最大不等式](src/maximal_inequality.md)
    * Efron-Stein's inequality
    * Sub-additivity of entropy
    * McDiarmid's inequality
  * Donsker's variational representation of KL divergence
  * log Sobolev inequality
  * Isoperimetric inequality
  * 凸幾何学
    * [Brunn-Minkowskiの不等式](src/brunn_minkowski_inequality.md)
    * [Prekopa-Leindlerの不等式](src/prekopa_leindler_inequality.md)
  * 情報理論
    * Fano inequality
    * Le Cam inequality
    * Data processing inequality
    * Strong data processing inequality
  * 凸解析
    * Jensen's inequality
    * 種々の双対定理
    * KKT条件 (学習理論のバウンドを出すときに0次最適性よりタイトになる傾向)
    * Luo-Tseng error bound
    * Lojasiewicz不等式
* 確率論
  * [Slepianの不等式](src/slepian_inequality.md)
  * Gaussian correlation inequality
  * [Berry--Esseenの定理](src/berry_esseen_univariate.md)
  * [Dvoretzky--Kiefer--Wolfowitzの不等式](dvoretzky_kiefer_wolfowitz_inequality.md)
* 確率過程・確率微分方程式
  * Doobの不等式
  * Borel-Cantelliの定理
  * Levyの不等式
  * 重複対数の法則
* 統計学
  * Cramer-Rao bound系 (オリジナル1変数版，Bhattacharya)
  * Muirheadの不等式
  * Steinのパラドックス
  * ミニマックスリスク >= ベイズリスク
  * 分類問題のBayes errorをBhattacharya affinityとかchi^2-divergenceで抑えるもの (名前不明)
* 関数解析
  * Holder inequality
  * Sobolev embedding
  * Fatou's lemma
  * 優収束定理
  * 単調収束定理
  * 項別微分
  * 期待値を確率の積分で表示
  * Kinchin-type inequality
  * Poincare inequality
* 線形代数
  * Min-max theorem
  * Cauchy's interacing theorem
* elementaryな不等式
  * 1 + x =< e^x, a^2 + b^2 >= abのような時々使う不等式
* スペクトル理論
  * Cheeger inequality
* Majorization inequality系
* Koksma-Hlawka inequality (quai-Monte Carlo法に関係)
