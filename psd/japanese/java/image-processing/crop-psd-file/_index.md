---
date: 2026-08-17
description: Aspose.PSD for Java を使用して Java で PSD ファイルをトリミングする方法を学びましょう – Java アプリケーションで
  Photoshop ドキュメントを高速かつ正確に切り取る手法です。
keywords:
- crop psd file java
- aspose.psd java
- java image cropping
lastmod: 2026-08-17
linktitle: PSD ファイルをトリミング
og_description: Aspose.PSD for Java を使用して Java で PSD ファイルをトリミングします。このガイドでは、コード不要の解説とベストプラクティスのヒントを交えて、Photoshop
  ファイルを効率的に切り取る手順をステップバイステップで示します。
og_image_alt: Guide showing how to crop a PSD file in Java using Aspose.PSD
og_title: Aspose.PSD を使用した Java の PSD ファイルのトリミング – 高速画像クロッピング
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to crop psd file java with Aspose.PSD for Java – a fast,
    precise way to trim Photoshop documents in your Java applications.
  headline: Crop psd file java using Aspose.PSD
  type: TechArticle
- description: Learn how to crop psd file java with Aspose.PSD for Java – a fast,
    precise way to trim Photoshop documents in your Java applications.
  name: Crop psd file java using Aspose.PSD
  steps:
  - name: set document directory
    text: Replace “Your Document Directory” with the absolute or relative path that
      contains the PSD you want to process.
  - name: load PSD file
    text: The `RasterImage` class is Aspose.PSD’s entry point for raster‑based operations
      on a PSD file. Loading the file creates an in‑memory representation that you
      can manipulate.
  - name: define crop area
    text: '`Rectangle` defines the X and Y coordinates together with width and height
      of the region to keep. This class is part of the standard Java AWT package and
      is used by Aspose.PSD to specify cropping bounds.'
  - name: save cropped PSD
    text: After applying the crop, you can persist the result back to PSD format.
      The library writes only the cropped pixels, keeping the original color mode
      and bit depth.
  - name: save cropped image as PNG
    text: If you need a web‑friendly version, export the cropped raster to PNG. Aspose.PSD
      provides PNG save options that let you control compression level and interlacing.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java.
    question: What library handles PSD cropping in Java?
  - answer: Two API calls after loading the image.
    question: How many lines of code are required for a basic crop?
  - answer: Yes, using the built‑in PNG save options.
    question: Can I export the cropped area as PNG?
  - answer: A commercial license is needed beyond the trial period.
    question: Is a license required for production use?
  - answer: Java 8 and later, including Java 11, 17, and 21.
    question: What Java versions are supported?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- crop psd
- aspose.psd
- java image processing
title: Aspose.PSD を使用した Java の PSD ファイルをトリミング
url: /ja/java/image-processing/crop-psd-file/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD を使用した Java の PSD ファイルのトリミング

## はじめに

Photoshop ドキュメントをプログラムでトリミングする必要がある場合、**crop psd file java** は、グラフィック パイプライン、アセット パイプライン、または自動化されたデザイン ワークフローで作業する Java 開発者にとって一般的なタスクです。Aspose.PSD for Java は、矩形を定義し、必要な領域を数行のコードで抽出できる専用 API を提供します。このチュートリアルでは、ライブラリが高性能なトリミング向けに設計されている理由、環境設定方法、そして PSD と PNG の両方の結果を生成する正確な手順を学びます。

## クイック回答
- **Java で PSD のトリミングを処理するライブラリは何ですか？** Aspose.PSD for Java.
- **基本的なトリミングに必要なコード行数は？** 画像をロードした後の API 呼び出しが 2 回です。
- **トリミングした領域を PNG としてエクスポートできますか？** はい、組み込みの PNG 保存オプションを使用します。
- **本番環境での使用にライセンスは必要ですか？** トライアル期間を過ぎた場合は商用ライセンスが必要です。
- **サポートされている Java バージョンは？** Java 8 以降、Java 11、17、21 を含みます。

## crop psd file java とは？

crop psd file java は、Java コードを使用して Photoshop ドキュメント（.psd）から矩形領域をプログラム的に切り取るプロセスを指します。Aspose.PSD を使用すれば、Photoshop を起動せずにこの操作を実行でき、サーバーサイドの画像パイプラインに最適です。

## なぜ Aspose.PSD for Java を使用するのか？

Aspose.PSD は **30 以上の入力および出力フォーマット** をサポートし、**500 MB** までの PSD ファイルをメモリ全体にロードせずに処理できるストリーミング アーキテクチャを備えています。レイヤー、マスク、カラープロファイルを保持し、Photoshop のネイティブ出力と一致するトリミング結果を提供します。この定量的なパフォーマンスにより、予測可能なメモリ使用量で汎用ハードウェア上のバッチ ジョブを処理できます。

