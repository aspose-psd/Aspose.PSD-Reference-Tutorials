---
date: 2025-12-10
description: Aspose.PSD for Java を使用して PSD レイヤーを抽出し、PSD レイヤーを PNG に変換する方法を学びましょう。堅牢なグラフィック操作が必要な開発者に最適です。
linktitle: Extract PSD Layers and Add Layer Support for PSD Files using Aspose.PSD
  Java
second_title: Aspose.PSD Java API
title: Aspose.PSD Java を使用して PSD ファイルのレイヤーを抽出し、レイヤーサポートを追加する
url: /ja/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD Java を使用した PSD レイヤーの抽出とレイヤーサポートの追加

## Introduction
Photoshop Document（PSD）ファイルの取り扱いは、グラフィックデザイナーも開発者も日常的に直面する課題です。最も一般的な作業のひとつは **PSD レイヤーの抽出** であり、これによりレイヤーを編集したり再利用したり、PNG などの他フォーマットに変換したりできます。Java アプリケーションでは Aspose.PSD がこのプロセスをシンプルかつコードフレンドリーにします。本チュートリアルでは、PSD レイヤーを抽出しレイヤーサポートを有効にし、**PSD レイヤーを PNG に変換**するために必要な手順を順を追って解説し、実用的なヒントも提供します。

## Quick Answers
- **「extract PSD layers」とは何ですか？** PSD ファイルを読み込み、個々のレイヤーにアクセスして操作またはエクスポートできるようにすることです。  
- **Java でこれを扱うライブラリはどれですか？** Aspose.PSD for Java が Photoshop を必要とせずにフル機能の PSD 処理を提供します。  
- **PSD レイヤーを一括で PNG に変換できますか？** はい。適切なオプションでファイルを読み込み、透過性を保持した PNG オプションで保存すれば可能です。  
- **本番環境で使用するにはライセンスが必要ですか？** 本番利用には商用ライセンスが必要です。評価用の無料トライアルも用意されています。  
- **必要な Java バージョンは？** JDK 8 以上（本チュートリアルは JDK 11 を例に使用）。

## What is “extract PSD layers”?
PSD レイヤーの抽出とは、PSD ファイル内部の構造を読み取り、各レイヤーを独立した画像オブジェクトとして取得することです。これにより、レイヤーを個別に編集、非表示、並び替え、エクスポートでき、デザイナーが Photoshop で行う操作をプログラム上で実現できます。

## Why extract PSD layers and convert them to PNG?
- **Reuse assets:** マスタ PSD からアイコンやボタン、UI 要素を手動でエクスポートせずに取得できます。  
- **Automation:** サムネイルや Web 用画像をリアルタイムで自動生成できます。  
- **Preserve transparency:** PNG はアルファチャンネルを保持するため、Web グラフィックに最適です。

## Prerequisites
本格的に取り組む前に、以下を準備してください。

