---
date: 2026-09-08
description: Aspose.PSD for Java を使用して Java でベジエ曲線を描く方法を学びます。ステップバイステップの手順、前提条件、コード不要の例に従ってください。
keywords:
- how to draw bezier
- how to use pen
- bezier curve example java
- java graphics draw curve
lastmod: 2026-09-08
linktitle: Java でベジエ曲線を描く
og_description: Aspose.PSD を使用して Java でベジエ曲線を描く方法。前提条件、ステップバイステップの描画手順、高解像度画像のためのヒントを網羅しています。
og_image_alt: Screenshot of a Java application rendering a Bezier curve with Aspose.PSD
og_title: Aspose.PSD ライブラリを使用した Java でのベジエ曲線の描き方
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to draw bezier curves in Java using Aspose.PSD for Java.
    Follow step‑by‑step instructions, prerequisites, and code‑free examples.
  headline: How to draw bezier curves in Java with Aspose.PSD library
  type: TechArticle
- description: Learn how to draw bezier curves in Java using Aspose.PSD for Java.
    Follow step‑by‑step instructions, prerequisites, and code‑free examples.
  name: How to draw bezier curves in Java with Aspose.PSD library
  steps:
  - name: create an image instance
    text: 'The `PsdImage` class is Aspose.PSD''s top‑level object that represents
      a single PSD file in memory. First, you need to create an instance of the `PsdImage`
      class, which represents a PSD image in memory. Explanation: - `PsdImage` is
      instantiated with width and height parameters (100 × 100 pixels in th'
  - name: initialize graphics context
    text: 'The `Graphics` class provides drawing capabilities on a `PsdImage`. Next,
      initialize an instance of the `Graphics` class to perform drawing operations
      on the image. Explanation: - `Graphics` object is initialized with the `image`
      instance, allowing drawing operations.'
  - name: clear the graphics surface
    text: 'The `clear()` method sets the background colour of the graphics surface.
      Clear the graphics surface using a specific background colour, here `Color.getYellow()`.
      Explanation: - `clear()` method sets the background colour of the graphics surface.'
  - name: initialize pen for drawing
    text: 'The `Pen` object defines stroke attributes such as colour and width. Set
      up a `Pen` object with properties like colour and width to define how the curve
      will be drawn. Explanation: - `Pen` is initialized with black colour and 3‑pixel
      width.'
  - name: define bezier curve parameters
    text: 'Control points determine the curvature. Specify the control points and
      end points for the Bezier curve. Explanation: - `startX`, `startY`: Starting
      point of the curve. - `controlX1`, `controlY1`: First control point. - `controlX2`,
      `controlY2`: Second control point. - `endX`, `endY`: Ending point of'
  - name: draw the bezier curve
    text: 'The `drawBezier()` method renders the curve using the supplied `Pen` and
      points. Use the `drawBezier()` method to draw the Bezier curve onto the image
      using the previously defined `Pen` and control points. Explanation: - `drawBezier()`
      method draws the curve with specified parameters using the `blac'
  - name: save the image
    text: Saving the image persists the drawing to disk. Save the drawn image to a
      BMP file format.
  type: HowTo
- questions:
  - answer: Yes, repeat the `drawBezier()` call inside a loop, updating the control
      points for each curve.
    question: Can I draw multiple Bezier curves in the same image?
  - answer: Modify the `Pen` object's colour property (`Color.getBlack()` in the example)
      before invoking `drawBezier()`.
    question: How can I change the colour of the Bezier curve?
  - answer: Yes, Aspose.PSD for Java supports high‑resolution images with efficient
      memory management, handling files larger than 500 MB without loading the entire
      file into memory.
    question: Is Aspose.PSD for Java suitable for high‑resolution images?
  - answer: Yes, Aspose.PSD for Java supports exporting to PNG, JPEG, TIFF, and many
      other raster formats.
    question: Can I export the image to formats other than BMP?
  - answer: Visit the [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/)
      for comprehensive guides and code samples.
    question: Where can I find more examples and documentation?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- drawing bezier
- Aspose.PSD
- Java graphics
- curve drawing
title: Aspose.PSD ライブラリを使用した Java でのベジエ曲線の描き方
url: /ja/java/java-graphics-drawing/drawing-bezier-curves/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# JavaでAspose.PSDライブラリを使用してベジエ曲線を描く方法

## はじめに
Java デスクトップまたはサーバーアプリケーションで **ベジエの描画方法** 形状の描画方法を知りたい場合、Aspose.PSD for Java はクリーンでメモリ効率の高い API を提供します。このチュートリアルでは、PSD キャンバスの作成、描画ペンの設定、制御点の定義、滑らかなベジエ曲線のレンダリングという正確な手順を示します—低レベルのピクセル操作コードを書くことなく実現できます。

## クイック回答
- **描画を処理するライブラリは何ですか？** Aspose.PSD for Java.  
- **必要なコード行数は？** 約10行の簡潔なステートメントです。  
- **曲線の色を変更できますか？** はい、`Pen` の colour プロパティを調整することで変更できます。  
- **高解像度出力はサポートされていますか？** はい、フルメモリロードなしで最大 500 MB のファイルをサポートします。  
- **商用ライセンスは必要ですか？** 開発には無料トライアルで動作しますが、本番環境ではライセンスが必要です。

## ベジエ曲線とは？
ベジエ曲線は、2 つ以上の点で制御される数学的に定義された滑らかな線です。ベクターグラフィックス、アニメーション、UI デザインで広く使用され、エレガントでスケーラブルな形状を作成します。曲線の形状は開始点、終了点、そして曲率に影響を与える1つ以上の制御点によって決まり、デザイナーはシンプルなパラメータで複雑なパスをモデル化できます。

## なぜ Aspose.PSD を使用してベジエ曲線を描くのか？
Aspose.PSD は **30+ 画像フォーマット** をサポートし、**数百ページの PSD ファイル** を RAM 全体にロードせずに処理できます。ライブラリの `drawBezier()` メソッドは自動的にアンチエイリアスとカラー管理を行い、典型的な 100 × 100 キャンバスでは 1 秒未満でピクセルパーフェクトな結果を提供します。

## 前提条件
1. **Java Development Kit (JDK)** – 任意の最新バージョン（8 以降）をインストールし、設定してください。  
2. **Aspose.PSD for Java JAR** – [Aspose.PSD Java ダウンロード](https://releases.aspose.com/psd/java/) から Aspose.PSD for Java ライブラリを取得し、プロジェクトのクラスパスに追加してください。  
3. **統合開発環境 (IDE)** – Eclipse、IntelliJ IDEA、NetBeans など、JDK が設定されたものを使用してください。

## パッケージのインポート
以下のインポートは、画像作成と描画に必要な Aspose.PSD クラスを取り込みます。
```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## Java でベジエ曲線を描く方法は？
空の `PsdImage` をロードし、`Graphics` オブジェクトを作成し、`Pen` を設定し、開始点、制御点、終了点を定義し、`drawBezier()` を呼び出し、最後に画像を保存します。この手順により、単一のメソッド呼び出しで滑らかな曲線が生成され、ピクセル計算を手動で行う必要はありません。

### 手順 1: 画像インスタンスの作成
`PsdImage` クラスは、メモリ内の単一 PSD ファイルを表す Aspose.PSD の最上位オブジェクトです。まず、メモリ内の PSD 画像を表す `PsdImage` クラスのインスタンスを作成する必要があります。
```java
String dataDir = "Your Document Directory";
Image image = new PsdImage(100, 100);
```
説明:
- `PsdImage` は幅と高さのパラメータでインスタンス化されます（この例では 100 × 100 ピクセル）。

### 手順 2: グラフィックスコンテキストの初期化
`Graphics` クラスは `PsdImage` 上で描画機能を提供します。次に、画像上で描画操作を行うために `Graphics` クラスのインスタンスを初期化します。
```java
Graphics graphics = new Graphics(image);
```
説明:
- `Graphics` オブジェクトは `image` インスタンスで初期化され、描画操作が可能になります。

### 手順 3: グラフィックスサーフェスのクリア
`clear()` メソッドはグラフィックスサーフェスの背景色を設定します。ここでは `Color.getYellow()` を使用して特定の背景色でサーフェスをクリアします。
```java
graphics.clear(Color.getYellow());
```
説明:
- `clear()` メソッドはグラフィックスサーフェスの背景色を設定します。

### 手順 4: 描画用ペンの初期化
`Pen` オブジェクトは色や幅などのストローク属性を定義します。色と幅などのプロパティを設定した `Pen` オブジェクトを用意し、曲線の描画方法を決定します。
```java
Pen blackPen = new Pen(Color.getBlack(), 3);
```
説明:
- `Pen` は黒色と 3 ピクセル幅で初期化されます。

### 手順 5: ベジエ曲線パラメータの定義
制御点が曲率を決定します。ベジエ曲線の制御点と終点を指定します。
```java
float startX = 10, startY = 25;
float controlX1 = 20, controlY1 = 5;
float controlX2 = 55, controlY2 = 10;
float endX = 90, endY = 25;
```
説明:
- `startX`、`startY`: 曲線の開始点。  
- `controlX1`、`controlY1`: 最初の制御点。  
- `controlX2`、`controlY2`: 2 番目の制御点。  
- `endX`、`endY`: 曲線の終了点。

### 手順 6: ベジエ曲線の描画
`drawBezier()` メソッドは、指定された `Pen` と点を使用して曲線を描画します。事前に定義した `Pen` と制御点を使って画像上にベジエ曲線を描くために `drawBezier()` メソッドを使用します。
```java
graphics.drawBezier(blackPen, startX, startY, controlX1, controlY1, controlX2, controlY2, endX, endY);
```
説明:
- `drawBezier()` メソッドは、指定されたパラメータと `blackPen` を使用して曲線を描画します。

### 手順 7: 画像の保存
画像を保存すると、描画結果がディスクに永続化されます。描画した画像を BMP 形式で保存します。
```java
String outpath = dataDir + "Bezier.bmp";
BmpOptions saveOptions = new BmpOptions();
image.save(outpath, saveOptions);
```

## よくある問題と解決策
- **曲線が平坦に見える** – 制御点が開始点と終了点と同一直線上になっていないか確認してください。少しずらすことで曲率が生まれます。  
- **色が変わらない** – `drawBezier()` を呼び出す前に `Pen` の色を変更していることを確認してください。  
- **大きなキャンバスでメモリ不足エラー** – ストリーミングを有効にする `PsdImage` コンストラクタを使用するか、描画をタイルに分割してください。

## よくある質問

**Q: 同じ画像に複数のベジエ曲線を描くことはできますか？**  
A: はい、ループ内で `drawBezier()` を繰り返し呼び出し、各曲線の制御点を更新すれば描画できます。

**Q: ベジエ曲線の色を変更するにはどうすればよいですか？**  
A: `drawBezier()` を呼び出す前に `Pen` オブジェクトの colour プロパティ（例では `Color.getBlack()`）を変更してください。

**Q: Aspose.PSD for Java は高解像度画像に適していますか？**  
A: はい、Aspose.PSD for Java は効率的なメモリ管理により高解像度画像をサポートし、ファイル全体をメモリにロードせずに 500 MB を超えるファイルを処理できます。

**Q: BMP 以外の形式で画像をエクスポートできますか？**  
A: はい、Aspose.PSD for Java は PNG、JPEG、TIFF など多数のラスタ形式へのエクスポートをサポートしています。

**Q: さらに例やドキュメントはどこで見つけられますか？**  
A: 包括的なガイドとコードサンプルについては、[Aspose.PSD for Java ドキュメント](https://reference.aspose.com/psd/java/) をご覧ください。

---

**最終更新日:** 2026-09-08  
**テスト環境:** Aspose.PSD for Java 24.11  
**作者:** Aspose

## 関連チュートリアル

- [Aspose.PSD for Java で画像サイズ変更 – シェイプ描画と基本画像操作](/psd/java/basic-image-operations/)
- [Aspose.PSD for Java を使用して PSD に矩形を描画・保存](/psd/java/basic-image-operations/simple-drawing/)
- [Aspose.PSD を使用した Java のストロークカラー変更方法](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}