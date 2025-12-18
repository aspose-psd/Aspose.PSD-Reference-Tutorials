---
date: 2025-12-17
description: Aspose.PSD for Java を使用して、長さレコード データ プロパティをサポートしながら PSD のベクタ形状を変更する方法を学びます。コード例付きのステップバイステップ
  ガイドです。
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: PSDベクタシェイプの変更方法 – Javaで長さレコードデータプロパティをサポート
url: /ja/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD の長さレコードデータプロパティをサポート - Java

## はじめに
プログラムから **PSD ベクタ形状を変更** したい場合、Aspose.PSD for Java ライブラリを使用すれば、Java コードだけで Photoshop ファイルをフルコントロールできます。このチュートリアルでは、ベクタ形状レイヤーを編集する際に必須となる長さレコードデータプロパティのサポート方法をすべて解説します。最後まで読むと、PSD を開いてベクタ形状プロパティを調整し、IDE を離れることなく更新されたファイルを保存できるようになります。さっそく始めましょう！

## クイックアンサー
- **“modify PSD vector shapes” とは何ですか？** PSD ファイル内のベクタベースレイヤーのジオメトリ、パス操作、その他のプロパティを調整することです。  
- **どのライブラリがこれを処理しますか？** Aspose.PSD for Java。  
- **ライセンスは必要ですか？** 評価用の無料トライアルで試すことができますが、商用利用には有料ライセンスが必要です。  
- **実装にどれくらい時間がかかりますか？** 基本的な形状変更スクリプトで約 10〜15 分程度です。  
- **主な前提条件は何ですか？** Java JDK、Aspose.PSD for Java、サンプル PSD ファイル。

## 「PSD ベクターシェイプの変更」とは何ですか？
PSD ベクタ形状の変更とは、ベクタパスデータ（長さレコードやパス操作など）を変更し、形状の見た目がそれに応じて更新されることを指します。自動化されたグラフィックパイプライン、バッチ処理、カスタムデザインツールなどで特に有用です。

## PSD ベクターシェイプの変更に Aspose.PSD for Java を使用する理由は何ですか？
- - **Photoshop は不要** – 任意のサーバー上で直接 PSD ファイルを操作できます。  
- **豊富な API** – 強く型付けされたクラスでレイヤー、リソース、ベクタデータにアクセスできます。  
- **クロスプラットフォーム** – Windows、Linux、macOS いずれでも任意の JDK で実行可能です。  
- **パフォーマンス重視** – メモリ管理が効率的で、保存処理も高速です。

## 前提条件
1. **Java 開発キット (JDK)** – [Oracle のウェブサイト](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) からダウンロードするか、お好みのパッケージマネージャをご利用ください。  
2. **Aspose.PSD for Java** – [Aspose リリースページ](https://releases.aspose.com/psd/java/) から最新の JAR を取得してください。  
3. **IDE** – IntelliJ IDEA、Eclipse、または任意の Java 対応エディタ。  
4. **PSD ファイル** – Photoshop で作成するか、サンプル PSD を入手して実験してください。  
5. **Java の基礎知識** – クラス、オブジェクト、例外処理に慣れていること。

## パッケージのインポート
まず、PSD ファイルとベクタ形状リソースを操作するために必要なクラスをインポートします。

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## ステップ 1: ソースディレクトリと出力ディレクトリの設定
元の PSD が存在する場所と、変更後のファイルを保存する場所を定義します。

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## ステップ 2: PSD ファイルの読み込み
`Image.load` を使用してファイルを開き、PSD 固有の機能を利用できるように `PsdImage` にキャストします。

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## ステップ 3: レイヤー内の Vsms リソースの検索
ベクタ形状データは `VsmsResource` 内に格納されています。2 番目のレイヤーのリソースをループして該当リソースを見つけます。

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## ステップ 4: 長さレコードへのアクセス
各 `LengthRecord` は個別のベクタパスを表します。変更したいレコードを取得しましょう。

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## ステップ 5: パス操作プロパティの変更
ここで `PathOperations` を変更することで **PSD ベクタ形状を変更** できます。これにより形状同士の相互作用（除外、交差、減算など）が決まります。

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## ステップ 6: 変更した PSD ファイルを保存する
変更内容を新しいファイルに保存します。

```java
psdImage.save(outPsdFilePath);
```

## ステップ 7: リソースのクリーンアップ
`PsdImage` を破棄してメモリを解放します。

```java
psdImage.dispose();
```

## ## よくある落とし穴とヒント
- **Null チェック** – `resource` が `null` でないことを必ず確認してからパスにアクセスしてください。  
- **パスのインデックス範囲** – 使用するインデックス（`[2]`、`[7]`、`[11]`）が対象 PSD に存在するか確認しましょう。  
- **ライセンス** – 有効なライセンスがない状態で実行すると、保存された PSD に透かしが埋め込まれます。  

## まとめ

これで、Aspose.PSD for Java を使用して長さレコードデータプロパティをサポートしながら **PSD ベクタ形状を変更** する完全なエンドツーエンドの例が完成しました。アセットパイプラインの自動化やカスタムデザインツールの構築において、これらの API を活用すれば Photoshop の手作業なしでベクタレイヤーを自在に操作できます。さらに `PathOperations` を試したり、複数の `LengthRecord` を組み合わせて複雑な形状を作成するなど、ぜひ色々と実験してみてください。

## よくある質問

**Q: ベクターシェイプレイヤーを含まないPSDファイルはどのように処理すればよいですか？**
  
A: `VsmsResource` が存在しないため、`resource` は `null のままです。チェックを追加して変更ステップをスキップするか、ユーザーに通知してください。

**Q: 塗りつぶしの色や線幅などの他のプロパティを変更できますか？**

A: はい、`LengthRecord` には塗りつぶし、ストローク、透明度などの追加セッターが用意されています。詳細は API ドキュメントをご参照ください。

**Q: 複数のPSDファイルを一括処理することはできますか？**

A: もちろんです。ディレクトリ内の PSD ファイルをループで処理し、入力・出力パスを毎回調整すれば実現できます。

**Q: パスから読み込む際に、ストリームを手動で閉じる必要がありますか？**
  
A: `Image.load` メソッドは内部でファイルストリームを処理しますが、`InputStream` からロードする場合は使用後に必ずクローズしてください。

**Q: これらのAPIを使用するには、どのバージョンのAspose.PSDが必要ですか？**
A: `LengthRecord` と `PathOperations` クラスは Aspose.PSD 20.10 以降で利用可能です。最新バージョンの使用を推奨します。

---

**最終更新日:** 2025年12月17日
**テスト環境:** Aspose.PSD for Java 24.11
**作成者:** Aspose 

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}