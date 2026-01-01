---
date: 2026-01-01
description: Aspose.PSD for Java を使用して XMP メタデータの作成方法、PSD ファイルへの XMP の追加方法、画像メタデータの更新方法を学びましょう。今すぐこのステップバイステップ
  ガイドをご覧ください。
linktitle: Create XMP Metadata
second_title: Aspose.PSD Java API
title: Aspose.PSD for JavaでXMPメタデータを作成する
url: /ja/java/image-editing/create-xmp-metadata/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java を使用した XMP メタデータの作成

## Introduction

Photoshop（PSD）ファイルを扱う Java 開発者にとって、画像メタデータの管理は一般的な要件です。このチュートリアルでは **XMP メタデータの作成方法** を Aspose.PSD ライブラリを使って学び、PSD 画像に XMP を追加し、プログラムで画像メタデータを更新する方法を紹介します。各ステップを順に解説し、なぜそれが重要かを説明し、実際のプロジェクトで活用できる実践的なヒントを提供します。

## Quick Answers
- **XMP メタデータとは何ですか？** 画像ファイル内に記述情報（作者、キーワードなど）を埋め込むための標準化されたフォーマットです。  
- **Aspose.PSD を使用する理由は？** Photoshop を使用せずに PSD ファイルの作成、読み取り、編集が可能な純粋な Java API を提供します。  
- **既存の PSD に XMP を追加できますか？** はい – `setXmpData` を使用してリアルタイムで画像メタデータを更新できます。  
- **主な手順は何ですか？** 画像サイズの設定、ヘッダー/トレーラーの作成、XMP パッケージの構築、添付、保存です。  
- **ライセンスは必要ですか？** 開発には無料トライアルで動作しますが、本番環境では商用ライセンスが必要です。

## What is “create XMP metadata” in Java?

Java で XMP メタデータを作成するとは、画像を記述する XMP パケット（ヘッダー、本文、トレーラー）を構築し、そのパケットを PSD ファイルに埋め込むことを意味します。Aspose.PSD ライブラリは低レベルの詳細を抽象化し、保存したい内容に集中できるようにします。

## Why add XMP to PSD files?

- **検索性:** 作者、タイトル、カスタムタグに基づく強力なアセット管理検索を可能にします。  
- **相互運用性:** XMP は Adobe 製品、Lightroom、そして多くの DAM システムで認識されます。  
- **バージョン管理:** 処理履歴（例: 市、カラーモード）をファイル内に直接保存します。

## Prerequisites

