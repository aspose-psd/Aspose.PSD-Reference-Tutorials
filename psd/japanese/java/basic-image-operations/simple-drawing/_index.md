---
date: 2026-06-13
description: Aspose.PSD for Java を使用して PSD ファイルに矩形を描く方法を学びます。このガイドでは、ステップバイステップのコード、レイヤーの追加、サーバーサイドの画像処理、形状の描画を紹介します。
keywords:
- how to draw rectangle
- how to create psd
- java graphics draw rectangle
- server side image processing
- add layer to psd
linktitle: シンプルな描画を実行
schemas:
- author: Aspose
  dateModified: '2026-06-13'
  description: Learn how to draw rectangle in PSD files using Aspose.PSD for Java.
    This guide shows step‑by‑step code, adding layers, server‑side image processing
    and shape drawing.
  headline: How to Draw Rectangle in PSD with Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: Yes, the `Graphics` class also supports drawing ellipses, lines, and custom
      paths via the `drawPath` method.
    question: Can I draw other shapes besides rectangles?
  - answer: Absolutely; you can use `SolidBrush` with an ARGB color to include alpha
      transparency, enabling semi‑transparent overlays.
    question: Does Aspose.PSD support transparency in drawn shapes?
  - answer: Yes, each `Layer` object has a `setOpacity` method that accepts a value
      from 0 to 255, allowing fine‑grained control over layer transparency.
    question: Is it possible to edit the opacity of a layer?
  - answer: Use `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` before
      manipulating layers. The loaded image retains all original layers and masks.
    question: How do I load an existing PSD file instead of creating a new one?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java を使用して PSD に矩形を描く方法
url: /ja/java/basic-image-operations/simple-drawing/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSDで矩形を描画する方法（Aspose.PSD for Java）

## はじめに

このチュートリアルでは、純粋な Java の Aspose.PSD ライブラリを使用して、Photoshop PSD ファイル内に **矩形を描画する** 方法を学びます。サーバーサイドのアセットパイプラインを構築したり、サムネイル作成を自動化したり、既存のデザインに動的なグラフィックを追加したりする場合でも、以下の手順で完全な本番環境向けソリューションを提供します。新しい PSD ドキュメントの作成、レイヤーの追加、背景のクリア、そして赤と青の矩形の描画を、Photoshop を起動せずに行う方法をカバーします。

## クイック回答
- **PSD ファイルを作成するための主要クラスは何ですか？** `PsdImage`
- **レイヤーの背景色をクリアするメソッドはどれですか？** `Graphics.clear(Color)`
- **赤い矩形を描くにはどうすればよいですか？** `graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(...))`
- **開発にライセンスは必要ですか？** テストには無料トライアルが利用でき、製品版にはライセンスが必要です。
- **同じ API で既存の PSD ファイルを操作できますか？** はい、Aspose.PSD は完全な PSD 編集をサポートしています。

## PSDファイルで赤い矩形を描くとは何ですか？

赤い矩形を描くとは、`Graphics` オブジェクトを使用して、特定の PSD 画像レイヤー上に赤色で塗りつぶすか輪郭を描く矩形形状を描画することです。この操作は、領域のハイライト、プレースホルダーの作成、またはプログラム的にシンプルなグラフィックを追加する際に一般的に使用されます。

## なぜ Aspose.PSD for Java を使用して PSD ファイルを操作するのか？

Aspose.PSD for Java は **50 以上の入力および出力形式** をサポートし、ファイル全体をメモリに読み込まずに数百ページに及ぶ PSD を処理でき、Java 8 以降をサポートする任意のプラットフォームで動作します。サーバーサイドの画像処理エンジンにより Photoshop が不要になり、ライセンスコストを削減し、**10 GB** の画像データを 1 時間あたりに処理できる自動化ワークフローを、低スペックの VM でも実現できます。

## 前提条件

