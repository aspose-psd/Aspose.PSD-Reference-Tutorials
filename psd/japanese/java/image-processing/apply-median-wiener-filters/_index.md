---
date: 2026-07-17
description: Aspose.PSD for Java を使用して Median と Wiener フィルターを適用するステップバイステップのフィルタ技術を学び、PSD
  を効率的に GIF に変換します。
keywords:
- convert psd to gif
- remove salt pepper noise
- median filter java
- wiener filter java
lastmod: 2026-07-17
linktitle: Median と Wiener フィルターを適用
og_description: Aspose.PSD for Java を使用して PSD を GIF に変換します。Median と Wiener フィルターの適用方法、ソルト＆ペッパーノイズの除去、高品質
  GIF のエクスポート方法を学びましょう。
og_image_alt: 'Developer guide: Convert PSD to GIF with Median and Wiener filters
  in Java using Aspose.PSD'
og_title: PSD を GIF に変換 – Median と Wiener フィルターを適用 (Java)
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Learn step by step filter techniques to apply Median and Wiener filters
    using Aspose.PSD for Java, and convert PSD to GIF efficiently.
  headline: Convert PSD to GIF – Step‑by‑Step Median & Wiener Filters (Java)
  type: TechArticle
- description: Learn step by step filter techniques to apply Median and Wiener filters
    using Aspose.PSD for Java, and convert PSD to GIF efficiently.
  name: Convert PSD to GIF – Step‑by‑Step Median & Wiener Filters (Java)
  steps:
  - name: Load the Image
    text: '`Image` is Aspose.PSD''s base class representing any supported image file.'
  - name: Cast Image into RasterImage
    text: '`RasterImage` extends `Image` and provides pixel‑level access for raster‑based
      operations.'
  - name: Create MedianFilterOptions Instance
    text: '`MedianFilterOptions` configures the median filter, allowing you to set
      the kernel size.'
  - name: Save the Resultant Image (Convert PSD to GIF)
    text: '`GifOptions` specifies settings for saving an image in GIF format, such
      as color depth and compression. `ExportFormat.Gif` is the enum value used to
      save an image as a GIF file. By following these steps you have successfully
      applied a Median filter and exported the cleaned image as a GIF.'
  type: HowTo
- questions:
  - answer: It reduces salt‑and‑pepper noise while preserving edges.
    question: What does the Median filter do?
  - answer: For adaptive noise reduction that considers local image variance.
    question: When should I use the Wiener filter?
  - answer: A free trial works for development; a commercial license is required for
      production.
    question: Do I need a license to run the code?
  - answer: Yes—Aspose.PSD lets you **convert PSD to GIF** in a single step.
    question: Can I save the output as GIF?
  - answer: Typically under 10 minutes for a basic setup.
    question: How long does the implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert psd
- Aspose.PSD
- Java image processing
- median filter
- wiener filter
title: PSD を GIF に変換 – ステップバイステップ Median & Wiener フィルター (Java)
url: /ja/java/image-processing/apply-median-wiener-filters/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD を GIF に変換: メディアンおよびウィーナーフィルタの適用 (Java)

Java でノイズの多い画像をクリーンアップするための **step‑by‑step filter** ワークフローをお探しなら、ここが最適です。Aspose.PSD for Java を使用すれば、Median と Wiener の両フィルタを簡単に適用でき、処理後に **convert PSD to GIF** も実行できます。このガイドでは、ライブラリのセットアップから最終的な GIF の保存まで、すべてのステップを順に解説するので、アプリケーションに高品質な画像除去機能を自信を持って組み込めます。

## クイック回答
- **What does the Median filter do?** メディアンフィルタはエッジを保持しながら塩胡椒ノイズを低減します。  
- **When should I use the Wiener filter?** ローカル画像分散を考慮した適応型ノイズ除去の際に使用します。  
- **Do I need a license to run the code?** 開発には無料トライアルで動作しますが、本番環境では商用ライセンスが必要です。  
- **Can I save the output as GIF?** はい—Aspose.PSD は **convert PSD to GIF** をワンステップで実行できます。  
- **How long does the implementation take?** 基本的な設定で通常 10 分未満です。

## ステップバイステップフィルタとは？

*step‑by‑step filter* アプローチは、画像処理を明確で管理しやすい段階—画像の読み込み、フィルタオプションの設定、フィルタの適用、そして最終的な保存—に分割します。この体系的なフローにより、各部分のデバッグ、コードの再利用、異なる画像フォーマットへの適応が容易になります。

## なぜ Aspose.PSD for Java を使用するのか？

Aspose.PSD for Java は **30+ image formats** をサポートし、PSD、PNG、JPEG、GIF、BMP、TIFF などを含み、ファイル全体をメモリに読み込むことなく数百ページにわたるドキュメントを処理できます。このライブラリは **zero external dependencies** で、ネイティブバイナリを気にせず任意の Java プロジェクトに組み込めます。Median や Wiener といった組み込みフィルタオプションはすぐに使用でき、API は処理後に GIF、PNG、JPEG へ直接エクスポートするワンクリック変換パスを提供します。

## 前提条件

開始する前に、以下が揃っていることを確認してください。

