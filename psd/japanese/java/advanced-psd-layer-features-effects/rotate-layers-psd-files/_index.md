---
date: 2026-07-22
description: Java で Aspose.PSD を使用して PSD を PNG に保存し、PNG の透過性を保持し、PSD のレイヤーを回転させる方法を学びます。ステップバイステップのガイド、コード不要の解説、トラブルシューティングのヒントを提供します。
keywords:
- save psd as png
- export psd layers png
- convert photoshop file png
- psd to png transparency
lastmod: 2026-07-22
linktitle: Java で Aspose.PSD を使用して PSD を PNG に保存し、レイヤーを回転する
og_description: Java 用 Aspose.PSD で PSD を PNG に保存します。透過性を保持し、レイヤーを回転させ、数行のコードで PNG
  をエクスポートできるため、自動化ワークフローに最適です。
og_image_alt: 'Developer guide: save PSD as PNG and rotate layers using Aspose.PSD
  for Java'
og_title: Java で Aspose.PSD を使用して PSD を PNG に保存し、レイヤーを回転する
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to save psd as png, preserve PNG transparency, and rotate
    PSD layers in Java with Aspose.PSD. Step‑by‑step guide, code‑free explanations,
    and troubleshooting tips.
  headline: save psd as png and rotate layers in Java using Aspose.PSD
  type: TechArticle
- description: Learn how to save psd as png, preserve PNG transparency, and rotate
    PSD layers in Java with Aspose.PSD. Step‑by‑step guide, code‑free explanations,
    and troubleshooting tips.
  name: save psd as png and rotate layers in Java using Aspose.PSD
  steps:
  - name: Set Up Your Java Project
    text: Create a new Java project in your IDE and add the Aspose.PSD JAR to the
      project’s build path.
  - name: Import Required Classes
    text: '`PsdImage` is the core class that represents a Photoshop document in memory.
      `PngOptions` controls PNG‑specific settings, and `RotateFlipType` defines rotation
      and flip operations. These imports give you access to image loading, rotation,
      and PNG‑specific options.'
  - name: Define File Paths
    text: Specify where your source PSD lives and where the output files should be
      written. Using absolute paths during testing avoids “file not found” errors.
      > **Pro tip:** Store paths in a configuration file for easier maintenance in
      larger projects.
  - name: Load the PSD File
    text: '`PsdImage` loads the entire Photoshop document, including all layers, masks,
      and effects, into a manipulable object. Now `im` represents the whole PSD, ready
      for transformations.'
  - name: Rotate the Image (How to rotate PSD)
    text: '`RotateFlipType` enumerates all supported rotations and flips. In this
      example we rotate 270° and flip both axes, which swaps width and height while
      mirroring the image. Feel free to experiment with other values such as `Rotate90FlipNone`
      or `Rotate180FlipX`.'
  - name: Save the Rotated Image as PNG (save PSD as PNG)
    text: Configure `PngOptions` to keep transparency (`PngColorType.TruecolorWithAlpha`)
      and then call `save`. The PNG retains layer transparency, ensuring it works
      seamlessly in web or mobile apps. The resulting PNG preserves alpha channels,
      making it suitable for compositing or further processing.
  - name: Save the Modified PSD (optional)
    text: If you also need a new PSD with the rotation applied, you can save the modified
      `PsdImage` back to disk. You now have both a PNG preview and an updated PSD
      file.
  type: HowTo
