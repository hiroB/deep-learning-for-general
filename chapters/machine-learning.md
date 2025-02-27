# 🤖 機械学習

世の中の特定の事象について**データを解析し**、その結果から学習し、**判断や予測を行う**ためのアルゴリズムを使用する手法

機械学習はデータが命。データから答えを探し、データからパターンを見つけ、データからストーリーを語る。
機械学習の中心には「データ」があり、このデータ駆動によるアプローチは、「人」を中心とするアプローチからの脱却とも言える。
重みパラメータの値をデータから自動で計算できる。（ディープラーニング）

## 処理の流れ
機械学習の処理は大きく「学習」と「推論」ステップに分かれる。

##### 学習
事前に与えられたデータからモデルをつくること。
学習が終わったモデルには、学習データの統計的な傾向や規則性が反映されている。

##### 推論
実環境で得られるデータなどを使い、学習済みモデルを使って判定、分類、予測などを行う。

## 特徴量

機械学習の予測モデルに入力する情報。

例えば明日の積雪の有無を予測するために、今日の気温（1.0℃)、降水量(0.8mm)、天気（曇り）使うとすると、それぞれを数値化したもののリスト（ex. [1, 0.8, 1]) が「特徴ベクトル」になります。

ここで、「曇り」のような特徴量を「カテゴリカル変数」と呼び、晴れは 0、曇は 1 というような数値データのことを「ダミー変数」と呼ぶ。

## 代表的な手法

