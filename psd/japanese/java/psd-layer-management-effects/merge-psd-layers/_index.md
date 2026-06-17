---
date: 2026-04-05
description: Aspose.PSD for Java を使用して、PSD を PNG にエクスポートし、PSD レイヤーを結合する方法を学びます。PSD
  を JPEG に変換する方法、JPEG の品質設定、PSD から TIFF への変換のヒントも含まれています。
keywords:
- export psd to png
- convert psd to jpeg
- how to merge psd
- set jpeg quality
- psd to tiff conversion
linktitle: Aspose.PSD for Java を使用して PSD を PNG にエクスポートし、レイヤーを結合する
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java を使用して PSD を PNG にエクスポートし、レイヤーを結合する
url: /ja/java/psd-layer-management-effects/merge-psd-layers/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java を使用した PSD の PNG へのエクスポートとレイヤーの結合

## はじめに

グラフィックデザイナーが Photoshop で複雑なレイヤー画像を実現する方法を不思議に思ったことはありませんか？その秘密はしばしば **exporting PSD to PNG** とレイヤーを賢く結合することにあります。Java で PSD ファイルを扱っているなら、これらのテクニックをマスターすることで、合成画像を作成し、ファイルサイズを削減し、Web やモバイル向けのアセットを準備できます。このチュートリアルでは Aspose.PSD for Java を使用して **how to merge PSD** レイヤーを実行する方法を順を追って説明し、結果を PNG（必要に応じて JPEG/TIFF）にエクスポートする方法も示します。最後まで読むと、Java アプリケーションから直接レイヤー管理とエクスポートのワークフローを自動化できるようになります。

## クイック回答
- **Java で PSD ファイルを扱うライブラリは何ですか？** Aspose.PSD for Java.  
- **PSD を PNG にエクスポートできますか？** はい – 適切な画像オプションを設定するだけです。  
- **複数のレイヤーをどのように結合しますか？** PSD をロードし、`Layer` コレクションを操作してから保存します。  
- **JPEG の品質制御が必要な場合はどうすればよいですか？** `JpegOptions` を使用し、品質を設定します（0‑100）。  
- **Photoshop は必要ですか？** いいえ、Aspose.PSD は Adobe ソフトウェアとは独立して動作します。

## export PSD to PNG とは何ですか？

Exporting PSD to PNG とは、Photoshop ドキュメント（PSD）をポータブルネットワークグラフィックス（PNG）ファイルに変換し、必要に応じてレイヤーをフラット化または結合することを指します。PNG は透過性を保持し、Web で広くサポートされているため、UI アセットの人気フォーマットです。

## プログラムで PSD レイヤーを結合する理由

- **Automation（自動化）:** 手動クリックなしで数百ファイルをバッチ処理します。  
- **Performance（パフォーマンス）:** 結合されたレイヤーは下流アプリケーションの描画時間を短縮します。  
- **File size（ファイルサイズ）:** 不要なレイヤーをフラット化すると最終画像が小さくなります。  
- **Consistency（一貫性）:** ビルド間で同じレイヤー順序とブレンドを保証します。

## 前提条件

1. **Aspose.PSD for Java Library** – [Aspose.PSD for Java ダウンロードリンク](https://releases.aspose.com/psd/java/) からダウンロードしてください。  
2. **Java Development Environment** – IntelliJ IDEA、Eclipse、またはお好みの IDE。  
3. **Sample PSD File** – 複数レイヤーを含むファイル（例: `layers.psd`）。  
4. **Basic Java Knowledge** – クラスやメソッドに慣れていることが必要です。  
5. **Aspose Temporary License (Optional)** – 大きなファイルやトライアル制限を解除するために、[temporary license](https://purchase.aspose.com/temporary-license/) を取得してください。  

## パッケージのインポート

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.JpegOptions;
```

## ステップバイステップガイド

### 手順 1: PSD ファイルの読み込み

```java
String dataDir = "Your Document Directory";
PsdImage psdImage = (PsdImage)Image.load(dataDir + "layers.psd");
```

> このコードは `layers.psd` を `PsdImage` オブジェクトに読み込み、レイヤーへのフルアクセスを提供します。

### 手順 2: レイヤーの検査 (how to merge psd)

```java
Layer[] layers = psdImage.getLayers();
System.out.println("Total layers: " + layers.length);

for (Layer layer : layers) {
    System.out.println("Layer name: " + layer.getName());
}
```

> レイヤー名を確認することで、フラット化するか別々に保持するかを判断できます。

### 手順 3: 画像オプションの設定 (set jpeg quality)

```java
JpegOptions jpgOptions = new JpegOptions();
jpgOptions.setQuality(80); // Set the quality of the JPEG image (0-100)
```

> PNG や TIFF を使用したい場合は、`JpegOptions` を `PngOptions` または `TiffOptions` に置き換えることができます – ここで **psd to tiff conversion** が設定されます。

### 手順 4: 結合画像の保存 (export psd to png)

```java
psdImage.save(dataDir + "MergePSDlayers_output.png", jpgOptions);
```

> `save` メソッドは結合結果を `MergePSDlayers_output.png` に書き込みます。  
> *Tip:* PNG にエクスポートするには、`jpgOptions` を `PngOptions` インスタンスに置き換えてください。コードの残りは同じです。

## よくある問題と解決策

- **File‑not‑found exception（ファイルが見つからない例外）:** `dataDir` がパス区切り文字（`/` または `\\`）で終わっていること、そして `layers.psd` が存在することを確認してください。  
- **Unexpected colors after merge（結合後の予期しない色）:** レイヤーのブレンドモードが互換性があるか確認し、`layer.setBlendMode(...)` で調整できます。  
- **Large output file（出力ファイルが大きい）:** JPEG の品質を下げるか、PNG の圧縮レベルを使用してサイズを削減してください。

## よくある質問

**Q: JPEG 以外の形式で結合画像を保存できますか？**  
A: もちろんです！Aspose.PSD は PNG、BMP、TIFF などをサポートしています。対応するオプションクラス（`PngOptions`、`BmpOptions`、`TiffOptions`）を使用してください。

**Q: 出力形式ごとに画像品質を調整するにはどうすればよいですか？**  
A: 各オプションクラスは独自の品質/圧縮設定を提供します。JPEG では `setQuality(int)` を使用し、PNG では `CompressionLevel` を制御できます。

**Q: Aspose.PSD for Java を使用するのに Photoshop をインストールする必要がありますか？**  
A: いいえ。Aspose.PSD は Adobe Photoshop とは独立して動作するため、任意のサーバーや CI 環境で実行できます。

**Q: 保存前に画像オプションを設定しなかった場合はどうなりますか？**  
A: ライブラリはデフォルト設定（例: JPEG 品質 75）を適用します。オプションを指定することで最終出力を制御できます。

**Q: PSD を直接 TIFF に一括変換できますか？**  
A: はい – `TiffOptions` をインスタンス化し、`psdImage.save("output.tiff", tiffOptions);` を呼び出します。

---

**最終更新日:** 2026-04-05  
**テスト環境:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}