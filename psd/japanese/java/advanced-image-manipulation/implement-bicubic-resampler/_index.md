---
date: 2026-04-12
description: Aspose.PSD のバイキュービックリサンパーを使用して Java で画像のサイズ変更方法を学びましょう。この画像スケーリングチュートリアルでは、優れた結果を得るためのステップバイステップの手順を示します。
keywords:
- resize image java
- image scaling tutorial
- java image library
linktitle: バイキュービックリサンプラーを実装する
second_title: Aspose.PSD Java API
title: 画像リサイズ Java – 高品質スケーリングのためのバイキュービックリサンプラー
url: /ja/java/advanced-image-manipulation/implement-bicubic-resampler/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 画像リサイズ Java – 高品質スケーリングのためのバイキュービックリサンプラー

## はじめに

シャープさを失ったりアーティファクトが発生したりすることなく **resize image java** プロジェクトを行う必要がある場合、ここが適切な場所です。この **image scaling tutorial** では、Aspose.PSD の Bicubic Resampler を使用する方法を解説します。これは PSD ファイルやその他多数のフォーマットに対して滑らかで鮮明な結果を提供する強力な **java image library** 機能です。このガイドの最後までに、数行のコードだけで任意の Java アプリケーションに高品質スケーリングを統合できるようになります。

## クイック回答
- **What does the Bicubic Resampler do?** 画像をリサイズする際にディテールを保持する高度な補間アルゴリズムを適用します。  
- **Which ResizeType values are available?** `CubicConvolution` と `Bell` は Aspose.PSD が提供する二つのバイキュービックオプションです。  
- **Do I need a license to run the code?** 評価用には一時的な aspose ライセンスで動作しますが、本番環境ではフルライセンスが必要です。  
- **What Java version is required?** Java 8 以上のランタイムであれば、最新の Aspose.PSD ライブラリと互換性があります。  
- **Can I resize other formats (PNG, JPEG) with the same API?** はい、Aspose.PSD は複数の画像タイプをサポートしていますが、例は PSD に焦点を当てています。

## 高品質画像スケーリングとは？

高品質画像スケーリングとは、画像をリサイズする際にシャープなエッジ、滑らかなグラデーション、正確な色再現を維持することを指します。Bicubic Resampler は、周囲のピクセルの値（キュービックコンボリューションまたはベルアルゴリズムを使用）を考慮して各新ピクセルを計算することで、最近傍法やバイリニア法に比べてより自然な見た目を実現します。

## 高品質画像スケーリングにバイキュービックリサンプラーを使用する理由

- **ディテールを保持:** 細かいテクスチャや線画も、サイズを大幅に変更しても鮮明に保たれます。  
- **アーティファクトを低減:** 単純なアルゴリズムでよく発生するリングやぼやけを最小限に抑えます。  
- **簡単な統合:** ワンラインのメソッド呼び出し (`image.resize`) で、コードを書き換えることなくアルゴリズムを切り替えられます。  

## 前提条件

- **Aspose.PSD for Java** – 最新の JAR を [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/) からダウンロードしてください。  
- **Java Development Kit** – JDK 8 以上がインストールされ、設定されていること。  
- **Sample PSD file** – テスト画像（例: `sample_bicubic.psd`）を既知のディレクトリに配置します。  

これらの項目は合わせて、チュートリアルのための堅牢な **java image library** 基盤を構成します。

## パッケージのインポート

必要なインポートを Java クラスに追加します。これにより、コアの Aspose.PSD クラスと `ResizeType` 列挙型が利用可能になります。

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
```

## バイキュービックリサンプラーで画像をリサイズする方法

### 手順 1: 画像をロードする

まず、リサイズしたい元の PSD ファイルをロードします。`Your Document Directory` を実際のパスに置き換えてください。

```java
String dataDir = "Your Document Directory";
String filePath = dataDir + "sample_bicubic.psd";
PsdImage image = (PsdImage)Image.load(filePath);
```

### 手順 2: キュービックコンボリューションでリサイズ (高品質)

次に、**Cubic Convolution** アルゴリズムを適用します。これは高品質画像スケーリングを実現する二つのバイキュービックオプションの一つです。例では画像を 300 × 300 ピクセルにリサイズします。

```java
String destNameCubicConvolution = dataDir + "ResamplerCubicConvolutionStripes_after.psd";
image.resize(300, 300, ResizeType.CubicConvolution);
image.save(destNameCubicConvolution, new PsdOptions(image));
```

### 手順 3: ベルアルゴリズムでリサイズ (代替高品質)

もし **Bell** アルゴリズムを好む場合、やや異なるスムージング効果を提供しますが、同様に使用できます。比較を公平に保つために、元の画像を再度ロードしていることに注意してください。

```java
String destNameBell = dataDir + "ResamplerBellStripes_after.psd";
PsdImage imageBellStripes = (PsdImage)Image.load(filePath);
imageBellStripes.resize(300, 300, ResizeType.Bell);
imageBellStripes.save(destNameBell, new PsdOptions(imageBellStripes));
```

他のサイズやファイル形式でも自由に試してみてください。パラメータを適宜調整すれば構いません。

## よくある落とし穴とヒント

- **パスが正しくない:** `dataDir` が OS に適したファイル区切り文字（`/` または `\`）で終わっていることを確認してください。  
- **ライセンス例外:** 有効なライセンスなしで実行すると、出力画像に透かしが付く可能性があります。テストには **temporary aspose license** を使用し、本番環境では永続ライセンスに切り替えてください。  
- **メモリ使用量:** 大きな PSD ファイルはかなりのメモリを消費する可能性があるため、保存後に画像を破棄（`image.dispose()`）することを検討してください。  

## よくある質問

**Q: Aspose.PSD for Java を他の画像フォーマットで使用できますか？**  
A: はい、ライブラリは PSD、PNG、JPEG、TIFF、BMP など多数の画像タイプをサポートしていますが、例は PSD に焦点を当てています。

**Q: Aspose.PSD for Java 用の一時ライセンスは利用可能ですか？**  
A: はい、[here](https://purchase.aspose.com/temporary-license/) から取得できます。

**Q: Aspose.PSD for Java のサポートはどこで見つけられますか？**  
A: サポートに関する問い合わせは Aspose.PSD フォーラム [here](https://forum.aspose.com/c/psd/34) をご利用ください。

**Q: Aspose.PSD for Java ライブラリをダウンロードできますか？**  
A: はい、リリースページ [here](https://releases.aspose.com/psd/java/) からダウンロードできます。

**Q: Aspose.PSD for Java の購入方法は？**  
A: 購入ページ [here](https://purchase.aspose.com/buy) から購入できます。

---

**最終更新日:** 2026-04-12  
**テスト環境:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**作者:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}