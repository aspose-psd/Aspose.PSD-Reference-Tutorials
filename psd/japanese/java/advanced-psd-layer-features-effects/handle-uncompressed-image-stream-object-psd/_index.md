---
date: 2026-08-01
description: Aspose.PSD for Java を使用して、PSD を PNG にエクスポートし、非圧縮画像ストリームを処理する方法を学びます。
keywords:
- export psd to png
- save psd as png
- java image manipulation
lastmod: 2026-08-01
linktitle: PSD の非圧縮画像ストリームオブジェクトを処理する - Java
og_description: Aspose.PSD for Java を使用して PSD を PNG にエクスポートします。非圧縮画像ストリームの処理、グラフィックスオブジェクトの作成、高品質
  PNG の保存方法を学びます。
og_image_alt: 'Developer guide: Export PSD to PNG with uncompressed stream using Aspose.PSD
  Java'
og_title: PSD を PNG にエクスポート – 非圧縮 PSD ストリームの Java ガイド
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to export PSD to PNG and handle uncompressed image streams
    with Aspose.PSD for Java.
  headline: Export PSD to PNG – Create PSD Graphics Object – Uncompressed Stream in
    Java
  type: TechArticle
- questions:
  - answer: Yes. After loading the PSD, retrieve the desired layer via `psdImage.getLayers().get_Item(index)`
      and pass that layer to the `Graphics` constructor.
    question: Can I use the graphics object to edit only one specific layer?
  - answer: Raw stores pixel data without any compression, so the resulting file is
      larger than a compressed PSD, but it guarantees 100 % pixel fidelity.
    question: Does the Raw compression method affect file size?
  - answer: Absolutely. After editing, call `psdImage.save("output.png", new PngOptions())`—this
      is the standard way to **export PSD to PNG** with lossless quality.
    question: Is it possible to export the edited PSD to another format (e.g., PNG)?
  - answer: Aspose.PSD for Java supports JDK 8 and later, including all LTS releases
      up to JDK 21.
    question: What Java version is required?
  - answer: Invoke `psdImage.dispose()` and close any streams (e.g., `ms.close()`)
      to free native memory and avoid leaks.
    question: How do I release resources after processing?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- export psd
- Aspose.PSD
- Java image processing
- uncompressed stream
- PSD graphics
title: PSD を PNG にエクスポート – PSD グラフィックスオブジェクトの作成 – Java の非圧縮ストリーム
url: /ja/java/advanced-psd-layer-features-effects/handle-uncompressed-image-stream-object-psd/
weight: 26
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD を PNG にエクスポート – PSD グラフィックスオブジェクトの作成 – Java の非圧縮ストリーム

## はじめに
このステップバイステップガイドでは、Aspose.PSD for Java を使用して非圧縮画像ストリームを扱いながら **export PSD to PNG** を行います。デザインパイプラインを自動化する場合やカスタムエディタを構築する場合でも、品質を損なうことなく Photoshop ファイルをレンダリングできることは重要です。必要なセットアップから始め、`Graphics` オブジェクトの作成手順を説明し、最後にロスレス PNG エクスポートで完了します。最後まで読むと、Aspose.PSD が raw ストリームを効率的に処理する理由と、任意の Java プロジェクトに統合する方法が理解できるようになります。

## クイック回答
- **What does “create PSD graphics object” mean?** それは、プログラムから PSD 画像を描画または変更できる `Graphics` コンテキストをインスタンス化することを意味します。  
- **Which library handles uncompressed streams?** Aspose.PSD for Java は raw（非圧縮）画像データの完全なサポートを提供します。  
- **Can I export PSD to PNG after editing?** はい—`Graphics` オブジェクトを取得すれば、PSD をレンダリングし、単一の呼び出しで PNG として保存できます。  
- **Do I need a license for development?** 無料トライアルはテストに利用可能ですが、本番環境では商用ライセンスが必要です。  
- **Is the export lossless?** PNG へのエクスポートは元のピクセルデータを保持し、raw PSD より小さいファイルサイズでロスレス品質を提供します。

## PSD を PNG にエクスポートとは何ですか？
PSD を PNG にエクスポートすると、レイヤー構造を持つ Photoshop ドキュメントが単一レイヤーのロスレスラスタ画像に変換され、任意のウェブブラウザや画像ビューアで表示可能になります。このプロセスは透明性、色深度、レイヤー効果を保持しつつ、Photoshop 固有のメタデータは破棄します。また、正確な色再現のために元のカラープロファイルも保持されます。

## なぜ画像操作に Aspose.PSD for Java を使用するのか？
Aspose.PSD は **50+** の入力および出力フォーマット（PSD、PNG、JPEG、BMP、TIFF など）をサポートし、**200+ レイヤー** をメモリ全体にロードせずに処理できます。`Raw` 圧縮オプションはピクセルデータを非圧縮で保存し、下流の編集やアーカイブに対してピクセル単位の完全な忠実性を保証します。