- Java Development Kit (JDK) 8 以降がマシンにインストールされていること。  
- Aspose.PSD for Java ライブラリ。以下の [Aspose.PSD for Java Documentation](https://reference.aspose.com/psd/java/) からダウンロードできます。

## パッケージのインポート

`import` 文は必要なクラスをスコープに持ち込み、PSD 画像、レイヤー、カラー、グラフィックを操作できるようにします。

`PsdImage` クラスは Aspose.PSD のトップレベルオブジェクトで、メモリ内の単一 PSD ファイルを表します。  
`Graphics` は線、矩形、楕円などの描画プリミティブを提供します。  
`Color` と `Pen` はストロークカラーと太さを指定するために使用します。  
`Layer` クラスは PSD ドキュメント内の個別画像レイヤーを表します。  
`Rectangle` クラスは描画操作で使用する矩形領域の位置とサイズを定義します。  
`SolidBrush` クラスは形状を単色で塗りつぶします。

## PSD ドキュメントを作成する最初のステップは何ですか？

`PsdImage` をピクセル単位のキャンバス幅と高さでインスタンス化すると、空の PSD ファイル構造が作成されます。初期レイヤーや背景を設定した後、`save` メソッドにファイルパスを渡してディスクに書き出します。これにより、後続の編集操作のための画像が準備されます。

## 手順 1: 新しいドキュメントの作成

まず、目的のキャンバスサイズで新しい PSD ドキュメントを作成します。このドキュメントが、描画対象となるレイヤーをホストします。

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```

## PSD 画像に新しい空白レイヤーを追加するにはどうすればよいですか？

まず、親 `PsdImage` と同じ幅と高さを持つ新しい `Layer` インスタンスを作成します。次に、`add` メソッドでこのレイヤーを画像の `Layers` コレクションに追加します。レイヤーが画像に含まれたら、その `Graphics` オブジェクトを取得して描画操作を行います。このステップがないと描画は表示されません。

## 手順 2: レイヤーの追加

画像の全幅・全高さにわたる新しい空白レイヤーを追加します。レイヤーは描画操作を分離するために不可欠です。

```java
//ExStart:CreateDocument
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
int width = 100;
int height = 100;

PsdImage image = new PsdImage(width, height);
//ExEnd:CreateDocument
```

## レイヤーの背景色をクリアする目的は何ですか？

`Graphics.clear` に特定の `Color` を渡すと、レイヤー全体がその色で塗りつぶされ、ピクセルデータがリセットされます。これにより、以前のコンテンツが除去され、レイヤーが既知の背景から開始するため、Photoshop で後から開いたり編集したりした際に予期しない透明度や色のブレンドが発生しません。

## 手順 3: 図形の描画

`Graphics` クラスを使用してレイヤーのピクセルデータを操作します。以下は、背景をクリアし、異なる色の矩形を描く 3 つの例です。

### レイヤーの色をクリア (背景を黄色に設定)

```java
//ExStart:AddLayer
Layer layer = new Layer();
layer.setBottom(height);
layer.setRight(width);
image.addLayer(layer);
//ExEnd:AddLayer
```

### 赤い矩形を描く (主な焦点)

```java
//ExStart:DrawRectangleYellow
Graphics graphic = new Graphics(layer);
graphic.clear(Color.getYellow());
//ExEnd:DrawRectangleYellow
```

### 青い矩形を描く (追加例)

```java
//ExStart:DrawRedRectangle
graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));
//ExEnd:DrawRedRectangle
```

## 編集した PSD ファイルをディスクに保存するにはどうすればよいですか？

`PsdImage` オブジェクトの `save` メソッドに完全なファイルパスを渡し、必要に応じて画像形式（デフォルトは PSD）を指定します。これにより、すべてのレイヤー、マスク、描画コマンドが Photoshop 仕様に準拠した単一の PSD ファイルに書き込まれ、警告なしで開くことができます。

## 手順 4: 変更の保存

最後に、変更された PSD 画像をディスクに書き出します。ファイルには新しいレイヤーと描画された形状が含まれます。

```java
//ExStart:DrawBlueRectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));
//ExEnd:DrawBlueRectangle
```

## よくある問題と解決策

- **描画後にレイヤーが表示されない:** `Graphics` オブジェクトを作成する **前に** レイヤーが画像に追加されていることを確認してください。描画対象は有効なレイヤーに紐付いている必要があります。
- **色が正しく表示されない:** `Color.getRed()`（または `Color.getBlue()`）を使用しているか確認し、0‑255 の範囲を超えるカスタム RGB 値を構築していないかチェックしてください。
- **ファイルが保存されない:** `outputDir` パスが存在し、アプリケーションに書き込み権限があることを確認してください。Linux 環境ではフォルダー所有権の調整や `Files.createDirectories` の使用が必要になる場合があります。
- **大容量ファイルでパフォーマンスが低下する:** `PsdImage` の `setLoadOptions` を使用して必要なチャンネルだけをロードし、200 MB を超える PSD のメモリ消費を削減してください。

## よくある質問

**Q1: Aspose.PSD for Java を使用して既存の PSD ファイルを操作できますか？**  
A1: はい、Aspose.PSD for Java はレイヤーの並び替え、マスク調整、ベクタ描画など、既存 PSD の編集と操作に関する豊富な機能を提供します。

**Q2: Aspose.PSD for Java のサポートはどこで受けられますか？**  
A2: コミュニティ主導の支援と公式 Aspose の回答は、[Aspose.PSD for Java Forum](https://forum.aspose.com/c/psd/34) で確認できます。

**Q3: Aspose.PSD for Java の無料トライアルはありますか？**  
A3: はい、[here](https://releases.aspose.com/) から無料トライアル版にアクセスできます。トライアルはすべての機能を含みますが、保存ファイルに透かしが追加されます。

**Q4: Aspose.PSD for Java のライセンスはどこで購入できますか？**  
A4: [Aspose.PSD Purchase Page](https://purchase.aspose.com/buy) からライセンスを購入できます。永続ライセンス、サブスクリプション、サイトライセンスなどのオプションがあります。

**Q5: Aspose.PSD for Java の一時ライセンスは利用可能ですか？**  
A5: はい、[here](https://purchase.aspose.com/temporary-license/) から一時ライセンスを取得できます。

## 追加のよくある質問

**Q: 矩形以外の形状も描画できますか？**  
A: はい、`Graphics` クラスは楕円、直線、`drawPath` メソッドによるカスタムパスの描画もサポートしています。

**Q: 描画した形状で透明度はサポートされていますか？**  
A: 完全にサポートしています。`SolidBrush` に ARGB カラーを使用すればアルファ透明度を含めることができ、半透明オーバーレイを実現できます。

**Q: レイヤーの不透明度を編集できますか？**  
A: はい、各 `Layer` オブジェクトには 0 から 255 の範囲で不透明度を設定できる `setOpacity` メソッドがあります。

**Q: 新規作成ではなく既存の PSD ファイルを読み込むには？**  
A: レイヤー操作の前に `PsdImage image = (PsdImage)Image.load("path/to/file.psd");` を使用してください。読み込んだ画像は元のすべてのレイヤーとマスクを保持します。

## 結論

これで **矩形を描画する** 方法と Aspose.PSD for Java を使用した PSD ファイル内のレイヤー操作を習得しました。ドキュメントの作成、レイヤーの追加、背景のクリア、`Graphics` API を用いた描画により、サーバーサイドで無数のグラフィックデザインタスクを自動化できます。さまざまなペンやブラシ、レイヤー効果を試して、フル機能の画像生成パイプラインへと拡張してください。

```java
//ExStart:SaveChanges
image.save(outPsdFilePath);
//ExEnd:SaveChanges
```

{{< blocks/products/products-backtop-button >}}

## 関連チュートリアル

- [Javaで図形を描く方法 – 基本画像操作](/psd/java/basic-image-operations/)
- [Aspose.PSD を使用したシンプルなリサイズ – Java 画像操作ライブラリ](/psd/java/basic-image-operations/simple-resizing/)
- [Aspose.PSD for Java で矩形による画像の切り抜き](/psd/java/image-editing/crop-image-by-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

---

**最終更新日:** 2026-06-13  
**テスト環境:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**作者:** Aspose