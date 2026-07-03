---
date: 2026-07-03
description: Aspose.PSD for Java を使用して Java で画像をクロップする方法を学びます。このステップバイステップの画像クロップチュートリアルでは、PSD
  ファイルの読み込み、シフト値の設定、結果の保存について解説します。
keywords:
- crop image java
- how to crop image
- load psd file
- java image processing
- crop image left right
linktitle: シフトで画像をクロップ
schemas:
- author: Aspose
  dateModified: '2026-07-03'
  description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  headline: Crop Image Java by Shifts with Aspose.PSD
  type: TechArticle
- description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  name: Crop Image Java by Shifts with Aspose.PSD
  steps:
  - name: Load the Image
    text: '`Image` is the base class for all image types in Aspose.PSD. `RasterImage`
      represents a raster image and provides cropping capabilities.'
  - name: Cache Image Data
    text: '`cacheData()` loads the image data into memory for faster processing.'
  - name: Define Shift Values
    text: Specify the shift values for all four sides of the image (left, top, right,
      bottom) in pixels.
  - name: Apply Cropping
    text: '`crop(left, right, top, bottom)` trims the image by the specified pixel
      shifts on each side.'
  - name: Save the Results
    text: '`JpegOptions` defines JPEG encoding settings such as quality and color
      profile. Congratulations! You''ve successfully cropped an image using Aspose.PSD
      for Java.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports over 30 raster formats, including PSD, JPEG,
      PNG, BMP, TIFF, and GIF, ensuring broad compatibility.
    question: Is Aspose.PSD compatible with all image formats?
  - answer: Absolutely. After each `crop` call you receive a new image object, which
      you can crop again as needed.
    question: Can I apply multiple cropping operations to the same image?
  - answer: Yes, you can find support and engage with the community at [Aspose.PSD
      Forum](https://forum.aspose.com/c/psd/34).
    question: Is there a community forum for Aspose.PSD support?
  - answer: Visit [here](https://purchase.aspose.com/temporary-license/) to obtain
      a temporary license.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Explore the documentation and examples at [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).
    question: Are there sample projects showcasing Aspose.PSD functionalities?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Aspose.PSD を使用したシフトで画像をクロップ（Java）
url: /ja/java/image-editing/crop-image-by-shifts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD を使用したシフトによる画像のクロップ（Java）

## はじめに

Java の画像処理において、**crop image java** はグラフィック、サムネイル、UI アセットの準備に頻繁に必要とされます。Aspose.PSD for Java は、サポートされているラスタ形式で動作するシンプルな `crop` メソッドを提供し、このタスクを簡単にします。このチュートリアルでは、PSD ファイルの読み込み、左‑右‑上‑下のシフト値の定義、クロップの適用、結果の保存を学びます—カスタムのピクセル操作コードを書く必要はありません。

## クイック回答
- **どのライブラリがクロップを処理しますか？** Aspose.PSD for Java は組み込みの `crop` メソッドを提供します。  
- **ライセンスは必要ですか？** 評価用には一時ライセンスで動作しますが、本番環境では正式ライセンスが必要です。  
- **サポートされている形式は？** PSD、JPEG、PNG、BMP、TIFF など、30 以上のラスタ形式をサポートしています。  
- **最大ファイルサイズは？** 画像全体をメモリに読み込まずに、最大 2 GB のファイルを処理できます。  
- **コード行数は？** ロード、キャッシュ、シフト定義、クロップ、保存の 5 つの論理ステップだけです。

## crop image java とは？
`crop image java` は Java アプリケーションでビットマップをトリミングする操作を指します。Aspose.PSD を使用すると、この操作は `crop` メソッドで実行され、画像の各側のシフト値を受け取り、新しい画像インスタンスを返します。

## 画像クロップに Aspose.PSD を使用する理由
Aspose.PSD は **30 以上** の画像形式をサポートし、レイジーローディング アーキテクチャにより 150 MB 未満の RAM で数百ページに及ぶ PSD ファイルを処理できます。また、ピクセル単位で完全な結果を保証し、レイヤー、マスク、カラープロファイルを保持します—多くの汎用画像ライブラリでは保証できない点です。

## 前提条件

### Java Development Kit (JDK)

システムに最新バージョンの JDK がインストールされていることを確認してください。ダウンロードは [here](https://www.oracle.com/java/technologies/javase-downloads.html) から行えます。

### Aspose.PSD for Java ライブラリ

まず、Aspose.PSD for Java ライブラリを入手する必要があります。[download page](https://releases.aspose.com/psd/java/) から最新バージョンを取得してください。

### 統合開発環境 (IDE)

Eclipse や IntelliJ など、お好みの Java IDE を選択して、スムーズなコーディング体験を実現してください。

## crop image java の手順

ソースファイルを読み込み、各側のピクセルシフトを定義し、`crop` メソッドを呼び出します—この一連の作業は 5 行の簡潔なコードで記述できます。`crop` 操作は、指定した領域のみを含む新しい画像を作成し、元のファイルは変更されません。

### 手順 1: 画像の読み込み

`Image` は Aspose.PSD のすべての画像タイプの基底クラスです。  
`RasterImage` はラスタ画像を表し、クロップ機能を提供します。  
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

### 手順 2: 画像データのキャッシュ

`cacheData()` は画像データをメモリにロードし、処理を高速化します。  
```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
```

### 手順 3: シフト値の定義

画像の四辺（左、上、右、下）のシフト値をピクセル単位で指定します。  
```java
if (!rasterImage.isCached()) {
  rasterImage.cacheData();
}
```

### 手順 4: クロップの適用

`crop(left, right, top, bottom)` は各側の指定されたピクセルシフトで画像をトリミングします。  
```java
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

### 手順 5: 結果の保存

`JpegOptions` は品質やカラープロファイルなどの JPEG エンコード設定を定義します。  
```java
rasterImage.crop(leftShift, rightShift, topShift, bottomShift);
```

おめでとうございます！Aspose.PSD for Java を使用して画像のクロップに成功しました。

## よくある問題と解決策

- **画像が変わらない場合:** シフト値が正の数であり、元の寸法を超えていないことを確認してください。  
- **大きなファイルで OutOfMemoryError が発生する場合:** 手順 2 のようにキャッシュを有効にしてください。これにより、Aspose.PSD は画像全体を RAM に保持せず、一時ファイルを使用します。  
- **クロップ後に色が変わる場合:** 正確な色再現が必要な場合は、`image.save(..., new JpegOptions { ColorProfile = image.ColorProfile })` を呼び出してカラープロファイルを保持してください。

## よくある質問

**Q: Aspose.PSD はすべての画像形式に対応していますか？**  
A: はい、Aspose.PSD は PSD、JPEG、PNG、BMP、TIFF、GIF など、30 以上のラスタ形式をサポートし、幅広い互換性を提供します。

**Q: 同じ画像に複数回のクロップ操作を適用できますか？**  
A: もちろんです。各 `crop` 呼び出しの後に新しい画像オブジェクトが返され、必要に応じて再度クロップできます。

**Q: Aspose.PSD のサポート用コミュニティフォーラムはありますか？**  
A: はい、[Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) でサポートを受け、コミュニティと交流できます。

**Q: Aspose.PSD の一時ライセンスはどこで取得できますか？**  
A: [here](https://purchase.aspose.com/temporary-license/) から一時ライセンスを取得してください。

**Q: Aspose.PSD の機能を示すサンプルプロジェクトはありますか？**  
A: [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/) でドキュメントとサンプルを確認してください。

---

**最終更新日:** 2026-07-03  
**テスト環境:** Aspose.PSD 24.11 for Java  
**作者:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
String destName = dataDir + "CroppingByShifts_out.jpg";
rasterImage.save(destName, new JpegOptions());
```

## 関連チュートリアル

- [Aspose.PSD for Java で矩形による画像のクロップ](/psd/java/image-editing/crop-image-by-rectangle/)
- [Crop Image Java - Aspose.PSD for Java で画像を拡張およびクロップ](/psd/java/image-editing/expand-and-crop-images/)
- [Resize Image Java - Aspose.PSD for Java の Resize Type 列挙体を使用](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}