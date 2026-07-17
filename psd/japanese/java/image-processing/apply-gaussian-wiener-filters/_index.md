---
date: 2026-07-17
description: Aspose.PSD を使用した Java 画像処理チュートリアルです。Gaussian と Wiener フィルタをステップバイステップで適用し、驚くべきビジュアル結果を得る方法を学びます。
keywords:
- java image processing tutorial
- export png java
- gaussian filter java
- wiener filter java
lastmod: 2026-07-17
linktitle: Gaussian と Wiener フィルタを適用する
og_description: Aspose.PSD for Java を使用した Java 画像処理チュートリアルで、Gaussian と Wiener フィルタの適用方法と、PNG
  などの形式へのエクスポートを示します。
og_image_alt: 'Developer guide: Apply Gaussian and Wiener filters to images in Java
  using Aspose.PSD'
og_title: Java 画像処理チュートリアル – Gaussian と Wiener フィルタの適用
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Java image processing tutorial using Aspose.PSD learn how to apply
    Gaussian and Wiener filters step‑by‑step for stunning visual results.
  headline: Java Image Processing Tutorial – Apply Gaussian & Wiener Filters
  type: TechArticle
- questions:
  - answer: It smooths an image by averaging neighboring pixels, reducing high‑frequency
      noise.
    question: What does the Gaussian filter do?
  - answer: It performs adaptive smoothing, preserving edges while diminishing noise.
    question: What is the Wiener filter?
  - answer: Aspose.PSD for Java provides built‑in support for both filters.
    question: Which library is used?
  - answer: A trial works for testing, but a commercial license is required for production.
    question: Do I need a license?
  - answer: Yes—Aspose.PSD supports PNG, JPEG, BMP, and many more.
    question: Can I output formats other than GIF?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- Aspose.PSD
- gaussian filter
- wiener filter
- export png java
title: Java 画像処理チュートリアル – Gaussian と Wiener フィルタの適用
url: /ja/java/image-processing/apply-gaussian-wiener-filters/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java 画像処理チュートリアル – Aspose.PSD を使用したガウスおよびウィーナーフィルタの適用

## はじめに

私たちの **java image processing tutorial** へようこそ。Aspose.PSD for Java を使用してガウスフィルタとウィーナーフィルタを適用する方法を示します。ノイズの多い写真のクリーンアップやウェブ配信用のグラフィックの準備など、これらのフィルタは滑らかでプロフェッショナルな結果を提供します。次の数分で、PSD ファイルの読み込みからフィルタ適用後の GIF への保存までの全工程をご覧いただけます。

## クイック回答
- **Gaussian フィルタは何をしますか？** 画像の隣接ピクセルを平均化して平滑化し、高周波ノイズを低減します。  
- **Wiener フィルタとは何ですか？** 適応的に平滑化を行い、エッジを保持しながらノイズを減少させます。  
- **使用されているライブラリはどれですか？** Aspose.PSD for Java は両方のフィルタを組み込みでサポートしています。  
- **ライセンスは必要ですか？** テストにはトライアルが使用できますが、本番環境では商用ライセンスが必要です。  
- **GIF 以外の形式で出力できますか？** はい、Aspose.PSD は PNG、JPEG、BMP など多数の形式をサポートしています。

## Java 画像処理チュートリアルとは？

Java 画像処理チュートリアルは、開発者に画像の読み込み、フィルタやリサイズなどの変換の適用、そして最終的に希望の形式で保存するという基本的な手順を案内します。明確なコード例と解説を提供することで、画像操作機能を Java アプリケーションに直接組み込むことができ、外部ツールの必要性を減らします。

## なぜ Gaussian と Wiener フィルタを使用するのか？

画像を読み込み、Gaussian‑Wiener フィルタを適用すると、粒状ノイズが大幅に減少し、重要なエッジは鮮明に保たれます。これはウェブ用グラフィックやアーカイブスキャンの準備に最適です。Gaussian 部分は高周波ノイズを除去し、Wiener 部分は局所的な分散に適応して重要なディテールを保持します。

## 前提条件

