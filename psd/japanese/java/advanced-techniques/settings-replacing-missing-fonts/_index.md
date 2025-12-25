---
date: 2025-12-25
description: Aspose.PSD for Java を使用して PSD ファイルのフォントを置き換える方法を学びましょう – ステップバイステップのガイドで、PSD
  を PNG に保存する方法や欠落フォントの処理方法も示しています。
linktitle: Settings for Replacing Missing Fonts
second_title: Aspose.PSD Java API
title: Aspose.PSD for Javaでフォントを置き換える方法
url: /ja/java/advanced-techniques/settings-replacing-missing-fonts/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java でフォントを置き換える方法

## Introduction

Java アプリケーションで Photoshop（PSD）ファイルを扱う際、フォントが欠落しているとレイアウトが崩れ、描画エラーが発生します。**フォントを置き換える方法**を迅速かつ確実に行うことは、デザインの忠実性を保つために重要です。このチュートリアルでは、Aspose.PSD for Java を使用して欠落フォントを置き換え、結果を PNG に変換し、画像変換ワークフローをスムーズに保つ方法を学びます。最後まで読むと、画像内のフォントを置き換え、PSD を PNG として保存し、開発者が直面しがちな一般的な落とし穴を回避できるようになります。

## Quick Answers
- **「フォント置き換え」とは PSD 処理で何を意味しますか？** 欠落または利用できないフォントを、指定したフォールバックフォントに置き換えます。  
- **どのライブラリが自動的にこれを処理しますか？** Aspose.PSD for Java が `PsdLoadOptions.setDefaultReplacementFont` を提供しています。  
- **置き換え後に PSD を PNG に変換できますか？** はい – `PngOptions` を使用し、`psdImage.save` を呼び出します。  
- **本番環境で使用するにはライセンスが必要ですか？** 評価版以外のビルドでは有効な Aspose.PSD ライセンスが必要です。  
- **サポートされている Java バージョンは？** 現行の Aspose.PSD リリースは Java 8 以上のランタイムで動作します。

## What is Font Replacement in PSD Files?

PSD がホストマシンにインストールされていないフォントを参照している場合、レンダリングエンジンは汎用フォントにフォールバックし、テキストがずれることがあります。フォント置き換えを使用すると、欠落フォントが検出されたときにライブラリが使用するデフォルトフォント（例: Arial）を定義でき、視覚的な出力を一貫させることができます。

## Why Replace Missing Fonts with Aspose.PSD?

- **Zero‑dependency solution** – ネイティブ Photoshop や外部ツールは不要です。  
- **Batch‑ready** – 同じ設定で多数のファイルをループ処理できます。  
- **Image conversion ready** – 置き換え後に **PSD を PNG として保存** または **PSD から PNG へ変換** が余分な手順なしで可能です。  
- **Cross‑platform** – Windows、Linux、macOS の Java ランタイムで動作します。

## Prerequisites

1. **Aspose.PSD Library** – [releases page](https://releases.aspose.com/psd/java/) から Aspose.PSD for Java ライブラリをダウンロードしてインストールします。  
2. **Java Development Environment** – JDK 8 以上がインストールされ、設定されていることを確認してください。  

以上が準備できたら、コードに入りましょう。

## Import Packages

必要な Aspose.PSD クラスをインポートします。これにより、画像の読み込み、フォント置き換えオプション、PNG エクスポート機能が利用可能になります。

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## Step 1: Set Up Your Document Directory

ソース PSD が格納され、結果の PNG が保存されるフォルダーを定義します。

```java
String dataDir = "Your Document Directory";
```

## Step 2: Specify Source and Destination Files

入力 PSD と出力 PNG のフルパスを指定します。これによりワークフローが明確になり、コードの保守性が向上します。

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "result.png";
```

## Step 3: Configure Font Replacement Settings

`PsdLoadOptions` インスタンスを作成し、欠落フォントが見つかったときに Aspose.PSD が使用するフォントを指定します。この例では **Arial** を使用しますが、システムにインストールされている任意のフォントに置き換えることができます。

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setDefaultReplacementFont("Arial");
```

## Step 4: Load PSD Image and Replace Fonts

上記で定義したオプションを使用して PSD を読み込みます。ライブラリは自動的に欠落フォントを指定したデフォルトフォントに置き換えます。

```java
Image image = Image.load(sourceFile, loadOptions);
PsdImage psdImage = (PsdImage) image;
```

## Step 5: Save the Modified Image

PNG エクスポートオプション（アルファチャンネル付きの真カラー）を設定し、透過性を保持します。このステップは、フォント置き換え後の **PSD から PNG への画像変換** を実演します。

```java
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
psdImage.save(destName, options);
```

### What Just Happened?

- PSD がフォールバックフォント（Arial）で開かれました。  
- 元々欠落フォントを参照していたすべてのテキストレイヤーが Arial で描画されます。  
- 最終画像が PNG として保存され、視覚的忠実性を保ったまま **PSD を PNG として保存** できました。

## Common Issues & Troubleshooting

| Issue | Cause | Solution |
|-------|-------|----------|
| テキストがまだ崩れている | フォントメトリクスが異なる（サイズ、ウェイト） | プログラム上で置き換えフォントのサイズを調整するか、メトリクスが似たフォントを選択してください。 |
| PNG が予想より大きい | デフォルトの PNG オプションが 32‑bit カラーになっている | アルファが不要な場合は `PngColorType` を `Truecolor` に変更してください。 |
| ライセンス例外が発生 | 有効なライセンスなしで実行 | 画像を読み込む前に一時的または永続的な Aspose.PSD ライセンスを適用してください。 |

## Frequently Asked Questions

**Q: Aspose.PSD はすべての PSD ファイルバージョンに対応していますか？**  
A: Aspose.PSD は初期の Photoshop リリースから最新機能まで、幅広い PSD バージョンをサポートしています。

**Q: カスタムフォントを置き換えに使用できますか？**  
A: はい、`setDefaultReplacementFont` にカスタムフォント名を渡すだけです。フォントが JVM からアクセス可能であることを確認してください。

**Q: Aspose.PSD のライセンスオプションはありますか？**  
A: ニーズに合わせた最適なプランを選べるよう、[こちら](https://purchase.aspose.com/buy) でライセンスオプションをご確認ください。

**Q: Aspose.PSD のサポートフォーラムはありますか？**  
A: はい、[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34) でコミュニティサポートやディスカッションが行われています。

**Q: Aspose.PSD の一時ライセンスはどこで取得できますか？**  
A: テストや評価目的で使用できる一時ライセンスは [こちら](https://purchase.aspose.com/temporary-license/) から取得できます。

---

**Last Updated:** 2025-12-25  
**Tested With:** Aspose.PSD 24.11 for Java (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}