---
date: 2026-02-17
description: Aspose.PSD for Java を使用して PSD レイヤーを抽出し、PNG に変換する方法を学びましょう。堅牢なグラフィック操作が必要な開発者に最適です。
linktitle: Extract PSD Layers and Add Layer Support for PSD Files using Aspose.PSD
  Java
second_title: Aspose.PSD Java API
title: Aspose.PSD Java を使用して PSD ファイルのレイヤーを抽出し、レイヤーサポートを追加する
url: /ja/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD レイヤーの抽出と PSD ファイルのレイヤーサポートの追加（Aspose.PSD Java）

## Introduction
Photoshop Document（PSD）ファイルの取り扱いは、グラフィックデザイナーも開発者も日常的に行う作業です。最も一般的なタスクのひとつは **PSD レイヤーを抽出** して、編集・再利用・PNG など他の形式への変換を行うことです。Java アプリケーションでは、Aspose.PSD を使用すればこのプロセスがシンプルかつコードフレンドリーになります。本チュートリアルでは、PSD レイヤーの抽出、レイヤーサポートの有効化、そして **PSD レイヤーを PNG に変換** する手順を、分かりやすい解説と実践的なヒントとともに紹介します。

## Quick Answers
- **「PSD レイヤーを抽出する」とは何ですか？** PSD ファイルを読み込み、個々のレイヤーにアクセスして操作またはエクスポートできるようにすることです。  
- **Java でこれを扱うライブラリはどれですか？** Aspose.PSD for Java が Photoshop を必要とせずにフル機能の PSD 処理を提供します。  
- **PSD レイヤーを一括で PNG に変換できますか？** はい。適切なオプションでファイルを読み込み、透明度を保持した PNG オプションで保存すれば可能です。  
- **本番環境で使用するにはライセンスが必要ですか？** 商用利用には商用ライセンスが必要です。評価用の無料トライアルが利用可能です。  
- **必要な Java バージョンは？** JDK 8 以上（本チュートリアルは JDK 11 を例に使用）。

## How to extract PSD layers using Aspose.PSD for Java
以下に、環境構築から最終的な PNG の保存までをカバーしたステップバイステップガイドを示します。各番号付きステップに従えば、数分で動作するソリューションが完成します。

## Why extract PSD layers and convert them to PNG?
- **アセットの再利用:** マスタ PSD からアイコンやボタン、UI 要素を手動でエクスポートせずに取得できます。  
- **自動化:** サムネイルや Web 用画像をその場で生成できます。  
- **透明度の保持:** PNG はアルファチャンネルを保持するため、Web グラフィックに最適です。  
- **クロスプラットフォーム:** サーバ上に Photoshop が不要です。Aspose.PSD は Java が動く環境ならどこでも動作します。

## Prerequisites
作業を始める前に、以下を用意してください。