- **Java 開発環境:** JDK 8 以上がインストールされ、Java の基本的な理解があること。  
- **Aspose.PSD ライブラリ:** Aspose.PSD for Java ライブラリをダウンロードして設定します。ライブラリと詳細なドキュメントは[こちら](https://reference.aspose.com/psd/java/)にあります。  
- **ドキュメントディレクトリ:** システム上で PSD ファイルを読み書きする場所を決定してください。

## Import Packages

Java プロジェクトで Aspose.PSD の機能を利用するために必要なパッケージをインポートします。

```java
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.system.io.MemoryStream;
import com.aspose.psd.xmp.XmpHeaderPi;
import com.aspose.psd.xmp.XmpMeta;
import com.aspose.psd.xmp.XmpPacketWrapper;
import com.aspose.psd.xmp.XmpTrailerPi;
import com.aspose.psd.xmp.schemas.dublincore.DublinCorePackage;
import com.aspose.psd.xmp.schemas.photoshop.ColorMode;
import com.aspose.psd.xmp.schemas.photoshop.PhotoshopPackage;
```

## Step 1: Specify Image Size

まず、新しい PSD 画像のキャンバスサイズを定義します。

```java
// Specify the size of the image by defining a Rectangle
Rectangle rect = new Rectangle(0, 0, 100, 200);
```

## Step 2: Create a New Image

後で XMP メタデータで拡張するための空白の PSD 画像を作成します。

```java
// Create a brand new image for sample purposes
PsdImage image = new PsdImage(rect.getWidth(), rect.getHeight());
```

## Step 3: Create XMP Header

ヘッダーには、XML 処理指示の開始部とドキュメントを識別する GUID が含まれます。

```java
// Create an instance of XMP-Header
XmpHeaderPi xmpHeader = new XmpHeaderPi();
xmpHeader.setGuid("Your Document Directory");
```

## Step 4: Create XMP Trailer

トレーラーは XMP パケットの終了を示します。`true` フラグを設定すると、閉じる処理指示が書き込まれます。

```java
// Create an instance of Xmp-TrailerPi 
XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## Step 5: Create XMP Metadata

作者や説明などの汎用属性をコア XMP メタデータオブジェクトに追加します。

```java
// Create an instance of XMPmeta class to set different attributes
XmpMeta xmpMeta = new XmpMeta();
xmpMeta.addAttribute("Author", "Mr Smith");
xmpMeta.addAttribute("Description", "The fake metadata value");
```

## Step 6: Create XMP Packet Wrapper

ヘッダー、トレーラー、コアメタデータを単一のパケットにラップし、画像に添付できるようにします。

```java
// Create an instance of XmpPacketWrapper that contains all metadata
XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## Step 7: Set Photoshop Attributes

多くの Adobe ツールが期待する Photoshop 固有のフィールド（都市、国、カラーモード）を設定します。

```java
// Create an instance of Photoshop package and set Photoshop attributes
PhotoshopPackage photoshopPackage = new PhotoshopPackage();
photoshopPackage.setCity("London");
photoshopPackage.setCountry("England");
photoshopPackage.setColorMode(ColorMode.Rgb);
```

## Step 8: Add Photoshop Package to XMP Metadata

Photoshop パッケージを XMP パケットに添付します。

```java
// Add Photoshop package into XMP metadata
xmpData.addPackage(photoshopPackage);
```

## Step 9: Set DublinCore Attributes

作者、タイトル、カスタム movie タグなどの Dublin Core メタデータを追加します。

```java
// Create an instance of DublinCore package and set DublinCore attributes
DublinCorePackage dublinCorePackage = new DublinCorePackage();
dublinCorePackage.setAuthor("Charles Bukowski");
dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
dublinCorePackage.addValue("dc:movie", "Barfly");
```

## Step 10: Add DublinCore Package to XMP Metadata

既存の XMP パケットに Dublin Core パッケージを組み合わせます。

```java
// Add DublinCore Package into XMP metadata
xmpData.addPackage(dublinCorePackage);
```

## Step 11: Update XMP Metadata into Image

これで完全な XMP パケットを PSD 画像に埋め込みます。

```java
// Update XMP metadata into the image
image.setXmpData(xmpData);
```

## Step 12: Save Image

最後に、メタデータが永続化されるように PSD ファイルをディスク（またはメモリストリーム）に書き込みます。

```java
// Save the image on the disk or in a memory stream
image.save("Your Document Directory" + "create_XMP_Metadata.psd");
```

## Common Issues and Solutions

| Issue | Why it Happens | Fix |
|-------|----------------|-----|
| **`setXmpData` での NullPointerException** | XMP パケットが完全に構築されていません（ヘッダー/トレーラーが欠如）。 | `XmpHeaderPi`、`XmpTrailerPi` を作成し、`setXmpData` を呼び出す前にすべてのパッケージを追加していることを確認してください。 |
| **Metadata not visible in Photoshop** | Photoshop は XMP パケットが正しくラップされていることを期待します。 | `XmpTrailerPi(true)` が使用され、パケットが画像と共に保存されていることを確認してください。 |
| **File path errors** | 適切な権限なしで相対パスを使用しています。 | 絶対パスを使用するか、アプリケーションが対象フォルダーへの書き込み権限を持っていることを確認してください。 |

## Frequently Asked Questions

**Q: Aspose.PSD はさまざまな画像フォーマットに対応していますか？**  
A: はい、Aspose.PSD は PSD、PSB、BMP、GIF、JPEG、PNG、TIFF など多数のフォーマットをサポートしており、フォーマット間の柔軟性を提供します。

**Q: Aspose.PSD を使用して既存のメタデータを操作できますか？**  
A: もちろんです。既存の PSD をロードし、`getXmpData()` で XMP データを取得し、パケットを変更して再保存できます。

**Q: Aspose.PSD が扱える画像サイズに制限はありますか？**  
A: Aspose.PSD は大きな画像（数ギガピクセルまで）を扱えるよう設計されており、利用可能なメモリが唯一の制限です。

**Q: Aspose.PSD のトライアル版はありますか？**  
A: はい、無料トライアルは[こちら](https://releases.aspose.com/)から入手できます。

**Q: Aspose.PSD に関する質問はどこでサポートを受けられますか？**  
A: サポートや質問は[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34)をご利用ください。

## Conclusion

あなたは今、**XMP メタデータの作成方法** をマスターし、PSD に XMP を追加し、Aspose.PSD for Java を使って画像メタデータを更新できるようになりました。これらの手順により、画像に埋め込まれた記述情報を完全にコントロールでき、検索可能にし、下流のワークフローに備えることができます。ぜひ追加の XMP スキーマを試したり、このコードを大規模な画像処理パイプラインに統合したりしてください。

---

**Last Updated:** 2026-01-01  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}