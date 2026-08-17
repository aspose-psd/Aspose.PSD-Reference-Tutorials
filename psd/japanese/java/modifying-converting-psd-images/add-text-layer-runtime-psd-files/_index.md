---
date: 2026-03-07
description: Java と Aspose.PSD を使用して、実行時に PSD ファイルにテキストを追加する方法を学びましょう。このステップバイステップガイドに従って、PSD
  にテキストレイヤーをすばやく作成できます。
linktitle: Add Text Layer on Runtime in PSD Files using Java
second_title: Aspose.PSD Java API
title: Javaを使用して実行時にPSDファイルにテキストを追加する
url: /ja/java/modifying-converting-psd-images/add-text-layer-runtime-psd-files/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Javaで実行時にPSDファイルへテキストを追加する

## はじめに
Photoshop のドキュメントを手動で編集したことがある方は、レイヤーの威力をご存知でしょう。Java アプリケーションから **PSD にテキストを自動で追加** できたらどうでしょうか？Aspose.PSD for Java ライブラリを使えば、実行時に PSD にテキストレイヤーを作成でき、バッチ処理や動的グラフィック生成、ブランド化の自動化ワークフローへの扉が開きます。このチュートリアルでは、プロジェクトのセットアップから更新ファイルの保存まで、全工程を順を追って解説します。

## クイック回答
- **必要なライブラリは？** Aspose.PSD for Java。  
- **既存の PSD にテキストを追加できるか？** はい – ファイルを読み込み、`TextLayer` を追加して保存するだけです。  
- **本番環境でライセンスは必要か？** 評価版以外で使用する場合は商用ライセンスが必要です。  
- **対応している Java バージョンは？** JDK 8 以降（最新の LTS を推奨）。  
- **Web バックエンドでも使えるか？** もちろん – API はあらゆる Java ベースのサーバ環境で動作します。

## 「PSD にテキストを追加する」とは？
PSD にテキストを追加するとは、プログラムから Photoshop ドキュメント内に新しいテキストレイヤーを作成することです。このレイヤーは通常の Photoshop テキストレイヤーと同様に扱え、移動や内容の編集、スタイリングが可能です – Photoshop を開く必要はありません。

## Java で PSD にテキストレイヤーを作成するメリット
- **自動化** – マーケティング資産、透かし、商品ラベルなどを一括生成。  
- **一貫性** – 数千ファイルでも同じフォント・サイズ・位置を保証。  
- **統合** – 他の Java サービス（e‑コマース、レポーティング、CI パイプライン）と組み合わせて、オンザフライでグラフィックを提供。

## 前提条件
コードを書く前に、以下を準備してください。

