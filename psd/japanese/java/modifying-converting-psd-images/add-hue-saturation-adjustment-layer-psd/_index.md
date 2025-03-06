---
title: PSDに色相彩度調整レイヤーを追加する
linktitle: PSDに色相彩度調整レイヤーを追加する
second_title: Aspose.PSD Java API
description: この包括的なステップバイステップのチュートリアルでは、Aspose.PSD for Java を使用して PSD に色相彩度調整レイヤーを追加する方法を学びます。グラフィック デザインのワークフローを強化します。
weight: 14
url: /ja/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSDに色相彩度調整レイヤーを追加する

## 導入
グラフィック デザインでは、色の操作が重要な役割を果たします。特に、色相、彩度、明度を微調整すると、画像の雰囲気や品質が劇的に変化します。これを実現する効果的な方法の 1 つは、Photoshop (PSD ファイル) の調整レイヤーを使用することです。Java を使用してプログラムで PSD ファイルを強化したい場合は、Aspose.PSD ライブラリが役立ちます。このチュートリアルでは、PSD ファイルに色相彩度調整レイヤーを追加して、ワークフローの生産性と効率を高める手順を説明します。
このガイドでは、必要なパッケージのインポートからコード例の細かい詳細まで、すべてをカバーします。
## 前提条件
コードに進む前に、次のものが揃っていることを確認してください。
1.  Java開発キット（JDK）：マシンにJDK 8以上がインストールされていることを確認してください。[Java SE 開発キットのダウンロード](https://www.oracle.com/java/technologies/javase-downloads.html).
2. Aspose.PSD for Javaライブラリ: Aspose.PSDライブラリが必要です。[ここからダウンロード](https://releases.aspose.com/psd/java/). 
3. IDE: Java 開発に適した IntelliJ IDEA や Eclipse などの統合開発環境 (IDE)。
4. 基本的な Java の知識: Java プログラミングの知識があればなお良いですが、心配はいりません。コードをステップごとに説明します。
前提条件が整ったので、楽しい部分であるコーディングに進みましょう。
## パッケージのインポート
Aspose.PSD ライブラリの使用を開始するには、まず必要なクラスをインポートします。Java ファイルでこれを行う方法は次のとおりです。
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```
これらのインポートがシームレスに機能するように、適切なライブラリがプロジェクトに追加されていることを確認してください。
## ステップ1: ドキュメントディレクトリを設定する
すべてのプロジェクトには開始点が必要ですが、私たちのプロジェクトも例外ではありません。PSD ファイルが保存されているディレクトリを指定する必要があります。これは、画像を適切に読み込み、保存するために非常に重要です。
```java
String dataDir = "Your Document Directory"; //このパスを実際のディレクトリに更新します
```
## ステップ2: 既存のPSDファイルを読み込む
既存の PSD ファイルを操作するには、まずそれをプログラムに読み込む必要があります。その方法は次のとおりです。
```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
このコードでは、更新`"HueSaturationAdjustmentLayer.psd"`編集する既存の PSD ファイルの名前に置き換えます。
## ステップ3: 色相/彩度レイヤーを編集する
次に、読み込んだ PSD 画像のレイヤーをループして、既存の色相/彩度レイヤーを見つけて編集します。この手順では、色相、彩度、明度の値を変更します。
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
この例では、
- 色相を -25、彩度を -12、明度を +67 に調整します。
- の`getRange(2)`この方法を使用すると、必要に応じて特定の色の範囲を微調整できます。
## ステップ4: 変更したPSDファイルを保存する
調整を行った後、次のステップはファイルを保存することです。これは、行った変更が失われないようにするためのプロセスの重要な部分です。
```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
## ステップ5: 新しい色相/彩度レイヤーを追加する
次に、別の PSD ファイルに新しい色相/彩度調整レイヤーを追加したい場合があります。異なる PSD ファイルで、以前と同じアプローチに従ってください。
```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```
## ステップ6: 新しいレイヤーに新しい色相/彩度の値を設定する
新しいレイヤーを作成したので、前と同じように、希望する色相、彩度、明度の設定を適用します。
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
## ステップ7: 更新されたPSDファイルを保存する
最後に、変更内容を確認できるように、色相/彩度レイヤーを追加した PSD ファイルを保存します。
```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```
おめでとうございます! Aspose.PSD for Java を使用して PSD ファイルの操作に成功しました。これで、さまざまな画像やより詳細な変更を試して、グラフィック デザイン プロジェクトを実現できます。
## 結論
プログラムでグラフィックを操作すると、可能性の世界が広がります。Aspose.PSD for Java を使用して色相彩度調整レイヤーを追加および変更すると、柔軟性と効率性が向上し、デザイン ワークフローが合理化されます。プロジェクトの写真を強化する場合でも、魅力的なビジュアル コンテンツを作成する場合でも、これらのツールを習得すると、出力を大幅に向上できます。
 Aspose.PSDのさらなる機能については、以下をご覧ください。[ドキュメント](https://reference.aspose.com/psd/java/)または、[一時ライセンス](https://purchase.aspose.com/temporary-license/)ライブラリの全機能をテストします。
## よくある質問
### 色相彩度調整レイヤーとは何ですか?
色相/彩度調整レイヤーを使用すると、元のピクセルを永続的に変更せずに、画像の色のプロパティを変更できます。
### Aspose.PSD を使用するには Photoshop をインストールする必要がありますか?
いいえ、Aspose.PSD は Photoshop から独立して動作するスタンドアロン ライブラリです。
### Aspose.PSD をバッチ処理に使用できますか?
はい、Aspose.PSD を使用すると、複数の PSD ファイルを自動化してバッチ処理できます。
### Aspose.PSD は無料ですか?
Aspose.PSDは無料トライアルを提供していますが、長期使用にはライセンスが必要です。価格を見ることができます。[ここ](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
