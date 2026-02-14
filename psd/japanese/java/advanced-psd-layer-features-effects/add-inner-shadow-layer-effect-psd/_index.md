---
date: 2026-02-14
description: Aspose.PSD for Java を使用して PSD にインナーレイヤーのシャドウを追加し、プログラムで PSD レイヤー効果を適用する方法を、ステップバイステップのチュートリアルで学びましょう。ヒントやベストプラクティスも含んでいます。
linktitle: Add Inner Shadow PSD Layer Effect in Java
second_title: Aspose.PSD Java API
title: Javaで内部シャドウのPSDレイヤー効果を追加する方法
url: /ja/java/advanced-psd-layer-features-effects/add-inner-shadow-layer-effect-psd/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java でインナ―シャドウ PSD レイヤー効果を追加する方法

## Introduction
プログラムで **インナ―シャドウ PSD** を追加したい場合は、ここが適切な場所です。このガイドでは、Aspose.PSD for Java を使用して任意の Photoshop ドキュメントに **インナ―シャドウ** を追加する方法を示します。バッチ処理ツール、自動デザインパイプラインの構築、あるいは画像効果の実験など、以下の手順で Java アプリケーションに統合可能な本格的なソリューションを提供します。

## Quick Answers
- **What library do I need?** Aspose.PSD for Java.  
- **How long does the implementation take?** Around 10‑15 minutes for a basic setup.  
- **Do I need Photoshop installed?** No, the library works independently of Photoshop.  
- **Can I change the shadow color?** Yes – the `setColor` method accepts any `Color`.  
- **Is a license required for production?** A commercial license is required; a free trial is available.

## What is “add inner shadow psd”?
PSD ファイルにインナ―シャドウを追加することは、レイヤー内部に微妙な陰影効果を作り、奥行きを表現することを意味します。この効果は、UI 要素やアイコン、テキストを外部の光彩を付けずに際立たせる際に一般的に使用されます。

## Why apply PSD layer effect with Java?
Java で **PSD レイヤー効果を適用** すると、繰り返しのデザイン作業を自動化でき、バックエンドサービスに画像処理を組み込んだり、手動で Photoshop を操作せずに資産をオンザフライで生成したりできます。Aspose.PSD は、PSD ファイル形式の複雑さを抽象化したクリーンなオブジェクト指向 API を提供します。

## Prerequisites
コードに入る前に、以下を用意してください。

