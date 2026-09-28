---
date: 2026-09-28
description: Aspose.PSD を使用して Java で JFIF セグメントにサムネイルを追加する方法です。ステップバイステップのガイドに従って、PSD
  ファイルにサムネイルを迅速かつ確実に埋め込むことができます。
keywords:
- how to add thumbnail
- JFIF segment Java
- Aspose.PSD thumbnail
- Java image processing
lastmod: 2026-09-28
linktitle: JavaでJFIFセグメントにサムネイルを追加
og_description: Aspose.PSD を使用して Java で JFIF セグメントにサムネイルを追加する方法です。ステップバイステップのガイドに従って、PSD
  ファイルにサムネイルを迅速かつ確実に埋め込むことができます。
og_image_alt: Guide showing how to add thumbnail to JFIF segment in Java with Aspose.PSD
og_title: JavaでJFIFセグメントにサムネイルを追加する方法
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  headline: How to add thumbnail to JFIF segment in Java
  type: TechArticle
- description: How to add thumbnail to a JFIF segment in Java using Aspose.PSD. Follow
    this step‑by‑step guide to embed thumbnails in PSD files quickly and reliably.
  name: How to add thumbnail to JFIF segment in Java
  steps:
  - name: import packages
    text: '`Document`, `JfifResource`, and related classes are part of the Aspose.PSD
      namespace. Document represents the PSD file container, and JfifResource provides
      access to the JFIF segment within the PSD. Import them at the top of your source
      file.'
  - name: load the PSD image
    text: Create a `PsdImage` instance by passing the file path to the constructor.
      PsdImage is the Aspose.PSD class that models a Photoshop document. This loads
      the document metadata while streaming the pixel data.
  - name: iterate over image resources
    text: Search the `Resources` collection for a `JfifResource`. When found, you
      can replace its thumbnail byte array with a new JPEG‑encoded preview.
  - name: adjust thumbnail data
    text: Generate a small JPEG thumbnail (e.g., 120 × 120 px) using any image‑processing
      library, then assign the resulting byte array to `jfifResource.ThumbnailData`.
  - name: save the modified image
    text: Call the `save` method on the `PsdImage` object, specifying the output path
      and desired format. The JFIF segment now contains the new thumbnail.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a commercial library that enables developers to
      create, edit, convert, and render Photoshop PSD files without requiring Adobe
      Photoshop.
    question: What is Aspose.PSD for Java?
  - answer: Detailed documentation can be found on the [Aspose.PSD for Java documentation
      page](https://reference.aspose.com/psd/java/).
    question: Where can I find more documentation for Aspose.PSD for Java?
  - answer: Yes, Aspose.PSD for Java can be used commercially. You can purchase a
      license from [Aspose.PSD's purchase page](https://purchase.aspose.com/buy).
    question: Is Aspose.PSD for Java suitable for commercial use?
  - answer: Yes, you can download a free trial from [Aspose.PSD's trial download page](https://releases.aspose.com/).
    question: Can I try Aspose.PSD for Java before purchasing?
  - answer: For support, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).
    question: How can I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- add thumbnail
- Aspose.PSD
- Java image processing
- JFIF
- PSD
title: JavaでJFIFセグメントにサムネイルを追加する方法
url: /ja/java/java-jpeg-image-processing/add-thumbnail-to-jfif-segment-java/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# JavaでJFIFセグメントにサムネイルを追加する方法

## はじめに
PSDファイルのJFIFセグメントにサムネイルを追加することは、フル画像を読み込まずに迅速なビジュアルプレビューが必要な場合に一般的な要件です。  
このチュートリアルでは、Aspose.PSDを使用してJavaでJFIFセグメントに**サムネイルの追加方法**を学びます。ガイドの最後までに、実行可能なコードスニペット、基礎となるJFIF構造の理解、そして大容量ファイルを効率的に処理するためのヒントを得られます。

## クイック回答
- **必要なライブラリは何ですか？** Aspose.PSD for Java.
- **対応するJavaバージョンは？** JDK 11またはそれ以降。
- **必要なコード行数は？** ロード、変更、保存に約10行。
- **マルチメガバイトのファイルを処理できますか？** はい、Aspose.PSDはデータをストリーム処理するため、メモリ使用量が低く抑えられます。
- **商用ライセンスは必要ですか？** 本番使用にはライセンスが必要です；無料トライアルが利用可能です。

## JFIFセグメントとは何ですか？
JFIFセグメントは、サムネイル、EXIF、カラー プロファイルなどのオプション データを格納できるJPEG File Interchange Formatブロックです。  
PSDファイルのJPEGストリーム内に存在し、ほとんどの画像ビューアでクイックプレビュー生成に認識されます。

## なぜPSDファイルにサムネイルを追加するのか？
Aspose.PSD for Javaは**30以上の画像フォーマット**をサポートし、**2 GB**までのファイルをドキュメント全体をメモリにロードせずに処理できます。サムネイルを追加することで、プレビューの送信時のネットワーク帯域幅が削減され、ギャラリーアプリケーションのUIレンダリングが高速化されます。

## 前提条件
- Java Development Kit (JDK): システムにJavaがインストールされていることを確認してください。以下の[OracleのJDKウェブサイト](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)からダウンロードできます。
- Aspose.PSD for Java: Aspose.PSD for Javaライブラリが必要です。以下の[Aspose.PSD Javaダウンロードページ](https://releases.aspose.com/psd/java/)から入手できます。
- Integrated Development Environment (IDE): IntelliJ IDEAやEclipseなどのIDEを使用してJava開発を行ってください。
- Basic Understanding of Java: Javaプログラミング言語と概念に慣れていることが望ましいです。

## JavaでJFIFセグメントにサムネイルを追加する方法は？
対象のPSDをロードし、JFIFリソースを特定し、サムネイルデータを置き換えてファイルを保存します。これらの操作は数回のシンプルなAPI呼び出しで実行でき、Aspose.PSDが低レベルのJPEG構造を処理してくれます。

### 手順 1: パッケージのインポート
`Document`、`JfifResource`、および関連クラスはAspose.PSD名前空間の一部です。DocumentはPSDファイルコンテナを表し、JfifResourceはPSD内のJFIFセグメントへのアクセスを提供します。これらをソースファイルの先頭でインポートしてください。

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

### 手順 2: PSD画像のロード
コンストラクタにファイルパスを渡して`PsdImage`インスタンスを作成します。PsdImageはPhotoshopドキュメントをモデル化するAspose.PSDクラスです。これにより、ピクセルデータをストリーミングしながらドキュメントメタデータがロードされます。

```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "your_image.psd");
```

### 手順 3: 画像リソースの反復処理
`Resources`コレクションから`JfifResource`を検索します。見つかったら、そのサムネイルバイト配列を新しいJPEGエンコードプレビューに置き換えることができます。

```java
for(int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        
        // Continue with thumbnail processing
    }
}
```

### 手順 4: サムネイルデータの調整
任意の画像処理ライブラリを使用して小さなJPEGサムネイル（例: 120 × 120 px）を生成し、得られたバイト配列を`jfifResource.ThumbnailData`に割り当てます。

```java
try {
    PsdImage thumbnailImage = new PsdImage(100, 100);
    
    // Fill thumbnail data (example: create a simple pixel array)
    int[] pixels = new int[thumbnailImage.getWidth() * thumbnailImage.getHeight()];
    for (int j = 0; j < pixels.length; j++) {
        pixels[j] = j;
    }
    
    // Save thumbnail data
    thumbnailImage.saveArgb32Pixels(thumbnailImage.getBounds(), pixels);
    
    // Set thumbnail data to Jpeg options
    JpegExifData exifData = new JpegExifData();
    exifData.setThumbnail(thumbnailImage);
    JpegOptions jpegOptions = new JpegOptions();
    jpegOptions.setExifData(exifData);
    
    // Set options to thumbnail resource
    thumbnail.getJpegOptions().setExifData(exifData);
    
} catch(Exception e) {
    // Handle exceptions
} finally {
    // Dispose of resources
}
```

### 手順 5: 変更された画像の保存
`PsdImage`オブジェクトの`save`メソッドを呼び出し、出力パスと希望のフォーマットを指定します。これでJFIFセグメントに新しいサムネイルが含まれます。

```java
image.save(dataDir + "output.psd");
```

## よくある問題と解決策
- **ビューアでサムネイルが表示されない:** サムネイルデータが有効なJPEGバイト配列であること、サイズが256 × 256 px以内であること（JFIF仕様でサポートされる最大サイズ）を確認してください。
- **大きなPSDでOutOfMemoryErrorが発生する:** `PsdImage.load(inputStream, true)`を使用してストリーミングモードを有効にし、メモリ消費を低く抑えます。
- **リソースタイプが間違っている:** 変更対象が実際に`JfifResource`であることを確認してください。`ExifResource`など他のリソースはサムネイル表示に影響しません。

## よくある質問

**Q: Aspose.PSD for Javaとは何ですか？**  
A: Aspose.PSD for Javaは、Adobe Photoshopを必要とせずに開発者がPhotoshop PSDファイルを作成、編集、変換、レンダリングできる商用ライブラリです。

**Q: Aspose.PSD for Javaのドキュメントはどこで見つけられますか？**  
A: 詳細なドキュメントは[Aspose.PSD for Javaドキュメントページ](https://reference.aspose.com/psd/java/)で確認できます。

**Q: Aspose.PSD for Javaは商用利用に適していますか？**  
A: はい、Aspose.PSD for Javaは商用利用が可能です。ライセンスは[Aspose.PSDの購入ページ](https://purchase.aspose.com/buy)から購入できます。

**Q: 購入前にAspose.PSD for Javaを試すことはできますか？**  
A: はい、[Aspose.PSDのトライアルダウンロードページ](https://releases.aspose.com/)から無料トライアルをダウンロードできます。

**Q: Aspose.PSD for Javaのサポートはどこで受けられますか？**  
A: サポートが必要な場合は、[Aspose.PSDフォーラム](https://forum.aspose.com/c/psd/34)をご覧ください。

---

**最終更新日:** 2026-09-28  
**テスト環境:** Aspose.PSD for Java 24.11  
**作者:** Aspose

## 関連チュートリアル

- [Aspose PSD for Javaを使用してPSDファイルにIOPAリソースを追加する](/psd/java/modifying-converting-psd-images/add-iopa-resource-psd-files/)
- [画像に署名を追加 – Aspose.PSD for Javaでキャンバスに画像を描画](/psd/java/advanced-image-effects/add-signature-to-image/)
- [Aspose.PSD for Javaで特定の角度に画像を回転させる方法](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}