1. **Java 開発環境** – JDK がインストールされていること。[Oracle のウェブサイト](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)からダウンロードできます。  
2. **Aspose.PSD for Java** – 公式ダウンロードページ [here](https://releases.aspose.com/psd/java/) から最新ライブラリを取得してください。  
3. **基本的な Java 知識** – Java プログラムのコンパイルと実行に慣れていること。  
4. **IDE** – IntelliJ IDEA、Eclipse、またはお好みのエディタ。  
5. **PSD ファイル** – 任意の PSD を使用するか、テスト用にサンプル PSD をダウンロードしてください。

これらが揃ったら、PSD レイヤーの抽出を開始できます。

## Import Packages
まず、Aspose.PSD ライブラリから必要なクラスをインポートします。

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## Step 1: Define Your Directories
ソース PSD と出力 PNG のパスを設定します。`dataDir` を実際のフォルダに合わせて変更してください。

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "layers.psd";
String output = dataDir + "layers.png";
```

- `dataDir` – `"Your Document Directory"` を実際のフォルダパスに置き換えます。  
- `sourceFileName` – 処理したい PSD のフルパス。  
- `output` – 抽出したレイヤーを含む PNG の保存先パス。

## Step 2: Set Up the Load Options
`PsdLoadOptions` を設定すると、レイヤー効果やリソースが正しく読み込まれ、**PSD レイヤーを抽出** する際に必須です。

```java
PsdLoadOptions imageLoadOptions = new PsdLoadOptions();
imageLoadOptions.setLoadEffectsResource(true);
imageLoadOptions.setUseDiskForLoadEffectsResource(true);
```

- `setLoadEffectsResource(true)` – レイヤーに付随するドロップシャドウなどの追加効果を読み込みます。  
- `setUseDiskForLoadEffectsResource(true)` – 重いリソースをディスクにオフロードし、メモリ使用量を抑えます。

## Step 3: Load the PSD File
先ほど設定したオプションを使って、PSD を `PsdImage` オブジェクトに読み込みます。

```java
PsdImage image = (PsdImage) Image.load(sourceFileName, imageLoadOptions);
```

この時点で `image` にはすべてのレイヤー、マスク、エフェクトが含まれ、抽出の準備が整っています。

## Step 4: Set Up the Save Options
PNG の保存方法を設定します。`TruecolorWithAlpha` を使用すると、元レイヤーの透明度が保持されます。

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

## Step 5: Save the Image (Convert PSD Layers to PNG)
読み込んだ PSD（すべてのレイヤーを含む）を単一の PNG ファイルにエクスポートします。この操作で **convert psd layers png** が一度に実行されます。

```java
image.save(output, saveOptions);
```

各レイヤーを個別の PNG にしたい場合は `image.getLayers()` をイテレートすれば可能ですが、多くのユースケースではマージされた PNG で十分です。

## Step 6: Wrap It Up
処理が正常に完了したことを示すコンソールメッセージを追加します。

```java
System.out.println("PSD Layers have been successfully converted to PNG!");
```

## Common Issues & Tips
- **Out‑of‑Memory エラー:** 非常に大きな PSD を処理する場合は `setUseDiskForLoadEffectsResource(true)` を有効にして一時データをディスクにオフロードしてください。  
- **エフェクトが欠落:** `setLoadEffectsResource(true)` が設定されていることを確認してください。設定しないと一部のレイヤー効果が無視されます。  
- **パスの問題:** `java.nio.file` の `Paths.get(...)` を使用すると、プラットフォームに依存しないパス処理が可能です。

## Frequently Asked Questions

**Q: Aspose.PSD for Java とは何ですか？**  
A: Aspose.PSD for Java は、Photoshop をインストールせずに PSD ファイルを操作できるライブラリです。

**Q: 他のファイル形式にも Aspose.PSD を使えますか？**  
A: はい。主に PSD 用ですが、Aspose は他のさまざまな形式向けのライブラリも提供しています。

**Q: トライアル版はありますか？**  
A: もちろんです！無料トライアル版は [here](https://releases.aspose.com/) からダウンロードできます。

**Q: サポートはどこで受けられますか？**  
A: Aspose フォーラムの [here](https://forum.aspose.com/c/psd/34) でサポートを受けられます。

**Q: PNG から PSD に戻すことはできますか？**  
A: Aspose.PSD ライブラリは PSD の読み取りと操作に重点を置いており、他形式から PSD への変換は主な機能ではありません。

**Q: 各レイヤーを個別の PNG に抽出するには？**  
A: `image.getLayers()` をイテレートし、各レイヤー用に新しい `Bitmap` を作成して `PngOptions` で保存します。これによりレイヤーごとの PNG が生成されます。

## Conclusion
これで **PSD レイヤーを抽出** し、フルレイヤーサポートを有効にし、**PSD レイヤーを PNG に変換** する方法を Aspose.PSD for Java を使って習得できました。自動化されたアセットパイプラインの構築やデスクトップアプリへのグラフィック機能追加など、Photoshop が不要な環境でも細かい制御が可能です。ぜひ、フィルタ適用やレイヤーのプログラム的なマージ、個別レイヤーのエクスポートなど、さらに踏み込んだ活用を試してみてください。

---

**Last Updated:** 2026-02-17  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}