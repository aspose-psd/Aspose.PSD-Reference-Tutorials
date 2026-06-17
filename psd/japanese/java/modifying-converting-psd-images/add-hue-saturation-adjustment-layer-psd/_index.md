---
date: 2026-03-13
description: Aspose.PSD for Java を使用して PSD ファイルに色相・彩度レイヤーを追加する方法を学びます。このガイドでは、PSD
  ファイルをバッチ処理し、プログラムで色相調整レイヤーを作成する方法も示しています。
linktitle: Add Hue Saturation Layer to PSD
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java を使用して PSD に色相・彩度レイヤーを追加する
url: /ja/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD に色相・彩度レイヤーを追加する

## はじめに
グラフィックデザインにおいて、カラー操作は極めて重要な役割を果たします。特に、色相、彩度、明度を微調整することで、画像の雰囲気や品質を劇的に変えることができます。この目的を達成する効果的な方法の一つが、Photoshop（PSD ファイル）での調整レイヤーの使用です。Java で **add hue saturation layer** をプログラム的に追加したい場合は、Aspose.PSD ライブラリが役立ちます！本チュートリアルでは、PSD ファイルに Hue Saturation Adjustment Layer を追加する手順を解説し、ワークフローをより生産的かつ効率的にします。

## クイック回答
- **Javaで色相・彩度レイヤーを追加できるライブラリは何ですか？** Aspose.PSD for Java。  
- **Photoshop をインストールする必要がありますか？** いいえ、ライブラリは Photoshop とは独立して動作します。  
- **この方法で PSD ファイルをバッチ処理できますか？** はい—手順を自動化すれば多数のファイルに適用できます。  
- **必要な Java バージョンはどれですか？** JDK 8 以降。  
- **本番利用にライセンスは必要ですか？** はい、トライアル期間終了後は商用ライセンスが必要です。

## “add hue saturation layer” 操作とは？
**add hue saturation layer** 操作は、元のピクセルデータを変更せずに色相、彩度、明度の値を調整できる非破壊的な調整レイヤーを作成します。全体の構成や特定のカラー範囲の微調整に最適です。

## なぜ Aspose.PSD for Java を使用するのか？
- **Photoshop 依存なし** – Java が動作する任意のプラットフォームで使用可能。  
- **完全な PSD 再現性** – すべてのレイヤー情報、マスク、エフェクトを保持。  
- **バッチ対応** – フォルダーをループして多数のファイルに同じ調整を適用可能。  
- **パフォーマンス重視** – 大規模ドキュメントやサーバーサイド自動化に最適化。

## 前提条件
コードに入る前に、以下が揃っていることを確認してください。

