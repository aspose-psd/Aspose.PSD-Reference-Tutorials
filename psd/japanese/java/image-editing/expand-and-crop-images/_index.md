---
date: 2026-07-08
description: Java 画像編集ライブラリのチュートリアル：Aspose.PSD for Java を使用して画像を crop、resize、expand
  canvas、そして PSD を JPEG に変換する方法を学びます。
keywords:
- java image editing library
- java image processing tutorial
- how to crop image java
lastmod: 2026-07-08
linktitle: 画像の Expand と Crop
og_description: Java 画像編集ライブラリのチュートリアルでは、Aspose.PSD for Java を使用して数分で画像を crop、expand
  canvas、そして PSD を JPEG に変換する方法を示します。
og_image_alt: 'Guide: Crop and expand images in Java with Aspose.PSD'
og_title: Java 画像編集ライブラリ – Aspose.PSD で画像を crop
schemas:
- author: Aspose
  dateModified: '2026-07-08'
  description: 'Java image editing library tutorial: learn how to crop image java
    using Aspose.PSD for Java, resize, expand canvas, and convert PSD to JPEG.'
  headline: Java Image Editing Library – Crop Image with Aspose.PSD
  type: TechArticle
- questions:
  - answer: Aspose.PSD for Java.
    question: What library handles crop image java?
  - answer: A free trial works for testing; a commercial license is required for production.
    question: Do I need a license for development?
  - answer: Yes, using `JpegOptions` together with a cropping rectangle.
    question: Can I convert PSD to JPEG while cropping?
  - answer: Aspose.PSD supports Java 8 and newer versions.
    question: Is Java 8 supported?
  - answer: Typically under 10 minutes for a basic crop operation.
    question: How long does the implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image editing
- Aspose.PSD
- image cropping
- PSD to JPEG
title: Java 画像編集ライブラリ – Aspose.PSD で画像を crop
url: /ja/java/image-editing/expand-and-crop-images/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java 画像編集ライブラリ: Aspose.PSD を使用した Java の画像クロップ

## はじめに

このチュートリアルでは、**java image editing library**（具体的には Aspose.PSD for Java）を使用して、PSD ファイルをクロップ、拡張、JPEG に変換する方法を学びます。Web ポータル用のアセットを準備する場合やサムネイル生成を自動化する場合でも、以下の手順は繰り返し使用できる本番環境向けのワークフローを提供し、Java 8 以降のプロジェクトに統合できます。

## クイック回答
- **crop image java を処理するライブラリは何ですか？** Aspose.PSD for Java.  
- **開発にライセンスは必要ですか？** 無料トライアルでテストは可能ですが、本番環境では商用ライセンスが必要です。  
- **クロップしながら PSD を JPEG に変換できますか？** はい、`JpegOptions` とクロップ矩形を組み合わせて使用します。  
- **Java 8 はサポートされていますか？** Aspose.PSD は Java 8 以降をサポートしています。  
- **実装にどれくらい時間がかかりますか？** 基本的なクロップ操作で通常 10 分未満です。

## “crop image java” とは？

Crop image java とは、元画像の矩形領域を選択し、その領域外を破棄することを指します。Aspose.PSD を使用すると、領域を定義する `Rectangle` を作成し、`RasterImage` に適用してから、JPEG などのサポートされている形式で結果を保存できます。

## なぜ Java の画像クロップに Aspose.PSD を使用するのか？

Aspose.PSD は **java image editing library** を提供し、PSD ファイルをネイティブに処理し、100 以上のレイヤー機能をサポートし、最大 10 000 × 10 000 ピクセルの画像をメモリ使用量 500 MB 未満で処理できます。また、外部ツールを必要とせずに JPEG、PNG、BMP などへの組み込み変換も提供します。これにより、バルク処理パイプラインが高速で信頼性が高く、保守が容易になります。

## 前提条件

