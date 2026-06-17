---
date: 2026-03-21
description: Aspose.PSD for Java を使用して PSD 画像を作成する際に、ICC プロファイルでカラープロファイルを変換し、ICC
  プロファイル設定を適用し、RGB プロファイルを設定する方法を学びましょう。
linktitle: Color Conversion using ICC Profiles
second_title: Aspose.PSD Java API
title: Aspose.PSDでのカラー変換にICCプロファイルを使用する方法
url: /ja/java/psd-conversion/color-conversion-icc-profiles/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD で ICC プロファイルを使用したカラー変換の方法

## Introduction
デバイス間で正確な色を保証するために **ICC プロファイルの使用方法** をお探しなら、ここが適切な場所です。このチュートリアルでは、カラー プロファイルの変換、ICC プロファイルの適用、そして **PSD 画像の作成** 時に RGB プロファイルを設定する手順を解説します。バッチ処理パイプラインを構築する場合でも、単一画像エディタを作成する場合でも、以下の手順で実用的な基盤を構築できます。

## Quick Answers
- **ICC プロファイルの主な目的は何ですか？** 特定のデバイスまたはカラースペースで色をどのように解釈すべきかを定義します。  
- **Aspose.PSD で PSD 画像を表すクラスはどれですか？** `PsdImage`。  
- **RGB と CMYK の両方のプロファイルを変更できますか？** はい。`setRgbColorProfile` と `setCmykColorProfile` を使用します。  
- **開発にライセンスは必要ですか？** テストには無料トライアルで動作しますが、本番環境ではライセンスが必要です。  
- **YCCK をサポートする出力形式は何ですか？** `JpegCompressionColorMode.Ycck` を使用した JPEG。

## ICC カラー変換とは何ですか？
ICC（International Color Consortium）プロファイルは、デバイス（モニター、プリンター、スキャナー）の色特性を記述した標準化されたデータセットです。**カラー プロファイルを変換**することで、画像が **画像が表示される場所** に関係なく視覚的な外観が一貫していることを保証します。

## Aspose.PSD で ICC プロファイルを使用する理由は？
- **正確な色再現** – ブランドや印刷ワークフローに不可欠です。  
- **クロスプラットフォームの一貫性** – 同じ画像が Windows、macOS、モバイルで同様に表示されます。  
- **組み込み API のサポート** – Aspose.PSD を使用すると、数行の Java で **icc プロファイルを適用** および **rgb プロファイルを設定** できます。

## Prerequisites
開始する前に、以下が揃っていることを確認してください：

