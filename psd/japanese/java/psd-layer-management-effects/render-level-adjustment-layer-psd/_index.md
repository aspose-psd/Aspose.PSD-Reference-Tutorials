---
title: PSD ファイルのレンダリング レベル調整レイヤー - Java
linktitle: PSD ファイルのレンダリング レベル調整レイヤー - Java
second_title: Aspose.PSD Java API
description: Aspose.PSD for Java を使用して、画像のコントラストと鮮やかさを簡単に高める方法を学びます。このステップバイステップ ガイドでレベル調整レイヤーをマスターします。
type: docs
weight: 17
url: /ja/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
---
## 導入

PSD ファイルを開いたら、画像のコントラストや鮮やかさが欠けていることに気づいたことはありませんか? 画像編集の達人、ご心配なく! Aspose.PSD for Java は、強力なレベル調整レイヤー操作機能でその問題を解決します。このガイドでは、レベルを使用して画像を簡単に微調整するための知識を身に付けることができます。 

## 前提条件

- Java Development Kit (JDK): システムに最新バージョンの JDK がインストールされていることを確認してください。Oracle の Web サイト ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)）。
- Aspose.PSD for Java ライブラリ: ダウンロード ページ ([詳細はこちらpsd/java/](https://releases.aspose.com/psd/java/)）。すべての機能を使用するには有効なライセンスが必要ですが、無料で試用できます（[https://releases.aspose.com/](https://releases.aspose.com/)）。

## パッケージのインポート

コードに進む前に、PSD ファイルとやり取りするために必要な Aspose.PSD クラスをインポートする必要があります。必要なものは次のとおりです。

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

の`com.aspose.psd`パッケージはPSD操作機能へのアクセスを提供しますが、`com.aspose.psd.imaging.PngOptions`画像を PNG として保存する際のオプションを定義できます。

それでは、レベル調整の冒険に出かけましょう。

## ステップ 1: ファイル パスの設定:

- ドキュメントディレクトリの変数を定義します（`dataDir`）、ソースPSDファイル名（`sourceFileName`）、変更後の対象PSDファイル名（`psdPathAfterChange`）、および最終的なPNGエクスポートパス（`pngExportPath`) コードの読みやすさを向上させるために、説明的な名前を使用することを検討してください。

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

## ステップ2: PSDイメージの読み込み:

- 使用`Image.load`ソースPSDファイルを開いて保存する方法`PsdImage`物体 （`im`）。Aspose.PSD はファイル形式を自動的に検出します。

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## ステップ 3: レイヤーの反復処理:

- PSD 内のレベル調整レイヤーを見つける必要があります。Aspose は、ループを使用してすべてのレイヤーを反復処理する便利な方法を提供します。

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (レベル レイヤーを確認するためのコードがここに追加されます)
}
```

## ステップ 4: レベル レイヤーの識別:

- ループ内で、現在のレイヤー（`im.getLayers()[i]` ）は、`LevelsLayer`クラスを使用して`instanceof`オペレーター。 
- もしそうなら、レイヤーを`LevelsLayer`さらなる操作の対象となるオブジェクト。

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ...（レベルを調整するコードはここに追加されます）
   }
}
```
## ステップ 5: レベルの微調整 (続き):

- 出力レベルを調整するには`setOutputShadowLevel`そして`setOutputHighlightLevel`結果の画像の暗さと明るさを制御します。これらの値によって、出力範囲にマッピングされる入力レベルの範囲が決まります。

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   //入力レベルを調整します（0〜255）：
	   channel.setInputShadowLevel((short) 10); //影を少し暗くする
	   channel.setInputMidtoneLevel(2.0f);     //中間調を増やす
	   channel.setInputHighlightLevel((short) 230); //ハイライトを減らす

	   //出力レベルを調整します（0～255）：
	   channel.setOutputShadowLevel((short) 20); //影をさらに暗くする
	   channel.setOutputHighlightLevel((short) 200); //ハイライトを明るくする
   }
}
```

## ステップ6: 変更したPSDを保存する:

- 使用`save`方法の`PsdImage`オブジェクトは変更された画像を指定されたパスに保存します（`psdPathAfterChange`）。

```java
im.save(psdPathAfterChange);
```

## ステップ 7: PNG としてエクスポートする (オプション):

- 調整した画像のPNGバージョンが必要な場合は、`PngOptions`オブジェクトの色の種類を`TruecolorWithAlpha`次に、`save` PNG エクスポート パスとオプションを使用して、メソッドを再度実行します。

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

これで完了です。Aspose.PSD for Java を使用して、PSD ファイルのレベル調整レイヤーを正常に調整できました。これらの手順を理解し、さまざまな値を試すことで、画像のコントラストと全体的な外観を向上させることができます。

## 結論

Aspose.PSD for Java を使用すると、画像編集プロセスを制御できます。レベル調整レイヤーをマスターすることで、写真やデザインに新たな命を吹き込むことができます。練習を重ねれば完璧になります。ためらわずに実験し、この強力なツールの可能性を探求してください。
 
## よくある質問

### 個々のカラーチャンネル (RGB) を個別に調整できますか? 
はい、各カラーチャンネルには`getChannel`方法の`LevelsLayer`オブジェクトを作成し、そのレベルを個別に変更します。

### PSD 内の複数のレベル調整レイヤーをどのように処理しますか?
コードはすべてのレイヤーを反復処理するため、画像内で見つかった追加のレベル レイヤーは自動的に処理されます。

### レベル以外に画像のコントラストを調整する方法はありますか?
もちろんです! Aspose.PSD には、曲線、明るさ/コントラストなどのさまざまな画像調整ツールが用意されています。

### 複数の画像に対してこのプロセスを自動化できますか? 
はい、このコードをループまたはバッチ処理スクリプトに組み込むことで、複数の PSD ファイルを効率的に処理できます。

### さらに詳しい情報やサポートはどこで入手できますか?
Asposeは広範なドキュメントを提供しています（[https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) とサポートフォーラム ([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)ご質問や問題がございましたら、お気軽にお問い合わせください。