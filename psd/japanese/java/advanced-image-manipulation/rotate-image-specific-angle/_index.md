---
date: 2025-12-08
description: Aspose.PSD を使用して Java で画像を特定の角度に回転させる方法を学びましょう。このガイドでは、rotate image java、rotate
  image specific angle、背景処理などについて解説しています。
linktitle: How to Rotate Image on a Specific Angle
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java を使用して特定の角度で画像を回転する方法
url: /ja/java/advanced-image-manipulation/rotate-image-specific-angle/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java で特定の角度に画像を回転する方法

## はじめに

Java アプリケーションで **画像の回転方法** をプログラム的に実装したい場合、Aspose.PSD for Java は高性能で使いやすい API を提供し、重い処理を代行してくれます。写真エディタの構築、サムネイル生成、Web サービス向けのアセット準備など、正確な角度で画像を回転させる必要はよくある要件です。このチュートリアルでは、PSD ファイルの読み込みから回転後の保存までの全工程を解説し、キャッシュやバックグラウンド処理といったベストプラクティスも併せて紹介します。

> **クイック回答**  
> - **Java で画像を回転させるのに最適なライブラリは？** Aspose.PSD for Java。  
> - **任意の角度で回転できるか？** はい、`rotate` メソッドは `float` 型の角度（正負どちらも可）を受け取ります。  
> - **開発時にライセンスは必要か？** 無料トライアルでテスト可能です。商用利用にはライセンスが必要です。  
> - **対応している画像形式は？** PSD、JPEG、PNG、TIFF、GIF、BMP など多数。  
> - **空白領域の背景色はどう設定するか？** `rotate` メソッドに `Color` インスタンスを渡します。

## Java における画像回転とは？

画像回転とは、ピクセルマトリックスを基準点（通常は中心）を中心に指定した角度だけ回転させることです。Java では `Graphics2D` を使って手動で実装できますが、Aspose.PSD は数学的計算を抽象化し、色深度の違いを処理し、PSD ファイルの場合はレイヤ情報も保持します。

## なぜ Aspose.PSD を画像回転に使うのか？

- **精度:** 任意の小数点以下の角度でも品質を損なわずに回転可能。  
- **パフォーマンス:** 組み込みキャッシュ (`image.cacheData()`) により大容量ファイルでも高速に処理。  
- **背景制御:** 回転で生じる空白領域を任意の背景色で埋められる。  
- **フォーマットの柔軟性:** PSD を読み込み、JPEG、PNG など任意のサポート形式で出力可能。

## 前提条件

作業を始める前に以下を用意してください。

1. **Java Development Kit (JDK 8 以上)** – 動作する Java IDE またはコマンドライン環境。  
2. **Aspose.PSD for Java** – 最新の JAR を [Aspose.PSD Java ページ](https://reference.aspose.com/psd/java/) からダウンロード。  
3. **サンプル PSD ファイル** – 例: `sample.psd` をコードから参照できるフォルダに配置。

## パッケージのインポート

まず、必要なクラスをインポートします。回転角度に関係なくインポートは同じです。

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## 手順ガイド

### 手順 1: ドキュメントディレクトリを定義

ソース PSD があるフォルダと出力先フォルダを設定します。

```java
String dataDir = "Your Document Directory";
```

> **プロのコツ:** 絶対パスまたは `System.getProperty("user.dir")` を使用して、相対パスによる予期せぬ動作を回避しましょう。

### 手順 2: ソースと出力ファイルのパスを指定

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "RotatingImageOnSpecificAngle_out.jpg";
```

`destName` は必要に応じて `.png`、`.tiff` など任意のサポート拡張子に変更できます。

### 手順 3: 画像を読み込む

```java
RasterImage image = (RasterImage)Image.load(sourceFile);
```

`Image.load` はファイル形式を自動判別し、ラスタベースの操作に適した `RasterImage` を返します。

### 手順 4: 画像データをキャッシュ（任意だが推奨）

```java
if (!image.isCached())
{
    image.cacheData();
}
```

キャッシュは画像ピクセルをメモリに保持し、後続の変換処理を高速化します。特に大きな PSD ファイルで有効です。

### 手順 5: 画像を回転

```java
image.rotate(20f, true, Color.getRed());
```

- **20f** – 回転角度（度、float）。任意の角度に変更可能です。例: 反時計回りに `-45f`。  
- **true** – キャンバスを拡張して回転後の画像全体が収まるようにし、アスペクト比を維持します。  
- **Color.getRed()** – 回転で生じた空白コーナーを埋める背景色。必要に応じて `Color.getWhite()` やカスタムカラーに置き換えてください。

### 手順 6: 結果を保存

```java
image.save(destName, new JpegOptions());
```

`JpegOptions` で品質や圧縮設定など JPEG 固有のオプションを制御できます。ロスレス出力が必要な場合は `PngOptions` に差し替えてください。

## よくある問題と対策

| 問題 | 原因 | 対策 |
|------|------|------|
| **回転後に空白が黒くなる** | 背景色が指定されていない | `rotate` に `Color`（例: `Color.getWhite()`）を渡す。 |
| **大容量 PSD でメモリ不足エラー** | 画像がキャッシュされていない | 処理前に `image.cacheData()` を呼び出す。 |
| **角度の向きが期待と逆** | 正負の角度の取り違え | 時計回りは負の値、反時計回りは正の値（座標系に依存）を使用。 |
| **変更が保存されない** | `save` 呼び出しを忘れている | 回転後に必ず `image.save(...)` を実行する。 |

## FAQ

**Q: Aspose.PSD for Java で透過画像を回転できますか？**  
A: はい。アルファチャンネルは保持されます。透明なコーナーが必要な場合は不透明な背景色を指定しないでください。

**Q: 回転に対応していない画像形式はありますか？**  
A: ありません。Aspose.PSD は PSD、JPEG、PNG、TIFF、GIF、BMP、JPEG2000、WMF、EMF など多数の形式をサポートしています。

**Q: 負の角度で回転できますか？**  
A: もちろんです。`rotate` に負の float（例: `-30f`）を渡すと時計回りに回転します。

**Q: 回転中にリアルタイムプレビューは可能ですか？**  
A: API はサーバーサイド専用です。ライブプレビューが必要な場合は、回転後のビットマップを Swing や JavaFX などの UI フレームワークに組み込み、ビューを更新してください。

**Q: Aspose.PSD のコミュニティフォーラムはありますか？**  
A: はい、[Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34) で質問や情報共有ができます。

## まとめ

これで **Aspose.PSD for Java** を使って特定の角度で画像を回転させる方法が分かりました。キャッシュ活用、背景色制御、柔軟な出力オプションを組み合わせることで、あらゆる Java ベースの画像ワークフローに正確な回転機能を組み込めます。

---

**最終更新日:** 2025-12-08  
**テスト環境:** Aspose.PSD for Java 24.11（執筆時点の最新バージョン）  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}