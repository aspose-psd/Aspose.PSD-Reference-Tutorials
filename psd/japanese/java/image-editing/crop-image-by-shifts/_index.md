---
date: 2026-01-01
description: Aspose.PSD for Java を使用した画像のトリミング方法を学び、Java の画像処理をマスターしましょう。シームレスな画像操作のための包括的なチュートリアルです。
linktitle: Crop Image by Shifts
second_title: Aspose.PSD Java API
title: Java 画像処理 – Aspose.PSD を使用したシフトによる画像の切り抜き
url: /ja/java/image-editing/crop-image-by-shifts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java 画像処理 – Aspose.PSD を使用したシフトによる画像の切り抜き

## はじめに

**java image processing** に取り組むと、正確なトリミングがあらゆるグラフィックワークフローの基本的な構成要素であることにすぐ気付くでしょう。境界線を削除したり、不要な背景を取り除いたり、Web 配信用にアセットを準備したりする際に、**画像の切り抜き方法** をプログラムで実行できれば、手作業の時間を大幅に削減できます。本チュートリアルでは、強力な **Aspose.PSD for Java** ライブラリを使用して、各辺のシフト値を指定してラスタ画像を切り抜く手順を解説します。最後まで読めば、**crop メソッド** を自信を持って使えるようになり、**画像の切り抜き最適化** も行えるようになります。

## クイック回答
- **java 画像処理を扱うライブラリは？** Aspose.PSD for Java  
- **ラスタ画像を切り抜くメソッドは？** `RasterImage.crop(left, right, top, bottom)`  
- **データを先にキャッシュする必要がありますか？** はい – 大きな PSD ファイルではキャッシュが速度向上に寄与します  
- **カスタムの切り抜き余白を設定できますか？** もちろんです – left、right、top、bottom のシフトを指定します  
- **サポートされている出力形式は？** JPEG、PNG、BMP など多数、`ImageOptions` で指定可能

## java 画像処理とは？
Java 画像処理とは、Java ベースの API を用いてビットマップやベクターグラフィックを操作することを指します。リサイズ、フィルタリング、フォーマット変換、そして **画像の切り抜き余白** の調整などのタスクを、サーバーサイドやデスクトップアプリケーションで自動化できます。

## Aspose.PSD を java 画像処理に使う理由
Aspose.PSD は、Photoshop 互換の PSD ファイル、レイヤー、チャンネル、マスクを理解する純粋な Java ソリューションです。ネイティブライブラリが不要で、クロスプラットフォームに対応し、既存の Java プロジェクトにシンプルに統合できる **crop raster image** API を提供します。

## 前提条件

- **Java Development Kit (JDK)** – 最新版は [here](https://www.oracle.com/java/technologies/javase-downloads.html) からダウンロードしてください。  
- **Aspose.PSD for Java Library** – 最新リリースは [download page](https://releases.aspose.com/psd/java/) から入手できます。  
- **統合開発環境 (IDE)** – Eclipse、IntelliJ IDEA、またはお好みのエディタをご使用ください。

## パッケージのインポート

Java プロジェクトで必要なクラスをインポートし、切り抜きワークフローを開始します。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## 手順別ガイド

### 手順 1: 画像の読み込み（how to crop image）

まず、ソース PSD ファイルを `RasterImage` インスタンスにロードします。これによりピクセルレベルで直接操作できるようになります。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
```

### 手順 2: 画像データのキャッシュ（optimize image cropping）

画像データをメモリにキャッシュすると、切り抜きなどの複数操作時の I/O オーバーヘッドが削減されます。

```java
if (!rasterImage.isCached()) {
  rasterImage.cacheData();
}
```

### 手順 3: 切り抜き余白の定義（image cropping margins）

各辺から何ピクセル削除するかを指定します。希望する **画像の切り抜き余白** に合わせて値を調整してください。

```java
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

### 手順 4: 切り抜きの適用（use crop method）

シフト値を渡して `crop` メソッドを呼び出します。この **crop raster image** 操作により、基になるビットマップが変更されます。

```java
rasterImage.crop(leftShift, rightShift, topShift, bottomShift);
```

### 手順 5: 結果の保存（how to crop image to a new format）

最後に、切り抜いた画像をディスクに書き出します。この例では JPEG を選択していますが、Aspose.PSD がサポートする任意の形式を使用できます。

```java
String destName = dataDir + "CroppingByShifts_out.jpg";
rasterImage.save(destName, new JpegOptions());
```

おめでとうございます！Aspose.PSD for Java を使って **シフトによる画像の切り抜き** に成功しました。これは **java image processing** ツールキットにおける重要なスキルです。

## よくある問題と解決策

| 問題 | 解決策 |
|------|--------|
| **大きな PSD ファイルで `OutOfMemoryError` が発生** | Step 2 の `cacheData()` を必ず呼び、JVM のヒープサイズ (`-Xmx`) を増やすことを検討してください。 |
| **予期しない透明な境界が出る** | シフト値が期待通りの余白を示しているか確認してください。負の値はトリミングではなく拡張になります。 |
| **誤った形式で保存される** | `save` 時に適切な `ImageOptions` サブクラス（例: `PngOptions`）を使用してください。 |

## FAQ

**Q: Aspose.PSD はすべての画像形式に対応していますか？**  
A: はい、Aspose.PSD は多数のラスタおよびベクター形式をサポートしており、プロジェクトでの汎用性が高いです。

**Q: 同じ画像に対して複数回切り抜きを行うことはできますか？**  
A: 可能です。`crop` を繰り返し呼び出すことができ、各呼び出しは画像の現在の状態に対して適用されます。

**Q: Aspose.PSD のサポートフォーラムはありますか？**  
A: はい、[Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) でサポートやコミュニティとの交流が可能です。

**Q: Aspose.PSD の一時ライセンスはどこで取得できますか？**  
A: [here](https://purchase.aspose.com/temporary-license/) から一時ライセンスを取得できます。

**Q: Aspose.PSD のサンプルプロジェクトはありますか？**  
A: はい、[Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/) にドキュメントとサンプルが掲載されています。

## 結論

本ガイドでは、シフト値を指定して **ラスタ画像を切り抜く** 方法を解説しました。このテクニックは、細かい調整が必要な **java image processing** において不可欠です。これで、Web 用アセットの準備、サムネイル生成、スキャン文書のクリーンアップなど、さまざまなワークフローに切り抜きを組み込むための確固たる基盤ができました。

---

**最終更新日:** 2026-01-01  
**テスト環境:** Aspose.PSD 24.11 for Java  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}