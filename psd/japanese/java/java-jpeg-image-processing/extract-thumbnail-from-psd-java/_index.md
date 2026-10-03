---
date: 2026-10-03
description: Aspose.PSD を使用して Java で PSD からサムネイルを抽出する方法を学びます。このステップバイステップガイドでは、setup、code
  snippets、サムネイルを JPEG 画像として保存する方法をカバーしています。
keywords:
- extract thumbnail from psd
- java aspose psd
- psd thumbnail extraction
lastmod: 2026-10-03
linktitle: JavaでPSDからサムネイルを抽出する
og_description: Aspose.PSD とともに Java で PSD からサムネイルを抽出する方法を学びます。このガイドでは、setup、loading
  the file、サムネイルの抽出、JPEG 画像としての保存手順を案内します。
og_image_alt: Screenshot showing Java code extracting a thumbnail from a PSD file
  using Aspose.PSD
og_title: Aspose.PSD を使用して Java で PSD からサムネイルを抽出する
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to extract thumbnail from PSD in Java using Aspose.PSD. This
    step‑by‑step guide covers setup, code snippets, and saving the thumbnail as a
    JPEG image.
  headline: Extract thumbnail from PSD in Java
  type: TechArticle
- questions:
  - answer: Aspose.PSD is a Java library that enables programmatic creation, manipulation,
      and conversion of PSD and other raster image formats without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD?
  - answer: You can refer to the [documentation](https://reference.aspose.com/psd/java/)
      for detailed API references and examples.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: Yes, you can download a [free trial](https://releases.aspose.com/) to
      evaluate the library’s capabilities.
    question: Can I try Aspose.PSD for free before purchasing?
  - answer: Temporary licenses are available from the [temporary license](https://purchase.aspose.com/temporary-license/)
      page.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Yes, Aspose.PSD can be used in both personal and commercial projects under
      its licensing terms.
    question: Is Aspose.PSD suitable for commercial use?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose.psd
- thumbnail extraction
title: JavaでPSDからサムネイルを抽出する
url: /ja/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# JavaでPSDからサムネイルを抽出する

## はじめに
PSDファイルからサムネイルを抽出すると、フル解像度の画像を読み込まずにクイックプレビューを生成できます。Javaでは、Aspose.PSDがこのプロセスをシンプルかつ高速に実現します。このチュートリアルでは、ライブラリの設定方法、サムネイルリソースの位置特定、そしてJPEGファイルとして保存する方法を、数行のコードだけで学びます。

## クイック回答
- **PSDサムネイルを処理するライブラリはどれですか？** Aspose.PSD for Java.
- **必要なコード行数は？** 読み込み、抽出、保存に約5行です。
- **大きなPSDファイルからサムネイルを抽出できますか？** はい、Aspose.PSDは最大500 MBのファイルをフルメモリ読み込みせずに処理できます。
- **開発にライセンスは必要ですか？** 無料トライアルで評価できますが、本番環境ではライセンスが必要です。
- **サポートされている出力形式は何ですか？** 抽出したサムネイルはJPEG、PNG、またはBMPとして保存できます。

## PSDからサムネイルを抽出するとは何ですか？
PSDからサムネイルを抽出するとは、Photoshop（PSD）ドキュメントに埋め込まれた小さなプレビュー画像を読み取るプロセスです。このプレビューはリソースとして保存されており、カタログ化や表示目的で個別に保存できます。サムネイルは通常、フルサイズ画像を読み込まずにアプリケーションが迅速な視覚的概要を示すために使用する低解像度の表現です。

## このタスクにAspose.PSDを使用する理由は？
Aspose.PSDは**30以上の画像フォーマット**をサポートし、**500 MB**までのPSDファイルをメモリ使用量を抑えて処理できます。リソースをオンデマンドで読み込むためです。また、APIは堅牢なエラーハンドリングを提供するので、破損したファイルからでも確実にサムネイルを抽出できます。

## 前提条件
- Java Development Kit (JDK) がインストールされていること。
- Aspose.PSD for Java ライブラリを [Aspose.PSD for Java download](https://releases.aspose.com/psd/java/) からダウンロード。
- Java の構文とプロジェクト設定に関する基本的な知識。

## JavaでPSDファイルからサムネイルを抽出する方法は？
`PsdImage`でPSDファイルをロードし、`ThumbnailResource`を見つけて画像データをJPEGとして保存します。Aspose.PSDは低レベルのパースを抽象化しているため、`getResources()`を呼び出し、抽出した画像に対して`save()`するだけで済みます。この方法は、ファイルサイズに関係なくサムネイルを含むすべてのPSDで機能します。

## パッケージのインポート
`Image`は画像読み込みの基底クラスです。`PsdImage`はPSDドキュメントを表します。`ThumbnailResource`と`Thumbnail4Resource`はサムネイルリソースを表します。`JpegOptions`はJPEG保存オプションを指定します。

```text
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
```

## ステップ1: PSDファイルをロードする
まず、PSDファイルを指す`PsdImage`インスタンスを作成します。コンストラクタはヘッダーと必要なリソースだけを読み取り、メモリ使用量を最小限に抑えます。

```text
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
```

`"Your_Document_Directory/"` をPSDファイルがあるディレクトリパスに、`"your_file.psd"` をPSDファイル名に置き換えてください。

## ステップ2: 画像リソースを反復処理する
Aspose.PSDはサムネイルを画像のリソースコレクション内の`ThumbnailResource`オブジェクトとして保存します。コレクションをループし、リソースタイプを確認して、最初に見つかったサムネイルを取得します。

```text
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Extract thumbnail data
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Create a new image with the extracted thumbnail data
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Save the extracted thumbnail as a separate JPEG file
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Output success message
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Exit the loop once thumbnail is found and processed
    }
}
```
```

## ステップ3: 抽出したサムネイルを保存する
サムネイル画像が取得できたら、`save`メソッドを呼び出してディスクに書き込みます。JPEG、PNG、BMPのいずれかを選択できますが、WebプレビューではJPEGが最も一般的です。

## ステップ4: 異なるサムネイルタイプの処理
PSDに`Thumbnail4Resource`など複数のサムネイルバリエーションが含まれる場合、各タイプをチェックするようにイテレーションロジックを拡張します。APIは各リソースに対して個別のクラスを提供しているため、必要な解像度を選択できます。

## 一般的な問題と解決策
- **サムネイルが見つかりません:** すべてのPSDファイルがプレビューを埋め込んでいるわけではありません。Photoshop の「File → File Info」パネルでソースファイルを確認してください。
- **Unsupported format error:** 最新の Aspose.PSD バージョンを使用していることを確認してください。古いリリースでは新しいサムネイルリソースタイプがサポートされていない場合があります。
- **Out‑of‑memory on large files:** サムネイルだけが必要な場合は、`PsdImage.load(..., LoadOptions)` と `LoadOptions.setLoadResourcesOnly(true)` を使用してフル画像データのロードを回避してください。

## よくある質問

**Q: Aspose.PSDとは何ですか？**  
A: Aspose.PSDは、Adobe Photoshopを必要とせずに、PSDやその他のラスタ画像フォーマットのプログラムによる作成、操作、変換を可能にするJavaライブラリです。

**Q: Aspose.PSD for Java のドキュメントはどこで見つけられますか？**  
A: 詳細な API リファレンスとサンプルは、[documentation](https://reference.aspose.com/psd/java/) を参照してください。

**Q: 購入前に Aspose.PSD を無料で試すことはできますか？**  
A: はい、[free trial](https://releases.aspose.com/) をダウンロードしてライブラリの機能を評価できます。

**Q: Aspose.PSD の一時ライセンスはどのように取得できますか？**  
A: [temporary license](https://purchase.aspose.com/temporary-license/) ページから取得できます。

**Q: Aspose.PSD は商用利用に適していますか？**  
A: はい、ライセンス条件の下で個人・商用プロジェクトの両方で使用できます。

---

**最終更新日:** 2026-10-03  
**テスト環境:** Aspose.PSD for Java 24.12  
**作者:** Aspose

## 関連チュートリアル

- [Aspose.PSD for JavaでPSDをラスタ画像フォーマットに変換する方法](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [Aspose.PSD JavaでPSDをJPEGとして保存しRGBカラーをサポートする](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)
- [Aspose.PSD for Javaで画像をリサイズ – 図形描画と基本画像操作](/psd/java/basic-image-operations/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}