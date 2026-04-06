---
date: 2026-01-07
description: Aspose.PSD for Java を使用した Java の画像トリミング方法を学びましょう。画像のトリミング、リサイズ、PSD から
  JPEG への変換に関するステップバイステップガイドです。
linktitle: Expand and Crop Images
second_title: Aspose.PSD Java API
title: '画像のトリミング Java - Aspose.PSD for Javaで画像を拡大・トリミング'
url: /ja/java/image-editing/expand-and-crop-images/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crop Image Java: Aspose.PSD for Java で画像の拡張とトリミング

## はじめに

このチュートリアルでは、Aspose.PSD ライブラリを使用して **crop image java** を実現する方法を紹介します。キャンバスを拡張したり不要な端をトリミングしたり、PSD ファイルを JPEG に変換したりする必要がある場合でも、以下の手順に従えばクリーンで再現性のあるプロセスを実行できます。前提条件、インポート文、各コーディングステップをわかりやすく解説するので、実務プロジェクトにすぐ適用できます。

## よくある質問
- **Javaで画像切り抜きを行うライブラリはどれですか？** Aspose.PSD for Javaです。
- **開発にはライセンスが必要ですか？** 無料トライアルはテストに使用できますが、本番環境では商用ライセンスが必要です。
- **切り抜き時にPSDをJPEGに変換できますか？** はい、`JpegOptions`と切り抜き範囲を指定することで可能です。
- **Java 8はサポートされていますか？** Aspose.PSDはJava 8以降のバージョンをサポートしています。
- **実装にはどれくらい時間がかかりますか？** 基本的な切り抜き操作であれば、通常10分以内です。

## 「Javaで画像切り抜き」とは何ですか？

Java で画像をトリミングするとは、元画像の矩形領域を選択し、残りの部分を破棄することを指します。Aspose.PSD を使用すると、この領域を `Rectangle` オブジェクトで定義し、JPEG など別の形式で結果を保存できます。

## Javaでの画像切り抜きにAspose.PSDを使用する理由

- **Full PSD support** – 変換せずにレイヤー構造を持つ PSD ファイルを直接操作できます。  
- **High‑performance raster handling** – 大容量画像でもメモリ使用量を抑えて高速に処理できます。  
- **Built‑in conversion** – トリミングやキャンバス拡張を行いながら、JPEG、PNG、BMP などに簡単にエクスポートできます。  
- **Cross‑platform** – Java が動作するあらゆる環境で利用可能です。

## 前提条件

1. **Java Development Kit (JDK)** – Java 8 以降がインストールされていること。  
2. **Aspose.PSD for Java** – 公式サイト **[here](https://releases.aspose.com/psd/java/)** からライブラリをダウンロードしてください。  

**ヒント:** `ClassNotFoundException` を回避するために、Aspose.PSD JAR をプロジェクトのクラスパスまたは Maven/Gradle の依存関係に追加してください。

## パッケージのインポート

必要なインポートを Java ソースファイルに追加してください。これらのクラスを使用すると、画像の読み込み、ラスター操作、矩形定義、および JPEG エクスポートオプションにアクセスできます。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

## ステップ 1: ドキュメントディレクトリの設定

ソース PSD ファイルが格納されているフォルダを指定してください。プレースホルダーを実際のパスに置き換えてください。

```java
String dataDir = "Your Document Directory";
```

## ステップ 2: ソースパスと出力パスの指定

PSD ファイルの読み込み元と、切り抜き後の JPEG ファイルの出力先を指定してください。

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## ステップ 3: 画像の読み込みとキャッシュ

PSD ファイルを `RasterImage` オブジェクトに読み込みます。キャッシュすることで、切り抜きなどの後続処理のパフォーマンスが向上します。

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

## ステップ 4: 切り抜き用の矩形の作成

残したい領域を表す `Rectangle` オブジェクトを作成します。座標に負の値を指定することで、切り抜き前にキャンバスを **拡張**できます。これは、元の画像に境界線を追加する場合に便利です。

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

> **なぜ負の座標を使うのか？** > 負のX/Y値は切り抜き領域を左/上に移動させ、最終的な切り抜きを行う前に元のコンテンツの周囲に余白（拡張）を効果的に追加します。

## ステップ5：切り抜き画像の保存

最後に、`JpegOptions`を使用して結果の画像を保存します。このステップでは、切り抜き矩形を適用しながら**PSDをJPEGに変換する**方法も示しています。

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

**結果:** `jpeg_out.jpg` には、300×300ピクセルの画像が格納されました。この画像は、各辺が200ピクセルずつ拡大され、指定された長方形にトリミングされています。

おめでとうございます！わずか数行の簡潔なコードで、**Javaによる画像トリミング**、キャンバスの拡大、そしてPSDファイルのJPEG変換を成功させました。

## 一般的な使用例

- **Preparing assets for web** – アップロード前にスクリーンショットやデザインをトリミング・リサイズできます。  
- **Generating thumbnails** – 大きな PSD から特定領域を抽出してサムネイルとして利用できます。  
- **Automated batch processing** – フォルダー内の PSD ファイルを一括で処理し、同一のトリミング矩形を適用できます。

## トラブルシューティングとヒント

| 問題 | 推奨される解決策 |

|-------|----------------|

| 大きなPSDファイルを読み込む際に`OutOfMemoryError`が発生する | `rasterImage.cacheData()`を早めに呼び出し、JVMヒープサイズを増やす（`-Xmx`）ことを検討してください。 |

| 切り抜き領域が中心からずれている | 矩形のX/Yオフセットを確認してください。負の値はキャンバスを拡大することに注意してください。 |

| 出力JPEGがぼやけている | `JpegOptions`の品質設定を調整してください（例：`new JpegOptions { Quality = 90 }`）。 |

## よくある質問

### Q1: Aspose.PSDは様々なJavaバージョンに対応していますか？

A1: はい、Aspose.PSDは様々なJavaバージョンに対応しており、幅広い開発環境との互換性を確保しています。

### Q2: Aspose.PSDを商用プロジェクトに使用できますか？


A2: はい、Aspose.PSDは開発者向けに商用ライセンスを提供しており、個人プロジェクトと商用プロジェクトの両方でご利用いただけます。

### Q3: サポートされている画像ファイル形式に制限はありますか？

A3: Aspose.PSDは、PSD、JPEG、PNGなど、さまざまな画像ファイル形式をサポートしています。[ドキュメント](https://reference.aspose.com/psd/java/)で完全なリストをご確認ください。

### Q4: Aspose.PSDに関する質問へのサポートを受けるにはどうすればよいですか？

A4: [Aspose.PSDフォーラム](https://forum.aspose.com/c/psd/34)にアクセスして、コミュニティまたはAsposeサポートチームにご相談ください。

### Q5: 無料トライアルはありますか？

A5: はい、Aspose.PSDの無料トライアルをご利用いただけます。[こちら](https://releases.aspose.com/)からダウンロードしてください。

---

**最終更新日:** 2026年1月7日
**テスト環境:** Aspose.PSD for Java 24.12
**作成者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}