## 前提条件
- **Java Development Kit (JDK)** – JDK 8 以降がインストールされていること。  
- **Aspose.PSD for Java** – 公式リリースページから最新の JAR をダウンロードしてください: [Aspose.PSD Java download](https://releases.aspose.com/psd/java/)。[このリンク](https://releases.aspose.com/psd/java/) または [リリースページ](https://releases.aspose.com/psd/java/) からもアクセスできます。他の Aspose 製品については [here](https://releases.aspose.com/) をクリックしてください。  
- **IDE** – IntelliJ IDEA、Eclipse、または任意の Java 対応エディタ。  
- **Basic Java knowledge** – クラス、メソッド、例外処理に慣れていること。

これらが揃っていれば、コーディングを開始する準備が整います。

## パッケージのインポート
`Graphics` クラスは Aspose.PSD の描画サーフェスで、ピクセルデータを直接レンダリングまたは編集できます。`PsdImage` クラスはメモリ上の PSD ファイルを表し、`PsdOptions` は画像の保存方法を制御します。

```java
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

さて、コードを理解しやすいステップに分解していきます。環境設定、PSD ファイルの読み込み、操作、最終的な保存までを順に解説します。

## ステップ 1: ドキュメントディレクトリを定義する
ファイル操作を行う前に、プログラムが PSD アセットを探す場所を指定する必要があります。このディレクトリパスはチュートリアル全体で使用されます。

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` を `layers.psd` が格納されている絶対パスに置き換えてください。パスを設定可能にしておくことで、プロジェクト間でコードを再利用しやすくなります。

## ステップ 2: ByteArrayOutputStream を作成する
`ByteArrayOutputStream` はバイト配列としてメモリ内にデータを保持する Java ストリームです。変更された画像のインメモリバッファとして機能し、ディスクへの書き込みやネットワーク送信の前に raw バイトを取得できます。

```java
ByteArrayOutputStream ms = new ByteArrayOutputStream();
```

変数 `ms` は `save` 操作後の非圧縮画像データを保持します。

## ステップ 3: PSD ファイルをロードする
`PsdImage` クラスは PSD ファイルをメモリにロードして操作可能にします。ファイルをロードすると、ディスク上の PSD が操作できる `PsdImage` オブジェクトに変換されます。このステップで Aspose.PSD はファイルヘッダー、レイヤー、リソースを読み取ります。

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "layers.psd");
```

パスが間違っている場合、Aspose.PSD は `FileNotFoundException` をスローします。実運用コードではこれを捕捉すべきです。

## ステップ 4: 保存用に PsdOptions を設定する
`PsdOptions` は PSD ファイルの保存パラメータを指定します。圧縮方式を `Raw` に設定すると、ピクセルデータが圧縮なしで保存され、メモリ上のピクセルと完全に同一になります。

```java
PsdOptions saveOptions = new PsdOptions();
saveOptions.setCompressionMethod(CompressionMethod.Raw);
```

`CompressionMethod.Raw` オプションはピクセルデータを一切圧縮せずに保存するため、後でさらに編集する予定がある場合に最適です。

## ステップ 5: 画像を出力ストリームに保存する
ここで、（変更があれば）PSD を先ほど作成した `ByteArrayOutputStream` に永続化します。`save` メソッドは設定した `PsdOptions` を尊重します。

```java
psdImage.save(ms, saveOptions);
```

この時点で `ms` には非圧縮 PSD の完全なバイナリ表現が格納されています。

## ステップ 6: 出力ストリームをリセットする
書き込み後、ストリームの内部ポインタは末尾に位置します。リセットするとストリームが先頭に戻り、最初から読み取れるようになります。

```java
ms.reset();
```

テープのヘッドを再生開始位置に戻すイメージです。

## ステップ 7: 新しく作成した画像をロードする
バイト配列から直接新しい `PsdImage` インスタンスを作成できます。このステップで、保存されたデータが破損せずに再ロードできることを確認します。

```java
PsdImage img = (PsdImage) Image.load(new ByteArrayInputStream(ms.toByteArray()));
```

画像が正常にロードできれば、非圧縮ストリームが正しく書き込まれたことが分かります。

## ステップ 8: Graphics オブジェクトを作成する
`Graphics` クラスは Aspose.PSD の描画キャンバスです。`PsdImage` のピクセルマトリックス上に直接図形、テキスト、フィルタを描画するメソッドを提供します。

```java
Graphics graphics = new Graphics(psdImage);
```

この `Graphics` インスタンスを使って新しいコンテンツを描画したり、部分を消去したり、追加レイヤーを合成したりできます。

## Aspose.PSD for Java を使用して PSD を PNG にエクスポートするには？
`new PsdImage(dataDir + "layers.psd")` で PSD をロードし、`Graphics` オブジェクトを作成し、必要な描画を行った後、`psdImage.save("output.png", new PngOptions())` を呼び出します。このシーケンスは編集済み PSD をレンダリングし、単一のステップでロスレス PNG を書き出します。Aspose.PSD の組み込み変換エンジンを活用しています。

## Graphics オブジェクトで PSD レイヤーを操作する
`Graphics` インスタンスがあれば、各レイヤーをピクセルレベルで制御できます。幾何学的形状の描画、テキストのレンダリング、カスタムフィルタの適用が可能です。グラフィックコンテキストはレイヤーのラスタライズビュー上で動作するため、画像を保存した瞬間に変更が即座に反映されます。

## 一般的な問題と解決策
- **NullPointerException when loading the file** – `dataDir` パスを再確認し、ファイル名が正確に（大文字小文字も含めて）一致しているか確認してください。  
- **Compressed output despite using Raw** – `save` を呼び出す **前に** `saveOptions.setCompressionMethod(CompressionMethod.Raw);` が実行されていることを確認してください。  
- **Graphics object appears blank** – 正しい `PsdImage` インスタンス（ロードしたもの）に対して描画しているか確認し、空の新規画像に描画していないか確認してください。  
- **OutOfMemoryError on large files** – `PsdImage.load(dataDir, LoadOptions)` と `loadOptions.setLoadMode(LoadMode.Memory)` を使用して、ドキュメント全体を RAM にロードせずに大容量ファイルをストリーミングできます。

## よくある質問

### What is Aspose.PSD?
Aspose.PSD は、Adobe Photoshop を必要とせずに Java 開発者がプログラムから Photoshop PSD ファイルを作成、編集、変換できるライブラリです。レイヤー、マスク、チャンネル、各種画像リソースの読み書きをサポートし、ラスタおよびベクトル操作用の API を提供するため、サーバーサイドの画像処理や自動化タスクに適しています。

### How can I download Aspose.PSD for Java?
公式リリースページからダウンロードできます: [Aspose.PSD Java download](https://releases.aspose.com/psd/java/).

### Is there a free trial for Aspose.PSD?
はい、同じダウンロードページでフル機能のトライアル版が利用可能です。開発および評価目的で使用できます。

### Can I get support for Aspose.PSD?
もちろんです！Aspose のサポートフォーラムでは、製品チームやコミュニティからの回答が得られます: [Aspose support forum](https://forum.aspose.com/c/psd/34)。

### How can I obtain a temporary license for Aspose.PSD?
Aspose のライセンスポータルから 30 日間有効な一時ライセンスキーを直接リクエストできます。これにより、商用ライセンスを購入せずに Aspose.PSD のフル機能を評価できます。トライアル期間終了後は、永続ライセンスに置き換える必要があります。時間制限付きキーの生成は、[temporary license page](https://purchase.aspose.com/temporary-license/) から行ってください。

## 頻繁に尋ねられる質問

**Q: Can I use the graphics object to edit only one specific layer?**  
A: はい。PSD をロードした後、`psdImage.getLayers().get_Item(index)` で目的のレイヤーを取得し、そのレイヤーを `Graphics` コンストラクタに渡すことで、特定レイヤーのみを編集できます。

**Q: Does the Raw compression method affect file size?**  
A: Raw はピクセルデータを圧縮せずに保存するため、圧縮された PSD よりファイルサイズは大きくなりますが、100 % のピクセル忠実度が保証されます。

**Q: Is it possible to export the edited PSD to another format (e.g., PNG)?**  
A: もちろんです。編集後に `psdImage.save("output.png", new PngOptions())` を呼び出すことで、**export PSD to PNG** と同様にロスレス品質で PNG へエクスポートできます。

**Q: What Java version is required?**  
A: Aspose.PSD for Java は JDK 8 以降をサポートしており、JDK 21 までのすべての LTS リリースに対応しています。

**Q: How do I release resources after processing?**  
A: `psdImage.dispose()` を呼び出し、ストリーム（例: `ms.close()`）を閉じてネイティブメモリを解放し、リークを防止してください。

---

**最終更新日:** 2026-08-01  
**テスト環境:** Aspose.PSD for Java (latest release)  
**作者:** Aspose  

{{< blocks/products/products-backtop-button >}}

## 関連チュートリアル

- [Aspose.PSD for Java で画像をストリームに保存](/psd/java/advanced-techniques/save-images-to-stream/)
- [Java を使用して PSD レイヤー グループを画像にエクスポート](/psd/java/working-with-psd-files/export-psd-layer-group-to-image/)
- [Aspose.PSD for Java でストリームを使用して画像を作成](/psd/java/image-editing/create-image-using-stream/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}