1. **Aspose.PSD for Java** – 最新のライブラリは [releases](https://releases.aspose.com/psd/java/) ページからダウンロードしてください。  
2. **Java 開発環境** – JDK 8 以上とお好みの IDE。  
3. **ICC プロファイル** – この例では `eciRGB_v2.icc`（RGB）と `ISOcoated_v2_FullGamut4.icc`（CMYK）を使用します。信頼できるカラーマネジメントソースから取得できます。

## Import Packages
プロジェクトに必要な Aspose.PSD 名前空間を追加します。これらのインポートにより、画像処理、JPEG オプション、ストリーム ソースにアクセスできます。

```java
import com.aspose.psd.Color;
import com.aspose.psd.fileformats.jpeg.JpegCompressionColorMode;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.JpegOptions;
import com.aspose.psd.sources.StreamSource;
import java.io.File;
import java.io.FileInputStream;
import java.io.FileNotFoundException;
```

## How to Use ICC Profiles for Color Conversion
以下は、ICC プロファイルを使用して **カラーを変換** しながら **PSD 画像を作成** する手順を示すステップバイステップガイドです。

### Step 1: Create a New Image (Create PSD Image)
ステップ 1: 新しい画像を作成 (PSD 画像の作成)  
まず、空の `PsdImage` をインスタンス化します。これにより、ピクセルデータで埋めることができるキャンバスが得られます。

```java
String dataDir = "Your Document Directory";
PsdImage image = new PsdImage(500, 500);
```

### Step 2: Fill Image Data
ステップ 2: 画像データを埋める  
画像に生の ARGB ピクセル値を設定します。実際のシナリオでは別のソースからピクセルデータをロードすることもありますが、ここでは単にプロセスを示しています。

```java
int count = image.getWidth() * image.getHeight();
int[] pixels = new int[count];
int r = 0, g = 0, b = 0, channel = 0;
for (int i = 0; i < count; i++) {
    // Fill pixels with color values.
    // ...
}
// Save the newly created pixels.
image.saveArgb32Pixels(image.getBounds(), pixels);
```

### Step 3: Save Image with Default ICC Profiles
ステップ 3: デフォルトの ICC プロファイルで画像を保存  
この時点で保存すると、ライブラリのデフォルトカラー プロファイルを使用して画像が書き込まれます。この手順により、後でカスタムプロファイルを適用した後の違いが確認できます。

```java
image.save(dataDir + "Default_profiles.jpg");
```

### Step 4: Update Color Profiles (Apply ICC Profile & Set RGB Profile)
ステップ 4: カラープロファイルを更新 (ICC プロファイルを適用 & RGB プロファイルを設定)  
外部の ICC ファイルをロードし、画像に割り当てます。ここで **icc プロファイルを適用** および **rgb プロファイルを設定** します。

```java
File rgbFile = new File(dataDir + "eciRGB_v2.icc");
FileInputStream rgbInputStream = new FileInputStream(rgbFile);
StreamSource rgbprofile = new StreamSource(rgbInputStream);
File cmykFile = new File(dataDir + "ISOcoated_v2_FullGamut4.icc");
FileInputStream cmykInputStream = new FileInputStream(cmykFile);
StreamSource cmykprofile = new StreamSource(cmykInputStream);
image.setRgbColorProfile(rgbprofile);
image.setCmykColorProfile(cmykprofile);
```

### Step 5: Save Image with New YCCK Profiles
ステップ 5: 新しい YCCK プロファイルで画像を保存  
最後に、先ほど設定した CMYK プロファイルを考慮した YCCK カラーモードで JPEG として画像をエクスポートします。

```java
JpegOptions options = new JpegOptions();
options.setColorType(JpegCompressionColorMode.Ycck);
image.save(dataDir + "Ycck_profiles.jpg", options);
```

これらの手順に従うことで、PSD 画像の **カラー プロファイルを変換**し、**ICC プロファイルを適用**、そして正確なレンダリングのために **RGB プロファイルを設定** しました。

## Common Issues and Solutions
| 問題 | 原因 | 対策 |
|------|------|------|
| 変換後に色がくすんで見える | 誤ったプロファイルが割り当てられた、またはプロファイルデータが欠如している | ICC ファイルが元画像のカラースペースに対応しているか確認してください。 |
| `FileNotFoundException` が ICC ファイルの読み込み時に発生 | `dataDir` パスが正しくない | 絶対パスを使用するか、ファイルが指定ディレクトリに配置されていることを確認してください。 |
| YCCK カラーなしで JPEG が保存される | `JpegOptions` が `Ycck` に設定されていない | 保存前に `options.setColorType(JpegCompressionColorMode.Ycck)` を呼び出してください。 |

## Frequently Asked Questions
**Q: Aspose.PSD for Java でカスタム ICC プロファイルを使用できますか？**  
A: はい、提供された ICC ファイルを独自のものに置き換え、`StreamSource` を新しいファイルに指すだけです。

**Q: 結果画像の色差をどのように処理できますか？**  
A: ICC プロファイルを微調整するか、変換後に明るさ、コントラスト、ガンマを調整する Aspose.PSD のカラー調整 API を使用してください。

**Q: Aspose.PSD は画像のバッチ処理に適していますか？**  
A: はい。PSD ファイルが入ったフォルダーをループし、同じプロファイルロジックを適用して、結果を効率的に保存できます。

**Q: カラーマネジメント用の ICC プロファイルはどこで入手できますか？**  
A: ICC の公式サイト、Adobe のカラーレソースページ、またはデバイス固有のプロファイルを提供するベンダーのライブラリをご覧ください。

**Q: カラー変換で ICC プロファイルを使用する利点は何ですか？**  
A: デバイス間で一貫した色を保証し、ワークフローの自動化を簡素化し、手動でのカラーマッチング作業を削減します。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**最終更新日:** 2026-03-21  
**テスト環境:** Aspose.PSD for Java (latest)  
**作者:** Aspose