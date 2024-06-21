---
title: Javaでストロークレイヤーのグラデーションを追加する方法
linktitle: Javaでストロークレイヤーのグラデーションを追加する方法
second_title: Aspose.PSD Java API
description: この包括的なステップバイステップのチュートリアルでは、Aspose.PSD for Java を使用して PSD ファイルにストローク レイヤー グラデーションを追加およびカスタマイズする方法を学びます。
type: docs
weight: 10
url: /ja/java/java-graphics-drawing/add-stroke-layer-gradient/
---
## 導入
Java を使用して画像にストローク レイヤーのグラデーションを追加する方法を考えたことはありますか?そうですね、あなたは正しい場所にいます！今日は、PSD ファイルを簡単に操作できる強力なライブラリである Aspose.PSD for Java の世界に飛び込みます。初心者でも経験豊富な開発者でも、このステップバイステップのガイドでは、ストローク レイヤーのグラデーションを PSD ファイルに追加するプロセスを順を追って説明します。さあ、シートベルトを締めて、グラフィック編集スキルを向上させる準備をしましょう。
## 前提条件
始める前に、準備しておく必要があることがいくつかあります。以下のものがあることを確認してください。
1.  Java Development Kit (JDK): システムに JDK がインストールされていることを確認してください。からダウンロードできます[オラクルのウェブサイト](https://www.oracle.com/java/technologies/javase-downloads.html).
2. Aspose.PSD for Java ライブラリ: 次の場所からダウンロードできます。[Aspose.PSD ダウンロード ページ](https://releases.aspose.com/psd/java/).
3. 統合開発環境 (IDE): IntelliJ IDEA、Eclipse、NetBeans などのあらゆる IDE が動作します。
4. 有効なライセンス: 取得できます。[仮免許](https://purchase.aspose.com/temporary-license/)フルのものを持っていない場合。
## パッケージのインポート
まずは必要なパッケージをインポートしましょう。これらにより、PSD ファイルの操作に必要なクラスとメソッドを使用できるようになります。
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.examples.Utils.Utils;
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
ここで、理解を深めるために例を複数のステップに分けてみましょう。
## ステップ 1: PSD ファイルをロードする
まず、変更したい PSD ファイルをロードする必要があります。を使用します。`PsdLoadOptions`エフェクト リソースをロードすることを指定します。
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```
## ステップ 2: ストローク エフェクトにアクセスする
次に、関心のあるレイヤーのストローク エフェクトにアクセスする必要があります。ここでは、PSD ファイルの 3 番目のレイヤー (インデックス 2) であると仮定します。
```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```
## ステップ 3: ストローク エフェクトのプロパティを確認する
変更を加える前に、ストローク エフェクトのプロパティを確認して、正しい設定を変更していることを確認してください。
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
## ステップ 4: グラデーション塗りつぶし設定を変更する
次に、要件に従ってグラデーションの塗りつぶし設定を変更します。色、不透明度、ブレンド モード、その他のプロパティを変更します。
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
## ステップ 5: カラーポイントと透明ポイントを追加および変更する
新しい色と透明度のポイントを追加し、既存のポイントを変更して、目的のグラデーション効果を実現しましょう。
```java
//新しいカラーポイントを追加
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
//前のポイントの位置を変更する
fillSettings.getColorPoints()[1].setLocation(1899);
//新しい透明ポイントを追加
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
//前の透明ポイントの位置を変更する
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```
## ステップ 6: 変更した PSD ファイルを保存する
必要な変更をすべて行った後、PSD ファイルを保存する必要があります。
```java
im.save(exportPath);
```
## ステップ 7: 変更を確認する
最後に、保存した PSD ファイルをロードし、変更が正しく適用されたことを確認しましょう。
```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
//カラーポイントをチェック
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
//透明点を確認する
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
そして、それができました！ Aspose.PSD for Java を使用して PSD ファイルにストローク レイヤーのグラデーションを追加および操作する方法がわかりました。このチュートリアルでは、PSD ファイルのロード、ストローク エフェクトへのアクセスと変更、および変更の保存について説明しました。これらのスキルがあれば、視覚的に魅力的なグラデーションを作成し、ニーズに合わせて PSD ファイルをカスタマイズできます。
## よくある質問
### Java 用 Aspose.PSD とは何ですか?
Aspose.PSD for Java は、開発者が Java アプリケーションで PSD ファイルを操作できるようにするライブラリであり、PSD ファイルを作成、操作、変換する機能を提供します。
### Aspose.PSD for Java を使用するにはライセンスが必要ですか?
はい、Aspose.PSD for Java を使用するには有効なライセンスが必要です。を得ることができます[仮免許](https://purchase.aspose.com/temporary-license/)評価目的のため。
### Aspose.PSD for Java を使用して PSD ファイルを最初から作成できますか?
絶対に！ Aspose.PSD for Java は、PSD ファイルをプログラムで作成および操作するための包括的な API を提供します。
### Aspose.PSD for Java を使用して他の効果を適用することはできますか?
はい、Aspose.PSD for Java を使用して、シャドウ、グローなどのさまざまな効果を適用できます。
### Aspose.PSD for Java のドキュメントはどこで見つけられますか?
ドキュメントを見つけることができます[ここ](https://reference.aspose.com/psd/java/).