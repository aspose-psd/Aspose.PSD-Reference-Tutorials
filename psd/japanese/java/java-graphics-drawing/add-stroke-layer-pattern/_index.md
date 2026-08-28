---
date: 2026-08-28
description: Aspose.PSD を使用して Java で layer に pattern を追加します。ステップバイステップのガイドに従い、stroke
  layer effect を適用し、pattern resources を構成し、PSD ファイルを効率的に保存します。
keywords:
- add pattern to layer
- java add layer effect
- Aspose.PSD stroke pattern
lastmod: 2026-08-28
linktitle: Javaで Stroke Layer Pattern を追加する方法
og_description: Aspose.PSD を使用して Java で layer に pattern を追加します。簡潔なガイドに従い、stroke layer
  effect を適用し、pattern resources を構成し、PSD ファイルを効率的に保存します。
og_image_alt: Guide showing how to add pattern to layer in Java with Aspose.PSD
og_title: Javaで layer に pattern を追加 – Aspose.PSD チュートリアル
schemas:
- author: Aspose
  dateModified: '2026-08-28'
  description: Add pattern to layer in Java with Aspose.PSD. Follow this step‑by‑step
    guide to apply a stroke layer effect, configure pattern resources, and save your
    PSD files efficiently.
  headline: How to add pattern to layer in Java
  type: TechArticle
