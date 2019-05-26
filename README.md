<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [機械学習のまとめ](#%E6%A9%9F%E6%A2%B0%E5%AD%A6%E7%BF%92%E3%81%AE%E3%81%BE%E3%81%A8%E3%82%81)
  - [『Pythonではじめる機械学習 ―scikit-learnで学ぶ特徴量エンジニアリングと機械学習の基礎』まとめ](#%E3%80%8Epython%E3%81%A7%E3%81%AF%E3%81%98%E3%82%81%E3%82%8B%E6%A9%9F%E6%A2%B0%E5%AD%A6%E7%BF%92-%E2%80%95scikit-learn%E3%81%A7%E5%AD%A6%E3%81%B6%E7%89%B9%E5%BE%B4%E9%87%8F%E3%82%A8%E3%83%B3%E3%82%B8%E3%83%8B%E3%82%A2%E3%83%AA%E3%83%B3%E3%82%B0%E3%81%A8%E6%A9%9F%E6%A2%B0%E5%AD%A6%E7%BF%92%E3%81%AE%E5%9F%BA%E7%A4%8E%E3%80%8F%E3%81%BE%E3%81%A8%E3%82%81)
    - [sklearnでデータセットを訓練データとテストデータに分割する](#sklearn%E3%81%A7%E3%83%87%E3%83%BC%E3%82%BF%E3%82%BB%E3%83%83%E3%83%88%E3%82%92%E8%A8%93%E7%B7%B4%E3%83%87%E3%83%BC%E3%82%BF%E3%81%A8%E3%83%86%E3%82%B9%E3%83%88%E3%83%87%E3%83%BC%E3%82%BF%E3%81%AB%E5%88%86%E5%89%B2%E3%81%99%E3%82%8B)
    - [教師あり学習は分類と回帰に大別できる](#%E6%95%99%E5%B8%AB%E3%81%82%E3%82%8A%E5%AD%A6%E7%BF%92%E3%81%AF%E5%88%86%E9%A1%9E%E3%81%A8%E5%9B%9E%E5%B8%B0%E3%81%AB%E5%A4%A7%E5%88%A5%E3%81%A7%E3%81%8D%E3%82%8B)
    - [汎化とは](#%E6%B1%8E%E5%8C%96%E3%81%A8%E3%81%AF)
    - [過剰適合](#%E9%81%8E%E5%89%B0%E9%81%A9%E5%90%88)
  - [『機械学習入門 ボルツマン機械学習から深層学習まで』まとめ](#%E3%80%8E%E6%A9%9F%E6%A2%B0%E5%AD%A6%E7%BF%92%E5%85%A5%E9%96%80-%E3%83%9C%E3%83%AB%E3%83%84%E3%83%9E%E3%83%B3%E6%A9%9F%E6%A2%B0%E5%AD%A6%E7%BF%92%E3%81%8B%E3%82%89%E6%B7%B1%E5%B1%A4%E5%AD%A6%E7%BF%92%E3%81%BE%E3%81%A7%E3%80%8F%E3%81%BE%E3%81%A8%E3%82%81)
  - [『はじめてのディープラーニング』まとめ](#%E3%80%8E%E3%81%AF%E3%81%98%E3%82%81%E3%81%A6%E3%81%AE%E3%83%87%E3%82%A3%E3%83%BC%E3%83%97%E3%83%A9%E3%83%BC%E3%83%8B%E3%83%B3%E3%82%B0%E3%80%8F%E3%81%BE%E3%81%A8%E3%82%81)
    - [２次元配列のスライス](#%EF%BC%92%E6%AC%A1%E5%85%83%E9%85%8D%E5%88%97%E3%81%AE%E3%82%B9%E3%83%A9%E3%82%A4%E3%82%B9)
    - [多次元配列の軸](#%E5%A4%9A%E6%AC%A1%E5%85%83%E9%85%8D%E5%88%97%E3%81%AE%E8%BB%B8)
    - [numpyのwhere関数](#numpy%E3%81%AEwhere%E9%96%A2%E6%95%B0)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# 機械学習のまとめ
- 参考
  - [Pythonではじめる機械学習 ―scikit-learnで学ぶ特徴量エンジニアリングと機械学習の基礎](https://www.amazon.co.jp/Python%E3%81%A7%E3%81%AF%E3%81%98%E3%82%81%E3%82%8B%E6%A9%9F%E6%A2%B0%E5%AD%A6%E7%BF%92-%E2%80%95scikit-learn%E3%81%A7%E5%AD%A6%E3%81%B6%E7%89%B9%E5%BE%B4%E9%87%8F%E3%82%A8%E3%83%B3%E3%82%B8%E3%83%8B%E3%82%A2%E3%83%AA%E3%83%B3%E3%82%B0%E3%81%A8%E6%A9%9F%E6%A2%B0%E5%AD%A6%E7%BF%92%E3%81%AE%E5%9F%BA%E7%A4%8E-Andreas-C-Muller/dp/4873117984)
  - [機械学習入門 ボルツマン機械学習から深層学習まで](https://www.amazon.co.jp/gp/product/4274219984/ref=ppx_yo_dt_b_asin_title_o08_s00?ie=UTF8&psc=1)
  - [はじめてのディープラーニング](https://www.amazon.co.jp/%E3%81%AF%E3%81%98%E3%82%81%E3%81%A6%E3%81%AE%E3%83%87%E3%82%A3%E3%83%BC%E3%83%97%E3%83%A9%E3%83%BC%E3%83%8B%E3%83%B3%E3%82%B0-Python%E3%81%A7%E5%AD%A6%E3%81%B6%E3%83%8B%E3%83%A5%E3%83%BC%E3%83%A9%E3%83%AB%E3%83%8D%E3%83%83%E3%83%88%E3%83%AF%E3%83%BC%E3%82%AF%E3%81%A8%E3%83%90%E3%83%83%E3%82%AF%E3%83%97%E3%83%AD%E3%83%91%E3%82%B2%E3%83%BC%E3%82%B7%E3%83%A7%E3%83%B3-Machine-Learning-%E6%88%91%E5%A6%BB/dp/4797396814/ref=sr_1_1?__mk_ja_JP=%E3%82%AB%E3%82%BF%E3%82%AB%E3%83%8A&keywords=%E3%81%AF%E3%81%98%E3%82%81%E3%81%A6%E3%81%AE%E3%83%87%E3%82%A3%E3%83%BC%E3%83%97%E3%83%A9%E3%83%BC%E3%83%8B%E3%83%B3%E3%82%B0&qid=1557630774&s=gateway&sr=8-1)

## 『Pythonではじめる機械学習 ―scikit-learnで学ぶ特徴量エンジニアリングと機械学習の基礎』まとめ

### sklearnでデータセットを訓練データとテストデータに分割する
- train_test_split関数を使う
- train_test_split関数は分割を行う前にデータセットをシャッフルするので、関数呼び出しのたびに同じ結果が得られるようにrandom_stateパラメータをつける
- 訓練セット75%、テストセット25%の割合で分割する

```python
from sklearn.model_selection import train_test_split
X_train, X_test, y_train, y_test = train_test_split(iris_dataset['data'], iris_dataset['target'], random_state=0)
```

### 教師あり学習は分類と回帰に大別できる
- 分類: 与えられた花の画像からあやめの種類を推測するなど。
- 回帰: 与えられたデータから将来どのようになるかを予測する。

### 汎化とは
- 教師あり学習では訓練データを用いてモデルを構築する。そのモデルが未見のデータに対しても正確に予測できるものならば、訓練セットがテストセットに対して**汎化**できていると言う。

### 過剰適合
- 訓練セットからモデルを作る際は出来るだけ適度に単純化するのが望ましいが、過剰に複雑なモデルを作成してしまうこと。
- 逆に単純化しすぎて訓練セットにもうまく機能しないことを**適合不足**という

## 『機械学習入門 ボルツマン機械学習から深層学習まで』まとめ

### 2-2
特徴量をまとめたものをベクトルという
傾きなど直線の形を決める要素をパラメータという。このパラメータを操作して、データに合うように直線を変化させていく。
データから関数を予測することを回帰という

### 2-3
重みはそれぞれの特徴量の重要度。

## 『はじめてのディープラーニング』まとめ

### ２次元配列のスライス
`配列[行のスライス指定, 列のスライス指定]`

```py
b = np.array([[0,1, 2],
              [3, 4, 5],
              [6, 7, 8]])
print(b[0:2, 0:2])

###
[[0 1]
 [3 4]]
###
```

### 多次元配列の軸
多次元列には軸がある。例えば２次元配列の場合、縦方向は`axis=0`横方向は`axis=1`
transposeメソッドを使って軸を入れ替えることができる。

```py
a = np.array([[0,1, 2], [3, 4, 5]])
print(a)
###
[[0 1 2]
 [3 4 5]]
###
print(a.transpose(1, 0))
###
[[0 3]
 [1 4]
 [2 5]]
###
```

### numpyのwhere関数
`np.where(条件, 条件を満たしている場合の値, 条件を満たしていない場合の値`
```py
a = np.array([[0, 1],
              [2, 3]])
print(np.where(a < 2, 9, a))
###
[[9 9]
 [2 3]]
###
```
