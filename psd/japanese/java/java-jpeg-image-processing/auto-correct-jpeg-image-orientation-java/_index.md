---
date: 2026-09-18
description: Aspose.PSD を使用して Java で JPEG の向きを自動補正する方法を学びます。自動 EXIF ベースの回転により画像処理ワークフローを強化します。
keywords:
- auto correct jpeg orientation
- Aspose.PSD for Java
- Java image processing
lastmod: 2026-09-18
linktitle: JavaでJPEG画像の向きを自動補正
og_description: Aspose.PSD を使用して Java で JPEG の向きを自動補正する方法を学びます。このガイドでは、EXIF データの検出、画像の自動回転、補正ファイルの効率的な保存方法をステップバイステップで示します。
og_image_alt: Guide showing auto correction of JPEG orientation in Java with Aspose.PSD
og_title: Aspose.PSD を使用した Java の JPEG 向き自動補正
schemas:
- author: Aspose
  dateModified: '2026-09-18'
  description: Learn how to auto correct JPEG orientation in Java using Aspose.PSD.
    Enhance your image processing workflow with automatic EXIF‑based rotation.
  headline: Auto correct JPEG image orientation in Java
  type: TechArticle
- questions:
  - answer: Aspose.PSD for Java is a powerful library that allows Java developers
      to work with PSD, JPEG, and other image formats programmatically.
    question: What is Aspose.PSD for Java?
  - answer: You can download the library from the [Aspose PSD Java release page](https://releases.aspose.com/psd/java/).
    question: How can I download Aspose.PSD for Java?
  - answer: Yes, it supports various image manipulation tasks such as resizing, cropping,
      and adjusting orientation.
    question: Does Aspose.PSD for Java support image manipulation?
  - answer: Comprehensive documentation is available on the [Aspose.PSD for Java documentation
      site](https://reference.aspose.com/psd/java/).
    question: Where can I find documentation for Aspose.PSD for Java?
  - answer: Yes, you can get a free trial from the [Aspose free trial page](https://releases.aspose.com/).
    question: Can I try Aspose.PSD for Java for free?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- auto correct jpeg
- Aspose.PSD
- Java image processing
title: JavaでJPEG画像の向きを自動補正
url: /ja/java/java-jpeg-image-processing/auto-correct-jpeg-image-orientation-java/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# JavaでJPEG画像の向きを自動補正

## はじめに
今日のデジタル時代において、プログラムで画像を操作・最適化することは、さまざまな分野の開発者にとって重要なタスクとなっています。**Auto correct JPEG orientation** は、異なるデバイスで撮影された写真を扱う際の一般的な要件です。Aspose.PSD for Java は、PSD、JPEG、その他の画像フォーマットを効率的に処理するための強力なツールを提供します。本チュートリアルでは、Aspose.PSD for Java を使用して JPEG 画像の向きを自動的に補正するという具体的なタスクに踏み込みます。写真編集アプリの構築、CMS における画像リソースの管理、あるいは画像処理パイプラインの自動化など、あらゆるシナリオでこの機能をシームレスに統合する方法を学びます。

## クイック回答
- **Auto correct JPEG orientation は何をしますか？** EXIF の回転データを読み取り、画像を回転させて、どのデバイスでも正しく表示されるようにします。  
- **どのライブラリが回転を処理しますか？** Aspose.PSD for Java は組み込みの EXIF 処理と自動回転を提供します。  
- **開発にライセンスは必要ですか？** 無料トライアルで評価は可能ですが、製品版には商用ライセンスが必要です。  
- **大量バッチ処理は可能ですか？** はい。フォルダーをループして数千枚の画像を最小限のメモリ使用で処理できます。  
- **どの Java バージョンがサポートされていますか？** Aspose.PSD は JDK 8 から 21 まで対応しています。

## Auto correct JPEG orientation とは何ですか？
Auto correct JPEG orientation は、画像の EXIF “Orientation” タグを自動的に検出し、ビットマップを回転させて手動操作なしで正しい向きに表示させる機能です。このプロセスは JPEG ファイルに埋め込まれたメタデータを読み取り、必要な回転または反転を判定し、変換を適用して、すべての閲覧プラットフォームで写真家の意図通りの表示になるようにします。

## Auto correcting JPEG orientation に Aspose.PSD を使用する理由
Aspose.PSD は **30 以上の画像フォーマット** をサポートし、画像全体をメモリに読み込むことなく **2 GB** までのファイルを処理でき、同等のハードウェア上で手動のピクセル単位回転に比べて最大 **5 倍高速** のパフォーマンスを実現します。また、PSD ファイル内の JPEG サムネイルなどの埋め込みリソースも処理でき、低レベルの EXIF パースを抽象化した高レベル API を提供するため、実装がシンプルかつ信頼性があります。

## 前提条件
- Java 開発環境: システムに Java Development Kit (JDK) がインストールされていることを確認してください。  
- Aspose.PSD for Java JAR: [Aspose PSD Java リリースページ](https://releases.aspose.com/psd/java/) から Aspose.PSD for Java ライブラリをダウンロードしてください。  
- 統合開発環境 (IDE): IntelliJ IDEA、Eclipse、またはお好みの Java 開発用 IDE を使用してください。  
- Java と画像処理の基本的な理解: Java プログラミングと画像処理の基本概念に慣れていると役立ちます。

## パッケージのインポート
例を始める前に、Aspose.PSD for Java から必要なパッケージをインポートしてください。`Image` クラスは画像の読み込みと保存の基本型で、`JpegExifData` は EXIF メタデータへのアクセスを提供し、サムネイルリソースクラスは埋め込み JPEG プレビューを表します。  

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## Aspose.PSD を使用した Java での JPEG 画像向き自動補正方法
対象の PSD ファイルをロードし、埋め込み JPEG サムネイルを見つけ、Aspose.PSD に EXIF の向き情報を読み取らせ、自動回転を適用し、最後に補正された画像を保存します。このワークフローは数回のメソッド呼び出しだけで済み、PSD コンテナに埋め込まれた任意の JPEG 画像に対して機能するため、単一画像でもバッチ処理でも適用可能です。

## 手順 1: PSD 画像のロード
`PsdImage` クラスは PSD ファイルを表し、埋め込み JPEG サムネイルを含むリソースへのアクセスを提供します。  
まず、向き補正が必要な JPEG サムネイルを含む PSD 画像をロードします:

```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```
`"Your Document Directory"` を、PSD ファイルが置かれている実際のディレクトリパスに置き換えてください。

## 手順 2: 画像リソースのイテレーション
次に、画像リソースをイテレートして JPEG サムネイルリソースを見つけます。`ThumbnailResource` と `Thumbnail4Resource` は、PSD ファイル内に埋め込まれた JPEG プレビューの異なるバージョンを表します。

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    // Find thumbnail resource. Typically they are in the Jpeg file format.
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // Adjust thumbnail data.
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
        if (exifData != null && exifData.getThumbnail() != null) {
            // If there is a thumbnail stored, auto-rotate it.
            PsdImage jpegImage = (PsdImage) exifData.getThumbnail();
            if (jpegImage != null) {
                jpegImage.autoRotate();
            }
        }
    }
}
```

## 手順 3: 画像の保存
最後に、自動回転を適用した後、補正された画像を保存します:

```java
image.save();
```
この手順により、画像への変更が永続化されます。

## よくある問題とトラブルシューティング
- **EXIF タグが検出されない** – JPEG サムネイルに実際に Orientation タグが含まれていることを確認してください。カメラによっては省略されることがあります。  
- **大きなファイルでのメモリエラー** – メモリ使用量を抑えるために `PsdImage.load(..., LoadOptions)` と `LoadOptions.setLoadAllResources(false)` を使用してください。  
- **回転方向が正しくない** – 最新の Aspose.PSD バージョンを使用しているか確認してください。古いリリースには特定の向き値で既知のバグがありました。

## よくある質問

**Q: Aspose.PSD for Java とは何ですか？**  
**A:** Aspose.PSD for Java は、Java 開発者が PSD、JPEG、その他の画像フォーマットをプログラムで操作できる強力なライブラリです。

**Q: Aspose.PSD for Java はどこからダウンロードできますか？**  
**A:** ライブラリは [Aspose PSD Java リリースページ](https://releases.aspose.com/psd/java/) からダウンロードできます。

**Q: Aspose.PSD for Java は画像操作をサポートしていますか？**  
**A:** はい、リサイズ、クロップ、向き調整などさまざまな画像操作タスクをサポートしています。

**Q: Aspose.PSD for Java のドキュメントはどこで見つけられますか？**  
**A:** 詳細なドキュメントは [Aspose.PSD for Java ドキュメントサイト](https://reference.aspose.com/psd/java/) にあります。

**Q: Aspose.PSD for Java を無料で試せますか？**  
**A:** はい、[Aspose 無料トライアルページ](https://releases.aspose.com/) から無料トライアルを取得できます。

**Q: 自動回転機能はスレッドセーフですか？**  
**A:** はい、各 `PsdImage` インスタンスは共有状態なしで別スレッドで処理できます。

**Q: 数千枚の画像のバッチ処理はどう行いますか？**  
**A:** ディレクトリをループし、各 PSD をロードして自動回転手順を適用し、保存します。ライブラリはバッファを再利用してメモリ消費を低く抑えます。

## 結論
結論として、Aspose.PSD for Java を使用することで、PSD ファイル内の JPEG 画像の向きを自動的に補正する強力なソリューションが得られます。本チュートリアルの手順に従うことで、画像処理ワークフローを強化し、すべてのプラットフォームやデバイスで画像が正しく表示されるようにできます。

---

**Last Updated:** 2026-09-18  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose

## 関連チュートリアル

- [Java JPEG 画像処理](/psd/java/java-jpeg-image-processing/)
- [Aspose.PSD for Java で PSD を JPEG に変換し 270° 回転](/psd/java/advanced-image-manipulation/rotate-image/)
- [Aspose.PSD for Java で特定の角度で画像を回転する方法](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}