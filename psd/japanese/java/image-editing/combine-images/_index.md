---
date: 2025-12-30
description: Aspose.PSD を使用して 2 つの画像を組み合わせ、Java で PSD ファイルを作成する方法を学びましょう。ステップバイステップのガイドに従って、画像をすばやく
  PSD ファイルに結合できます。
linktitle: Combine Images
second_title: Aspose.PSD Java API
title: JavaでPSDファイルを作成する方法 – Aspose.PSDで画像を結合
url: /ja/java/image-editing/combine-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD ファイルを Java で作成 – Aspose.PSD を使用した画像結合

## はじめに

複数の画像をマージして **Java で PSD ファイルを作成** したい場合、Aspose.PSD を使えば作業がシンプルになります。このチュートリアルでは、2 つの画像を 1 つの PSD キャンバスに結合する手順を解説し、なぜこの方法が有用かを説明し、すぐに実行できるコードを提供します。最後まで読むと、**Java スタイルで画像を結合** し、プロフェッショナルなレイヤー構造のファイルを生成できるようになります。

## クイック回答
- **画像を PSD に結合するのに最適なライブラリは？** Aspose.PSD for Java。  
- **実装にかかる時間は？** 基本的な結合で約 10〜15 分。  
- **ライセンスは必要ですか？** テスト用の無料トライアルは利用可能です。商用利用には有償ライセンスが必要です。  
- **2 つ以上の画像を追加できますか？** はい – 追加のレイヤーごとに `drawImage` 呼び出しを繰り返します。  
- **対応している Java バージョンは？** Java 8 以降。

## 前提条件

作業を始める前に、以下を用意してください。

1. **Aspose.PSD ライブラリ** – [こちら](https://releases.aspose.com/psd/java/) からダウンロード。  
2. **Java Development Kit (JDK)** – Java 8 以上を推奨。  
3. **ドキュメントディレクトリ** – ソース画像と生成される PSD を保存するローカルフォルダー。

## パッケージのインポート

プロジェクトに必要な Aspose.PSD クラスをインポートします。

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

## 手順ガイド

### 手順 1: PSD オプションの作成（ファイル設定）

まず、出力設定を保持する `PsdOptions` インスタンスを作成します。

```java
PsdOptions imageOptions = new PsdOptions();
```

### 手順 2: FileCreateSource の設定（保存先の指定）

`FileCreateSource` をオプションに割り当て、結果ファイルの保存先を指定します。

```java
imageOptions.setSource(new FileCreateSource(dataDir + "Two_images_result_out.psd", false));
```

### 手順 3: Image インスタンスの作成（キャンバスサイズの初期化）

`Image` オブジェクトをオプションと共に作成し、600 × 600 ピクセルのキャンバスを指定します。

```java
Image image = Image.create(imageOptions, 600, 600);
```

### 手順 4: Graphics の初期化と最初の画像描画

`Graphics` オブジェクトでキャンバスに描画します。背景を白でクリアし、左半分に最初の画像を描画します。

```java
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
graphics.drawImage(Image.load(dataDir + "example1.psd"), 0, 0, 300, 600);
```

### 手順 5: 2 番目の画像を描画（結合完了）

同じキャンバスの右半分に 2 番目の画像を配置します。

```java
graphics.drawImage(Image.load(dataDir + "example2.psd"), 300, 0, 300, 600);
```

### 手順 6: 結合した PSD ファイルの保存

最後に、結合したキャンバスをディスクに保存します。

```java
image.save();
```

おめでとうございます！ **画像を PSD に結合** し、Java で PSD ファイルを作成できました。

## Aspose.PSD で画像を結合するメリット

- **レイヤー対応** – 各 `drawImage` 呼び出しが別々のレイヤーとして追加され、後から編集可能。  
- **フォーマットの柔軟性** – PSD、PNG、JPEG、BMP など多数の形式をサポート。  
- **ネイティブ依存なし** – 純粋な Java 実装で、JDK が動作する OS ならどこでも利用可能。  

## よくある問題と対策

| 問題 | 原因 | 解決策 |
|------|------|--------|
| `File not found` エラーが発生する | `dataDir` パスが誤っている | `dataDir` が `example1.psd` と `example2.psd` を含むフォルダーを指しているか確認 |
| 出力 PSD が空白になる | `graphics.clear` が描画後に呼び出されている | `graphics.clear(Color.getWhite())` を **すべての `drawImage` 呼び出しの前** に実行 |
| 実行時にライセンス例外が出る | Aspose.PSD のライセンスが未設定または期限切れ | API 呼び出し前に `License license = new License(); license.setLicense("Aspose.PSD.lic");` で有効なライセンスを適用 |

## FAQ

### Q1: Aspose.PSD はすべての画像形式に対応していますか？
A1: 主に PSD 形式に特化していますが、入力・出力に多数の他形式もサポートしています。

### Q2: 結合した画像にさらに加工を加えることはできますか？
A2: もちろんです。画像を結合した後、Aspose.PSD の豊富な機能で PSD を自由に操作できます。

### Q3: Aspose.PSD の使用にはライセンスが必要ですか？
A3: 商用利用には有効なライセンスが必要です。購入は [こちら](https://purchase.aspose.com/buy) から。

### Q4: 無料トライアルはありますか？
A4: はい、無料トライアルは [こちら](https://releases.aspose.com/) から利用できます。

### Q5: Aspose.PSD に関する質問はどこでサポートを受けられますか？
A5: コミュニティサポートやディスカッションは [Aspose.PSD フォーラム](https://forum.aspose.com/c/psd/34) をご利用ください。

---

**最終更新日:** 2025-12-30  
**テスト環境:** Aspose.PSD 24.11 for Java  
**作成者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}