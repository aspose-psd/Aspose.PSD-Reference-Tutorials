---
date: 2026-07-27
description: Aspose.PSD for Java（業界トップクラスの Java 画像操作ライブラリ）を使用して、PSD を TIFF に変換し、画像のコントラスト調整を行う方法を学びます。
keywords:
- convert psd to tiff
- java image processing
- improve image contrast
lastmod: 2026-07-27
linktitle: PSD を TIFF に変換し、コントラストを調整する
og_description: Aspose.PSD for Java を使用して、コントラスト調整付きで PSD を TIFF に変換します。本ガイドでは、ステップバイステップのコード、パフォーマンス向上のヒント、そして高品質な
  TIFF 出力のためのエクスポートオプションを紹介します。
og_image_alt: 'Guide: Convert PSD to TIFF and adjust contrast using Aspose.PSD for
  Java'
og_title: PSD を TIFF に変換しコントラスト調整 – Aspose.PSD Java
schemas:
- author: Aspose
  dateModified: '2026-07-27'
  description: Learn how to convert PSD to TIFF and perform image contrast adjustment
    using Aspose.PSD for Java, a leading java image manipulation library.
  headline: Convert PSD to TIFF and Adjust Contrast with Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: It changes the difference between the darkest and brightest pixels, making
      details pop.
    question: What does “adjust contrast” mean?
  - answer: Aspose.PSD for Java – a full‑featured image processing toolkit.
    question: Which library handles this?
  - answer: A **temporary Aspose license** works for testing; a full license is required
      for production.
    question: Do I need a license?
  - answer: Absolutely – we’ll use `TiffOptions` to export the processed image.
    question: Can I convert PSD to TIFF?
  - answer: For a typical 30 MB PSD the whole pipeline runs under one second on a
      modern CPU.
    question: How fast is the conversion?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert psd
- Aspose.PSD
- Java image manipulation
- tiff export options
title: Aspose.PSD for Java を使用して PSD を TIFF に変換し、コントラストを調整する
url: /ja/java/advanced-techniques/adjust-contrast/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java を使用した PSD から TIFF への変換とコントラスト調整方法

## はじめに

グラフィックの視覚品質を微調整しながら **PSD を TIFF に変換** したい場合は、ここが適切な場所です。このチュートリアルでは、堅牢な **java 画像操作** ライブラリである Aspose.PSD for Java を使用した完全なワークフローを順に解説します。**画像コントラスト調整** を強化し、パフォーマンス向上のために大きなラスターデータをキャッシュし、最後に **画像を TIFF として保存** します。このステップで下流処理が可能になります。さっそく始めましょう！

## クイック回答
- **“adjust contrast” は何を意味しますか？** 最も暗いピクセルと最も明るいピクセルの差を変えることで、ディテールが際立ちます。  
- **どのライブラリがこれを処理しますか？** Aspose.PSD for Java – フル機能の画像処理ツールキットです。  
- **ライセンスは必要ですか？** テスト用には **一時的な Aspose ライセンス** で動作しますが、本番環境ではフルライセンスが必要です。  
- **PSD を TIFF に変換できますか？** もちろんです – 処理した画像をエクスポートするために `TiffOptions` を使用します。  
- **変換はどのくらい速いですか？** 標準的な 30 MB の PSD では、最新の CPU でパイプライン全体が 1 秒未満で完了します。

## 画像コントラスト調整とは？
コントラスト調整は画像のトーン範囲を変更し、明暗領域の差を拡大します。スキャン後に画像が平坦に見える場合や、印刷用のグラフィックを準備する際に特に有用です。ピクセル強度のヒストグラムを伸縮させることで、シャドウを深く、ハイライトを明るくし、視覚的な奥行きとディテールを向上させます。

## なぜ Aspose.PSD for Java を使用するのか？
Aspose.PSD は高性能で機能豊富なエンジンを提供し、**50 以上のラスタおよびベクタ形式** を扱い、最大 500 MB のファイルを完全にメモリにロードせずに処理でき、TIFF へのエクスポート時にビット／サンプルやフォトメトリック解釈を正確に制御できます。これらの数値化された機能により、エンタープライズ向け画像パイプラインの最適な選択肢となります。

