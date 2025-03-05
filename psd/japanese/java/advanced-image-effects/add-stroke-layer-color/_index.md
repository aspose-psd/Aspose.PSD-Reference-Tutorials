---
title: Aspose.PSD for Java でストローク レイヤーの色を追加する
linktitle: ストロークレイヤーカラーを追加
second_title: Aspose.PSD Java API
description: ストローク レイヤー カラーの追加に関するステップ バイ ステップ ガイドを使用して、Aspose.PSD for Java のパワーを体験してください。グラフィック デザインを簡単に向上できます。
type: docs
weight: 14
url: /ja/java/advanced-image-effects/add-stroke-layer-color/
---
## 導入

Aspose.PSD を使用すると、Java アプリケーションのグラフィック デザインの可能性を最大限に引き出すことができます。このチュートリアルでは、Aspose.PSD for Java を使用してストローク レイヤーの色を追加する魅力的な世界を詳しく見ていきます。目立つストロークでグラフィックを強化し、視覚的に魅力的なデザインを簡単に作成します。

## 前提条件

この創造的な旅に乗り出す前に、次の前提条件が満たされていることを確認してください。

-  Aspose.PSDライブラリ: Aspose.PSDライブラリをダウンロードしてセットアップするには、[ドキュメント](https://reference.aspose.com/psd/java/).

- Java 開発キット (JDK): システムに Java がインストールされていることを確認してください。

- 統合開発環境 (IDE): 好みの IDE を選択します。Eclipse または IntelliJ が一般的な選択肢です。

## パッケージのインポート

まず、Aspose.PSD マジックを実現するために必要なパッケージをインポートすることから始めましょう。

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

## ステップ1: プロジェクトを設定する

まず、お好みの IDE で新しい Java プロジェクトを作成します。Aspose.PSD ライブラリがプロジェクトに追加されていることを確認します。

## ステップ2: PSDファイルを読み込む

Aspose.PSD を使用して PSD ファイルを読み込み、エフェクト リソースの読み込みを有効にします。

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## ステップ3: ストロークレイヤーにアクセスする

PSD ファイル内のストローク効果レイヤーにアクセスします。

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## ステップ4: ストロークのプロパティを検証する

ストロークのプロパティが期待どおりであることを確認します。

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

## ステップ5: 色と不透明度を設定する

ストローク レイヤーの色と不透明度を変更します。

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

## ステップ6: 変更したPSDを保存する

新しく追加されたストローク レイヤーの色を使用して、変更された PSD ファイルを保存します。

```java
im.save(exportPath);
```

## 結論

おめでとうございます! Aspose.PSD for Java を使用して、PSD ファイルにストローク レイヤーの色を正常に追加しました。さまざまな色と設定を試して、グラフィック デザインを生き生きとさせましょう。

## よくある質問

### Q1: Aspose.PSD を他の Java グラフィック ライブラリと一緒に使用できますか?

A1: はい、Aspose.PSD は他の Java グラフィック ライブラリと統合して機能を強化できます。

### Q2: Aspose.PSD は最新の PSD ファイル形式と互換性がありますか?

A2: もちろんです! Aspose.PSD は最新の PSD ファイル形式仕様に準拠しており、互換性が保証されています。

### Q3: Aspose.PSD の使用中に例外を処理するにはどうすればよいですか?

 A3: を参照してください[サポートフォーラム](https://forum.aspose.com/c/psd/34)例外処理とトラブルシューティングのサポート。

### Q4: 購入前に Aspose.PSD を試すことはできますか?

 A4: もちろんです！[無料トライアル](https://releases.aspose.com/)購入する前に Aspose.PSD の機能を調べてください。

### Q5: Aspose.PSD の一時ライセンスはどこで入手できますか?

 A5: 取得する[一時ライセンス](https://purchase.aspose.com/temporary-license/)Aspose.PSD を使用して、プロジェクトでその機能を評価します。