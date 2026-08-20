---
date: 2026-06-03
description: Aspose.PSD for Java を使用して、PSD を PNG に簡単にディスクへ保存できます。PSD ファイル操作のための強力な
  Java ライブラリです。
keywords:
- save psd as png
- convert psd to png
- export psd to png
- save image file java
linktitle: 画像をディスクに保存
schemas:
- author: Aspose
  dateModified: '2026-06-03'
  description: Effortlessly save PSD as PNG to disk using Aspose.PSD for Java. A powerful
    Java library for PSD file manipulation.
  headline: Save PSD as PNG with Aspose.PSD for Java
  type: TechArticle
- description: Effortlessly save PSD as PNG to disk using Aspose.PSD for Java. A powerful
    Java library for PSD file manipulation.
  name: Save PSD as PNG with Aspose.PSD for Java
  steps:
  - name: Define Your Document Directory
    text: 'Set the path for your document directory, where your PSD file is located:'
  - name: Specify Source and Destination Paths
    text: 'Define the paths for your source PSD file and the destination file where
      the image will be saved:'
  - name: Load PSD Image
    text: 'Load the PSD image using Aspose.PSD:'
  - name: Save Image with Options
    text: '`PsdImage` is Aspose.PSD''s core class that represents a Photoshop document
      in memory. Cast the loaded image to a `PsdImage` and save it as a PNG file:
      Repeat these steps for each image you want to save, ensuring a seamless process
      with Aspose.PSD.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD for Java supports various formats, including JPEG, BMP,
      TIFF, and more.
    question: Can I use Aspose.PSD for Java with other image formats?
  - answer: Yes, you can explore a free trial of Aspose.PSD for Java by visiting [this
      link](https://releases.aspose.com/).
    question: Is there a free trial available for Aspose.PSD for Java?
  - answer: Refer to the [documentation](https://reference.aspose.com/psd/java/) for
      detailed information on Aspose.PSD for Java.
    question: Where can I find comprehensive documentation for Aspose.PSD for Java?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community
      support and discussions.
    question: How can I get support for Aspose.PSD for Java?
  - answer: Yes, you can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java で PSD を PNG に保存
url: /ja/java/advanced-techniques/save-images-to-disk/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java を使用した PSD の PNG への保存

## はじめに

**Save PSD as PNG** は、Java アプリケーションで Photoshop ファイルを扱う際によくある要件です。Aspose.PSD for Java を使用すると、数行のコードで任意の PSD レイヤーまたはドキュメント全体を PNG 画像に変換できます。このチュートリアルでは、正確な手順を解説し、ライブラリがこのタスクに最適な理由を説明し、複数画像を効率的に処理する方法を示します。

## クイック回答
- **PSD から PNG への変換を処理するライブラリは何ですか？** Aspose.PSD for Java.
- **必要なコード行数は何行ですか？** 通常、ファイルのロード後は 2 行です。
- **大きな PSD ファイルを処理できますか？** はい – API はデータをストリーミングし、2 GB を超えるファイルをサポートします。
- **開発にライセンスは必要ですか？** テストには無料トライアルが使用できますが、本番環境ではライセンスが必要です。
- **サポートされている Java バージョンはどれですか？** Java 8 から Java 21（LTS およびそれ以降）まで。

## “save psd as png” とは何ですか？

PSD を PNG として保存することは、Photoshop ドキュメントからラスタ画像データを可搬性のある PNG 形式にエクスポートし、透明性、色の忠実度、埋め込みカラー プロファイルを保持することを意味します。生成された PNG は、Web、モバイル、デスクトップ アプリケーション全般で使用でき、ロスレス圧縮と画像ビューアやエディタとの広範な互換性を提供します。

## PSD を PNG に変換するために Aspose.PSD for Java を使用する理由

Aspose.PSD は **30+ input and output formats** をサポートし、ドキュメント全体をメモリに読み込むことなく **process files up to 2 GB** を処理でき、手動のピクセル操作と比較して最大 **3× faster conversion** を実現します。ライブラリはレイヤー効果、マスク、カラー プロファイルも自動的に保持するため、ポストプロセッシングの必要がなくなります。

## 前提条件

チュートリアルに入る前に、以下の前提条件が整っていることを確認してください：

- Aspose.PSD for Java ライブラリ: ライブラリは [release page](https://releases.aspose.com/psd/java/) からダウンロードしてインストールしてください。
- Java 開発環境: マシン上に機能する Java 開発環境が設定されていることを確認してください。

## パッケージのインポート

以下のインポートは、PSD ファイルの読み込みと PNG エクスポートオプションの設定に必要な Aspose.PSD のコアクラスを導入します。  
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

画像を保存するプロセスを複数のステップに分解し、明確かつ包括的に理解できるようにしましょう。

## Aspose.PSD for Java を使用して PSD を PNG として保存する方法？

`PsdImage` クラスはメモリ内の Photoshop ドキュメントを表し、`ImageSaveOptions` と `SaveFormat` を組み合わせて目的の出力形式と圧縮設定を指定します。PSD を読み込み、PNG オプションで save メソッドを呼び出すだけで、ファイルを単一の効率的な呼び出しで変換できます。  

`new PsdImage("source.psd")` で PSD ファイルをロードし、`psd.save("output.png", ImageSaveOptions.createSaveOptions(SaveFormat.Png))` を呼び出します。このワンラインの呼び出しはレイヤーのフラット化、カラー プロファイルの保持、PNG 圧縮を自動的に処理します。バッチ処理の場合は、ソースファイルごとにループ内でこの呼び出しを行ってください。

### 手順 1: ドキュメント ディレクトリの定義

PSD ファイルが配置されているドキュメント ディレクトリのパスを設定します：

```java
String dataDir = "Your Document Directory";
```

### 手順 2: ソースと出力パスの指定

ソース PSD ファイルと、画像を保存する先の出力ファイルのパスを定義します：

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "result.png";
```

### 手順 3: PSD 画像の読み込み

Aspose.PSD を使用して PSD 画像を読み込みます：

```java
Image image = Image.load(sourceFile);
```

### 手順 4: オプション付きで画像を保存

`PsdImage` は、メモリ内の Photoshop ドキュメントを表す Aspose.PSD のコアクラスです。読み込んだ画像を `PsdImage` にキャストし、PNG ファイルとして保存します：

```java
PsdImage psdImage = (PsdImage)image;
psdImage.save(destName, new PngOptions());
```

保存したい各画像についてこれらの手順を繰り返すことで、Aspose.PSD によるシームレスな処理が実現します。

## よくある問題と解決策

- **OutOfMemoryError on large files** – `PsdImage.load(inputStream, true)` を使用してストリーミングを有効にし、ファイル全体を RAM に読み込むのを回避します。
- **Missing transparency** – アルファチャンネルを保持するために、`ColorType = PngColorType.Rgba` を設定した `PngOptions` を使用してください。
- **Incorrect colors** – ソース PSD にカラー プロファイルが埋め込まれていることを確認してください。Aspose.PSD はエクスポート時に自動的に適用します。

## よくある質問

**Q: Aspose.PSD for Java を他の画像形式でも使用できますか？**  
A: はい、Aspose.PSD for Java は JPEG、BMP、TIFF などさまざまな形式をサポートしています。

**Q: Aspose.PSD for Java の無料トライアルは利用可能ですか？**  
A: はい、[this link](https://releases.aspose.com/) にアクセスして Aspose.PSD for Java の無料トライアルをご利用いただけます。

**Q: Aspose.PSD for Java の包括的なドキュメントはどこで見つけられますか？**  
A: 詳細情報は [documentation](https://reference.aspose.com/psd/java/) を参照してください。

**Q: Aspose.PSD for Java のサポートはどのように受けられますか？**  
A: コミュニティサポートやディスカッションは [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) をご覧ください。

**Q: Aspose.PSD for Java の一時ライセンスは利用可能ですか？**  
A: はい、[here](https://purchase.aspose.com/temporary-license/) から一時ライセンスを取得できます。

**Q: ライブラリは単一レイヤーを PNG としてエクスポートすることをサポートしていますか？**  
A: もちろんです。目的の `Layer` オブジェクトを取得し、`layer.save("layer.png", ImageSaveOptions.createSaveOptions(SaveFormat.Png))` を呼び出してください。

**Q: PNG の圧縮レベルを制御できますか？**  
A: はい、`PngOptions.setCompressionLevel(int level)` で圧縮レベルを設定できます。`level` は 0（圧縮なし）から 9（最大圧縮）までの範囲です。

## 結論

Aspose.PSD for Java を使用した PSD の PNG への保存は、シンプルでありながら強力な操作です。上記の手順に従うことで、Java アプリケーションに高性能な画像エクスポートを組み込み、大きなファイルを効率的に処理し、完全なビジュアル忠実度を維持できます。

---

**最終更新日:** 2026-06-03  
**テスト環境:** Aspose.PSD 24.10 for Java  
**作者:** Aspose

## 関連チュートリアル

- [Aspose.PSD for Java を使用した PSD のラスタ画像形式への変換](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [Aspose.PSD for Java を使用した画像のストリームへの保存](/psd/java/advanced-techniques/save-images-to-stream/)
- [Aspose.PSD for Java で PSD を PNG として保存し、レンダリングドロップシャドウを適用](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}