1. **Java Development Kit (JDK 11 以上)** – [Oracle のウェブサイト](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) からダウンロード。  
2. **Aspose.PSD for Java** – [Aspose のリリースページ](https://releases.aspose.com/psd/java/) から最新の JAR を取得。  
3. **IDE** – IntelliJ IDEA、Eclipse、または NetBeans（いずれでも可）。  
4. **Basic Java knowledge** – クラス、オブジェクト、例外処理に慣れていること。  
5. **Sample PSD file** – テスト用に少なくとも 1 つのレイヤーがあるシンプルな PSD。

## Import Required Packages
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.layereffects.IShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```
これらのインポートにより、PSD の読み込み、レイヤー操作、シャドウ効果の設定に必要なコアクラスへアクセスできます。

## How to add inner shadow psd in a PSD file using Java
以下はステップバイステップのガイドです。各ステップに簡単な説明と、コピーすべき正確なコードを示します。

### Step 1: Define source and destination directories
```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String sourceFile = sourceDir + "sample.psd";
String destName = outputDir + "sample_out.psd";
```
プレースホルダーのパスを、実際の環境に合わせて置き換えてください。

### Step 2: Load the PSD file with effect resources
```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage image = (PsdImage) Image.load(sourceFile, loadOptions);
```
`setLoadEffectsResource(true)` により、既存のレイヤー効果も読み込まれ、変更が可能になります。

### Step 3: Access the target layer
```java
try {
    Layer layer = image.getLayers()[image.getLayers().length - 1];
```
ここではドキュメントの **最後のレイヤー** を取得しています。別のレイヤーを対象にしたい場合はインデックスを調整してください。

### Step 4: Configure the inner shadow effect
```java
    IShadowEffect shadowEffect = (IShadowEffect) layer.getBlendingOptions().getEffects()[0];
    shadowEffect.setColor(Color.getGreen());
    shadowEffect.setOpacity((byte) 128);
    shadowEffect.setDistance(1);
    shadowEffect.setUseGlobalLight(false);
    shadowEffect.setSize(2);
    shadowEffect.setAngle(45);
    shadowEffect.setSpread(50);
    shadowEffect.setNoise(5);
```
このブロックで **インナ―シャドウ** を適用し、外観をカスタマイズします。
- **Color** – 緑色に設定（任意の `Color` に変更可能）。  
- **Opacity** – 50 % の透明度（`255` 中 `128`）。  
- **Distance, Size, Angle** – 影のオフセットと拡がりを制御。  
- **Spread & Noise** – アーティスティックな変化を付加。

### Step 5: Save the modified PSD
```java
    image.save(destName, new PsdOptions(image));
```
`sample_out.psd` にインナ―シャドウ効果が適用された状態で保存されます。

### Step 6: Clean up resources
```java
} finally {
    image.dispose();
}
```
`image` オブジェクトを破棄してメモリを解放し、特に多数のファイルをループ処理する場合のリークを防止します。

## Common Use Cases
- **Automated branding pipelines** – ロゴに一貫したインナ―シャドウを追加して公開。  
- **Dynamic UI asset generation** – Web やモバイルアプリ向けに、ボタン状態などの深みをオンザフライで生成。  
- **Batch processing of legacy PSD libraries** – 古いデザインに最新の陰影を付与し、Photoshop を開かずにリファクタリング。

## Common Issues and Solutions
| 問題 | 発生原因 | 対策 |
|------|----------|------|
| `ArrayIndexOutOfBoundsException` on `getEffects()[0]` | 対象レイヤーにまだエフェクトが付いていません。 | キャストする前に、`layer.getBlendingOptions().addEffect(new ShadowEffect())` を使用して新しい `IShadowEffect` を追加します。 |
| Shadow color not changing | レイヤーに既に別のエフェクトタイプがあり、影を上書きしています。 | `layer.getBlendingOptions().clearEffects()` で既存のエフェクトをクリアするか、正しいエフェクトインデックスを編集していることを確認してください。 |
| File not saved | 保存先ディレクトリが存在しないか、書き込み権限がありません。 | 事前にディレクトリを作成（`new File(outputDir).mkdirs();`）するか、書き込み可能なパスを選択してください。 |

## Frequently Asked Questions

**Q: What is Aspose.PSD?**  
A: Aspose.PSD is a Java library for working with PSD files, allowing developers to manipulate layer effects, masks, and image properties programmatically.

**Q: Do I need Photoshop to use Aspose.PSD?**  
A: No, you do not need Photoshop to use Aspose.PSD. The library functions independently for PSD file manipulation.

**Q: Can I apply multiple effects to the same layer?**  
A: Absolutely! You can apply multiple effects by accessing each effect type similarly to how we accessed the inner shadow effect.

**Q: Is Aspose.PSD free?**  
A: Aspose.PSD is a commercial product; however, you can use a free trial available through Aspose.

**Q: Where can I find more documentation?**  
A: You can find comprehensive documentation for Aspose.PSD [here](https://reference.aspose.com/psd/java/).

## Conclusion
You’ve now seen how to **add inner shadow PSD** and **apply PSD layer effect** using Aspose.PSD for Java. This approach lets you automate sophisticated design tweaks, integrate them into backend services, or build batch processors for large image libraries. Feel free to experiment with other effect types—drop shadows, glows, bevels—to expand your toolkit.

---

**Last Updated:** 2026-02-14  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}