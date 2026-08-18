---
date: 2026-03-26
description: Aspose.PSD for Java を使用して PSD レイヤーを PNG にエクスポートする方法を学びましょう。PSD をラスタ画像に変換し、PSD
  レイヤーを効率的にバッチエクスポートできます。
linktitle: Export psd layers to png using Java
second_title: Aspose.PSD Java API
title: JavaでPSDレイヤーをPNGにエクスポート
url: /ja/java/psd-image-modification-conversion/export-psd-layers-raster-images/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java を使用した PSD レイヤーの PNG へのエクスポート

## Introduction

デジタルデザインの世界では、レイヤー化された画像を扱うことは大きな利点であると同時に課題でもあります。Photoshop（PSD 形式）で何時間もかけて作成した、複数のレイヤーで構成された素晴らしい画像を想像してください。今、その各レイヤーを **export psd layers to png** として個別にエクスポートしたいとします。ここで Aspose.PSD for Java が活躍し、PSD ファイル内の各レイヤーを高品質なラスタ画像（PNG など）に変換する手間のかかる作業を自動化します。本稿では、環境構築から数行のコードで PSD レイヤーをバッチエクスポートするまでの全工程を詳しく解説します。

## Quick Answers
- **What does the tutorial cover?** Aspose.PSD for Java を使用して各 PSD レイヤーを PNG ファイルにエクスポートする方法。  
- **Primary benefit?** 手動で Photoshop から抽出する場合に比べて数時間の作業時間を短縮できます。  
- **Prerequisites?** JDK 8 以上、Aspose.PSD ライブラリ、サンプル PSD ファイル。  
- **Can I export to other raster formats?** はい – BMP、TIFF、JPEG などのラスタ形式にも変換可能です。  
- **Is batch processing supported?** もちろんです。コード内のループで PSD レイヤーを一括エクスポートできます。

## What is “psd layers to png”?
**psd layers to png** のエクスポートとは、Photoshop ドキュメントから個々のレイヤーを取り出し、別々の PNG 画像として保存することを指します。PNG は透過情報を保持できるため、ウェブグラフィックや UI アセット、さらなる画像処理に最適です。

## Why use Aspose.PSD for Java?
- **No Photoshop required** – 任意のサーバーや CI 環境で動作します。  
- **High fidelity** – レイヤー効果、マスク、アルファチャンネルを保持します。  
- **Scalable** – 自動化パイプラインでのバッチエクスポートに最適です。  

## Prerequisites

コードに取り掛かる前に、以下を用意してください。

1. **Java Development Kit (JDK)** – バージョン 8 以上。  
2. **Aspose.PSD for Java** – 最新ライブラリは [Aspose Releases](https://releases.aspose.com/psd/java/) からダウンロードしてください。  
3. **IDE** – IntelliJ IDEA、Eclipse、またはお好みのエディタ。  
4. **Sample PSD file** – 例: `sample.psd` をプロジェクトフォルダーに配置します。

準備が整ったら、さっそくコーディングを始めましょう！

## Import Packages

まず、Aspose.PSD ライブラリから必要なクラスをインポートします。

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

これらのインポートにより、画像の読み込み、PNG オプション、レイヤー操作が可能になります。

## Step 1: Define Your Document Directory

ソース PSD と出力 PNG が格納されるディレクトリを指定します。

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` を `sample.psd` が存在する絶対パスまたは相対パスに置き換えてください。

## Step 2: Load the PSD File

PSD を `PsdImage` オブジェクトにロードし、レイヤーにアクセスできるようにします。

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "sample.psd");
```

`PsdImage` にキャストすることで、レイヤー固有の機能が利用可能になります。

## Step 3: Configure PNG Options

PNG エクスポート時のパラメータを設定します。`TruecolorWithAlpha` を使用すると透過情報が保持されます。

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

## Step 4: Loop Through Layers and Export Each One

すべてのレイヤーを走査し、個別の PNG ファイルとして保存します。このループにより **batch export psd layers** が自動的に実行されます。

```java
for (int i = 0; i < psdImage.getLayers().length; i++) {
    // Convert and save the layer to PNG file format.
    psdImage.getLayers()[i].save(dataDir + String.format("layer_out%d.png", i + 1), pngOptions);
}
```

各イテレーションで `layer_out1.png`、`layer_out2.png` といったファイルが生成されます。

## Common Issues and Solutions

- **FileNotFoundException** – `dataDir` が正しいフォルダーを指しているか、`sample.psd` が存在するか確認してください。  
- **OutOfMemoryError** – 非常に大きな PSD ファイルの場合、レイヤーを小分けに処理するか、JVM のヒープサイズ（`-Xmx`）を増やしてください。  
- **Missing Transparency** – `pngOptions.setColorType(PngColorType.TruecolorWithAlpha)` が設定されていることを確認してください。設定しないとアルファチャンネルなしで PNG が保存されます。

## Frequently Asked Questions

### What is Aspose.PSD for Java?
Aspose.PSD for Java は、Adobe Photoshop を必要とせずに Photoshop ファイルの作成、変更、変換、レンダリングを可能にする強力なライブラリです。

### Can I export layers to formats other than PNG?
はい、Aspose.PSD は BMP、TIFF、JPEG など多数のラスタ形式をサポートしています。対応するオプションクラス（例: `JpegOptions`）をインスタンス化し、`save` メソッドに渡すだけです。

### Is there a free trial available for Aspose.PSD?
もちろんです！[free trial page](https://releases.aspose.com/) から無料でダウンロードしてお試しいただけます。

### What if I encounter issues while using Aspose.PSD?
Aspose コミュニティでサポートを受けられます。フォーラムは [here](https://forum.aspose.com/c/psd/34) でご利用ください。

### Where can I purchase a license for Aspose.PSD?
ライセンスは購入ページ [here](https://purchase.aspose.com/buy) から簡単にご購入いただけます。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-03-26  
**Tested With:** Aspose.PSD for Java 24.12 (latest)  
**Author:** Aspose