---
date: 2026-01-14
description: このステップバイステップのチュートリアルで、Aspose.PSD for Java を使用して PSD ファイルにグラデーションストロークレイヤーを作成し、ストロークのグラデーションをカスタマイズする方法を学びましょう。
linktitle: How to Create Gradient Stroke Layer in Java
second_title: Aspose.PSD Java API
title: Javaでグラデーションストロークレイヤーを作成する方法
url: /ja/java/java-graphics-drawing/add-stroke-layer-gradient/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Javaでグラデーションストロークレイヤーを作成する方法

## はじめに
Javaを使ってPSDファイルに**グラデーションストロークレイヤー**を作成する方法を考えたことはありますか？ここが正解です！本日は Aspose.PSD for Java に深く入り込み、PSDファイルを簡単に操作できる強力なライブラリをご紹介します。グラフィックプログラミングが初めての方でも、既存のデザインを微調整したい方でも、このガイドではストロークグラデーションの追加とカスタマイズをステップバイステップで説明します。

## クイック回答
- **主な目的は何ですか？** PSDファイルにグラデーションストロークレイヤーを作成することです。  
- **どのライブラリが必要ですか？** Aspose.PSD for Java。  
- **ライセンスは必要ですか？** はい、製品環境では有効な（または一時的な）ライセンスが必要です。  
- **どのJavaバージョンが動作しますか？** Java 8 以上。  
- **実装にどれくらい時間がかかりますか？** 基本的なグラデーションストロークでおおよそ10‑15 分です。

## グラデーションストロークレイヤーとは？
グラデーションストロークレイヤーは、形状やテキストの周囲に描かれるベクター輪郭で、色が滑らかに変化します。Aspose.PSD を使用すると、ストロークの色、透明度、角度、タイプ（線形、放射状など）をプログラムで定義できます。

## なぜ Aspose.PSD for Java を使用するのか？
- **フル PSD サポート** – Photoshop を使用せずに PSD ファイルの読み取り、編集、書き込みが可能。  
- **豊富なエフェクト API** – ストローク、シャドウ、グローなど多数のレイヤーエフェクトにアクセス。  
- **クロスプラットフォーム** – Java が動作するすべての OS で利用可能。  
- **ネイティブ依存なし** – 純粋な Java 実装で、CI パイプラインへの統合が容易。