![](https://jp.mathworks.com/discovery/machine-learning/_jcr_content/mainParsys3/discoverysubsection_1965078453/mainParsys3/image_2109075398_cop.adapt.full.high.svg/1591624225922.svg)

[機械学習とは？これだけは知っておきたい3つのこと - MATLAB & Simulink](https://jp.mathworks.com/discovery/machine-learning.html)

##### 代表的な「予測」アルゴリズム

| アルゴリズム | 回帰 | 分類 | クラスタリング |
| :---: | :---: | :---: | :---: |
| 線形回帰 | o | x | x |
| ロジスティック回帰 | x | o | x |
| サポートベクターマシン | o | o | x |
| ナイーブベイズ | x | o | x |
| 決定木 | o | o | x |
| ランダムフォレスト | o | o | x |
| ニューラルネットワーク | o | o | x |
| kNN(k近傍） | o | o | x |
| k-means | x | x | o |

##### scikit-learnのアルゴリズム・チートシート
![](https://scikit-learn.org/stable/_static/ml_map.png)

[Choosing the right estimator — scikit-learn 0.23.1 documentation](https://scikit-learn.org/stable/tutorial/machine_learning_map/index.html)

##### 教師あり学習
教師データ（入力とそれに対応する正解ラベルの組）を使って予測値を正解ラベルに近づけることを目標に学習する手法
自然言語処理、スパムメールフィルタリング、手書き文字認識などの応用がある。

##### 教師なし学習
教師データを使わずに、データの本質的な構造を浮かび上がらせる手法。
クラスタリングやデータ次元圧縮技術などがこれに含まれる。

##### 強化学習
ゴールや目標を仮定せず、学習を行う「エージェント」が状態を観察し、環境からの報酬を最大化するように試行錯誤しながら行動を選択することで学習を行う。
ロボット操作などに使われることが多い。

##### 転移学習
すでにある領域で学習済みのモデルを他の領域に流用する手法。

##### 半教師あり学習
教師あり学習におけるラベル付けコストを低減するために用いられる手法。
データの一部分にのみ正解ラベルをつける。

##### 回帰問題
正解となる数値を入力データの組み合わせで学習し、未知のデータから連続値を予測する。

統計学において、目的変数と説明変数の関係を明らかにすることで、未知のデータ属性の値を既知のデータ属性から予測できる。
（ex. 家賃の高さを広さ、築年数、駅からの近さの値から計算）

入力データが1つの単回帰分析、複数の入力データの重回帰分析などの種類がある。

##### 分類問題
正解となる離散的なカテゴリ（クラス）と入力データの組み合わせ出学h数詞、未知のデータからクラスを予測する。

あらかじめ設定したクラスにデータを割り振る（ex. 画像に写っている犬や猫の識別）。
サポートベクターマシン、決定木、ランダムフォレスト、ロジスティック回帰、kNN法などの手法がある。深層学習でも分類を行うことができる。

##### クラスタリング
データを何かしらの基準でグルーピングする。
分類と違い、事前にクラスなどの分類の軸が提供されないため、与えられたデータの特徴などから自動的にクラスタを構成する。

事前学習が不要なため、過去のデータがない場合でもクラスタ化可能だが、クラスに基づく分類とは異なる結果がでる場合がある。
代表的なアルゴリズムに k-means法などがある。

##### 次元削減
高次元のデータを可視化や計算量削減などのために低次元にマッピングする。

##### 汎化誤差
まだ手に入れていないデータを予測した時の誤差。汎化誤差の小さいということは、機械学習の精度が高いと言える。

- バイアス
  - データとモデルのズレの大きさを示す。モデルが単純すぎて未学習の状態になると高くなる。
  - 複雑なデータへの当てはまりを向上させることで減少する。
- バリアンス
  - モデルの予測のばらつきやすさを示す。モデルが複雑すぎて過学習の状態になると高くなる。 
  - 過去のデータへの当てはまりを過剰に高くしないことで減少する。
- ノイズ
  - データ自体に原因があり、学習の妨げとなるもの。
  - ある程度残るのは仕方がない。

## データの前処理

データをモデルに正しく入力できるようにする。
データの大きさをある程度均一にする。

### 正規化
各成分ごとに平均と分散を揃える。

各成分から平均を引き0に揃える。その後標準偏差で割って分散を1にする。

##### 離散化
![](https://miro.medium.com/max/2000/1*LGTAObYYj2-fdBMFLz30rw.jpeg)
https://heartbeat.fritz.ai/hands-on-with-feature-engineering-techniques-variable-discretization-7deb6a5c6e27

連続した値をある区分にわけること。

##### 対数変換
![](https://www.researchgate.net/profile/Matthieu_Komorowski4/publication/308007227/figure/fig5/AS:405478883512321@1473685107077/[55-Example-of-the-effect-of-a-log-transformation-on-the-distribution-of-the-dataset.png)
https://www.researchgate.net/figure/55-Example-of-the-effect-of-a-log-transformation-on-the-distribution-of-the-dataset_fig5_308007227

値の log（対数）を取る（log に変換する）こと。

正の値をもつ数値データにおいて、長い裾を短く圧縮し、小さい値を拡大することができる。
機械学習では正規分布に近いデータが効果を発揮しやすいため、対数変換は有効な手段の一つ。

##### スケーリング
![](https://kharshit.github.io/img/scaling.png)

https://kharshit.github.io/blog/2018/03/23/scaling-vs-normalization

データを 0 から 1 に収まるようにスケーリングすること。

代表的なスケーリングの方法に「Min-Maxスケーリング」と「標準化」がある。

- Min-Maxスケーリング

  最小値を 0、最大値を 1 にし、データの範囲を 0 ~ 1 に変換する。

- 標準化

  平均を 0、標準偏差（分散）を 1 に変換する。
  対数変換をしてから標準化を行う場合もある。

##### 白色化　　
各特徴量を無相関化した上で標準化する手法。
白色化は計算コストが高いので、標準化を用いるのが一般的。

##### PCA白色化

##### ゼロ位相白色化

##### 基礎集計
データの傾向を事前に把握する。散布図行列をプロットして傾向を調べる。相関行列を表示し傾向を調べる。


## 過学習を抑制する手法

##### 正則化
線形回帰式で利用可能な手法。

学習に用いる式に項を追加することによってとりうる重みの値の範囲を制限し、過度に重みが訓練データに対してのみ調整されることを防ぐ。

（回帰）係数を大きくなりすぎないように自動で調整することで、予測結果を安定化させる。

誤差関数にパラメータのノルムによる正則化（LASSOなど）を付け加える。

##### L1正則化
一部のパラメータの値をゼロにすることで、特徴選択を行うことができる。

線形回帰に対してL1正則化を適応した手法を「[ラッソ回帰](https://ja.wikipedia.org/wiki/%E3%83%A9%E3%83%83%E3%82%BD%E5%9B%9E%E5%B8%B0)」という。
ラッソ回帰は、自動的に「特徴量の選択」が行われる性質を持つ。

##### L2正則化
パラメータの大きさに応じてゼロに近づけることで、汎化されたなめらかなモデルを得ることができる。

線形回帰に対してL2正則化を適応した手法を「リッジ回帰」という。
リッジ回帰は、特徴量選択は行わないが、パタメータのノルムを小さく抑える。

##### [Elastic Net](https://jp.mathworks.com/help/stats/lasso-and-elastic-net.html)
ラッソ回帰とリッジ回帰の両者を組み合わせた手法。

##### 重み上限
重みの上限を制限する。
各ユニットの重みの二乗和に上限を与える。
制約を満たしていない場合、重みに１以下の定数をかけるなどの処理を行う。

ドロップアウトとともに用いると高い精度を示すことが報告されている。

##### 重み減衰
誤差関数に重みの二乗和を加算し、これを最小化する。学習時にはより小さい重みが選好されるようになる。重みは自身の大きさに比例した速さで常に減衰する。

##### スパース正則化
個々の訓練サンプルをなるべく少ない中間層を使って再現するように学習するよう、
誤差関数に制約をかける

## 教師あり学習

### パーセプトロン

入力ベクトルと学習した重みベクトルを掛け合わせた値を足して、その値が0以上のときはクラス1, 0未満のときはクラス2と分類するという、シンプルなアルゴリズム。

過学習しやすく、線形分離可能な問題のみ解ける。

### 誤差逆伝播法（バックプロゲーション）

### 回帰分析

簡単にいうと「データにもっともフィットする線を引くこと」

#### 単回帰分析
1つの説明変数（手がかりとなる変数）から目的変数を予測する。
データと回帰直線との最小二乗法が誤差関数（損失関数）。

※ 説明変数は文脈にとっては特徴量と呼ばれることがある。特徴量の方が少し大きな概念になるが、同じものを指していると考えていい。

#### 重回帰分析
複数の説明変数から目的変数を予測する。
多重共線性に注意する必要がある。

##### 多重共線性
相関係数が高い特徴量の組を同時に説明変数に選ぶと、予測がうまくいかなくなる現象。

多重共線性を避けるには、相関の強い説明変数のどちらか一方を除く。
特徴量エンジニアリングにおいては、多重共線性がでないような特徴量を選ぶ必要がある。

### 用語

##### 相関係数
特徴量同士の相関の正負と強さを表す指標。-1 <= x <= 1。
1に近いほど強い正の相関、-1に近いほど強い負の相関をもつ。0のときは相関がない。

##### 線形分離可能
パーセプトロンを使って解ける問題。2次元のグラフ上で直線を使って分離できる。
論理ゲートでは OR, AND, NAND は線形分離可能だが、XOR のみ線形分離不可能。

### SVM（サポートベクターマシン）

データを最も引き離す境界線を引くための手法で、ディープラーニングを使わない機械学習の中では主流の方法。

##### [SVM (サポートベクターマシン)](https://ja.wikipedia.org/wiki/%E3%82%B5%E3%83%9D%E3%83%BC%E3%83%88%E3%83%99%E3%82%AF%E3%82%BF%E3%83%BC%E3%83%9E%E3%82%B7%E3%83%B3)
「マージン最大化」というコンセプトで2つのクラスを線形分離可能にするアルゴリズム。

もともとは2つのクラス分類アルゴリズムとして考案されたが、性能がいいので多クラス分類や回帰分析にも応用されている。

線形分離可能でないデータに対しても、カーネル法を組み合わせることで決定境界を求めることができる。
未学習のデータに対しても高い識別性能があるが、仮説の設定や特徴の選択が必要。

##### マージン
判別する境界線とデータの距離

##### ハードマージン
AかBかきっちり判別できることを前提としたマージンのこと。
教師データに対して無理に整合性を高めるため、未知のデータに対して精度が下がる（＝過学習を起こす）

##### ソフトマージン
誤判別を許容する前提としたマージンのこと。汎化性を高めるためにあえて誤判別を許容する。

##### [スラック変数](http://sudillap.hatenablog.com/entry/2013/04/08/235602)
超平面を構成した結果として発生する誤差の程度を測る変数。
SVMにおいてソフトマージンを導入するのに用いられる。

##### [ハイパーパラメータ](https://ja.wikipedia.org/wiki/%E3%83%8F%E3%82%A4%E3%83%91%E3%83%BC%E3%83%91%E3%83%A9%E3%83%A1%E3%83%BC%E3%82%BF)
推論や予測の枠組みの中で決定されないパラメータ。
SVM においては誤りをどの程度許容するかの度合いをエンジニアが事前に調整する必要がある。

##### グリッドサーチ
適切だと考えられるパラメータを複数用意し、それらの値の組み合わせを全通り総当たりで行い、最も良いハイパーパラメータを探す方法。

##### ランダムサーチ
考えられるパラメータの範囲を決め、ランダムにパラメータを組み合わせて学習させ、最も良いハイパーパラメータを探す方法。

##### ナイーブベイズ（単純ベイズ）
各要素（説明変数）が独立に予測に影響を与えていると仮定して、最もその分類が発生する確率が高いものを予測とする。
文章の単語をベースにした分類などに使われる。

##### ベイズ最適化
過去の試行結果から次に行う範囲を確率分布を用いて計算する手法。

ハイパーパラメータを含め最適化問題とする方法で、近年、効率的なチューニング方法として注目されている。

##### [カーネル法](https://ja.wikipedia.org/wiki/%E3%82%AB%E3%83%BC%E3%83%8D%E3%83%AB%E6%B3%95)
派閥の境界が非線形になっている場合に用いる手法。

データから新しい特徴量をつくって、線形分離可能になるようにプロットしなおす。

次のアイディアをカーネル関数の計算によって実現するもの。
- データを高次元空間にうまく埋め込む
- 高次元空間で線形分離 (SVM) し、その境界を元の空間に戻す

##### カーネルトリック
カーネル関数を使って、計算複雑度の増大を抑えつつ内積にもとづく解析手法を高次元特徴空間へ拡張するアプローチ。
計算量を現実的に抑えつつ、非線形分離を実現する。

### 決定木
![](https://s3-ap-southeast-1.amazonaws.com/he-public-data/XOR%203df51ae5.png)

https://www.hackerearth.com/ja/practice/machine-learning/machine-learning-algorithms/ml-decision-tree/tutorial/

Yes or No で答えられる条件によって予測を行う手法。

人間の思考プロセスに近い方法のため、結果がわかりやすいのが特徴。

##### 決定木
性質（ex. 男女）や数値（ex. 購入数5個以上/未満）に基づき、データを木構造に分類する手法。予測にも使える。

人が理解しやすく前処理が少なくてすむ（データのスケールを事前に揃えておく必要がない）が、データに対する条件分岐が複雑になりやすく、過学習を起こしやすい。

1. 不純度が最も減少（情報利得が最も増加）するように、条件分岐を作りデータを振り分ける
1. それを繰り返す

不純度とは「クラスの混じり具合」を表す指標で、代表的なものにジニ係数やエントロピーがある。

##### 剪定
精度に大きく影響を与えないノードやエッジを刈ることで、データ量と計算回数を削減し、汎化性能を高める。

### アンサンブル学習

学習器を複数組み合わせて1つの学習モデルを生成する方法。

「三人集まれば文殊の知恵」を機械学習で実現する方法ともいえるかも。

##### アンサンブル学習
複数の学習モデルを組み合わせて1つの学習モデルを生成する手法。

弱学習器を使って学習を行うため、学習スピードが早く、訓練や予測にかかる時間が少なくて済む。
最終的な予測結果は「多数決」「平均」「加重平均」といった方法で求める。

#### 手法

アンサンブル学習の手法は大きく分けて以下の2つの手法がある。

##### バギング
ブートストラップ法を使って、全データから訓練データを複数組生成し、訓練データ1組1組に対してモデルを用意して並列して学習を行う。
各モデルの結果平均をとって予測結果とする。

##### ブースティング
以下のフローで各モデルを逐次的に学習させる手法。

1. 訓練データ1つ目のモデルに学習させ、予測結果と実際の値を比較する
1. 次のモデルを学習する際に、間違えた部分を正解にできるように学習したデータを重視して学習する

ブースティングには以下のようなアルゴリズムがある。
##### [AdaBoost](https://ja.wikipedia.org/wiki/AdaBoost)
##### 勾配ブースティング
各モデルの最適化に勾配降下法を用いる。
##### XGBoost
勾配ブースティング法を使ったライブラリ。
確率的な最適化処理をしているため大規模なデータでも高速に処理できる。

#### アンサンブル学習の応用
##### ランダムフォレスト
ランダムに選んだ学習データを説明変数を用いて決定木群を作成し、その多数決や平均値を結果として出力する。

ある特徴量についてデータをシャッフルし、前後で予測精度が下がれば、その特徴量は重要。変わらなければ重要でない。というように相対的な特徴量の重要度を求めることができる。

決定木にバギングを組み合わせていて、以下のような利点があり、非常によく使われている。
- データの前処理が少なくて済む
- 安定して良い精度が出る
- 過学習を起こしにくい

一方で、中身がブラックボックス化するという面もある。

##### スタッキング
前段階のモデルの予測結果を学習するため、データの偏り（バイアス）とデータの散らばり（バランス）を上手に調整できる。

1. バギングと同じように、ブートストラップ法で得たデータを各モデルに学習させ、各モデルの予測結果を出す
1. 上記予測結果を入力としてモデルを学習させる
1. 以降も同様に前段階の予測結果を入力として学習する

##### 勾配ブースティング（Gradient Boosting）
サンプリングしたデータに対して直列的に浅い決定木を学習していく手法。
前モデルの誤差を取ることによって、新しいモデルが古いモデルの欠点を穴埋めをする。

1. 決定木を用いて1回目の予測を行う
1. 訓練セットの正解データと予測結果の差をとり、誤差を算出する
1. この誤差を正解データとして、決定木を使って2回目の予測を行う
1. 上記を繰り返す 

### ロジスティック回帰

「回帰」という言葉がついているが、主に分類に使われるアルゴリズム。

Yes / No の確率を計算するさまざまな場面で利用される。

##### [ロジスティク回帰](https://ja.wikipedia.org/wiki/%E3%83%AD%E3%82%B8%E3%82%B9%E3%83%86%E3%82%A3%E3%83%83%E3%82%AF%E5%9B%9E%E5%B8%B0)
AかBどちらかしか起こらない確率などに、事象がどちらかに分類できるかの確率を計算する。

線形回帰を分類問題に応用したアルゴリズム。（線形分離可能な対象を分離するアルゴリズム）

1. 「対数オッズ」を重回帰分析により予測する
2. 「対数オッズ」をロジスティック関数（シグモイド関数）で変換することで、クラスiに属する確率piを求める
3. 各クラスに属する確率を計算し、最大確率を実現するクラスが、データの所属するクラスと予測する

また、「ロジット変換」を行うことで、出力値が 0 から 1 の間の値に正規化され、確率としての解釈が可能になる。

目的関数には「[尤度関数](https://ja.wikipedia.org/wiki/%E5%B0%A4%E5%BA%A6%E9%96%A2%E6%95%B0)」が用いられる。

### ベイジアンモデル

ベイズ推定を用いて、不確実性を考慮した予測を行うことができる。

##### ベイズ推定
確率の初期状態（事前確率）に対して、得られたデータにより確率（事後確率）を計算（ベイズ更新）して推定を行う。
推定結果（値）がどれだけふさわしいかがわかる。

データを増やすことで精度を向上できるが、学習データで仮定した確率分布以外では未対応。

### KNN法（k近傍法）

##### [kNN法 (k-nearest neighbor)](https://ja.wikipedia.org/wiki/K%E8%BF%91%E5%82%8D%E6%B3%95)
クラス分類のアルゴリズムの一種。 

データから近い順に k 個のデータを見て、それらの多数決によって所属クラスを決定する。
kNN法は柔軟にモデルを作れるが、実用上、以下の条件がないと精度が上がらない弱点がある。

- 各クラスのデータ数に偏りがない
- 各クラスがよく別れている

##### 最近傍法
分類するデータに最も近いデータと同じ分類である。とみなす方法。
正解データが密である場合に有効。

## 教師なし学習

代表的な手法は、クラスタリングと次元分析。

##### クラスタリング
データ群をいくつかの集まり（クラスタ）に分けることで、データの本質的な構造を浮かび上がらせる手法。
クラスタはデータから自動的に導かれる。

##### クラス分類
エンジニアが予め設定した「クラス」にデータを適切に分類する（教師データを使う）

##### 主成分分析
多次元のデータに対して正味に効果のあるより少ない成分を抽出（次元の削減）する手法。
データから「主成分」という新たなデータを求める、線形な次元削減の手法。

データの情報を失わず、データを圧縮できるため、データの意味が解釈しやすくなる。

寄与率を調べることで各成分の重要度を測ることができる。

変数間に相関のないデータに対しては有効でない。

##### 次元圧縮
データの情報を失わないようにデータを低い次元に圧縮する手法の総称。（ex. 身長と体重から肥満度を表す BMI を計算する）

##### [k-means (k平均法)](https://www.albert2005.co.jp/knowledge/data_mining/cluster/non-hierarchical_clustering)
異なる性質のものが混ざり合った集団から、互いに似た性質を持つものを集め、クラスターを作る方法の1つ。

あらかじめいくつのクラスターに分けるかを決め、決めた数の塊（排他的部分集合）にサンプルを分割する。
手法が理解しやすく、大規模なデータにも適応可能。

## 手法の評価

機械学習において重要なことは、データを学習することで未知のデータの予測や分類を行えるようにする（汎化性能）こと。

学習が終わった段階では未知のデータに対する性能が保証されていないので、汎化性能を検証する必要がある。

##### 教師データ
区別がまぎらわしい少数のデータのラベルを作成して学習したほうが精度があがる。

##### 訓練データ
学習に用いる分の教師データ。

##### 精度検証データ（validation data）
「モデルの評価」で使うチューニング用データ。

このデータを使って、正解ラベルと一致するかをチェックすることで、「対象の機械学習モデルがどのくらいの精度が出せるのか」というパフォーマンス（性能）を評価・検証する。

##### テストデータ
未知データへの予測性能（汎化性能）を測るための教師データ。

##### 過学習
学習済みのモデルが、訓練に対しては高い精度で正解ラベルを予測できる（訓練誤差が小さい）にもかかわらず、未知のデータに対しての予測精度が悪いままになってしまう現象。
機械学習における最大の問題？と呼ばれている。

##### 推定誤差 (Validation Loss)
未知のデータ（テストデータ）とモデルとの間に生じた誤差のこと。

##### 訓練誤差
出力データと正答データの間に生じた誤差。

##### 内部共変量シフト
ある層の入力がそれより下層の学習が進むにつれて変化してしまうことがある。これにより学習が止まってしまうこと。

大規模なニューラルネットワークの学習が困難となる原因の一つ。

これを防ぐために出力値の分布の偏りを抑制する「バッチ正規化」が使用される。

### 学習データとテストデータを分ける手法

##### ホールドアウト検証
データを訓練データとテストデータにある割合で分割して、モデルが過学習を起こしていないか調べるための手法。

**モデルを評価するためのデータ**
- テストデータ

  やがて手に入るであろう、正解ラベルがあるとは限らないデータ。

- 検証データ

  あらかじめ手元にあり、正解ラベルがあることが約束されているデータ。

##### 交差検証
データを分割し、1つを検証データ、残りを訓練データとし、これを入れ替えながら繰り返し学習する。
モデルの汎化性能を高めるために行う。

##### [K-flod クロスバリデーション（K-分割交差検証）](https://ja.wikipedia.org/wiki/%E4%BA%A4%E5%B7%AE%E6%A4%9C%E8%A8%BC)
テストデータに用いるブロックを順に移動しながらホールドアウト法による検証を行う。

計算量が多くなるなど欠点があるが、データ数が少ない場合にもホールドアウト法と比較して信頼できる精度が増えるなどの理由で、精度検証において最もよく用いられる。

### 学習結果に対する評価基準

#### 回帰
回帰モデルの性能は基本的に、出力と正答の数値の差分である「予測誤差」によって評価できる。

回帰モデルの評価指標の違いは、**予測誤差をどのように集計するか**の違い。

##### 決定係数
予測誤差を正規化することで得られる指標。
まったく予測できていない場合を 0、すべて予測できている場合を 1 として大きいほど性能が良いことを示す。

##### RMSE（平方平均二乗誤差）
予測誤差を二乗して平均したあとに集計する指標。
小さいほど性能が良いこと示す。
正規分布の誤差に対して正確な評価ができるため、多くのケースで使われている。

##### MAE（平均絶対誤差）
予測誤差の絶対値を平均したあとに集計する指標。
小さいほど性能が良いことを示す。
RMSE と比較して外れ値に強いため、多くの外れ値が存在するデータセットで評価する場合に利用される。

#### 分類

##### 混同行列

| | 正解が「o」| 正解が「x」|
| :---: | :---: | :---: |
|「o」と予想 | TP | FP |
|「x」と予想 | FN | TN |

##### 正解率（Accuracy）
`(TP + TN) / (TP + TF + FN + TN)`

全体のデータのうち正しく分類できたデータの数の割合。

##### 再現率 (Recall)
`TP / (TP + FN)`

実際に正であるものの中で、正だと予測できたデータの割合。

出力した結果が実際の正解全体のうち、どのくらいの割合をカバーしていたかを表す指標。

「絶対にミスをしてはいけない」などのケースでは重視される指標。（ex. 医療検診）

##### 適合率 (Precision)
`TP / (TP + FP)`

予測が正の中で、実際に正だったデータの割合。

適合率は精度とも呼ばれ、出力した結果がどの程度正解していたかを表す指標。

見逃しが多くてもより正確な予測をしたい場合は、適合率を重視する。
（重要なメールがスパムと誤判定されるよりは、たまにスパムがすり抜けても構わない）

「顧客の好みでない商品を提案したくない」などのケースでは重視される指標。（ex. WEBマーケティング）

##### F値 (f-score)
`(2 x Recall x Precision) / (Recall + Precision)`

適合率と再現率の調和平均。
適合率のみあるいは再現率のみで判断すると、予測が偏っているときも値が高くなってしまうので、F値を用いることも多い。

適合率と再現率のバランスが見れる。機械学習モデルの評価の際に、正解率と並んで最も使われる指標。

##### PR曲線
横軸を再現率(Recall)、縦軸を適合率/精度(Precision)として、データをプロットしたグラフを表したもの。

PR曲線には適合率と再現率が一致する点があり、この点を「ブレークイーブンポイント(BEP)」と呼ぶ。
この点では、適合率と再現率の関係をバランスよく保ったまま、コストと利益を最適化できるので、ビジネスにおいては重要な点となる。BEPが右上に遷移するほど良いモデルが構築できたと言える。

## 用語

##### [No Free Lunch（ノーフリーランチ）定理](https://ja.wikipedia.org/wiki/%E3%83%8E%E3%83%BC%E3%83%95%E3%83%AA%E3%83%BC%E3%83%A9%E3%83%B3%E3%83%81%E5%AE%9A%E7%90%86)
一つの学習済みモデルで様々用途に対応できるわけではないこと数学的に証明した定理。

##### [みにくいアヒルの子定理](https://dic.nicovideo.jp/a/%E3%81%BF%E3%81%AB%E3%81%8F%E3%81%84%E3%82%A2%E3%83%92%E3%83%AB%E3%81%AE%E5%AD%90%E3%81%AE%E5%AE%9A%E7%90%86)
1969年に情報理論学者・理論物理学者の[渡辺慧](https://ja.wikipedia.org/wiki/%E6%B8%A1%E8%BE%BA%E6%85%A7)が提唱した定理。

対象がもつ特徴をすべて同等に評価すると識別が困難になること。
機械学習で行われる「特徴選択」や「次元削減」といった処理が人間の主観的な特徴選択と同様であり、識別にとって本質的であることも示している。
