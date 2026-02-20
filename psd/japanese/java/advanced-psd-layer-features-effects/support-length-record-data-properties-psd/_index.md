---
date: 2026-02-20
description: Aspose.PSD for Java を使用して、長さレコードプロパティのサポート方法と PSD ファイルのバッチ処理方法を学びましょう。コード例付きのステップバイステップガイド。
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: 長さレコードプロパティのサポート – PSDベクタ形状の変更（Java）
url: /ja/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# サポート長レコードプロパティ – PSDベクタ形状の変更 (Java)

## Introduction
プログラムから **PSDベクタ形状を変更** したい場合、Aspose.PSD for Java ライブラリを使用すれば、Java コードだけで Photoshop ファイルをフルコントロールできます。このチュートリアルでは、ベクタ形状レイヤーを編集する際に必須となる **サポート長レコードプロパティ** の扱い方をすべて解説します。最後まで読めば、PSD を開き、ベクタ形状プロパティを調整し、IDE を離れることなく更新されたファイルを保存できるようになります。さっそく始めましょう！

## Quick Answers
- **「PSDベクタ形状を変更する」とは何ですか？** PSD ファイル内のベクタベースレイヤーのジオメトリ、パス操作、その他のプロパティを調整することです。  
- **どのライブラリがこれを扱いますか？** Aspose.PSD for Java。  
- **ライセンスは必要ですか？** 評価用の無料トライアルは利用可能です。商用利用には有償ライセンスが必要です。  
- **実装にかかる時間は？** 基本的な形状変更スクリプトで約 10〜15 分です。  
- **主な前提条件は？** Java JDK、Aspose.PSD for Java、サンプル PSD ファイル。

## What is “support length record properties”?
サポート長レコードプロパティとは、PSD 内の各ベクタパスを記述する `LengthRecord` オブジェクトにアクセスし、更新することを指します。これらのレコードを変更することで、形状同士の結合、交差、減算の方法を制御できます。

## Why use Aspose.PSD for Java to support length record properties?
- **Photoshop 不要** – 任意のサーバー上で直接 PSD ファイルを操作できます。  
- **リッチ API** – レイヤー、リソース、ベクタデータに強く型付けされたクラスでアクセスできます。  
- **クロスプラットフォーム** – Windows、Linux、macOS で任意の JDK と共に実行可能です。  
- **パフォーマンス重視** – メモリ管理が効率的で、保存処理も高速です。  

## Prerequisites
1. **Java Development Kit (JDK)** – [Oracle のウェブサイト](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) からダウンロードするか、好みのパッケージマネージャを使用してください。  
2. **Aspose.PSD for Java** – 最新の JAR を [Aspose リリースページ](https://releases.aspose.com/psd/java/) から取得します。  
3. **IDE** – IntelliJ IDEA、Eclipse、または任意の Java 対応エディタ。  
4. **PSD ファイル** – Photoshop で作成するか、実験用のサンプル PSD を用意してください。  
5. **基本的な Java 知識** – クラス、オブジェクト、例外処理に慣れていること。

## Import Packages
まず、PSD ファイルとベクタ形状リソースを操作するために必要なクラスをインポートします。

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Step 1: Set Up Your Source and Output Directories
元の PSD が存在する場所と、変更後のファイルを保存する場所を定義します。

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Step 2: Load the PSD File
`Image.load` を使用してファイルを開き、PSD 固有機能のために `PsdImage` にキャストします。

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Step 3: Locate the Vsms Resource in the Layer
ベクタ形状データは `VsmsResource` 内に格納されています。第 2 レイヤーのリソースを走査してそれを見つけます。

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## Step 4: Access Length Records
各 `LengthRecord` は個別のベクタパスを表します。変更したいレコードを取得しましょう。

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Step 5: Modify Path Operation Properties
ここで **PSDベクタ形状を変更** するために `PathOperations` を変更します。これにより形状同士の相互作用（除外、交差、減算など）を制御できます。

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Step 6: Save the Modified PSD File
変更を新しいファイルに保存します。

```java
psdImage.save(outPsdFilePath);
```

## Step 7: Clean Up Resources
`PsdImage` を破棄してメモリを解放します。

```java
psdImage.dispose();
```

## How to batch process PSD files with support length record properties
多数の PSD に同じベクタ形状調整を適用したい場合は、上記コードをディレクトリ内のファイルを走査するループで包みます。各イテレーションで `inPsdFilePath` と `outPsdFilePath` を更新すれば、**PSD ファイルのバッチ処理** が効率的に行えます。

## Common Pitfalls & Tips
- **Null チェック** – `resource` が `null` でないことを必ず確認してからパスにアクセスしてください。  
- **パスインデックスの範囲** – 使用するインデックス（`[2]`、`[7]`、`[11]` など）が対象 PSD に存在するか確認しましょう。  
- **ライセンス** – 有効なライセンスがない状態で実行すると、保存された PSD に透かしが埋め込まれます。  

## Conclusion
これで、Aspose.PSD for Java を使用してサポート長レコードプロパティを操作し、**PSDベクタ形状を変更** する完全なエンドツーエンド例が完成しました。アセットパイプラインの自動化やカスタムデザインツールの構築など、手動で Photoshop を開かずにベクタレイヤーを操作できる柔軟性が手に入ります。さらに `PathOperations` を試したり、複数の `LengthRecord` を組み合わせて複雑な形状を作成するなど、ぜひ色々実験してみてください。

## Frequently Asked Questions

**Q: ベクタ形状レイヤーが全く含まれていない PSD はどう扱いますか？**  
A: `VsmsResource` が存在しないため `resource` は `null` のままです。チェックを入れて変更ステップをスキップするか、ユーザーに通知してください。

**Q: 塗りつぶし色やストローク幅といった他のプロパティも変更できますか？**  
A: はい、`LengthRecord` には塗り、ストローク、透明度用のセッターが用意されています。詳細は API ドキュメントをご参照ください。

**Q: 複数の PSD をバッチ処理することは可能ですか？**  
A: もちろんです。ディレクトリ内の PSD を走査するループでコードを包み、毎回入力・出力パスを調整すれば実現できます。

**Q: ファイルパスからロードする場合、ストリームを手動で閉じる必要がありますか？**  
A: `Image.load` は内部でファイルストリームを処理しますが、`InputStream` からロードする場合は使用後に必ず閉じてください。

**Q: これらの API を利用するために必要な Aspose.PSD のバージョンは？**  
A: `LengthRecord` と `PathOperations` クラスは Aspose.PSD 20.10 以降で利用可能です。最新バージョンの使用を推奨します。

---

**Last Updated:** 2026-02-20  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}