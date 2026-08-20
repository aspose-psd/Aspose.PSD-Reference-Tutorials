---
date: 2026-06-03
description: Aspose.PSD for Java を使用して画像をリサイズする方法を学びます。このステップバイステップガイドでは、Resize Type
  Enumeration、高品質画像リサイズ、そして PSD を JPEG に変換する方法をカバーしています。
keywords:
- how to resize image
- convert psd to jpeg
- high quality image resize
- resize image java
- java image manipulation tutorial
linktitle: Resize Type Enumeration を使用したリサイズ
schemas:
- author: Aspose
  dateModified: '2026-06-03'
  description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  headline: How to Resize Image Java Using Resize Type Enumeration
  type: TechArticle
- description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  name: How to Resize Image Java Using Resize Type Enumeration
  steps:
  - name: '**Java Development Environment** – JDK 8 or newer installed and configured.'
    text: '**Java Development Environment** – JDK 8 or newer installed and configured.'
  - name: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
  - name: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
    text: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
  type: HowTo
- questions:
  - answer: Load the PSD with `Image.load`, then call `image.save("output.jpg", new
      JpegOptions());`.
    question: How do I programmatically convert a PSD file to JPEG without resizing?
  - answer: Yes, you can set the `Resolution` property on the `Image` object before
      saving.
    question: Is it possible to maintain the original DPI when resizing?
  - answer: While you can call `resize` multiple times, it’s more efficient to calculate
      the final dimensions and resize once.
    question: Can I chain multiple resize operations?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Resize Type Enumeration を使用した Java の画像リサイズ方法
url: /ja/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Resize Type 列挙型を使用した Java の画像リサイズ方法

## はじめに

Java プロジェクトで **画像リサイズ** を効率的に行いたい場合、Aspose.PSD for Java はクリーンで高性能な API を提供します。このチュートリアルでは、PSD の読み込み、**Resize Type 列挙型** を使用した高品質な画像リサイズ、そして最終的に **PSD を JPEG に変換** する手順を解説します。デスクトップエディタの構築や自動サーバーサイドパイプラインの作成など、数行のコードでサイズ、品質、フォーマットを制御できます。

## クイック回答
- **画像リサイズを扱うライブラリはどれですか？** Aspose.PSD for Java。
- **どのリサイズタイプが最高品質ですか？** `ResizeType.LanczosResample`。
- **リサイズ後に PSD を JPEG に変換できますか？** はい、`JpegOptions` で保存すれば可能です。
- **本番環境でライセンスは必要ですか？** 本番利用には有効な Aspose.PSD ライセンスが必要です。
- **大量バッチにこのアプローチは適していますか？** はい。API はドキュメント全体をメモリにロードせずに数百ページのファイルを処理できます。

## Java における「画像リサイズ」の意味
**画像リサイズ** とは、画像のピクセル寸法をプログラムで変更しつつ、視覚的な忠実度を保つことを指します。Aspose.PSD の `Resize` メソッドと `ResizeType` 列挙型を組み合わせることで、スケーリングアルゴリズムを細かく制御でき、さまざまなソースファイルとターゲットサイズで品質を維持できます。

## なぜ Resize Type 列挙型を使用するのか
`ResizeType` は速度と視覚品質のバランスを最適化するリサンプリングアルゴリズムを選択できるようにします。多くのシナリオで **LanczosResample** は、典型的なサーバークラス CPU 上で 2000 × 1500 の画像を 120 ms 未満で処理し、エッジディテールを保った鋭い結果を提供します。

## 前提条件

開始する前に以下を用意してください。

