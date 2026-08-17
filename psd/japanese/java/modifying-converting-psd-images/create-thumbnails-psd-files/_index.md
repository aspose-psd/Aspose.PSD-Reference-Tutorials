---
date: 2026-03-13
description: Aspose.PSD を使用した Java での PSD サムネイル作成方法を学びましょう。ステップバイステップのガイドに従って、PSD
  ファイルからサムネイルを迅速に生成できます。
linktitle: Create Thumbnails from PSD Files using Java
second_title: Aspose.PSD Java API
title: PSDサムネイル作成 Java – PSDからサムネイルを生成
url: /ja/java/modifying-converting-psd-images/create-thumbnails-psd-files/
weight: 24
---

 bullet lists.

Let's produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSDサムネイル作成 Java – PSDからサムネイルを生成

## はじめに
**PSDサムネイル作成 Java** のコードで Photoshop ファイルからプレビュー画像を抽出したい場合は、ここが最適です。デジタル資産管理システム、ウェブギャラリー、あるいは自動バッチ処理パイプラインを構築する際に、PSD ファイルからサムネイルを生成すれば、パフォーマンスとユーザー体験が大幅に向上します。このチュートリアルでは、Aspose.PSD for Java を使用して PSD を読み込み、埋め込まれたサムネイルリソースを取得し、個別の画像ファイルとして保存する手順をすべて解説します。

## クイック回答
- **PSDサムネイル抽出に最適なライブラリは？** Aspose.PSD for Java。  
- **実装にかかる時間は？** 基本的なセットアップで約 10〜15 分。  
- **Photoshop のインストールは必要？** いいえ、Aspose.PSD は単独で動作します。  
- **サムネイルをエクスポートできる画像形式は？** Aspose.PSD がサポートするすべての形式（例：BMP、PNG、JPEG）。  
- **本番環境でライセンスは必要？** はい、商用ライセンスが必要です。

## 「create PSD thumbnail Java」とは？
Java で PSD サムネイルを作成するとは、Photoshop ドキュメント（PSD）内に保存されているサムネイルプレビューをプログラムで読み取り、別の画像ファイルとして書き出すことを指します。これにより、サイズが大きくなることが多い PSD 本体を読み込むことなく、素早くプレビューを生成できます。

## なぜ Aspose.PSD を使うのか？
- **Photoshop 依存なし:** JDK があればどのプラットフォームでも動作。  
- **完全な PSD サポート:** すべての PSD バージョンとリソース（サムネイルを含む）に対応。  
- **シンプルな API:** 数行のコードでサムネイルの抽出と保存が可能。  
- **パフォーマンス最適化:** 大容量ファイルでも効率的にメモリを扱える。

## 前提条件
サムネイル作成の詳細に入る前に、必要な環境を確認しましょう。

### Java 開発環境
- **Java JDK:** コンピュータに Java Development Kit（JDK）がインストールされていることを確認してください。ダウンロードは [here](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)。  
- **IDE:** IntelliJ IDEA、Eclipse、NetBeans などの統合開発環境（IDE）を使用するとコーディングが楽になります。

