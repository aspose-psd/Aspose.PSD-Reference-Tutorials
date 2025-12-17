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

## Introduction
プログラムから **PSD ベクタ形状を変更** したい場合、Aspose.PSD for Java ライブラリを使用すれば、Java コードだけで Photoshop ファイルをフルコントロールできます。このチュートリアルでは、ベクタ形状レイヤーを編集する際に必須となる長さレコードデータプロパティのサポート方法をすべて解説します。最後まで読むと、PSD を開いてベクタ形状プロパティを調整し、IDE を離れることなく更新されたファイルを保存できるようになります。さっそく始めましょう！

## Quick Answers
- **“modify PSD vector shapes” とは何ですか？** PSD ファイル内のベクタベースレイヤーのジオメトリ、パス操作、その他のプロパティを調整することです。  
- **どのライブラリがこれを処理しますか？** Aspose.PSD for Java。  
- **ライセンスは必要ですか？** 評価用の無料トライアルで試すことができますが、商用利用には有料ライセンスが必要です。  
- **実装にどれくらい時間がかかりますか？** 基本的な形状変更スクリプトで約 10〜15 分程度です。  
- **主な前提条件は何ですか？** Java JDK、Aspose.PSD for Java、サンプル PSD ファイル。

## What is “modify PSD vector shapes”?
PSD ベクタ形状の変更とは、ベクタパスデータ（長さレコードやパス操作など）を変更し、形状の見た目がそれに応じて更新されることを指します。自動化されたグラフィックパイプライン、バッチ処理、カスタムデザインツールなどで特に有用です。

## Why use Aspose.PSD for Java to modify PSD vector shapes?
- **No Photoshop required** – 任意のサーバー上で直接 PSD ファイルを操作できます。  
- **Rich API** – 強く型付けされたクラスでレイヤー、リソース、ベクタデータにアクセスできます。  
- **Cross‑platform** – Windows、Linux、macOS いずれでも任意の JDK で実行可能です。  
- **Performance‑focused** – メモリ管理が効率的で、保存処理も高速です。

## Prerequisites
1. **Java Development Kit (JDK)** – [Oracle のウェブサイト](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) からダウンロードするか、お好みのパッケージマネージャをご利用ください。  
2. **Aspose.PSD for Java** – [Aspose リリースページ](https://releases.aspose.com/psd/java/) から最新の JAR を取得してください。  
3. **IDE** – IntelliJ IDEA、Eclipse、または任意の Java 対応エディタ。  
4. **A PSD file** – Photoshop で作成するか、サンプル PSD を入手して実験してください。  
5. **Basic Java knowledge** – クラス、オブジェクト、例外処理に慣れていること。

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
`Image.load` を使用してファイルを開き、PSD 固有の機能を利用できるように `PsdImage` にキャストします。

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Step 3: Locate the Vsms Resource in the Layer
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

## Step 4: Access Length Records
各 `LengthRecord` は個別のベクタパスを表します。変更したいレコードを取得しましょう。

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Step 5: Modify Path Operation Properties
ここで `PathOperations` を変更することで **PSD ベクタ形状を変更** できます。これにより形状同士の相互作用（除外、交差、減算など）が決まります。

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Step 6: Save the Modified PSD File
変更内容を新しいファイルに保存します。

```java
psdImage.save(outPsdFilePath);
```

## Step 7: Clean Up Resources
`PsdImage` を破棄してメモリを解放します。

```java
psdImage.dispose();
```

## Common Pitfalls & Tips
- **Null checks** – `resource` が `null` でないことを必ず確認してからパスにアクセスしてください。  
- **Path index bounds** – 使用するインデックス（`[2]`、`[7]`、`[11]`）が対象 PSD に存在するか確認しましょう。  
- **License** – 有効なライセンスがない状態で実行すると、保存された PSD に透かしが埋め込まれます。  

## Conclusion
これで、Aspose.PSD for Java を使用して長さレコードデータプロパティをサポートしながら **PSD ベクタ形状を変更** する完全なエンドツーエンドの例が完成しました。アセットパイプラインの自動化やカスタムデザインツールの構築において、これらの API を活用すれば Photoshop の手作業なしでベクタレイヤーを自在に操作できます。さらに `PathOperations` を試したり、複数の `LengthRecord` を組み合わせて複雑な形状を作成するなど、ぜひ色々と実験してみてください。

## FAQ's
### What is Aspose.PSD for Java?
Aspose.PSD for Java は、開発者が Java を使用してプログラム Photoshop PSD ファイルを操作できるライブラリです。

### Can I use Aspose.PSD in a free project?
はい、Aspose のウェブサイトで提供されているトライアル版を無料で試すことができます。

### What types of modifications can I make to PSD files?
レイヤー、シェイプ、テキスト、パス操作など、PSD ファイル内のさまざまな要素を操作できます。

### Is Aspose.PSD compatible with other programming languages?
はい、.NET や Python など、他のプログラミング言語向けのライブラリも提供されています。

### Where can I find the documentation for Aspose.PSD?
完全なドキュメントは [here](https://reference.aspose.com/psd/java/) からアクセスできます。

## Frequently Asked Questions

**Q: How do I handle a PSD that contains no vector shape layers?**  
A: `VsmsResource` が存在しないため、`resource` は `null のままです。チェックを追加して変更ステップをスキップするか、ユーザーに通知してください。

**Q: Can I change other properties like fill color or stroke width?**  
A: はい、`LengthRecord` には塗りつぶし、ストローク、透明度などの追加セッターが用意されています。詳細は API ドキュメントをご参照ください。

**Q: Is it possible to batch‑process multiple PSD files?**  
A: もちろんです。ディレクトリ内の PSD ファイルをループで処理し、入力・出力パスを毎回調整すれば実現できます。

**Q: Do I need to close streams manually when loading from path?**  
A: `Image.load` メソッドは内部でファイルストリームを処理しますが、`InputStream` からロードする場合は使用後に必ずクローズしてください。

**Q: What version of Aspose.PSD is required for these APIs?**  
A: `LengthRecord` と `PathOperations` クラスは Aspose.PSD 20.10 以降で利用可能です。最新バージョンの使用を推奨します。

---

**Last Updated:** 2025-12-17  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}