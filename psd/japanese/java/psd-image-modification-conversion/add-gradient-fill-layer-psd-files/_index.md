---
date: 2026-03-23
description: Aspose.PSD を使用して Java でグラデーション塗りつぶしの PSD ファイルを作成する方法を学びましょう。このガイドでは、PSD
  のグラデーションレイヤーを編集し、色や透明度、その他のプロパティをプログラムで調整する方法を示します。
linktitle: Create Gradient Fill PSD with Java – Add Gradient Fill Layer
second_title: Aspose.PSD Java API
title: Javaでグラデーション塗りつぶしPSDを作成 – グラデーション塗りつぶしレイヤーを追加
url: /ja/java/psd-image-modification-conversion/add-gradient-fill-layer-psd-files/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# JavaでPSDファイルにグラデーション塗りつぶしレイヤーを追加する

## Introduction

PSDファイルにさらにビジュアルマジックを加えたいと考えたことはありませんか？ **Javaでグラデーション塗りつぶしPSDを作成する方法** を探している方へ。グラデーションはデザインに奥行きを与えますが、手動で調整するのは手間がかかります。**Aspose.PSD for Java** を使えば、プログラムでPSDのグラデーションを編集し、色や透明度を変更し、あらゆるプロパティを微調整できるため、時間を節約し、数十ファイルにわたって一貫性を保てます。

## Quick Answers
- **JavaでPSDのグラデーションを編集できるライブラリは？** Aspose.PSD for Java。  
- **PSDファイルを読み込むメソッドは？** `Image.load(path)`。  
- **グラデーションの角度を変更するには？** `settings.setAngle(double)`。  
- **新しいカラーポイントを追加できますか？** はい—`GradientColorPoint` オブジェクトを作成し、カラーポイントリストに追加します。  
- **本番環境で使用するにはライセンスが必要ですか？** 商用ライセンスが必要です。評価用の無料トライアルがあります。

## “create gradient fill PSD” とは？
グラデーション塗りつぶしPSDを作成するとは、Photoshopドキュメント内にグラデーションベースの塗りつぶしレイヤーをプログラムで挿入または変更することを指します。これにより、Photoshopを開かずに自動スタイリング、バッチ処理、動的画像生成が可能になります。

## Aspose.PSDでPSDグラデーションを編集するメリット
- **完全な .PSD サポート** – スマートオブジェクトを含むすべてのレイヤータイプに対応。  
- **Photoshop不要** – 任意のサーバーやCIパイプラインで実行可能。  
- **細かな制御** – 角度、オフセット、ディザリング、カラーポイント、透明度ポイントをクリーンなJava APIで調整可能。  

## Prerequisites

作業を始める前に、以下を準備してください。

- Java Development Kit (JDK): 安定版のJDKが必要です。Oracle のウェブサイトからダウンロードできます: [Link to Oracle JDK download page]
- Aspose.PSD for Java: Java アプリケーションで PSD ファイルを扱うための強力なライブラリです。Aspose のサイトからダウンロードしてください: [Link to Aspose.PSD for Java download]（無料トライアルあり）

## Import Packages

PSD ファイルを操作するために必要な Aspose.PSD パッケージをインポートします:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.imageoptions.PsdOptions;
import java.util.ArrayList;
import java.util.Collections;
import java.util.List;
```

これらのインポートにより、PSD の読み込み、操作、保存に必要なクラスとメソッドが利用可能になります。

さあ、グラデーション塗りつぶしレイヤーの変更というエキサイティングな旅に出発しましょう！

## How to Create Gradient Fill PSD with Java

### Step 1: Load the PSD File

まず、変更したいグラデーション塗りつぶしレイヤーが含まれる PSD ファイルを読み込みます。`Image.load` メソッドにファイルパスを指定してください:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ComplexGradientFillLayer.psd";
String outputFile = dataDir + "ComplexGradientFillLayer_output.psd";
PsdImage image = (PsdImage)Image.load(sourceFileName);
```

このコードは指定ディレクトリから PSD を読み込み、`image` 変数に格納します。

### Step 2: Identify the Gradient Fill Layer

PSD には多数のレイヤーが存在します。対象となるグラデーション塗りつぶしレイヤーを特定する必要があります。`image.getLayers()` 配列を走査して目的のレイヤーを探します:

```java
for (int i = 0; i < image.getLayers().length; i++) {
if (image.getLayers()[i] instanceof FillLayer) {
   FillLayer fillLayer = (FillLayer) image.getLayers()[i];
   // Further checks and modifications will happen here
   break;
}
}
```

このループは各レイヤーをチェックします。レイヤーが `FillLayer` の場合は `FillLayer` 型にキャストされ、`fillLayer` 変数に保存され、以降の処理に使用できます。レイヤー名など、特定の条件で絞り込みたい場合はループ内に追加チェックを入れてください。

### Step 3: Verify Gradient Fill Type

すべての塗りつぶしレイヤーがグラデーションを使用しているわけではありません。このコードは、特定したレイヤーが実際にグラデーション塗りつぶしかどうかを確認します:

```java
if (fillLayer.getFillSettings().getFillType() != FillType.Gradient) {
   throw new Exception("Wrong Fill Layer");
}
```

