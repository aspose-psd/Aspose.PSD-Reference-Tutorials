---
date: 2026-10-18
description: Aspose.PSD を使用して Java 画像にラジアルグラデーション効果を作成する方法を学びます。シームレスな統合のためのステップバイステップガイドに従ってください。
keywords:
- create radial gradient java
- apply gradient overlay psd
- add radial gradient image
lastmod: 2026-10-18
linktitle: gradient 効果を追加
og_description: Aspose.PSD を使用して Java のラジアルグラデーション効果を作成する方法を学びます。このチュートリアルでは、数分で gradient
  オーバーレイを追加、カスタマイズ、保存する方法を示します。
og_image_alt: Screenshot of Aspose.PSD Java code creating a radial gradient effect
og_title: Aspose.PSD で Java のラジアルグラデーションを作成 – ステップバイステップガイド
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Learn how to create radial gradient effects in Java images using Aspose.PSD.
    Follow this step‑by‑step guide for seamless integration.
  headline: How to create radial gradient effects in Aspose.PSD for Java
  type: TechArticle
- description: Learn how to create radial gradient effects in Java images using Aspose.PSD.
    Follow this step‑by‑step guide for seamless integration.
  name: How to create radial gradient effects in Aspose.PSD for Java
  steps:
  - name: Load the PSD file and access the gradient overlay
    text: '`PsdLoadOptions` configures how a PSD file is loaded, allowing you to enable
      loading of effect resources. `Image.load` reads the file into an `Image` object.
      In this step, we load a PSD file and retrieve the first `GradientOverlayEffect`
      from the second layer (index 1). The `loadOptions.setLoadEffec'
  - name: Verify Initial Settings
    text: Before making changes, it’s a good practice to confirm the current blend
      mode, opacity, and visibility. This helps you understand the baseline state
      of the gradient overlay.
  - name: Modify Gradient Settings
    text: Here you can customize the gradient’s color, opacity, and blend mode. The
      example changes the color to green, reduces opacity to 193 (out of 255), and
      switches the blend mode to **Lighten**. Feel free to experiment with other `BlendMode`
      values such as `Multiply`, `Screen`, or `Overlay`.
  - name: Save the Edited Image
    text: After applying your modifications, persist the changes by saving the PSD
      to a new file. This step ensures the original file remains untouched.
  - name: Verify Changes
    text: The snippet above demonstrates how to open a PSD, pull the second layer’s
      first effect (assumed to be a gradient overlay), and prepare it for modification.
  - name: Verify the original settings (optional but recommended)
    text: Before you change anything, checking the existing blend mode, opacity, and
      visibility helps you understand the baseline. The `Assert` calls in the code
      confirm that the effect is currently set to **Normal** blend mode, fully opaque,
      and visible.
  - name: Adjust gradient properties to achieve a radial style
    text: 'You can change the gradient’s color, opacity, and blend mode. For a true
      radial effect, set the gradient style: *Pro tip:* Use `Color.getGreen()` or
      any `java.awt.Color` instance to define the start color, and `gradientOverlay.setColor2(Color.getBlue())`
      for the end color.'
  - name: Save the edited PSD
    text: Calling `im.save(exportPath);` writes the modified image to disk. The saved
      file retains the radial gradient overlay and can be opened in Photoshop, previewed
      in browsers, or converted to other formats.
  type: HowTo
- questions:
  - answer: Yes. Retrieve the layer’s `BlendingOptions`, iterate through the `Effects`
      collection, and add a new `GradientOverlayEffect` for each gradient you need.
    question: Can I apply multiple gradient effects to a single image?
  - answer: Aspose.PSD provides shadows, glows, bevels, and more. Each effect appears
      in the `Effects` array and can be configured independently.
    question: What other effects can I combine with gradient overlays?
  - answer: Verify that the PSD was loaded with `setLoadEffectsResource(true)`, check
      layer visibility, and confirm you are modifying the correct effect index.
    question: How can I troubleshoot if the effects are not rendering correctly?
  - answer: Yes, you can get a free trial [here](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.PSD for Java?
  - answer: Visit the [purchase page](https://purchase.aspose.com/buy) for licensing
      information.
    question: Where can I purchase a license for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- create radial gradient
- gradient overlay effect
- Aspose.PSD Java
title: Aspose.PSD for Javaでラジアルグラデーション効果を作成する方法
url: /ja/java/advanced-image-effects/add-gradient-effects/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Javaで放射状グラデーション効果を作成する方法

## はじめに

このガイドでは、Aspose.PSD ライブラリを使用して **create radial gradient java** 効果を作成する方法を学びます。放射状グラデーションは、Photoshop を開かずに PSD レイヤーに深み、焦点、または微妙な光彩を追加するのに最適です。チュートリアルの最後までに、PSD を読み込み、グラデーションオーバーレイを適用し、プロパティを調整し、結果を保存できるようになります—すべて Java コードだけで実行できます。

## クイック回答
- **What can I achieve?** PSD レイヤー上で放射状グラデーションオーバーレイを追加、編集、ブレンドできます。  
- **Which library is required?** Aspose.PSD for Java（最新バージョン）。  
- **Do I need a license?** 開発には無料トライアルが利用可能です。商用利用にはライセンスが必要です。  
- **How long does implementation take?** 基本的な放射状グラデーションオーバーレイでおおよそ 10‑15 分です。  
- **Is it compatible with Java 8+?** はい、API は Java 8 以降のランタイムをサポートしています。

## 前提条件

チュートリアルに入る前に、以下の前提条件が整っていることを確認してください。

1. **Aspose.PSD for Java Library** – Aspose.PSD for Java ライブラリをダウンロードしてインストールしてください。ライブラリとドキュメントは [Aspose.PSD Java documentation page](https://reference.aspose.com/psd/java/) にあります。  
2. **Java Development Environment** – マシンに Java 開発環境（JDK 8 以上、好みの IDE）をセットアップしてください。  
3. **Latest Aspose.PSD release** – 最新バージョンは [Aspose releases page](https://releases.aspose.com/) からダウンロードできます。  
4. **Support resources** – 問題が発生した場合は、[Aspose.PSD Support forum](https://forum.aspose.com/c/psd/34) を参照してください。  
5. **License purchase** – 本番環境で使用する際は、[purchase page](https://purchase.aspose.com/buy) からライセンスを取得してください。

すべての準備が整ったら、ステップバイステップのガイドに進みましょう。

## グラデーションオーバーレイ効果とは？

グラデーションオーバーレイ効果は、レイヤーの選択領域全体に 2 色以上の滑らかな色変化を描画します。Photoshop ではこの効果をブレンド、カラー、位置調整でき、洗練されたビジュアルデザインを作成できます。`GradientOverlayEffect` クラスは Aspose.PSD における同様のレイヤースタイルを表し、カラー ストップ、透明度、ブレンドモード、グラデーションスタイルなどのプロパティを公開します。

## 放射状グラデーション効果の作成方法

PSD を読み込み、対象レイヤーを特定し、`GradientOverlayEffect` のプロパティを調整し、最後にファイルを保存します。画像がロードされたら、わずか 4 行の Java コードで完結します。

### 手順 1: PSD ファイルを読み込み、グラデーションオーバーレイにアクセスする

`PsdLoadOptions` は PSD ファイルの読み込み方法を構成し、エフェクトリソースのロードを有効にできます。`Image.load` はファイルを `Image` オブジェクトに読み込みます。

```javaString dataDir = "Your Document Directory";