## 前提条件

- **Java 開発環境** – JDK 8 以上がインストールされ、設定されていること。
- **Aspose.PSD for Java** – 最新の JAR とドキュメントをダウンロードしてください [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/)。
- **サンプル PSD ファイル** – プロジェクトディレクトリ内に .psd ファイルを配置し、コードが参照できるようにします。

## Java で PSD ファイルをトリミングする方法は？

ソース ファイルを読み込み、保持したい矩形を定義し、トリミングを適用し、最後に希望のフォーマットで結果を保存します。全体のワークフローはわずか 5 つのシンプルな手順で完了し、各手順はプレースホルダーで示されていますので、そこに自分のコードを挿入してください。

### 手順 1: ドキュメントディレクトリの設定

“Your Document Directory” を、処理したい PSD が格納されている絶対パスまたは相対パスに置き換えてください。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.xmp.types.complex.colorant.ColorType;
```

### 手順 2: PSD ファイルの読み込み

`RasterImage` クラスは、PSD ファイルに対するラスターベースの操作のエントリ ポイントです。ファイルを読み込むことで、メモリ内表現が作成され、操作できるようになります。

```java
String dataDir = "Your Document Directory";
```

### 手順 3: トリミング領域の定義

`Rectangle` は、保持する領域の X、Y 座標と幅・高さを定義します。このクラスは標準の Java AWT パッケージの一部で、Aspose.PSD がトリミング境界を指定するために使用します。

```java
String sourceFileName = dataDir + "1.psd";
RasterImage image = (RasterImage)Image.load(sourceFileName);
```

### 手順 4: トリミングした PSD の保存

トリミングを適用した後、結果を PSD 形式で永続化できます。ライブラリはトリミングされたピクセルのみを書き込み、元のカラーモードとビット深度を保持します。

```java
image.crop(new Rectangle(10, 30, 100, 100));
```

### 手順 5: トリミング画像を PNG として保存

Web フレンドリーなバージョンが必要な場合、トリミングされたラスタを PNG にエクスポートします。Aspose.PSD は圧縮レベルやインターレースを制御できる PNG 保存オプションを提供します。

```java
String exportPathPsd = dataDir + "CropTest.psd";
image.save(exportPathPsd, new PsdOptions());
```

## よくある問題と解決策

- **矩形座標が正しくない** – X/Y の値が左上隅で 0 から始まっていることを確認してください。負の値は `ArgumentException` をスローします。
- **大きなファイルでのメモリスパイク** – 隠しレイヤーが不要な場合は `loadOptions.setLoadOnlyVisibleLayers(true)` オプションを使用してメモリ使用量を削減します。
- **カラープロファイルの喪失** – トリミング前に `image.getColorProfile()` を呼び出して元の ICC プロファイルを取得し、操作後に再割り当てして保持します。

## よくある質問

### Q1: Aspose.PSD for Java を使用して他の形式の画像をトリミングできますか？

A1: Aspose.PSD は主に PSD ファイルを対象としていますが、BMP、GIF、JPEG、PNG、TIFF などの複数のラスタ形式の入力および出力もサポートしています。

### Q2: Aspose.PSD for Java は大規模画像処理に適していますか？

A2: はい。ライブラリのストリーミング アーキテクチャは、メモリ フットプリントを 100 MB 未満に抑えながら、数百ページに及ぶ PSD ファイルを処理できるため、バッチ ジョブに最適です。

### Q3: Aspose.PSD for Java の使用に関するライセンス上の考慮点はありますか？

A3: 本番環境での導入には商用ライセンスが必要です。詳細は [Aspose.PSD for Java purchase page](https://purchase.aspose.com/buy) にあります。

### Q4: Aspose.PSD for Java に関する問題のサポートはどう受けられますか？

A4: [Aspose.PSD for Java forum](https://forum.aspose.com/c/psd/34) にアクセスして質問を投稿したり、コード スニペットを共有したり、コミュニティや製品エンジニアから支援を受けてください。

### Q5: 購入前に Aspose.PSD for Java を試せますか？

A5: はい、完全に機能する無料トライアルを [Aspose.PSD free trial download](https://releases.aspose.com/) からダウンロードできます。

{{< blocks/products/products-backtop-button >}}

```java
String exportPathPng = dataDir + "CropTest.png";
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
image.save(exportPathPng, options);
```

## 関連チュートリアル

- [Aspose.PSD for Java で矩形による画像のトリミング](/psd/java/image-editing/crop-image-by-rectangle/)
- [Aspose.PSD for Java でシフトによる画像のトリミング](/psd/java/image-editing/crop-image-by-shifts/)
- [Aspose.PSD を使用した Java での画像回転方法](/psd/java/advanced-image-manipulation/rotate-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}