## 前提条件
1. **Java Development Kit (JDK)** – 最新の JDK を [Oracle のウェブサイト](https://www.oracle.com/java/technologies/javase-downloads.html) からインストール。  
2. **Aspose.PSD for Java** – ライブラリを [Aspose.PSD ダウンロードページ](https://releases.aspose.com/psd/java/) から取得。  
3. **IDE** – IntelliJ IDEA、Eclipse、または NetBeans。  
4. **License** – 完全版がない場合は、[一時ライセンス](https://purchase.aspose.com/temporary-license/) を取得。

## パッケージのインポート
まず、PSD の読み込み、エフェクトへのアクセス、グラデーションフィルの設定に必要なクラスをインポートします。

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

それでは、プロセスを明確な手順に分解していきましょう。

## ステップ 1: PSD ファイルの読み込み
ソース PSD を読み込み、ストロークエフェクトが利用できるようにエフェクトリソースを有効化します。

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

## ステップ 2: ストロークエフェクトへのアクセス
変更したいストロークが 3 番目のレイヤー（インデックス 2）に属していると仮定し、`StrokeEffect` を取得します。

```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```

## ステップ 3: ストロークエフェクトのプロパティを確認
変更を加える前に、既存の設定を確認して正確に何を更新するか把握します。

```java
Assert.areEqual(BlendMode.Normal, gradientStroke.getBlendMode());
Assert.areEqual(255, gradientStroke.getOpacity());
Assert.areEqual(true, gradientStroke.isVisible());
GradientFillSettings fillSettings = (GradientFillSettings) gradientStroke.getFillSettings();
Assert.areEqual(Color.getBlack(), fillSettings.getColor());
Assert.areEqual(FillType.Gradient, fillSettings.getFillType());
Assert.areEqual(true, fillSettings.getAlignWithLayer());
Assert.areEqual(GradientType.Linear, fillSettings.getGradientType());
Assert.isTrue(Math.abs(90 - fillSettings.getAngle()) < 0.001, "Angle is incorrect");
Assert.areEqual(false, fillSettings.getDither());
Assert.isTrue(Math.abs(0 - fillSettings.getHorizontalOffset()) < 0.001, "Horizontal offset is incorrect");
Assert.isTrue(Math.abs(0 - fillSettings.getVerticalOffset()) < 0.001, "Vertical offset is incorrect");
Assert.areEqual(false, fillSettings.getReverse());
```

## ステップ 4: グラデーションフィル設定の変更
ここでは、目的の外観を実現するために色、透明度、ブレンドモード、その他のプロパティを変更します。

```java
fillSettings.setColor(Color.getGreen());
gradientStroke.setOpacity((byte) 127);
gradientStroke.setBlendMode(BlendMode.Color);
fillSettings.setAlignWithLayer(false);
fillSettings.setGradientType(GradientType.Radial);
fillSettings.setAngle(45);
fillSettings.setDither(true);
fillSettings.setHorizontalOffset(15);
fillSettings.setVerticalOffset(11);
fillSettings.setReverse(true);
```

## ステップ 5: カラーと透明度ポイントの追加と変更
新しいカラーおよび透明度ポイントを追加し、既存のポイントを調整してグラデーションの形状を整えます。

```java
// Add new color point
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Change location of previous point
fillSettings.getColorPoints()[1].setLocation(1899);
// Add new transparency point
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Change location of previous transparency point
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```

## ステップ 6: 変更後の PSD ファイルを保存
すべての調整が完了したら、更新されたファイルをディスクに書き戻します。

```java
im.save(exportPath);
```

## ステップ 7: 変更の検証
保存したファイルを読み込み、すべてのプロパティが適用した変更を反映していることを確認します。

```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// Check color points
Assert.areEqual(3, fillSetting.getColorPoints().length);
IGradientColorPoint point = fillSetting.getColorPoints()[0];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getBlack(), point.getColor());
Assert.areEqual(0, point.getLocation());
point = fillSettings.getColorPoints()[1];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getWhite(), point.getColor());
Assert.areEqual(1899, point.getLocation());
point = fillSettings.getColorPoints()[2];
Assert.areEqual(75, point.getMedianPointLocation());
Assert.areEqual(Color.getGreen(), point.getColor());
Assert.areEqual(4096, point.getLocation());
// Check transparency points
Assert.areEqual(3, fillSettings.getTransparencyPoints().length);
IGradientTransparencyPoint transparencyPoint1 = fillSettings.getTransparencyPoints()[0];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(0, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[1];
Assert.areEqual(50, transparencyPoint.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint.getOpacity());
Assert.areEqual(2411, transparencyPoint.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[2];
Assert.areEqual(25, transparencyPoint.getMedianPointLocation());
Assert.areEqual(25, transparencyPoint.getOpacity());
Assert.areEqual(4096, transparencyPoint.getLocation());
```

## 結論
これで Aspose.PSD for Java を使用して PSD ファイルに**グラデーションストロークレイヤー**効果を作成する方法が分かりました。PSD を読み込み、ストロークエフェクトにアクセスし、グラデーションフィル設定を調整して結果を保存することで、Photoshop を開くことなくプログラム的にプロフェッショナルなグラフィックを生成できます。

## FAQ

### Aspose.PSD for Java とは？
Aspose.PSD for Java は、Java アプリケーションで PSD ファイルを操作できるライブラリで、PSD の作成、編集、変換機能を提供します。

### Aspose.PSD for Java の使用にライセンスは必要ですか？
はい、Aspose.PSD for Java を使用するには有効なライセンスが必要です。評価目的であれば、[一時ライセンス](https://purchase.aspose.com/temporary-license/) を取得できます。

### Aspose.PSD for Java でゼロから PSD ファイルを作成できますか？
もちろんです！Aspose.PSD for Java は、プログラムから PSD ファイルをゼロから作成・操作するための包括的な API を提供しています。

### Aspose.PSD for Java で他のエフェクトを適用できますか？
はい、シャドウ、グローなど、さまざまなエフェクトを Aspose.PSD for Java を使って適用できます。

### Aspose.PSD for Java のドキュメントはどこで見つけられますか？
ドキュメントは [こちら](https://reference.aspose.com/psd/java/) にあります。

---

**最終更新日:** 2026-01-14  
**テスト環境:** Aspose.PSD for Java 24.11  
**作者:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
