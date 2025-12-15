---
date: 2025-12-15
description: Aspose.PSD を使用して Java で PSD を PNG に変換し、PSD レイヤーを回転させる方法を学びましょう。コードサンプル付きのステップバイステップガイドです。
linktitle: Convert PSD to PNG and Rotate Layers in PSD Files using Java
second_title: Aspose.PSD Java API
title: JavaでPSDをPNGに変換し、PSDファイルのレイヤーを回転させる
url: /ja/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# JavaでPSDをPNGに変換し、PSDファイルのレイヤーを回転する

## Introduction
**PSD を PNG に変換**しながらレイヤーを回転させる必要がある場合は、このガイドが役立ちます。バッチ処理ツールを作成する場合や、Web サービスに画像操作機能を組み込む場合、プログラムで実行すれば時間を節約でき、Adobe Photoshop への依存もなくなります。このチュートリアルでは、Aspose.PSD for Java ライブラリを使用して **PSD のレイヤーを回転**し、結果を PNG としてエクスポートする方法を示します。さあ、袖をまくってデザインワークフローをスムーズにしましょう！

## Quick Answers
- **どのライブラリを使用できますか？** Aspose.PSD for Java  
- **回転と変換を同時に行えますか？** はい – PSD を回転させてから PNG として保存  
- **ライセンスは必要ですか？** 無料トライアルでテスト可能；本番環境では有料ライセンスが必要  
- **対応している Java バージョンは？** Java 8 以降  
- **PNG の出力は透過されますか？** はい、`PngColorType.TruecolorWithAlpha` を設定すれば透過されます  

## What is “convert PSD to PNG”?
Photoshop ドキュメント（PSD）を PNG 画像に変換することは、すべてのレイヤー、マスク、透過情報を抽出し、広くサポートされているラスタ形式に変換することを意味します。PNG はアルファチャネルを保持できるため、Web グラフィック、サムネイル、さらなる画像処理に最適です。

## Why use Aspose.PSD for Java to convert PSD to PNG and rotate PSD layers?
- **Photoshop が不要** – 任意のサーバーや CI 環境で動作  
- **フルレイヤーサポート** – 透過やレイヤー効果を保持  
- **シンプルな API** – 回転、フリップ、保存が数行のコードで完了  
- **クロスプラットフォーム** – Windows、Linux、macOS で動作  

## Prerequisites
コードに入る前に、以下を用意してください。

- **Java Development Kit (JDK)** – [Oracle のウェブサイト](https://www.oracle.com/java/technologies/javase-downloads.html) からダウンロード。  
- **統合開発環境 (IDE)** – IntelliJ IDEA、Eclipse、NetBeans のいずれかで OK。  
- **Aspose.PSD for Java ライブラリ** – [リリースページ](https://releases.aspose.com/psd/java/) から最新の JAR を取得。  
- **基本的な Java 知識** – クラス、オブジェクト、例外処理に慣れていること。

## Step-by-Step Guide

### Step 1: Set Up Your Java Project
IDE で新規 Java プロジェクトを作成し、Aspose.PSD の JAR をビルドパスに追加します。

### Step 2: Import Required Classes
Java ソースファイルの先頭に以下のインポートを追加します。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

これらのクラスで画像の読み込み、回転、PNG 固有のオプションにアクセスできます。

### Step 3: Define File Paths
ソース PSD の場所と出力ファイルの保存先を指定します。

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **Pro tip:** テスト時は絶対パスを使用すると “file not found” エラーを回避できます。

### Step 4: Load the PSD File
PSD を操作可能なオブジェクトにロードします。

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

これで `im` はすべてのレイヤーを含む Photoshop ドキュメント全体を表します。

### Step 5: Rotate the Image (How to rotate PSD)
`RotateFlipType` から回転タイプを選択します。この例では 270° 回転し、両軸をフリップしています。

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

`Rotate90FlipNone` や `Rotate180FlipX` など、他の値でも試してみてください。

### Step 6: Save the Rotated Image as PNG (convert PSD to PNG)
透過を保持するために PNG オプションを設定し、保存します。

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

生成された PNG はレイヤーの透過情報を保持しているため、Web でそのまま使用できます。

### Step 7: Save the Modified PSD (optional)
回転を適用した新しい PSD が必要な場合は、こちらで保存します。

```java
im.save(psdPath);
```

これで PNG プレビューと更新された PSD の両方が手に入ります。

## Common Issues and Solutions
- **File not found:** `dataDir` の末尾にパス区切り文字（`/` または `\`）が付いているか確認してください。  
- **OutOfMemoryError on large PSDs:** JVM のヒープサイズを増やします（例: `-Xmx2g`）。  
- **Transparency lost:** `PngColorType.TruecolorWithAlpha` が設定されているか確認。設定しないとアルファが失われた PNG が保存されます。

## FAQs
### Can I rotate a specific layer in a PSD file?
はい、`im.getLayers()` をイテレートし、個々のレイヤーに対して `Layer.rotateFlip()` を呼び出すことで可能です。

### Is there any performance limitation with Aspose.PSD for Java?
ほとんどのファイルは効率的に処理できますが、500 MB を超える超大型 PSD は追加メモリが必要になる場合があります。

### Is Aspose.PSD free to use?
Aspose は無料トライアルを提供していますが、本番環境では有料ライセンスが必要です。テスト用の [temporary license](https://purchase.aspose.com/temporary-license/) をご確認ください。

### Where can I find detailed documentation?
詳細なドキュメントは [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/) にあります。

### What if I encounter issues while using Aspose.PSD?
[Aspose Support Forum](https://forum.aspose.com/c/psd/34) で質問してください。

## Additional Frequently Asked Questions

**Q: Does converting PSD to PNG preserve layer effects?**  
A: はい、`PngColorType.TruecolorWithAlpha` で保存すれば、ほとんどの視覚効果が PNG にラスタライズされます。

**Q: Can I batch‑process multiple PSD files?**  
A: もちろんです。ディレクトリ内の PSD ファイルをループで処理すれば一括変換できます。

**Q: Is it possible to set PNG compression level?**  
A: `PngOptions` クラスの `setCompressionLevel(int)` メソッドで圧縮レベルを調整できます。

**Q: Do I need to close the image object?**  
A: `PsdImage` は `Closeable` を実装しています。`finally` ブロックで `im.close()` を呼ぶか、try‑with‑resources を使用してください。

**Q: Will the rotated PNG have the same dimensions as the original?**  
A: 90° または 270° 回転すると幅と高さが入れ替わります。PNG は新しい向きに合わせたサイズになります。

## Conclusion
Aspose.PSD for Java を活用すれば、**PSD を PNG に変換**し、**PSD のレイヤーを回転**させる処理を数行のコードで実現できます。この方法により Photoshop が不要になり、ワークフローが自動化され、画像出力を完全にコントロールできます。ぜひご自身のプロジェクトで試して、どれだけ時間が節約できるか体感してください！

---

**Last Updated:** 2025-12-15  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}