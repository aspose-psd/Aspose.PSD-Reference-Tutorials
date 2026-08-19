---
date: 2026-04-03
description: Aspose.PSD for Java を使用して、ストローク効果とカラー塗りつぶしを適用した PSD を PNG として保存する方法を学びましょう。このステップバイステップガイドでは、PSD
  を PNG にすばやくエクスポートする手順を示します。
keywords:
- save psd as png
- export psd to png
- set stroke color
- apply layer effects
- customize stroke width
linktitle: ストローク効果付きでPSDをPNGとして保存 – Java
second_title: Aspose.PSD Java API
title: ストローク効果付きでPSDをPNGとして保存 – Java
url: /ja/java/psd-layer-management-effects/apply-stroke-effect-color-fill-psd/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ストローク効果とカラー塗りつぶしで PSD を PNG に保存 – Java

## はじめに

このガイドでは、Aspose.PSD for Java を使用して **PSD を PNG に保存** しながら、ストローク効果とカラー塗りつぶしを適用する方法を学びます。経験豊富な開発者でも初心者でも、ステップバイステップのチュートリアルで簡単に作業を完了できます。環境設定から最終画像のエクスポートまでを網羅し、プロジェクトで **PSD を PNG にエクスポート** できるようになります。

## クイック回答
- **このチュートリアルの目的は何ですか？** カスタマイズ可能なストローク効果を適用した後、PSD ファイルを PNG に保存する方法を示します。  
- **使用するライブラリはどれですか？** Aspose.PSD for Java。  
- **ライセンスは必要ですか？** テスト用の無料トライアルは利用可能ですが、本番環境ではライセンスが必要です。  
- **ストロークの色は変更できますか？** はい、`ColorFillSettings` を介して任意の色を設定できます。  
- **バッチ処理は可能ですか？** もちろんです。コードをループでラップすれば複数の PSD ファイルを処理できます。

## 「PSD を PNG に保存」とは？
PSD を PNG に保存するとは、Photoshop のネイティブなレイヤー形式のファイルを、視覚的な忠実度を保ちつつフラットな Web 向け画像形式に変換することです。PSD コンテンツをウェブサイトやモバイルアプリ、PSD を直接サポートしないプラットフォームで表示したい場合に便利です。

## なぜストローク効果とカラー塗りつぶしを適用するのか？
ストロークはレイヤー内容の周囲に鮮明な輪郭を付加し、複雑な背景に対してグラフィックを際立たせます。カスタム塗りつぶしカラーと組み合わせることで、ブランドイメージの統一や UI 要素の強調、目を引くサムネイル作成が Photoshop を離れずに実現できます。

## 前提条件

1. **Java Development Kit (JDK) 8+** – `java` が PATH に設定されていることを確認してください。  
2. **Aspose.PSD for Java** – [website](https://releases.aspose.com/psd/java/) からダウンロードしてください。  
3. **IDE** – IntelliJ IDEA、Eclipse、またはお好みのエディタ。  
4. **サンプル PSD** – 既にストローク効果が含まれているファイル（または Photoshop で追加してください）。  
5. **基本的な Java 知識** – 数行のコードを書くだけで、特別な高度な知識は不要です。

これらが揃ったら、コーディングを開始できます。

## パッケージのインポート

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

これらのインポートは、PSD の読み込み、ストロークの変更、PSD と PNG の両方の出力に必要なクラスをすべて取り込みます。

## ストローク効果付きで PSD を PNG に保存する方法

### 手順 1: PSD ファイルを読み込む

まず、ソース PSD が格納されているフォルダを指定します。

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` を実際のパスに置き換えてください。

次に、既存のエフェクトリソースを保持したままファイルを読み込みます。

```java
String sourceFileName = dataDir + "StrokeComplex.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### 手順 2: ストロークカラーを設定（必要に応じて幅もカスタマイズ）

以下のループは各レイヤーを走査し、最初の `StrokeEffect` を取得して塗りつぶしカラーを変更します。必要に応じて `setWidth` や `setPosition` でストローク幅や位置も調整できます。

```java
for (int i = 0; i < im.getLayers().length; i++) {
    StrokeEffect effect = (StrokeEffect) im.getLayers()[i].getBlendingOptions().getEffects()[0];
    ColorFillSettings settings = (ColorFillSettings) effect.getFillSettings();
    // Set the stroke color – change to any Color you like
    settings.setColor(Color.getDeepPink());
}
```

> **プロのコツ:** `Color.getDeepPink()` は例です。カスタム RGB 値は `new Color(r, g, b)` を使用してください。

### 手順 3: 変更した PSD を保存（オプション）

更新されたストロークを保持した PSD バージョンを残したい場合は、次のように保存します。

```java
String exportPath = dataDir + "StrokeComplexRendering.psd";
im.save(exportPath, new PsdOptions());
```

### 手順 4: 画像を PNG としてエクスポート（「PSD を PNG に保存」のコアステップ）

最後に、編集した PSD を Web 用に最適化された PNG ファイルに変換します。

```java
String exportPathPng = dataDir + "StrokeComplexRendering.png";
PngOptions option = new PngOptions();
option.setColorType(PngColorType.TruecolorWithAlpha);

im.save(exportPathPng, option);
```

PNG は先ほど設定したディープピンクのストロークを保持し、`TruecolorWithAlpha` オプションにより透過も保たれます。

## よくある問題と解決策

| 問題 | 原因 | 対策 |
|------|------|------|
| **`ArrayIndexOutOfBoundsException`** | レイヤーにエフェクトが無い、または最初のエフェクトが `StrokeEffect` ではありません。 | レイヤーにストロークが実際に含まれているか確認するか、`getEffects()` を反復して正しいタイプを探してください。 |
| **Color not changing** | 設定のコピーを編集していて、元の設定を変更していない可能性があります。 | `effect.getFillSettings()` から直接 `ColorFillSettings` にキャストしていることを確認してください。 |
| **PNG appears blank** | レイヤーをラスタライズせずに PSD を読み込んだためです。 | すべての変更後に `im.save(..., new PngOptions())` を呼び出してください。変更前に元の `im` を保存しないようにします。 |

## FAQ

**Q: Aspose.PSD for Java を使用して、単一レイヤーに複数のエフェクトを適用できますか？**  
A: はい、レイヤーのブレンドオプションにアクセスし、必要に応じてシャドウ、グロー、ストロークなど複数のエフェクトを追加できます。

**Q: 複数の PSD ファイルをバッチ処理で自動化できますか？**  
A: もちろんです。ディレクトリ内のファイルを `for‑each` ループで回し、読み込み、エフェクト適用、保存のロジックをまとめて実行できます。

**Q: PSD ファイルへの変更を元に戻すにはどうすればよいですか？**  
A: 変更を保存する前に元のファイルを再度読み込みます。Aspose.PSD には Undo スタックがありません。

**Q: ストロークの幅や位置をカスタマイズできますか？**  
A: はい。`effect.setWidth(float)` と `effect.setPosition(StrokeEffect.Position)` を使用して、太さと配置（内部、外部、または中央）を制御できます。

**Q: Aspose.PSD for Java ライブラリは無料で使用できますか？**  
A: 評価用の無料トライアルがあります。フル機能を使用するにはライセンスの購入が必要です。詳細は [buy options](https://purchase.aspose.com/buy) をご覧ください。

---

**最終更新日:** 2026-04-03  
**テスト環境:** Aspose.PSD 24.12 for Java  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}