1. **Java Development Environment** – JDK がインストールされていること。ダウンロードは [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) から。  
2. **Aspose.PSD for Java** – 公式ダウンロードページから最新ライブラリを取得してください [here](https://releases.aspose.com/psd/java/)。  
3. **Basic Java knowledge** – Java プログラムのコンパイルと実行に慣れていること。  
4. **IDE** – IntelliJ IDEA、Eclipse、またはお好みのエディタ。  
5. **A PSD file** – 任意の PSD を使用するか、テスト用にサンプル PSD をダウンロードしてください。

これらが揃えば、PSD レイヤーの抽出を開始できます。

## Import Packages
まず、Aspose.PSD ライブラリから必要なクラスをインポートします。

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## Step 1: Define Your Directories
ソース PSD と出力 PNG のパスを設定します。`dataDir` を実際のフォルダに合わせて調整してください。

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "layers.psd";
String output = dataDir + "layers.png";
```

- `dataDir` – `"Your Document Directory"` を実際のフォルダパスに置き換えます。  
- `sourceFileName` – 処理対象の PSD のフルパス。  
- `output` – 抽出されたレイヤーを含む PNG の出力先パス。

## Step 2: Set Up the Load Options
`PsdLoadOptions` を設定して、レイヤー効果やリソースが正しく読み込まれるようにします。これは **extract PSD layers** を行う際に重要です。

```java
PsdLoadOptions imageLoadOptions = new PsdLoadOptions();
imageLoadOptions.setLoadEffectsResource(true);
imageLoadOptions.setUseDiskForLoadEffectsResource(true);
```

- `setLoadEffectsResource(true)` – レイヤーに付随するドロップシャドウなどの追加効果を読み込みます。  
- `setUseDiskForLoadEffectsResource(true)` – 重いリソースをディスクにオフロードし、メモリ使用量を抑えます。

## Step 3: Load the PSD File
上記オプションを使用して、PSD を `PsdImage` オブジェクトにロードします。

```java
PsdImage image = (PsdImage) Image.load(sourceFileName, imageLoadOptions);
```

この時点で `image` にはすべてのレイヤー、マスク、エフェクトが含まれ、抽出の準備が整っています。

## Step 4: Set Up the Save Options
PNG の保存方法を設定します。`TruecolorWithAlpha` を使用すると、元レイヤーの透過性が保持されます。

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

## Step 5: Save the Image (Convert PSD Layers to PNG)
ロードした PSD（すべてのレイヤーを含む）を単一の PNG ファイルへエクスポートします。この手順で **convert psd layers png** が一度に実行されます。

```java
image.save(output, saveOptions);
```

各レイヤーを個別の PNG にしたい場合は `image.getLayers()` をイテレートすれば可能です。ただし多くのユースケースではマージされた PNG で十分です。

## Step 6: Wrap It Up
処理が正常に完了したことを示すコンソールメッセージを追加します。

```java
System.out.println("PSD Layers have been successfully converted to PNG!");
```

## Common Issues & Tips
- **Out‑of‑Memory Errors:** 非常に大きな PSD を処理する場合は、`setUseDiskForLoadEffectsResource(true)` を有効にして一時データをディスクにオフロードしてください。  
- **Missing Effects:** `setLoad設定されていないと、一部のレイヤー効果が無視されることがあります。  
- **Path Problems:** プラットフォームに依存しないパス処理のために、`java.nio.file` の `Paths.get(...)` を使用してください。

## Frequently Asked Questions

**Q: Aspose.PSD for Java とは何ですか？**  
A: Aspose.PSD for Java は、Photoshop をインストールせずに PSD ファイルを操作できるライブラリです。

**Q: 他のファイル形式でも Aspose.PSD を使用できますか？**  
A: はい。主に PSD 用ですが、Aspose は他の多数のフォーマット向けライブラリも提供しています。

**Q: トライアル版はありますか？**  
A: もちろんです！無料トライアル版は [here](https://releases.aspose.com/) からダウンロードできます。

**Q: サポートが必要なときはどこへ問い合わせればよいですか？**  
A: Aspose フォーラムのサポートページ [here](https://forum.aspose.com/c/psd/34) で質問できます。

**Q: PNG から PSD へ変換できますか？**  
A: Aspose.PSD ライブラリは主に PSD の読み取りと操作に焦点を当てており、他フォーマットから PSD への変換はサポートしていません。

**Q: 各レイヤーを個別の PNG として抽出するには？**  
A: `image.getLayers()` をイテレートし、各レイヤーごとに新しい `Bitmap` を作成して `PngOptions` で保存します。これによりレイヤーごとの PNG が得られます。

## Conclusion
これで **PSD レイヤーの抽出**、フルレイヤーサポートの有効化、そして Aspose.PSD for Java を使用した **PSD レイヤーの PNG への変換** 方法を習得しました。自動化されたアセットパイプラインの構築やデスクトップアプリへのグラフィック機能追加など、Photoshop 本体が不要な環境でも Photoshop ファイルを細かく制御できるようになります。フィルタ適用やプログラム上でのレイヤー結合、個別レイヤーのエクスポートなど、さらに踏み込んだ活用もぜひお試しください。

---

**Last Updated:** 2025-12-10  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}