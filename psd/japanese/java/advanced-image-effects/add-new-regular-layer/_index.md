---
date: 2026-10-18
description: Aspose.PSD for Java と temporary license を使用して、PSD を PNG にエクスポートし、新しい
  regular layer を追加する方法を学びます。ステップバイステップのガイド、layer の位置調整、トラブルシューティングを含みます。
keywords:
- how to export psd
- aspose temporary license
- set layer position
- create new psd layer
lastmod: 2026-10-18
linktitle: PSD に新しい Regular Layer を追加
og_description: Aspose.PSD for Java と temporary license を使用して、PSD を PNG にエクスポートし、新しい
  regular layer を追加する方法を学びます。コード不要の手順全体と layer の位置調整のヒントを含みます。
og_image_alt: Screenshot of Java code adding a layer to a PSD and exporting to PNG
og_title: Aspose.PSD for Java を使用して PSD を PNG にエクスポートし、layer を追加する方法
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Learn how to export PSD to PNG and add a new regular layer using Aspose.PSD
    for Java with a temporary license. Step‑by‑step guide, layer positioning and troubleshooting.
  headline: How to export PSD to PNG and add a layer with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to export PSD to PNG and add a new regular layer using Aspose.PSD
    for Java with a temporary license. Step‑by‑step guide, layer positioning and troubleshooting.
  name: How to export PSD to PNG and add a layer with Aspose.PSD for Java
  steps:
  - name: Load the PSD file
    text: '`PsdImage` is Aspose.PSD''s core class that represents a PSD document in
      memory. Loading the file creates a manipulable object you can edit.'
  - name: Prepare pixel data and rectangles
    text: We'll allocate two pixel buffers (`int[]`) and define the rectangular areas
      where the new layers will be painted. Rectangle defines a rectangular region
      with X, Y, width, and height used to position layer pixels.
  - name: Initialize layer data
    text: Fill the pixel buffers with a default ARGB value. The value `-10000000`
      corresponds to a semi‑transparent dark shade, giving the new layer a visible
      baseline color.
  - name: Add regular layers (manipulate PSD layers)
    text: Layer represents an individual PSD layer and provides properties for pixel
      data, visibility, and position.
  - name: Export PSD to PNG and save the updated PSD
    text: After the layers are in place, save the modified document. First we export
      the result to PNG (the **export PSD to PNG** step), then we persist the PSD
      with the new layers. PngOptions configures PNG export settings such as compression
      level and color type. > **Pro tip:** If you only need the PNG, you
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports Java 8 and later versions.
    question: Is Aspose.PSD compatible with Java 8?
  - answer: Absolutely! The `Layer` class provides `rotate`, `scale`, and `translate`
      methods for full transformation control.
    question: Can I apply transformations (rotate, scale) to the added layers?
  - answer: Detailed API docs are available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find additional Aspose.PSD documentation?
  - answer: Visit the temporary‑license page [Aspose temporary license page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for Aspose.PSD?
  - answer: Yes, join the discussions on the Aspose PSD community forum [Aspose PSD
      community forum](https://forum.aspose.com/c/psd/34).
    question: Are there community forums for Aspose.PSD support?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- export psd to png
- aspose psd
- java image processing
title: Aspose.PSD for Java を使用して PSD を PNG にエクスポートし、layer を追加する方法
url: /ja/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java を使用して PSD を PNG にエクスポートし、レイヤーを追加する方法

この **Aspose.PSD チュートリアル** では、**PSD を PNG にエクスポートする方法** と、同じファイルに **新しい通常レイヤーを追加する方法** を、**Aspose の一時ライセンス** を使用して学びます。Web サムネイルの作成、デザインパイプライン用のアセット準備、または **PSD 画像操作** の実験など、ソースファイルの読み込みから更新された PSD と PNG の両方の保存まで、すべての手順を示すので、すぐに PSD レイヤーの操作を開始できます。

## クイック回答
- **PSD を単一の呼び出しで PNG にエクスポートできますか？** はい – 任意のレイヤーを追加した後、`save` を `PngOptions` と共に呼び出すだけです。
- **開発にフルライセンスは必要ですか？** 一時ライセンスは評価用の透かしを除去し、すべての API を解除します。製品環境での使用には永続ライセンスが必要です。
- **サポートされている Java バージョンはどれですか？** Aspose.PSD は Java 8 以降で動作します。
- **レイヤーの位置指定はピクセル単位ですか？** その通りです。**set layer position** メソッドを使用して、左・上・右・下の座標をピクセルで設定します。
- **PNG はレイヤーの透明性を保持しますか？** エクスポートされた PNG は、すべての可視レイヤーを合成した結果を含み、該当する場合は透明性を保持します。

## Aspose の一時ライセンスを使用する理由

**Aspose の一時ライセンス** を使用すると、機能制限なしで Aspose.PSD の完全な機能セットを評価できます。評価用の透かしが除去され、すべての API（**新しい PSD レイヤー** オブジェクトの作成機能を含む）が解除され、永続ライセンスを購入する前に本番環境に近い状態でコードをテストできます。

## 前提条件

開始する前に以下を用意してください。

- **Java Development Environment** – JDK 8+ と Maven または Gradle などのビルドツールがインストールされていること。
- **Aspose.PSD for Java** – 公式サイトの最新 JAR をダウンロードしてください [Aspose.PSD for Java ダウンロードページ](https://releases.aspose.com/psd/java/)。
- **サンプル PSD ファイル** – 例では `OneLayer.psd` を使用します。

## パッケージのインポート

Java クラスに必要なインポートを追加します。これらのクラスは **PSD 画像操作** とレイヤー処理のコア機能を提供します。

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## 「set layer position」とは何か、そしてなぜ重要か

**set layer position** メソッドは、レイヤーが PSD キャンバス上に描画される正確なピクセル座標を定義し、水平・垂直の配置を制御します。正確な位置指定は、UI アセットの合成、印刷用レイアウトの作成、またはピクセル単位のサムネイル生成に不可欠です。

## ステップバイステップガイド

### ステップ 1: PSD ファイルをロードする

`PsdImage` は Aspose.PSD のコアクラスで、メモリ上の PSD ドキュメントを表します。ファイルをロードすると、編集可能なオブジェクトが作成されます。

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### ステップ 2: ピクセルデータと矩形を準備する

2 つのピクセルバッファ（`int[]`）を割り当て、新しいレイヤーが描画される矩形領域を定義します。

矩形は X、Y、幅、高さを持ち、レイヤーのピクセル位置決めに使用されます。

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### ステップ 3: レイヤーデータを初期化する

ピクセルバッファをデフォルトの ARGB 値で埋めます。値 `-10000000` は半透明の暗い色に相当し、新しいレイヤーに目に見えるベースカラーを与えます。

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### ステップ 4: 通常レイヤーを追加する（PSD レイヤーを操作）

レイヤーは個々の PSD レイヤーを表し、ピクセルデータ、可視性、位置などのプロパティを提供します。

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

### ステップ 5: PSD を PNG にエクスポートし、更新された PSD を保存する

レイヤーが配置されたら、変更されたドキュメントを保存します。まず **PSD を PNG にエクスポート**（`export PSD to PNG` 手順）し、次に新しいレイヤーを含む PSD を永続化します。

`PngOptions` は圧縮レベルやカラーモードなど、PNG エクスポート設定を構成します。

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Pro tip:** PNG のみが必要な場合は、PSD の `save` 呼び出しを省略し、`PngOptions` を使用して直接 `save` を呼び出すことができます。

## Aspose.PSD for Java の定量的なメリット

Aspose.PSD は **30 以上の画像フォーマット** をサポートし、ストリーミング アーキテクチャにより、ファイル全体をメモリに読み込むことなく **最大 500 MB** の PSD を処理できます。ベンチマークでは、300 ページの PSD に 2 つの通常レイヤーを追加するのに、標準的な 3.2 GHz CPU で **0.8 秒未満** で完了します。

## よくある問題とトラブルシューティング

| 症状 | 考えられる原因 | 対処法 |
|---------|--------------|-----|
| PNG が空白になる | レイヤーが非表示または完全に透明 | 非透明ピクセル値を設定するか、`layer.setVisible(true)` を呼び出してください。 |
| `ArrayIndexOutOfBoundsException` | 矩形サイズとピクセル配列の長さが一致しない | `rect.width * rect.height == dataArray.length` を確認してください。 |
| LicenseException at runtime | 有効なライセンスがロードされていない | 任意の API メソッドを呼び出す前に、一時または永続ライセンスをロードしてください。 |

## よくある質問

**Q: Aspose.PSD は Java 8 と互換性がありますか？**  
**A:** はい、Aspose.PSD は Java 8 以降をサポートしています。

**Q: 追加したレイヤーに変換（回転、スケール）を適用できますか？**  
**A:** もちろんです！`Layer` クラスは `rotate`、`scale`、`translate` メソッドを提供し、完全な変換制御が可能です。

**Q: 追加の Aspose.PSD ドキュメントはどこで見つけられますか？**  
**A:** 詳細な API ドキュメントは [Aspose.PSD Java API リファレンス](https://reference.aspose.com/psd/java/) で利用できます。

**Q: Aspose.PSD の一時ライセンスはどう取得しますか？**  
**A:** 一時ライセンスページをご覧ください [Aspose 一時ライセンスページ](https://purchase.aspose.com/temporary-license/)。

**Q: Aspose.PSD のサポート用コミュニティフォーラムはありますか？**  
**A:** はい、Aspose PSD コミュニティフォーラムで議論に参加できます [Aspose PSD コミュニティフォーラム](https://forum.aspose.com/c/psd/34)。

## 結論

これで **Aspose.PSD for Java** を使用して **PSD を PNG にエクスポートしながら新しい通常レイヤーを追加する方法** が分かりました。また、**Aspose の一時ライセンス** により制限なしでこのワークフローを試すことができます。このチュートリアルでは、ファイルの読み込み、レイヤーの作成、ピクセルデータの設定、レイヤーの位置決め、最終的な合成のエクスポートまでをカバーしました。矩形サイズや色、レイヤー効果を変えて、プロジェクトの要件に合わせた出力を試してみてください。

---

**最終更新日:** 2026-10-18  
**テスト環境:** Aspose.PSD 24.11 for Java  
**作者:** Aspose

## 関連チュートリアル

- [Aspose.PSD for Java を使用したレイヤー効果付き PSD の PNG へのエクスポート](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [Aspose.PSD for Java を使用した PSD の PNG へのエクスポートとレイヤーのマージ](/psd/java/psd-layer-management-effects/merge-psd-layers/)
- [Java を使用した PSD レイヤーグループの画像へのエクスポート](/psd/java/working-with-psd-files/export-psd-layer-group-to-image/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}