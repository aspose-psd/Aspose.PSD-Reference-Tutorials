---
date: 2026-01-07
description: Aspose.PSD for Java を使用して、メディアンフィルタとウィナーフィルタの適用手順をステップバイステップで学び、PSD を効率的に
  GIF に変換しましょう。
linktitle: Apply Median and Wiener Filters
second_title: Aspose.PSD Java API
title: ステップバイステップフィルタ - メディアンフィルタとウィーナーフィルタの適用（Java）
url: /ja/java/image-processing/apply-median-wiener-filters/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ステップバイステップ フィルタ: Median と Wiener フィルタの適用 (Java)

## はじめに

Java でノイズの多い画像をクリーンアップするための **ステップバイステップ フィルタ** ワークフローを探しているなら、ここが最適です。Aspose.PSD for Java を使用すれば、Median と Wiener の両フィルタを簡単に適用でき、処理後に **PSD を GIF に変換** することも可能です。このチュートリアルでは、ライブラリの設定からフィルタ結果の保存まで、必要な手順をすべて解説しますので、高品質な画像デノイズを自信を持ってアプリケーションに組み込めます。

## クイック回答
- **Median フィルタは何をしますか？** 塩胡椒ノイズを低減し、エッジを保持します。  
- **Wiener フィルタはいつ使用すべきですか？** 局所的な画像分散を考慮した適応型ノイズ除去のためです。  
- **コードを実行するのにライセンスが必要ですか？** 開発には無料トライアルで動作しますが、本番環境では商用ライセンスが必要です。  
- **出力を GIF として保存できますか？** はい—Aspose.PSD を使用すると **convert PSD to GIF** をワンステップで行えます。  
- **実装にどれくらい時間がかかりますか？** 基本的なセットアップで通常 10 分未満です。

## ステップバイステップ フィルタとは？

*ステップバイステップ フィルタ* アプローチは、画像処理を明確で管理しやすい段階—画像の読み込み、フィルタオプションの設定、フィルタの適用、最終的な保存—に分割します。この体系的なフローにより、各部分のデバッグ、コードの再利用、異なる画像フォーマットへの適応が容易になります。

## なぜ Aspose.PSD for Java を使用するのか？

- **幅広いフォーマットサポート** – PSD、PNG、JPEG、GIF などに対応。  
- **外部依存なし** – 純粋な Java で、どのプロジェクトにも簡単に組み込めます。  
- **組み込みフィルタオプション** – Median、Wiener、その他高度なフィルタがすぐに使用可能です。  
- **ワンクリック変換** – 処理後に直接 GIF、PNG、または JPEG にエクスポートできます。

## 前提条件

開始する前に、以下を用意してください：

1. **Aspose.PSD for Java Library** – ライブラリは [here](https://releases.aspose.com/psd/java/) からダウンロードしてインストールします。  
2. **Java Development Environment** – JDK 8 以上と、IDE またはビルドツール（Maven/Gradle）がセットアップされた環境。

## パッケージのインポート

画像処理とフィルタオプションにアクセスできる必要なクラスをインポートします。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.MedianFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

## ステップバイステップ フィルタ: Median フィルタの適用方法

### 手順 1: 画像の読み込み

まず、クリーンアップしたい PSD ファイルを API に指定します。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load the source image
Image image = Image.load(sourceFile);
```

### 手順 2: 画像を RasterImage にキャスト

フィルタはラスターデータ上で動作するため、汎用 `Image` を `RasterImage` にキャストします。

```java
// Cast the image into RasterImage
RasterImage rasterImage = (RasterImage)image;
if (rasterImage == null) {
    return;
}
```

### 手順 3: MedianFilterOptions インスタンスの作成

Median カーネルのサイズを設定します。**4** のサイズは中程度のノイズに適しています。

```java
// Create an instance of MedianFilterOptions class and set the filter size
MedianFilterOptions options = new MedianFilterOptions(4);
```

### 手順 4: Median フィルタの適用

画像全体の境界に対してフィルタを適用します。

```java
// Apply MedianFilterOptions filter to RasterImage object
rasterImage.filter(image.getBounds(), options);
```

### 手順 5: 結果画像の保存 (PSD を GIF に変換)

フィルタ処理後、出力を GIF として保存します—**convert PSD to GIF** 機能を実演します。

```java
String destName = dataDir + "median_test_denoise_out.gif";
// Save the resultant image as a GIF
image.save(destName, new GifOptions());
```

これらの手順に従うことで、Median フィルタを正常に適用し、クリーンアップした画像を GIF としてエクスポートできました。

## Wiener フィルタの適用 (オプション拡張)

プロジェクトで適応型ノイズ除去が必要な場合は、Median フィルタを Wiener フィルタに置き換えることができます。コード構造は同一で、`WienerFilterOptions` をインポートし、希望の半径でインスタンス化するだけです。

> **プロのヒント:** 両フィルタのカーネルサイズを色々試して、ノイズ除去とディテール保持のベストバランスを見つけてください。

## よくある問題とトラブルシューティング

| 症状 | 考えられる原因 | 対策 |
|------|----------------|------|
| `RasterImage` へのキャスト時の `ClassCastException` | 入力ファイルがラスタ互換の PSD ではない | PSD にラスタレイヤが含まれているか確認するか、まずレイヤをラスタに変換してください |
| 出力 GIF が空白 | 出力先パスが間違っている、またはフォルダに書き込み権限がない | `dataDir` が存在し、書き込み可能なディレクトリを指していることを確認してください |
| フィルタが効果を示さないように見える | ノイズレベルに対してカーネルサイズが小さすぎる | フィルタサイズを増やす（例: `new MedianFilterOptions(6)`） |

## よくある質問

**Q1: これらのフィルタは任意のフォーマットの画像に適用できますか？**  
A1: はい、Aspose.PSD は幅広い画像フォーマットをサポートしているため、さまざまなプロジェクトで汎用的に利用できます。

**Q2: Aspose.PSD for Java の無料トライアルはありますか？**  
A2: はい、[here](https://releases.aspose.com/) から無料トライアルを取得できます。

**Q3: Aspose.PSD for Java のサポートはどこで受けられますか？**  
A3: コミュニティサポートは [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) で利用できます。

**Q4: Aspose.PSD for Java のドキュメントはどこにありますか？**  
A4: ドキュメントは [here](https://reference.aspose.com/psd/java/) にあります。

**Q5: Aspose.PSD for Java を購入するには？**  
A5: 製品は [here](https://purchase.aspose.com/buy) から購入できます。

## 結論

本ガイドでは、Aspose.PSD for Java を使用して Median（必要に応じて Wiener）フィルタを適用する **ステップバイステップ フィルタ** プロセスを実演し、デノイズ後に **PSD を GIF に変換** する方法を示しました。これらの構成要素を組み合わせることで、写真のクリーンアップ、Web 用アセットの準備、バッチ変換の自動化など、あらゆる Java アプリケーションに堅牢な画像処理パイプラインを統合できます。

---

**最終更新日:** 2026-01-07  
**テスト環境:** Aspose.PSD for Java 24.12 (執筆時点での最新)  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}