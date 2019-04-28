# 機械学習のまとめ
- 参考
  - [Pythonではじめる機械学習 ―scikit-learnで学ぶ特徴量エンジニアリングと機械学習の基礎](https://www.amazon.co.jp/Python%E3%81%A7%E3%81%AF%E3%81%98%E3%82%81%E3%82%8B%E6%A9%9F%E6%A2%B0%E5%AD%A6%E7%BF%92-%E2%80%95scikit-learn%E3%81%A7%E5%AD%A6%E3%81%B6%E7%89%B9%E5%BE%B4%E9%87%8F%E3%82%A8%E3%83%B3%E3%82%B8%E3%83%8B%E3%82%A2%E3%83%AA%E3%83%B3%E3%82%B0%E3%81%A8%E6%A9%9F%E6%A2%B0%E5%AD%A6%E7%BF%92%E3%81%AE%E5%9F%BA%E7%A4%8E-Andreas-C-Muller/dp/4873117984)
  - [機械学習入門 ボルツマン機械学習から深層学習まで](https://www.amazon.co.jp/gp/product/4274219984/ref=ppx_yo_dt_b_asin_title_o08_s00?ie=UTF8&psc=1)

## [Pythonではじめる機械学習 ―scikit-learnで学ぶ特徴量エンジニアリングと機械学習の基礎](https://www.amazon.co.jp/Python%E3%81%A7%E3%81%AF%E3%81%98%E3%82%81%E3%82%8B%E6%A9%9F%E6%A2%B0%E5%AD%A6%E7%BF%92-%E2%80%95scikit-learn%E3%81%A7%E5%AD%A6%E3%81%B6%E7%89%B9%E5%BE%B4%E9%87%8F%E3%82%A8%E3%83%B3%E3%82%B8%E3%83%8B%E3%82%A2%E3%83%AA%E3%83%B3%E3%82%B0%E3%81%A8%E6%A9%9F%E6%A2%B0%E5%AD%A6%E7%BF%92%E3%81%AE%E5%9F%BA%E7%A4%8E-Andreas-C-Muller/dp/4873117984)まとめ

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

## [機械学習入門 ボルツマン機械学習から深層学習まで](https://www.amazon.co.jp/gp/product/4274219984/ref=ppx_yo_dt_b_asin_title_o08_s00?ie=UTF8&psc=1)まとめ
