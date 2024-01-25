---
title: Java 用 Aspose.PSD にパターン効果を追加する
linktitle: パターン効果を追加する
second_title: Aspose.PSD Java API
description: Aspose.PSD for Java を使用して、Java イメージ パターンを簡単に強化します。ステップバイステップのチュートリアルに従って、魅力的なパターン効果を追加します。
type: docs
weight: 12
url: /ja/java/advanced-image-effects/add-pattern-effects/
---
## 導入

Java 開発の世界では、イメージ パターンの強化は一般的なタスクであり、Aspose.PSD for Java はこれに対する堅牢なソリューションを提供します。このチュートリアルでは、Aspose.PSD を使用してパターン効果を追加するプロセスを説明し、独自のオーバーレイと拡張機能で画像を目立たせることができます。

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。

- Java Development Kit (JDK) がシステムにインストールされています。
-  Java ライブラリ用の Aspose.PSD がダウンロードされ、プロジェクトに追加されました。からダウンロードできます。[Aspose.PSD Web サイト](https://releases.aspose.com/psd/java/).

## パッケージのインポート

Java プロジェクトで、Aspose.PSD を操作するために必要なパッケージをインポートします。 Java クラスの先頭に次のコードを含めます。

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.PatternOverlayEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;

import java.util.UUID;
```

## ステップ 1: 画像をロードする

```java
//PSD画像をロードする
String sourceFileName = "YourImagePath/PatternOverlay.psd";
String exportPath = "YourExportPath/PatternOverlayChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

「YourImagePath」と「YourExportPath」をプロジェクト内の実際のパスに置き換えてください。

## ステップ 2: パターン オーバーレイ情報を抽出する

```java
//パターンオーバーレイに関する情報を抽出する
PatternOverlayEffect patternOverlay = (PatternOverlayEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## ステップ 3: パターン オーバーレイ設定を変更する

```java
//パターンオーバーレイ設定を変更する
PatternFillSettings settings = patternOverlay.getSettings();
settings.setColor(Color.getGreen());
patternOverlay.setOpacity((byte)193);
patternOverlay.setBlendMode(BlendMode.Difference);
settings.setHorizontalOffset(15);
settings.setVerticalOffset(11);
```

## ステップ4: パターンデータを編集する

```java
//パターンデータを編集する
PattResource resource;
UUID guid = UUID.randomUUID();
String newPatternName = "$$/Presets/Patterns/Pattern=Some new pattern name\0";

for (int i = 0; i < im.getGlobalLayerResources().length; i++) {
    if (im.getGlobalLayerResources()[i] instanceof PattResource) {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName(newPatternName);
        resource.setPattern(new int[]{Color.getAqua().toArgb(), Color.getRed().toArgb(),
                        Color.getRed().toArgb(), Color.getAqua().toArgb(),
                        Color.getAqua().toArgb(), Color.getWhite().toArgb(),
                        Color.getWhite().toArgb(), Color.getAqua().toArgb()}, new Rectangle(0, 0, 4, 2));
    }
}
```

## ステップ 5: 編集した画像を保存する

```java
//編集した画像を保存する
settings.setPatternName(newPatternName);
settings.setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

## ステップ 6: 変更を確認する

```java
//編集したファイルの変更を確認する
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
PatternOverlayEffect patternOverlayEffect = (PatternOverlayEffect)img.getLayers()[1].getBlendingOptions().getEffects()[0];

//アサーションを追加して、変更が正常に適用されたことを確認します
```

## 結論

おめでとう！ Aspose.PSD for Java を使用してパターン効果を追加する方法を学習しました。この強力なライブラリを使用すると、カスタマイズされたパターンで視覚的に魅力的な画像を作成でき、Java ベースのプロジェクトに無限の可能性をもたらします。

## よくある質問

### Q1: Aspose.PSD for Java を他の Java 画像処理ライブラリと一緒に使用できますか?

A1: Aspose.PSD for Java は独立して動作するように設計されていますが、必要に応じて他の Java ライブラリと統合できます。

### Q2: Aspose.PSD for Java の詳細なドキュメントはどこで見つけられますか?

 A2: を参照してください。[Java 用 Aspose.PSD ドキュメント](https://reference.aspose.com/psd/java/)包括的な情報については。

### Q3: Aspose.PSD for Java の無料トライアルはありますか?

 A3: はい、無料トライアルにアクセスできます。[ここ](https://releases.aspose.com/).

### Q4: Java 用 Aspose.PSD のサポートを受けるにはどうすればよいですか?

 A4: にアクセスしてください。[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34)コミュニティ サポートが必要な場合は、サポート プランの購入を検討してください。

### Q5: Aspose.PSD for Java の一時ライセンスを取得できますか?

A5: はい、仮免許を取得できます。[ここ](https://purchase.aspose.com/temporary-license/).