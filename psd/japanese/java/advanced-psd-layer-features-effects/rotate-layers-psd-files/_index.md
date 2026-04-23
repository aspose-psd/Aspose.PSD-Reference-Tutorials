---
date: 2026-02-17
description: Aspose.PSD を使用して Java で PSD を PNG に変換し、PNG の透過性を保持し、PSD レイヤーを回転させる方法を学びます。コードサンプル付きのステップバイステップガイド。
linktitle: Convert PSD to PNG and Rotate Layers in PSD Files using Java
second_title: Aspose.PSD Java API
title: Javaを使用してPSDをPNGに変換し、PSDファイル内のレイヤーを回転させる
url: /ja/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java を使用して PSD を PNG に変換し、PSD ファイルのレイヤーを回転する

## Introduction
**PSD を PNG に変換**しながらレイヤーも回転させる必要がある場合は、このガイドが最適です。バッチ処理ツールの構築や、オンザフライで画像操作が必要な Web サービス、あるいはデザインワークフローの自動化など、プログラムで実行すれば時間を節約でき、Adobe Photoshop への依存もなくなります。このチュートリアルでは、Aspose.PSD for Java ライブラリを使用して **PSD のレイヤーを回転**し、結果を PNG としてエクスポートする方法を順を追って解説します。さあ、袖をまくってデザインワークフローをスムーズにしましょう！

## Quick Answers
- **どのライブラリを使えばよいですか？** Aspose.PSD for Java  
- **回転と変換を同時に行えますか？** はい – PSD を回転させてから PNG として保存します  
- **ライセンスは必要ですか？** テスト用の無料トライアルで動作しますが、製品版では有料ライセンスが必要です  
- **対応している Java バージョンは？** Java 8 以降  
- **PNG の出力は透過されますか？** はい、`PngColorType.TruecolorWithAlpha` を設定すれば透過が保持されます  

## What is “convert PSD to PNG”?
Photoshop ドキュメント（PSD）を PNG 画像に変換することは、すべてのレイヤー、マスク、透過情報を抽出し、広くサポートされているラスタ形式に変換することを意味します。PNG はアルファチャンネルを保持できるため、Web グラフィックやサムネイル、さらなる画像処理に最適です。

## Why use Aspose.PSD for Java to convert PSD to PNG and rotate PSD layers?
- **Photoshop 不要** – 任意のサーバーや CI 環境で動作  
- **フルレイヤーサポート** – 透過やレイヤー効果をそのまま保持  
- **シンプルな API** – 数行のメソッド呼び出しで回転、フリップ、保存が可能  
- **クロスプラットフォーム** – Windows、Linux、macOS で実行可能  
- **Java 画像変換** を単一ライブラリで手軽に実現  

## Prerequisites
コードに入る前に、以下を用意してください。

- **Java Development Kit (JDK)** – [Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html) からダウンロード。  
- **Integrated Development Environment (IDE)** – IntelliJ IDEA、Eclipse、NetBeans などお好みのもの。  
- **Aspose.PSD for Java library** – 最新の JAR を [release page](https://releases.aspose.com/psd/java/) から取得。  
- **Basic Java knowledge** – クラス、オブジェクト、例外処理に慣れていること。

## Step‑by‑Step Guide

### Step 1: Set Up Your Java Project
IDE で新規 Java プロジェクトを作成し、Aspose.PSD JAR をプロジェクトのビルドパスに追加します。

### Step 2: Import Required Classes
Java ソースファイルの冒頭に以下のインポートを追加します。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

これらのクラスにより、画像の読み込み、回転、PNG 固有のオプションが利用可能になります。

### Step 3: Define File Paths
ソース PSD の場所と出力ファイルの保存先を指定します。

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **Pro tip:** テスト時は絶対パスを使用して「ファイルが見つからない」エラーを回避しましょう。

### Step 4: Load the PSD File
PSD を操作可能なオブジェクトにロードします。

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

これで `im` はすべてのレイヤーを含む Photoshop ドキュメント全体を表します。

### Step 5: Rotate the Image (How to rotate PSD)
`RotateFlipType` から回転タイプを選択します。この例では 270° 回転させ、両軸をフリップしています。

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

`Rotate90FlipNone` や `Rotate180FlipX` など、他の値でも自由に試してみてください。これがチュートリアルの **how to rotate PSD** 部分です。

### Step 6: Save the Rotated Image as PNG (convert PSD to PNG)
透過を保持するよう PNG オプションを設定し、保存します。

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

生成された PNG はレイヤーの透過情報を保持し、**preserve PNG transparency** が下流で利用できるようになります。

### Step 7: Save the Modified PSD (optional)
回転を適用した新しい PSD が必要な場合は、こちらで保存します。

```java
im.save(psdPath);
```

これで PNG プレビューと更新された PSD の両方が手に入ります。

## Common Issues and Solutions
- **File not found:** `dataDir` がパス区切り文字（`/` または `\`）で終わっているか確認してください。  
- **OutOfMemoryError on large PSDs:** JVM ヒープサイズを増やします（例: `-Xmx2g`）。  
- **Transparency lost:** `PngColorType.TruecolorWithAlpha` が設定されているか確認。設定しないと PNG はアルファなしで保存されます。  
- **Flip PSD image not behaving as expected:** 選択した `RotateFlipType` 定数を再確認してください。一部の定数は回転とフリップを同時に行います。

## Frequently Asked Questions

**Q: Can I rotate a specific layer in a PSD file?**  
A: Yes, you can use `Layer.rotateFlip()` on individual layers after iterating through `im.getLayers()`.

**Q: Is there any performance limitation with Aspose.PSD for Java?**  
A: The library handles most files efficiently, but extremely large PSDs (>500 MB) may require additional memory.

**Q: Is Aspose.PSD free to use?**  
A: Aspose offers a free trial, but a paid license is needed for production. Check the [temporary license](https://purchase.aspose.com/temporary-license/) for testing.

**Q: Where can I find detailed documentation?**  
A: You can find comprehensive documentation at [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).

**Q: What if I encounter issues while using Aspose.PSD?**  
A: Reach out for help via the [Aspose Support Forum](https://forum.aspose.com/c/psd/34).

**Q: Does converting PSD to PNG preserve layer effects?**  
A: Yes, when you save with `PngColorType.TruecolorWithAlpha`, most visual effects are rasterized into the PNG.

**Q: Can I batch‑process multiple PSD files?**  
A: Absolutely. Wrap the code in a loop that iterates over a directory of PSD files.

**Q: Is it possible to set PNG compression level?**  
A: The `PngOptions` class provides a `setCompressionLevel(int)` method for fine‑tuning.

**Q: Do I need to close the image object?**  
A: `PsdImage` implements `Closeable`; call `im.close()` in a `finally` block or use try‑with‑resources.

**Q: Will the rotated PNG have the same dimensions as the original?**  
A: Rotating by 90° or 270° swaps width and height. The PNG will reflect the new orientation.

## Conclusion
Aspose.PSD for Java を活用すれば、**PSD を PNG に変換**し、**PNG の透過を保持**しながら **PSD のレイヤーを回転** する処理を数行のコードで実現できます。Photoshop が不要になるため、自動化ワークフローが高速化し、画像出力をフルコントロールできます。ぜひご自身のプロジェクトで試して、どれだけ時間が節約できるか体感してください！

---

**Last Updated:** 2026-02-17  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}