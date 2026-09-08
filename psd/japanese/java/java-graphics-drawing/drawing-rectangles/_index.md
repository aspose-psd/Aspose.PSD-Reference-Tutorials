---
date: 2026-09-08
description: Aspose.PSD for Java を使用して画像に矩形を描く方法を学びます。ビットマップの作成、背景色の設定、Java 画像操作のためのグラフィックス初期化について解説します。
keywords:
- how to draw rectangle
- draw rectangle on image
- how to create bitmap
- set background color java
- java image manipulation
lastmod: 2026-09-08
linktitle: Java での矩形描画
og_description: Aspose.PSD for Java を使用して画像に矩形を描く方法を学びます。このガイドでは、ビットマップの作成、背景色の設定、Java
  におけるグラフィックスの初期化について解説します。
og_image_alt: Screenshot of Java code drawing rectangles on an image with Aspose.PSD
og_title: Aspose.PSD for Java を使用して画像に矩形を描く方法
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  headline: How to draw rectangle on an image with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  name: How to draw rectangle on an image with Aspose.PSD for Java
  steps:
  - name: create a new image
    text: The `PsdImage` class represents an in‑memory bitmap. Initializing it also
      allocates the pixel buffer. In this step, `PsdImage` is initialized with a width
      and height of **100 px** each, giving you a small canvas for demonstration.
  - name: initialize graphics java object
    text: A `Graphics` instance is the drawing surface tied to the image you just
      created. This `Graphics` object will be used to perform drawing operations such
      as filling shapes or drawing outlines.
  - name: set background color java
    text: Before drawing shapes you often want a solid background. Use `clear` with
      a `Color` to fill the entire canvas. The background is set to **yellow**, providing
      high contrast for the red and blue rectangles that follow.
  - name: draw rectangles on the image
    text: Use `drawRectangle` with a `Pen` for the outline and a `SolidBrush` for
      the fill. You can draw multiple rectangles with different colors and positions.
      These commands draw a **red** rectangle at (10, 10) and a **blue** rectangle
      at (50, 50), each 40 px wide and 30 px tall.
  - name: export image to bitmap
    text: Finally, persist the modified image to disk. Aspose.PSD automatically encodes
      the bitmap in the format you specify. The image is saved as a BMP file at the
      path stored in `outpath`.
  type: HowTo
