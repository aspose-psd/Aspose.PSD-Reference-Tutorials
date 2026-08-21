---
date: 2026-06-08
description: Aspose.PSD for Java を使用して PSD を PNG に保存する方法と、必要に応じて変換を中断する方法を学びます。画像ワークフローを効率的に管理しましょう。
keywords:
- save psd as png
- how to interrupt conversion
- psd to png conversion
- manage image workflow
linktitle: Interrupt Monitor のサポート
schemas:
- author: Aspose
  dateModified: '2026-06-08'
  description: Learn how to save PSD as PNG using Aspose.PSD for Java and interrupt
    conversion when needed. Manage image workflow efficiently.
  headline: How to Save PSD as PNG with Interrupt Monitor in Aspose.PSD for Java
  type: TechArticle
- description: Learn how to save PSD as PNG using Aspose.PSD for Java and interrupt
    conversion when needed. Manage image workflow efficiently.
  name: How to Save PSD as PNG with Interrupt Monitor in Aspose.PSD for Java
  steps:
  - name: Set Your Document Directory
    text: Ensure to replace “Your Document Directory” with the actual path where your
      PSD documents are stored.
  - name: Define Image Options and Output Path
    text: Specify the image options, source PSD file, and the desired output path
      for the converted image.
  - name: Initialize Interrupt Monitor and SaveImageWorker
    text: The `InterruptMonitor` class watches a running conversion and can interrupt
      it when `requestInterrupt()` is called. Create instances of `InterruptMonitor`
      and `SaveImageWorker`, linking the monitor to the image conversion worker.
  - name: Start Image Conversion Thread
    text: Initiate a new thread for the image conversion process and introduce a timeout
      period to anticipate interruption.
  - name: Interrupt the Process
    text: Calling `monitor.requestInterrupt()` signals the monitor to abort the ongoing
      conversion. Interrupt the image conversion process using the `InterruptMonitor`
      and wait for the interruption to complete. Finally, clean up by deleting the
      output file.
  type: HowTo
- questions:
  - answer: Yes, use `InterruptMonitor` to stop the process on demand.
    question: Can I interrupt a PSD‑to‑PNG conversion?
  - answer: Call `save(outputPath, new PngOptions())`.
    question: Which method saves a PSD as PNG?
  - answer: A commercial license is required; a free trial is available.
    question: Do I need a license for production?
  - answer: Java 8 and later are fully supported.
    question: What Java version is supported?
  - answer: Conversions can run in separate threads; the monitor handles interruptions
      safely.
    question: Is the library thread‑safe?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java で Interrupt Monitor を使用して PSD を PNG に保存する方法
url: /ja/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java のインタラプトモニターを使用して PSD を PNG に保存する

## はじめに

長時間実行される変換を完全に制御しながら **PSD を PNG に保存** したい場合、Aspose.PSD for Java のインタラプトモニターがまさにそれを提供します。このチュートリアルでは、モニターの設定方法、PSD ファイルを PNG に変換する方法、そして必要に応じて安全に処理を中止する方法を順を追って説明します。また、これが一般的な画像処理ワークフローにどのように組み込まれるか、そして堅牢なアプリケーションにとってなぜ必須なのかも確認できます。

## クイック回答
- **PSD から PNG への変換を中断できますか？** はい、`InterruptMonitor` を使用して要求に応じてプロセスを停止できます。  
- **PSD を PNG に保存するメソッドはどれですか？** `save(outputPath, new PngOptions())` を呼び出します。  
- **本番環境でライセンスが必要ですか？** 商用ライセンスが必要です。無料トライアルも利用可能です。  
- **サポートされている Java バージョンは何ですか？** Java 8 以降が完全にサポートされています。  
- **このライブラリはスレッドセーフですか？** 変換は別々のスレッドで実行でき、モニターは安全に中断を処理します。

## 前提条件

インタラプトモニターの使用の詳細に入る前に、以下の前提条件が整っていることを確認してください。

