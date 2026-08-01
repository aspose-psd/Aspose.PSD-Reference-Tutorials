---
date: 2026-08-01
description: Aspose.PSD for Java を使用して Java で画像をブラーする方法、ガウスブラー フィルターを適用し、PSD を GIF
  に変換する手順を簡単に学びましょう。
keywords:
- blur image java
- apply gaussian blur
- convert psd to gif
- aspose psd conversion
lastmod: 2026-08-01
linktitle: 画像をブラーする
og_description: Aspose.PSD を使用して Java で画像をすばやくブラーします。ガウスブラーを適用し、ブラー効果を追加し、PSD を GIF
  に変換する簡潔な Java チュートリアルをご覧ください。
og_image_alt: Guide showing Java code to blur an image and convert PSD to GIF using
  Aspose.PSD
og_title: Java で画像をブラー – Aspose.PSD でガウスブラー効果を追加
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to blur image java using Aspose.PSD for Java, apply gaussian
    blur filter and convert PSD to GIF in a few simple steps.
  headline: Blur Image Java with Aspose.PSD – Add Blur Effect
  type: TechArticle
- description: Learn how to blur image java using Aspose.PSD for Java, apply gaussian
    blur filter and convert PSD to GIF in a few simple steps.
  name: Blur Image Java with Aspose.PSD – Add Blur Effect
  steps:
  - name: Define File Paths
    text: Set the source PSD file and the destination GIF file. Using absolute or
      correctly resolved relative paths prevents “File not found” errors.
  - name: Load the Image
    text: The `Image` class represents any image format that Aspose.PSD can read.
      Loading a PSD returns a concrete subclass that gives you access to layers and
      raster data.
  - name: Convert to RasterImage
    text: '`RasterImage` is the raster‑based representation required by most filters,
      including Gaussian blur. Casting the loaded image ensures the blur algorithm
      works on pixel data rather than vector information.'
  - name: Apply Blur Filter
    text: '`GaussianBlurFilter` applies a Gaussian kernel with a configurable radius.
      In this example we use a radius of 15 pixels on both the X and Y axes, which
      yields a smooth, natural‑looking blur.'
  - name: Save the Result
    text: '`GifOptions` tells Aspose.PSD to encode the final raster image as a GIF.
      The library handles color quantisation automatically, so the output file size
      stays small without manual tweaking. By following these five steps, you have
      successfully **blurred an image** using Aspose.PSD for Java and saved th'
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java.
    question: What library can blur images in Java?
  - answer: Gaussian blur filter.
    question: Which filter creates a smooth blur?
  - answer: Yes – use `GifOptions`.
    question: Can I output to GIF after blurring?
  - answer: A free trial works for testing; a license is required for production.
    question: Do I need a license for development?
  - answer: About 10‑15 minutes for a basic blur.
    question: How long does the implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- blur image java
- Aspose.PSD
- Java image processing
- gaussian blur
- PSD to GIF
title: Aspose.PSD を使用した Java の画像ブラー – ブラー効果を追加
url: /ja/java/advanced-techniques/blur-image/
weight: 24
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD を使用した Java の画像ブラー – ブラー効果の追加

## はじめに

