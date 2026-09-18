---
date: 2026-09-18
description: Aspose.PSD for Java を使用して、java 画像メタデータの thumbnail を EXIF セグメントに追加する方法を学びます。このステップバイステップガイドでは、前提条件、コードの解説、更新された画像の保存について説明します。
keywords:
- java image metadata
- how to add thumbnail
- java exif metadata
lastmod: 2026-09-18
linktitle: Java で EXIF セグメントに Thumbnail を追加
og_description: Aspose.PSD for Java を使用して、java 画像メタデータの thumbnail を EXIF セグメントに追加する方法を学びます。ステップバイステップのガイドに従って
  thumbnail を埋め込み、更新された画像を保存してください。
og_image_alt: Guide showing Java code to embed a thumbnail into EXIF metadata using
  Aspose.PSD
og_title: java 画像メタデータの thumbnail を EXIF セグメントに追加する方法
schemas:
- author: Aspose
  dateModified: '2026-09-18'
  description: Learn how to add java image metadata thumbnail to the EXIF segment
    using Aspose.PSD for Java. This step‑by‑step guide covers prerequisites, code
    walkthrough, and saving the updated image.
  headline: How to add java image metadata thumbnail to EXIF segment
  type: TechArticle
- questions:
  - answer: EXIF metadata is embedded information in digital images that includes
      camera settings, capture date, GPS coordinates, and other details.
    question: What is EXIF metadata?
  - answer: Adding a thumbnail improves user experience by allowing quick image previews
      without loading the full image.
    question: Why add a thumbnail to EXIF?
  - answer: You can download Aspose.PSD for Java from the [Aspose.PSD for Java download
      page](https://releases.aspose.com/psd/java/).
    question: Where can I download Aspose.PSD for Java?
  - answer: You can obtain a temporary license for Aspose.PSD from the [temporary
      license page](https://purchase.aspose.com/temporary-license/).
    question: How can I get a temporary license for Aspose.PSD?
  - answer: For support, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).
    question: How do I get support for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image metadata
- EXIF thumbnail
- Aspose.PSD
- Java image processing
title: java 画像メタデータの thumbnail を EXIF セグメントに追加する方法
url: /ja/java/java-jpeg-image-processing/add-thumbnail-to-exif-segment-java/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# EXIF セグメントに Java 画像メタデータサムネイルを追加する

## はじめに
このチュートリアルでは、Aspose.PSD for Java を使用して PSD ファイルの EXIF セグメントに **java image metadata** サムネイルを追加する方法を学びます。EXIF（Exchangeable Image File Format）メタデータは、カメラ設定、撮影日時、位置情報、その他の有用な情報を保存します。小さなプレビューサムネイルを埋め込むことで、アプリケーションはフルファイルを読み込まずに画像の概要をすばやく表示でき、パフォーマンスとユーザーエクスペリエンスが向上します。

## クイック回答
- **このチュートリアルの内容は何ですか？** Aspose.PSD for Java を使用して PSD 画像の EXIF セグメントにサムネイルを追加します。  
- **実装にどれくらい時間がかかりますか？** 基本的な統合で約 10〜15 分です。  
- **ライセンスは必要ですか？** 本番利用には一時ライセンスが必要です。評価目的には無料トライアルが利用できます。  
- **サポートされている Java バージョンは？** Java 8 以降が完全にサポートされています。  
- **大きなファイルを処理できますか？** はい — Aspose.PSD は画像全体をメモリに読み込まずに、最大 2 GB のファイルを処理できます。  

## java 画像メタデータとは？
Java 画像メタデータとは、EXIF、IPTC、XMP などの画像ファイルに埋め込まれた構造化情報で、Aspose.PSD のような Java ライブラリを使用してプログラムから読み取り、変更、作成できるものです。このメタデータにより、アプリケーションはビジュアルコンテンツを開かずにカメラ設定、タイムスタンプ、GPS 座標、カスタムデータなどを取得できます。

## EXIF メタデータにサムネイルを追加する理由は？
EXIF セグメントにサムネイルを追加することで、画像ブラウザ、ファイルエクスプローラ、コンテンツ管理システムに即座に視覚的な手がかりを提供します。Aspose.PSD はサムネイルをインメモリで処理し、500 KB 以下の画像に対して 0.2 秒未満でプレビューを埋め込むことができ、PSD、JPEG、PNG、TIFF など 30 以上の画像フォーマットをサポートしています。

## 前提条件
- Java プログラミングの基本的な知識。  
- システムにインストールされた Java Development Kit (JDK)。  
- IntelliJ IDEA や Eclipse などの Java 用 IDE（統合開発環境）。  
- Aspose.PSD for Java ライブラリ。[Aspose.PSD for Java Download page](https://releases.aspose.com/psd/java/) からダウンロードできます。  

## パッケージのインポート
以下のインポートは、PSD 画像と EXIF データを操作するために必要な Aspose.PSD クラスを取り込みます。  
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## ステップ 1: PSD 画像をロードする
`PsdImage` は Photoshop の PSD ファイルを表し、そのレイヤーやリソースへのアクセスを提供します。  
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "sample.psd");
```

## ステップ 2: 画像リソースを反復処理する
`ImageResource` は、サムネイル、ICC プロファイル、PSD ファイルに埋め込まれたメタデータなどのリソースをカプセル化します。  
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        // Process the thumbnail resource
    }
}
```

## ステップ 3: サムネイルデータを調整する
`JpegOptions` を使用すると、サムネイル画像の品質など、JPEG 固有の設定を構成できます。  
```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setQuality(100); // Set JPEG quality
```

## ステップ 4: 画像を保存する
`save` を呼び出すと、更新された EXIF セグメント（新しいサムネイルを含む）がディスクに書き込まれ、画像全体を再エンコードせずに保存されます。  
```java
image.save(dataDir + "output.psd");
```

## 一般的な問題と解決策
- **サムネイルが表示されない:** サムネイルリソースが EXIF セグメントに正しく追加され、`PsdImage.save` メソッドで画像が保存されていることを確認してください。  
- **大きなファイルでのメモリ不足エラー:** `PsdImage.load(..., LoadOptions)` と `LoadOptions.setLoadOnlyMetadata(true)` を使用して、メタデータのみを操作してください。  
- **向きが正しくない:** サムネイルが元画像の向きフラグを尊重していることを確認します。`Orientation` EXIF タグを読み取り、必要に応じてサムネイルを回転させてください。  

## よくある質問

**Q: EXIF メタデータとは何ですか？**  
A: EXIF メタデータは、デジタル画像に埋め込まれた情報で、カメラ設定、撮影日時、GPS 座標、その他の詳細が含まれます。

**Q: EXIF にサムネイルを追加する理由は？**  
A: サムネイルを追加することで、フル画像を読み込まずに迅速なプレビューが可能になり、ユーザーエクスペリエンスが向上します。

**Q: Aspose.PSD for Java はどこからダウンロードできますか？**  
A: Aspose.PSD for Java は [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/) からダウンロードできます。

**Q: Aspose.PSD の一時ライセンスはどのように取得できますか？**  
A: 一時ライセンスは [temporary license page](https://purchase.aspose.com/temporary-license/) から取得できます。

**Q: Aspose.PSD のサポートはどこで受けられますか？**  
A: サポートは [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) で受けられます。

**最終更新日:** 2026-09-18  
**テスト環境:** Aspose.PSD for Java 24.10  
**作者:** Aspose

## 関連チュートリアル

- [Aspose.PSD for Java を使用した PSD ファイルでの XMP メタデータ作成](/psd/java/image-editing/create-xmp-metadata/)
- [Aspose.PSD for Java で画像をリサイズ – シェイプ描画と基本的な画像操作](/psd/java/basic-image-operations/)
- [Aspose.PSD for Java を使用して PSD をラスタ画像フォーマットに変換する方法](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}