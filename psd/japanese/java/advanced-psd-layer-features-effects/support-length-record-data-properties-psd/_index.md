---
date: 2026-09-23
description: Aspose.PSD for Java を使用して PSD ベクターシェイプを変更し、PSD ファイルをバッチ処理する方法を学びます。完全なソリューションのための詳細な手順、ヒント、コードプレースホルダーを提供します。
keywords:
- modify psd vector shapes
- batch process psd files
- Aspose.PSD Java
- vector shape editing
lastmod: 2026-09-23
linktitle: PSD の Length Record データプロパティをサポート - Java
og_description: Aspose.PSD for Java を使用して PSD ベクターシェイプを変更し、PSD ファイルをバッチ処理する方法を学びます。コードプレースホルダーと専門家のヒントを含むステップバイステップガイドです。
og_image_alt: Guide showing how to edit vector shapes in PSD files using Aspose.PSD
  for Java
og_title: Aspose.PSD for Java を使用して PSD ベクターシェイプを変更する
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  headline: Modify PSD vector shapes with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  name: Modify PSD vector shapes with Aspose.PSD for Java
  steps:
  - name: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
    text: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
  - name: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
  - name: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
    text: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
  - name: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
    text: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
  type: HowTo
- questions:
  - answer: The `VsmsResource` will be absent, so `resource` stays `null`. Add a check
      and skip the modification step or inform the user.
    question: How do I handle a PSD that contains no vector shape layers?
  - answer: Yes, `LengthRecord` provides setters for fill, stroke, and opacity. See
      the API docs for the full list.
    question: Can I change other properties like fill color or stroke width?
  - answer: Absolutely. Wrap the code inside a loop that iterates over a directory
      of PSD files, adjusting the input and output paths each time.
    question: Is it possible to batch‑process multiple PSD files?
  - answer: '`Image.load` handles file streams automatically, but if you load from
      an `InputStream`, remember to close it after use.'
    question: Do I need to close streams manually when loading from a file path?
  - answer: The `LengthRecord` and `PathOperations` classes have been available since
      Aspose.PSD 20.10. Using the latest version (24.11 at time of writing) is recommended.
    question: What version of Aspose.PSD is required for these APIs?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- modify psd vector shapes
- Aspose.PSD
- Java image processing
- batch PSD processing
title: Aspose.PSD for Java を使用して PSD ベクターシェイプを変更する
url: /ja/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java を使用した PSD ベクターシェイプの変更

## はじめに
プログラムで **modify PSD vector shapes** を行う必要がある場合、Aspose.PSD for Java は Java コードから直接 Photoshop ファイルを完全に制御できます。このチュートリアルでは、ベクターシェイプレイヤーを編集する際に不可欠なステップである length record プロパティのサポート方法を説明します。最後まで実行すれば、PSD を開き、ベクターシェイプデータを調整し、Photoshop を起動せずに更新されたファイルを保存できるようになります。

## クイック回答
- **What does “modify PSD vector shapes” mean?** PSD ファイル内のベクターベースのレイヤーのジオメトリ、パス操作、その他の属性を調整することです。  
- **Which library handles this?** Aspose.PSD for Java.  
- **Do I need a license?** 無料トライアルで評価は可能ですが、製品版では商用ライセンスが必要です。  
- **How long does the implementation take?** 基本的なシェイプ変更スクリプトで約10〜15分です。  
- **What are the main prerequisites?** Java JDK、Aspose.PSD for Java、サンプル PSD ファイルです。  

## 「support length record properties」とは何ですか？
support length record properties をサポートするとは、PSD 内の各ベクターパスを記述する `LengthRecord` オブジェクトにアクセスし、更新することを意味します。これらのレコードはパスの長さ、タイプ、他のパスとの結合方法などの情報を保持します。これらを変更することで、シェイプの結合、交差、減算を制御でき、精密なベクトル編集が可能になります。

## length record properties をサポートするために Aspose.PSD for Java を使用する理由
Photoshop を使用せずに PSD をロードし、ベクターデータを編集し、保存できます。Aspose.PSD は、典型的なサーバー上で数百ページの PSD を 2 秒未満で処理し、150 以上のクラス（うち 30 以上はベクトル関連）を提供し、Windows、Linux、macOS 上で任意の JDK 11+ と共に動作します。このパフォーマンス重視のライブラリにより、高価なデスクトップソフトウェアは不要です。

