---
title: Java でストローク レイヤー パターンを追加する方法
linktitle: Java でストローク レイヤー パターンを追加する方法
second_title: Aspose.PSD Java API
description: Aspose.PSD for Java を使用して PSD ファイルにストローク レイヤー パターンを追加する方法を学びます。このステップ バイ ステップ ガイドに従って、画像を簡単に強化します。
type: docs
weight: 11
url: /ja/java/java-graphics-drawing/add-stroke-layer-pattern/
---
## 導入
Java で画像にストローク レイヤー パターンを追加するのは大変な作業のように思えるかもしれませんが、Aspose.PSD for Java を使用すると、思ったより簡単になります。グラフィックスをデザインする場合でも、写真編集アプリケーションで作業する場合でも、このガイドではプロセスをステップごとに説明します。準備はできましたか? さあ、始めましょう!
## 前提条件
始める前に、いくつか必要なものがあります:
- Java 開発キット (JDK): システムに JDK がインストールされていることを確認してください。
-  Aspose.PSD for Java: ライブラリをダウンロードするには、[ここ](https://releases.aspose.com/psd/java/)それをプロジェクトに含めます。
- IDE: IntelliJ IDEA や Eclipse などのお気に入りの統合開発環境 (IDE) を使用します。
## パッケージのインポート
まず最初に、必要なパッケージを Java プロジェクトにインポートする必要があります。これらのパッケージは、Aspose.PSD を操作するために不可欠です。
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
## ステップ1: PSDファイルを読み込む
ストローク レイヤー パターンを追加する最初の手順は、編集する PSD ファイルを読み込むことです。
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
PSD ファイルを読み込むと、レイヤーやエフェクトにアクセスして操作できるようになります。
## ステップ2: 新しいパターンデータを準備する
次に、ストローク レイヤーに適用する新しいパターン データを準備する必要があります。
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
このパターン データは、新しいストローク効果を作成するために使用されます。
## ステップ3: ストローク効果にアクセスする
ストローク効果を変更するには、特定のレイヤーとそのブレンド オプションにアクセスする必要があります。
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
これにより、正しいレイヤーとエフェクトで作業していることが保証されます。
## ステップ4: ストローク効果を変更する
次に、新しいパターン データを使用してストローク効果を変更してみましょう。
### ストローク効果のプロパティを更新
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
### パターンリソースを更新する
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
このコード スニペットは、パターン リソースを新しいパターン データで更新します。
## ステップ5: 新しいパターンを適用する
最後に、新しいパターンをストローク効果に適用し、変更を保存します。
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
これにより、新しいパターンが正しく適用され、変更が反映されたファイルが保存されます。
## ステップ6: 変更を確認する
すべてが正しく機能したことを確認するには、ファイルを再度ロードして変更を確認します。
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
この手順では、パターン データがストローク効果に正しく適用されていることを確認します。
## 結論
これで完了です。Aspose.PSD for Java を使用して、PSD ファイルにストローク レイヤー パターンを正常に追加できました。次の手順に従うことで、画像を簡単にカスタマイズおよび強化できます。コーディングを楽しんでください。
## よくある質問
### Aspose.PSD for Java とは何ですか?
Aspose.PSD for Java は、開発者が PSD (Photoshop ドキュメント) ファイルをプログラムで作成、編集、変換できるようにするライブラリです。
### Aspose.PSD for Java を商用プロジェクトで使用できますか?
はい、商用プロジェクトでも使用できます。ライセンスは以下から購入できます。[ここ](https://purchase.aspose.com/buy).
### Aspose.PSD for Java の無料試用版はありますか?
はい、無料試用版は以下からダウンロードできます。[ここ](https://releases.aspose.com/).
### Aspose.PSD for Java のサポートを受けるにはどうすればよいですか?
 Asposeコミュニティフォーラムからサポートを受けることができます[ここ](https://forum.aspose.com/c/psd/34).
### Aspose.PSD for Java のシステム要件は何ですか?
開発には JDK と IDE のインストールが必要です。ライブラリは、Windows、Linux、macOS を含む複数のオペレーティング システムをサポートしています。