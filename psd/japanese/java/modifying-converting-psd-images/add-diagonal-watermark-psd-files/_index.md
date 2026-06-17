---
date: 2026-03-04
description: Aspose.PSD を使用して Java でグラフィックスオブジェクトを作成し、PSD ファイルに対角線の透かしを追加する方法を学びます。このステップバイステップガイドでは、Java
  の画像透かしライブラリの使用方法をカバーしています。
linktitle: Add Diagonal Watermark to PSD Files with Java
second_title: Aspose.PSD Java API
title: JavaでGraphicsオブジェクトを作成 – PSD用の斜めウォーターマーク
url: /ja/java/modifying-converting-psd-images/add-diagonal-watermark-psd-files/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java で PSD ファイルに斜めの透かしを追加する

## Introduction
このチュートリアルでは **create graphics object java** を作成し、PSD ファイルに斜めの透かしを追加する方法を紹介します。デザイナーが作品を保護したり、マーケティング担当者が画像にブランドを付与したりする際に、きれいな透かしはプロフェッショナルで安全な印象を与えます。各ステップを明確に解説するので、すぐに自分のプロジェクトに応用できます。

## Quick Answers
- **どのライブラリが必要ですか？** Aspose.PSD for Java（堅牢な Java 画像透かしライブラリ）。  
- **このチュートリアルがカバーする主要キーワードは何ですか？** create graphics object java。  
- **ライセンスは必要ですか？** 無料トライアルでテスト可能です。商用利用には製品ライセンスが必要です。  
- **透かしのテキストやスタイルは変更できますか？** はい。フォント、色、不透明度、回転角度をカスタマイズできます。  
- **サポートされている出力形式は何ですか？** 例では PNG で保存しますが、Aspose.PSD は PSD、JPEG、BMP など多数の形式にエクスポート可能です。

## What is a Graphics Object in Java?
**Graphics** オブジェクトは画像の描画領域を表します。Graphics オブジェクトを作成すると、テキストや図形、その他のビジュアル要素をビットマップや PSD キャンバスに直接描画できるメソッドにアクセスできます。これが主要キーワード **create graphics object java** の核心概念です。

## Why Use Aspose.PSD for Watermarking?
Aspose.PSD は Adobe Photoshop を使用せずに動作する専用の **java image watermark library** です。レイヤー、テキスト描画、画像変換をフルコントロールできるため、サーバーサイド処理やバッチ操作に最適です。

## Prerequisites
コードに入る前に、以下を準備してください。

### 1. Java Development Environment
最新の JDK を [Java website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) からインストールします。

### 2. Aspose.PSD Library
[Aspose Downloads page](https://releases.aspose.com/psd/java/) からライブラリをダウンロードし、Maven、Gradle、または手動でクラスパスに JAR を追加します。

### 3. Basic Understanding of Java
クラス、オブジェクト、ファイル I/O の基本が分かっているとスムーズに進められます。

### 4. IDE Setup
IntelliJ IDEA、Eclipse、NetBeans など、使いやすい IDE を使用してください。

## Import Packages
PSD ファイルを操作するために必要な Aspose.PSD クラスをインポートします。

```java
import com.aspose.psd.Color;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Matrix;
import com.aspose.psd.PointF;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringAlignment;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

必要なパッケージをインポートしたら、次に PSD ファイルに斜めの透かしを追加する手順を見ていきましょう。

## Step 1: Set Up Your Directory
```java
String dataDir = "Your Document Directory";
```
`"Your Document Directory"` を PSD ソースファイルが格納されているフォルダーのパスに置き換えてください。

## Step 2: Load the PSD File
```java
PsdImage psdImage = (PsdImage)Image.load(dataDir + "layers.psd");
```
`Image.load` メソッドでファイルを読み込み、`PsdImage` にキャストして PSD 固有の機能を利用できるようにします。

## Step 3: Create a Graphics Object
```java
Graphics graphics = new Graphics(psdImage);
```
ここで **create graphics object java** を作成します。透かしを描画するキャンバスとなります。

## Step 4: Create a Font for the Watermark
```java
Font font = new Font("Arial", 20.0f);
```
インストールされている任意のフォントを選択します。サイズは透かしの目立ち度を決めます。

## Step 5: Create a Brush for the Watermark
```java
SolidBrush brush = new SolidBrush(Color.fromArgb(50, 128, 128, 128));
```
最初のパラメータ `alpha` が透明度を設定します。`50` のアルファ値で控えめな半透明効果になります。

## Step 6: Set Up the Transform Matrix
```java
graphics.setTransform(new Matrix());
graphics.getTransform().rotateAt(45, new PointF(psdImage.getWidth() / 2, psdImage.getHeight() / 2));
```
画像の中心を基点に 45° 回転させ、斜め効果を実現します。

## Step 7: Define String Alignment
```java
StringFormat sf = new StringFormat();
sf.setAlignment(StringAlignment.Center);
```
センター揃えにすることで、回転した矩形の中央に透かしがきれいに配置されます。

## Step 8: Draw the Watermark
```java
graphics.drawString("Some watermark text", font, brush, new RectangleF(0, psdImage.getHeight() / 2, psdImage.getWidth(), psdImage.getHeight() / 2), sf);
```
`"Some watermark text"` をブランド名や著作権表示に置き換えてください。矩形はテキストが描画される領域を定義します。

## Step 9: Save the Image
```java
psdImage.save(dataDir + "AddDiagnolWatermark_output.png", new PngOptions());
```
出力は PNG としていますが、Aspose.PSD がサポートする任意の形式で保存可能です。

## Common Use Cases
- **ブランド保護:** 半透明ロゴを追加して不正利用を防止。  
- **バッチ処理:** サーバー上で大量画像ライブラリの透かし付与を自動化。  
- **クリエイティブプレビュー:** クライアントに透かし入りドラフトを提示し、オリジナルファイルはそのまま保持。

## Troubleshooting & Tips
- **透明度が見えませんか？** アルファ値を大きく（例: `100`）して透かしを強くします。  
- **透かしがずれていますか？** 回転の基点が画像の幅・高さの正確な半分になっているか確認してください。  
- **パフォーマンスが気になる場合:** 複数画像をループ処理する際は同じ `Graphics` オブジェクトを再利用すると効率的です。

## FAQ's
### What is Aspose.PSD?
Aspose.PSD は Adobe Photoshop を必要とせずに PSD ファイルの操作・加工を行える Java ライブラリです。

### Can I use other fonts for watermarking?
はい。システムにインストールされている任意のフォントを透かしに使用できます。

### Is there a way to customize the watermark's transparency?
もちろんです。`SolidBrush` のアルファ値を調整すれば透明度を変更できます。

### Can I add multiple watermarks?
はい。`drawString` メソッドを複数回呼び出し、異なるパラメータで複数の透かしを追加できます。

### Where can I find more information about Aspose.PSD?
ドキュメントは [here](https://reference.aspose.com/psd/java/) をご覧ください。

---

**Last Updated:** 2026-03-04  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}