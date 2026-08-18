---
date: 2026-03-26
description: Aspose.PSD for Java を使用して、テキストレイヤーの PSD ファイルを編集し、テキストカラーを変更する方法を学びましょう。開発者とデザイナー向けのステップバイステップガイドです。
linktitle: Edit Text Layers PSD Files using Java
second_title: Aspose.PSD Java API
title: Java を使用して PSD ファイルのテキストレイヤーを編集 – Aspose.PSD チュートリアル
url: /ja/java/psd-image-modification-conversion/format-text-portions-psd-files/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Edit Text Layers PSD Files Using Java

## Introduction

視覚的なコンテンツが増える現代において、**edit text layers PSD** ファイルをプログラムで編集できることは、手作業の時間を大幅に削減します。バッチでグラフィックを更新したいデザイナーや、動的な画像生成サービスを構築したい開発者にとって、Aspose.PSD for Java を使用すれば、Photoshop で行うのと同じようにコードだけで PSD のテキストを変更できます。本チュートリアルでは、テキストレイヤー PSD ファイルの編集手順をすべて解説し、個々のテキスト部分の **change text color PSD** 方法も紹介します。

## Quick Answers
- **What library lets you edit text layers PSD?** Aspose.PSD for Java  
- **Can you change text color PSD programmatically?** Yes, using `ITextStyle.setFillColor`  
- **Do I need a license for production?** A commercial license is required; a free trial is available.  
- **Which Java version is supported?** Java 8 and later.  
- **Is memory management required?** Yes—dispose of the `PsdImage` after saving.

## What is edit text layers PSD?

Editing text layers PSD とは、Photoshop PSD ファイル内に保存されたテキストデータにアクセスし、文字やスタイル、書式を変更したうえで、変更内容をファイルに書き戻すことを指します。この機能は、ブランド更新の自動化、ローカライズされたグラフィックの作成、手動で Photoshop を操作せずにパーソナライズされたマーケティング資産を生成する際に不可欠です。

## Why edit text layers PSD with Aspose.PSD?

- **Full control** – フォント、色、配置を変更でき、テキスト部分の追加・削除も可能。  
- **Cross‑platform** – Java が動作するすべての OS で利用可能。  
- **No Photoshop required** – サーバーや CI パイプライン上でバッチ処理を実行できる。  
- **High fidelity** – レイヤー効果、マスク、その他 PSD の機能を保持したまま処理できる。

## Prerequisites

コードを書く前に、以下が揃っていることを確認してください。

