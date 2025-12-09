---
date: 2025-12-06
description: Aspose.PSD for Java を使用して画像を 270 度回転させる方法を学びましょう。このガイドでは、PSD ファイルの回転、画像のフリップ、PSD
  を JPEG に変換する方法を示します。
linktitle: Rotate Image 270 Degrees
second_title: Aspose.PSD Java API
title: Aspose.PSD for Javaで画像を270度回転させる方法
url: /ja/java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Javaで画像を270度回転する

## はじめに

この **java image processing tutorial** では、Aspose.PSD for Java を使用して **rotate image 270 degrees** を迅速かつ確実に行う方法をご紹介します。写真編集ツールの構築、バッチ変換の自動化、または PSD レイヤーの向き変更が必要な場合でも、このライブラリを使えば作業は簡単です。画像のフリップや回転した PSD を JPEG に変換する方法にも触れ、エンドツーエンドのワークフローを提供します。

## クイック回答
- **回転を処理するライブラリは何ですか？** Aspose.PSD for Java  
- **例で使用されている回転角度は何度ですか？** 270 degrees  
- **画像をフリップすることもできますか？** Yes – use `RotateFlipType` options like `Rotate90FlipX`  
- **結果はどのように保存しますか？** In the example we save as JPEG using `JpegOptions`  
- **本番環境でライセンスが必要ですか？** A valid Aspose.PSD license is required for commercial use  

## 「rotate image 270 degrees」とは何ですか？

画像を270度回転するとは、画像を時計回りに円の3/4回転させる（または反時計回りに90度回転させる）ことを意味します。多くのグラフィック編集シナリオでは、この向きは一連の変換後に元の縦向きレイアウトと一致します。

## なぜこのタスクに Aspose.PSD を使用するのか？

- **Full PSD support** – レイヤー、マスク、調整オブジェクトを含むフル PSD サポート。  
- **No native Photoshop required** – ネイティブの Photoshop は不要で、任意の Java ランタイムで実行可能。  
- **Simple API** – シンプルな API – 単一のメソッド呼び出し (`rotateFlip`) で回転とフリップを処理。  
- **Easy format conversion** – 簡単なフォーマット変換 – JPEG、PNG、その他の一般的なフォーマットへ直接エクスポート。  

## 前提条件

開始する前に、以下が揃っていることを確認してください：

- **Aspose.PSD for Java** ライブラリがインストールされていること。ダウンロードと完全な API リファレンスは [here](https://reference.aspose.com/psd/java/) で確認できます。  
- Java 開発環境 (JDK 8 以上)。  
- 回転させたいサンプル PSD ファイル。コード内の `sourceFile` 変数を実際のファイルパスに更新してください。

## パッケージのインポート

まず、Aspose.PSD パッケージから必要なクラスをインポートします。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## PSD の回転方法 – ステップ 1: 画像をロードする

`Image` インスタンスを作成し、ソース PSD ファイルを指すようにします。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## PSD の回転方法 – ステップ 2: 画像を270 度回転する

`rotateFlip` メソッドに `RotateFlipType.Rotate270FlipNone` を指定して、フリップなしで 270 度回転させます。

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **プロのコツ:** 画像を水平または垂直にフリップする必要がある場合は、`Rotate90FlipX` や `Rotate180FlipY` などの別の `RotateFlipType` を選択してください。

## PSD の回転方法 – ステップ 3: PSD を JPEG に変換して保存する

回転後、適切なオプションクラスを使用して **PSD を JPEG に変換**（または他のサポートされているフォーマット）できます。

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

ファイル `RotatedImage_out.jpg` には、元の PSD コンテンツが 270 度回転され、JPEG として保存されたものが含まれます。

## よくある問題と解決策

| 問題 | 解決策 |
|------|--------|
| **画像が逆さまに表示される** | `Rotate270FlipNone` を使用したことを確認してください。時計回りに90度回転させる場合は `Rotate90FlipNone` を使用します。 |
| **出力ファイルが破損している** | 出力先フォルダが存在し、書き込み権限があることを確認してください。 |
| **ライセンス例外** | 本番環境で画像をロードする前に、一時的または永続的な Aspose.PSD ライセンスをインストールしてください。 |

## よくある質問

**Q: Aspose.PSD はさまざまな画像フォーマットに対応していますか？**  
A: はい、Aspose.PSD は PSD、JPEG、PNG、BMP、GIF、その他多数のラスターフォーマットをサポートしています。

**Q: 事前定義されたフリップだけでなく、カスタム回転を適用できますか？**  
A: もちろんです！`RotateFlipType` は一般的な角度を提供しますが、複数回呼び出すか変換行列を使用して任意の角度に回転させることができます。

**Q: 回転した PSD を PNG など別のフォーマットに変換するにはどうすればよいですか？**  
A: `save` メソッドで `JpegOptions` を `PngOptions`（または適切なオプションクラス）に置き換えてください。

**Q: 追加のサポートや支援はどこで得られますか？**  
A: コミュニティのサポートは、[Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) をご覧ください。

**Q: 無料トライアルは利用できますか？**  
A: はい、[free trial](https://releases.aspose.com/) で Aspose.PSD をお試しいただけます。

**Q: 一時ライセンスはどのように取得できますか？**  
A: 一時ライセンスが必要な場合は、[here](https://purchase.aspose.com/temporary-license/) から取得できます。

## 結論

これで、Aspose.PSD for Java を使用して **rotate image 270 degrees** を行い、必要に応じて画像をフリップし、結果を JPEG にエクスポートする方法を学びました。このシンプルなワークフローは、より大規模な Java ベースの画像処理パイプラインに組み込むことができ、Photoshop に依存せずに PSD の操作を完全にコントロールできます。

---

**最終更新日:** 2025-12-06  
**テスト環境:** Aspose.PSD for Java 24.12  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}