// Gradient overlay effect. Example
String sourceFileName = dataDir + "GradientOverlay.psd";
String exportPath = dataDir + "GradientOverlayChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);

GradientOverlayEffect gradientOverlay = (GradientOverlayEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

この手順では PSD ファイルを読み込み、2 番目のレイヤー（インデックス 1）から最初の `GradientOverlayEffect` を取得します。`loadOptions.setLoadEffectsResource(true)` 呼び出しにより、エフェクトリソースが編集可能になります。

### 手順 2: 初期設定の確認

```java
// Verify initial settings
Assert.areEqual(BlendMode.Normal, gradientOverlay.getBlendMode());
Assert.areEqual(255, gradientOverlay.getOpacity());
Assert.areEqual(true, gradientOverlay.isVisible());
// ... (additional verifications)
```

変更を加える前に、現在のブレンドモード、透明度、可視性を確認することをお勧めします。これにより、グラデーションオーバーレイのベースライン状態が把握できます。

### 手順 3: グラデーション設定の変更

```java
// Modify gradient settings
settings.setColor(Color.getGreen());
gradientOverlay.setOpacity((byte)193);
gradientOverlay.setBlendMode(BlendMode.Lighten);
// ... (additional modifications)
```

ここではグラデーションの色、透明度、ブレンドモードをカスタマイズできます。例では色を緑に変更し、透明度を 193（255 中）に下げ、ブレンドモードを **Lighten** に切り替えています。`BlendMode` の他の値（`Multiply`、`Screen`、`Overlay` など）でも試してみてください。

### 手順 4: 編集した画像の保存

```java
// Save the edited image
im.save(exportPath);
```

変更を適用したら、PSD を新しいファイルに保存して変更を永続化します。この手順により元のファイルはそのまま残ります。

### 手順 5: 変更の確認

```java
// Verify changes after editing
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);

GradientOverlayEffect gradientOverlayEffect = (GradientOverlayEffect)img.getLayers()[1].getBlendingOptions().getEffects()[0];
// ... (additional verifications)
```

上記スニペットは、PSD を開き、2 番目のレイヤーの最初のエフェクト（グラデーションオーバーレイと想定）を取得し、変更の準備をする方法を示しています。

### 手順 2: 元の設定の確認（任意だが推奨）

何も変更する前に、既存のブレンドモード、透明度、可視性を確認するとベースラインが把握しやすくなります。コード内の `Assert` 呼び出しは、エフェクトが現在 **Normal** ブレンドモードで、完全に不透明かつ可視であることを確認します。

### 手順 3: 放射状スタイルを実現するためにグラデーションプロパティを調整する

グラデーションの色、透明度、ブレンドモードを変更できます。真の放射状効果を得るには、グラデーションスタイルを設定します：

```java
gradientOverlay.setGradientStyle(GradientStyle.Radial);
gradientOverlay.setAngle(0f); // angle is ignored for radial, but required by API
gradientOverlay.setScale(100f); // 100 % fills the layer
```

*プロのヒント:* `Color.getGreen()` や任意の `java.awt.Color` インスタンスで開始色を定義し、`gradientOverlay.setColor2(Color.getBlue())` で終了色を設定します。

### 手順 4: 編集した PSD の保存

`im.save(exportPath);` を呼び出すと、変更された画像がディスクに書き込まれます。保存されたファイルは放射状グラデーションオーバーレイを保持し、Photoshop で開いたり、ブラウザでプレビューしたり、他のフォーマットに変換したりできます。

## なぜ放射状グラデーションオーバーレイを作成するのか？

放射状グラデーションはデザインに深みと焦点を加え、要素を立体的またはスポットライト効果に見せます。以下のようなシーンに最適です：

- **背景の塗りつぶし**：中央の被写体へ視線を誘導します。  
- **ボタンやアイコンのハイライト**：微細な光彩が必要な場合に。  
- **クリエイティブな写真効果**：ビネットや光のバーストなど。  

Aspose.PSD は **50 以上の入出力フォーマット** を処理でき、数百ページに及ぶ PSD ファイルでも全体をメモリに読み込まずに扱えるため、大規模なアセットライブラリでのグラデーション自動生成が可能です。

## よくある問題とヒント

- **Effect not visible:** `gradientOverlay.isVisible()` が `true` を返すことを確認してください。一部の PSD はデフォルトでエフェクトを非表示にします。  
- **Incorrect layer index:** レイヤーは 0 ベースです。正しいレイヤーを対象にしているか二重チェックしてください（`im.getLayers()[1]` は 2 番目のレイヤーを指します）。  
- **Opacity casting:** `setOpacity` メソッドは `byte` を期待します。`int` を渡すとコンパイルエラーになるため、明示的にキャストしてください。  
- **Resource loading:** エフェクトに `null` が返る場合は、画像読み込み前に `loadOptions.setLoadEffectsResource(true)` が設定されているか確認してください。

## よくある質問

**Q: 1 つの画像に複数のグラデーション効果を適用できますか？**  
A: はい。レイヤーの `BlendingOptions` を取得し、`Effects` コレクションを走査して、必要な数だけ新しい `GradientOverlayEffect` を追加できます。

**Q: グラデーションオーバーレイと組み合わせられる他のエフェクトはありますか？**  
A: Aspose.PSD は影、光彩、ベベルなどを提供します。各エフェクトは `Effects` 配列に現れ、個別に設定可能です。

**Q: エフェクトが正しく描画されない場合のトラブルシューティングは？**  
A: `setLoadEffectsResource(true)` で PSD をロードしたか、レイヤーの可視性を確認し、正しいエフェクトインデックスを変更しているかをチェックしてください。

**Q: Aspose.PSD for Java のトライアル版はありますか？**  
A: はい、無料トライアルは [here](https://releases.aspose.com/) から入手できます。

**Q: Aspose.PSD for Java のライセンスはどこで購入できますか？**  
A: ライセンス情報は [purchase page](https://purchase.aspose.com/buy) をご覧ください。

## 追加の FAQ

**Q: プログラムからグラデーションの方向を変更できますか？**  
A: はい。`GradientOverlayEffect.setAngle(float angle)` メソッドで角度（度）を設定できます。放射状グラデーションでは角度は無視されますが、メソッドは呼び出す必要があります。

**Q: Aspose.PSD は放射状グラデーションをサポートしていますか？**  
A: 完全にサポートしています。`GradientOverlayEffect` のプロパティで `GradientStyle.Radial` を設定してください。

**Q: PSD を他のフォーマット（例: PNG）に変換した際にグラデーションオーバーレイは保持されますか？**  
A: PSD をラスタライズして PNG などで保存すると、グラデーションオーバーレイの視覚結果は保持されますが、エフェクト自体はピクセルデータの一部になります。

**Q: レイヤーからグラデーションオーバーレイを削除するには？**  
A: レイヤーの `BlendingOptions` を取得し、`Effects` コレクション内の `GradientOverlayEffect` を見つけて `remove(effect)` で削除します。

**Q: グラデーションの変化をアニメーション化できますか？**  
A: Aspose.PSD は直接アニメーションを扱いませんが、異なるグラデーションパラメータで PSD ファイルを連続生成し、別のライブラリで動画や GIF に組み立てることが可能です。

## 結論

おめでとうございます！Aspose.PSD for Java を使用して画像に **create radial gradient java** 効果を作成する方法を学びました。上記手順に従えば、プログラムでグラデーションオーバーレイを追加、変更、保存でき、PSD アセットに対する完全なクリエイティブコントロールが得られます。さまざまな色、ブレンドモード、透明度で実験し、必要なビジュアルインパクトを実現してください。

---

**Last Updated:** 2026-10-18  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  








```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.*;
import com.aspose.psd.fileformats.psd.layers.layereffects.GradientOverlayEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## 関連チュートリアル

- [Java と Aspose.PSD を使用してグラデーション塗りつぶし PSD を作成 – グラデーション塗りつぶしレイヤーの追加](/psd/java/psd-image-modification-conversion/add-gradient-fill-layer-psd-files/)
- [パターンオーバーレイ PSD: Aspose.PSD for Java でエフェクトを追加](/psd/java/advanced-image-effects/add-pattern-effects/)
- [Java でカラーオーバーレイを適用し不透明度を設定 – Aspose.PSD 使用](/psd/java/image-editing/color-overlay-effect/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}