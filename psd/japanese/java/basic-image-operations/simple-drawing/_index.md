---
date: 2025-12-27
description: Aspose.PSD for Java を使用して、PSD ファイルに赤い長方形やその他の図形を描く方法を学びます。このステップバイステップガイドでは、ドキュメントの作成、レイヤーの追加、コード例による描画について説明します。
linktitle: Perform Simple Drawing
second_title: Aspose.PSD Java API
title: Aspose.PSD for Javaで赤い矩形を描く
url: /ja/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Javaで赤い長方形を描く

## はじめに

このステップバイステップガイドへようこそ！Aspose.PSD for Java を使用して **赤い長方形を描く** 方法をご紹介します。本チュートリアルでは、PSD ドキュメントの作成、レイヤーの追加、カスタムカラーでの図形描画の手順を解説します。グラフィック資産の自動化やデザインツールのバックエンド構築に役立つ基本的な構成要素が学べます。

## クイック回答
- **PSD ファイルを作成するための主要クラスは？** `PsdImage`
- **レイヤーの背景色をクリアするメソッドは？** `Graphics.clear(Color)`
- **赤い長方形を描くには？** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **開発時にライセンスは必要ですか？** テストには無料トライアルで動作しますが、本番環境ではライセンスが必要です。
- **同じ API で既存の PSD ファイルを操作できますか？** はい、Aspose.PSD は完全な PSD 編集をサポートしています。

## PSD ファイルで赤い長方形を描くとは？
赤い長方形を描くとは、`Graphics` オブジェクトを使用して、PSD 画像の特定レイヤー上に赤色で塗りつぶすか輪郭だけの長方形形状を描画することです。この操作は、領域のハイライト、プレースホルダーの作成、またはシンプルなグラフィックをプログラムで追加する際に一般的に使用されます。

## なぜ Aspose.PSD for Java を使って PSD ファイルを操作するのか？
Aspose.PSD は純粋な Java API を提供し、Photoshop をインストールせずに PSD ファイルの読み取り、編集、書き込みが可能です。レイヤー管理、カラー操作、ベクタ描画をサポートしており、サーバーサイドの画像処理、自動資産パイプライン、カスタムグラフィック生成に最適です。

## 前提条件

- お使いのマシンに Java Development Kit (JDK) がインストールされていること。  
- Aspose.PSD for Java ライブラリ。以下のドキュメントからダウンロードできます: [Aspose.PSD for Java Documentation](https://reference.aspose.com/psd/java/)。

## パッケージのインポート

まず、Java プロジェクトに必要なクラスをインポートします。

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## 手順 1: 新しいドキュメントの作成

希望するキャンバスサイズで新しい PSD ドキュメントを作成します。このドキュメントが、図形を描画するレイヤーを保持します。

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## 手順 2: レイヤーの追加

画像の幅と高さ全体にわたる空白のレイヤーを新規作成します。レイヤーは描画操作を分離するために必須です。

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

## 手順 3: 図形の描画

`Graphics` クラスを使用してレイヤーのピクセルデータを操作します。以下の 3 つの例では、背景のクリアと異なる色での長方形描画を示します。

### レイヤーの色をクリア (背景を黄色に設定)

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### 赤い長方形の描画 (メインの焦点)

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

### 青い長方形の描画 (追加例)

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## 手順 4: 変更の保存

最後に、変更した PSD 画像をディスクに書き出します。ファイルには新しいレイヤーと描画された図形が含まれます。

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

## よくある問題と解決策

- **描画後にレイヤーが表示されない:** `Graphics` オブジェクトを作成する **前に** レイヤーが画像に追加されていることを確認してください。  
- **色が正しく表示されない:** `Color.getRed()` などの静的メソッドを使用しているか確認し、範囲外のカスタム RGB 値を使用していないかチェックしてください。  
- **ファイルが保存されない:** `outputDir` パスが存在し、アプリケーションに書き込み権限があることを確認してください。

## FAQ（よくある質問）

### Q1: Aspose.PSD for Java を使って既存の PSD ファイルを操作できますか？

A1: はい、Aspose.PSD for Java は既存の PSD ファイルを編集・操作するための豊富な機能を提供しています。

### Q2: Aspose.PSD for Java のサポートはどこで受けられますか？

A2: サポートに関する質問は [Aspose.PSD for Java Forum](https://forum.aspose.com/c/psd/34) で受け付けています。

### Q3: Aspose.PSD for Java の無料トライアルはありますか？

A3: はい、無料トライアル版は [here](https://releases.aspose.com/) から入手できます。

### Q4: Aspose.PSD for Java のライセンスはどこで購入できますか？

A4: ライセンスは [Aspose.PSD Purchase Page](https://purchase.aspose.com/buy) から購入できます。

### Q5: Aspose.PSD for Java の一時ライセンスはありますか？

A5: はい、一時ライセンスは [here](https://purchase.aspose.com/temporary-license/) から取得可能です。

## 追加の FAQ

**Q: 長方形以外の図形も描画できますか？**  
A: はい、`Graphics` クラスは楕円、直線、カスタムパスの描画もサポートしています。

**Q: 描画した図形で透明度を使用できますか？**  
A: もちろんです。`SolidBrush` に ARGB カラーを指定すればアルファ透明度を含めることができます。

**Q: レイヤーの不透明度を変更できますか？**  
A: はい、各 `Layer` オブジェクトには 0 から 255 の範囲で値を設定できる `setOpacity` メソッドがあります。

**Q: 新規作成ではなく既存の PSD ファイルを読み込むには？**  
A: レイヤーを操作する前に `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` を使用してください。

## 結論

これで Aspose.PSD for Java を使用して **赤い長方形** やその他の基本図形を PSD ファイルに描画する方法が学べました。ドキュメント作成、レイヤー追加、背景クリア、`Graphics` API での描画という手順を踏むことで、多くのグラフィックデザイン作業を自動化できます。さまざまなブラシ、レイヤー効果、ファイル形式を試して、さらに可能性を広げてみてください。

---

**最終更新日:** 2025-12-27  
**テスト環境:** Aspose.PSD for Java 24.12（執筆時点での最新バージョン）  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}