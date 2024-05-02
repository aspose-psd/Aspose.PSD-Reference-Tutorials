---
title: Aspose.PSD for Java を使用して簡単な描画を実行する
linktitle: 簡単な描画を実行する
second_title: Aspose.PSD Java API
description: Aspose.PSD for Java を使用して PSD ファイルに図形を描画する方法を学びます。このステップバイステップのガイドでは、コード例を使用してレイヤーの作成、追加、描画について説明します。
type: docs
weight: 10
url: /ja/java/basic-image-operations/simple-drawing/
---
## 導入

Aspose.PSD for Java を使用して簡単な描画を実行するためのこのステップバイステップ ガイドへようこそ。このチュートリアルでは、新しい PSD ドキュメントの作成、レイヤーの追加、さまざまな色での図形の描画の基本を学びます。 Aspose.PSD for Java は、PSD ファイルをプログラムで操作できる強力なライブラリであり、グラフィック デザイン タスクに広範な機能を提供します。

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。

- Java Development Kit (JDK) がマシンにインストールされています。
-  Java ライブラリの Aspose.PSD。からダウンロードできます。[Java 用 Aspose.PSD ドキュメント](https://reference.aspose.com/psd/java/).

## パッケージのインポート

まず、必要なパッケージを Java プロジェクトにインポートします。 Java ファイルの先頭に次のコードを含めます。

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## ステップ 1: 新しいドキュメントを作成する

指定された幅と高さで新しい PSD ドキュメントを作成することから始めましょう。

```java
//ExStart:ドキュメントの作成
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:ドキュメントの作成
```

## ステップ 2: レイヤーを追加する

次に、引数なしのコンストラクターを使用してドキュメントにレイヤーを追加しましょう。

```java
//ExStart:レイヤーの追加
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

## ステップ 3: 形状を描く

このステップでは、Graphics クラスを使用して、作成したレイヤー上に図形を描画します。

### 黄色で長方形を描く

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### 赤い長方形を描く

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

### 青い長方形を描く

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## ステップ 4: 変更を保存する

最後に、ロードした PSD ファイルのコピーを変更を含めて保存します。

```java
//ExStart:変更の保存
image.save(outPsdFilePath);
//ExEnd:変更の保存
```

## 結論

おめでとう！ Aspose.PSD for Java を使用して簡単な描画を正常に実行できました。このチュートリアルでは、新しいドキュメントの作成、レイヤーの追加、さまざまな色での四角形の描画について説明しました。グラフィック デザインのニーズに合わせて、ライブラリが提供するさらに高度な機能を自由に探索してください。

## よくある質問

### Q1: Aspose.PSD for Java を使用して既存の PSD ファイルを操作できますか?

A1: はい、Aspose.PSD for Java は、既存の PSD ファイルを編集および操作するための広範な機能を提供します。

### Q2: Java 用 Aspose.PSD のサポートはどこで見つけられますか?

 A2: にアクセスできます。[Java フォーラム用 Aspose.PSD](https://forum.aspose.com/c/psd/34)サポート関連の質問については、

### Q3: Aspose.PSD for Java の無料トライアルはありますか?

 A3: はい、無料試用版にアクセスできます。[ここ](https://releases.aspose.com/).

### Q4: Aspose.PSD for Java のライセンスはどのように購入できますか?

 A4: ライセンスは以下から購入できます。[Aspose.PSD 購入ページ](https://purchase.aspose.com/buy).

### Q5: Aspose.PSD for Java の一時ライセンスは利用できますか?

A5: はい、次のサイトから一時ライセンスを取得できます。[ここ](https://purchase.aspose.com/temporary-license/).