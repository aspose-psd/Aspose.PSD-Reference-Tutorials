---
date: 2026-02-12
description: Aspose.PSD を使用して Java で特定の角度に画像を回転する方法を学びます。このガイドでは、画像の回転、角度（度）での画像回転、そして背景色の処理方法を示します。
linktitle: How to Rotate Image on a Specific Angle
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java を使用して特定の角度で画像を回転する方法
url: /ja/java/advanced-image-manipulation/rotate-image-specific-angle/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java を使用した特定の角度で画像を回転させる方法

## はじめに

Java アプリケーションでプログラム的に **画像の回転方法** が必要な場合、Aspose.PSD for Java はクリーンで高性能な API を提供し、重い処理を代行してくれます。フォトエディタの構築、サムネイルの生成、または Web サービス向けのアセット準備など、正確な角度で画像を回転させることは一般的な要件です。このチュートリアルでは、PSD ファイルの読み込みから回転結果の保存までの全工程を解説し、キャッシュや背景処理といったベストプラクティスも紹介します。

## クイック回答
- **Javaで画像を回転させるのに最適なライブラリは何ですか？** Aspose.PSD for Java。  
- **任意の角度で回転できますか？** はい、`rotate` メソッドは `float` の角度（正または負）を受け取ります。  
- **開発にライセンスは必要ですか？** 無料トライアルでテストは可能ですが、本番環境ではライセンスが必要です。  
- **サポートされている画像フォーマットは何ですか？** PSD、JPEG、PNG、TIFF、GIF、BMP など多数。  
- **空白領域の背景色はどう設定しますか？** `rotate` メソッドに `Color` インスタンスを渡します。

## Java における画像回転とは？

画像回転とは、ピクセルマトリックスを基準点（通常は中心）を中心に指定された角度だけ回転させることです。Java では `Graphics2D` を使って手動で実装できますが、Aspose.PSD は数学的計算を抽象化し、異なるカラー深度を処理し、PSD ファイルの場合はレイヤ情報も保持します。

## 画像回転に Aspose.PSD を使用する理由

- **精度:** 任意の小数角度で品質劣化なしに回転できます。  
- **パフォーマンス:** 組み込みキャッシュ (`image.cacheData()`) により大きなファイルの処理が高速化します。  
- **背景制御:** 回転で生じた隙間を埋める背景色を指定できます。  
- **フォーマットの柔軟性:** PSD を読み込み、JPEG、PNG、または任意のサポートフォーマットで出力できます。

## 前提条件

開始する前に、以下が揃っていることを確認してください。

1. **Java Development Kit (JDK 8 以上)** – 動作する Java IDE またはコマンドライン環境。  
2. **Aspose.PSD for Java** – 最新の JAR を [Aspose.PSD Java ページ](https://reference.aspose.com/psd/java/) からダウンロードしてください。  
3. **サンプル PSD ファイル** – 例: `sample.psd` をコードから参照できるフォルダーに配置します。

## パッケージのインポート

まず、必要なクラスをインポートします。回転角度に関係なくインポートは同じです。

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## 手順ガイド

### 手順 1: ドキュメントディレクトリの定義

ソース PSD が格納され、出力が書き込まれるフォルダーを設定します。

```java
String dataDir = "Your Document Directory";
```

> **プロのコツ:** 絶対パスまたは `System.getProperty("user.dir")` を使用して、相対パスの予期せぬ問題を回避してください。

### 手順 2: ソースおよび出力ファイルパスの指定

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "RotatingImageOnSpecificAngle_out.jpg";
```

出力のニーズに応じて、`destName` を任意のサポート拡張子（`.png`、`.tiff` など）に変更できます。

### 手順 3: 画像の読み込み

```java
RasterImage image = (RasterImage)Image.load(sourceFile);
```

`Image.load` はファイル形式を自動検出し、ラスタベースの操作用に具体的な `RasterImage` を返します。

### 手順 4: 画像データのキャッシュ（任意だが推奨）

```java
if (!image.isCached())
{
    image.cacheData();
}
```

キャッシュは画像ピクセルをメモリに保持し、以降の変換処理を高速化します。特に大きな PSD ファイルで有効です。

### 手順 5: 画像の回転

```java
image.rotate(20f, true, Color.getRed());
```

- **20f** – 度数（float）で指定する回転角度です。この値を変更して任意の角度で回転できます。例: 反時計回りに回転させる場合は `-45f`。  
- **true** – 回転後の画像が収まるようにキャンバスを拡張し、元のアスペクト比を維持します。  
- **Color.getRed()** – 回転で生じた空白のコーナーを埋める背景色です。必要に応じて `Color.getWhite()` や任意のカスタムカラーに置き換えてください。

#### Java で角度指定で画像を回転

`rotate` メソッドは任意の浮動小数点値を受け取るため、`30f`、`90f`、`-15f` のように **画像を角度で回転** できます。正の値は時計回り、負の値は反時計回りです。

#### Aspose.PSD を使用した特定の角度で画像を回転

メソッドが `float` を受け取るため、グラフィックデザインのワークフローで正確に制御したい場合は `22.5f` のように **画像を特定の角度で回転** できます。

#### Java での画像回転サンプルまとめ

上記の手順は、ファイルの読み込みから回転後の保存まで、完全な **rotate image java** ワークフローを示しています。

### 手順 6: 結果の保存

```java
image.save(destName, new JpegOptions());
```

`JpegOptions` では品質や圧縮、その他 JPEG 固有の設定を制御できます。ロスレス出力が必要な場合は `PngOptions` に置き換えてください。

## よくある問題と解決策

| 問題 | 原因 | 対策 |
|------|------|------|
| **回転後の空白コーナー** | 背景色が指定されていない | `rotate` に `Color`（例: `Color.getWhite()`）を渡す。 |
| **大きな PSD でのメモリ不足エラー** | 画像がキャッシュされていない | 処理前に `image.cacheData()` を呼び出す。 |
| **角度の方向が正しくない** | 負の角度と正の角度の混同 | 時計回り回転には負の値を使用（または座標系に応じて逆） |
| **変更が保存されない** | `save` の呼び出し忘れ | 回転後に `image.save(...)` が実行されていることを確認する。 |

## よくある質問

**Q: Aspose.PSD for Java で透過画像を回転できますか？**  
A: はい。ライブラリはアルファチャンネルを保持します。透明なコーナーが必要な場合は不透明な背景色を指定しないでください。

**Q: 回転に対応している画像フォーマットに制限はありますか？**  
A: ありません。Aspose.PSD は PSD、JPEG、PNG、TIFF、GIF、BMP、JPEG2000、WMF、EMF など多数をサポートしています。

**Q: 負の角度で画像を回転できますか？**  
A: もちろんです。負の `float`（例: `-30f`）を `rotate` に渡すと時計回りに回転します。

**Q: 回転中にリアルタイムの画像プレビューは提供されますか？**  
A: API はサーバーサイド専用です。ライブプレビューが必要な場合は、回転後のビットマップを Swing や JavaFX などの UI フレームワークに統合し、ビューを更新してください。

**Q: Aspose.PSD のコミュニティフォーラムはありますか？**  
A: はい、[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34) で質問や情報共有ができます。

## 結論

これで Aspose.PSD for Java を使用して特定の角度で画像ファイルを **回転させる方法** が分かりました。キャッシュ、背景色制御、柔軟な出力オプションを活用すれば、任意の Java ベースの画像ワークフローに正確な回転機能を組み込むことができます。

---

**最終更新日:** 2026-02-12  
**テスト環境:** Aspose.PSD for Java 24.11 (執筆時点での最新)  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}