- Java 開発環境 (JDK 8 以上)。  
- Aspose.PSD for Java ライブラリ。**[here](https://releases.aspose.com/psd/java/)** からダウンロードできます。  
- Java の構文とオブジェクト指向概念に関する基本的な知識。

## パッケージのインポート

インポート文は Aspose.PSD のクラスをスコープに持ち込み、ラスタ画像、フィルタオプション、出力形式を操作できるようにします。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.GaussWienerFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

これらのインポートにより、画像の読み込み、ラスタ操作、フィルタオプション、出力形式にアクセスできます。

## 手順 1: 画像の読み込み

`RasterImage` クラスは、ピクセル単位で処理できるラスタベースの画像を表します。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);
RasterImage rasterImage = (RasterImage)image;
```

指定ディレクトリから PSD ファイルを読み込み、`RasterImage` にキャストしてピクセルデータを操作できるようにします。

## 手順 2: RasterImage の確認

安全チェックで、読み込んだファイルがラスタベースであることを確認します。そうでない場合は、ルーチンが安全に終了します。

```java
if (rasterImage == null) {
    return;
}
```

## 手順 3: フィルタオプションの設定

`GaussWienerFilterOptions` クラスを使用すると、Gaussian と Wiener の両方のパラメータを単一オブジェクトで細かく調整できます。

```java
GaussWienerFilterOptions options = new GaussWienerFilterOptions(12, 3);
options.setGrayscale(true);
```

- 最初の引数 (`12`) は Gaussian カーネルの半径サイズを定義します。  
- 2 番目の引数 (`3`) は Wiener アルゴリズムで使用されるスムーズ値を設定します。  
- `setGrayscale(true)` はフィルタにグレースケールで動作させるよう指示し、ノイズ低減でよりクリーンな結果が得られます。

## 手順 4: フィルタの適用と保存

`filter` メソッドは、設定された Gaussian‑Wiener の組み合わせを画像全体に適用します。最後に、`GifOptions` を使用して処理済み画像を GIF として保存します。`GifOptions` を `PngOptions`、`JpegOptions` などに置き換えることで、**export PNG Java** や他の形式でエクスポートできます。

```java
rasterImage.filter(image.getBounds(), options);
String destName = dataDir + "gauss_wiener_out.gif";
image.save(destName, new GifOptions());
```

## よくある問題とヒント

- **Null RasterImage:** ソースファイルが PSD または他のラスタ互換形式であることを確認してください。  
- **Performance:** 大きな画像は処理に時間がかかる場合があります。半径を小さくするか、縮小コピーで先に処理することを検討してください。  
- **Color vs. Grayscale:** カラーを保持したい場合は、`options.setGrayscale(false)` を設定してください。

## よくある質問

**Q1: これらのフィルタを PSD 以外の形式の画像に適用できますか？**  
A1: はい、Aspose.PSD for Java は PSD 以外にも PNG、JPEG、BMP、GIF などさまざまな画像形式をサポートしています。

**Q2: Aspose.PSD for Java のトライアル版に制限はありますか？**  
A2: トライアル版は出力サイズを制限し、透かしが追加されます。フル機能を利用するには有効なライセンスを取得してください。

**Q3: Aspose.PSD for Java のサポートはどこで受けられますか？**  
A3: コミュニティ支援と公式回答のために **[Aspose.PSD Forum](https://forum.aspose.com/c/psd/34)** をご覧ください。

**Q4: テスト用の一時ライセンスはありますか？**  
A4: はい、**[here](https://purchase.aspose.com/temporary-license/)** から一時ライセンスを取得できます。

**Q5: Aspose.PSD for Java の詳細なドキュメントはどこで見つけられますか？**  
A5: 詳細な API リファレンスと追加サンプルについては **[documentation](https://reference.aspose.com/psd/java/)** を参照してください。

## 結論

これで、Aspose.PSD for Java を使用して **Gaussian** と Wiener フィルタを **適用** する方法を示す完全な **java image processing tutorial** が完了しました。さまざまな半径やスムーズ値を試し、グレースケールの切り替えや PNG などの他の出力形式を試して、フィルタが画像に与える影響を確認してください。コーディングを楽しんでください！

---

**Last Updated:** 2026-07-17  
**Tested With:** Aspose.PSD for Java 23.12 (latest at time of writing)  
**Author:** Aspose

## 関連チュートリアル

- [ステップバイステップフィルタ - Aspose.PSD for Java を使用したモーションウィーナーフィルタの適用](/psd/java/image-processing/apply-motion-wiener-filters/)
- [ステップバイステップフィルタ - Median と Wiener フィルタの適用 (Java)](/psd/java/image-processing/apply-median-wiener-filters/)
- [Aspose.PSD for Java で PNG ファイルをフィルタリングする方法](/psd/java/optimizing-png-files/apply-filters-png-files/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}