1. **Java Development Kit (JDK)** – Java 8+ がインストールされ、設定済みであること。  
2. **Aspose.PSD for Java Library** – [here](https://releases.aspose.com/psd/java/) からダウンロード、または [free trial](https://releases.aspose.com/) を開始。  
3. **IDE for Java Development** – IntelliJ IDEA、Eclipse、NetBeans のいずれかで、プロジェクトのクラスパスに Aspose.PSD JAR を追加。  
4. **Basic Knowledge of Java** – オブジェクト、ループ、例外処理に慣れていること。

## Importing Necessary Packages

Aspose.PSD for Java を使用する際は、必要なクラスやメソッドにアクセスできるように特定のパッケージをインポートする必要があります。以下をご確認ください。

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
import com.aspose.psd.fileformats.psd.layers.text.ITextPortion;
import com.aspose.psd.fileformats.psd.layers.text.ITextStyle;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.internal.Exceptions.Exception;
```

これらのインポートにより、例で使用する Aspose.PSD の主要機能が利用可能になります。

## Step 1: Define Your Directories

PSD ファイルの処理を始める前に、元の PSD ファイルがある場所と、変更後のファイルを保存する場所を定義します。

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "ThreeColorsParagraphs.psd";
String outPsdFilePath = outputDir + "ThreeColorsParagraph_out.psd";
```

プレースホルダーのパスを実際の環境に合わせて置き換えてください。

## Step 2: Load the PSD File

次に、操作対象の PSD ファイルを読み込みます。Aspose なら非常にシンプルです。

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

`Image.load` がファイルを開き、レイヤーの検査が可能になります。

## Step 3: Loop Through the Layers

PSD がロードされたら、レイヤーを走査します。テキストを含むレイヤーだけを抽出したいので、フィルタリングを行います。

```java
for (Layer layer : psdImage.getLayers()) {
    if (!(layer instanceof TextLayer)) {
        continue;
    }
    // Process only text layers…
}
```

このループはすべてのレイヤーを走査し、`TextLayer` のインスタンスでないものはスキップします。

## Step 4: Access Text Portions

テキストレイヤーが特定できたら、編集対象となるテキスト部分（text portions）にアクセスします。ここからが本番です！

```java
TextLayer textLayer = (TextLayer) layer;
ITextPortion[] portions = textLayer.getTextData().getItems();
```

テキスト部分は、個別に編集可能な単語や文の単位と考えてください。

## Step 5: Modify Text Portions

テキストを実際に編集します。既存のテキストを変更したり、不要な部分を削除したり、新しいテキストを追加したりします。

```java
portions[0].setText("Hello ");
portions[1].setText("World");
// Removing text portions
textLayer.getTextData().removePortion(3);
textLayer.getTextData().removePortion(2);
// Adding new text portion
ITextPortion createdPortion = textLayer.getTextData().producePortion();
createdPortion.setText("!!!\r");
textLayer.getTextData().addPortion(createdPortion);
```

段落の一部を書き換えたり削除したりする手順がシンプルに示されています。

## Step 6: Justify and Style Text

テキストを変更した後は、スタイル調整が必要になることがあります。文字揃えや色の変更を行いましょう。

```java
// Set right justification
portions[0].getParagraph().setJustification(1); // Right
portions[1].getParagraph().setJustification(1);
portions[2].getParagraph().setJustification(1);

// Set fill colors individually
portions[0].getStyle().setFillColor(Color.getAquamarine());
portions[1].getStyle().setFillColor(Color.getViolet());
portions[2].getStyle().setFillColor(Color.getLightBlue());
```

ここでは各テキスト部分に対して **change text color PSD** を行い、`fillColor` を設定しています。これにより単語ごとに異なる色を付与できます。

## Step 7: Update Layer Data

すべての変更を加えたら、レイヤーのデータに反映させます。

```java
textLayer.getTextData().updateLayerData();
```

この呼び出しにより、変更が PSD の内部構造にコミットされます。

## Step 8: Save the Modified PSD File

最後に、変更済み PSD ファイルを保存します。

```java
psdImage.save(outPsdFilePath, new PsdOptions(psdImage));
```

出力先パスを指定すれば、編集後のファイルが書き出されます。

## Step 9: Dispose of Resources

メモリ使用量を抑えるため、処理が終わったら画像リソースを必ず破棄してください。

```java
finally {
    psdImage.dispose();
}
```

リソースを解放することで、特に大量のファイルをバッチ処理する際のメモリリークを防げます。

## Common Issues and Solutions

| Issue | Reason | Fix |
|-------|--------|-----|
| **NullPointerException on `portions[2]`** | The source PSD has fewer than three portions. | Verify the number of portions with `portions.length` before accessing indexes. |
| **Colors not applied** | Using an outdated Aspose.PSD version. | Upgrade to the latest Aspose.PSD for Java release. |
| **File not found** | Incorrect path in `sourceDir` or `outputDir`. | Use absolute paths or double‑check relative paths. |
| **License not set** | Trial version may add watermarks. | Apply a valid license with `License license = new License(); license.setLicense("Aspose.PSD.lic");` |

## Frequently Asked Questions

### What is Aspose.PSD for Java?
Aspose.PSD for Java is a library that allows developers to manipulate and work with Photoshop PSD files programmatically.

### Can I use Aspose.PSD for free?
Yes, you can start with a free trial available on the Aspose website before deciding to purchase.

### What prerequisites do I need?
You need the Java Development Kit (JDK) installed, the Aspose.PSD library, and basic knowledge of Java programming.

### Are there any limitations with the free trial?
Yes, the free trial may have certain limitations regarding the features available, such as watermarking or limited usage.

### Where can I find more information about Aspose.PSD?
You can check the documentation for detailed usage scenarios and API references [here](https://reference.aspose.com/psd/java/).

---

**Last Updated:** 2026-03-26  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}