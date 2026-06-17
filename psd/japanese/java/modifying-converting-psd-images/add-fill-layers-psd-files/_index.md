---
date: 2026-03-04
description: Aspose.PSD for Java を使用して塗りつぶしレイヤーを追加し、プログラムで PSD レイヤーを変更する方法を学びましょう。このステップバイステップガイドに従って、デザインをすばやく強化してください。
linktitle: Modify PSD Layers Programmatically – Add Fill Layers (Java)
second_title: Aspose.PSD Java API
title: PSDレイヤーをプログラムで変更する – 塗りレイヤーを追加 (Java)
url: /ja/java/modifying-converting-psd-images/add-fill-layers-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSDレイヤーをプログラムで変更する – 塗りつぶしレイヤーを追加 (Java)

## Quick Answers
- **何が実現できますか？** プログラムでPSDファイルにカラー、グラデーション、パターンの塗りつぶしレイヤーを追加します。  
- **どのライブラリが必要ですか？** Aspose.PSD for Java（最新リリース）。  
- **ライセンスは必要ですか？** テスト用の無料トライアルで動作しますが、商用利用には商用ライセンスが必要です。  
- **実装にどれくらい時間がかかりますか？** 基本的な例で約10〜15分です。  
- **サポートされているJavaバージョンは？** JDK 11以降。

## “PSDレイヤーをプログラムで変更する” とは？
プログラムでPSDレイヤーを変更するとは、コードを使用してPhotoshopドキュメント内のレイヤーを作成、編集、削除することを指し、手動のUI操作なしでデザインワークフローを完全に制御できます。

## なぜ Aspose.PSD で塗りつぶしレイヤーを追加するのか？
- **自動化** – バッチジョブで数十個のPSDを生成。  
- **一貫性** – 複数ファイルに同じカラー、グラデーション、パターンを適用。  
- **高速** – Photoshop の手作業ステップを省略。  
- **クロスプラットフォーム** – Java をサポートする任意の OS で動作。

## 前提条件
コードに取り掛かる前に、以下を用意してください。

1. **Java Development Kit (JDK)** – JDK 11 以上をインストールします。ダウンロードは [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) から。  
2. **Aspose.PSD for Java** – 公式ダウンロードページから最新ライブラリを取得します [here](https://releases.aspose.com/psd/java/)。  
3. **IDE** – IntelliJ IDEA、Eclipse、またはお好みのエディタ。  
4. **基本的な Java 知識** – クラスやメソッドに慣れていると便利ですが、チュートリアルはステップバイステップで説明します。

## Import Packages
PSD ファイルを操作するために、必要な Aspose.PSD クラスをインポートします。

```java
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
```

これらのインポートにより、`PsdImage` オブジェクト（ドキュメント本体）や、使用する各種 `FillLayer` タイプにアクセスできるようになります。

## How to Modify PSD Layers Programmatically – Step‑by‑Step Guide

### Step 1: Set Up Your Output Directory
結果の PSD を保存するディレクトリを定義し、後で見つけやすくします。

```java
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
```

`"Your Document Directory"` をマシン上の絶対パスまたは相対パスに置き換えてください。

### Step 2: Create a New Photoshop Document
塗りつぶしレイヤーを配置する空のキャンバスを作成します。

```java
PsdImage psdImage = new PsdImage(100, 100);
```

`100, 100` は幅と高さ（ピクセル）を表します。デザイン要件に合わせて調整してください。

### Step 3: Add a Color Fill Layer
単色の塗りつぶしレイヤーを作成し、分かりやすい名前を付けます。

```java
FillLayer colorFillLayer = FillLayer.createInstance(FillType.Color);
colorFillLayer.setDisplayName("Color Fill Layer");
psdImage.addLayer(colorFillLayer);
```

実際のカラーはレイヤーの塗りつぶし設定で後から変更可能です（簡略化のためここでは省略）。

### Step 4: Add a Gradient Fill Layer
グラデーション塗りつぶしは奥行きと視覚的な興味を加えます。

```java
FillLayer gradientFillLayer = FillLayer.createInstance(FillType.Gradient);
gradientFillLayer.setDisplayName("Gradient Fill Layer");
psdImage.addLayer(gradientFillLayer);
```

レイヤー設定で線形または放射状グラデーションを自由に試せます。

### Step 5: Add a Pattern Fill Layer
パターン塗りつぶしにより、画像やテクスチャをレイヤー全体にタイル状に配置できます。

```java
FillLayer patternFillLayer = FillLayer.createInstance(FillType.Pattern);
patternFillLayer.setDisplayName("Pattern Fill Layer");
patternFillLayer.setOpacity((byte)50);
psdImage.addLayer(patternFillLayer);
```

不透明度を 50 % に設定すると、下のレイヤーと自然にブレンドされます。

### Step 6: Save Your PSD File
変更をディスクに永続化します。

```java
psdImage.save(outPsdFilePath);
```

保存したファイルを Photoshop または任意の PSD ビューアで開くと、3 つの新しい塗りつぶしレイヤーが確認できます。

### Step 7: Clean Up Resources
`PsdImage` オブジェクトを必ず破棄し、ネイティブメモリを解放します。

```java
psdImage.dispose();
```

## Common Issues & Tips
- **無効な出力パス** – ディレクトリが存在し、書き込み権限があることを確認してください。  
- **メモリ使用量** – 非常に大きなキャンバスの場合、画像の処理が終わったらすぐに `psdImage.dispose()` を呼び出してください。  
- **レイヤー順序** – デフォルトではレイヤーはスタックの最上部に追加されます。特定の順序が必要な場合は `psdImage.insertLayer(layer, index)` を使用します。

## Frequently Asked Questions

**Q: Aspose.PSD for Java で追加できる塗りつぶしレイヤーの種類は何ですか？**  
A: カラー、グラデーション、パターンの塗りつぶしレイヤーを追加できます。

**Q: Aspose.PSD は他の画像フォーマットもサポートしていますか？**  
A: はい、BMP、JPEG、PNG など多数のフォーマットに対応しています。

**Q: Aspose.PSD を無料で使用できますか？**  
A: Aspose.PSD for Java の無料トライアルを [here](https://releases.aspose.com/) で試せます。

**Q: Aspose.PSD のドキュメントはどこで確認できますか？**  
A: 完全なドキュメントは [here](https://reference.aspose.com/psd/java/) からアクセスできます。

**Q: Aspose.PSD のサポートコミュニティはありますか？**  
A: はい、Aspose フォーラムのコミュニティでサポートを受けられます [here](https://forum.aspose.com/c/psd/34)。

## Conclusion
これで **PSDレイヤーをプログラムで変更する** 方法として、Aspose.PSD for Java を使ってさまざまな塗りつぶしレイヤーを追加する手順を習得しました。このアプローチにより時間を節約し、プロジェクト間での一貫性が保たれ、強力なバッチ処理シナリオが実現できます。異なるカラー、グラデーション、パターンを試して、どこまで自動化されたデザイン作成が可能かぜひ体験してみてください。

---

**最終更新日:** 2026-03-04  
**テスト環境:** Aspose.PSD for Java（最新リリース）  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}