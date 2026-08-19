---
date: 2026-04-05
description: Aspose.PSD for Java を使用して PSD を PNG にエクスポートし、画像のコントラストを簡単に強化する方法を学びましょう。このステップバイステップガイドでレベル調整レイヤーをマスターしてください。
keywords:
- export psd to png
- how to adjust levels
- batch process psd files
linktitle: PSD を PNG にエクスポートし、Java でレベル調整レイヤーをレンダリングする
second_title: Aspose.PSD Java API
title: JavaでPSDをPNGにエクスポートし、レベル調整レイヤーをレンダリングする
url: /ja/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# JavaでPSDをPNGにエクスポートし、レベル調整レイヤーをレンダリングする

## はじめに

PSDファイルを開いたときに、色が平坦に見えたりコントラストが足りないと感じたことはありませんか？Aspose.PSD for Java を使用すれば、**PSDをPNGにエクスポート**しながらレベル調整レイヤーで画像を微調整できます。このチュートリアルでは、PSDの読み込み、レベルの調整、PNGとしての保存までの全工程を順を追って解説し、数分で鮮やかさを高め、Web向けのアセットを作成できるようにします。

## クイック回答
- **「PSDをPNGにエクスポート」とは何ですか？** Photoshopドキュメントを透過性を保持したままロスレスPNG画像に変換します。  
- **エクスポート前にレベルを調整できますか？** はい、Aspose.PSDを使用すると入力および出力レベルをプログラムで変更できます。  
- **ライセンスは必要ですか？** 開発には無料トライアルが使用できますが、本番環境では商用ライセンスが必要です。  
- **バッチ処理は可能ですか？** もちろんです。コードをループ内に配置して複数のPSDファイルを処理できます。  
- **必要なJavaバージョンは？** Java 8以降が推奨されます。

## 「PSDをPNGにエクスポート」とは何ですか？
PSDをPNGにエクスポートするとは、レイヤー構造を持つPhotoshopファイルをフラット化し、Portable Network Graphics 画像に変換することです。PNGはロスレス圧縮とアルファチャンネルをサポートしているため、Webグラフィックや UI アセットに最適です。

## エクスポート前にレベルを調整する理由は？
レベルを調整することで、シャドウ、ミッドトーン、ハイライトをコントロールし、全体的なコントラストとカラーバランスを向上させます。このステップにより、最終的な PNG が手作業で Photoshop で調整する必要なく、洗練された見た目になります。

## 前提条件

- **Java Development Kit (JDK)** – Oracleのウェブサイトから最新バージョンをダウンロードしてください（[https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)）。  
- **Aspose.PSD for Java Library** – 公式ダウンロードページから入手してください（[https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)）。無料トライアルも利用可能です（[https://releases.aspose.com/](https://releases.aspose.com/)）。  

## パッケージのインポート

コードに取り掛かる前に、PSD 操作と PNG エクスポートに必要なクラスをインポートします：

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

## ステップバイステップガイド

### ステップ1: ファイルパスの定義（PSD処理の自動化方法）

ソース PSD、変更後の PSD、最終 PNG のエクスポート先を示す、明確で説明的な変数を設定します。

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

### ステップ2: PSD画像の読み込み

`Image.load` を使用して PSD ファイルを `PsdImage` オブジェクトに読み込みます。Aspose.PSD は自動的にフォーマットを検出します。

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### ステップ3: レイヤーの反復処理（レベル調整方法）

すべてのレイヤーをループし、レベル調整レイヤーを見つけます。

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (code to check for Levels Layer will be added here)
}
```

### ステップ4: レベルレイヤーの特定

`instanceof LevelsLayer` で各レイヤーをチェックします。見つかったらキャストしてプロパティを変更できるようにします。

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (code to adjust levels will be added here)
   }
}
```

### ステップ5: レベルの微調整（レベル調整方法）

最初のチャンネル（通常は合成チャンネル）に対して入力レベルと出力レベルの両方を調整します。これらの値は例示ですので、自由に試してみてください。

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // Adjust Input Levels (0‑255):
	   channel.setInputShadowLevel((short) 10); // Darken shadows slightly
	   channel.setInputMidtoneLevel(2.0f);     // Increase midtones
	   channel.setInputHighlightLevel((short) 230); // Reduce highlights

	   // Adjust Output Levels (0‑255):
	   channel.setOutputShadowLevel((short) 20); // Darken shadows further
	   channel.setOutputHighlightLevel((short) 200); // Brighten highlights
   }
}
```

### ステップ6: 変更されたPSDの保存（PSDの自動化方法）

変更を新しい PSD ファイルに永続化します。

```java
im.save(psdPathAfterChange);
```

### ステップ7: PNGとしてエクスポート（PSDをPNGにエクスポート）

PNG バージョンが必要な場合は `PngOptions` を設定し、画像を保存します。

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

## 一般的な使用例

- **Web資産の準備:** デザイナー提供のPSDモックアップをブラウザ対応のPNGに変換します。  
- **バッチ処理:** CIパイプラインで数十個のPSDファイルの変換を自動化します。  
- **動的画像生成:** エクスポート前にユーザー入力に基づいてレベルをリアルタイムで調整します。  

## トラブルシューティングとヒント

- **レイヤーアクセス時のNullポインタ:** PSDにレベル調整レイヤーが含まれていることを確認してください。含まれていない場合はnullチェックを追加します。  
- **エクスポート後の予期しない色:** 透過性を保持するためにPNGのカラ―タイプが `TruecolorWithAlpha` に設定されていることを確認してください。  
- **多数ファイルでのパフォーマンス:** バッチ処理時に同じ `PsdImage` インスタンスを再利用してメモリ使用量を削減します。  

## よくある質問

**Q: 個別のカラー チャンネル（RGB）を別々に調整できますか？**  
A: はい。`levelsLayer.getChannel(index)` を使用し、`index` = 0 （赤）、1 （緑）、2 （青）で各チャンネルを個別に調整できます。

**Q: 1つのPSDに複数のレベル調整レイヤーがある場合、どう処理しますか？**  
A: ループはすべてのレイヤーを処理します。見つかった各 `LevelsLayer` は `if` ブロック内のコードに従って調整されます。

**Q: レベル以外にコントラストを向上させる方法はありますか？**  
A: Aspose.PSDはカーブ、明るさ/コントラスト、ヒストグラム均等化の調整も提供しています。

**Q: PSDファイルのフォルダーに対して自動化できますか？**  
A: 全体のワークフローを `File[] files = new File(dataDir).listFiles((d, name) -> name.endsWith(".psd"));` ループで囲み、各ファイルを順次処理します。

**Q: さらにドキュメントやサポートはどこで見つけられますか？**  
A: 公式リファレンス（[https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)）とコミュニティフォーラム（[https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)）をご覧ください。

## 結論

**export PSD to PNG** ワークフローと **レベル調整方法** をプログラムで習得することで、Java環境を離れることなく画像品質を完全にコントロールできます。Web用資産の準備、デザインパイプラインの自動化、バッチプロセッサの構築など、どのようなケースでも Aspose.PSD for Java がシンプルかつ信頼性の高い作業を実現します。

---

**最終更新日:** 2026-04-05  
**テスト済み:** Aspose.PSD 24.11 for Java  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}