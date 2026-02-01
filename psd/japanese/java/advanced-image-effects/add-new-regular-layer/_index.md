---
date: 2026-02-01
description: Aspose.PSD for Java を使用して、psd を png にエクスポートし、新しい psd レイヤーを作成する方法を学びます。このステップバイステップのチュートリアルでは、psd
  画像の操作と psd から png への変換について解説します。
linktitle: Add a New Regular Layer to PSD
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java を使用して PSD を PNG にエクスポートし、新しい通常レイヤーを追加
url: /ja/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java を使用して PSD を PNG にエクスポートし、新しいレギュラーレイヤーを追加する

## Introduction

この **aspose psd tutorial** では、**export PSD to PNG** の方法と、同じファイル内で **creating a new regular layer** の手順を学びます。Web 用サムネイルの生成、デザインパイプライン用アセットの準備、または単に **psd image manipulation** を試したい場合でも、Aspose.PSD for Java はプログラムからフルコントロールできる機能を提供します。ソースファイルの読み込みから、更新された PSD と PNG コピーの保存まで、すべての手順を順に解説するので、すぐに PSD レイヤーの操作を開始できます。

## How to export PSD to PNG using Aspose.PSD

PSD を PNG にエクスポートするには、まず必要なレイヤーを追加または変更し、次に `PngOptions` インスタンスを使用して `save` を呼び出すという 2 段階のプロセスが必要です。この方法により、**convert PSD to PNG** または **export PSD as PNG** をシンプルに実行できます。

## What is a regular layer and why add a new PSD layer?

**regular layer** は、ピクセルデータ、透明度、位置情報を保持できる基本的なラスターレイヤーです。新しい PSD レイヤーを追加すると、既存のアートワークを変更せずにグラフィック、透かし、プレースホルダーなどを挿入できます。これは、**add layer to PSD** を自動化バッチ処理でプログラム的に行う場合に特に有用です。

## Quick Answers
- **Can I export PSD to PNG with one call?** はい、レイヤーを追加した後、`PngOptions` を使用して `save` を呼び出すだけで可能です。
- **Do I need a license for development?** テスト用の一時ライセンスで動作しますが、本番環境ではフルライセンスが必要です。
- **Which Java version is supported?** Aspose.PSD は Java 8 以降をサポートしています。
- **Is layer positioning pixel‑based?** はい、左、上、右、下の座標はピクセル単位で設定します。
- **Will the PNG retain layer transparency?** PNG はすべての可視レイヤーをマージした結果を保持します。

## Prerequisites

開始する前に、以下を用意してください：

- **Java Development Environment** – JDK 8+ とビルドツール（Maven/Gradle）をインストール。
- **Aspose.PSD for Java** – 公式サイトから最新の JAR をダウンロード [here](https://releases.aspose.com/psd/java/)。
- **A sample PSD file** – 本例では `OneLayer.psd` を使用します。

## Import Packages

Java クラスに必要なインポートを追加します。これらのクラスは **psd image manipulation** とレイヤー操作のコア機能を提供します。

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Step 1: Load the PSD File

まず、変更したい既存の PSD を読み込みます。これにより操作対象の `PsdImage` オブジェクトが取得できます。

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## Step 2: Prepare Pixel Data and Rectangles

2 つのピクセルバッファ（`int[]`）を作成し、新しいレイヤーを描画する矩形領域を定義します。これは **creating a new PSD layer** の基礎となります。

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

## Step 3: Initialize Layer Data

ピクセルバッファにデフォルトの ARGB 値を設定します。値 `-10000000` は半透明の暗い色に相当します。

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

## Step 4: Add Regular Layers (Manipulate PSD Layers)

ここで **add regular layers** を PSD 画像に追加し、境界を設定します。これにより **manipulate PSD layers** をプログラム的に実行し、効果的に **add layer to PSD** が行えます。

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

## Step 5: Export PSD to PNG and Save the Updated PSD

レイヤーが配置されたら、変更されたドキュメントを保存します。まず PNG にエクスポート（**export psd to png** 手順）し、次に新しいレイヤーを含む PSD を永続化します。

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Pro tip:** PNG だけが必要な場合は、PSD の `save` 呼び出しを省略し、`PngOptions` で直接 `save` すれば完了です。

## Common Issues & Troubleshooting

| Symptom | Likely Cause | Fix |
|---------|--------------|-----|
| PNG appears blank | Layers are invisible or fully transparent | Ensure you set non‑transparent pixel values or| `ArrayIndexOutOfBoundsException` | Mismatch between rectangle size and pixel array length | Verify that `rect.width * rect.height == dataArray.length`. |
| LicenseException at runtime | No valid license loaded | Load a temporary or permanent license before calling any API methods. |

## Frequently Asked Questions

**Q: Is Aspose.PSD compatible with Java 8?**  
A: Yes, Aspose.PSD supports Java 8 and later versions.

**Q: Can I apply transformations (rotate, scale) to the added layers?**  
A: Absolutely! The `Layer` class provides methods such as `rotate`, `scale`, and `translate` for full transformation control.

**Q: Where can I find additional Aspose.PSD documentation?**  
A: Detailed API docs are available [here](https://reference.aspose.com/psd/java/).

**Q: How do I obtain a temporary license for Aspose.PSD?**  
A: Visit the temporary‑license page [here](https://purchase.aspose.com/temporary-license/).

**Q: Are there community forums for Aspose.PSD support?**  
A: Yes, join the discussions on the Aspose forums [here](https://forum.aspose.com/c/psd/34).

## Conclusion

これで **export PSD to PNG** と **adding new regular layers** を Aspose.PSD for Java で実行する方法を習得しました。このワークフローは、ファイルの読み込み、レイヤーの作成、ピクセルデータの設定、最終的な合成画像のエクスポートという **psd image manipulation** の主要機能を示しています。矩形サイズ、ピクセルカラー、レイヤー効果などを自由に試して、プロジェクトの要件に合わせた出力を作り出してください。

---

**Last Updated**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}