---
date: 2025-12-01
description: Aspose.PSD のバイキュービックリサンプラーを使用して、Java で高品質な画像スケーリングを実現する方法を学びましょう。優れた結果を得るためのステップバイステップガイドをご覧ください。
linktitle: Implement Bicubic Resampler
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java のバイキュービックリサンプラーによる高品質画像スケーリング
url: /ja/java/advanced-image-manipulation/implement-bicubic-resampler/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java のバイキュービックリサンプラーによる高品質画像スケーリング

## はじめに

高品質画像スケーリングは、視覚的忠実度を損なうことなくグラフィックのサイズを変更する必要がある場合に頻繁に求められます。Aspose.PSD for Java は **Bicubic Resampler** を提供し、PSD ファイルやその他のサポート形式に対して滑らかで鮮明な結果を実現します。このチュートリアルでは、Bicubic Resampler の実装方法をステップバイステップで正確に学び、Java アプリケーションに高品質画像スケーリングをすぐに導入できるようにします。

## クイック回答
- **Bicubic Resampler は何を行いますか？** 画像のリサイズ時にディテールを保持する高度な補間アルゴリズムを適用します。  
- **利用可能な ResizeType の値は何ですか？** `CubicConvolution` と `Bell` の 2 つのバイキュービックオプションが Aspose.PSD に用意されています。  
- **コード実行にライセンスは必要ですか？** 評価用に一時ライセンスで動作しますが、本番環境では正式ライセンスが必要です。  
- **必要な Java バージョンは何ですか？** Java 8 以降のランタイムであれば、最新の Aspose.PSD ライブラリと互換性があります。  
- **同じ API で他の形式 (PNG、JPEG) をリサイズできますか？** はい、Aspose.PSD は複数の画像タイプをサポートしていますが、例は PSD に焦点を当てています。

## 高品質画像スケーリングとは？

高品質画像スケーリングとは、画像をリサイズする際にエッジの鮮明さ、グラデーションの滑らかさ、色表現の正確さを保つことを指します。Bicubic Resampler は、周囲のピクセル値（キュービックコンボリューションまたはベルアルゴリズム）を考慮して各新ピクセルを計算し、最近傍法や双一次補間に比べてより自然な見た目を実現します。

## なぜ高品質画像スケーリングにバイキュービックリサンプラーを使用するのか？

- **ディテールを保持:** 細かなテクスチャや線画が大幅なサイズ変更後でもクリアに保たれます。  
- **アーティファクトを低減:** 簡易アルゴリズムでよく見られるリングやぼやけを最小化します。  
- **簡単に統合:** ワンラインのメソッド呼び出し (`image.resize`) でアルゴリズムを切り替えられ、コードの書き換えが不要です。  

## 前提条件

開始する前に以下を用意してください。

- **Aspose.PSD for Java** – 最新の JAR を [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/) からダウンロード。  
- **Java Development Kit** – JDK 8 以上がインストールされ、設定済みであること。  
- **Sample PSD file** – テスト画像（例: `sample_bicubic.psd`）を既知のディレクトリに配置。  

## パッケージのインポート

Java クラスに必要なインポートを追加します。これにより、コアの Aspose.PSD クラスと `ResizeType` 列挙型が利用可能になります。

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
```

## 手順 1: 画像の読み込み

まず、リサイズしたい元の PSD ファイルを読み込みます。`Your Document Directory` を実際のパスに置き換えてください。

```java
String dataDir = "Your Document Directory";
String filePath = dataDir + "sample_bicubic.psd";
PsdImage image = (PsdImage)Image.load(filePath);
```

## 手順 2: キュービックコンボリューションでリサイズ (高品質)

次に、**Cubic Convolution** アルゴリズムを適用します。これはバイキュービックオプションの 1 つで、高品質画像スケーリングを実現します。例では画像を 300 × 300 ピクセルにリサイズします。

```java
String destNameCubicConvolution = dataDir + "ResamplerCubicConvolutionStripes_after.psd";
image.resize(300, 300, ResizeType.CubicConvolution);
image.save(destNameCubicConvolution, new PsdOptions(image));
```

## 手順 3: ベルアルゴリズムでリサイズ (代替高品質)

**Bell** アルゴリズムを使用したい場合は、こちらの手順で同様にリサイズできます。比較を公平に保つため、元の画像を再度読み込んでいます。

```java
String destNameBell = dataDir + "ResamplerBellStripes_after.psd";
PsdImage imageBellStripes = (PsdImage)Image.load(filePath);
imageBellStripes.resize(300, 300, ResizeType.Bell);
imageBellStripes.save(destNameBell, new PsdOptions(imageBellStripes));
```

他のサイズやファイル形式でも自由に試してみてください。パラメータを調整するだけで対応できます。

## よくある落とし穴とヒント

- **パスが正しくない:** `dataDir` が OS に適したファイル区切り文字（`/` または `\`）で終わっていることを確認してください。  
- **ライセンス例外:** 有効なライセンスなしで実行すると、出力画像に透かしが付加される場合があります。  
- **メモリ使用量:** 大きな PSD ファイルは多くのメモリを消費します。保存後は `image.dispose()` で画像を破棄することを検討してください。  

## よくある質問

**Q: Aspose.PSD for Java を他の画像形式でも使用できますか？**  
A: はい、ライブラリは PSD、PNG、JPEG、TIFF、BMP など多数の形式をサポートしています。

**Q: Aspose.PSD for Java 用の一時ライセンスは入手可能ですか？**  
A: はい、[here](https://purchase.aspose.com/temporary-license/) から一時ライセンスを取得できます。

**Q: Aspose.PSD for Java のサポートはどこで受けられますか？**  
A: サポートに関する質問は Aspose.PSD フォーラム [here](https://forum.aspose.com/c/psd/34) で受け付けています。

**Q: Aspose.PSD for Java ライブラリをダウンロードできますか？**  
A: はい、リリースページからライブラリをダウンロードできます。[here](https://releases.aspose.com/psd/java/)

**Q: Aspose.PSD for Java を購入するには？**  
A: 購入ページから購入できます。[here](https://purchase.aspose.com/buy)

---

**最終更新日:** 2025-12-01  
**テスト環境:** Aspose.PSD for Java 24.11 (執筆時点での最新バージョン)  
**作者:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}