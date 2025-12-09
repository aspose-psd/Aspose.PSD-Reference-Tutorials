---
date: 2025-11-30
description: Aspose.PSD for Java を使用してストロークを追加し、PSD のストロークカラーを変更する方法を学びましょう。このステップバイステップガイドに従って、ストロークレイヤーの色と不透明度を変更してください。
linktitle: Add Stroke Layer Color
second_title: Aspose.PSD Java API
title: Aspose.PSD for Javaでストロークレイヤーの色を追加する方法
url: /ja/java/advanced-image-effects/add-stroke-layer-color/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java でストロークレイヤーの色を追加する方法

## Introduction

Photoshop ドキュメントにプログラムで **ストロークを追加する方法** が必要な場合、Aspose.PSD for Java を使えば簡単に実装できます。このチュートリアルでは、ストロークレイヤーの色を追加し、透明度を調整し、結果を保存する手順を解説します。最後には、既存レイヤーの **ストロークの色を変更する方法**（*change PSD stroke color*）も確認でき、Java コードからフルコントロールが可能になります。

## Quick Answers
- **必要なライブラリは？** Aspose.PSD for Java（最新バージョン）。  
- **ストロークの色は変更できるか？** はい – `ColorFillSettings` を使って任意の `Color` を設定できます。  
- **ライセンスは必要か？** 評価用の一時ライセンスで動作しますが、本番環境ではフルライセンスが必要です。  
- **対応 Java バージョンは？** Java 8 以上。  
- **実装にかかる時間は？** 基本的なストローク変更であれば通常 10 分未満です。

## What is a Stroke Layer in a PSD?
ストロークレイヤーは、レイヤーの内容の周囲に輪郭線を描画するベクターエフェクトです。色、太さ、透明度、ブレンドモードをカスタマイズできます。プログラムからこのエフェクトを変更することで、ブランドの自動適用やバッチ処理、動的グラフィック生成が可能になります。

## Why Use Aspose.PSD to Change Stroke Color?
- **Photoshop が不要** – 完全に Java だけで作業できます。  
- **PSD 仕様に完全準拠** – 最新の PSD 機能すべてをサポート。  
- **高性能** – 大容量ファイルも高速に処理。  
- **クロスプラットフォーム** – JVM が動作する任意の OS で実行可能。

## Prerequisites

- **Aspose.PSD Library** – [公式ドキュメント](https://reference.aspose.com/psd/java/) からダウンロード。  
- **Java Development Kit (JDK)** – バージョン 8 以上。  
- **IDE** – Eclipse、IntelliJ IDEA、または任意の Java 対応エディタ。

## Import Packages

まず、必要なクラスをインポートします。これにより、PSD の操作とストロークエフェクト API が利用可能になります。

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Step 1: Set Up Your Project

新規 Java プロジェクトを作成し、Aspose.PSD の JAR をビルドパスに追加して、エラーなくライブラリがロードされることを確認します。

## Step 2: Load the PSD File

エフェクトリソースの読み込みを有効にし、ストローク情報が取得できるようにします。

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Step 3: Access the Stroke Effect Layer

2 番目のレイヤー（インデックス 1）から最初のストロークエフェクトを取得します。

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## Step 4: Validate Stroke Properties

変更前に既存プロパティを確認します。これにより予期しない結果を防げます。

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

## Step 5: Set Color and Opacity (How to Change Stroke Color)

ここで **PSD のストローク色を黄色に変更** し、透明度を 50 %（127 / 255）に設定します。

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

## Step 6: Save the Modified PSD

更新した画像をディスクに書き出します。新しいファイルには変更されたストロークが含まれます。

```java
im.save(exportPath);
```

## Common Pitfalls & Tips

- **Null チェック** – `getEffects()` が null でない配列を返すことを必ず確認してからキャストしてください。  
- **レイヤーインデックス** – PSD のレイヤーは 0 から始まります。対象レイヤーが正しいか確認しましょう。  
- **カラー形式** – `Color.getYellow()` は例示です。`new Color(r, g, b)` でカスタムカラーも作成可能です。  
- **透明度の範囲** – 透明度はバイト値（0–255）です。255 を超える値はクランプされます。

## Conclusion

これで **PSD にストロークを追加する方法** と **ストロークの色を変更する方法** を Aspose.PSD for Java を使って習得できました。さまざまな色、ブレンドモード、透明度を試して、プロジェクトに最適なビジュアルスタイルを実現してください。

## Frequently Asked Questions

**Q: Aspose.PSD を他の Java グラフィックライブラリと併用できますか？**  
A: はい、Apache Commons Imaging や Java2D などと組み合わせて、機能を拡張できます。

**Q: 最新の PSD ファイル形式に対応していますか？**  
A: もちろんです。ライブラリは定期的に更新され、最新の Photoshop 仕様をサポートしています。

**Q: Aspose.PSD 使用時の例外処理はどうすればよいですか？**  
A: 詳細なトラブルシューティングとサンプル例外処理コードは [サポートフォーラム](https://forum.aspose.com/c/psd/34) を参照してください。

**Q: 購入前に Aspose.PSD を試すことはできますか？**  
A: もちろんです！すべての機能を体験できる [無料トライアル](https://releases.aspose.com/) をご利用ください。

**Q: Aspose.PSD の一時ライセンスはどこで取得できますか？**  
A: 開発環境で評価するための [一時ライセンス](https://purchase.aspose.com/temporary-license/) を取得してください。

---

**Last Updated:** 2025-11-30  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}