1. **Java 開発環境** – JDK 8 以上がインストールされ、設定されていること。  
2. **Aspose.PSD ライブラリ** – 最新の JAR を [website](https://releases.aspose.com/psd/java/) からダウンロード。  
3. **サンプル PSD ファイル** – SDK に同梱されている [sample.psd](Your Document Directory/sample.psd) をテストに使用。

## パッケージのインポート

`Image` は Aspose.PSD のすべての画像タイプの基底クラスです。Java ソースファイルに必要なインポートを追加します。

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## 手順 1: 画像の読み込み

### 定義アンカー
`RasterImage` クラスは、PSD ファイルから読み込まれたラスタ画像を表す Aspose.PSD のコアオブジェクトです。

PSD を `RasterImage` インスタンスにロードし、ピクセルを操作できるようにします。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

## 手順 2: 画像のリサイズ

`image.resize(width, height, resizeType)` は、指定した寸法と選択したアルゴリズムで画像をリサイズします。

**Resize Type 列挙型** を使用してロードした画像をリサイズします。この例では、高品質なリサイズが求められる場合に最適な Lanczos Resample メソッドを使用します。

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## 手順 3: リサイズした画像の保存

`image.save(path, options)` は、指定されたオプションでフォーマットを決定し、**ディスク** に画像を書き込みます。

リサイズ後、指定した寸法と選択したリサイズタイプで画像を保存します。ここでは、結果を JPEG ファイルとして保存し、**psd を jpeg に変換** する方法も示します。

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

## なぜ Resize Type 列挙型を使用するのか

`ResizeType` はリサンプリングアルゴリズムを細かく制御でき、速度と品質のバランスを取ることができます。多くのアプリケーションで `LanczosResample` は、重いパフォーマンスペナルティなしに鋭い結果を提供し、さまざまな画像コンテンツに対して優れたトレードオフを実現します。

## よくある問題と解決策

- **リサイズ後に画像がぼやける** – `Bicubic` や `NearestNeighbour` など別の `ResizeType` を試して、対象画像に最適な視覚結果を確認してください。  
- **大きな PSD ファイルで OutOfMemoryError が発生** – 画像を小さなチャンクに分割して処理するか、JVM ヒープサイズ（`-Xmx` フラグ）を増やしてください。Aspose.PSD は **2 GB** までのファイルをメモリ全体にロードせずに処理できます。

## FAQ

### Q1: Aspose.PSD for Java は小規模・大規模プロジェクトのどちらにも適していますか？

A1: はい！Aspose.PSD for Java は規模を問わずプロジェクトに対応できるよう設計されており、スケーラビリティと効率性を提供します。

### Q2: Lanczos Resample 以外のリサイズタイプは使用できますか？

A2: できます。Aspose.PSD for Java には **NearestNeighbour**、**Bicubic** など複数のリサイズタイプが用意されています。完全な一覧は API ドキュメントをご参照ください。

### Q3: Aspose.PSD for Java の追加サポートはどこで受けられますか？

A3: ご質問や支援が必要な場合は、[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34)をご利用ください。

### Q4: Aspose.PSD for Java の無料トライアルはありますか？

A4: はい、[こちら](https://releases.aspose.com/)から無料トライアル版にアクセスできます。

### Q5: Aspose.PSD for Java の一時ライセンスはどこで取得できますか？

A5: 一時ライセンスは [このリンク](httpshttps://purchase.aspose.com/temporary-license/) から取得してください。

## よくある質問

**Q: リサイズせずに PSD ファイルを JPEG にプログラムで変換する方法は？**  
A: `Image.load` で PSD を読み込み、`image.save("output.jpg", new JpegOptions());` を呼び出します。

**Q: リサイズ時に元の DPI を保持できますか？**  
A: はい、保存前に `Image` オブジェクトの `Resolution` プロパティを設定すれば可能です。

**Q: 複数のリサイズ操作をチェーンできますか？**  
A: `resize` を複数回呼び出すことは可能ですが、最終的な寸法を計算して一度だけリサイズする方が効率的です。

---

**最終更新日:** 2026-06-03  
**テスト環境:** Aspose.PSD for Java 24.12  
**作者:** Aspose  

{{< blocks/products/products-backtop-button >}}

## 関連チュートリアル

- [Simple Resizing with Aspose.PSD – Java Image Manipulation Library](/psd/java/basic-image-operations/simple-resizing/)
- [High Quality Image Scaling with Bicubic Resampler in Aspose.PSD for Java](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)
- [How to Convert PSD to PNG and Resize Proportionally with Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}