# Deep Learning for General

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**

- [:scroll: 歴史](#scroll-%E6%AD%B4%E5%8F%B2)
  - [人工知能のレベル](#%E4%BA%BA%E5%B7%A5%E7%9F%A5%E8%83%BD%E3%81%AE%E3%83%AC%E3%83%99%E3%83%AB)
  - [第1次AIブーム（1956 - 1974: 探索・推論による人工知能）](#%E7%AC%AC1%E6%AC%A1ai%E3%83%96%E3%83%BC%E3%83%A01956---1974-%E6%8E%A2%E7%B4%A2%E3%83%BB%E6%8E%A8%E8%AB%96%E3%81%AB%E3%82%88%E3%82%8B%E4%BA%BA%E5%B7%A5%E7%9F%A5%E8%83%BD)
  - [第2次AIブーム（1980 - 1987: 知識表現による人工知能）](#%E7%AC%AC2%E6%AC%A1ai%E3%83%96%E3%83%BC%E3%83%A01980---1987-%E7%9F%A5%E8%AD%98%E8%A1%A8%E7%8F%BE%E3%81%AB%E3%82%88%E3%82%8B%E4%BA%BA%E5%B7%A5%E7%9F%A5%E8%83%BD)
  - [第3次AIブーム（2000 -: 機械学習と深層学習による人工知能）](#%E7%AC%AC3%E6%AC%A1ai%E3%83%96%E3%83%BC%E3%83%A02000---%E6%A9%9F%E6%A2%B0%E5%AD%A6%E7%BF%92%E3%81%A8%E6%B7%B1%E5%B1%A4%E5%AD%A6%E7%BF%92%E3%81%AB%E3%82%88%E3%82%8B%E4%BA%BA%E5%B7%A5%E7%9F%A5%E8%83%BD)
- [:bug: 人工知能分野の問題](#bug-%E4%BA%BA%E5%B7%A5%E7%9F%A5%E8%83%BD%E5%88%86%E9%87%8E%E3%81%AE%E5%95%8F%E9%A1%8C)
- [🖥️ 機械学習](#-%E6%A9%9F%E6%A2%B0%E5%AD%A6%E7%BF%92)
  - [代表的な手法](#%E4%BB%A3%E8%A1%A8%E7%9A%84%E3%81%AA%E6%89%8B%E6%B3%95)
  - [データの前処理](#%E3%83%87%E3%83%BC%E3%82%BF%E3%81%AE%E5%89%8D%E5%87%A6%E7%90%86)
  - [教師あり学習](#%E6%95%99%E5%B8%AB%E3%81%82%E3%82%8A%E5%AD%A6%E7%BF%92)
  - [教師なし学習](#%E6%95%99%E5%B8%AB%E3%81%AA%E3%81%97%E5%AD%A6%E7%BF%92)
  - [手法の評価](#%E6%89%8B%E6%B3%95%E3%81%AE%E8%A9%95%E4%BE%A1)
- [:robot: ディープラーニング](#robot-%E3%83%87%E3%82%A3%E3%83%BC%E3%83%97%E3%83%A9%E3%83%BC%E3%83%8B%E3%83%B3%E3%82%B0)
  - [活性化関数](#%E6%B4%BB%E6%80%A7%E5%8C%96%E9%96%A2%E6%95%B0)
  - [学習率の最適化](#%E5%AD%A6%E7%BF%92%E7%8E%87%E3%81%AE%E6%9C%80%E9%81%A9%E5%8C%96)
  - [テクニック](#%E3%83%86%E3%82%AF%E3%83%8B%E3%83%83%E3%82%AF)
  - [CNN: 畳み込みニューラルネットワーク](#cnn-%E7%95%B3%E3%81%BF%E8%BE%BC%E3%81%BF%E3%83%8B%E3%83%A5%E3%83%BC%E3%83%A9%E3%83%AB%E3%83%8D%E3%83%83%E3%83%88%E3%83%AF%E3%83%BC%E3%82%AF)
  - [RNN: リカレントニューラルネットワーク](#rnn-%E3%83%AA%E3%82%AB%E3%83%AC%E3%83%B3%E3%83%88%E3%83%8B%E3%83%A5%E3%83%BC%E3%83%A9%E3%83%AB%E3%83%8D%E3%83%83%E3%83%88%E3%83%AF%E3%83%BC%E3%82%AF)
  - [深層強化学習](#%E6%B7%B1%E5%B1%A4%E5%BC%B7%E5%8C%96%E5%AD%A6%E7%BF%92)
  - [深層生成モデル](#%E6%B7%B1%E5%B1%A4%E7%94%9F%E6%88%90%E3%83%A2%E3%83%87%E3%83%AB)
- [🔬 ディープラーニングの研究分野](#-%E3%83%87%E3%82%A3%E3%83%BC%E3%83%97%E3%83%A9%E3%83%BC%E3%83%8B%E3%83%B3%E3%82%B0%E3%81%AE%E7%A0%94%E7%A9%B6%E5%88%86%E9%87%8E)
  - [画像認識分野](#%E7%94%BB%E5%83%8F%E8%AA%8D%E8%AD%98%E5%88%86%E9%87%8E)
  - [自然言語処理](#%E8%87%AA%E7%84%B6%E8%A8%80%E8%AA%9E%E5%87%A6%E7%90%86)
  - [音声認識](#%E9%9F%B3%E5%A3%B0%E8%AA%8D%E8%AD%98)
  - [強化学習](#%E5%BC%B7%E5%8C%96%E5%AD%A6%E7%BF%92)
- [🏛️ 法律・倫理・現行の議論](#-%E6%B3%95%E5%BE%8B%E3%83%BB%E5%80%AB%E7%90%86%E3%83%BB%E7%8F%BE%E8%A1%8C%E3%81%AE%E8%AD%B0%E8%AB%96)
- [🏢 事例](#-%E4%BA%8B%E4%BE%8B)
- [:tv: Youtube](#tv-youtube)
  - [松尾豊](#%E6%9D%BE%E5%B0%BE%E8%B1%8A)
  - [NDIVIA](#ndivia)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## :scroll: 歴史
- [ダートマス会議](http://www.dartmouth.edu/~ai50/homepage.html)  
1956年7月から8月にかけて開催された[ジョン・マッカーシー](https://ja.wikipedia.org/wiki/%E3%82%B8%E3%83%A7%E3%83%B3%E3%83%BB%E3%83%9E%E3%83%83%E3%82%AB%E3%83%BC%E3%82%B7%E3%83%BC)が主催した会議。  
史上初めて「人工知能（Artificial Intelligence）」という用語が使われた。

- [ENIAC (エニアック)](https://ja.wikipedia.org/wiki/ENIAC)  
1946年にアメリカで開発された世界初のコンピュータ

### 人工知能のレベル
- 人工知能 (AI: Artificial Intelligence)  
コンピュータによる知的な情報処理システムを設計、または実現するための研究分野。研究者によって定義は異なる。

- 機械学習  
人工知能を実現するための手法のうち特に、人間の学習能力、予測能力をコンピュータで実現しようとする技法や手法の総称

- ディーブラーニング（深層学習）  
ディープニューラルネットワークを用いて学習を行う、機械学習のアルゴリズムの1つ。

- 特化型人工知能  
特定のタスクでのみ成果を出せる人工知能。弱い人工知能。現在の技術ではこちらしか実現できていない。

- 汎用人工知能  
人間と同等の知能を持もった人工知能。強い人工知能。

- レベル1 (マーケティング用 AI)  
「人工知能搭載X」のような家電など

- レベル2 (弱い AI)  
チェスプログラム、将棋マシーン

- レベル3 (強い AI)  
人間の知能を目指そうとするもの

- レベル4 (強い AI を超えうるもの)  
表現学習、深層学習

### 第1次 AI ブーム（1956 - 1974: 探索・推論による人工知能）

冷戦下のアメリカで、自然言語処理による機械翻訳の研究に注力されていたことが有名。しかし当時は、実用的な機械翻訳を行うことはきわめて困難であると結論された。

- [チューリングテスト](https://ja.wikipedia.org/wiki/%E3%83%81%E3%83%A5%E3%83%BC%E3%83%AA%E3%83%B3%E3%82%B0%E3%83%BB%E3%83%86%E3%82%B9%E3%83%88)(1950)  
ある機械が人工知能かどうか判定するためのテスト。「機械が知能をもっているか」という問いから、「機械が知能をもっている存在として人間が認知できるか」という問題に置き換えている。

- 推論  
自分がもつ知識と知識を組み合わせることで新しい知識を見つけ出す

- 探索  
推論により導き出せる結果を、いかに早くおこなえるかを求めた手法。問題をうまく表現することができれば、効率的に解を見つけ出すことができる

- 人工知能を考える視点  
環境・状態・行動をコード化できるとそのタスクは人工知能で解くことができる。推論・探索ではこの3要素を機械が理解できる形に書けないと解くことができない。

- トイ・プロブレム  
迷路やオセロなど、機械にときやすい簡単な問題

- [ELIZA (イライザ)](https://ja.wikipedia.org/wiki/ELIZA)  
1966年に発表された自然言語処理プログラム。人工無脳の起源となった。

- [PARRY](https://ja.wikipedia.org/wiki/PARRY)  
1972年に開発された ELIZA と共に有名な初期の会話ボット。ELIZA との最初の会話記録は [RFC439](https://tools.ietf.org/html/rfc439) に残されている。

- [BFS (幅優先探索)](https://ja.wikipedia.org/wiki/%E5%B9%85%E5%84%AA%E5%85%88%E6%8E%A2%E7%B4%A2)  
隣接するノードを優先して探索するアルゴリズム

- [DFS (深さ優先探索)](https://ja.wikipedia.org/wiki/%E6%B7%B1%E3%81%95%E5%84%AA%E5%85%88%E6%8E%A2%E7%B4%A2)  
目的のノードが見つかるか子のないノードに行き着くまで、深く探索するアルゴリズム

- ハノイの塔  

- ロボットの行動計画（プランニング）  

- STRIPS  

- SHRDLU  

- [Mini-Max法](https://ja.wikipedia.org/wiki/%E3%83%9F%E3%83%8B%E3%83%9E%E3%83%83%E3%82%AF%E3%82%B9%E6%B3%95)  
想定される最大の損害が最小になるように決断を行う戦略

- [モンテカルロ法](https://ja.wikipedia.org/wiki/%E3%83%A2%E3%83%B3%E3%83%86%E3%82%AB%E3%83%AB%E3%83%AD%E6%B3%95)  
シミュレーションや数値計算を乱数を用いて行う手法の総称。ランダム法とも呼ばれる。

### 第2次 AI ブーム（1980 - 1987: 知識表現による人工知能）
エキスパートシステムにより問題を解く人工知能が台頭。しかし専門家の知識の定式化は難しく、複雑な問題が解けるようにならなかった。

- エキスパートシステム  
専門家の知識をそのまま人工知能に移植する事により、さまざまな問題を解決するアイディア

- [MYCIN (マイシン)](https://ja.wikipedia.org/wiki/Mycin)  
1970年代初めに5、6年の歳月をかけて開発された抗生物質を処方するAI

- [DENDRAL](https://ja.wikipedia.org/wiki/Dendral)  
1906年代の人工知能プロジェクト。有機化合物の特定を行う

- 知識ベース  
if-then 文よって記述できる知識の集まり

- 推論エンジン  
知識ベースを用いて推論を行うプログラム

- 第五世代コンピュータ  
通商産業省（現経済産業省）が1982年に立ち上げた国家プロジェクト。  
[第五世代コンピュータ・プロジェクト最終評価報告書](https://www.jipdec.or.jp/archives/publications/J0005062)（平成5年3月30日 電子計算機基礎技術開発推進委員会）

- 人工無能  

- 意味ネットワーク  

- Cycプロジェクト  

- オントロジー  

- ヘビーウェイトオントロジー  

- ライトウェイトオントロジー  

- ワトソン  


### 第3次 AI ブーム（2000 -: 機械学習と深層学習による人工知能）

- 機械学習

- ディーブラーニング

- 特徴量  
データをよく表す特徴を数値で示したもの（ex. 「人間」を表す特徴量としては、身長、体重、年齢、性別など）

- 特徴量エンジニアリング  
モデルが認識しやすいような「特徴」をデータから新しく作ること。  
たった1つの成分だけが1、残りの成分が0という特徴量（ベクトル）に変換します。この形のことを [one-hot-encoding](https://ja.wikipedia.org/wiki/One-hot) と呼ぶ。

- 内部表現  
ディープラーニングにより自動的に獲得された特徴量。

- [ILSVRC (Large Scale Visual Recognition Challenge)](http://www.image-net.org/challenges/LSVRC/)  
2010年から始まった ImageNet データセットを用いた画像認識の精度を競うコンペ。  
2012年、トロント大学の[ジェフリー・ヒントン](https://ja.wikipedia.org/wiki/%E3%82%B8%E3%82%A7%E3%83%95%E3%83%AA%E3%83%BC%E3%83%BB%E3%83%92%E3%83%B3%E3%83%88%E3%83%B3)教授のチームが [AlexNet](https://en.wikipedia.org/wiki/AlexNet) と呼ばれる畳み込みニューラルネットワーク(CNN)で[2位以下を10%以上引き離す結果](http://image-net.org/challenges/LSVRC/2012/results.html)を出す。これがきっかけとなり、ディーブラーニングが一気に脚光を浴びる。

[人工知能](https://ja.wikipedia.org/wiki/%E4%BA%BA%E5%B7%A5%E7%9F%A5%E8%83%BD) > [機械学習](https://ja.wikipedia.org/wiki/%E6%A9%9F%E6%A2%B0%E5%AD%A6%E7%BF%92) > [ニューラルネットワーク](https://ja.wikipedia.org/wiki/%E3%83%8B%E3%83%A5%E3%83%BC%E3%83%A9%E3%83%AB%E3%83%8D%E3%83%83%E3%83%88%E3%83%AF%E3%83%BC%E3%82%AF) > [ディープラーニング](https://ja.wikipedia.org/wiki/%E3%83%87%E3%82%A3%E3%83%BC%E3%83%97%E3%83%A9%E3%83%BC%E3%83%8B%E3%83%B3%E3%82%B0)

- [モラベックのパラドックス](https://ja.wikipedia.org/wiki/%E3%83%A2%E3%83%A9%E3%83%99%E3%83%83%E3%82%AF%E3%81%AE%E3%83%91%E3%83%A9%E3%83%89%E3%83%83%E3%82%AF%E3%82%B9)  
子供のできることほど人工知能には難しい

## :bug: 人工知能分野の問題

- [シンギュラリティー（技術的特異点）](https://ja.wikipedia.org/wiki/%E6%8A%80%E8%A1%93%E7%9A%84%E7%89%B9%E7%95%B0%E7%82%B9)  
[レイ・カーツワイル](https://ja.wikipedia.org/wiki/%E3%83%AC%E3%82%A4%E3%83%BB%E3%82%AB%E3%83%BC%E3%83%84%E3%83%AF%E3%82%A4%E3%83%AB) が提唱した、人工知能が人間を超えて文明の主役に取って代わる時点。カーツワイルは 自著「The Singularity Is Near」で「シンギュラリティは2045年に到来する」と述べた。

- トイ・プロブレム

- フレーム問題  
ある問題を解決する際に、その問題位関連する、考慮すべき事柄を抽出することが AI には難しいこと

- 強いAI  
フレーム問題を打破し、人間のようにあらゆる問題に適切に対処できるようになった AI

- 弱いAI  
フレーム問題に縛られたままの AI

- シンボルグラウディング問題  
記号システム内のシンボルがどのようにして実世界の意味と結び付けられるかという問題

- [He saw a woman in the garden with a telescope](https://www.deepl.com/ja/translator#en/ja/He%20saw%20a%20woman%20in%20the%20garden%20with%20a%20telescope)

- 特徴量設計  


## 🖥️ 機械学習
- [ネオコグニトロン](https://ja.wikipedia.org/wiki/%E3%83%8D%E3%82%AA%E3%82%B3%E3%82%B0%E3%83%8B%E3%83%88%E3%83%AD%E3%83%B3)

### 代表的な手法

- 教師あり学習  
教師データ（入力とそれに対応する正解ラベルの組）を使って予測値を正解ラベルに近づけることを目標に学習する手法

- 教師なし学習  
教師データを使わずに、データの本質的な構造を浮かび上がらせる手法

- 強化学習  
収益（報酬の和）を最大化する方策を獲得することを目的とした手法

- 半教師あり学習  
教師あり学習におけるラベル付けコストを低減するために用いられる手法。
データの一部分にのみ聖会話ベルをつける。

- 回帰問題  
出力値の予測（ex. 家賃、年収、天気の予測）

- 線形回帰  
入力データが1つの単回帰分析、複数の入力データの重回帰分析などの種類がある

- 分類問題  
あらかじめ設定したクラスにデータを割り振る（ex. 画像に写っている犬や猫の識別）。  
サポートベクターマシン、決定木、ランダムフォレスト、ロジスティック回帰、kNN法などの手法がある。深層学習でも分類を行うことができる。

### データの前処理

データをモデルに正しく入力できるようにする。  
データの大きさをある程度均一にする。

- 正規化  
データを 0 から 1 に収まるようにスケーリングすること

- 標準化  
平均を 0、標準偏差（分散）を 1 に変換すること

- 正則化  
過学習を抑制するための手法

- 基礎集計  
データの傾向を事前に把握する。散布図行列をプロットして傾向を調べる。相関行列を表示し傾向を調べる。


### 教師あり学習

- 線形回帰  
  - 単回帰分析  
  1つの説明変数（手がかりとなる変数）から目的変数を予測する  
  ※ 説明変数は文脈にとっては特徴量と呼ばれることがある。特徴量の方が少し大きな概念になるが、同じものを指していると考えていい。

  - 重回帰分析  
  複数の説明変数から目的変数を予測する

- 相関係数  
特徴量同士の相関の正負と強さを表す指標。-1 <= x <= 1  
1に近いほど強い正の相関、-1に近いほど強い負の相関をもつ。0のときは相関がない。

- 多重共線性  
相関係数が高い特徴量の組を同時に説明変数に選ぶと、予測がうまくいかなくなる現象。  
特徴量エンジニアリングにおいては、多重共線性がでないような特徴量を選ぶ必要がある。

- 線形分離可能  
パーセプトロンを使って解ける問題。2次元のグラフ上で直線を使って分離できる。  
論理ゲートでは、OR, AND, NAND は線形分離可能だが、XOR のみ線形分離不可能。

- [SVM (サポートベクターマシン)](https://ja.wikipedia.org/wiki/%E3%82%B5%E3%83%9D%E3%83%BC%E3%83%88%E3%83%99%E3%82%AF%E3%82%BF%E3%83%BC%E3%83%9E%E3%82%B7%E3%83%B3)  
「マージン最大化」というコンセプトで2つのクラスを線形分離可能にするアルゴリズム。  
もともとは2つのクラス分類アルゴリズムとして考案されたが、性能がいいので多クラス分類や回帰分析にも応用されている。  
線形分離可能でないデータに対しても、カーネル法を組み合わせることで決定境界を求めることができる。

- [スラック変数](http://sudillap.hatenablog.com/entry/2013/04/08/235602)  
超平面を構成した結果として発生する誤差の程度を測る変数。


- [ハイパーパラメータ](https://ja.wikipedia.org/wiki/%E3%83%8F%E3%82%A4%E3%83%91%E3%83%BC%E3%83%91%E3%83%A9%E3%83%A1%E3%83%BC%E3%82%BF)  
推論や予測の枠組みの中で決定されないパラメータ。  
SVN においては誤りをどの程度許容するかの度合いをエンジニが事前に調整する必要がある。

- [カーネル法](https://ja.wikipedia.org/wiki/%E3%82%AB%E3%83%BC%E3%83%8D%E3%83%AB%E6%B3%95)  
次のアイディアをカーネル関数の計算によって実現するもの  
・ データを高次元空間にうまく埋め込む  
・高次元空間で線形分離 (SVM) し、その境界を元の空間に戻す

- カーネルトリック  
カーネル関数を使って、計算複雑度の増大を抑えつつ内積にもとづく解析手法を高次元特徴空間へ拡張するアプローチ。  
計算量を現実的に抑えつつ、非線形分離を実現する。

- 決定木  
以下のような仕組みの分類アルゴリズム。  
・不純度が最も減少（情報利得が最も増加）するように、条件分岐を作りデータを振り分ける  
・それを繰り返す  
不純度とは「クラスの混じり具合」を表す指標で、代表的なものにジニ係数やエントロピーがある。

- ランダムフォレスト  
決定木にバギングを組み合わせた手法。以下のような利点があり、非常によく使われている。  
・データの前処理が少なくて済む  
・安定して良い精度が出る

- バギング  
アンサンブル学習の一種で、複数のモデルを使用し、それらの平均の多数決をとって予測結果とする

- [ロジスティク回帰](https://ja.wikipedia.org/wiki/%E3%83%AD%E3%82%B8%E3%82%B9%E3%83%86%E3%82%A3%E3%83%83%E3%82%AF%E5%9B%9E%E5%B8%B0)  
線形回帰を分類問題に応用したアルゴリズム。  
  1. 「対数オッズ」を重回帰分析により予測する  
  2. 「対数オッズ」をロジスティック関数（シグモイド関数）で変換することで、クラスiに属する確率piを求める  
  3. 各クラスに属する確率を計算し、最大確率を実現するクラスが、データの所属するクラスと予測する  
また、「ロジット変換」を行うことで、出力値が 0 から 1 の間の値に正規化され、確率としての解釈が可能になる

- [kNN法 (k-nearest neighbor)](https://ja.wikipedia.org/wiki/K%E8%BF%91%E5%82%8D%E6%B3%95)  
クラス分類のアルゴリズムの一種。   
データから近い順に k 個のデータを見て、それらの多数決によって所属クラスを決定する。  
kNN法は実用上、以下の条件がないと精度が上がらない弱点がある。  
・各クラスのデータ数に偏りがない  
・各クラスがよく別れている  

- ブートストラップサンプリング  

- ブースティング
  - AdaBoost
  - 勾配ブースティング
  - XgBoost

- ニューラルネットワーク
  - 単純パーセプトロン
  - 誤差逆伝播法
  - シグモイド関数

### 教師なし学習

代表的な手法は、クラスタリングと次元分析。

- クラスタリング  
データ群をいくつかの集まり（クラスタ）に分けることで、データの本質的な構造を浮かび上がらせる手法。  
クラスタはデータから自動的に導かれる。

- クラス分類  
エンジニアが予め設定した「クラス」にデータを適切に分類する（教師データを使う）

- 次元圧縮  
データの情報を失わないようにデータを低い次元に圧縮する手法の総称。（ex. 身長と体重から肥満度を表す BMI を計算する）

- 主成分分析  
データから「主成分」という新たなデータを求める、線形な次元削減の手法。

- [k-means (k平均法)](https://www.albert2005.co.jp/knowledge/data_mining/cluster/non-hierarchical_clustering)  
異なる性質のものが混ざり合った集団から、互いに似た性質を持つものを集め、クラスターを作る方法の1つ。  
あらかじめいくつのクラスターに分けるかを決め、決めた数の塊（排他的部分集合）にサンプルを分割する。

### 手法の評価

- 訓練データ  
学習に用いる分の教師データ

- テストデータ  
未知データへの予測性能（汎化性能）を測るための教師データ

- 過学習  
学習済みのモデルが、訓練に対しては高い精度で正解ラベルを予測できる（訓練誤差が小さい）にもかかわらず、未知のデータに対しての予測精度が悪いままになってしまう現象。  
機械学習における最大の問題？と呼ばれている。

- ホールドアウト検証  
データを訓練データとテストデータにわけて、モデルが過学習を起こしていないか調べるための手法。

- モデルを評価するためのデータ
  - テストデータ  
やがて手に入るであろう、正解ラベルがあるとは限らないデータ

  - 検証データ  
あらかじめ手元にあり、正解ラベルがあることが約束されているデータ

- [交差検証](https://ja.wikipedia.org/wiki/%E4%BA%A4%E5%B7%AE%E6%A4%9C%E8%A8%BC)  
テストデータに用いるブロックを順に移動しながらホールドアウト法による検証を行う。  
計算量が多くなるなど欠点があるが、データ数が少ない場合にもホールドアウト法と比較して信頼できる精度が偉えるなどの理由で、精度検証において最もよく用いられる。

- k-分割交差検証  

- 混同行列  

- 正解率  

- 適合率  

- 再現率  

- F値  

- オーバーフィッティング  

- アンダーフィッティング  

- ラッソ回帰  

- リッジ回帰  

- Elastic Net  

## :robot: ディープラーニング

- ニューロン  
単純な数値予測ができ予測器。ニューラルネットワークの最小単位

- ニューラルネットワーク  
ニューロンをたくさんつなげててきる予測器。入力が行わる層を「入力層」、出力される層を「出力層」、それ以外の層を「中間層」または「隠れ層」と呼ぶ。

- 単純パーセプトロン

- 多層パーセプトロン

- オートエンコーダ  

- ディープオートエンコーダ  

- 事前学習  

- ファインチューニング  


### 活性化関数
- [tanh (ハイパボリックタンジェント関数)](https://ja.wikipedia.org/wiki/%E5%8F%8C%E6%9B%B2%E7%B7%9A%E9%96%A2%E6%95%B0)  

- [ReLU関数](https://ja.wikipedia.org/wiki/%E6%AD%A3%E8%A6%8F%E5%8C%96%E7%B7%9A%E5%BD%A2%E9%96%A2%E6%95%B0)  

- Leaky ReLU関数  

- Parametric ReLU  

- Randomized ReLU  


### 学習率の最適化
- [勾配降下法](https://ja.wikipedia.org/wiki/%E7%A2%BA%E7%8E%87%E7%9A%84%E5%8B%BE%E9%85%8D%E9%99%8D%E4%B8%8B%E6%B3%95)  

- [誤差関数](https://ja.wikipedia.org/wiki/%E8%AA%A4%E5%B7%AE%E9%96%A2%E6%95%B0)  

- Adagrad  

- Adadelta  

- RMSprop  

- Adan  


### テクニック
- ドロップアウト  

- early stopping  

- 正規化  

- 標準化  

- 白色化  

- バッチ正規化  


### CNN: 畳み込みニューラルネットワーク
- LeNet  

- 畳み込み  

- プーリング  

- maxプーリング  

- avgプーリング  

- 全結合層  

- データ拡張  

- AlexNet  

- VGG  

- GoogLeNet  

- Skip connection  
層を飛び越えた結合

- 転移学習  
学習済みのネットワークを利用して新しいタスクの識別に利用すること

### RNN: リカレントニューラルネットワーク
時系列データを入力して、データから時間依存性を学習できるモデル

- Backpropagation Through Time (BPTT)  

- 入力重み衝突  

- 出力重み衝突  

- LSTM (Long Short-Term Memory)  

- GRU (Gated Recurrent Unit)  

- Bidirectional RNN  
LSTM を2つ組み合わせることで、未来から過去方向も含めて学習できるモデル

- Sequence-to-Sequence  
入力が時系列なら出力も時系列で予測する。自然言語処理を中心に研究されている分野。

- RNN Encoder–Decoder

- Attention  
過去の時点それぞれの重みを学習することで、時間の重みをネットワークに組み込む。

### 深層強化学習

- 強化学習  
行動を学習する仕組み。目的とする報酬（スコア）を最大化するためにはどのような行動をとっていけばいいかを学習していく。

### 深層生成モデル

- WaveNet  

- 生成モデル  

- VAE (変分オートエンコーダ)  

- GAN (敵対的生成ネットワーク)  

- DCGAN (Deep Convolutional GAN)  


## 🔬 ディープラーニングの研究分野

### 画像認識分野
- AlexNet (アレックスネット)  

- R-CNN  

- fast RCNN  

- faster RCNN  

- YOLO (You Only Look Once)  

- SSD (Single Shot Detector)  

- セマンティックセグメンテーション  

- FCN (完全畳み込みネットワーク)  

- アンサンプリング  

- インスタンスセグメンテーション  

- Mask RCNN  


### 自然言語処理
- word2vec  

- 単語埋め込みモデル  

- スキップグラム  

- CBOW  

- fastText  

- ELMo  

- 普遍埋め込みモデル  

- NIC (ニューラル画像脚注付け)  

- NTM (ニューラルチューリングマシン)  


### 音声認識
- WaveNet

### 強化学習
- DQN (Deep Q-Network)  

- MCTS (モンテカルロ木探索)  

- AlphaGo Zero  

- セルフプレイ  

- RAINBOWモデル  


## 🏛️ 法律・倫理・現行の議論
- プライバシーバイ・デザイン

- 倫理的に調和された設計  
2016年にIEEEが出したレポート

- データの利用条件
1. 著作権法 2. 不正競争防止法 3. 個人情報保護法 4. 個別の契約 5. その他の理由により、データの利用に制約がかかっている場合

- 日本の著作権法  
著作権法47条の７によって、著作者にモダンで記録や翻案をしても適法となっている。2018年の著作権法改正によって、学習データを第三者と共有したり、一般に販売したり、ネット上で公開するとことも、一定の条件下で適法となっている（改正著作権法30条4）

- オープン・イノベーション  

- [AI・データの利用に関する契約ガイドライン](https://www.meti.go.jp/press/2018/06/20180615001/20180615001.html)  

- データセットの偏り  

- プライバシーリスクを低減するデータ加工  

- 協調フィルタリング  

- [FAT (Fairness, Accountability, and Transparency)](https://www.fatml.org/)  

- 敵対的な攻撃  

- 知的財産法  

- GDPR  

- アルゴリズムバイアス  
Google Photos がアフリカ系の女性に「ゴリラ」とラベル付をしてしまった事件

- インセンティブ設計  

- クライシスマネージメント    
危機管理対応
- エスカレーション  

- 透明性レポート
  - [Twitter](https://transparency.twitter.com/ja.html)
  - [Google](https://transparencyreport.google.com/?hl=ja)
  - [Facebook](https://transparency.facebook.com/)

- [PAI(Partnership on AI)](https://www.partnershiponai.org/)  

- アシロマAI原則  

- [AIネットワーク社会推進会議](https://www.soumu.go.jp/main_sosiki/kenkyu/ai_network/index.html)  

- [人間中心のＡＩ社会原則検討会議](https://www8.cao.go.jp/cstp/tyousakai/humanai/index.html)  



## 🏢 事例
- [BRETT: Deep-learning robot](https://engineering.berkeley.edu/brett/)
- [AlphaGo](https://ja.wikipedia.org/wiki/AlphaGo)
- [Google DeepMind's Deep Q-learning playing Atari](https://deepmind.com/research/publications/playing-atari-deep-reinforcement-learning)

## :tv: Youtube

### 松尾豊
- [2014/11/01 人工知能が閻魔大王になる日](https://www.youtube.com/watch?v=U-O4eINZNXE)
- [2015/06/05 人工知能は人間を超えるか ディープラーニングの先にあるもの](https://www.youtube.com/watch?v=lqywEafvq_Q)
- [2015/11/03 人工知能の未来～ディープラーニングの先にあるもの](https://www.youtube.com/watch?v=GbmKWY7SLng)
- [2016/08/02 【SoftBank World 2016】 人工知能は人間を超えるか](https://www.youtube.com/watch?v=7bvfl_M5vPQ)

### NDIVIA
- [ディープ・ラーニング最新技術情報 何故GPUはディープラーニングに向いているか](https://www.youtube.com/watch?v=1aHQ2tVVlj8)