1. **Java Development Kit (JDK)：** マシンに JDK 8 以上がインストールされていることを確認してください。ダウンロードは [Java SE Development Kit Downloads](https://www.oracle.com/java/technologies/javase-downloads.html) から行えます。  
2. **Aspose.PSD for Java ライブラリ：** Aspose.PSD ライブラリが必要です。こちらから [download here](https://releases.aspose.com/psd/java/)。  
3. **IDE：** IntelliJ IDEA や Eclipse など、Java 開発に適した統合開発環境。  
4. **基本的な Java 知識：** Java プログラミングの基礎があると便利ですが、心配いりません—各行を丁寧に解説します。

前提条件が整ったので、さあ楽しいコーディングパートへ進みましょう！

## Import Packages
Aspose.PSD ライブラリを使用し始めるには、まず必要なクラスをインポートします。Java ファイルでの記述例は次のとおりです。

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```

プロジェクトに適切なライブラリが追加されていることを確認し、インポートがシームレスに機能するようにしてください。

## Step 1: Set Up Your Document Directory
すべてのプロジェクトには開始地点が必要です。今回も例外ではありません。PSD ファイルが保存されているディレクトリを指定する必要があります。これは画像の読み込みと保存を正しく行うために重要です。

```java
String dataDir = "Your Document Directory"; // Update this path to your actual directory
```

## Step 2: Load an Existing PSD File
既存の PSD ファイルを操作するには、まずプログラムに読み込む必要があります。以下のように実装できます。

```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

このコードでは、`"HueSaturationAdjustmentLayer.psd"` を編集したい既存の PSD ファイル名に置き換えてください。

## Step 3: Edit the Hue/Saturation Layer
次に、読み込んだ PSD 画像のレイヤーをループし、既存の Hue/Saturation レイヤーを検索して編集します。このステップでは色相、彩度、明度の値を変更します。

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof HueSaturationLayer) {
        HueSaturationLayer hueLayer = (HueSaturationLayer) im.getLayers()[i];
        hueLayer.setHue((short) -25);
        hueLayer.setSaturation((short) -12);
        hueLayer.setLightness((short) 67);
        ColorRangeHsl colorRange = hueLayer.getRange(2);
        colorRange.setHue((short) -40);
        colorRange.setSaturation((short) 50);
        colorRange.setLightness((short) -20);
        colorRange.setMostLeftBorder((short) 300);
    }
}
```

この例では：  
- 色相を **-25**、彩度を **-12**、明度を **+67** に調整しています。  
- `getRange(2)` メソッドを使用すると、目的のカラー範囲を個別に調整できます。

## Step 4: Save the Modified PSD File
調整が完了したら、次のステップはファイルを保存することです。これは変更が失われないようにする重要なプロセスです。

```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```

## Step 5: Add a New Hue/Saturation Layer
**create hue adjustment layer** をゼロから作成したい場合は、別の PSD ファイルに新しい Hue/Saturation 調整レイヤーを追加できます。同じ読み込みパターンを使用し、`addHueSaturationAdjustmentLayer()` メソッドを呼び出します。

```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```

## Step 6: Set New Hue/Saturation Values for the New Layer
新しいレイヤーを作成したら、先ほどと同様に希望する色相、彩度、明度の設定を適用します。

```java
hueLayerNew.setHue((short) -25);
hueLayerNew.setSaturation((short) -12);
hueLayerNew.setLightness((short) 67);
ColorRangeHsl newColorRange = hueLayerNew.getRange(2);
newColorRange.setHue((short) -160);
newColorRange.setSaturation((short) 100);
newColorRange.setLightness((short) 20);
newColorRange.setMostLeftBorder((short) 300);
```

## Step 7: Save the Updated PSD File
最後に、追加した Hue/Saturation レイヤーを含む PSD ファイルを保存し、変更を確認できるようにします。

```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```

おめでとうございます！Aspose.PSD for Java を使用して PSD ファイルを正常に操作できました。これでさまざまな画像や高度な変更を試し、グラフィックデザインプロジェクトに命を吹き込むことができます。

## How to batch process PSD files with hue adjustments
上記コードは完全にスクリプト化できるため、フォルダー内のすべての `.psd` ファイルをループで処理するように全シーケンスをラップできます。これにより **batch process psd files** が可能となり、同じ色相、彩度、明度の調整を一度の実行で多数のファイルに適用できるため、大規模なブランディング更新に最適です。

## Common Issues and Solutions
- **NullPointerException when loading a file:** `dataDir` が適切なファイルセパレーター（`/` または `\`）で終わっているか、ファイル名が正しいかを確認してください。  
- **Adjustment values out of range:** 色相、彩度、明度は -255 から 255 の範囲で受け付けます。この範囲内に数値を収めてください。  
- **Layer not found:** PSD に Hue/Saturation レイヤーが存在しない場合、`instanceof` チェックでブロックがスキップされます。まず `addHueSaturationAdjustmentLayer()` でレイヤーを作成してください。

## よくある質問

**Q: Hue Saturation Adjustment Layer とは何ですか？**  
A: 画像のピクセルを永久に変更せずに、カラー属性を変更できる調整レイヤーです。

**Q: Aspose.PSD を使用するのに Photoshop をインストールする必要がありますか？**  
A: いいえ、Aspose.PSD は Photoshop とは独立したスタンドアロンライブラリです。

**Q: Aspose.PSD でバッチ処理は可能ですか？**  
A: はい、Aspose.PSD を使って複数の PSD ファイルを自動化・バッチ処理できます。

**Q: Aspose.PSD は無料ですか？**  
A: 無料トライアルは提供されていますが、長期利用にはライセンスが必要です。価格は [here](https://purchase.aspose.com/buy) で確認できます。

## 結論
プログラムでグラフィックを操作することで、可能性が広がります。Aspose.PSD for Java を使って **add hue saturation layer** や **create hue adjustment layer** を実現すれば、デザインワークフローの柔軟性と効率が大幅に向上します。プロジェクトの写真を強化したり、魅力的なビジュアルコンテンツを作成したりする際に、これらのツールをマスターすれば成果物が格段に向上します。

Aspose.PSD のさらなる機能は [documentation](https://reference.aspose.com/psd/java/) を参照するか、[temporary license](https://purchase.aspose.com/temporary-license/) を取得してライブラリのフルパワーを体験してください。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

---