- questions:
  - answer: Yes, you can call `layer.rotateFlip(RotateFlipType.Rotate90FlipNone)`
      after iterating through `im.getLayers()`.
    question: Can I rotate a specific layer in a PSD file?
  - answer: The library handles most files efficiently, but extremely large PSDs (>500
      MB) may require additional memory or streaming options.
    question: Is there any performance limitation with Aspose.PSD for Java?
  - answer: Aspose offers a free trial, but a paid license is needed for production.
      See the [temporary license](https://purchase.aspose.com/temporary-license/)
      for testing.
    question: Is Aspose.PSD free to use?
  - answer: Comprehensive docs are available at [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/).
    question: Where can I find detailed documentation?
  - answer: Get help via the [Aspose Support Forum](https://forum.aspose.com/c/psd/34).
    question: What if I encounter issues while using Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert PSD
- Aspose.PSD
- Java image processing
- rotate PSD layers
title: Java で Aspose.PSD を使用して PSD を PNG に保存し、レイヤーを回転する
url: /ja/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/
weight: 21
---

## 関連チュートリアル

- [Aspose.PSD for JavaでPSDをPNGとして保存し、レンダリングドロップシャドウを適用する](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Aspose.PSD for Javaを使用してPNGファイルを圧縮する方法](/psd/java/optimizing-png-files/compress-png-files/)
- [Aspose.PSDを使用したJavaでの画像回転方法](/psd/java/advanced-image-manipulation/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/pf/main-wrap-class >}}

# JavaでAspose.PSDを使用してPSDをPNGとして保存し、レイヤーを回転する

## はじめに
レイヤーを回転させながら **PSDをPNGとして保存** したい場合は、このガイドが最適です。バッチ処理ツールやオンザフライで画像操作が必要なWebサービス、あるいはデザインワークフローの自動化を行う場合でも、プログラムで実行すれば時間を節約でき、Adobe Photoshop への依存もなくなります。このチュートリアルでは **PSDレイヤーの回転方法** と、結果を PNG としてエクスポートする手順を Aspose.PSD for Java ライブラリを使って解説します。さあ、袖をまくってデザインワークフローをスムーズにしましょう！

## クイック回答
- **使用できるライブラリは何ですか？** Aspose.PSD for Java  
- **PSDを回転させてPNGとして保存することは同時にできますか？** はい – PSDを回転させてからPNGとして保存します  
- **ライセンスは必要ですか？** 無料トライアルでテスト可能です。製品版には有料ライセンスが必要です  
- **サポートされているJavaバージョンは？** Java 8以降  
- **PNG出力は透過ですか？** はい、`PngColorType.TruecolorWithAlpha` を設定すれば透過になります  

## “PSDをPNGに変換”とは何ですか？
Photoshop ドキュメント（PSD）を PNG 画像に変換すると、レイヤー、マスク、アルファチャンネルなどの視覚コンテンツを、透過を保持したまま広くサポートされているラスタ形式に抽出します。これにより PNG は Web グラフィック、サムネイル、下流の画像処理に最適です。生成された PNG は Web ページやモバイルアプリで直接使用でき、他の画像ライブラリでもさらに処理できます。

## なぜAspose.PSD for Javaを使用してPSDをPNGとして保存し、PSDレイヤーを回転させるのか？
Aspose.PSD を使えば **PSDをPNGとして保存** しつつレイヤーを回転でき、Photoshop のインストールは不要です。**50 以上の入力・出力フォーマット** に対応し、200 MB 未満のメモリで数百ページの PSD を処理でき、Windows、Linux、macOS で動作します。API は数行のメソッド呼び出しだけで、レイヤー効果、マスク、アルファチャンネルを自動的に処理し、高忠実度の結果を提供します。

## 前提条件
- **Java Development Kit (JDK)** – [Oracleのウェブサイト](https://www.oracle.com/java/technologies/javase-downloads.html)からダウンロードしてください。  
- **統合開発環境 (IDE)** – IntelliJ IDEA、Eclipse、NetBeansのいずれでも構いません。  
- **Aspose.PSD for Java ライブラリ** – 最新のJARは[リリースページ](https://releases.aspose.com/psd/java/)から入手してください。  
- **基本的なJavaの知識** – クラス、オブジェクト、例外処理に慣れていること。  

## 手順ガイド

### 手順 1: Javaプロジェクトの設定
IDE で新規 Java プロジェクトを作成し、Aspose.PSD の JAR をビルドパスに追加します。

### 手順 2: 必要なクラスをインポート
`PsdImage` はメモリ上の Photoshop ドキュメントを表すコアクラスです。`PngOptions` は PNG 固有の設定を制御し、`RotateFlipType` は回転とフリップ操作を定義します。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

これらのインポートにより、画像の読み込み、回転、PNG 固有のオプションにアクセスできます。

### 手順 3: ファイルパスの定義
ソース PSD の場所と出力ファイルの保存先を指定します。テスト時は絶対パスを使用すると「ファイルが見つかりません」エラーを回避できます。

```java
String dataDir = "Your Document Directory"; // Change this to your actual document directory.
String sourceFile = dataDir + "1.psd"; // Source PSD file
String pngPath = dataDir + "RotateFlipTest2617.png"; // Output PNG file path
String psdPath = dataDir + "RotateFlipTest2617.psd"; // Output PSD file path
```

> **プロのコツ:** 大規模プロジェクトでは、パスを設定ファイルに保存すると保守が容易です。

### 手順 4: PSDファイルの読み込み
`PsdImage` はすべてのレイヤー、マスク、エフェクトを含む Photoshop ドキュメント全体を操作可能なオブジェクトとしてロードします。

```java
PsdImage im = (PsdImage) Image.load(sourceFile);
```

これで `im` が PSD 全体を表し、変換の準備が整いました。

### 手順 5: 画像の回転 (PSDの回転方法)
`RotateFlipType` はサポートされているすべての回転・フリップを列挙します。この例では 270° 回転し、両軸をフリップして幅と高さを入れ替えます。

```java
int flipType = RotateFlipType.Rotate270FlipXY; // Choose the rotation type
im.rotateFlip(flipType); // Rotate the image
```

`Rotate90FlipNone` や `Rotate180FlipX` など、他の値でも自由に試してみてください。

### 手順 6: 回転した画像をPNGとして保存 (PSDをPNGに変換)
`PngOptions` で透過 (`PngColorType.TruecolorWithAlpha`) を保持するよう設定し、`save` を呼び出します。PNG はレイヤーの透過情報を保持し、Web やモバイルアプリでシームレスに使用できます。

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha); // Preserve transparency
im.save(pngPath, options); // Save the rotated image
```

生成された PNG はアルファチャンネルを保持しているため、合成やさらなる処理に適しています。

### 手順 7: 変更したPSDを保存 (オプション)
回転を適用した新しい PSD が必要な場合は、変更済みの `PsdImage` をディスクに保存できます。

```java
im.save(psdPath);
```

これで PNG プレビューと更新された PSD の両方が手に入ります。

## よくある問題と解決策
- **ファイルが見つかりません:** `dataDir` がパス区切り文字 (`/` または `\`) で終わっているか確認してください。  
- **大きなPSDでOutOfMemoryError:** JVMヒープサイズを増やしてください (`-Xmx2g`)。  
- **透過が失われる:** `PngColorType.TruecolorWithAlpha` が設定されていることを確認してください。設定しないと PNG はアルファなしで保存されます。  
- **PSD画像のフリップが期待通りに動作しない:** 選択した `RotateFlipType` 定数を再確認してください。一部の定数は回転とフリップを同時に行います。  

## よくある質問

**Q: PSDファイル内の特定のレイヤーを回転させることはできますか？**  
A: はい、`im.getLayers()` を走査した後で `layer.rotateFlip(RotateFlipType.Rotate90FlipNone)` を呼び出せば可能です。

**Q: Aspose.PSD for Java にパフォーマンス上の制限はありますか？**  
A: ライブラリはほとんどのファイルを効率的に処理しますが、500 MB 超の超大型 PSD は追加メモリまたはストリーミングオプションが必要になる場合があります。

**Q: Aspose.PSD は無料で使用できますか？**  
A: 無料トライアルは利用可能ですが、製品版には有料ライセンスが必要です。テスト用は [temporary license](https://purchase.aspose.com/temporary-license/) を参照してください。

**Q: 詳細なドキュメントはどこで見つけられますか？**  
A: 完全なドキュメントは [Aspose.PSD Documentation](https://reference.aspose.com/psd/java/) にあります。

**Q: Aspose.PSD 使用中に問題が発生したらどうすればよいですか？**  
A: [Aspose Support Forum](https://forum.aspose.com/c/psd/34) でサポートを受けられます。

**Q: PSDをPNGに変換するとレイヤー効果は保持されますか？**  
A: はい、`PngColorType.TruecolorWithAlpha` で保存すれば、ほとんどの視覚効果が PNG にラスタライズされます。

**Q: 複数の PSD ファイルを一括処理できますか？**  
A: もちろんです。ディレクトリ内の PSD を走査するループでコードをラップすれば実現できます。

**Q: PNG の圧縮レベルを設定できますか？**  
A: `PngOptions` の `setCompressionLevel(int)` メソッドで出力サイズを細かく調整できます。

**Q: 画像オブジェクトを閉じる必要がありますか？**  
A: `PsdImage` は `Closeable` を実装しています。try‑with‑resources を使用するか、`finally` ブロックで `im.close()` を呼び出してください。

**Q: 回転した PNG は元のサイズと同じですか？**  
A: 90° または 270° の回転では幅と高さが入れ替わるため、PNG は自動的に新しい向きを反映します。

## 結論
Aspose.PSD for Java を活用すれば、**PSDをPNGとして保存** し、**PNG の透過を保持** しながら **PSDレイヤーを回転** させる処理を数行のコードで実現できます。Photoshop が不要になり、ワークフローの自動化が高速化され、画像出力を完全にコントロールできます。ぜひご自身のプロジェクトで試して、どれだけ時間が節約できるか体感してください！

---

**最終更新日:** 2026-07-22  
**テスト環境:** Aspose.PSD for Java 24.11  
**作者:** Aspose  

{{< blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}