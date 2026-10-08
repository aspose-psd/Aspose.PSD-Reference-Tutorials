---
date: 2026-10-08
description: 'Java image processing tutorial: Aspose.PSD を使用して PSD ファイルを操作し、JPEG に保存する方法を学びます。初心者と上級者向けのコード例を含む
  step‑by‑step ガイド。'
keywords:
- java image processing tutorial
- Aspose.PSD
- 2 bit JPEG
- 7 bit JPEG
lastmod: 2026-10-08
linktitle: Java における 2 ビットと 7 ビット JPEG のサポート
og_description: 'Java image processing tutorial: Aspose.PSD を使用して PSD ファイルを操作し、JPEG
  に保存する方法を学びます。developers 向けの詳細な手順、迅速な回答、トラブルシューティングを提供。'
og_image_alt: Guide to processing 2‑ and 7‑bit JPEG images in Java with Aspose.PSD
og_title: 'Java image processing tutorial: 2‑bit と 7‑bit JPEG のサポート'
schemas:
- author: Aspose
  dateModified: '2026-10-08'
  description: 'Java image processing tutorial: learn how to manipulate PSD files
    and save them as JPEGs using Aspose.PSD. Step‑by‑step guide with code examples
    for beginners and pros.'
  headline: 'Java image processing tutorial: support 2‑ and 7‑bit JPEGs'
  type: TechArticle