## 前提条件

- Java プログラミングの基本的な知識。  
- Aspose.PSD for Java ライブラリがインストールされていること。ダウンロードは [here](https://releases.aspose.com/psd/java/) から可能です。

## パッケージのインポート

Java クラスに必要なインポートを追加します:
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## ステップ 1: 画像の読み込み

`Image` クラスは Aspose.PSD のエントリーポイントで、サポートされている任意のラスタ画像をメモリ上で表現します。  
```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

ソース PSD ファイル（`sample.psd`）を `Image` オブジェクトに読み込みます。これが以降のすべての処理のエントリーポイントとなります。

## ステップ 2: RasterImage にキャストしてデータをキャッシュ

`RasterImage` はピクセルレベルの直接アクセスを提供し、大きなファイルのキャッシュを可能にします。  
```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

`RasterImage` にキャストすることでピクセルレベルの操作が可能になります。キャッシュは特に大きなファイルでパフォーマンスを向上させます。

## 画像のコントラストを調整する方法

`adjustContrast` メソッドは、パーセンテージ値で画像のコントラストを変更するシンプルな API 呼び出しです。  
```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

`adjustContrast` メソッドは、変化率を表す整数を受け取ります。この例ではコントラストを **50 %** 増加させます。

## Aspose.PSD を使用して PSD を TIFF に変換

`TiffOptions` を使用すると、ビット／サンプル、圧縮タイプ、フォトメトリック解釈など、TIFF 固有の設定を指定できます。  
```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Save the resultant image to TIFF format
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

ここでは `TiffOptions`（ビット／サンプル、フォトメトリック解釈）を設定し、**画像を TIFF として保存**します。このステップで **PSD を TIFF に変換**するワークフローが完了します。

## 一般的な問題と解決策
- **画像がキャッシュされていない:** 大きな PSD では必ず `cacheData()` を呼び出して `OutOfMemoryError` を回避してください。  
- **予期しない色シフト:** `setPhotometric` が対象のカラースペース（RGB と CMYK）と一致しているか確認してください。  
- **ファイルが見つからない:** `dataDir` が正しいフォルダーを指していること、ファイル名が正しく綴られていることを確認してください。

## よくある質問

### Q1: Aspose.PSD はさまざまな画像形式に対応していますか？

A1: はい、Aspose.PSD は **50 以上の入力および出力形式** をサポートしており、PSD、TIFF、PNG、JPEG、BMP、GIF など、プロジェクト間で柔軟に使用できます。

### Q2: Aspose.PSD の一時ライセンスはどのように取得できますか？

A2: 一時ライセンスは [here](https://purchase.aspose.com/temporary-license/) から取得できます。

### Q3: Aspose.PSD のドキュメントはどこで見つけられますか？

A3: ドキュメントは [here](https://reference.aspose.com/psd/java/) にあります。

### Q4: Aspose.PSD のサポートオプションは何がありますか？

A4: サポートについては [Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34) をご覧ください。

### Q5: Aspose.PSD を購入できますか？

A5: はい、[here](https://purchase.aspose.com/buy) から購入できます。

## 結論

これで **PSD を TIFF に変換**し、Aspose.PSD for Java を使用して **画像コントラスト調整** を行う方法が分かりました。これらの手順により、コードをシンプルかつ保守しやすく保ちつつ、画像品質を細かく制御できます。`adjustBrightness` や `adjustGamma` など、他の調整メソッドも自由に試して、特定のニーズに合わせてください。

**最終更新日:** 2026-07-27  
**テスト環境:** Aspose.PSD for Java 24.12  
**作者:** Aspose

## 関連チュートリアル

- [Java 画像処理チュートリアル - Aspose.PSD for Java で画像の明るさを調整](/psd/java/advanced-techniques/adjust-brightness/)
- [Aspose.PSD を使用した Java 画像処理でガンマを調整する方法](/psd/java/advanced-techniques/adjust-gamma/)
- [Aspose.PSD for Java で PSD をラスタ画像形式に変換](/psd/java/advanced-techniques/convert-psd-to-raster-forms/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}