もし **blur image java** プログラムを迅速かつ確実に実行したい場合、Aspose.PSD for Java は任意の PSD ファイルにブラー効果を追加するシンプルな API を提供します。この **java image processing tutorial** では **apply gaussian blur** の方法、**convert psd to gif** の方法、そして Java アプリケーションで背景効果としてブラーを使用したい理由を解説します。手順は平易な言葉で説明しているので、画像処理ライブラリが初めての方でも追従できます。また、他の Aspose ライブラリは [here](https://releases.aspose.com/) で確認できます。

## クイック回答
- **What library can blur images in Java?** Aspose.PSD for Java.  
- **Which filter creates a smooth blur?** Gaussian blur filter.  
- **Can I output to GIF after blurring?** Yes – use `GifOptions`.  
- **Do I need a license for development?** A free trial works for testing; a license is required for production.  
- **How long does the implementation take?** About 10‑15 minutes for a basic blur.

## 「blur image java」とは何ですか？

Java で画像をブラーすることは、隣接するピクセルを平均化する畳み込みを適用し、通常は Gaussian カーネルを使用してディテールを柔らかくすることを意味します。この操作は高周波情報を減少させ、滑らかでピントが合っていない外観を作り出します。背景効果、プライバシーマスキング、または芸術的なスタイリングによく使用され、PSD ファイル内の任意のラスターレイヤーに適用できます。

## このタスクに Aspose.PSD を使用する理由は？

Aspose.PSD は、PSD ファイル内の任意のラスターレイヤーで動作する、即座に使用できる高性能な Gaussian ブラー実装を提供します。このライブラリは **120+ image formats** をサポートし、**2 GB** までの PSD ファイルをドキュメント全体をメモリに読み込まずに処理でき、Java 8+ をサポートする任意の OS 上で動作します。また、ワンクリックで GIF、PNG、JPEG など多数のフォーマットへの変換を提供し、追加の画像ライブラリが不要です。

## 前提条件

- Java Development Kit (JDK) がインストールされていること。  
- Aspose.PSD for Java ライブラリ。ダウンロードは [here](https://releases.aspose.com/psd/java/) から。  
- Java 構文の基本的な知識。

## パッケージのインポート

`com.aspose.psd` パッケージは、Photoshop ドキュメントの読み込み、編集、保存のためのコアクラスを提供します。コーディングを開始する前に必要なクラスをインポートしてください。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.GaussianBlurFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

## ステップバイステップ ガイド

### ステップ 1: ファイルパスの定義  
ソース PSD ファイルと出力先 GIF ファイルを設定します。絶対パスまたは正しく解決された相対パスを使用することで “File not found” エラーを防止できます。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "BlurAnImage_out.gif";
```

### ステップ 2: 画像の読み込み  
`Image` クラスは、Aspose.PSD が読み取れる任意の画像フォーマットを表します。PSD を読み込むと、レイヤーとラスターデータにアクセスできる具体的なサブクラスが返されます。

```java
// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

### ステップ 3: RasterImage への変換  
`RasterImage` は、ほとんどのフィルタ（Gaussian ブラーを含む）で必要となるラスターベースの表現です。読み込んだ画像をキャストすることで、ブラーアルゴリズムがベクトル情報ではなくピクセルデータ上で動作することが保証されます。

```java
// Convert the image into RasterImage
RasterImage rasterImage = (RasterImage)image;
```

### ステップ 4: ブラーフィルタの適用  
`GaussianBlurFilter` は、設定可能な半径を持つ Gaussian カーネルを適用します。この例では X 軸と Y 軸の両方で半径 15 ピクセルを使用し、滑らかで自然なブラーを実現しています。

```java
// Pass Bounds[rectangle] of the image and GaussianBlurFilterOptions instance to the Filter method
rasterImage.filter(rasterImage.getBounds(), new GaussianBlurFilterOptions(15, 15));
```

### ステップ 5: 結果の保存  
`GifOptions` は、最終的なラスタ画像を GIF としてエンコードするよう Aspose.PSD に指示します。ライブラリはカラー量子化を自動的に処理するため、手動で調整しなくても出力ファイルサイズは小さく保たれます。

```java
// Save the results in GIF format
rasterImage.save(destName, new GifOptions());
```

これらの5つのステップを実行することで、Aspose.PSD for Java を使用して画像を **blurred an image** し、GIF として保存することに成功しました。

## なぜ重要なのか

画像のブラーは単なる見た目の調整以上のもので、UI の可読性向上、機密データの保護、プロフェッショナルな被写界深度効果の作成に役立ちます。Aspose.PSD で Gaussian ブラーを適用すると、典型的な 3.0 GHz CPU 上で 1920×1080 の画像に対して 200 ms 未満で処理でき、デスクトップやウェブアプリケーションのリアルタイムプレビューシナリオに適しています。

## 一般的な使用例

1. **User‑interface overlays** – モーダルダイアログが表示されたときに背景を暗くするために、控えめなブラーを適用します。  
2. **Privacy protection** – 画像を共有する前に顔やナンバープレートを隠します。  
3. **Artistic filters** – 複数のブラーパスを組み合わせて夢のような外観を作ります。

## 一般的な問題とヒント

- **Incorrect file path** – `dataDir` が OS に適した区切り文字 (`/` または `\`) で終わっていることを確認してください。  
- **Unsupported image format** – ブラーフィルタはラスタ画像でのみ動作します。ベクターレイヤーは事前にラスタライズする必要があります。  
- **Performance** – 大きな画像は処理に時間がかかる場合があります。速度が重要な場合は、フィルタ適用前に画像のリサイズを検討してください。  
- **Memory consumption** – 処理後に `System.gc()` を呼び出すか、ループで多数の画像を扱う場合はストリームを閉じてメモリ使用量を抑えてください。

## よくある質問

### Q1: Aspose.PSD for Java は初心者開発者に適していますか？
**A:** もちろんです！Aspose.PSD は包括的なドキュメントと直感的な API を備えており、すべてのスキルレベルの開発者をサポートします。

### Q2: Aspose.PSD を商用プロジェクトで使用できますか？
**A:** はい、使用できます。ライセンスオプションは [here](https://purchase.aspose.com/buy) で確認してください。

### Q3: 無料トライアルは利用可能ですか？
**A:** はい、無料トライアルは [here](https://releases.aspose.com/) から取得できます。

### Q4: Aspose.PSD for Java のサポートはどこで受けられますか？
**A:** サポートに関する質問は [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) をご覧ください。

### Q5: Aspose.PSD の一時ライセンスはどのように取得できますか？
**A:** 一時ライセンスは [here](https://purchase.aspose.com/temporary-license/) から取得できます。

## 結論

Aspose.PSD for Java は **blur image java** タスクを簡単に実行できます。**apply gaussian blur**、**add blur effect**、または **convert PSD to GIF** が必要な場合でも、ライブラリがすべての重い処理を担当します。さまざまなブラー半径を試したり、フィルタを組み合わせたりして、**blur background java** がアプリケーションをどのように向上させるかを探ってみてください。

---

**最終更新日:** 2026-08-01  
**テスト環境:** Aspose.PSD for Java 24.11  
**作者:** Aspose

## 関連チュートリアル

- [PSD を GIF に変換 - Aspose.PSD for Java でカラー画像に Gaussian と Wiener フィルタを適用](/psd/java/image-processing/apply-gaussian-wiener-filters-color-image/)
- [ステップバイステップ フィルタ - Aspose.PSD for Java を使用してモーション Wiener フィルタを適用](/psd/java/image-processing/apply-motion-wiener-filters/)
- [Aspose.PSD for Java でグラデーション効果を適用する方法](/psd/java/advanced-image-effects/add-gradient-effects/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}