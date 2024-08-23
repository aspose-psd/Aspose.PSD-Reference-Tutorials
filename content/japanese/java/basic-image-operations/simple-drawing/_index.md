---
title: Aspose.PSD for Java で簡単な描画を実行する
linktitle: 簡単な描画を実行する
second_title: Aspose.PSD Java API
description: Aspose.PSD for Java を使用して PSD ファイルに図形を描画する方法を学びます。このステップ バイ ステップ ガイドでは、コード例を使用して、レイヤーの作成、追加、描画について説明します。
type: docs
weight: 10
url: /ja/java/basic-image-operations/simple-drawing/
---
## 導入

Aspose.PSD for Java を使用して簡単な描画を実行するためのステップバイステップ ガイドへようこそ。このチュートリアルでは、新しい PSD ドキュメントの作成、レイヤーの追加、さまざまな色での図形の描画の基本について説明します。Aspose.PSD for Java は、PSD ファイルをプログラムで操作できる強力なライブラリであり、グラフィック デザイン タスクに幅広い機能を提供します。

## 前提条件

チュートリアルに進む前に、次の前提条件が満たされていることを確認してください。

- マシンに Java 開発キット (JDK) がインストールされています。
- Aspose.PSD for Javaライブラリ。ダウンロードは以下から行えます。[Aspose.PSD for Java ドキュメント](https://reference.aspose.com/psd/java/).

## パッケージのインポート

まず、必要なパッケージを Java プロジェクトにインポートします。Java ファイルの先頭に次のコードを含めます。

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## ステップ1: 新しいドキュメントを作成する

まず、幅と高さを指定した新しい PSD ドキュメントを作成しましょう。

```java
//ExStart:ドキュメントの作成
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:ドキュメントの作成
```

## ステップ2: レイヤーを追加する

次に、引数なしのコンストラクターを使用してドキュメントにレイヤーを追加してみましょう。

```java
//ExStart:レイヤーの追加
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:レイヤーの追加
```

## ステップ3: 図形を描く

このステップでは、Graphics クラスを使用して、作成したレイヤーに図形を描画します。

### 黄色の長方形を描く

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### 赤い四角形を描く

```java
//ExStart:赤い四角形を描画
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:赤い四角形を描画
```

### 青い長方形を描く

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## ステップ4: 変更を保存する

最後に、変更を含めて読み込んだ PSD ファイルのコピーを保存します。

```java
//ExStart:変更を保存
image.save(outPsdFilePath);
//ExEnd:変更を保存
```

## 結論

おめでとうございます。Aspose.PSD for Java を使用して簡単な描画を実行できました。このチュートリアルでは、新しいドキュメントの作成、レイヤーの追加、さまざまな色での四角形の描画について説明しました。グラフィック デザインのニーズに合わせて、ライブラリが提供するより高度な機能を自由に探索してください。

## よくある質問

### Q1: Aspose.PSD for Java を使用して既存の PSD ファイルを操作できますか?

A1: はい、Aspose.PSD for Java は、既存の PSD ファイルを編集および操作するための広範な機能を提供します。

### Q2: Aspose.PSD for Java のサポートはどこで見つかりますか?

 A2:[Aspose.PSD for Java フォーラム](https://forum.aspose.com/c/psd/34)サポート関連のお問い合わせについては、

### Q3: Aspose.PSD for Java の無料試用版はありますか?

A3: はい、無料試用版をご利用いただけます[ここ](https://releases.aspose.com/).

### Q4: Aspose.PSD for Java のライセンスはどうすれば購入できますか?

 A4: ライセンスは[Aspose.PSD 購入ページ](https://purchase.aspose.com/buy).

### Q5: Aspose.PSD for Java の一時ライセンスは利用できますか?

A5: はい、一時ライセンスを取得することができます。[ここ](https://purchase.aspose.com/temporary-license/).