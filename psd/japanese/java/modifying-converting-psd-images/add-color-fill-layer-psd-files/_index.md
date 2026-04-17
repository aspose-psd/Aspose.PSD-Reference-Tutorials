---
date: 2026-03-02
description: Java と Aspose.PSD を使用して PSD ファイルにカラー塗りつぶしレイヤーを作成し、塗りつぶしを追加する方法を学びましょう。ステップバイステップのガイドに従って、塗りつぶしレイヤーの色をすばやく設定できます。
linktitle: Add Color Fill Layer to PSD Files using Java
second_title: Aspose.PSD Java API
title: フィルの追加方法：JavaでPSDファイルにカラー塗りつぶしレイヤーを追加する
url: /ja/java/modifying-converting-psd-images/add-color-fill-layer-psd-files/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java を使用して PSD ファイルにカラー フィル レイヤーを追加する

## Introduction
Photoshop ファイルをプログラムで操作し、デザインに色を加えたいことはありませんか？ **PSD にフィルを追加する方法** を知りたいなら、ここが最適です。このチュートリアルでは、Java と Aspose.PSD ライブラリを使用して PSD（Photoshop Document）ファイルにカラー フィル レイヤーを追加する手順を解説します。PSD をデジタル キャンバスと考えてください――数行のコードでカラー フィル レイヤーの作成、色の設定、ファイルの保存ができるようになります。

## Quick Answers
- **What library is needed?** Aspose.PSD for Java  
- **Primary use case?** Programmatically add or change PSD fill colors  
- **How long does implementation take?** About 10‑15 minutes for a basic scenario  
- **Do I need a license?** A free trial works for evaluation; a commercial license is required for production  
- **Supported Java version?** Java 8 and above  

## What is a Color Fill Layer?
カラー フィル レイヤーは、Photoshop ドキュメント内の他のレイヤーの上に配置される単色のオーバーレイです。背景色の追加、マスクの作成、個々のピクセルを編集せずにデザインのビジュアルテーマを素早く変更する際に使用されます。

## Why add a color fill layer with code?
- **Automation:** 多数のファイルに対して一貫したブランディング資産を自動生成。  
- **Batch processing:** 手作業ではなく、数秒で数十個の PSD を更新。  
- **Dynamic designs:** ユーザー入力やデータ ソースに応じて、リアルタイムに色を変更。

## Prerequisites
コードに入る前に、以下が揃っていることを確認してください。

1. **Java Development Kit (JDK)** – JDK 8 以上がインストール済み。  
2. **Aspose.PSD Library** – 最新の JAR を [Aspose Releases page](https://releases.aspose.com/psd/java/) からダウンロード。  
3. **IDE** – IntelliJ IDEA、Eclipse、NetBeans、またはお好みのエディタ。  
4. **Basic Java knowledge** – オブジェクト、ループ、例外処理に慣れていること。

## Import Packages
基本が整ったので、必要なクラスをインポートします。これらのインポートにより、PSD の操作とフィル レイヤーの操作が可能になります。

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IColorFillSettings;
```

## How to Add Fill – Step‑by‑Step Guide

### Step 1: Set Up Your Environment
ソース PSD の場所と、編集後のファイルを保存する場所を定義し、ドキュメントをロードします。

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ColorFillLayer.psd";
String exportPath     = dataDir + "ColorFillLayer_output.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- `dataDir` は PSD が格納されているフォルダーを指します。  
- `sourceFileName` は変更対象の元ファイルです。  
- `exportPath` は **add color fill layer** が適用された新しいファイルを書き出す場所です。  

### Step 2: Loop Through the Layers
既存のフィル レイヤーを検索し、必要に応じて変更または新規作成します。

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof FillLayer) {
        FillLayer fillLayer = (FillLayer) im.getLayers()[i];
```

- `for` ループは PSD 内のすべてのレイヤーを走査します。  
- `instanceof FillLayer` のチェックにより、フィル レイヤーのみを対象にします。

### Step 3: Verify the Fill Type
対象レイヤーが **color fill layer** であることを確認してから、色の変更を行います。

```java
if (fillLayer.getFillSettings().getFillType() != FillType.Color) {
    throw new Exception("Wrong Fill Layer");
}
```

フィル タイプが `FillType.Color` でない場合は、中止してグラデーションやパターン フィルの誤変更を防ぎます。

### Step 4: Set the Fill Color
ここで **set fill layer color** を実行します。例ではレイヤーを赤に変更していますが、`Color.getRed()` を `Color.getBlue()` や `new Color(255, 165, 0)`（オレンジ）など、必要な任意の `Color` に置き換えて構いません。

```java
IColorFillSettings settings = (IColorFillSettings) fillLayer.getFillSettings();
settings.setColor(Color.getRed());
fillLayer.update();
```

- `settings.setColor(...)` が実際のフィル色を変更します。  
- `fillLayer.update()` がレイヤーを更新し、新しい色を適用します。  

### Step 5: Save the Changes
最後に、変更された PSD をディスクに書き出します。

```java
im.save(exportPath);
break;
```

- `break` により、最初に見つかった該当フィル レイヤーの更新後にループを終了します。これは **change PSD fill color** を一度だけ行う場合に一般的な動作です。

## Common Issues & Tips
- **No FillLayer found:** PSD にフィル レイヤーが無い場合は、`new FillLayer(im)` で作成し、`im.getLayers()` に追加してください。  
- **Color not updating:** 色設定後に必ず `fillLayer.update()` を呼び出すことを確認してください。  
- **File not saved:** `exportPath` が書き込み可能なディレクトリを指しているか、書き込み権限があるかを確認してください。  

## Frequently Asked Questions

**Q: What is Aspose.PSD?**  
A: Aspose.PSD は、Adobe Photoshop を必要とせずに Photoshop PSD ファイルの作成、編集、変換を可能にする強力な Java ライブラリです。

**Q: Can I use Aspose.PSD for free?**  
A: Yes, a free trial is available on the [Aspose Releases page](https://releases.aspose.com/).  

**Q: Which file formats can I work with besides PSD?**  
A: Aspose.PSD supports PSD, PSB, BMP, JPEG, PNG, GIF, TIFF, and more.

**Q: How do I get support if I run into problems?**  
A: You can ask questions on the [Aspose Support Forum](https://forum.aspose.com/c/psd/34).  

**Q: Where can I purchase a full license?**  
A: Licenses are sold through the [Aspose Purchase page](https://purchase.aspose.com/buy).

## Conclusion
Java でプログラム的に Photoshop ドキュメントに **fill を追加する方法** が分かりました。カラー フィル レイヤーを作成または取得し、色を設定して結果を保存するだけで、繰り返しのデザイン作業を自動化したり、動的なアセットを生成したり、PSD 操作を大規模な Java アプリケーションに組み込むことができます。ぜひ試してみてください――異なる色で実験したり、複数のフィル レイヤーを追加したり、他の Aspose.PSD 機能と組み合わせて強力な画像処理パイプラインを構築してみましょう。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-03-02  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

---