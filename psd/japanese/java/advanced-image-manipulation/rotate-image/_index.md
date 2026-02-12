---
date: 2026-02-12
description: Aspose.PSD for Java を使用して画像の回転方法と 270 度回転方法を学びます。このガイドでは、PSD ファイルの回転、画像のフリップ、Photoshop
  を使わずに PSD を JPEG に変換する方法をカバーしています。
linktitle: Rotate Image 270 Degrees
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java を使用した画像の270度回転方法
url: /ja/java/advanced-image-manipulation/rotate-image/
weight: 19
---

 final output.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Javaで画像を270度回転する

## はじめに

この **java image processing tutorial** では、Aspose.PSD for Java を使用して **how to rotate image** を 270 度素早く確実に実行する方法を紹介します。写真編集ツールの構築、バッチ変換の自動化、または PSD レイヤーの向き変更が必要な場合でも、ライブラリは作業を簡単にします。また、**flip image java** のテクニックや、回転した PSD を JPEG に変換する方法にも触れ、Photoshop を使わない完全なエンドツーエンドのワークフローを提供します。

## クイック回答
- **回転を処理するライブラリは何ですか？** Aspose.PSD for Java  
- **例で使用されている回転角度は何度ですか？** 270 degrees  
- **画像もフリップできますか？** はい – `RotateFlipType` のオプション（例: `Rotate90FlipX`）を使用します。  
- **結果はどのように保存しますか？** 例では `JpegOptions` を使用して JPEG として保存しています。  
- **本番環境でライセンスは必要ですか？** 商用利用には有効な Aspose.PSD ライセンスが必要です  

## 「画像を270度回転する」とは？

画像を 270 度回転するとは、画像を時計回りに 3/4 回転（または反時計回りに 90 度）させることを意味します。多くのグラフィック編集シナリオでは、この向きは一連の変換の後に元の縦向きレイアウトと一致します。

## このタスクに Aspose.PSD を使用する理由

- **フル PSD サポート** – レイヤー、マスク、調整オブジェクトに対応。  
- **Photoshop が不要** – 任意の Java ランタイムで実行可能。  
- **シンプルな API** – 単一メソッド呼び出し (`rotateFlip`) で回転とフリップを処理。  
- **簡単なフォーマット変換** – JPEG、PNG、その他一般的なフォーマットへ直接エクスポート。  

## Aspose.PSD for Javaで画像を回転する方法
以下に、PSD を読み込み、270° 回転を適用し、必要に応じて画像をフリップし、最終的に JPEG として保存するまでのステップバイステップガイドを示します。

### 前提条件

開始する前に、以下が揃っていることを確認してください。

- **Aspose.PSD for Java** ライブラリがインストールされていること。ダウンロードと完全な API リファレンスは [here](https://reference.aspose.com/psd/java/) から確認できます。  
- Java 開発環境 (JDK 8 以上)。  
- 回転させたいサンプル PSD ファイル。コード内の `sourceFile` 変数を実際のファイルパスに更新してください。

### パッケージのインポート

まず、Aspose.PSD パッケージから必要なクラスをインポートします。

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

### 手順 1: 画像の読み込み

`Image` インスタンスを作成し、ソース PSD ファイルを指すようにします。

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

### 手順 2: 画像を 270 度回転する

`rotateFlip` メソッドに `RotateFlipType.Rotate270FlipNone` を指定して、フリップなしで 270 度回転させます。

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **プロのコツ:** 画像を水平または垂直にフリップする必要がある場合は、`Rotate90FlipX` や `Rotate180FlipY` などの別の `RotateFlipType` を選択してください。これは **flip image java** 操作で最も一般的な方法です。

### 手順 3: PSD を JPEG に変換して保存

回転後、適切なオプションクラスを使用して **convert PSD to JPEG**（または他のサポート形式）に変換できます。

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

ファイル `RotatedImage_out.jpg` には、元の PSD コンテンツが 270 度回転され、JPEG として保存されたものが含まれます。

## なぜ重要か – 実際のユースケース

- **製品カタログのバッチ処理** – 公開前に多数の PSD アセットを統一された向きに回転させます。  
- **自動サムネイル生成** – Photoshop を開かずに、ウェブギャラリー用に正しい向きのプレビューを作成します。  
- **モバイルアプリのバックエンド** – 純粋な Java でサーバー側でユーザーがアップロードした PSD ファイルの向きを再調整します。  

## よくある落とし穴とトラブルシューティング

| 問題 | 解決策 |
|------|--------|
| **画像が上下逆になる** | `Rotate270FlipNone` を使用したことを確認してください。時計回りに 90 度回転させる場合は `Rotate90FlipNone` を使用します。 |
| **出力ファイルが破損している** | 出力先フォルダーが存在し、書き込み権限があることを確認してください。 |
| **ライセンス例外** | 本番環境で画像をロードする前に、臨時または永続的な Aspose.PSD ライセンスをインストールしてください。 |
| **Photoshop なしで画像を回転する必要がある** | この API はコードのみで回転を実行し、Photoshop への依存を排除します。 |
| **同じ操作で画像をフリップしたい** | `Rotate90FlipX` などの他の `RotateFlipType` 値を使用してください（**how to flip image** をカバーします）。 |

## よくある質問

**Q: Aspose.PSD はさまざまな画像フォーマットに対応していますか？**  
A: はい、Aspose.PSD は PSD、JPEG、PNG、BMP、GIF、その他多数のラスターフォーマットをサポートしています。

**Q: 事前定義されたフリップだけでなく、カスタム回転を適用できますか？**  
A: もちろんです！`RotateFlipType` は一般的な角度を提供しますが、複数の呼び出しを組み合わせたり、変換行列を使用して任意の角度を実現できます。

**Q: 回転した PSD を PNG など別のフォーマットに変換するにはどうすればよいですか？**  
A: `save` メソッドで `JpegOptions` を `PngOptions`（または適切なオプションクラス）に置き換えてください。

**Q: 追加のサポートや支援はどこで得られますか？**  
A: コミュニティのサポートは [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34) をご覧ください。

**Q: 無料トライアルは利用できますか？**  
A: はい、[無料トライアル](https://releases.aspose.com/) で Aspose.PSD をお試しいただけます。

**Q: 一時ライセンスはどのように取得できますか？**  
A: 一時ライセンスが必要な場合は、[こちら](https://purchase.aspose.com/temporary-license/) から取得できます。

**Q: この方法はヘッドレスサーバーでも動作しますか？**  
A: はい、Aspose.PSD for Java は標準的な JVM 環境で動作するため、CI/CD パイプラインやクラウド関数に最適です。

## 結論

これで、Aspose.PSD for Java を使用して画像を 270 度回転させる **how to rotate image** の方法、必要に応じて **flip image** する方法、そして結果を JPEG にエクスポートする方法を学びました。このシンプルなワークフローは、より大規模な Java ベースの画像処理パイプラインに組み込むことができ、Photoshop に依存せずに PSD 操作を完全にコントロールできます。

**最終更新日:** 2026-02-12  
**テスト環境:** Aspose.PSD for Java 24.12  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}