- description: 'Java image processing tutorial: learn how to manipulate PSD files
    and save them as JPEGs using Aspose.PSD. Step‑by‑step guide with code examples
    for beginners and pros.'
  name: 'Java image processing tutorial: support 2‑ and 7‑bit JPEGs'
  steps:
  - name: '**Java Development Kit (JDK)** – version 8 or higher.'
    text: '**Java Development Kit (JDK)** – version 8 or higher.'
  - name: '**Aspose.PSD for Java library** – you can [download it here](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – you can [download it here](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or NetBeans.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or NetBeans.'
  - name: '**Sample PSD file** – any PSD you wish to convert.'
    text: '**Sample PSD file** – any PSD you wish to convert.'
  - name: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
    text: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a commercial library that enables creation, manipulation,
      and conversion of Photoshop PSD files directly from Java applications.
    question: What is Aspose.PSD for Java?
  - answer: You can download the library from the [website](https://releases.aspose.com/psd/java/)
      and add the JAR to your project’s build path or Maven/Gradle dependencies.
    question: How do I install Aspose.PSD for Java?
  - answer: Yes, you can load custom RGB or CMYK ICC profiles and assign them to the
      `JpegOptions` before saving.
    question: Can I use custom color profiles with Aspose.PSD for Java?
  - answer: It supports PSD, JPEG, PNG, BMP, TIFF, GIF, and over 20 additional raster
      formats.
    question: What image formats does Aspose.PSD for Java support?
  - answer: Yes, you can download a [free trial](https://releases.aspose.com/) to
      evaluate the library before purchasing a license.
    question: Is there a free trial available for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- Aspose.PSD
- JPEG conversion
title: 'Java image processing tutorial: 2‑bit と 7‑bit JPEG のサポート'
url: /ja/java/java-jpeg-image-processing/support-2-7-bits-jpeg-java/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java 画像処理チュートリアル：2 ビットおよび 7 ビット JPEG のサポート

## はじめに
この **Java 画像処理チュートリアル** では、Aspose.PSD for Java ライブラリを使用して PSD ファイルを読み込み、2 ビットまたは 7 ビット JPEG としてエクスポートする方法を紹介します。バッチ変換サービスを構築する場合でも、画像品質を細かく制御したい場合でも、以下の手順で環境設定から最終 JPEG の保存までをすべて解説します。さっそく始めましょう！

## クイック回答
- **2 ビットおよび 7 ビット JPEG を扱えるライブラリはどれですか？** Aspose.PSD for Java。  
- **最低限必要な Java バージョンは？** JDK 8 以降。  
- **開発にライセンスは必要ですか？** 評価用には無料トライアルで利用可能ですが、本番環境では商用ライセンスが必要です。  
- **カラーモードを変更できますか？** はい。`JpegCompressionColorMode` を使用して CMYK、YCCK、その他のモードがサポートされています。  
- **どれくらいファイルサイズが削減できますか？** チャンネルあたり 2 ビットを使用すると、8 ビット出力に比べて JPEG のサイズを最大約 80 % 縮小できます。

## Java 画像処理チュートリアルとは？
Java 画像処理チュートリアルとは、開発者が Java を使用してプログラム的に画像データを操作する方法を段階的に学ぶガイドです。さまざまなフォーマットの読み込み、変換の適用、色や圧縮設定の調整、結果の保存までを網羅し、独自の画像処理ワークフローを構築できるようにします。

## なぜ Aspose.PSD for Java を使用するのか？
Aspose.PSD for Java は、Photoshop 自体を必要とせずに Photoshop ファイルを操作できる包括的な API を提供します。30 以上の画像フォーマットをサポートし、データをストリーミングすることで最大 2 GB のファイルを扱え、レイヤー、チャンネル、カラープロファイルに対する細かな制御が可能なため、高性能なサーバーサイド処理に最適です。

## 前提条件
1. **Java Development Kit (JDK)** – バージョン 8 以上。  
2. **Aspose.PSD for Java ライブラリ** – [ここからダウンロード](https://releases.aspose.com/psd/java/) できます。  
3. **IDE** – IntelliJ IDEA、Eclipse、または NetBeans。  
4. **サンプル PSD ファイル** – 変換したい任意の PSD。  
5. **基本的な Java の知識** – クラス、オブジェクト、例外処理に慣れていること。

## パッケージのインポート
まず、Aspose.PSD の JAR をプロジェクトのクラスパスに追加します。その後、必要な名前空間をインポートします：

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.jpeg.JpegCompressionColorMode;
import com.aspose.psd.fileformats.jpeg.JpegCompressionMode;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.JpegOptions;
```

## Java で PSD 画像を読み込む方法は？
PSD ファイルを読み込むには、`Image` クラスの静的 `load` メソッドを呼び出し、結果を `PsdImage` にキャストします。これにより Photoshop ドキュメントのメモリ内表現が作成され、レイヤー、チャンネル、マスク、メタデータにアクセスでき、これらを操作したり他のフォーマットにエクスポートしたりできます。

`PsdImage` は、Aspose.PSD のコアクラスで、メモリ内の Photoshop ドキュメントを表し、その内容に対する読み書き操作を可能にします。

```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage) Image.load(dataDir + "PsdImage.psd");
```

## 2 ビットまたは 7 ビット出力用の JPEG オプションを設定する方法は？
新しい `JpegOptions` インスタンスを作成し、目的の出力に合わせてプロパティを設定します。`setColorType` を使用して適切な `JpegCompressionColorMode`（例：CMYK や YCCK）を選択し、`setCompressionType` で圧縮アルゴリズムを指定します。最後に、`bitsPerChannel` の値（2 または 7）を設定して各カラーチャンネルのビット深度を制御します。

```java
JpegOptions options = new JpegOptions();
options.setColorType(JpegCompressionColorMode.Cmyk);
options.setCompressionType(JpegCompressionMode.JpegLs);
```

## 低ビット JPEG のチャンネルあたりビット数を設定する方法は？
`bitsPerChannel` は、出力 JPEG の各カラーチャンネルに使用するビット数を指定します。このプロパティを 2 に設定すると各チャンネルが 2 ビットに縮小され、バンディングが目立つ高度に圧縮された画像になります。一方、7 に設定するとより多くのディテールが保持され、極端な低ビットと標準の 8 ビット出力の間のファイルサイズになります。用途に合わせて品質とサイズのバランスが取れる値を選択してください。

```java
byte bpp = 2;
options.setBitsPerChannel(bpp);
```

## カラープロファイルを適用する方法（オプション）？
`ICCProfile` は、デバイスまたは作業空間の色特性を記述する International Color Consortium のプロファイルを表します。カスタム ICC ファイルがある場合は、`ICCProfile.getInstance(path)` で読み込み、`jpegOptions` オブジェクトの `iccProfile` プロパティに割り当てます。プロパティを null のままにすると、Aspose.PSD はデフォルトのシステムプロファイルを使用し、ほとんどのシナリオで機能します。

```java
options.setRgbColorProfile(null);
options.setCmykColorProfile(null);
```

## 処理した画像を JPEG として保存する方法は？
`save` メソッドは、指定されたオプションを使用して画像をファイルに書き込みます。`PsdImage` インスタンスでこのメソッドを呼び出し、対象のファイル名（.jpg 拡張子を含む）と設定した `JpegOptions` を渡します。ライブラリはエンコード、選択したチャンネルあたりビット数とカラープロファイルの適用を処理し、指定通りの JPEG を生成します。

```java
image.save(dataDir + "2_7BitsJPEG_output.jpg", options);
```

## よくある問題と解決策
- **ファイルが大きすぎるエラー** – データをストリーミングし、ファイル全体を RAM に読み込まない最新の Aspose.PSD バージョンを使用していることを確認してください。  
- **予期しない色** – 選択した `JpegCompressionColorMode` が元画像のカラースペースと一致しているか確認してください。  
- **ICC プロファイルが見つからない** – 特定のプロファイルが必要な場合は、`ICCProfile.getInstance(path)` で読み込み、`JpegOptions` に割り当ててください。

## よくある質問

**Q: Aspose.PSD for Java とは何ですか？**  
A: Aspose.PSD for Java は、Java アプリケーションから直接 Photoshop PSD ファイルの作成、操作、変換を可能にする商用ライブラリです。

**Q: Aspose.PSD for Java はどうやってインストールしますか？**  
A: ライブラリは [ウェブサイト](https://releases.aspose.com/psd/java/) からダウンロードでき、JAR をプロジェクトのビルドパスまたは Maven/Gradle の依存関係に追加します。

**Q: Aspose.PSD for Java でカスタムカラープロファイルを使用できますか？**  
A: はい、カスタムの RGB または CMYK ICC プロファイルを読み込み、保存前に `JpegOptions` に割り当てることができます。

**Q: Aspose.PSD for Java がサポートする画像フォーマットは何ですか？**  
A: PSD、JPEG、PNG、BMP、TIFF、GIF、その他 20 以上のラスターフォーマットをサポートしています。

**Q: Aspose.PSD for Java の無料トライアルはありますか？**  
A: はい、ライセンス購入前にライブラリを評価できる [無料トライアル](https://releases.aspose.com/) をダウンロードできます。

**最終更新日:** 2026-10-08  
**テスト環境:** Aspose.PSD 24.12 for Java  
**作者:** Aspose

## 関連チュートリアル

- [Java 画像処理 – CMYK 対応 JPEG-LS のサポート](/psd/java/java-jpeg-image-processing/support-jpeg-ls-cmyk-java/)
- [PSD を JPEG として保存し、RGB カラーをサポートする Aspose.PSD Java](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)
- [Aspose.PSD for Java で PSD をラスタ画像フォーマットに変換する方法](/psd/java/advanced-techniques/convert-psd-to-raster-forms/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}