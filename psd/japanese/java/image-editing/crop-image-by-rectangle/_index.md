---
date: 2026-01-01
description: Aspose.PSD for Java を使用した Java での画像トリミング方法を探求しましょう。ステップバイステップのガイドに従って、PSD
  ファイルを読み込み、画像の矩形をトリミングし、PSD を JPEG に変換します。
linktitle: Crop Image by Rectangle
second_title: Aspose.PSD Java API
title: 'Javaで画像をトリミング: Aspose.PSDで矩形による画像の切り抜き'
url: /ja/java/image-editing/crop-image-by-rectangle/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crop Image Java: Aspose.PSD を使用した矩形での画像トリミング

## Introduction

グラフィックの操作は **java image processing** の日常的な作業であり、Aspose.PSD for Java は PSD ファイルを扱うためのクリーンで高性能な API を提供します。このチュートリアルでは、矩形を使用して **画像をトリミング** する方法、PSD ファイルの読み込み、そして最終的に結果を JPEG に変換する方法を、数行の Java コードだけで学びます。

## Quick Answers
- **“crop image java” とは何ですか？** Java コードで定義された矩形に画像をトリミングすることを指します。  
- **どのライブラリがこの操作を処理しますか？** Aspose.PSD for Java が必要なクラスを提供します。  
- **テストにライセンスは必要ですか？** 無料トライアルが利用可能です。製品版ではライセンスが必要です。  
- **トリミングした PSD を JPEG に変換できますか？** はい、保存時に `JpegOptions` を使用します。  
- **実装にどれくらい時間がかかりますか？** 基本的なシナリオでは通常 10 分未満です。

## What is cropping an image rectangle in Java?

画像の矩形トリミングとは、X、Y、幅、高さで定義された特定領域を選択し、その領域外のすべてを破棄することです。この操作は、より大きな PSD ドキュメントの中から特定の領域にフォーカスしたい場合に一般的に使用されます。

## Why use Aspose.PSD for this task?

- **外部依存関係が不要** – 純粋な Java だけで動作します。  
- **PSD、PNG、JPEG など多数のフォーマットに対応** – **PSD を JPEG に変換** も即座に行えます。  
- **高忠実度レンダリング** – トリミング中もレイヤー情報やカラープロファイルを保持します。  

## Prerequisites

- Java Development Kit (JDK) がインストールされていること。  
- Aspose.PSD for Java ライブラリ – [website](https://releases.aspose.com/psd/java/) からダウンロードしてください。  

## Import Packages

Aspose.PSD for Java の機能を活用できるよう、Java プロジェクトに必要なパッケージを必ずインポートしてください。Java ファイルの先頭に以下のインポート文を追加します。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

Now, let's break down the process into multiple steps to guide you through cropping an image by a rectangle using Aspose.PSD for Java.

## Step 1: Set up Your Document Directory

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` を PSD ファイルが実際に保存されているパスに置き換えてください。

## Step 2: Specify Source and Destination Files

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "CroppingByRectangle_out.jpg";
```

ソース PSD ファイルと出力先 JPEG ファイルのパスを定義します。

## Step 3: Load and Cache the Image

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);

if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

ここでは **PSD ファイルを** `RasterImage` インスタンスに **ロード** し、パフォーマンス向上のためにデータをキャッシュします。

## Step 4: Create and Define the Crop Rectangle

```java
Rectangle rectangle = new Rectangle(20, 20, 20, 20);
```

`Rectangle` クラスのインスタンスを作成し、トリミングしたいサイズを指定します。パラメータはそれぞれ **X**、**Y**、幅、高さ を表します。

## Step 5: Crop and Save the Image

```java
rasterImage.crop(rectangle);
rasterImage.save(destName, new JpegOptions());
```

指定した矩形でトリミングを実行し、`JpegOptions` を使用して **PSD を JPEG に変換** して結果を保存します。

必要に応じてこれらの手順を繰り返し、パラメータを目的に合わせて調整してください。

## Common Issues & Tips

- **矩形が画像範囲外** – 矩形の座標がソース画像のサイズ内に収まっていることを確認してください。  
- **メモリ消費** – 終了時に `rasterImage.dispose()` を呼び出してネイティブリソースを解放します。  
- **品質管理** – `JpegOptions.setQuality(int)` で出力 JPEG の圧縮レベルを調整できます。

## Conclusion

このチュートリアルでは、Aspose.PSD for Java を使用して **crop image java** を矩形で実行する手順を解説しました。これらの手順に従うことで、PSD ファイルの読み込み、特定領域のトリミング、JPEG への変換という強力な画像操作機能を任意の Java アプリケーションに簡単に組み込むことができます。

## FAQ's

### Q1: Can I use Aspose.PSD for Java with other Java frameworks?

A1: Yes, Aspose.PSD for Java can be integrated with various Java frameworks, providing flexibility in your development projects.

### Q2: Is there a free trial available for Aspose.PSD for Java?

A2: Yes, you can access the free trial version [here](https://releases.aspose.com/).

### Q3: Where can I find additional support or assistance?

A3: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community support and discussions.

### Q4: How do I obtain a temporary license for Aspose.PSD for Java?

A4: You can acquire a temporary license [here](https://purchase.aspose.com/temporary-license/).

### Q5: What are the supported image formats for cropping in Aspose.PSD for Java?

A5: Aspose.PSD for Java supports various image formats, including PSD, PNG, JPEG, and more.

---

**Last Updated:** 2026-01-01  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}