### Aspose.PSD ライブラリ
- プロジェクトに Aspose.PSD ライブラリを組み込む必要があります。最新版は [download the latest version here](https://releases.aspose.com/psd/java/) から取得できます。

### Java の基本知識
- クラス、オブジェクト、ループなどの Java 基礎が分かっていると、サンプルコードをスムーズに理解できます。

## パッケージのインポート
まず、Aspose.PSD ライブラリから必要なクラスをインポートします。このステップは、ライブラリ機能をコードで利用できるようにするために必須です。

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.ThumbnailFormat;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

前提条件が整ったので、本題に入りましょう！ PSD ファイルからサムネイルを作成する手順はシンプルで、以下の流れで解説します。

## PSDサムネイル作成 Java – ステップバイステップガイド

### 手順 1: 環境のセットアップ
プロジェクトを開始し、サムネイル生成の準備を行います。

1. **Java プロジェクトを作成**  
   - IDE で新規 Java プロジェクトを作成します。  
   - プロジェクト名は `"PsdThumbnailGenerator"` など分かりやすい名前にします。

2. **Aspose.PSD ライブラリを組み込む**  
   - Aspose.PSD の JAR ファイルをプロジェクトのビルドパスに追加します。  
   - Maven を使用している場合は、`pom.xml` に以下を追加します。

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-psd</artifactId>
    <version>your_version_here</version>
</dependency>
```

### 手順 2: PSD ファイルの読み込み
サムネイルを作成したい PSD ファイルをロードします。

1. **ドキュメントディレクトリを指定**  
   PSD ファイルが格納されているディレクトリを定義します。

```java
String dataDir = "Your Document Directory"; // Replace with your path
```

2. **PSD ファイルをロード**  
   `PsdImage` クラスを使って PSD を読み込みます。

```java
PsdImage image = (PsdImage) Image.load(dataDir + "sample.psd");
```

> **プロのコツ:** PSD ファイルは `src/main/resources` など専用フォルダーに置くと、パスの問題を回避しやすくなります。

### 手順 3: PSD リソースの走査
PSD 画像がロードできたら、次はリソースを調べます。

1. **リソース数を取得**  
   PSD ファイル内のすべてのリソースをループで走査します。

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    // Processing resources
}
```

2. **サムネイルリソースを特定**  
   ループ内で、リソースがサムネイルかどうかを判定します。

```java
if (image.getImageResources()[i] instanceof ThumbnailResource) {
    // Process the thumbnail
}
```

### 手順 4: サムネイルの処理
サムネイルリソースが見つかったら、適切に処理します。

1. **サムネイル形式を取得・確認**  
   リソースがサムネイルであることを確認し、形式を取得します。

```java
ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
if (thumbnail.getFormat() == ThumbnailFormat.KJpegRgb) {
    // Create and save the thumbnail
}
```

### 手順 5: サムネイルの作成と保存
ここが本番です！ サムネイルデータから新しい画像を作成し、保存します。

1. **新しい画像を作成**  
   サムネイルリソースの幅と高さを使ってビットマップ画像を生成します。

```java
PsdImage thumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
```

2. **ピクセルを新画像に転送**  
   サムネイルデータを作成した画像にコピーします。

```java
thumbnailImage.savePixels(thumbnailImage.getBounds(), thumbnail.getThumbnailData());
```

3. **サムネイル画像を保存**  
   ユニークな名前でドキュメントディレクトリに保存します。

```java
thumbnailImage.save(dataDir + "CreateThumbnailsFromPSDFiles_out_" + i + ".bmp");
```

> **よくある落とし穴:** `PsdImage` オブジェクトを閉じ忘れるとメモリリークの原因になります。Java 7 以降を使用している場合は、try‑with‑resources ブロックで画像処理コードを囲んでください。

## まとめ
この手順を実行すれば、**PSDサムネイル作成 Java** の実装が確実にでき、任意の Photoshop ファイルからプレビュー画像を抽出できます。この手法はバッチプロセッサ、Web サービス、デスクトップユーティリティなどに組み込んで、画像カタログ化を高速化し UI の応答性を向上させることができます。ぜひご自身の PSD コレクションで試し、軽量プレビューの生成速度を体感してみてください！

## FAQ
### Aspose.PSD とは？
Aspose.PSD は、Java 開発者が Photoshop ファイルをプログラムから操作・管理できるようにするライブラリです。

### Aspose.PSD は無料で使える？
はい、ライセンス購入前に試用できる無料トライアルが提供されています。

### サムネイルはどの形式で保存できる？
本例では BMP 形式で保存しましたが、Aspose.PSD は他にも多数の形式に対応しています。

### Photoshop のインストールは必要？
いいえ、Aspose.PSD は Photoshop とは独立して動作します。

### Aspose.PSD の詳細情報はどこで得られる？
より詳しい情報やチュートリアルは [Aspose.PSD documentation](https://reference.aspose.com/psd/java/) をご覧ください。

## Frequently Asked Questions

**Q: パスワード保護された PSD からサムネイルを抽出するには？**  
A: パスワードを受け取るオーバーロード版 `Image.load` を使用して PSD をロードします。

**Q: BMP ではなく PNG でサムネイルを生成できる？**  
A: もちろんです。`save` メソッドの拡張子を PNG に変更すれば、Aspose.PSD が自動的に変換します。

**Q: 複数の PSD ファイルを一括処理する方法は？**  
A: ディレクトリ内の PSD ファイルを走査するループで、同じ抽出ロジックを繰り返し呼び出します。

**Q: 必要な Java バージョンは？**  
A: Aspose.PSD は Java 8 以降をサポートしています。最新の JDK を使用すると、パフォーマンスとセキュリティが向上します。

**Q: 大容量 PSD ファイルでも効率的に処理できるか？**  
A: はい、Aspose.PSD は遅延ロードと最適化されたメモリ管理を採用しており、ヒープ領域を圧迫せずに大きなファイルを扱えます。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最終更新日:** 2026-03-13  
**テスト環境:** Aspose.PSD 24.11 for Java (執筆時点での最新バージョン)  
**作者:** Aspose  

---