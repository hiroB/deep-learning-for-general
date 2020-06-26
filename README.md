![](https://github.com/shgtkshruch/deep-learning-for-general/workflows/Build%20README.md/badge.svg)

# Deep Learning for General

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**

- [:scroll: 歴史](#scroll-%E6%AD%B4%E5%8F%B2)
  - [人工知能のレベル](#%E4%BA%BA%E5%B7%A5%E7%9F%A5%E8%83%BD%E3%81%AE%E3%83%AC%E3%83%99%E3%83%AB)
  - [第1次AIブーム（1956 - 1974: 探索・推論による人工知能）](#%E7%AC%AC1%E6%AC%A1ai%E3%83%96%E3%83%BC%E3%83%A01956---1974-%E6%8E%A2%E7%B4%A2%E3%83%BB%E6%8E%A8%E8%AB%96%E3%81%AB%E3%82%88%E3%82%8B%E4%BA%BA%E5%B7%A5%E7%9F%A5%E8%83%BD)
  - [第2次AIブーム（1980 - 1987: 知識表現による人工知能）](#%E7%AC%AC2%E6%AC%A1ai%E3%83%96%E3%83%BC%E3%83%A01980---1987-%E7%9F%A5%E8%AD%98%E8%A1%A8%E7%8F%BE%E3%81%AB%E3%82%88%E3%82%8B%E4%BA%BA%E5%B7%A5%E7%9F%A5%E8%83%BD)
  - [第3次AIブーム（2000 -: 機械学習と深層学習による人工知能）](#%E7%AC%AC3%E6%AC%A1ai%E3%83%96%E3%83%BC%E3%83%A02000---%E6%A9%9F%E6%A2%B0%E5%AD%A6%E7%BF%92%E3%81%A8%E6%B7%B1%E5%B1%A4%E5%AD%A6%E7%BF%92%E3%81%AB%E3%82%88%E3%82%8B%E4%BA%BA%E5%B7%A5%E7%9F%A5%E8%83%BD)
- [:ghost: 人工知能分野の問題](#ghost-%E4%BA%BA%E5%B7%A5%E7%9F%A5%E8%83%BD%E5%88%86%E9%87%8E%E3%81%AE%E5%95%8F%E9%A1%8C)
- [:robot: 機械学習](#robot-%E6%A9%9F%E6%A2%B0%E5%AD%A6%E7%BF%92)
  - [処理の流れ](#%E5%87%A6%E7%90%86%E3%81%AE%E6%B5%81%E3%82%8C)
  - [代表的な手法](#%E4%BB%A3%E8%A1%A8%E7%9A%84%E3%81%AA%E6%89%8B%E6%B3%95)
    - [代表的な「予測」アルゴリズム](#%E4%BB%A3%E8%A1%A8%E7%9A%84%E3%81%AA%E4%BA%88%E6%B8%AC%E3%82%A2%E3%83%AB%E3%82%B4%E3%83%AA%E3%82%BA%E3%83%A0)
  - [データの前処理](#%E3%83%87%E3%83%BC%E3%82%BF%E3%81%AE%E5%89%8D%E5%87%A6%E7%90%86)
  - [教師あり学習](#%E6%95%99%E5%B8%AB%E3%81%82%E3%82%8A%E5%AD%A6%E7%BF%92)
  - [教師なし学習](#%E6%95%99%E5%B8%AB%E3%81%AA%E3%81%97%E5%AD%A6%E7%BF%92)
  - [手法の評価](#%E6%89%8B%E6%B3%95%E3%81%AE%E8%A9%95%E4%BE%A1)
  - [用語](#%E7%94%A8%E8%AA%9E)
- [:globe_with_meridians: ディープラーニング](#globe_with_meridians-%E3%83%87%E3%82%A3%E3%83%BC%E3%83%97%E3%83%A9%E3%83%BC%E3%83%8B%E3%83%B3%E3%82%B0)
  - [ニューラルネットワーク](#%E3%83%8B%E3%83%A5%E3%83%BC%E3%83%A9%E3%83%AB%E3%83%8D%E3%83%83%E3%83%88%E3%83%AF%E3%83%BC%E3%82%AF)
    - [学習の手順](#%E5%AD%A6%E7%BF%92%E3%81%AE%E6%89%8B%E9%A0%86)
  - [従来の機機械学習との違い](#%E5%BE%93%E6%9D%A5%E3%81%AE%E6%A9%9F%E6%A9%9F%E6%A2%B0%E5%AD%A6%E7%BF%92%E3%81%A8%E3%81%AE%E9%81%95%E3%81%84)
  - [用語](#%E7%94%A8%E8%AA%9E-1)
  - [活性化関数](#%E6%B4%BB%E6%80%A7%E5%8C%96%E9%96%A2%E6%95%B0)
  - [学習の流れ](#%E5%AD%A6%E7%BF%92%E3%81%AE%E6%B5%81%E3%82%8C)
  - [学習率の最適化](#%E5%AD%A6%E7%BF%92%E7%8E%87%E3%81%AE%E6%9C%80%E9%81%A9%E5%8C%96)
  - [最適化](#%E6%9C%80%E9%81%A9%E5%8C%96)
  - [テクニック](#%E3%83%86%E3%82%AF%E3%83%8B%E3%83%83%E3%82%AF)
  - [CNN: 畳み込みニューラルネットワーク](#cnn-%E7%95%B3%E3%81%BF%E8%BE%BC%E3%81%BF%E3%83%8B%E3%83%A5%E3%83%BC%E3%83%A9%E3%83%AB%E3%83%8D%E3%83%83%E3%83%88%E3%83%AF%E3%83%BC%E3%82%AF)
    - [処理の流れ](#%E5%87%A6%E7%90%86%E3%81%AE%E6%B5%81%E3%82%8C-1)
    - [手法](#%E6%89%8B%E6%B3%95)
  - [RNN: リカレントニューラルネットワーク](#rnn-%E3%83%AA%E3%82%AB%E3%83%AC%E3%83%B3%E3%83%88%E3%83%8B%E3%83%A5%E3%83%BC%E3%83%A9%E3%83%AB%E3%83%8D%E3%83%83%E3%83%88%E3%83%AF%E3%83%BC%E3%82%AF)
  - [深層強化学習](#%E6%B7%B1%E5%B1%A4%E5%BC%B7%E5%8C%96%E5%AD%A6%E7%BF%92)
  - [深層生成モデル](#%E6%B7%B1%E5%B1%A4%E7%94%9F%E6%88%90%E3%83%A2%E3%83%87%E3%83%AB)
  - [GNN: グラフニューラルネットワーク](#gnn-%E3%82%B0%E3%83%A9%E3%83%95%E3%83%8B%E3%83%A5%E3%83%BC%E3%83%A9%E3%83%AB%E3%83%8D%E3%83%83%E3%83%88%E3%83%AF%E3%83%BC%E3%82%AF)
- [🔬 ディープラーニングの研究分野](#-%E3%83%87%E3%82%A3%E3%83%BC%E3%83%97%E3%83%A9%E3%83%BC%E3%83%8B%E3%83%B3%E3%82%B0%E3%81%AE%E7%A0%94%E7%A9%B6%E5%88%86%E9%87%8E)
  - [画像認識分野](#%E7%94%BB%E5%83%8F%E8%AA%8D%E8%AD%98%E5%88%86%E9%87%8E)
  - [自然言語処理](#%E8%87%AA%E7%84%B6%E8%A8%80%E8%AA%9E%E5%87%A6%E7%90%86)
  - [音声認識](#%E9%9F%B3%E5%A3%B0%E8%AA%8D%E8%AD%98)
  - [強化学習](#%E5%BC%B7%E5%8C%96%E5%AD%A6%E7%BF%92)
- [🏛️ 法律・倫理・現行の議論](#-%E6%B3%95%E5%BE%8B%E3%83%BB%E5%80%AB%E7%90%86%E3%83%BB%E7%8F%BE%E8%A1%8C%E3%81%AE%E8%AD%B0%E8%AB%96)
- [🏢 事例](#-%E4%BA%8B%E4%BE%8B)
- [:books: 参考資料](#books-%E5%8F%82%E8%80%83%E8%B3%87%E6%96%99)
  - [書籍](#%E6%9B%B8%E7%B1%8D)
  - [WEB](#web)
  - [Youtube](#youtube)
    - [松尾豊](#%E6%9D%BE%E5%B0%BE%E8%B1%8A)
    - [NDIVIA](#ndivia)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## :scroll: 歴史

- [ENIAC (エニアック)](https://ja.wikipedia.org/wiki/ENIAC)  
1946年にアメリカで開発された世界初のコンピュータ。  
17,468本もの真空管を使った巨大な電子計算機。  
設計したのはペンシルベニア大学の[ジョン・モークリー](https://ja.wikipedia.org/wiki/%E3%82%B8%E3%83%A7%E3%83%B3%E3%83%BB%E3%83%A2%E3%83%BC%E3%82%AF%E3%83%AA%E3%83%BC)と[ジョン・プレスパー・エッカート](https://ja.wikipedia.org/wiki/%E3%82%B8%E3%83%A7%E3%83%B3%E3%83%BB%E3%83%97%E3%83%AC%E3%82%B9%E3%83%91%E3%83%BC%E3%83%BB%E3%82%A8%E3%83%83%E3%82%AB%E3%83%BC%E3%83%88)  
[マーヴィン・ミンスキー](https://ja.wikipedia.org/wiki/%E3%83%9E%E3%83%BC%E3%83%93%E3%83%B3%E3%83%BB%E3%83%9F%E3%83%B3%E3%82%B9%E3%82%AD%E3%83%BC)、[ジョン・マッカーシー](https://ja.wikipedia.org/wiki/%E3%82%B8%E3%83%A7%E3%83%B3%E3%83%BB%E3%83%9E%E3%83%83%E3%82%AB%E3%83%BC%E3%82%B7%E3%83%BC)、[アレン・ニューウェル](https://ja.wikipedia.org/wiki/%E3%82%A2%E3%83%AC%E3%83%B3%E3%83%BB%E3%83%8B%E3%83%A5%E3%83%BC%E3%82%A6%E3%82%A7%E3%83%AB)、[ハーバート・サイモン](https://ja.wikipedia.org/wiki/%E3%83%8F%E3%83%BC%E3%83%90%E3%83%BC%E3%83%88%E3%83%BB%E3%82%B5%E3%82%A4%E3%83%A2%E3%83%B3)など、後に人工知能の研究で重要な役割を果たす著名な研究者たちも参加した。

- [ダートマス会議](http://www.dartmouth.edu/~ai50/homepage.html)  
1956年7月から8月にかけて開催された[ジョン・マッカーシー](https://ja.wikipedia.org/wiki/%E3%82%B8%E3%83%A7%E3%83%B3%E3%83%BB%E3%83%9E%E3%83%83%E3%82%AB%E3%83%BC%E3%82%B7%E3%83%BC)が主催した会議。  
史上初めて「人工知能（Artificial Intelligence）」という用語が使われた。

- [ロジック・セオリスト](https://ja.wikipedia.org/wiki/Logic_Theorist)  
1955年から1956年にかけてアレン・ニューウェル、ハーバート・サイモン、J・C・ショーが開発した世界初の人工知能プログラム。  
コンピュータを使って数学の定理が自動的に証明することが実現可能であることを示した。

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

- AI効果  
人工知能で何か新しいことを実現したときに、その原理がわかってしまうと、「それは単純な自動化であって知能とは関係ない」と結論づける人間の心理的効果

- [ELIZA効果](https://ja.wikipedia.org/wiki/ELIZA%E5%8A%B9%E6%9E%9C)  
人間は、相手が高度な知能を持った存在ではなくとも、自分に適切に反応してくれれば、本物の人間と対話しているように錯覚する傾向があること

### 第1次AIブーム（1956 - 1974: 探索・推論による人工知能）

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
1966年に発表された自然言語処理プログラム。[人工無脳](https://ja.wikipedia.org/wiki/%E4%BA%BA%E5%B7%A5%E7%84%A1%E8%84%B3)の起源となった。

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

### 第2次AIブーム（1980 - 1987: 知識表現による人工知能）
エキスパートシステムにより問題を解く人工知能が台頭。しかし専門家の知識の定式化は難しく、複雑な問題が解けるようにならなかった。

- エキスパートシステム  
専門家の知識をそのまま人工知能に移植する事により、さまざまな問題を解決するアイディア

- [MYCIN (マイシン)](https://ja.wikipedia.org/wiki/Mycin)  
1970年代初めに開発された抗生物質を処方するAI

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
AI におけるオントロジーとは「概念化の明示的な仕様」（Tom Gruber）であり、共通の概念の体系（語彙とその定義とそれらの関係のことを指す。  

- ヘビーウェイトオントロジー  

- ライトウェイトオントロジー  

- ワトソン  


### 第3次AIブーム（2000 -: 機械学習と深層学習による人工知能）

- 機械学習

- ディーブラーニング

- 特徴量  
データをよく表す特徴を数値で示したもの（ex. 「人間」を表す特徴量としては、身長、体重、年齢、性別など）

- 特徴量エンジニアリング  
モデルが認識しやすいような「特徴」をデータから新しく作ること。  
たった1つの成分だけが 1、残りの成分が 0 という特徴量（ベクトル）に変換する。この形のことを [one-hot-encoding](https://ja.wikipedia.org/wiki/One-hot) と呼ぶ。

- 内部表現  
ディープラーニングにより自動的に獲得された特徴量。

- [ILSVRC (Large Scale Visual Recognition Challenge)](http://www.image-net.org/challenges/LSVRC/)  
2010年から始まった ImageNet データセットを用いた画像認識の精度を競うコンペ。  
2012年、トロント大学の[ジェフリー・ヒントン](https://ja.wikipedia.org/wiki/%E3%82%B8%E3%82%A7%E3%83%95%E3%83%AA%E3%83%BC%E3%83%BB%E3%83%92%E3%83%B3%E3%83%88%E3%83%B3)教授のチームが [AlexNet](https://en.wikipedia.org/wiki/AlexNet) と呼ばれる畳み込みニューラルネットワーク(CNN)で[2位以下を10%上回る正答率](http://image-net.org/challenges/LSVRC/2012/results.html)を出す。これがきっかけとなり、ディーブラーニングが脚光を浴びる。

[人工知能](https://ja.wikipedia.org/wiki/%E4%BA%BA%E5%B7%A5%E7%9F%A5%E8%83%BD) > [機械学習](https://ja.wikipedia.org/wiki/%E6%A9%9F%E6%A2%B0%E5%AD%A6%E7%BF%92) > [ニューラルネットワーク](https://ja.wikipedia.org/wiki/%E3%83%8B%E3%83%A5%E3%83%BC%E3%83%A9%E3%83%AB%E3%83%8D%E3%83%83%E3%83%88%E3%83%AF%E3%83%BC%E3%82%AF) > [ディープラーニング](https://ja.wikipedia.org/wiki/%E3%83%87%E3%82%A3%E3%83%BC%E3%83%97%E3%83%A9%E3%83%BC%E3%83%8B%E3%83%B3%E3%82%B0)

- [モラベックのパラドックス](https://ja.wikipedia.org/wiki/%E3%83%A2%E3%83%A9%E3%83%99%E3%83%83%E3%82%AF%E3%81%AE%E3%83%91%E3%83%A9%E3%83%89%E3%83%83%E3%82%AF%E3%82%B9)  
子供のできることほど人工知能には難しい

## :ghost: 人工知能分野の問題

- [シンギュラリティー（技術的特異点）](https://ja.wikipedia.org/wiki/%E6%8A%80%E8%A1%93%E7%9A%84%E7%89%B9%E7%95%B0%E7%82%B9)  
[レイ・カーツワイル](https://ja.wikipedia.org/wiki/%E3%83%AC%E3%82%A4%E3%83%BB%E3%82%AB%E3%83%BC%E3%83%84%E3%83%AF%E3%82%A4%E3%83%AB) が提唱した、人工知能が人間を超えて文明の主役に取って代わる時点。カーツワイルは自著「The Singularity Is Near」で「シンギュラリティは2045年に到来する」と述べた。

- トイ・プロブレム

- フレーム問題  
ある問題を解決する際に、その問題に関連する、考慮すべき事柄を抽出することが AI には難しいこと

- 強いAI  
フレーム問題を打破し、人間のようにあらゆる問題に適切に対処できるようになった AI

- 弱いAI  
フレーム問題に縛られたままの AI

- シンボルグラウディング問題  
記号システム内のシンボルがどのようにして実世界の意味と結び付けられるかという問題

- [He saw a woman in the garden with a telescope](https://www.deepl.com/ja/translator#en/ja/He%20saw%20a%20woman%20in%20the%20garden%20with%20a%20telescope)

- 特徴量設計  

## :robot: 機械学習

機械学習はデータが命。データから答えを探し、データからパターンを見つけ、データからストーリーを語る。  
機械学習の中心には「データ」があり、このデータ駆動によるアプローチは、「人」を中心とするアプローチからの脱却とも言える。  
重みパラメータの値をデータから自動で計算できる。（学習する）

### 処理の流れ
機械学習の処理は大きく「学習」と「推論」ステップに分かれる。  
- 学習  
事前に与えられたデータからモデルをつくること  
学習が終わったモデルには、学習データの統計的な傾向や規則性が反映されている。

- 推論  
実環境で得られるデータなどを使い、学習済みモデルを使って判定、分類、予測などを行う

### 代表的な手法

- 教師あり学習  
教師データ（入力とそれに対応する正解ラベルの組）を使って予測値を正解ラベルに近づけることを目標に学習する手法  
自然言語処理、スパムメールフィルタリング、手書き文字認識などの応用がある。

- 教師なし学習  
教師データを使わずに、データの本質的な構造を浮かび上がらせる手法  
クラスタリングやデータ次元圧縮技術などがこれに含まれる。

- 強化学習  
ゴールや目標を仮定せず、学習を行う「エージェント」が状態を観察し、環境からの報酬を最大化するように試行錯誤しながら行動を選択することで学習を行う。  
ロボット操作などに使われることが多い。

- 転移学習  
すでにある領域で学習済みのモデルを他の領域に流用する手法

- 半教師あり学習  
教師あり学習におけるラベル付けコストを低減するために用いられる手法。
データの一部分にのみ正解ラベルをつける。

- 回帰問題  
統計学に置いて、目的変数と説明変数の関係を明らかにすることで、未知のデータ属性の値を既知のデータ属性から予測できる。
（ex. 家賃の高さを広さ、築年数、駅からの近さの値から計算）

- 線形回帰  
入力データが1つの単回帰分析、複数の入力データの重回帰分析などの種類がある

- 分類問題  
あらかじめ設定したクラスにデータを割り振る（ex. 画像に写っている犬や猫の識別）。  
サポートベクターマシン、決定木、ランダムフォレスト、ロジスティック回帰、kNN法などの手法がある。深層学習でも分類を行うことができる。

- クラスタリング  
分類と違い、事前にクラスなどの分類の軸が提供されないため、与えられたデータの特徴などから自動的にクラスタを構成する。  
事前学習が不要なため、過去のデータがない場合でもクラスタ化可能だが、クラスに基づく分類とは異なる結果がでる場合がある。  
代表的なアルゴリズムに k平均法などがある。

#### 代表的な「予測」アルゴリズム

| アルゴリズム | 回帰 | 分類 | クラスタリング |
| :---: | :---: | :---: | :---: |
| 線形回帰 | o | x | x |
| ロジスティック回帰 | x | o | x |
| サポートベクターマシン | o | o | x |
| ナイーブベイズ | x | o | x |
| 決定木 | o | o | x |
| ランダムフォレスト | o | o | x |
| ニューラルネットワーク | o | o | x |
| kNN | o | o | x |
| k-means | x | x | o |

### データの前処理

データをモデルに正しく入力できるようにする。  
データの大きさをある程度均一にする。

- 正規化  
データを 0 から 1 に収まるようにスケーリングすること

- 標準化  
平均を 0、標準偏差（分散）を 1 に変換すること

- 正則化  
過学習を抑制するための手法。  
誤差関数にパラメータのノルムによる正則化（LASSOなど）を付け加える

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
論理ゲートでは OR, AND, NAND は線形分離可能だが、XOR のみ線形分離不可能。

- [SVM (サポートベクターマシン)](https://ja.wikipedia.org/wiki/%E3%82%B5%E3%83%9D%E3%83%BC%E3%83%88%E3%83%99%E3%82%AF%E3%82%BF%E3%83%BC%E3%83%9E%E3%82%B7%E3%83%B3)  
「マージン最大化」というコンセプトで2つのクラスを線形分離可能にするアルゴリズム。  
もともとは2つのクラス分類アルゴリズムとして考案されたが、性能がいいので多クラス分類や回帰分析にも応用されている。  
線形分離可能でないデータに対しても、カーネル法を組み合わせることで決定境界を求めることができる。  
未学習のデータに対しても高い識別性能があるが、仮説の設定や特徴の選択が必要。

- [スラック変数](http://sudillap.hatenablog.com/entry/2013/04/08/235602)  
超平面を構成した結果として発生する誤差の程度を測る変数。

- [ハイパーパラメータ](https://ja.wikipedia.org/wiki/%E3%83%8F%E3%82%A4%E3%83%91%E3%83%BC%E3%83%91%E3%83%A9%E3%83%A1%E3%83%BC%E3%82%BF)  
推論や予測の枠組みの中で決定されないパラメータ。  
SVM においては誤りをどの程度許容するかの度合いをエンジニアが事前に調整する必要がある。

- [カーネル法](https://ja.wikipedia.org/wiki/%E3%82%AB%E3%83%BC%E3%83%8D%E3%83%AB%E6%B3%95)  
次のアイディアをカーネル関数の計算によって実現するもの  
・ データを高次元空間にうまく埋め込む  
・高次元空間で線形分離 (SVM) し、その境界を元の空間に戻す

- カーネルトリック  
カーネル関数を使って、計算複雑度の増大を抑えつつ内積にもとづく解析手法を高次元特徴空間へ拡張するアプローチ。  
計算量を現実的に抑えつつ、非線形分離を実現する。

- 決定木  
性質（ex. 男女）や数値（ex. 購入数5個以上/未満）に基づき、データを木構造に分類する手法。予測にも使える。  
人が理解しやすく前処理が服内が、過学習を起こしやすい。  

  1. 不純度が最も減少（情報利得が最も増加）するように、条件分岐を作りデータを振り分ける  
  2. それを繰り返す  

  不純度とは「クラスの混じり具合」を表す指標で、代表的なものにジニ係数やエントロピーがある。

- ランダムフォレスト  
ランダムに選んだ学習データを説明変数を用いて決定木群を作成し、その多数決や平均値を結果として出力する  
決定木にバギングを組み合わせていて、以下のような利点があり、非常によく使われている。  
  - データの前処理が少なくて済む  
  - 安定して良い精度が出る
  
  一方で、中身がブラックボックス化するという面もある。

- バギング  
アンサンブル学習の一種で、複数のモデルを使用し、それらの平均の多数決をとって予測結果とする

- アンサンブル学習  
複数の学習モデルを組み合わせて1つの学習モデルを生成する手法

- [ロジスティク回帰](https://ja.wikipedia.org/wiki/%E3%83%AD%E3%82%B8%E3%82%B9%E3%83%86%E3%82%A3%E3%83%83%E3%82%AF%E5%9B%9E%E5%B8%B0)  
AかBどちらかしか起こらない確率などに、事象がどちらかに分類できるかの確率を計算する。  
線形回帰を分類問題に応用したアルゴリズム。  
  1. 「対数オッズ」を重回帰分析により予測する  
  2. 「対数オッズ」をロジスティック関数（シグモイド関数）で変換することで、クラスiに属する確率piを求める  
  3. 各クラスに属する確率を計算し、最大確率を実現するクラスが、データの所属するクラスと予測する  

  また、「ロジット変換」を行うことで、出力値が 0 から 1 の間の値に正規化され、確率としての解釈が可能になる

- [kNN法 (k-nearest neighbor)](https://ja.wikipedia.org/wiki/K%E8%BF%91%E5%82%8D%E6%B3%95)  
クラス分類のアルゴリズムの一種。   
データから近い順に k 個のデータを見て、それらの多数決によって所属クラスを決定する。  
kNN法は柔軟にモデルを作れるが、実用上、以下の条件がないと精度が上がらない弱点がある。  
  - 各クラスのデータ数に偏りがない  
  - 各クラスがよく別れている  

- ベイズ推定  
確率の初期状態（事前確率）に対して、得られたデータにより確率（事後確率）を計算（ベイズ更新）して推定を行う  
データを増やすことで精度を向上できるが、学習データで仮定した確率分布以外では未対応。

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
多次元のデータに対して正味に効果のあるより少ない成分を抽出（次元の削減）する手法。  
データから「主成分」という新たなデータを求める、線形な次元削減の手法。  
変数間に相関のないデータに対しては有効でない。

- [k-means (k平均法)](https://www.albert2005.co.jp/knowledge/data_mining/cluster/non-hierarchical_clustering)  
異なる性質のものが混ざり合った集団から、互いに似た性質を持つものを集め、クラスターを作る方法の1つ。  
あらかじめいくつのクラスターに分けるかを決め、決めた数の塊（排他的部分集合）にサンプルを分割する。  
手法が理解しやすく、大規模なデータにも適応可能。

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


### 用語

- [No Free Lunch（ノーフリーランチ）定理](https://ja.wikipedia.org/wiki/%E3%83%8E%E3%83%BC%E3%83%95%E3%83%AA%E3%83%BC%E3%83%A9%E3%83%B3%E3%83%81%E5%AE%9A%E7%90%86)  
一つの学習済みモデルで様々用途に対応できるわけではないこと数学的に証明した定理

- [みにくいアヒルの子定理](https://dic.nicovideo.jp/a/%E3%81%BF%E3%81%AB%E3%81%8F%E3%81%84%E3%82%A2%E3%83%92%E3%83%AB%E3%81%AE%E5%AD%90%E3%81%AE%E5%AE%9A%E7%90%86)  
1969年に情報理論学者・理論物理学者の[渡辺慧](https://ja.wikipedia.org/wiki/%E6%B8%A1%E8%BE%BA%E6%85%A7)が提唱した定理。  
対象がもつ特徴をすべて同等に評価すると識別が困難になること。  
機械学習で行われる「特徴選択」や「次元削減」といった処理が人間の主観的な特徴選択と同様であり、識別にとって本質的であることも示している

## :globe_with_meridians: ディープラーニング

ディープニューラルネットワークを用いた機械学習の手法。  
2010年代に脚光を浴びたが、アルゴリズム自体は1960年代にはすでに考案されていた。  

深い関数を使った最小二乗法。  
シグモイド関数など活性化関数を使って非線形性を入れ、多層に構成した関数を使った、損失関数の最小化。

### ニューラルネットワーク

- ニューロン  
単純な数値予測ができ予測器。ニューラルネットワークの最小単位  
重みが乗算された入力を受け取り、それらを総和して出力する

- ニューラルネットワーク  
ニューロンをたくさんつなげててきる予測器。入力が行わる層を「入力層」、出力される層を「出力層」、それ以外の層を「中間層」または「隠れ層」と呼ぶ。  
人間の脳を模倣したモデルではなく、「人間の脳の仕組みの一部」を模倣している。

- [ネオコグニトロン](https://ja.wikipedia.org/wiki/%E3%83%8D%E3%82%AA%E3%82%B3%E3%82%B0%E3%83%8B%E3%83%88%E3%83%AD%E3%83%B3)  
1982年に福島邦彦氏によって発表された畳み込みニューラルネットワークの発想の基となったネットワークモデル

- 宝くじ仮説  
「ランダムに初期化された密なニューラルネットワークは、たまたまうまく学習ができるように初期化されたサブネットワークが含まれており、このサブネットは、学習が進むにつれて他のサブネットよりも優れているので早く学習が進み、他の劣るサブネットの活性が抑制される」という仮説。  
この仮説を提唱した論文「[The Lottery Ticket Hypothesis: Finding Sparse, Trainable Neural Networks](https://arxiv.org/abs/1803.03635)」は、2019年5月にはディープラーニングのカンファレンス ICLR 2019で [Best Paper Award](https://iclr.cc/Conferences/2019/Awards) に選ばれた。

#### 学習の手順

1. ミニバッチ  
訓練データの中からランダムに一部のデータを選び出す。   
その選ばれたデータをミニバッチと言い、ここでは、そのミニバッチの損失関数の値を減らすことを目的とする。
1. 勾配算出  
ミニバッチの損失関数をひらすために、各重みパラメータの勾配を求める。  
勾配は、損失関数の値を最も減らす方向を示す。
1. パラメータの更新  
重みパラメータを勾配方向に微小量だけ更新する。（確率的勾配降下法）
1. 1 ~ 3 を繰り返す。

### 従来の機機械学習との違い

機械学習では、対象領域の知識に基づいて適切に手法を選択する必要があるが、ディーブラーニングでは、表現力の高い「深い関数」を用いるため、データを計算量されあれば精度が上がる。  
ディーブラーニングに適した学習データは、正規化されているものよりも、画像や音声そのもの、膨大なテキストなど。  
どうやてデータを集めるか、どうやってアノテーション（ラベルやメダデータを与えて学習データを整備）するかが課題となる。

### 用語

- [ノーフリーランチ定理](ノーフリーランチ定理)  
「あらゆる問題に対して万能なアルゴリズムは存在しない」という定理

- 単純パーセプトロン

- 多層パーセプトロン

- オートエンコーダ  
2006年に発表され、今日のディーブラーニング隆盛のきっかけともなった技術。  
次元数を減らしたニューロン層を重ねていくことで特徴の圧縮を行うエンコーダと逆の構造を持つデコーダーを接続したもの。  
砂時計型の構造をもつニューラルネットワークで、入力側から半分をエンコーダ、残り半分をデコーダーと呼ぶ。  
入力層と出力層のノード数が等しく、中間層のノード数が入出力層よりが少ない。  
入力情報と同じ出力情報を再現するこを目指す（「正解ラベル」として「入力自身」を用いる）

- 次元削減  
オートエンコーダにおいて、隠れ層で特徴的な情報だけに次元を圧縮すること

- ディープオートエンコーダ  
オートエンコーダを順番に学習させ、それを積み重ねる手法。  
ディープニューラルネットワークのように一気にすべての層を学習するのではなく、**入力層に近い層から順番に学習されるという、逐次的な方法をとった。**  
事前学習とファインチューニングの工程で構成される。

- 事前学習  
オートエンコーダを順番に学習していく手法

- ファインチューニング  
最後にロジスティック回帰層（シグモイド関数あるいはソフトマックス関数による出力層）を足すことで、教師学習を実現する。  
これにより、ネットワーク全体は隠れ層が複数あるディープニューラルネットワークになる。  
事前学習を終え、ロジスティック回帰層を足したら、最後の仕上げとしてディープニューラルネットワーク全体で学習を行い重みを調整する。

### 活性化関数

入力信号の総和を出力信号に変換する関数。  
出力層で使用する活性化関数は、回帰問題では恒等関数、分類問題ではソフトマックス関数を一般的に利用する。

パーセプトロンとニューラルネットワークの主な違いは、活性化関数。  
パーセプトロンではステップ関数、ニューラルネットワークではシグモイド関数など非線形関数を用いる。

- ステップ関数  
微分できないのでニューラルネットワークの学習で実際に使われることはない

- [シグモイド関数](https://ja.wikipedia.org/wiki/%E3%82%B7%E3%82%B0%E3%83%A2%E3%82%A4%E3%83%89%E9%96%A2%E6%95%B0)  
入力を 0 ~ 1の間に値に変換する性質を持つ関数。  
ステップ関数と形が似ていて、なめらかなので微分できる関数として考案された

- [tanh (ハイパボリックタンジェント関数)](https://ja.wikipedia.org/wiki/%E5%8F%8C%E6%9B%B2%E7%B7%9A%E9%96%A2%E6%95%B0)  

- [ReLU関数](https://ja.wikipedia.org/wiki/%E6%AD%A3%E8%A6%8F%E5%8C%96%E7%B7%9A%E5%BD%A2%E9%96%A2%E6%95%B0)  
正則化機能を持たいない活性化関数で、勾配消失問題が起きにくく、最近の主流。  
入力が 0 を超えていればその入力をそのまま出力し、0 以下ならば 0 を出力する。  

- ソフトマックス関数  
出力を正規化して、確率として解釈する際に用いされる活性化関数。
分類問題の出力層付近で用いられることが一般的。

- Leaky ReLU関数  

- Parametric ReLU  

- Randomized ReLU  

### 学習の流れ
1. 教師データを用いて予測計算をする。その際の予測値を正解ラベルと比較して誤差を計算する。
1. 予測値は左から右へと順番に伝わる（順伝播）
1. 上記をいくつかの教師データについて繰り返し、誤差を足し合わせる
1. 累計された誤差が小さくなるように、勾配降下法を用いて各枝の重みを更新する。  
   枝の重みは右から左へと順番に更新される（誤差逆伝伝播法）
1. 上記を繰り返す

### 学習率の最適化
- [勾配降下法](https://ja.wikipedia.org/wiki/%E7%A2%BA%E7%8E%87%E7%9A%84%E5%8B%BE%E9%85%8D%E9%99%8D%E4%B8%8B%E6%B3%95)  
重みを少しずつ更新して勾配が最小になる点を探索するアルゴリズム。  
ディープニューラルネットワークの学習では、「局所最適解が求められればそれなりに誤差の値は小さくなるだろうから、それで妥協しよう」というスタンスに立つ。

  - 局所最適解  
    園周辺では誤差の値は小さいが、最小値を実現するわけではない解
  - 大局的最適解  
    誤差の値を最も小さくする解
  - 停留点  
    局所最適解でも大局的最適解でもないが、勾配が 0 になる点
  - 鞍点（あんてん）  
    停留点のうち、ある方向から見ると極小値だが、別の方向から見ると極大値になる点

- [誤差関数](https://ja.wikipedia.org/wiki/%E8%AA%A4%E5%B7%AE%E9%96%A2%E6%95%B0)  

- エポック  
1エポックとは、学習において訓練データをすべて使い切ったときの回数に対応する。
（訓練データを何度学習に用いたか）

- イテレーション  
  重みを何度更新したか

- SGD (確率的勾配降下法)  
無作為に選びだしたデータ（ミニバッチ）に対して行う勾配降下法。  
訓練データ1つに対して、重みを1回更新する（データ１つごとにイテレーションが増える）  
関数の形状が等方向的でないと非効率な経路で探索することが欠点、

- ミニバッチ勾配降下法  
ミニバッチに含まれるすべてのデータについて誤差の総和を計算し、その総和を小さくするように重みを1回更新する。  
ミニバッチは、いくつかの訓練データからランダムにサンプリングした小さなデータの集まり。

- 勾配降下法  
訓練データすべての誤差を計算し、重みを1回更新する（イテレーションとエポックが等しい）

- 蒸留  
大きいネットワークの入出力を小さいネットワークに再学習される手法

- Adadelta  

- 勾配消失問題  
誤差の勾配を逆伝播する過程において、勾配の値が消出し入力層付近での学習が進まなくなるディープニューラルネットワーク特有の現象。層が深いほど起こりやすい。  
活性化関数が何度も作用することで勾配が小さくなりすぎてしまうことが原因とされる。

### 最適化

- Momentum  
ボールが地面を転がるように、損失関数上での今までの動きを考慮することで SG Dの振動を抑える手法

- AdaGrad  
勾配降下法の学習率に関する手法。  
パラメータの要素ごとに適応的に学習係数を調整しながら学習を行う手法。

- RMSProp  
AdaGrad は学習雨を進めれば進めるほど、更新度合いは小さくなり、無限に学習すると、更新量は 0 になる。この問題を改善した手法が、RMSPop。  
過去のすべての勾配を均一に加算していくのではなく、過去の勾配を徐々に忘れて新しい勾配の情報が大きく反映されるように加算する手法。

- Adam  
2015年に提案された、直感的には、Momentum と　AdaGrad を融合した手法。  
先の2つの手法の利点を組み合わせることで、効率的にパラメータ空間を探索することが期待できる。  
ハイパーパラメータの補正が行われていることも特徴。


### テクニック
- ドロップアウト  
重み更新の際に一定の割合でランダムに枝を無効化する手法。単純だが効果が高い。  
アンサンブル学習と近い関係にある。

- early stopping  

- 正規化  

- 標準化  

- 白色化  

- バッチ正規化  


### CNN: 畳み込みニューラルネットワーク

特に画像認識に応答するために改良されたディープニューラルネットワーク。  
自動運転技術など、非常に広く応用されている。

従来のシグモイド関数のような活性化関数では、層が深くなるにつれ勾配が小さくなってくのでうまく学習ができないので、勾配消失問題を解決した ReLU関数を用いる。

#### 処理の流れ

1. 畳み込み層  
フィルタを用いて積和演算 + 活性化関数の作用を行う層。  
元の画像の特徴が抽出された小さな画像である「特徴マップ」に変換される。

2. プーリング層  
畳み込み層から「特徴マップ」を受け取り、平均値、最大値を用いてサブサンプリングを行う層。  
平均プーリング、最大プーリングによって更に小さな画像に変換される。

3. 全結合層  
プーリング層から出力された画像データを、縦横に並んだ2次元データから、一列に並べたフラットな1次元データに変換する出力層

#### 手法

- LeNet  
1988年に提案された、手書き数字認識を行うネットワーク。  
シグモイド関数を使用して、サンプリングによって中間データのサイズ縮小を行っている。  
初めての CNN。

- AlexNet  
2012年の ILSVRC でトロント大学のジェフリー・ヒントン率いるチームが用いた手法。 
  - 活性化関数に ReLU を使用
  - LRN (Local Response Noralization) という、局所的正規化を行う層を用いる
  - ドロップアウトを使用する

- maxプーリング  

- avgプーリング  

- データ拡張  

- VGG  
畳み込み層とプーリング層から構成される基本的な CNN。  
重みのある層を全部で16層まで重ねてディープにしている。  
3x3 の小さなフィルターによる畳み込み層を連続して行っている点が特徴。

- GoogLeNet  
基本的には CNN と同じ構成で、ネットワークが縦方向の深さだけでなく、横方向にも深さ（広がり）を持っているのが特徴。  
横方向の幅は「インセプション構造」と呼ばえる。  

- Skip connection  
層を飛び越えた結合

- 転移学習  
学習済みのネットワークを利用して新しいタスクの識別に利用すること

### RNN: リカレントニューラルネットワーク

時系列データにおいて、ある時間的に近接した要素同士は影響を与え合う可能性が高いが、時間的に遠く離れた要素が影響を与えることは少ない。  
この性質を使えば、パラメータの数を減らすことができる。これが RNN である。

時系列データを入力して、データから時間依存性を学習できるモデル。  
内部に閉路（行って戻ってくる経路）を持つニューラルネットワーク。  
RNN は過去の情報を保持できるため、過去の入力を参考に「時系列データの次の時点での値」を予測する。  
自然言語処理への応用が盛んで、機械翻訳技術などに応用されている。

- 入力重み衝突  

- 出力重み衝突  

- BPTT (Backpropagation Through Time)  
RNN を順伝播型ネットワークに置き換えて誤差逆伝播法を適用する手法

- CTC  
入出力間で系列長が違う場合のニューラルネットワークを用いた分類法

- LSTM (Long Short-Term Memory)  
遠い過去の入力を現在の出力に反映する手法

- seq2seq  
時系列データを入力・処理し、時系列データを出力するモデル。  
代表的な応用として入力と出力を異なる言語列とする翻訳が実現できる。  
これは NMT（ニューラル機械翻訳）と呼ばれ、従来の SMT（統計的機械翻訳）よりも大幅に性能が向上している。

- GRU (Gated Recurrent Unit)  

- Bidirectional RNN  
LSTM を2つ組み合わせることで、未来から過去方向も含めて学習できるモデル

- Sequence-to-Sequence  
入力が時系列なら出力も時系列で予測する。自然言語処理を中心に研究されている分野。

- RNN Encoder–Decoder

- Attention  
過去の時点それぞれの重みを学習することで、時間の重みをネットワークに組み込む。

### 深層強化学習

システムが「状態」を定義し、試行錯誤を重ねながら、自動的に報酬を最大化する「方策」を見つけることができる。  
さらに探索による先読みを組み合わせることで、AlphaGo（碁）の躍進につながった。

- 強化学習  
行動を学習する仕組み。目的とする報酬（スコア）を最大化するためにはどのような行動をとっていけばいいかを学習していく。  
機械学習では、想定する「状態」の数が非常に多くなったり、人による「状態」の想定に限界があったりした。

- [BRETT](https://engineering.berkeley.edu/brett/)  
カリフォルニア大学バークレー後が開発している、ディーブラーニングと強化学習を組み合わせたロボット。  
報酬の設定を変更すれば、異なる動作を学習することができる。  
一旦学習した内容はコピーして、同じタイプのロボットであれば同じように動かすことができる。

- Q学習

- [DQN (Deep Q-Network)](https://ja.wikipedia.org/wiki/DQN_(%E3%82%B3%E3%83%B3%E3%83%94%E3%83%A5%E3%83%BC%E3%82%BF))  
DeepMind が考案した、Q学習の行動価値関数を、深い構造を持ったニューラルネットワークで置き換えたモデル。  
アタリ社のゲームを学習された例では、49ゲームのうち29ゲームで、人間並、あるいはそれ以上のスコアを出した。

### 深層生成モデル

ディーブラーニング技術は、識別や回帰だけでなく、これまで存在していなかったデータ、例えば架空の画像の生成にも利用できる。  
一般に「生成モデル」と呼ばれるモデルを使うことで、AI 技術による「創作」が可能となる。  
ディープニューラルネットワークを使った生成モデルは「深層生成モデル」と呼ばれる。

- WaveNet  

- 生成モデル  

- VAE (変分オートエンコーダ)  
オートエンコーダの中間層の圧縮された特徴表現の数値を確率分布に従うように変更し、さらにエンコーダの出力とデコーダーの入力をこれにあわせて変更したのもの。  
確率分布に従うことで、圧縮された特徴表現の数値を変動させ、デコーダーの所期の性能（いろいろな猫の画像の生成）を達成できる。

- GAN (敵対的生成ネットワーク)  
2014年にイアン・グッドフェローらによって発表された、生成ネットワークと識別ネットワークからなる教師なし学習法。  
トレーニングに利用したデータに類似した出力を生成できるため、希少データの水増しや、作風をまねた絵画や楽曲の生成など、様々な応用が進められている。

  - 生成ネットワーク  
    ランダムノイズベクトルから入力データのレプリカを作ろうとする
    訓練データと同じようなデータを生成する

  - 識別ネットワーク  
    そのデータが訓練データから来たものか、生成ネットワークから来たものかを識別する

- DCGAN (Deep Convolutional GAN)  

### GNN: グラフニューラルネットワーク

グラフ構造（データ間のつながりを持った構造）のデータを入力とするニューラルネットワーク。  
GNN やオートエンコーダ、RNN を構築することができるため、広範囲の応用が可能。  
分子構造の予測や自然言語処理などへの応用がある。

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
  1. 著作権法
  2. 不正競争防止法
  3. 個人情報保護法
  4. 個別の契約
  5. その他の理由により、データの利用に制約がかかっている場合

- 日本の著作権法  
著作権法47条の７によって、著作者にモダンで記録や翻案をしても適法となっている。2018年の著作権法改正によって、学習データを第三者と共有したり、一般に販売したり、ネット上で公開するとことも、一定の条件下で適法となっている（改正著作権法30条4）

- オープン・イノベーション  

- [AI・データの利用に関する契約ガイドライン](https://www.meti.go.jp/press/2018/06/20180615001/20180615001.html)  

- データセットの偏り  

- プライバシーリスクを低減するデータ加工  

- 協調フィルタリング  

- [FAT (Fairness, Accountability, and Transparency)](https://www.fatml.org/)  
AIの公平性、説明可能性、透明性

- 敵対的な攻撃  

- 知的財産法  

- GDPR  
欧州経済領域（EEA）内の個人データの保護を規定する法律であり、データ管理者及びデータ処理者に対し、個人データの取り扱いや移転に係る義務を定めている。  
2016年4月に制定され、2018年5月に施行された。

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

- [人間中心のAI社会原則検討会議](https://www8.cao.go.jp/cstp/tyousakai/humanai/index.html)  
2018年5月に内閣府のCSTIの下に設置された会議。  
AIに関する倫理や中長期的な研究開発・利活用などについて、産学民官のマルチステークホルダーによる幅広い視野からの調査・検討が行われ、2019年3月に「人間中心のAI社会原則」が決定された。

- XAI (説明可能なAI)  
ディーブラーニングを使う機械学習では、特徴抽出も自動化されているため、与えられたデータに対する推論過程そのものが「見えない」状態となる。  
しかし、自動運転や医療診断など、推論結果が重大な問題を引き起こす可能性があるものに関しては、原因究明が要請される。

## 🏢 事例
- [BRETT: Deep-learning robot](https://engineering.berkeley.edu/brett/)
- [AlphaGo](https://ja.wikipedia.org/wiki/AlphaGo)
- [Google DeepMind's Deep Q-learning playing Atari](https://deepmind.com/research/publications/playing-atari-deep-reinforcement-learning)
- [分身ロボットカフェ DAWN](https://dawn2019.orylab.com/)

## :books: 参考資料

### 書籍
- [深層学習教科書 ディープラーニング G検定公式テキスト](https://www.shoeisha.co.jp/book/detail/9784798157559)
- [徹底攻略 ディープラーニングG検定 ジェネラリスト 問題集](https://book.impress.co.jp/books/1118101076)
- [AI白書 2020](https://www.ipa.go.jp/ikc/publish/ai_hakusyo.html)
- [ゼロから作るDeep Learning ―Pythonで学ぶディープラーニングの理論と実装](https://www.oreilly.co.jp/books/9784873117584/)
- [なっとく！ディープラーニング](https://www.shoeisha.co.jp/book/detail/9784798166247)

### WEB
- [ニコニコAIスクール](http://nico2.ai/)
  - 最終回: 脳神経科学と汎用人工知能 (福島邦彦)
- [G検定模擬テスト - Study-A](http://study-ai.com/generalist/)

### Youtube

#### 松尾豊
- [2014/11/01 人工知能が閻魔大王になる日 - Video News](https://www.youtube.com/watch?v=U-O4eINZNXE)
- [2015/06/05 人工知能は人間を超えるか ディープラーニングの先にあるもの - #LYVE](https://www.youtube.com/watch?v=lqywEafvq_Q)
- [2015/11/03 人工知能の未来～ディープラーニングの先にあるもの - GLOBIS](https://www.youtube.com/watch?v=GbmKWY7SLng)
- [2016/08/02 人工知能は人間を超えるか - SoftBank World 2016](https://www.youtube.com/watch?v=7bvfl_M5vPQ)

#### NDIVIA
- [ディープ・ラーニング最新技術情報 何故GPUはディープラーニングに向いているか](https://www.youtube.com/watch?v=1aHQ2tVVlj8)
