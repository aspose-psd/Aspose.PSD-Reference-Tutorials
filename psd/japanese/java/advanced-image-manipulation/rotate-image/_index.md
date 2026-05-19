---
date: 2026-05-19
description: Aspose.PSD for Java を使用して PSD を JPEG に変換し、画像を 270 度回転させる方法を学びます。このガイドでは、PSD
  ファイルの回転、画像の flip、そして PSD を JPEG に変換する方法を示します。
keywords:
- convert psd to jpeg
- how to rotate psd
- flip image java
- rotate psd layer
- rotate image without photoshop
linktitle: 画像を 270 度回転
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  headline: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  name: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  steps:
  - name: Load the PSD File
    text: '`Image` is Aspose.PSD''s core class that represents a single PSD document
      in memory. Instantiating it reads only the header information, keeping memory
      usage low.'
  - name: Rotate the Image 270 Degrees
    text: '`rotateFlip` performs the specified rotation and optional flip on the image.
      `RotateFlipType.Rotate270FlipNone` rotates the canvas 270 degrees clockwise
      while leaving the image orientation unchanged. > **Pro tip:** If you also need
      to flip the image horizontally or vertically, choose a different `Ro'
  - name: Convert PSD to JPEG and Save
    text: '`JpegOptions` defines JPEG‑specific parameters such as compression quality.
      The `save` method writes the transformed image to disk in the desired format.
      The file `RotatedImage_out.jpg` now contains the original PSD content rotated
      270 degrees and saved as a JPEG.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports PSD, JPEG, PNG, BMP, GIF, TIFF, and many other
      raster formats.
    question: Is Aspose.PSD compatible with different image formats?
  - answer: Absolutely! While `RotateFlipType` provides common angles, you can chain
      multiple calls or use transformation matrices for arbitrary angles.
    question: Can I apply custom rotations, not just predefined flips?
  - answer: Replace `JpegOptions` with `PngOptions` (or the appropriate options class)
      in the `save` method.
    question: How do I convert the rotated PSD to another format, such as PNG?
  - answer: For community help, visit the [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).
    question: Where can I find additional support or assistance?
  - answer: Yes, you can explore Aspose.PSD with a [free trial](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java を使用して PSD を JPEG に変換し、270° 回転させる
url: /ja/java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java を使用した PSD から JPEG への変換と画像の 270 度回転

## はじめに

この **Java image‑processing tutorial** では、Aspose.PSD for Java を使用して画像を 270 度回転させながら **PSD を JPEG に変換** する方法を学びます。バッチ処理パイプライン、Web ベースのエディタ、デスクトップユーティリティのいずれを構築していても、このライブラリを使用すれば Photoshop を使用せずに PSD レイヤーを操作できます。また、オプションのフリップについても説明し、PSD ファイルの読み込みから JPEG の保存までのエンドツーエンドのフロー全体を示します。

## クイック回答

- **回転を処理するライブラリは何ですか？** Aspose.PSD for Java  
- **例で使用されている回転角度は何度ですか？** 270 degrees  
- **画像をフリップすることもできますか？** Yes – use `RotateFlipType` options like `Rotate90FlipX`  
- **結果はどのように保存しますか？** In the example we save as JPEG using `JpegOptions`  
- **本番環境でライセンスが必要ですか？** A valid Aspose.PSD license is required for commercial use  

## 「画像を 270 度回転する」とは何ですか？

画像を 270 度回転するとは、画像を時計回りに 3/4 回転（または反時計回りに 90 度）させることを意味します。この向きは、以前の変換後に元の縦向きレイアウトを復元することが多く、風景モードで撮影された画像を縦向きで表示する必要がある場合に一般的に使用されます。結果として、品質を損なうことなく正しく向き付けされたビジュアルが得られます。

## このタスクに Aspose.PSD を使用する理由は？

Aspose.PSD は **50 以上の入力および出力フォーマット**（PSD、JPEG、PNG、BMP、GIF、TIFF など）をサポートし、**2 GB** までのファイルをドキュメント全体をメモリに読み込まずに処理できます。API は任意の Java ランタイム（JDK 8 以上）で動作し、ネイティブな Photoshop のインストールは不要です。また、`rotateFlip` の単一呼び出しで回転とフリップの両方を一度に処理できます。

## 前提条件

開始する前に、以下が揃っていることを確認してください。

- **Aspose.PSD for Java** ライブラリがインストールされていること。ダウンロードと完全な API リファレンスは [here](https://reference.aspose.com/psd/java/) で確認できます。  
- Java 開発環境（JDK 8 以上）。  
- 回転させたいサンプル PSD ファイル。コード内の `sourceFile` 変数をファイルの正しいパスに更新してください。

## パッケージのインポート

`Image`、`RotateFlipType`、`JpegOptions` クラスは、ファイルの読み込み、変換、保存に必要です。  
`Image` はメモリ上の PSD ドキュメントを表すコアクラスです。  
`RotateFlipType` はサポートされている回転およびフリップ操作を列挙します。  
`JpegOptions` は品質などの JPEG 出力設定を構成します。  

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## 回転後に PSD を JPEG に変換する方法

ソース PSD を読み込み、270 度回転を適用し、すぐに JPEG として保存します。この 3 ステップのフローは、一般的な 10 MP 画像でも最新の CPU で 1 秒未満で実行でき、高スループットのバッチジョブに最適です。必要な画像データのみを処理することでメモリ使用量は低く抑えられ、生成された JPEG はファイルサイズを削減しつつ視覚的忠実度を保持します。

### ステップ 1: PSD ファイルの読み込み

`Image` は Aspose.PSD のコアクラスで、メモリ上の単一 PSD ドキュメントを表します。インスタンス化するとヘッダー情報のみが読み込まれ、メモリ使用量が低く抑えられます。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

### ステップ 2: 画像を 270 度回転

`rotateFlip` は画像に対して指定された回転とオプションのフリップを実行します。`RotateFlipType.Rotate270FlipNone` はキャンバスを時計回りに 270 度回転させ、画像の向きは変更しません。

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **プロのコツ:** 画像を水平または垂直にフリップする必要がある場合は、`Rotate90FlipX` や `Rotate180FlipY` などの別の `RotateFlipType` を選択してください。

### ステップ 3: PSD を JPEG に変換して保存

`JpegOptions` は圧縮品質などの JPEG 固有のパラメータを定義します。`save` メソッドは変換された画像を指定された形式でディスクに書き込みます。

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

`RotatedImage_out.jpg` ファイルには、元の PSD コンテンツが 270 度回転され JPEG として保存されたものが含まれます。

## 一般的な問題と解決策

| 問題 | 解決策 |
|-------|----------|
| **画像が上下逆に表示される** | `Rotate270FlipNone` を使用したことを確認してください。時計回りに 90 度回転させる場合は `Rotate90FlipNone` を使用します。 |
| **出力ファイルが破損している** | 出力先フォルダーが存在し、書き込み権限があることを確認してください。 |
| **ライセンス例外** | 本番環境で画像を読み込む前に、臨時または永続的な Aspose.PSD ライセンスをインストールしてください。 |

## よくある質問

**Q: Aspose.PSD はさまざまな画像フォーマットに対応していますか？**  
A: はい、Aspose.PSD は PSD、JPEG、PNG、BMP、GIF、TIFF など多くのラスターフォーマットをサポートしています。

**Q: カスタム回転（事前定義されたフリップだけでなく）を適用できますか？**  
A: もちろんです！`RotateFlipType` は一般的な角度を提供しますが、複数の呼び出しをチェーンしたり、変換行列を使用して任意の角度を指定できます。

**Q: 回転した PSD を PNG など別の形式に変換するにはどうすればよいですか？**  
A: `save` メソッドで `JpegOptions` を `PngOptions`（または適切なオプションクラス）に置き換えてください。

**Q: 追加のサポートや支援はどこで得られますか？**  
A: コミュニティの支援は、[Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) をご覧ください。

**Q: 無料トライアルは利用できますか？**  
A: はい、[free trial](https://releases.aspose.com/) で Aspose.PSD をお試しできます。

**Q: 一時ライセンスはどのように取得できますか？**  
A: 一時ライセンスが必要な場合は、[here](https://purchase.aspose.com/temporary-license/) で取得できます。

---

**最終更新日:** 2026-05-19  
**テスト環境:** Aspose.PSD for Java 24.12  
**作者:** Aspose  

{{< blocks/products/products-backtop-button >}}

## 関連チュートリアル

- [Aspose.PSD for Java を使用した PSD をラスタ画像形式に変換](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [Java を使用して PSD を PNG に変換し、PSD ファイル内のレイヤーを回転](/psd/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/)
- [Aspose.PSD を使用した Java での画像回転方法](/psd/java/advanced-image-manipulation/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}