1. **Aspose.PSD for Java Library** – ライブラリは [here](https://releases.aspose.com/psd/java/) からダウンロードしてインストールします。他の Aspose 製品については [here](https://releases.aspose.com/) を参照してください。  
2. **Java Development Environment** – JDK 8 以上と、IDE またはビルドツール（Maven/Gradle）がマシンに設定されていること。

## パッケージのインポート

`Image`、`RasterImage`、およびフィルタオプションクラスは、画像処理とノイズ除去をフルコントロールできます。

## Aspose.PSD を使用した PSD から GIF への変換方法 (Java)

PSD をロードし、目的のフィルタを適用し、GIF 形式で `save` を呼び出すだけで、数行のコードで完了します。この直接的なパターンにより、個々のステップに入る前に全体の変換フローを把握できます。また、保存時にカラーデプスや圧縮レベルなどの追加オプションも指定可能です。

## ステップバイステップフィルタ: メディアンフィルタの適用方法

メディアンフィルタは **salt‑and‑pepper noise** を除去しつつ、エッジを鮮明に保ちます。各ピクセル上でウィンドウをスライドさせ、中心値を周囲の値の中央値に置き換えることで、重要なディテールをぼかさずに外れ値を効果的に除去します。

### 手順 1: 画像の読み込み

`Image` は、Aspose.PSD がサポートする任意の画像ファイルを表す基底クラスです。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.MedianFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

### 手順 2: Image を RasterImage にキャスト

`RasterImage` は `Image` を継承し、ラスタベースの操作のためにピクセルレベルのアクセスを提供します。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load the source image
Image image = Image.load(sourceFile);
```

### 手順 3: MedianFilterOptions インスタンスの作成

`MedianFilterOptions` はメディアンフィルタを設定し、カーネルサイズを指定できます。

```java
// Cast the image into RasterImage
RasterImage rasterImage = (RasterImage)image;
if (rasterImage == null) {
    return;
}
```

### 手順 4: メディアンフィルタの適用

```java
// Create an instance of MedianFilterOptions class and set the filter size
MedianFilterOptions options = new MedianFilterOptions(4);
```

### 手順 5: 結果画像の保存 (PSD を GIF に変換)

`GifOptions` は GIF 形式で画像を保存する際の設定（カラーデプスや圧縮など）を指定します。`ExportFormat.Gif` は画像を GIF ファイルとして保存するために使用される列挙値です。

```java
// Apply MedianFilterOptions filter to RasterImage object
rasterImage.filter(image.getBounds(), options);
```

これらの手順に従うことで、メディアンフィルタを正常に適用し、クリーンアップされた画像を GIF としてエクスポートできました。

## Wiener フィルタの適用 (オプション拡張)

Wiener フィルタはローカル分散を推定して適応型ノイズ除去を行い、ノイズレベルが変動する画像に最適です。Median フィルタを `WienerFilterOptions` に置き換え、同じワークフローを維持します。

> **Pro tip:** 両方のフィルタで異なるカーネルサイズを試し、ノイズ除去とディテール保持の最適なバランスを見つけてください。

## よくある問題とトラブルシューティング

| 症状 | 考えられる原因 | 対処法 |
|------|----------------|--------|
| `ClassCastException` が `RasterImage` へのキャスト時に発生 | 入力ファイルがラスタ互換の PSD ではありません | PSD にラスタレイヤが含まれているか確認するか、まずレイヤをラスタに変換してください |
| 出力 GIF が空です | 出力先パスが間違っているか、フォルダに書き込み権限がありません | `dataDir` が存在し、書き込み可能なディレクトリを指していることを確認してください |
| フィルタに効果がないように見える | ノイズレベルに対してカーネルサイズが小さすぎます | フィルタサイズを大きくしてください（例: `new MedianFilterOptions(6)`） |

## よくある質問

**Q1: これらのフィルタを任意のフォーマットの画像に適用できますか？**  
A1: はい、Aspose.PSD は 30 以上のフォーマットをサポートしているため、PSD、PNG、JPEG、BMP、TIFF などをフィルタリングできます。

**Q2: Aspose.PSD for Java の無料トライアルは利用できますか？**  
A2: はい、無料トライアルは [here](https://releases.aspose.com/) から取得できます。

**Q3: Aspose.PSD for Java のサポートはどうやって受けられますか？**  
A3: コミュニティサポートは [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) をご覧ください。

**Q4: 公式ドキュメントはどこで見られますか？**  
A4: ドキュメントは [here](https://reference.aspose.com/psd/java/) を参照してください。

**Q5: 商用ライセンスはどのように購入できますか？**  
A5: 製品は [here](https://purchase.aspose.com/buy) から購入できます。

## 結論

このガイドでは、Aspose.PSD for Java を使用して Median（およびオプションで Wiener）フィルタを適用する **step‑by‑step filter** プロセスを示し、除去後に **convert PSD to GIF** する方法を紹介しました。これらの構成要素を活用すれば、写真のクリーンアップ、Web 用アセットの準備、バッチ変換の自動化など、あらゆる Java アプリケーションに堅牢な画像処理パイプラインを統合できます。

---

**最終更新日:** 2026-07-17  
**テスト環境:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**作者:** Aspose  

{{< blocks/products/products-backtop-button >}}

## 関連チュートリアル

- [PSD を GIF に変換 - Aspose.PSD for Java でカラー画像にガウスおよびウィーナーフィルタを適用](/psd/java/image-processing/apply-gaussian-wiener-filters-color-image/)
- [ステップバイステップフィルタ - Aspose.PSD for Java を使用したモーションウィーナーフィルタの適用](/psd/java/image-processing/apply-motion-wiener-filters/)
- [Aspose.PSD for Java を使用した PSD から GIF への変換方法 – ロッシーコンプレッサー](/psd/java/advanced-image-manipulation/implement-lossy-gif-compressor/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

```java
String destName = dataDir + "median_test_denoise_out.gif";
// Save the resultant image as a GIF
image.save(destName, new GifOptions());
```