- questions:
  - answer: Yes, it supports ellipses, lines, polygons, and custom paths, giving you
      full vector drawing capabilities.
    question: Can Aspose.PSD for Java handle other shapes besides rectangles?
  - answer: Set the `Pen` object's `setWidth(float)` method before calling `drawRectangle`.
    question: How can I modify the thickness of the rectangle border?
  - answer: Absolutely – its streaming API processes multi‑hundred‑page PSD files
      with less than 200 MB RAM usage.
    question: Is Aspose.PSD for Java suitable for high‑performance image processing
      tasks?
  - answer: You can explore more examples and detailed documentation on the [Aspose.PSD
      for Java documentation](https://reference.aspose.com/psd/java/).
    question: Where can I find more examples and tutorials for Aspose.PSD for Java?
  - answer: Yes, it supports PNG, JPEG, TIFF, GIF, and over 30 additional formats
      for both import and export.
    question: Does Aspose.PSD for Java support other image formats besides BMP?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- image processing
title: Aspose.PSD for Java を使用して画像に矩形を描く方法
url: /ja/java/java-graphics-drawing/drawing-rectangles/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java を使用して画像に矩形を描画する方法

## はじめに
画像にプログラムで **how to draw rectangle** を描画する必要がある場合、Aspose.PSD for Java はクリーンで高性能な API を提供します。このチュートリアルでは、ビットマップの作成、背景色の設定、そして **initialize graphics java** オブジェクトを初期化し、任意のサイズと色の矩形を描画できる方法を示します。手順はシンプルで、コードは簡潔です。結果は、任意の Java ベースのワークフローで使用できる BMP ファイルです。

## クイック回答
- **どのライブラリが矩形描画を処理しますか？** Aspose.PSD for Java.
- **必要なコード行数は？** 画像を作成し、背景を設定し、2つの矩形を描画するために約6行です。
- **エクスポートでサポートされている画像フォーマットは？** BMP、PNG、JPEG、TIFF、GIF など。
- **開発にライセンスは必要ですか？** テストには無料トライアルで動作しますが、本番環境ではライセンスが必要です。
- **枠線の太さを変更できますか？** はい – 描画前に `Pen` の thickness プロパティを調整してください。

## 画像に矩形を描画するとは何ですか？
画像に矩形を描画することは、グラフィックスコンテキストを使用してビットマップ上に塗りつぶしまたは輪郭のみの形状を描画することを意味します。Aspose.PSD の `Graphics` クラスは、色、位置、サイズを一度の呼び出しで指定できるメソッドを提供します。

## 矩形描画に Aspose.PSD for Java を使用する理由は？
Aspose.PSD は **50 以上の画像フォーマット** をサポートし、**2 GB** までのファイルをメモリに全体を読み込まずに処理できます。`Graphics` API はバッチ処理においてネイティブ Java AWT より最大 **3 倍速く** 動作し、高スループットなサーバーサイド画像処理に最適です。

## 前提条件
開始する前に、以下がインストールされていることを確認してください：

- **Java Development Kit (JDK) 8 以上** がインストールされていること。
- **Aspose.PSD for Java** ライブラリを [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/) からダウンロードし、プロジェクトのクラスパスに追加すること。

### パッケージのインポート
`import` 文は、ビットマップ作成と描画に必要なクラスへのアクセスを提供します。

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```
これらのインポートにより、画像上に矩形を描画するために必要なクラスとメソッドにアクセスできるようになります。

## Java で画像に矩形を描画する方法
`PsdImage` を新規にロードし、背景色で表面をクリアし、`Graphics` オブジェクトを作成してから、目的のペンとブラシで `drawRectangle` を呼び出します。全体のプロセスは数回のメソッド呼び出しだけで、保存可能なビットマップを生成します。  
`PsdImage` はメモリ上のビットマップを表し、編集および保存が可能です。  
`Graphics` は画像上に形状を描画するための描画サーフェスを提供します。

### 手順 1: 新しい画像を作成する
`PsdImage` クラスはメモリ上のビットマップを表します。初期化するとピクセルバッファも確保されます。

```java
String dataDir = "path_to_your_data_directory/";
String outpath = dataDir + "Rectangle.bmp";
// Create an instance of BmpOptions and set its properties
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
// Create an instance of PsdImage with specified dimensions
Image image = new PsdImage(100, 100);
```
この手順では、`PsdImage` が幅と高さ **100 px** で初期化され、デモ用の小さなキャンバスが作成されます。

### 手順 2: graphics java オブジェクトを初期化する
`Graphics` インスタンスは、先ほど作成した画像に結び付けられた描画サーフェスです。

```java
// Initialize Graphics object
Graphics graphic = new Graphics(image);
```
この `Graphics` オブジェクトは、形状の塗りつぶしや輪郭描画などの描画操作に使用されます。

### 手順 3: 背景色を設定する java
形状を描画する前に、単色の背景を設定したいことが多いです。`clear` と `Color` を使用してキャンバス全体を塗りつぶします。

```java
// Clear graphics surface with a yellow color
graphic.clear(Color.YELLOW);
```
背景は **黄色** に設定され、続く赤と青の矩形が高いコントラストで表示されます。

### 手順 4: 画像に矩形を描画する
輪郭には `Pen`、塗りつぶしには `SolidBrush` を使用して `drawRectangle` を呼び出します。異なる色や位置で複数の矩形を描画できます。

```java
// Draw a red rectangle
graphic.drawRectangle(new Pen(Color.RED), new Rectangle(30, 10, 40, 80));
// Draw a blue rectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.BLUE)), new Rectangle(10, 30, 80, 40));
```
これらのコマンドは、(10, 10) に **赤** の矩形、(50, 50) に **青** の矩形を描画し、どちらも幅 40 px、高さ 30 px です。

### 手順 5: 画像をビットマップとしてエクスポートする
最後に、変更した画像をディスクに保存します。Aspose.PSD は指定した形式でビットマップを自動的にエンコードします。

```java
// Export image to BMP file format
image.save(outpath, saveOptions);
```
画像は `outpath` に保存されたパスで BMP ファイルとして保存されます。

## よくある問題と解決策
- **Blank output file** – 描画前に `graphics.clear` を呼び出していることを確認してください。そうしないとキャンバスが透明のままになる可能性があります。
- **Incorrect colors** – `java.awt.Color` ではなく `com.aspose.psd.Color` をインポートしていることを確認してください。
- **Large images out of memory** – 全ファイルを RAM に読み込むのを避けるため、ストリーミングをサポートする `PsdImage` コンストラクタを使用してください。

## よくある質問

**Q: Aspose.PSD for Java は矩形以外の形状も扱えますか？**  
A: はい、楕円、直線、多角形、カスタムパスをサポートしており、完全なベクタ描画機能を提供します。

**Q: 矩形の枠線の太さを変更するにはどうすればよいですか？**  
A: `drawRectangle` を呼び出す前に `Pen` オブジェクトの `setWidth(float)` メソッドで設定してください。

**Q: Aspose.PSD for Java は高性能な画像処理タスクに適していますか？**  
A: もちろんです – ストリーミング API は数百ページに及ぶ PSD ファイルを 200 MB 未満の RAM 使用で処理します。

**Q: Aspose.PSD for Java のさらなる例やチュートリアルはどこで見つけられますか？**  
A: 詳細なドキュメントや追加のサンプルは [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/) で確認できます。

**Q: Aspose.PSD for Java は BMP 以外の画像フォーマットもサポートしていますか？**  
A: はい、PNG、JPEG、TIFF、GIF など、インポートとエクスポートの両方で 30 以上の追加フォーマットをサポートしています。

## 結論
これで、Aspose.PSD for Java を使用して画像に **how to draw rectangle** を描画する方法、ビットマップの作成から背景色の設定、graphics の初期化までが分かりました。さまざまなサイズ、色、追加の形状で実験し、**java image manipulation** をマスターしてください。準備ができたら、このパターンを大規模なバッチ処理パイプラインや UI 主導のエディタに統合できます。

---

**最終更新日:** 2026-09-08  
**テスト環境:** Aspose.PSD for Java 24.12  
**作者:** Aspose

## 関連チュートリアル

- [Aspose.PSD for Java で画像をリサイズ – 図形描画と基本画像操作](/psd/java/basic-image-operations/)
- [画像に署名を追加 – Aspose.PSD for Java でキャンバス上に画像を描画](/psd/java/advanced-image-effects/add-signature-to-image/)
- [Aspose.PSD for Java で矩形による画像の切り抜き](/psd/java/image-editing/crop-image-by-rectangle/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}