1. **Java Development Kit (JDK)** – Java 8 以降がインストールされていること。  
2. **Aspose.PSD for Java** – 公式サイトからライブラリをダウンロードしてください **[こちら](https://releases.aspose.com/psd/java/)**。  

> **プロのヒント:** `ClassNotFoundException` を回避するため、Aspose.PSD JAR をプロジェクトのクラスパスまたは Maven/Gradle の依存関係に追加してください。

## パッケージのインポート

Java ソースファイルに必要なインポートを追加します。これらのクラスにより、画像の読み込み、ラスタ操作、矩形定義、JPEG エクスポートオプションにアクセスできます。

## Aspose.PSD を使用した Java の画像クロップ方法

`RasterImage` でソース PSD を読み込み、クロップ領域を表す `Rectangle`（負の座標でキャンバスを拡張できます）を定義し、最後に `JpegOptions` で結果を保存します。この 3 ステップのフローは、クロップとフォーマット変換を一度に処理し、中間ファイルの必要性を排除します。

## 手順 1: ドキュメントディレクトリの設定

ソース PSD ファイルが格納されているフォルダーを指定します。プレースホルダーを実際のパスに置き換えてください。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

## 手順 2: ソースと出力先のパスを指定

PSD を読み込む場所と、クロップした JPEG を書き込む場所を定義します。

```java
String dataDir = "Your Document Directory";
```

## 手順 3: 画像の読み込みとキャッシュ

`RasterImage` は PSD ファイルのラスタライズ版をメモリ上に表します。  
PSD を `RasterImage` オブジェクトに読み込みます。キャッシュすることで、クロップなどの後続操作のパフォーマンスが向上します。

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## 手順 4: クロップ用の矩形を作成

`Rectangle` はクロップ領域の X、Y 座標と幅/高さを定義します。  
保持したい領域を表す `Rectangle` を作成します。座標は負の値にでき、クロップ前にキャンバスを **拡張** できるため、元画像の周囲に余白を追加するのに便利です。

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

> **負の座標を使用する理由は？**  
> 負の X/Y 値はクロップ領域を左/上にシフトし、最終的なクロップの前に元コンテンツの周囲に空白（拡張）を効果的に追加します。

## 手順 5: クロップした画像を保存

`JpegOptions` は JPEG 出力の設定（品質や圧縮など）を指定します。  
最後に、`JpegOptions` を使用して結果画像を保存します。このステップは、クロップ矩形を適用しながら **convert psd jpeg** を実演しています。

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

> **結果:** `jpeg_out.jpg` には、各側が 200 px 拡張され、定義された矩形でクロップされた 300 × 300 ピクセルの画像が含まれます。

おめでとうございます！**java image cropping** を正常に実行し、キャンバスを拡張し、PSD ファイルを JPEG に変換しました—すべて数行のコードで完了です。

## 一般的な使用例

- **Web 用アセットの準備** – アップロード前にスクリーンショットやデザインをクロップおよびリサイズします。  
- **サムネイル生成** – プレビュー用に大きな PSD から特定領域を抽出します。  
- **自動バッチ処理** – PSD ファイルが入ったフォルダーをループし、同じクロップ矩形を各ファイルに適用します。

## トラブルシューティングとヒント

| 問題 | 推奨修正 |
|-------|----------------|
| 大きな PSD を読み込む際の `OutOfMemoryError` | 早期に `rasterImage.cacheData()` を呼び出し、JVM ヒープサイズ（`-Xmx`）の増加を検討してください。 |
| クロップ領域が中心からずれている | 矩形の X/Y オフセットを確認し、負の値がキャンバスを拡張することを忘れないでください。 |
| 出力 JPEG がぼやけている | `JpegOptions` の品質設定を調整します（例: `new JpegOptions { Quality = 90 }`）。 |

## よくある質問

### Q1: Aspose.PSD はさまざまな Java バージョンと互換性がありますか？

A1: はい、Aspose.PSD は Java 8、11、17 およびそれ以降のバージョンをサポートしており、開発環境全体で幅広い互換性を提供します。

### Q2: Aspose.PSD を商用プロジェクトで使用できますか？

A2: もちろんです。Aspose.PSD は開発者向けに商用ライセンスを提供しており、個人・商用問わず使用できます。

### Q3: サポートされている画像ファイル形式に制限はありますか？

A3: Aspose.PSD は PSD、JPEG、PNG、BMP、TIFF などを含む 30 種類以上の画像形式をサポートしています。完全な一覧は [ドキュメント](https://reference.aspose.com/psd/java/) を参照してください。

### Q4: Aspose.PSD に関する質問へのサポートはどのように受けられますか？

A4: [Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34) にアクセスし、コミュニティまたは Aspose サポートチームから支援を受けてください。

### Q5: 無料トライアルは利用できますか？

A5: はい、無料トライアルで Aspose.PSD をお試しいただけます。こちらからダウンロードしてください [こちら](https://releases.aspose.com/)。

---

**最終更新日:** 2026-07-08  
**テスト環境:** Aspose.PSD for Java 24.12  
**作者:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

## 関連チュートリアル

- [Aspose.PSD を使用したシンプルリサイズ – Java 画像操作ライブラリ](/psd/java/basic-image-operations/simple-resizing/)
- [Aspose.PSD for Java で画像を 270 度回転させる方法](/psd/java/advanced-image-manipulation/rotate-image/)
- [Aspose.PSD を使用した Java 画像処理でガンマを調整する方法](/psd/java/advanced-techniques/adjust-gamma/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}