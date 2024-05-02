---
title: Java 用 Aspose.PSD にストローク レイヤー カラーを追加する
linktitle: ストロークレイヤーカラーの追加
second_title: Aspose.PSD Java API
description: ストローク レイヤー カラーの追加に関するステップバイステップ ガイドを使用して、Aspose.PSD for Java の威力を体験してください。グラフィック デザインを簡単に向上させます。
type: docs
weight: 14
url: /ja/java/advanced-image-effects/add-stroke-layer-color/
---
## 導入

Aspose.PSD を使用して、Java アプリケーションのグラフィック デザインの可能性を解き放ちます。このチュートリアルでは、Aspose.PSD for Java を使用してストローク レイヤー カラーを追加する魅力的な世界を詳しく掘り下げていきます。ポップなストロークでグラフィックを強化し、視覚的に魅力的なデザインを簡単に作成します。

## 前提条件

このクリエイティブな旅に着手する前に、次の前提条件が満たされていることを確認してください。

-  Aspose.PSD ライブラリ: 次の手順に従って、Aspose.PSD ライブラリをダウンロードしてセットアップします。[ドキュメンテーション](https://reference.aspose.com/psd/java/).

- Java 開発キット (JDK): システムに Java がインストールされていることを確認してください。

- 統合開発環境 (IDE): 好みの IDE を選択します。 Eclipse または IntelliJ が一般的な選択肢です。

## パッケージのインポート

まずは、Aspose.PSD の魔法を実現するために必要なパッケージをインポートすることから始めましょう。

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

## ステップ 1: プロジェクトをセットアップする

まず、好みの IDE で新しい Java プロジェクトを作成します。 Aspose.PSD ライブラリがプロジェクトに追加されていることを確認します。

## ステップ 2: PSD ファイルをロードする

Aspose.PSD を使用して PSD ファイルをロードし、エフェクト リソースのロードを有効にします。

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## ステップ 3: ストローク レイヤーにアクセスする

PSD ファイル内のストローク エフェクト レイヤーにアクセスします。

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## ステップ 4: ストロークのプロパティを検証する

ストロークのプロパティが期待どおりであることを確認します。

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

## ステップ 5: 色と不透明度を設定する

ストロークレイヤーの色と不透明度を変更します。

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

## ステップ 6: 変更した PSD を保存する

変更した PSD ファイルを、新しく追加したストローク レイヤー カラーで保存します。

```java
im.save(exportPath);
```

## 結論

おめでとう！ Aspose.PSD for Java を使用して PSD ファイルにストローク レイヤー カラーを正常に追加しました。さまざまな色や設定を試して、グラフィック デザインに命を吹き込みます。

## よくある質問

### Q1: Aspose.PSD を他の Java グラフィック ライブラリと一緒に使用できますか?

A1: はい、Aspose.PSD は他の Java グラフィック ライブラリと統合して機能を強化できます。

### Q2: Aspose.PSD は最新の PSD ファイル形式と互換性がありますか?

A2: もちろんです！ Aspose.PSD は最新の PSD ファイル形式仕様に準拠し、互換性を確保します。

### Q3: Aspose.PSD の使用中に例外を処理するにはどうすればよいですか?

 A3: を参照してください。[サポートフォーラム](https://forum.aspose.com/c/psd/34)例外の処理とトラブルシューティングを支援します。

### Q4: 購入する前に Aspose.PSD を試してみることはできますか?

 A4：確かに！掴む[無料トライアル](https://releases.aspose.com/)コミットする前に、Aspose.PSD の機能を調べてください。

### Q5: Aspose.PSD の一時ライセンスはどこで入手できますか?

 A5: を入手してください。[仮免許](https://purchase.aspose.com/temporary-license/)Aspose.PSD のプロジェクトでの機能を評価します。