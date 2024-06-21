---
title: Javaでストロークレイヤーパターンを追加する方法
linktitle: Javaでストロークレイヤーパターンを追加する方法
second_title: Aspose.PSD Java API
description: Aspose.PSD for Java を使用して PSD ファイルにストローク レイヤー パターンを追加する方法を学びます。このステップバイステップのガイドに従って、画像を簡単に強化します。
type: docs
weight: 11
url: /ja/java/java-graphics-drawing/add-stroke-layer-pattern/
---
## 導入
Java でストローク レイヤー パターンを画像に追加するのは困難な作業のように聞こえるかもしれませんが、Aspose.PSD for Java を使用すると、思っているより簡単です。グラフィックをデザインしている場合でも、写真編集アプリケーションに取り組んでいる場合でも、このガイドではプロセスを段階的に説明します。始める準備はできていますか?飛び込んでみましょう！
## 前提条件
始める前に、いくつかのものが必要です。
- Java Development Kit (JDK): システムに JDK がインストールされていることを確認してください。
-  Java 用 Aspose.PSD: からライブラリをダウンロードします。[ここ](https://releases.aspose.com/psd/java/)そしてそれをプロジェクトに含めます。
- IDE: IntelliJ IDEA や Eclipse など、お気に入りの統合開発環境 (IDE) を使用します。
## パッケージのインポート
まず最初に、必要なパッケージを Java プロジェクトにインポートする必要があります。これらのパッケージは、Aspose.PSD を操作するために不可欠です。
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```
## ステップ 1: PSD ファイルをロードする
ストローク レイヤー パターンを追加する最初のステップは、編集する PSD ファイルをロードすることです。
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
PSD ファイルをロードすると、そのレイヤーとエフェクトにアクセスして操作できるようになります。
## ステップ2: 新しいパターンデータを準備する
次に、ストロークレイヤーに適用する新しいパターンデータを準備する必要があります。
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
このパターン データを使用して、新しいストローク エフェクトを作成します。
## ステップ 3: ストローク エフェクトにアクセスする
ストローク効果を変更するには、特定のレイヤーとそのブレンド オプションにアクセスする必要があります。
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
これにより、正しいレイヤーとエフェクトを使用して作業できるようになります。
## ステップ 4: ストローク効果を変更する
それでは、新しいパターンデータを使用してストローク効果を変更してみましょう。
### ストローク効果プロパティの更新
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
このコード スニペットは、新しいパターン データでパターン リソースを更新します。
## ステップ 5: 新しいパターンを適用する
最後に、新しいパターンをストローク エフェクトに適用し、変更を保存します。
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
これにより、新しいパターンが正しく適用され、ファイルが変更とともに保存されます。
## ステップ 6: 変更を確認する
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
このステップでは、パターン データがストローク エフェクトに正しく適用されていることを確認します。
## 結論
そして、それができました！ Aspose.PSD for Java を使用して、ストローク レイヤー パターンを PSD ファイルに正常に追加しました。以下の手順に従うことで、画像を簡単にカスタマイズおよび強化できます。コーディングを楽しんでください!
## よくある質問
### Java 用 Aspose.PSD とは何ですか?
Aspose.PSD for Java は、開発者が PSD (Photoshop Document) ファイルをプログラムで作成、編集、変換できるようにするライブラリです。
### Aspose.PSD for Java を商用プロジェクトで使用できますか?
はい、商用プロジェクトで使用できます。ライセンスは以下から購入できます[ここ](https://purchase.aspose.com/buy).
### Aspose.PSD for Java に利用できる無料トライアルはありますか?
はい、無料試用版を次からダウンロードできます。[ここ](https://releases.aspose.com/).
### Java 用 Aspose.PSD のサポートを取得するにはどうすればよいですか?
 Aspose コミュニティ フォーラムからサポートを受けることができます[ここ](https://forum.aspose.com/c/psd/34).
### Aspose.PSD for Java のシステム要件は何ですか?
開発には JDK がインストールされており、IDE が必要です。このライブラリは、Windows、Linux、macOS などの複数のオペレーティング システムをサポートしています。