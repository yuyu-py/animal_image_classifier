# 動物画像分類システム - CNN実装プロジェクト

## プロジェクト内容

畳み込みニューラルネットワーク（CNN）を使用した猫と犬の画像分類システムです。TensorFlow Datasetsから取得した高品質な動物画像データを用いて、深層学習による画像認識モデルを構築しました。TensorFlowによるCNN実装とコンピュータビジョン技術を学習することを目的として開発しました。

## プロジェクト構成

```
animal_image_classifier/
├── notebooks/
│   └── animal_classifier.ipynb    # メイン分析ノートブック
├── image_datasets/
│   ├── training_images/           # 訓練用画像データ
│   ├── test_images/              # テスト用画像データ
│   └── prediction_samples/       # 予測用サンプル画像
├── requirements.txt              # 依存関係管理
├── README.md                     # プロジェクト説明書
└── .gitignore                   # Git除外ファイル設定
```

## 必要要件/開発環境

- **Python 3.8以上**
- **VSCode** (開発環境)
- **Git** (バージョン管理)

### 使用ライブラリ

- **TensorFlow 2.16.2** ディープラーニングフレームワーク
- **NumPy 1.26.4** 数値計算ライブラリ
- **TensorFlow Datasets 4.9.4** 公開データセットライブラリ
- **scikit-learn 1.7.0** 機械学習ライブラリ
- **matplotlib 3.10.3** データ可視化ライブラリ
- **Pillow 11.2.1** 画像処理ライブラリ
- **jupyter 1.1.1** ノートブック実行環境

## 機能

- **画像データ前処理** データ拡張と特徴量スケーリング
- **CNN構築** TensorFlowによる畳み込みニューラルネットワーク構築
- **モデル学習** Adam最適化とバイナリクロスエントロピー損失による学習
- **画像分類** 猫と犬の二値分類予測
- **性能評価** 訓練・テストデータでの精度評価
- **単一画像予測** 新しい画像での分類予測

## 実行方法

### 1. リポジトリのクローン

```bash
git clone https://github.com/yourusername/animal_image_classifier.git
cd animal_image_classifier
```

### 2. 仮想環境の作成・アクティベート

**Windows**

```bash
python -m venv dl_env
dl_env\Scripts\activate
```

**macOS**

```bash
python3 -m venv dl_env
source dl_env/bin/activate
```

### 3. 依存関係のインストール

```bash
pip install -r requirements.txt
```

### 4. Jupyter Notebookの起動

```bash
jupyter notebook
```

### 5. 分析の実行

`notebooks/animal_classifier.ipynb`を開き、セルを順番に実行してください。

## データセットについて

* **データソース** TensorFlow Datasets - cats_vs_dogs
* **訓練データ** 猫8,000枚、犬8,000枚
* **テストデータ** 猫2,000枚、犬2,000枚
* **画像サイズ** 64×64ピクセル（RGB 3チャンネル）
* **データ拡張** シアー変換、ズーム変換、水平反転

## モデル詳細

* **アーキテクチャ** 入力層 → 畳み込み層×2 → プーリング層×2 → Flatten層 → 全結合層 → 出力層
* **畳み込み層** 32フィルター、3×3カーネル
* **プーリング層** 2×2最大プーリング
* **全結合層** 128ニューロン
* **活性化関数** 隠れ層：ReLU、出力層：Sigmoid
* **最適化アルゴリズム** Adam
* **損失関数** バイナリクロスエントロピー

## 学習内容

* TensorFlowによるCNN実装
* 画像データ前処理テクニック（正規化、データ拡張）
* 畳み込みニューラルネットワークの構築
* 二値分類問題への深層学習の適用
* コンピュータビジョンとパターン認識
* モデル評価と性能分析

## 開発者

YuYu