- **Java 開発環境:** システム上に Java 開発環境をセットアップしてください。  
- **Aspose.PSD ライブラリ:** Aspose.PSD for Java ライブラリを入手してください。こちらからダウンロードできます [here](https://releases.aspose.com/psd/java/)。また、メインの Aspose サイトもこちらからアクセスできます [here](https://releases.aspose.com/)。  
- **ドキュメントディレクトリ:** PSD ドキュメント用の指定ディレクトリを用意してください。

## パッケージのインポート

まず、必要なパッケージを Java プロジェクトにインポートします。これにより、Aspose.PSD の機能にアクセスできるようになります。

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

それでは、例コードを段階的に分解し、Aspose.PSD for Java プロジェクトにインタラプトモニターを組み込む手順をご紹介します。

## インタラプトモニターを使用して PSD を PNG に保存する方法

`PsdImage` はメモリにロードされた PSD ドキュメントを表します。  
`SaveImageWorker` は別スレッドで画像変換を実行します。  

`new PsdImage("source.psd")` で PSD ファイルをロードし、`InterruptMonitor` を `SaveImageWorker` に添付し、`save("output.png", new PngOptions())` を呼び出します。モニターはキャンセル要求を監視し、変換をきれいに中止して、数ミリ秒以内にアプリケーションへ制御を戻します。

### 手順 1: ドキュメントディレクトリの設定

```java
String dataDir = "Your Document Directory";
```

“Your Document Directory” を、PSD ドキュメントが保存されている実際のパスに置き換えてください。

### 手順 2: 画像オプションと出力パスの定義

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

画像オプション、ソース PSD ファイル、変換後画像の出力パスを指定してください。

### 手順 3: インタラプトモニターと SaveImageWorker の初期化

`InterruptMonitor` クラスは実行中の変換を監視し、`requestInterrupt()` が呼び出されたときに中断できます。  

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

`InterruptMonitor` と `SaveImageWorker` のインスタンスを作成し、モニターを画像変換ワーカーにリンクさせます。

### 手順 4: 画像変換スレッドの開始

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

画像変換プロセス用に新しいスレッドを開始し、中断を予測するためのタイムアウト期間を設定します。

### 手順 5: プロセスの中断

`monitor.requestInterrupt()` を呼び出すと、モニターに対して進行中の変換を中止するよう指示します。  

```java
    // Interrupt the process
    monitor.interrupt();
    System.out.println("Interrupting the save thread #" + thread.getId() + " at " + getDateTime().toString());

    // Wait for interruption...
    thread.join();
} finally {
    // Delete the output file if it exists
    File f = new File(output);
    if (f.exists()) {
        f.delete();
    }
}
```

`InterruptMonitor` を使用して画像変換プロセスを中断し、中断が完了するのを待ちます。最後に、出力ファイルを削除してクリーンアップします。

## なぜ PSD から PNG への変換にインタラプトモニターを使用するのか

Aspose.PSD は **30 以上の出力フォーマット**（PNG、JPEG、BMP、TIFF など）をサポートし、**500 MB** までのファイルをドキュメント全体をメモリにロードせずに処理できます。インタラプトモニターを追加することで、CPU の無駄を削減し、バッチ処理パイプラインの応答性を向上させます。特に、変換が予想時間を超える場合に有効です。

## よくある問題と解決策

- **変換が無期限にハングする:** `save` を呼び出す **前に** モニターが添付されていることを確認してください。  
- **中断後に出力ファイルが破損する:** モニターはきれいに中止しますが、使用する前に必ずファイルが存在するか確認してください。  
- **スレッドセーフ性の懸念:** 各変換を個別のスレッドで実行してください。モニターは関連付けられたワーカーにのみ影響します。

## よくある質問

**Q1: Aspose.PSD for Java のインタラプトモニターとは何ですか？**  
A: インタラプトモニターは、開発者が長時間実行される画像変換を一時停止またはキャンセルできるようにし、リソース使用量をリアルタイムで制御できます。

**Q2: Aspose.PSD for Java ライブラリはどこで入手できますか？**  
A: Aspose.PSD for Java ライブラリは [here](https://releases.aspose.com/psd/java/) からダウンロードできます。

**Q3: Aspose.PSD for Java の無料トライアルはありますか？**  
A: はい、Aspose.PSD の無料トライアルは [here](https://releases.aspose.com/) で試すことができます。

**Q4: Aspose.PSD for Java のサポートはどこで見つけられますか？**  
A: Aspose.PSD for Java のサポートフォーラムは [here](https://forum.aspose.com/c/psd/34) でご覧ください。

**Q5: Aspose.PSD for Java のライセンスはどこで購入できますか？**  
A: Aspose.PSD for Java のライセンスは [here](https://purchase.aspose.com/buy) から購入できます。

**Q6: 複数の PSD ファイルを並行して PNG に変換できますか？**  
A: はい、各ファイルごとに別々のスレッドを生成し、各変換ワーカーに個別の `InterruptMonitor` を添付してください。

**Q7: PSD から PNG への変換時にライブラリはカラープロファイルを処理しますか？**  
A: もちろんです。Aspose.PSD は埋め込まれた ICC プロファイルを保持し、出力 PNG に自動的に適用します。

---

**最終更新日:** 2026-06-08  
**テスト済み:** Aspose.PSD 23.12 for Java  
**作者:** Aspose  

{{< blocks/products/products-backtop-button >}}

## 関連チュートリアル

- [Aspose.PSD for Java で PSD を PNG に保存し、レンダリングドロップシャドウを適用する](/psd/java/advanced-image-manipulation/rendering-drop-shadow/)
- [Aspose.PSD for Java を使用して PSD を PNG にエクスポートし、新しいレギュラーレイヤーを追加する](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [PSD ファイルにおけるインタラプトモニターのサポート - Java](/psd/java/psd-layer-management-effects/support-interrupt-monitor-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}