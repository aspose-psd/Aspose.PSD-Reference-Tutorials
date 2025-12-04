---
date: 2025-12-04
description: Aspose.PSD for Java を使用して PSD を PNG として保存し、レンダリング ドロップ シャドウを適用する方法を学びます。このガイドでは、シャドウの追加、PSD
  から PNG への変換、そして Java でのドロップ シャドウの適用方法をカバーしています。
language: ja
linktitle: Apply Rendering Drop Shadow
second_title: Aspose.PSD Java API
title: Aspose.PSD JavaでPSDをPNGとして保存し、ドロップシャドウを追加する
url: /java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD を PNG に保存し、Aspose.PSD Java でドロップシャドウを追加

## はじめに

Java で Photoshop ファイルを扱う場合、**PSD を PNG に保存**しながらプロフェッショナルなドロップシャドウを付加することは一般的な要件です。Aspose.PSD を使用すれば、この作業は数行のコードで簡単に実現でき、**PSD から PNG への変換**と**Java でのドロップシャドウ適用**が可能です。このチュートリアルでは、PSD ファイルの読み込みから最終的な PNG のエクスポートまで、シャドウ効果が描画された状態での手順をすべて解説します。

## クイック回答
- **「PSD を PNG に保存」とは何ですか？** レイヤー構造を持つ Photoshop ファイルを、透過情報を保持したフラットな PNG 画像に変換することです。  
- **変換時にドロップシャドウを追加できますか？** はい。Aspose.PSD ではエクスポート前にレイヤー効果を変更できます。  
- **コード実行にライセンスは必要ですか？** 評価用の無料トライアルで動作しますが、本番環境ではライセンスが必要です。  
- **対応している Java のバージョンは？** Java 8 以降。  
- **ドロップシャドウ効果はカスタマイズできますか？** もちろんです。色、透明度、距離、サイズ、角度などを自由に調整できます。

## 前提条件

作業を始める前に以下を用意してください。

- **Java 開発環境** – JDK 8 以上がインストールされていること。  
- **Aspose.PSD ライブラリ** – 公式サイトから最新の JAR をダウンロードしてください [here](https://releases.aspose.com/psd/java/)。  
- **PSD ファイル** – シャドウを付けたいレイヤーが最低 1 つ含まれているファイル。  

## Java で PSD を PNG に保存し、ドロップシャドウを付加する方法

以下はステップバイステップのガイドです。各ステップには簡単な説明と、コピーして使用できる正確なコードが示されています。

### 手順 1: 必要なパッケージをインポート

画像の読み込み、エフェクト操作、PNG エクスポートに必要なクラスをインポートします。

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

### 手順 2: ドキュメントディレクトリを定義

ソース PSD と生成される PNG が格納されるフォルダーを設定します。

```java
String dataDir = "Your Document Directory";
```

### 手順 3: PSD と PNG のファイルパスを設定

入力 PSD と出力 PNG のフルパスを指定します。

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### 手順 4: エフェクトを有効にして PSD ファイルを読み込む

**loadEffectsResource** を有効にすると、レイヤー効果（シャドウなど）を操作できるようになります。

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### 手順 5: ドロップシャドウ効果にアクセス

ここでは、2 番目のレイヤー（インデックス 1）に適用されている最初のエフェクトを取得します。ここでシャドウのパラメータを読み取ったり変更したりします。

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### 手順 6: シャドウ効果のプロパティを検証（任意だが推奨）

既存のプロパティを確認することで、変更が必要かどうか判断できます。以下のアサーションはデフォルト値を確認します。

```java
Assert.areEqual(Color.getBlack(), shadowEffect.getColor());
Assert.areEqual(255, shadowEffect.getOpacity());
Assert.areEqual(3, shadowEffect.getDistance());
Assert.areEqual(7, shadowEffect.getSize());
Assert.areEqual(true, shadowEffect.getUseGlobalLight());
Assert.areEqual(90, shadowEffect.getAngle());
Assert.areEqual(0, shadowEffect.getSpread());
Assert.areEqual(0, shadowEffect.getNoise());
```

> **プロのコツ:** カスタム設定で **シャドウを追加** したい場合は、`shadowEffect` のプロパティを保存前に変更してください（例: `shadowEffect.setColor(Color.getRed());`）。

### 手順 7: 変更した画像を PNG として保存

最後に、レンダリングされたシャドウを含む PSD を PNG ファイルにエクスポートします。`TruecolorWithAlpha` オプションにより透過情報が保持されます。

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

これで、**PSD から PNG への変換**と**Java でのドロップシャドウ適用**を一括で行う完全なワークフローが完成です。

## なぜ Aspose.PSD をこのタスクに選ぶのか？

- **Photoshop が不要** – Java が動作する任意のプラットフォームで利用可能。  
- **PSD の完全再現** – すべてのレイヤー情報、マスク、エフェクトが保持されます。  
- **細かい制御** – エクスポート前にドロップシャドウの各パラメータを調整可能。  
- **高性能** – 大容量ファイルやバッチ処理に最適化されています。

## よくある問題とトラブルシューティング

| 症状 | 考えられる原因 | 対策 |
|------|----------------|------|
| `NullPointerException` が `shadowEffect` で発生 | 対象レイヤーにエフェクトが無い、またはインデックスが間違っている | レイヤーインデックス (`im.getLayers()[i]`) を確認し、エフェクトが存在することを確認 |
| エクスポートした PNG が真っ白 | PNG オプションが正しく設定されていない、または画像が保存されていない | `PngColorType.TruecolorWithAlpha` を使用し、`im.save()` のパスが書き込み可能か確認 |
| シャドウの色が見えない | シャドウの不透明度が 0、または背景と同色になっている | `shadowEffect.setOpacity(255);` で不透明度を上げ、コントラストのある色を選択 |

## FAQ（よくある質問）

**Q: 複数のレイヤーに同時にドロップシャドウを適用できますか？**  
A: はい。`im.getLayers()` をループし、各レイヤーの `DropShadowEffect` を必要に応じて変更してください。

**Q: “Spread” パラメータは何を制御しますか？**  
A: シャドウが完全に不透明から透明になる過程の急激さを決めます。値が大きいほどエッジがハードになります。

**Q: Aspose.PSD はすべての Photoshop バージョンに対応していますか？**  
A: 初期の PSD 形式から最新の Photoshop CC ファイルまで、幅広いバージョンをサポートしています。

**Q: 問題が発生した場合、どこでサポートを受けられますか？**  
A: [Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34) でコミュニティと公式サポートが利用できます。

**Q: 購入前に Aspose.PSD を試すことはできますか？**  
A: もちろんです。無料トライアルは [Aspose のウェブサイト](https://releases.aspose.com/) からダウンロードできます。

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**最終更新日:** 2025-12-04  
**テスト環境:** Aspose.PSD 24.12 for Java  
**作者:** Aspose  

---