## 前提条件
1. **Java Development Kit (JDK)** – [Oracle のウェブサイト](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) からダウンロードするか、お好みのパッケージマネージャを使用してください。  
2. **Aspose.PSD for Java** – 最新の JAR を [Aspose リリースページ](https://releases.aspose.com/psd/java/) から取得してください。  
3. **IDE** – IntelliJ IDEA、Eclipse、または任意の Java 対応エディタ。  
4. **A PSD file** – Photoshop で作成するか、実験用のサンプル PSD を取得してください。  
5. **Basic Java knowledge** – クラス、オブジェクト、例外処理に慣れていること。  

## パッケージのインポート
インポート文は `PsdImage`、`VsmsResource`、`LengthRecord` など、Aspose.PSD のコアクラスをスコープに持ち込みます。

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## 手順 1: ソースディレクトリと出力ディレクトリの設定
元の PSD が存在する場所と、変更後のファイルを書き込む場所を定義します。

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## 手順 2: PSD ファイルの読み込み
`Image.load` を使用してファイルを開き、PSD 固有の機能のために `PsdImage` にキャストします。

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## 手順 3: レイヤー内の Vsms リソースを見つける
`VsmsResource` はレイヤーのベクターシェイプデータを格納するコンテナです。2 番目のレイヤーのリソースをループしてそれを見つけます。

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## 手順 4: length レコードへのアクセス
`LengthRecord` は個別のベクターパスを表します。変更したいレコードを取得します。

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## 手順 5: パス操作プロパティの変更
`PathOperations` は個々のシェイプがどのように相互作用するか（例: 除外、交差、減算）を定義します。これらの値を変更すると、ベクターレイヤーの視覚的構成が更新されます。

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## 手順 6: 変更された PSD ファイルの保存
変更を新しいファイルに永続化します。

```java
psdImage.save(outPsdFilePath);
```

## 手順 7: リソースのクリーンアップ
メモリを解放しリソースリークを防ぐために `PsdImage` インスタンスを破棄します。

```java
psdImage.dispose();
```

## support length record properties を使用した PSD ファイルのバッチ処理方法
単一ファイルのワークフローをループでラップし、PSD ディレクトリを反復して各ファイルの `inPsdFilePath` と `outPsdFilePath` を更新します。この方法により、数十または数百のファイルに対して同一のベクターシェイプ調整を数分で適用でき、自動化されたアセットパイプラインに最適です。

## よくある落とし穴とヒント
- **Null checks** – メンバーにアクセスする前に `resource` が `null` でないことを必ず確認してください。  
- **Path index bounds** – 使用するインデックス（例: `[2]`、`[7]`、`[11]`）が、編集中の特定の PSD に存在することを確認してください。  
- **License** – 有効なライセンスなしで実行すると、保存された PSD に透かしが埋め込まれます。  

## 結論
これで、Aspose.PSD for Java を使用して length record プロパティをサポートしながら **modify PSD vector shapes** を行う完全なエンドツーエンドの例が手に入りました。アセットパイプラインの自動化やカスタムデザインツールの構築に関わらず、これらの API を使用すれば手動で Photoshop を操作せずにベクターレイヤーを操作できます。別の `PathOperations` の値を試したり、複数の `LengthRecord` 編集を組み合わせて複雑なシェイプを作成してみてください。

## よくある質問

**Q: ベクターシェイプレイヤーが含まれていない PSD をどう処理すればよいですか？**  
A: `VsmsResource` が存在しないため、`resource` は `null` のままです。チェックを追加して変更ステップをスキップするか、ユーザーに通知してください。

**Q: 塗りつぶしカラーやストローク幅など、他のプロパティを変更できますか？**  
A: はい、`LengthRecord` は塗り、ストローク、透明度のセッターを提供しています。完全な一覧は API ドキュメントをご覧ください。

**Q: 複数の PSD ファイルをバッチ処理することは可能ですか？**  
A: もちろん可能です。コードをループでラップし、PSD ファイルのディレクトリを反復して、毎回入力パスと出力パスを調整してください。

**Q: ファイルパスから読み込む際にストリームを手動で閉じる必要がありますか？**  
A: `Image.load` はファイルストリームを自動的に処理しますが、`InputStream` から読み込む場合は使用後に必ず閉じてください。

**Q: これらの API を使用するにはどのバージョンの Aspose.PSD が必要ですか？**  
A: `LengthRecord` と `PathOperations` クラスは Aspose.PSD 20.10 以降で利用可能です。執筆時点の最新バージョン (24.11) の使用を推奨します。

---

**最終更新日:** 2026-09-23  
**テスト環境:** Aspose.PSD for Java 24.11  
**作者:** Aspose

## 関連チュートリアル

- [PSD を PNG に変換し、Java でベクトルマスクを作成 – PSD ファイルの Vmsk リソース](/psd/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/)
- [Aspose.PSD for Java を使用してレイヤーマスクサポート付きで PSD を PNG に変換](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [PSD ファイルにレイヤーサポートを追加](/psd/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}