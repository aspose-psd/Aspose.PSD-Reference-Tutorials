---
date: 2026-11-04
description: Aspose.PSD for Java を使用して invert adjustment layer を適用し、PSD 画像をバッチ処理し、ネガティブ画像の
  PSD ファイルを作成する方法を学びます。
keywords:
- how to use aspose
- batch process psd images
- create negative image psd
- image processing java library
- apply multiple adjustment layers
lastmod: 2026-11-04
linktitle: Invert Adjustment Layer
og_description: Aspose.PSD for Java を使用して invert adjustment layer を追加し、PSD 画像をバッチ処理し、ネガティブ画像の
  PSD を作成する方法。ステップバイステップのガイドに従ってください。
og_image_alt: Screenshot showing Aspose.PSD Java code adding an invert adjustment
  layer
og_title: JavaでAspose.PSDを使用して invert adjustment layer を追加する方法
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to use Aspose.PSD for Java to apply an invert adjustment
    layer, batch process PSD images, and create negative image PSD files.
  headline: How to use Aspose.PSD to add an invert adjustment layer in Java
  type: TechArticle
- questions:
  - answer: Yes, it supports Java 6.0 and later, including Java 8, 11, and 17.
    question: Is Aspose.PSD compatible with all Java versions?
  - answer: Absolutely. After adding the invert layer you can call `addBrightnessAdjustmentLayer()`,
      `addHueSaturationAdjustmentLayer()`, etc., to stack effects.
    question: Can I apply multiple adjustment layers in a single operation?
  - answer: The complete documentation is available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find the full API reference?
  - answer: Yes, you can download a trial version [Aspose.PSD trial download](https://releases.aspose.com/).
    question: Is there a free trial for Aspose.PSD?
  - answer: Request a temporary license [temporary license request page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for testing?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- aspose psd
- java image processing
- invert adjustment layer
- batch psd processing
title: JavaでAspose.PSDを使用して invert adjustment layer を追加する方法
url: /ja/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# JavaでAspose.PSDを使用してインバート調整レイヤーを追加する方法

## はじめに

堅牢な **image processing java library** をお探しなら、Aspose.PSD for Java は市場で最も汎用性の高いオプションの一つです。このチュートリアルでは **how to use Aspose** を使って PSD ファイルに **Invert Adjustment Layer** を挿入し、他の調整レイヤーとスタックし、さらには数十ファイルにわたって操作を実行する方法を示します。バッチ処理ツール、サーバーサイドの画像サービス、あるいは単一画像エディタを構築する場合でも、以下の手順でソース PSD から数分で完全に編集可能なネガティブ画像へと変換できます。

## クイック回答

- **Invert Adjustment Layer は何をしますか？** 選択領域内のすべての RGB 値を反転させ、画像を写真のネガティブに変換します。  
- **どのライブラリがこの機能を提供しますか？** Aspose.PSD、業界トップクラスの **image processing java library** です。  
- **他の調整とスタックできますか？** はい – **apply multiple adjustment layers** など、Brightness/Contrast、Hue/Saturation などを追加できます。  
- **開発にライセンスは必要ですか？** 無料トライアルが利用可能です。製品版の使用にはライセンスが必要です。  
- **実装にどれくらい時間がかかりますか？** 基本的なケースでは通常 10 分未満です。

## Invert Adjustment Layer とは何ですか？

Invert Adjustment Layer は、影響を受けたすべてのピクセルのカラー値を反転させる非破壊編集です。レイヤースタックの最上位に配置されるため、可視性を切り替えたり順序を変更したりしても、元の画像データを永続的に変更することはありません。これは **create negative image PSD** ファイルを作成したり、クラシックなフィルムネガティブの外観を実現する最も簡単な方法です。

## なぜ Aspose.PSD を image processing java library として使用するのですか？

Aspose.PSD は **200+ PSD features** をサポートし、Photoshop を必要とせずに Photoshop ファイルの読み書きが可能で、500 MB 未満のヒープメモリで数百ページのドキュメントを処理します。Java 6 以降の任意の Java ランタイム上で動作するため、Windows、Linux、macOS サーバー上で **batch process psd images** を行うのに最適です。

## 前提条件

1. **Aspose.PSD for Java** – 公式サイトの [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/) から最新の JAR をダウンロードしてください。  
2. **Java Development Kit** – JDK 6.0 以降がインストールされ、`PATH` に設定されていることを確認してください。

これでコードを書く準備が整いました。

## パッケージのインポート

`PsdImage` クラスはメモリ内の Photoshop ドキュメント全体を表し、調整レイヤークラスは `com.aspose.psd.layers.adjustments` パッケージにあります。

`PsdImage` クラスは PSD ファイルの構造とピクセルデータをカプセル化する Aspose.PSD の最上位オブジェクトです。名前空間をインポートすれば、PSD ファイルの読み込み、編集、保存が可能になります。

## ステップ 1: ドキュメントディレクトリの設定

ソース PSD ファイルが格納され、出力が保存されるフォルダーを定義します。絶対パスを使用することで、作業ディレクトリが変わった際の `NullPointerException` を防げます。

## ステップ 2: PSD ファイルの読み込み

`PsdImage` オブジェクトにソースファイルをロードします。このオブジェクトはメモリ内に完全なレイヤーヒエラルキーを保持し、非破壊編集を可能にします。

`PsdImage` クラスは静的な `load` メソッドを提供し、ファイルヘッダーを読み取り、形式を検証し、操作可能なインメモリ表現を構築します。

## ステップ 3: インバート調整レイヤーの追加

組み込みメソッドを呼び出して、現在のレイヤースタックの最上位に Invert Adjustment Layer を挿入します。その後、さらにレイヤー（例: Brightness、Hue）を追加して、単一のワークフローで **apply multiple adjustment layers** が可能です。

`addInvertAdjustmentLayer()` は PSD のレイヤーコレクションに Invert Adjustment Layer を追加します。

## ステップ 4: 出力の保存

変更された PSD をディスクに永続化します。  

`save()` はすべてのレイヤーとメタデータを含む PSD ファイルを指定されたパスに書き込みます。

保存は同じ `save` メソッドを使用し、すべての調整レイヤー、マスク、メタデータを含む完全なドキュメントを指定された形式で書き出します。

### 何が起こったのか？

PSD ファイルは `PsdImage` オブジェクトにロードされ、`InvertAdjustmentLayer` が作成されて最上位レイヤーとして追加され、ドキュメントが保存されました。この手順により、元の画像データは保持されたまま、後で切り替えや順序変更が可能な非破壊的なインバート効果が追加されます。

これで、**image processing java library** である Aspose.PSD を使用して PSD ファイルを操作することに成功しました。

## インバート調整で PSD 画像をバッチ処理する方法は？

`for` ループ内で各ファイルをロードし、同じ手順を適用して各イテレーションで `save` を呼び出します。Aspose.PSD はストリーミング方式でファイルを処理するため、同じ `PsdImage` インスタンスを再利用することでメモリ使用量を 300 MB 未満に抑えながら **hundreds of PSDs** を処理できます。

## PSD をネガティブ画像に変換する方法は？

Invert Adjustment Layer を最上位アイテムとして追加し、ドキュメントを保存します。この操作は **convert PSD to negative** と同等です。後でレイヤーを無効化または削除すれば、ソースファイルを再読み込みせずに元の外観に戻すことができます。

## よくある問題とヒント

| 問題 | 原因 | 解決策 |
|-------|-------|----------|
| **NullPointerException on `Image.load`** | ファイルパスが間違っているか、ファイルが存在しません | `dataDir` とファイル名を確認し、テスト時は絶対パスを使用してください |
| **レイヤー順序が期待通りでない** | 既存レイヤーの後にレイヤーを追加するとスタック順序が変わります | インバートレイヤーを他の調整より前に挿入するか、`psdImage.getLayers().move()` で順序を変更してください |
| **大きな PSD でのパフォーマンス低下** | 非常に大きなファイルをメモリにロードするため | JVM ヒープを増やす（`-Xmx2g`）か、`psdImage.getPages().get(0).getResources().setMemoryOptimized(true)` を使用してファイルをチャンク処理してください |

## よくある質問

**Q: Aspose.PSD はすべての Java バージョンと互換性がありますか？**  
A: はい、Java 6.0 以降（Java 8、11、17 を含む）をサポートしています。

**Q: 単一の操作で複数の調整レイヤーを適用できますか？**  
A: もちろんです。インバートレイヤーを追加した後、`addBrightnessAdjustmentLayer()`、`addHueSaturationAdjustmentLayer()` などを呼び出して効果をスタックできます。

**Q: 完全な API リファレンスはどこで見つけられますか？**  
A: 完全なドキュメントは [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/) で入手可能です。

**Q: Aspose.PSD の無料トライアルはありますか？**  
A: はい、トライアル版は [Aspose.PSD trial download](https://releases.aspose.com/) からダウンロードできます。

**Q: テスト用の一時ライセンスはどう取得できますか？**  
A: 一時ライセンスは [temporary license request page](https://purchase.aspose.com/temporary-license/) でリクエストしてください。

---

**最終更新日:** 2026-11-04  
**テスト環境:** Aspose.PSD 24.12 for Java  
**作者:** Aspose  

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

```java
String dataDir = "Your Document Directory";
```

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

```java
im.addInvertAdjustmentLayer();
```

```java
im.save(outputPath);
```

## 関連チュートリアル

- [Aspose.PSD for Java を使用して PSD ファイルにレベル調整レイヤーを追加する](/psd/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/)
- [PSD に調整レイヤー – チャネルミキサーを追加する方法 (Java)](/psd/java/modifying-converting-psd-images/add-channel-mixer-adjustment-layer-psd/)
- [PSD を編集する - Java でカーブ調整レイヤーを追加する](/psd/java/modifying-converting-psd-images/add-curves-adjustment-layer-psd/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}