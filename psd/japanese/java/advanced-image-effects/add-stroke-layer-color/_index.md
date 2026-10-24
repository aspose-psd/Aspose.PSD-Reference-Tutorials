---
date: 2026-10-24
description: Aspose.PSD for Java を使用して Java でストロークレイヤーを作成する方法を学びましょう。このステップバイステップガイドでは、ストロークレイヤーの追加、色の変更、不透明度の調整、そして
  PSD の保存方法を示します。
keywords:
- create stroke layer java
- change stroke color java
- modify stroke opacity
- apply stroke effect
- psd stroke tutorial
lastmod: 2026-10-24
linktitle: ストロークレイヤーの色を追加
og_description: Aspose.PSD for Java を使用して Java のストロークレイヤーを作成します。この簡潔なチュートリアルに従って、ストロークレイヤーの追加、色の変更、不透明度の調整、そして
  PSD ファイルのエクスポートを行いましょう。
og_image_alt: Screenshot of a Java IDE showing Aspose.PSD code that creates and modifies
  a stroke layer in a PSD file
og_title: Aspose.PSD で Java のストロークレイヤーを作成 – クイックガイド
schemas:
- author: Aspose
  dateModified: '2026-10-24'
  description: Learn how to create stroke layer Java with Aspose.PSD for Java. This
    step‑by‑step guide shows you how to add a stroke layer, change its color, adjust
    opacity, and save the PSD.
  headline: How to create stroke layer Java using Aspose.PSD
  type: TechArticle