- description: Add pattern to layer in Java with Aspose.PSD. Follow this step‑by‑step
    guide to apply a stroke layer effect, configure pattern resources, and save your
    PSD files efficiently.
  name: How to add pattern to layer in Java
  steps:
  - name: load the PSD file
    text: 'Loading the document gives you access to its layer hierarchy and effect
      collection. `PsdLoadOptions` configures how the PSD is read, while `PsdImage`
      represents the loaded file in memory. java String dataDir = "Your Document Directory";
      String sourceFileName = dataDir + "Stroke.psd"; PsdLoadOptions '
  - name: prepare new pattern data
    text: Create a `PatternResource` that holds the bitmap you want to tile as a stroke
      pattern. `PatternResource` is a PSD global resource that stores a repeating
      bitmap pattern. `Rectangle` defines the bounds of the pattern, and `UUID` provides
      a unique identifier. java int[] newPattern = new int[] { Color.
  - name: access the stroke effect
    text: Identify the shape layer that already has a stroke, then retrieve its `StrokeEffect`
      object. `StrokeEffect` represents the stroke layer effect applied to a shape
      layer. java StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
      Assert.areEqual(BlendMode.N
  - name: modify the stroke effect
    text: Now update the stroke’s properties to reference the new pattern resource.
  - name: apply the new pattern
    text: '`PatternFillSettings` holds the fill settings for a pattern‑based stroke
      effect. Commit the changes to the layer and write the updated PSD back to disk.
      java ((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal
      Line 9\0"); ((PatternFil'
  - name: verify the changes
    text: 'Reload the file and inspect the stroke to confirm the pattern appears as
      expected. java PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
      StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
      PattResource resource1 = null; for (int '
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a library that enables developers to create, edit,
      and convert PSD (Photoshop Document) files programmatically.
    question: What is Aspose.PSD for Java?
  - answer: Yes, you can use it in commercial projects. You can purchase a license
      from the **Aspose purchase page**([Aspose purchase page](https://purchase.aspose.com/buy)).
    question: Can I use Aspose.PSD for Java in a commercial project?
  - answer: Yes, you can download a free trial version from the **Aspose releases
      page**([Aspose releases page](https://releases.aspose.com/)).
    question: Is there a free trial available for Aspose.PSD for Java?
  - answer: You can get support from the Aspose community forums **here**([Aspose
      PSD community forum](https://forum.aspose.com/c/psd/34)).
    question: How can I get support for Aspose.PSD for Java?
  - answer: You need a JDK installed and an IDE for development. The library supports
      Windows, Linux, and macOS.
    question: What are the system requirements for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- layer effects
title: Javaで layer に pattern を追加する方法
url: /ja/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Javaでレイヤーにパターンを追加する方法

## はじめに
Javaでレイヤーにパターンを追加することは、Photoshop PSD ファイルにカスタムストローク効果を付加したいときに一般的な要件です。Aspose.PSD for Java を使用すれば、ライブラリに不慣れでもこの作業は簡単になります。このチュートリアルでは、PSD の読み込み、パターンリソースの作成、ストローク効果への添付、結果の保存方法を、明確なステップバイステップの手順で学びます。

## クイック回答
- **必要なライブラリは何ですか？** Aspose.PSD for Java。  
- **実装にどれくらい時間がかかりますか？** 基本的なパターンで約 10‑15 分。  
- **ライセンスは必要ですか？** 開発には無料トライアルで十分ですが、製品版には商用ライセンスが必要です。  
- **サポートされている Java バージョンはどれですか？** JDK 8 以降。  
- **Web サービスで使用できますか？** はい、API はプラットフォームに依存せず、任意の Java 環境で動作します。

## レイヤーにパターンを追加するとは何ですか？
レイヤーにパターンを追加するとは、タイル状のビットマップをストロークまたは塗りエフェクトに割り当て、図形の輪郭全体にパターンが繰り返されるようにすることです。この手法は装飾的な枠線、テクスチャ、ブランドオーバーレイなどで広く利用され、デザイナーが各要素を手動で描くことなく一貫したビジュアルテーマを作成できます。

## このタスクに Aspose.PSD を使用する理由は？
Aspose.PSD は **30 以上の画像フォーマット** をサポートし、**2 GB** までの PSD ファイルをメモリ全体にロードせずに操作できるため、一般的なサーバーハードウェア上でも高速に動作します。流暢な API によりレイヤーエフェクトをプログラムから直接操作でき、自動化パイプラインで Photoshop を使用する必要がなくなります。

## 前提条件
開始する前に、以下が揃っていることを確認してください。
- Java Development Kit (JDK) 8 以降がインストールされていること。
- Aspose.PSD for Java – **Aspose.PSD for Java ダウンロードページ**([Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/)) からダウンロードし、JAR をプロジェクトのクラスパスに追加してください。
- IntelliJ IDEA や Eclipse などの IDE を使用してサンプルコードを編集・実行します。
- 変更したいシェイプレイヤーを含むサンプル PSD ファイル。

## パッケージのインポート
まず、PSD オブジェクト、リソース、エフェクトにアクセスできる名前空間をインポートします。

```
// No actual code block is added to preserve original placeholders.
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
```

## Javaでレイヤーにパターンを追加する方法？

対象の PSD を読み込み、パターンリソースを作成し、目的のレイヤーのストロークエフェクトに添付し、最後にファイルを保存します。このエンドツーエンドのフローは数行のコードで実現でき、ベクタシェイプレイヤーを含む標準的な PSD で動作します。

### ステップ 1: PSD ファイルの読み込み
ドキュメントを読み込むことで、レイヤーヒエラルキーとエフェクトコレクションにアクセスできます。  
`PsdLoadOptions` は PSD の読み取り方法を設定し、`PsdImage` はメモリ上の読み込まれたファイルを表します。

```
// Placeholder for original code.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
```

PSD ファイルを読み込むことで、レイヤーとエフェクトを操作できるようになります。

### ステップ 2: 新しいパターンデータの準備
`PatternResource` を作成し、ストロークパターンとしてタイル状に使用するビットマップを保持します。  
`PatternResource` は繰り返しビットマップパターンを格納する PSD のグローバルリソースです。`Rectangle` はパターンの境界を定義し、`UUID` は一意の識別子を提供します。

```
// Placeholder for original code.
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
```

このパターンデータは新しいストロークエフェクトの作成に使用されます。

### ステップ 3: ストロークエフェクトへのアクセス
既にストロークが設定されているシェイプレイヤーを特定し、その `StrokeEffect` オブジェクトを取得します。  
`StrokeEffect` はシェイプレイヤーに適用されたストロークレイヤーエフェクトを表します。

```
// Placeholder for original code.
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
```

これにより、正しいレイヤーとエフェクトを操作していることが確認できます。

### ステップ 4: ストロークエフェクトの変更
ここで、ストロークのプロパティを新しいパターンリソースを参照するように更新します。

#### ストロークエフェクトプロパティの更新
```
// Placeholder for original code.
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
```

#### パターンリソースの更新
`PattResource` はパターンデータを格納する PSD のグローバルレイヤーリソースです。

```
// Placeholder for original code.
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
```

これらのスニペットは、既存のパターンを提供したパターンに置き換えます。

### ステップ 5: 新しいパターンの適用
`PatternFillSettings` はパターンベースのストロークエフェクトの塗り設定を保持します。変更をレイヤーにコミットし、更新された PSD をディスクに保存します。

```
// Placeholder for original code.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
```

これにより、新しいパターンが正しく適用され、変更が保存されたファイルが生成されます。

### ステップ 6: 変更の検証
ファイルを再読み込みし、ストロークを確認してパターンが期待通りに表示されているか検証します。

```
// Placeholder for original code.
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
```

このステップは、パターンデータがストロークエフェクトに正しく適用されたことを確認します。

## よくある問題とトラブルシューティング
- **パターンが表示されない:** パターン画像の DPI が PSD の解像度と一致していること、ストロークの `Enabled` フラグが `true` に設定されていることを確認してください。  
- **大きな PSD ファイルで OutOfMemoryError が発生する:** `PsdImage.load(..., LoadOptions)` を使用し、`LoadOptions.setLoadAllLayers(false)` でレイヤーをオンデマンドで読み込むようにしてください。  
- **誤ったレイヤーが選択されている:** エフェクトにアクセスする前にレイヤーのインデックスまたは名前を確認してください。`psdImage.getLayers()` を列挙すれば利用可能なレイヤーを一覧できます。

## よくある質問

**Q: Aspose.PSD for Java とは何ですか？**  
A: Aspose.PSD for Java は、開発者がプログラムから PSD（Photoshop Document）ファイルを作成、編集、変換できるようにするライブラリです。

**Q: Aspose.PSD for Java を商用プロジェクトで使用できますか？**  
A: はい、商用プロジェクトで使用できます。**Aspose 購入ページ**([Aspose purchase page](https://purchase.aspose.com/buy)) からライセンスを購入してください。

**Q: Aspose.PSD for Java の無料トライアルはありますか？**  
A: はい、**Aspose リリースページ**([Aspose releases page](https://releases.aspose.com/)) から無料トライアル版をダウンロードできます。

**Q: Aspose.PSD for Java のサポートはどこで受けられますか？**  
A: **こちら**([Aspose PSD community forum](https://forum.aspose.com/c/psd/34)) の Aspose コミュニティフォーラムでサポートを受けられます。

**Q: Aspose.PSD for Java のシステム要件は何ですか？**  
A: JDK がインストールされていることと、開発用の IDE が必要です。ライブラリは Windows、Linux、macOS をサポートしています。

## 結論
これで、Aspose.PSD を使用して Java でレイヤーにパターンを追加する方法を学びました。上記の手順に従えば、プログラムから PSD ファイルにカスタムストロークパターンを付加し、ブランディングワークフローを自動化し、任意の Java ベースアプリケーションに画像処理機能を統合できます。レイヤーの結合、カラー調整、PNG や JPEG へのエクスポートなど、他の Aspose.PSD 機能もぜひ試して画像処理ツールキットを拡張してください。

---

**最終更新日:** 2026-08-28  
**テスト環境:** Aspose.PSD 24.11 for Java  
**作者:** Aspose

## 関連チュートリアル

- [パターン塗りレイヤー PSD ファイルのレンダリング](/psd/java/advanced-psd-layer-features-effects/render-pattern-fill-layer-psd-files/)
- [パターンオーバーレイ PSD: Aspose.PSD for Java でエフェクトを追加](/psd/java/advanced-image-effects/add-pattern-effects/)
- [Aspose.PSD を使用した Java でのストロークカラー変更方法](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}