# 第9章 TensorFlow を立ち上げる

## jupyter ファイルの構成
- test_TensorFlow.ipynb
  - 9.1 ~ 9.4 のコード
  - TensorFlow の簡単な使い方を試す
- linear_regression.ipynb
  - 9.5 のコード
  - NumPy ではなく TensorFlow で行列演算を使ってみる
- gradient_descent.ipynb

## 9.1 インストール
```bash
$ pip install tensorflow
$ pip install tensorflow-gpu
```

## 9.2 最初のグラフの作成とセッション内での実行
TensorFlow のプログラムは以下の2段階に分割される
- Construction Phase (構築フェーズ)    
ここで、機械学習モデルとそれを訓練するために必要な計算グラフを構築する
- Execution Phase (実行フェーズ)    
上で構築した計算グラフを実行し、モデルの訓練を行う

## 9.3 グラフの管理
作成したノードは自動的にデフォルトグラフに入るが、tf.Graph() を使って新しいグラフを定義できる

## 9.4 ノードの値のライフサイクル
グラフの実行ごとにノードの値は捨てられるが、変数の値は複数のグラフに跨ってセッションが保持する
（詳細は第12章で触れる）

## 9.5 TensorFlow による線形回帰
TensorFlow では NumPy の ndarray のような多次元配列テンソル（tensor）を使って行列演算を行う    
ここでは、線形回帰を例として行列演算を試している

## 9.6 勾配降下法の実装