1. **Java Development Kit (JDK)** – JDK 8 以上をインストールします。[こちらからダウンロード](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)。  
2. **Aspose.PSD for Java** – 最新の JAR を [Aspose リリースページ](https://releases.aspose.com/psd/java/) から取得。  
3. **IDE（任意）** – IntelliJ IDEA、Eclipse、またはお好みのエディタ。  
4. **Java の基礎知識** – クラス、オブジェクト、ファイル I/O に慣れていること。  
5. **サンプル PSD** – 本ガイドでは `OneLayer.psd` を使用します。任意のフォルダに配置してください。

## パッケージのインポート
まず、PSD ファイルとテキストレイヤーを操作するために必要なクラスをインポートします。

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
```

これらのインポートにより、Aspose.PSD のコア機能が利用可能になります。

## 手順ガイド

### 手順 1: ドキュメントディレクトリの設定
ソース PSD が格納されているフォルダと、出力先フォルダを定義します。

```java
String dataDir = "Your Document Directory"; 
```

`"Your Document Directory"` を、ファイルが存在する絶対パスまたは相対パスに置き換えてください。

### 手順 2: ソース PSD ファイルの読み込み
`Image.load()` を使って既存の PSD をメモリに読み込みます。

```java
String sourceFileName = dataDir + "OneLayer.psd"; 
Image img = Image.load(sourceFileName);
```

パスが正しければ、`img` がロードされた Photoshop ドキュメントを表します。

### 手順 3: `PsdImage` へキャスト
Photoshop 固有の機能を使用するため、汎用 `Image` を `PsdImage` にキャストします。

```java
PsdImage im = (PsdImage)img;
```

キャストにより `addTextLayer()` などのメソッドが利用可能になります。

### 手順 4: テキストレイヤー用矩形の定義
新しいテキストが表示される位置とサイズを指定します。矩形は (x, y) と (width, height) で構成されます。

```java
Rectangle rect = new Rectangle(
    (int)(im.getWidth() * 0.25),
    (int)(im.getHeight() * 0.25),
    (int)(im.getWidth() * 0.5),
    (int)(im.getHeight() * 0.5)
);
```

レイアウトに合わせて計算式を自由に調整してください。

### 手順 5: テキストレイヤーの追加
定義した矩形内に実際のテキストレイヤーを作成します。

```java
TextLayer layer = im.addTextLayer("Added text", rect);
```

`"Added text"` を、PSD に表示したい文字列に置き換えてください。ここで **プログラムからテキストレイヤー PSD を作成** します。

### 手順 6: 更新した PSD ファイルの保存
元のファイルを上書きしないよう、新しいファイル名で保存します。

```java
String psdPath = dataDir + "ImageWithTextLayer.psd";
im.save(psdPath);
```

実行後、ターゲットフォルダに `ImageWithTextLayer.psd` が生成され、テキストレイヤーが追加された状態になります。

## よくある問題と対策
| 問題 | 原因 | 対策 |
|------|------|------|
| **`NullPointerException` が `im.addTextLayer` で発生** | PSD が正しく読み込めていない（パスが間違っている） | `sourceFileName` が実在する PSD を指しているか確認 |
| **テキストが表示されない** | 矩形がキャンバス外、またはレイヤーが非表示 | 矩形座標を調整、または `layer.setVisible(true)` で可視化 |
| **LicenseException** | 本番環境で有効なライセンスなしで使用 | 商用ライセンスを取得し、`License license = new License(); license.setLicense("Aspose.PSD.lic");` で設定 |

## FAQ

**Q: 複数のテキストレイヤーを追加できますか？**  
A: はい – テキストを挿入したい分だけ手順 4 と 5 を繰り返してください。

**Q: テキストのスタイル（フォント、サイズ、色）はどう変更しますか？**  
A: `TextLayer` クラスの `getTextData()` メソッドで `Font`、`FontSize`、`Color` などを設定できます。詳細は Aspose.PSD API ドキュメントをご参照ください。

**Q: 既に多数のレイヤーがある PSD でも大丈夫ですか？**  
A: Aspose.PSD は複雑なレイヤー構造に対応しています。特定のグループを対象にしたり、`addTextLayer` のオーバーロードで挿入位置を指定できます。

**Q: Web アプリケーションでの利用は可能ですか？**  
A: 全く問題ありません。サーバ上で Java が動作していれば、オンザフライで PSD を生成・変更し、クライアントに配信できます。

**Q: 問題が発生した場合、どこでサポートを受けられますか？**  
A: [Aspose サポートフォーラム](https://forum.aspose.com/c/psd/34) でコミュニティや Aspose エンジニアに質問できます。

## 結論
これで、Java と Aspose.PSD を使って実行時に **PSD にテキストを追加** する方法が分かりました。この手法により、グラフィック作成の自動化、資産のパーソナライズ、Photoshop レベルの編集を任意の Java ベースソリューションに組み込むことが可能です。さらに、シェイプやラスターレイヤーの追加、フィルター適用など、Aspose.PSD API の他機能もぜひ探求してみてください。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最終更新日:** 2026-03-07  
**テスト環境:** Aspose.PSD for Java 24.12（執筆時点の最新）  
**作者:** Aspose  

---