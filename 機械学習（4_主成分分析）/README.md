# Study-AI 実装演習レポート

## 機械学習（主成分分析）

### 1. 要点まとめ

- 多変量データの持つ構造をより少数個の指標に圧縮する。
- 分散が最大になるような低次元化を行う。
- 主成分の分散は共分散行列を用いて表現できる。
- 制約条件の元で分散の最大化はラグランジュ関数の微分にて最適解を求めることができる。
- ラグランジュ関数<br>
物理系の力学特性を表す関数であり、運動方程式に用いられる。
- 寄与率<br>
第ｋ主成分の分散の、全分散に対する割合。

### 2. 実装演習

UCIから提供されている乳がんデータセットを使用。
- 課題<br>
乳がん検査データを使用し、30次元データを2次元に次元圧縮する。
- 手順<br>
[(scikit-learnでの実行結果)](Exercises-1.ipynb)
- 予測結果<br>
2次主成分までの累積寄与率は 63.17% であり、概ねうまく判別できている。

### 3. 考察

- 医療の診断に使用することを考慮すると False Negative を抑えることが望ましい。
- 2次主成分までの累積寄与率は 63.17% であるが、これを80%まで高めるためには 5次主成分までの利用が必要となる。

### 4. 関連記事

https://noppoman.github.io/mathematical-theory-of-pca-ja/
https://www.kaggle.com/uciml/breast-cancer-wisconsin-data
https://ohke.hateblo.jp/entry/2017/08/11/230000
https://qiita.com/TsutomuNakamura/items/a1a6a02cb9bb0dcbb37f