`getFillType` が `FillType.Gradient` を返さない場合は例外がスローされ、誤ったレイヤーを操作しようとしていることを示します。

## How to Edit PSD Gradient Using Aspose.PSD

### Step 4: Access and Modify Gradient Properties

ここが本番です！Aspose.PSD は `IGradientFillSettings` インターフェイスを通じてさまざまなグラデーション塗りつぶしプロパティへのアクセスを提供します。必要に応じて取得・変更できます:

```java
IGradientFillSettings settings = (IGradientFillSettings) fillLayer.getFillSettings();

// Modify properties (replace with desired values)
settings.setAngle(0.0);  // Set angle to 0 degrees
settings.setDither(false);  // Disable dithering
settings.setAlignWithLayer(true); // Align gradient with layer
settings.setReverse(true);  // Reverse gradient direction
settings.setHorizontalOffset(25);  // Set horizontal offset
settings.setVerticalOffset(-15);  // Set vertical offset
```

このコードは `IGradientFillSettings` オブジェクトを取得し、角度、ディザリング、配置、オフセットなどのプロパティを変更します。提供された値はご自身の目的に合わせて置き換えて、望むグラデーション効果を実現してください。

### Step 5: Manipulate Color and Transparency Points

グラデーションはスペクトル上のカラーポイントと透明度ポイントで構成されます。Aspose.PSD を使えば、これらのポイントを細かく制御できます:

```java
List<IGradientColorPoint> colorPoints = new ArrayList<IGradientColorPoint>();
Collections.addAll(colorPoints, settings.getColorPoints());
List<IGradientTransparencyPoint> transparencyPoints = new ArrayList<IGradientTransparencyPoint>();
Collections.addAll(transparencyPoints, settings.getTransparencyPoints());

// Add a new color point
GradientColorPoint gr1 = new GradientColorPoint();
gr1.setColor(Color.getViolet());
gr1.setLocation(4096);
gr1.setMedianPointLocation(75);
colorPoints.add(gr1);

// Modify an existing color point
colorPoints.get(1).setLocation(3000);

// Add a new transparency point
GradientTransparencyPoint gr2 = new GradientTransparencyPoint();
gr2.setOpacity(80.0);
gr2.setLocation(4096);
gr2.setMedianPointLocation(25);
transparencyPoints.add(gr2);

// Modify an existing transparency point
transparencyPoints.get(2).setLocation(3000);

settings.setColorPoints(colorPoints.toArray(new IGradientColorPoint[0]));
settings.setTransparencyPoints(transparencyPoints.toArray(new IGradientTransparencyPoint[0]));
```

### Step 6: Update and Save the PSD File

必要な変更が完了したら、塗りつぶしレイヤーを更新し、PSD ファイルを保存します:

```java
fillLayer.update();
image.save(outputFile, new PsdOptions(image));
```

`fillLayer.update()` メソッドがグラデーション塗りつぶしレイヤーに変更を適用し、`image.save` が指定した出力パスに修正済み PSD を保存します。

## Common Issues and Solutions

- **例外 “Wrong Fill Layer”** – 実際にグラデーションを使用している `FillLayer` を対象にしているか確認してください。レイヤー名やインデックスで事前にチェックすると安全です。  
- **カラー ポイントが反映されない** – ポイントリストを変更した後は必ず `settings.setColorPoints(...)` と `settings.setTransparencyPoints(...)` を呼び出して、レイヤーに更新をプッシュしてください。  
- **大容量 PSD のパフォーマンス** – 多数のファイルを処理する場合は同じ `PsdOptions` インスタンスを再利用し、`image.dispose()` で画像を速やかに解放してメモリを確保しましょう。

## Frequently Asked Questions

**Q: グラデーションに複数のカラー・透明度ポイントを追加できますか？**  
A: もちろんです！必要なだけポイントを作成し、各リストに追加すれば、希望のグラデーション効果を実現できます。

**Q: グラデーションからカラーまたは透明度ポイントを削除するには？**  
A: リストの `remove` メソッド、例 `colorPoints.remove(index)` を使用して不要なポイントを削除し、`setColorPoints` で再設定してください。

**Q: グラデーションの種類（線形、放射状など）を変更できますか？**  
A: 現在 Aspose.PSD は線形グラデーションをサポートしています。将来的なリリースで他のタイプが追加される可能性がありますが、カラー・透明度ポイントを操作することで類似の効果はシミュレート可能です。

**Q: グラデーション編集によるパフォーマンスへの影響は？**  
A: 影響はグラデーションの複雑さと変更回数に依存します。一般的なユースケースではオーバーヘッドは最小ですが、大量のファイルをバッチ処理する場合はメモリ管理の最適化が有効です。

**Q: PSD 内の複数のグラデーション塗りつぶしレイヤーに同じ手法を適用できますか？**  
A: はい。`image.getLayers()` を走査し、各 `FillLayer` の `FillType` が `Gradient` であるか確認して、同様の変更を適用してください。

**Q: 本番環境で使用するには商用ライセンスが必要ですか？**  
A: 本番デプロイには有効な Aspose.PSD ライセンスが必要です。評価用の無料トライアルも用意されています。

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**Last Updated:** 2026-03-23  
**Tested With:** Aspose.PSD for Java 24.11 (latest)  
**Author:** Aspose