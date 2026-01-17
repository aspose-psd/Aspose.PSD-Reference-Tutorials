---
date: 2026-01-17
description: Aspose.PSD for Java を使用してストロークパターンを追加する方法を学びましょう。ステップバイステップのガイドに従って、PSD
  画像をすばやく強化してください。
linktitle: How to Add Stroke Layer Pattern in Java
second_title: Aspose.PSD Java API
title: Aspose.PSD を使用した Java でのストロークパターンの追加方法
url: /ja/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD を使用した Stroke Pattern の追加方法（Java）

## Introduction
Photoshop ファイルに **stroke pattern java** を追加したい場合、Aspose.PSD for Java を使えば驚くほど簡単に実現できます。グラフィックデザインツールの構築、バッチ編集の自動化、あるいはレイヤー効果の実験など、今回のチュートリアルでは PSD の読み込みから新しいパターンの検証まで、すべての手順を詳しく解説します。さっそく画像を強化する方法を見てみましょう。

## Quick Answers
- **どのライブラリが必要ですか？** Aspose.PSD for Java  
- **対応している Java のバージョンは？** JDK 8 以降  
- **テスト用にライセンスは必要ですか？** 開発段階は無料トライアルで可。製品版ではライセンスが必要です。  
- **実装にかかる時間は？** 基本的なパターンストロークでおおよそ 10‑15 分程度  
- **複数のレイヤーでパターンを再利用できますか？** はい、同じ `PattResource` を他のレイヤーに割り当てるだけです  

## What is add stroke pattern java?
Java でストロークパターンを追加するとは、レイヤーのストローク効果にカスタムフィル（通常は繰り返しビットマップ）を適用することを指します。この手法を使うと、破線やレンガテクスチャ、独自のグラフィック枠など、PSD ファイル内で直接スタイライズされた輪郭を作成できます。Photoshop を開く必要はありません。

## Why Use Aspose.PSD for add stroke pattern java?
- **Full PSD fidelity** – すべてのレイヤー効果、リソース、ブレンドモードがそのまま保持されます。  
- **No native Photoshop required** – JDK があれば OS を問わず動作します。  
- **Programmatic control** – バッチ処理の自動化やサーバーサイドサービスへの統合が可能です。  
- **Rich API** – グローバルリソース、パターンフィル、ブレンドモードを単一のフルエントインターフェイスで操作できます。

## Prerequisites
- **Java Development Kit (JDK)** – JDK 8 以上がインストールされていることを確認してください。  
- **Aspose.PSD for Java** – ライブラリは [here](https://releases.aspose.com/psd/java/) からダウンロードし、プロジェクトのクラスパスに JAR を追加します。  
- **IDE** – IntelliJ IDEA、Eclipse、またはお好みのエディタを使用します。

## Import Packages
まず、PSD ファイル、カラー、矩形、ストローク効果を扱うために必要なクラスをインポートします。

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```

## Step 1: Load the PSD File
対象の PSD を読み込み、レイヤーやリソースにアクセスできるようにします。

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Step 2: Prepare New Pattern Data
ストロークに使用するシンプルな 4 × 4 ピクセルのパターンを作成します。

```java
int[] newPattern = new int[]
{
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
};
Rectangle newPatternBounds = new Rectangle(0, 0, 4, 4);
UUID guid = UUID.randomUUID();
```

## Step 3: Access the Stroke Effect
対象レイヤー（この例では 4 番目のレイヤー）に設定されているストローク効果を取得します。

```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```

## Step 4: Modify the Stroke Effect
### Update Stroke Effect Properties
不透明度とブレンドモードを調整し、新しいパターンの視覚的影響を確認します。

```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```

### Update the Pattern Resource
既存のグローバルパターンリソースを、先ほど作成したものに置き換えます。

```java
PattResource resource;
for (int i = 0; i < im.getGlobalLayerResources().length; i++)
{
    if (im.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
        resource.setPattern(newPattern, newPatternBounds);
    }
}
```

## Step 5: Apply the New Pattern
更新したパターンリソースをストローク効果にバインドし、PSD を保存します。

```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

## Step 6: Verify the Changes
ファイルを再度読み込み、新しいパターン・不透明度・ブレンドモードが正しく適用されていることを確認します。

```java
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
PattResource resource1 = null;
for (int i = 0; i < img.getGlobalLayerResources().length; i++)
{
    if (img.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource1 = (PattResource)img.getGlobalLayerResources()[i];
    }
}
try
{
    Assert.areEqual(newPattern, resource1.getPatternData());
    Assert.areEqual(newPatternBounds, new Rectangle(0, 0, resource1.getWidth(), resource1.getHeight()));
    Assert.areEqual(guid.toString(), resource1.getPatternId());
    Assert.areEqual(BlendMode.Color, patternStrokeEffect.getBlendMode());
    Assert.areEqual(127, patternStrokeEffect.getOpacity());
    Assert.areEqual(true, patternStrokeEffect.isVisible());
    PatternFillSettings fillSettings1 = (PatternFillSettings)patternStrokeEffect.getFillSettings();
    Assert.areEqual(FillType.Pattern, fillSettings1.getFillType());
}
catch (Exception e)
{
    System.out.println(e.getMessage());
}
```

## Common Issues and Solutions
| Issue | Cause | Fix |
|-------|-------|-----|
| パターンが表示されない | `PatternId` の参照が間違っている | `PattResource` に設定した `PatternId` が `PatternFillSettings` で使用されているものと一致していることを確認してください。 |
| 保存後にストロークが消える | 不透明度が 0 に設定されている、またはエフェクトが非表示 | `setOpacity` が 0‑255 の範囲内であること、`isVisible()` が `true` を返すことを確認してください。 |
| 予期しない色になる | ブレンドモードの不一致 | デザイン意図に合った `BlendMode.Color`（または他のモード）を使用してください。 |

## FAQ's
### Aspose.PSD for Java とは何ですか？
Aspose.PSD for Java は、開発者がプログラムから PSD（Photoshop Document）ファイルを作成、編集、変換できるようにするライブラリです。

### 商用プロジェクトで Aspose.PSD for Java を使用できますか？
はい、商用プロジェクトでも使用可能です。ライセンスは [here](https://purchase.aspose.com/buy) から購入できます。

### Aspose.PSD for Java の無料トライアルはありますか？
はい、無料トライアル版は [here](https://releases.aspose.com/) からダウンロードできます。

### Aspose.PSD for Java のサポートはどこで受けられますか？
サポートは Aspose コミュニティフォーラム [here](https://forum.aspose.com/c/psd/34) で受けられます。

### Aspose.PSD for Java のシステム要件は何ですか？
JDK がインストールされた環境と開発用 IDE が必要です。ライブラリは Windows、Linux、macOS など複数の OS をサポートしています。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最終更新日:** 2026-01-17  
**テスト環境:** Aspose.PSD for Java 24.12（執筆時点の最新バージョン）  
**作者:** Aspose