---
title: PSD でカラー塗りつぶしによるストローク効果を適用する - Java
linktitle: PSD でカラー塗りつぶしによるストローク効果を適用する - Java
second_title: Aspose.PSD Java API
description: Aspose.PSD for Java を使用して、PSD ファイルにカラー フィル付きのストローク効果を適用する方法を学びます。このステップ バイ ステップ ガイドに従って、画像を簡単に強化します。
type: docs
weight: 21
url: /ja/java/psd-layer-management-effects/apply-stroke-effect-color-fill-psd/
---
## 導入

このガイドでは、Aspose.PSD for Java を使用して、PSD ファイルにカラー フィル付きのストローク効果を適用する手順を説明します。熟練した開発者でも、初心者でも、このステップ バイ ステップのチュートリアルにより、作業を簡単に完了できます。環境の設定から、効果を適用した最終イメージの保存まで、すべてをカバーします。

## 前提条件

始める前に、このチュートリアルに従うために必要なものがすべて揃っていることを確認しましょう。

1. Java 開発キット (JDK) がインストールされている: システムに JDK 8 以降がインストールされていることを確認してください。
2.  Aspose.PSD for Javaライブラリ: Aspose.PSD for Javaライブラリが必要です。[Webサイト](https://releases.aspose.com/psd/java/).
3. 統合開発環境 (IDE): IntelliJ IDEA、Eclipse、またはその他の任意の IDE。
4. サンプル PSD ファイル: ストローク効果を適用できるサンプル PSD ファイル。サンプル PSD ファイルがない場合、Photoshop で簡単な PSD ファイルを作成するか、インターネットからダウンロードできます。
5. Java の基礎知識: このチュートリアルは初心者向けですが、Java の基本的な知識があると役立ちます。

これらの前提条件が満たされると、PSD ファイルにカラー塗りつぶしによるストローク効果を適用する準備が整います。

## パッケージのインポート

Aspose.PSD for Java の使用を開始するには、必要なパッケージを Java プロジェクトにインポートする必要があります。手順は次のとおりです。

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

これらのインポートにより、PSD ファイルの操作、効果の適用、および希望する形式での画像の保存に必要なすべてのクラスが取り込まれます。

## ステップ1: PSDファイルを読み込む

プロセスの最初のステップは、変更したいPSDファイルを読み込むことです。Aspose.PSD for Javaでは、この操作を非常に簡単に行うことができます。`PsdImage`クラス。やり方は次のとおりです。

### 1.1 ディレクトリパスを設定する

まず、PSD ファイルが保存されるディレクトリ パスを定義します。

```java
String dataDir = "Your Document Directory";
```

交換する`"Your Document Directory"`PSD ファイルが配置されている実際のパスを入力します。

### 1.2 PSDイメージを読み込む

次に、PSDファイルを読み込みます。`PsdLoadOptions`そして`PsdImage`クラス:

```java
String sourceFileName = dataDir + "StrokeComplex.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

ここでは、`PsdLoadOptions`エフェクト リソースをロードするように構成されており、PSD 内の既存のエフェクトにアクセスできるようになります。

## ステップ2: 塗りつぶしでストローク効果を適用する

PSD ファイルが読み込まれたら、次のステップは、画像のレイヤーにストローク効果を適用することです。ここで、本当の魔法が起こります。

各 PSD ファイルには複数のレイヤーが含まれている場合があり、各レイヤーにエフェクトを適用する必要があります。手順は次のとおりです。

```java
for (int i = 0; i < im.getLayers().length; i++) {
    StrokeEffect effect = (StrokeEffect) im.getLayers()[i].getBlendingOptions().getEffects()[0];
    ColorFillSettings settings = (ColorFillSettings) effect.getFillSettings();
    settings.setColor(Color.getDeepPink());
}
```

このループでは:

- `im.getLayers()`: PSD ファイル内のすべてのレイヤーを取得します。
- `StrokeEffect effect`: レイヤーに適用されたストローク効果を抽出します。
- `ColorFillSettings settings`: ストローク効果の塗りつぶし設定を変更します。
- `settings.setColor(Color.getDeepPink())`: 線の色を濃いピンクに設定します。お好みの色に変更できます。

## ステップ3: 変更したPSDを保存し、PNGとしてエクスポートする

ストローク効果を適用したら、変更を保存して画像をエクスポートします。

### 3.1 PSDファイルを保存する

変更した PSD ファイルを保存するには、次のコードを使用します。

```java
String exportPath = dataDir + "StrokeComplexRendering.psd";
im.save(exportPath, new PsdOptions());
```

これにより、ストローク効果を適用したファイルが指定されたパスに保存されます。

### 3.2 PNGとしてエクスポート

画像をもっとアクセスしやすくするには、PNG ファイルとしてエクスポートすることをお勧めします。手順は次のとおりです。

```java
String exportPathPng = dataDir + "StrokeComplexRendering.png";
PngOptions option = new PngOptions();
option.setColorType(PngColorType.TruecolorWithAlpha);

im.save(exportPathPng, option);
```

このコード スニペットは、画像をトゥルー カラーとアルファ透明度を持つ PNG として保存し、Web アプリケーションや他のプラットフォームで使用できるようにします。

## 結論

Aspose.PSD for Java を使用して PSD ファイルにカラー フィル付きのストローク効果を適用することは、簡単なだけでなく、非常に強力です。わずか数行のコードで、複雑な画像処理タスクを自動化し、時間と労力を節約できます。

大量の画像を扱う場合でも、いくつかのファイルを微調整するだけの場合でも、この方法は柔軟で効率的なソリューションを提供します。これで基本が理解できたので、さまざまな効果やカスタマイズを試して、画像を本当に際立たせることができます。

試してみる準備はできましたか? サンプル PSD ファイルを入手して、今すぐ魅力的なエフェクトを追加してみましょう。

## よくある質問

### Aspose.PSD for Java を使用して、単一のレイヤーに複数の効果を適用できますか?
はい、レイヤーのブレンド オプションにアクセスし、必要なエフェクトを追加することで、1 つのレイヤーに複数のエフェクトを適用できます。

### PSD ファイルのバッチ処理を自動化することは可能ですか?
もちろんです! PSD ファイルのディレクトリをループし、ストローク効果を適用して、結果を自動的に保存できます。

### Aspose.PSD for Java を使用して PSD ファイルに加えた変更を元に戻すにはどうすればよいですか?
変更を元に戻すには、変更を保存する前に元の PSD ファイルを再読み込みする必要があります。Aspose.PSD には直接元に戻す機能はありません。

### ストロークの幅と位置をカスタマイズできますか?
はい、Aspose.PSD for Javaでは、ストロークの幅、位置、その他のプロパティをカスタマイズできます。`StrokeEffect`クラス。

### Aspose.PSD for Java ライブラリは無料で使用できますか?
 Aspose.PSD for Javaは無料トライアルを提供していますが、すべての機能にアクセスするにはライセンスを購入する必要があります。[購入オプション](https://purchase.aspose.com/buy)彼らのウェブサイトで。