- description: Learn how to create stroke layer Java with Aspose.PSD for Java. This
    step‑by‑step guide shows you how to add a stroke layer, change its color, adjust
    opacity, and save the PSD.
  name: How to create stroke layer Java using Aspose.PSD
  steps:
  - name: set up your project
    text: Create a new Java project, add the Aspose.PSD JAR to the build path, and
      verify the library loads without errors.
  - name: load the PSD file
    text: Enable loading of effect resources so the stroke information is available.
  - name: access the stroke effect layer
    text: '`StrokeEffect` is Aspose.PSD’s class that represents a vector outline applied
      to a layer. Retrieve the first stroke effect from the second layer (index 1).'
  - name: validate stroke properties
    text: '`ColorFillSettings` holds the color and opacity values for a stroke. Confirm
      the existing properties before making changes to avoid unexpected results.'
  - name: set color and opacity (how to change stroke color)
    text: Here we **change stroke color** to yellow and reduce opacity to 50 % (127
      / 255). `ColorFillSettings` also lets you specify blend mode and size.
  - name: save the modified PSD
    text: Write the updated image back to disk. The new file now contains the modified
      stroke.
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD can be combined with libraries such as Apache Commons
      Imaging or Java2D for extended functionality.
    question: Can I use Aspose.PSD with other Java graphic libraries?
  - answer: Absolutely. The library supports the newest Photoshop specifications and
      over 150 PSD features.
    question: Is Aspose.PSD compatible with the latest PSD file format?
  - answer: Wrap your code in try‑catch blocks and consult the [support forum](https://forum.aspose.com/c/psd/34)
      for detailed troubleshooting examples.
    question: How do I handle exceptions while using Aspose.PSD?
  - answer: Certainly! Grab a [free trial](https://releases.aspose.com/) to explore
      all features.
    question: Can I try Aspose.PSD before purchasing?
  - answer: Obtain a [temporary license](https://purchase.aspose.com/temporary-license/)
      to evaluate the library in your development environment.
    question: Where can I get a temporary license for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- create stroke layer
- Aspose.PSD
- Java image processing
title: Aspose.PSD を使用した Java でのストロークレイヤーの作成方法
url: /ja/java/advanced-image-effects/add-stroke-layer-color/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Javaでストロークレイヤーを作成する方法 Aspose.PSD を使用して

## はじめに

プログラムで Photoshop ドキュメントに **create stroke layer Java** を作成する必要がある場合、Aspose.PSD for Java はクリーンなコードファーストアプローチを提供します。このチュートリアルでは、新しいストロークレイヤーの追加、色の変更、不透明度の調整、結果の保存方法を、Photoshop を起動せずに学びます。最後には、既存レイヤーのストロークを編集する方法も理解でき、Java アプリケーションから直接フルコントロールが可能になります。

## クイック回答
- **必要なライブラリは何ですか？** Aspose.PSD for Java (latest version)。  
- **ストロークの色を変更できますか？** はい – 任意の `Color` を設定するには `ColorFillSettings` を使用します。  
- **ライセンスは必要ですか？** 評価用の一時ライセンスで動作しますが、本番環境ではフルライセンスが必要です。  
- **サポートされている Java バージョンはどれですか？** Java 8 以上。  
- **実装にどれくらい時間がかかりますか？** 基本的なストローク変更で通常 10 分未満です。

## PSD のストロークレイヤーとは何ですか？
ストロークレイヤーは、レイヤーの内容の周囲にアウトラインを描画するベクターエフェクトです。色、太さ、不透明度、ブレンドモードでカスタマイズできます。このエフェクトをプログラムで変更することで、ブランドの自動化、バッチ処理、動的グラフィック生成が可能になります。

## なぜ Aspose.PSD を使用してストロークの色を変更するのか？
Aspose.PSD は **150+** の PSD 機能をサポートし、ベクターマスク、スマートオブジェクト、レイヤーエフェクトなどを含みます。マルチハンドルの数百ページファイルでもドキュメント全体をメモリにロードせずに処理できます。JVM が動作する任意の OS で動作し、典型的なアセットでサブ秒のパフォーマンスを提供し、Photoshop のインストールは不要です。

## Java でストロークレイヤーを作成する方法は？

PSD をロードし、ストロークエフェクトを追加し、外観を設定してファイルを保存します—数行のシンプルなコードで完了します。以下の回答で手順に入る前に、正確に何をすべきかを示します。

**直接回答（40‑70 語）：**  
`PsdImage` は PSD ドキュメントを表し、ファイルのロードと保存のメソッドを提供します。まず `PsdImage.load("input.psd", loadOptions)` で PSD をロードします。新しい `StrokeEffect` を作成し、`ColorFillSettings` に目的の `Color` を設定し、不透明度とサイズを調整したら、対象レイヤーの `BlendingOptions` にエフェクトを添付します。最後に `psd.save("output.psd", SaveFormat.PSD)` を呼び出します。このシーケンスで Aspose.PSD を使用した Java のストロークレイヤーが作成されます。

### 前提条件

- **Aspose.PSD ライブラリ** – [公式ドキュメント](https://reference.aspose.com/psd/java/) からダウンロードしてください。  
- **Java Development Kit (JDK)** – バージョン 8 以上。  
- **IDE** – Eclipse、IntelliJ IDEA、または任意の Java 対応エディタ。

### パッケージのインポート

まず、必要なクラスをインポートします。これにより、プロジェクトが PSD 処理とストロークエフェクト API にアクセスできるようになります。

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

### 手順 1: プロジェクトの設定

新しい Java プロジェクトを作成し、Aspose.PSD JAR をビルドパスに追加し、ライブラリがエラーなくロードされることを確認します。

### 手順 2: PSD ファイルの読み込み

ストローク情報が利用できるように、エフェクトリソースのロードを有効にします。

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

### 手順 3: ストロークエフェクトレイヤーへのアクセス

`StrokeEffect` はレイヤーに適用されるベクターアウトラインを表す Aspose.PSD のクラスです。2 番目のレイヤー（インデックス 1）から最初のストロークエフェクトを取得します。

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

### 手順 4: ストロークプロパティの検証

`ColorFillSettings` はストロークの色と不透明度の値を保持します。変更を加える前に既存のプロパティを確認し、予期しない結果を防ぎます。

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

### 手順 5: 色と不透明度の設定（ストロークの色を変更する方法）

ここでは **change stroke color** を黄色に変更し、不透明度を 50 %（127 / 255）に減らします。`ColorFillSettings` ではブレンドモードやサイズも指定できます。

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

### 手順 6: 変更された PSD の保存

更新された画像をディスクに書き戻します。新しいファイルには変更されたストロークが含まれます。

```java
im.save(exportPath);
```

## Java でストロークの色を変更する方法は？

`Color` は ARGB カラー値を表します。PSD をロードし、対象レイヤーを特定し、`ColorFillSettings` に新しい `Color` を設定してファイルを保存します。この操作は数行のコードで済み、典型的なアセットでは 1 秒未満で完了するため、迅速かつ効率的です。

**直接回答（40‑70 語）：**  
`layer.getEffects().getStrokeEffect()` で既存のストロークを取得し、`stroke.getColorFillSettings().setColor(Color.getRed())`（または必要な任意の `Color`）を呼び出します。必要に応じて `setOpacity((byte)200)` で 78 % の不透明度に調整し、`psd.save("output.psd", SaveFormat.PSD)` で PSD を保存します。変更は即座に適用され、ドキュメント全体の再レンダリングは不要です。

## ストロークの不透明度を変更する方法は？

元の色を保持したまま不透明度だけを調整したい場合は、`ColorFillSettings` の `setOpacity` 値（0‑255）を変更します。例として、`colorStroke.setOpacity((byte)200);` はストロークを約 78 % の不透明度にします。不透明度を調整することで、微妙なアウトラインから完全に不透明なストロークまで、デザイン要件に合わせて表現できます。

**直接回答（40‑70 語）：**  
目的のレイヤーから `StrokeEffect` を取得し、`stroke.getColorFillSettings().setOpacity((byte)desiredValue)` を呼び出します。`desiredValue` は 0（透明）から 255（完全不透明）までの範囲です。PSD を保存すれば新しい不透明度が即座に反映されます。この方法は元の色に関係なく、既存のストロークすべてに適用可能です。

## ストロークエフェクトを適用する方法は？

ストロークエフェクトがまだないレイヤーに新しいストロークを追加するには、`StrokeEffect` インスタンスを作成し、`ColorFillSettings` を設定してからレイヤーの `BlendingOptions` に添付します。同じ `setColor` と `setOpacity` メソッドで外観を定義します。

**直接回答（40‑70 語）：**  
`StrokeEffect newStroke = new StrokeEffect(); newStroke.getColorFillSettings().setColor(Color.getBlue()); newStroke.getColorFillSettings().setOpacity((byte)255); layer.getBlendingOptions().setEffect(newStroke);` エフェクトを添付したら PSD を保存します。これにより、ドキュメント内の任意の既存レイヤーに新しい、完全にカスタマイズ可能なストロークレイヤーが追加されます。

## ストロークの色を変更する一般的なユースケース
- **ブランディング自動化:** 数百の PSD アセットに対して企業カラーを一括で適用します。  
- **動的 UI 生成:** Web ベースのデザインツールでユーザー選択テーマに応じてストローク色をリアルタイムに変更します。  
- **プリフライト準備:** 印刷前にすべてのストローク色が印刷仕様を満たすことを確認し、プレスへ送る前に調整します。

## よくある落とし穴とヒント

- **Null チェック** – `getEffects()` が null でない配列を返すことを常に確認してください。  
- **レイヤーインデックス** – PSD のレイヤーは 0 から始まります。正しいレイヤーを対象にしてください。  
- **カラー形式** – `Color.getYellow()` は例示です。`new Color(r, g, b)` でカスタムカラーを作成できます。  
- **不透明度の範囲** – 不透明度はバイト (0–255) です。255 を超える値はクランプされます。  
- **リソースの読み込み** – `loadOptions.setLoadEffectsResource(true)` を忘れると `null` のエフェクト配列になります。

## よくある質問

**Q:** Aspose.PSD を他の Java グラフィックライブラリと併用できますか？  
**A:** はい、Aspose.PSD は Apache Commons Imaging や Java2D などのライブラリと組み合わせて、機能を拡張できます。

**Q:** Aspose.PSD は最新の PSD ファイル形式に対応していますか？  
**A:** もちろんです。ライブラリは最新の Photoshop 仕様と 150 以上の PSD 機能をサポートしています。

**Q:** Aspose.PSD 使用時の例外はどう処理すればよいですか？  
**A:** コードを try‑catch ブロックで囲み、詳細なトラブルシューティング例は [support forum](https://forum.aspose.com/c/psd/34) を参照してください。

**Q:** 購入前に Aspose.PSD を試すことはできますか？  
**A:** もちろんです！すべての機能を試せる [free trial](https://releases.aspose.com/) をご利用ください。

**Q:** Aspose.PSD の一時ライセンスはどこで取得できますか？  
**A:** 開発環境でライブラリを評価するための [temporary license](https://purchase.aspose.com/temporary-license/) を取得してください。

**最終更新日:** 2026-10-24  
**テスト環境:** Aspose.PSD 24.11 for Java  
**作者:** Aspose

## 関連チュートリアル

- [Java でストロークの色を変更する方法 Aspose.PSD を使用して](/psd/java/advanced-image-effects/add-stroke-layer-color/)
- [Java で PSD に影を追加する方法 – 高度なレイヤーエフェクト](/psd/java/advanced-psd-layer-features-effects/)
- [Pattern Overlay PSD: Aspose.PSD for Java でエフェクトを追加](/psd/java/advanced-image-effects/add-pattern-effects/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}