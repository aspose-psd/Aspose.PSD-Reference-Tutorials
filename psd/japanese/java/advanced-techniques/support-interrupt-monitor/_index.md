---
date: 2025-12-25
description: Aspose.PSD for Java の割り込みモニタサポートを使用して PSD を PNG に変換する方法を学び、Java スレッドの割り込み例や
  PSD を PNG として保存するコツも含めます。
linktitle: Support for Interrupt Monitor
second_title: Aspose.PSD Java API
title: Aspose.PSD for Javaで割り込みモニターサポートを使用してPSDをPNGに変換する方法
url: /ja/java/advanced-techniques/support-interrupt-monitor/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java の Interrupt Monitor を使用した PSD から PNG への変換

## はじめに

長時間実行される画像変換を完全に制御しながら **PSD を PNG に変換**したい場合、Aspose.PSD for Java の Interrupt Monitor が最適です。このチュートリアルでは、変換処理の途中で停止できる実際の **java スレッド割り込み例**を通して、リソース管理やタイムアウトの実装、ユーザーキャンセルへの対応方法を解説します。

## クイック回答
- **Interrupt Monitor とは何ですか？** 進行中の画像変換に安全に停止シグナルを送ることができます。  
- **これで PSD を PNG に変換できますか？** はい – 監視機能は PNG を含むすべての保存操作で使用できます。  
- **別スレッドは必須ですか？** 通常は変換処理を別スレッドで実行し、割り込みできるようにします。  
- **必要な Aspose.PSD のバージョンは？** `com.aspose.psd.multithreading.InterruptMonitor` を含む最近のバージョンであれば問題ありません。  
- **本番環境でライセンスは必要ですか？** はい、トライアル以外で使用する場合は有効な Aspose.PSD ライセンスが必要です。

## Interrupt Monitor 付きで「PSD を PNG に変換する」とは？

大容量の Photoshop ドキュメント（PSD/PSB）を PNG 画像に変換する際、CPU に大きな負荷がかかります。**Interrupt Monitor** を変換ワーカーに紐付けることで、プログラムから処理を中断できるようになり、Web サービスやバッチジョブ、ユーザーが操作を取り消す可能性のある UI アプリケーションに最適です。

## Interrupt Monitor を使用するメリット

- **レスポンシブな UI:** 大きなファイルを処理中でもアプリケーションがフリーズしません。  
- **リソース管理:** 時間やメモリの上限を超えた変換を自動的に停止できます。  
- **エラーハンドリング:** 割り込みが発生した際に、部分的に生成された出力ファイルを安全にクリーンアップできます。

## 前提条件

- Java 開発環境（JDK 8 以上）。  
- Aspose.PSD for Java ライブラリ – **[こちらからダウンロード](https://releases.aspose.com/psd/java/)**。  
- 変換対象の PSD/PSB ファイルが格納されたフォルダー。

## パッケージのインポート

必要なクラスをインポートします。これにより、画像オプション、Interrupt Monitor、スレッドユーティリティにアクセスできます。

```java
import com.aspose.psd.ImageOptionsBase;

import static com.aspose.psd.examples.Utils.Utils.getDateTime;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.multithreading.InterruptMonitor;
import com.aspose.psd.system.Threading.ThreadStart;
import java.io.File;
```

## 手順ガイド

### 手順 1: ドキュメントディレクトリを設定

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` を PSD ファイルが保存されている絶対パスに置き換えてください。

### 手順 2: 画像オプションと出力パスを定義

```java
ImageOptionsBase saveOptions = new PngOptions();
String source = dataDir + "big2.psb";
String output = dataDir + "big_out.png";
```

ここでは `PngOptions` を使用して **PSD を PNG として保存**しています。必要に応じてファイル名を変更してください。

### 手順 3: Interrupt Monitor と SaveImageWorker を初期化

```java
InterruptMonitor monitor = new InterruptMonitor();
SaveImageWorker worker = new SaveImageWorker(source, output, saveOptions, monitor);
```

`InterruptMonitor` インスタンスは後で変換を停止するために使用します。`SaveImageWorker` が監視対象の変換タスクとモニターを結び付けます。

### 手順 4: 別スレッドで画像変換を開始

```java
Thread thread = new Thread(worker.ThreadProc());
try {
    thread.start();
    // Add a timeout to allow for potential interruption
    Thread.sleep(3000);
```

変換処理をバックグラウンドスレッドで実行し、メインスレッドは応答性を保ちます。`Thread.sleep(3000)` はタイムアウトシナリオをシミュレートしています。

### 手順 5: プロセスを割り込む（Java スレッド割り込み例）

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

`monitor.interrupt()` を呼び出すことで **割り込みロジック** がトリガーされます。割り込み後は、途中で書き込まれた PNG ファイルをクリーンアップします。

## よくある問題と解決策

| 問題 | 原因 | 対策 |
|------|------|------|
| 変換が停止しない | Monitor が Worker にリンクされていない | `SaveImageWorker` に同じ `InterruptMonitor` インスタンスを渡しているか確認してください。 |
| 割り込み後も出力ファイルが残る | クリーンアップコードが実行されていない | `finally` ブロックが確実に実行され、ファイルパスが正しいか確認してください。 |
| 大容量 PSB ファイルで `OutOfMemoryError` が発生 | ストリーミングオプション未使用 | メモリ効率の良いロードを可能にする `LoadOptions` を使用してください。 |

## FAQ（よくある質問）

### Q1: Aspose.PSD for Java の Interrupt Monitor とは何ですか？

A1: Interrupt Monitor は、開発者が **画像変換プロセスを管理・割り込み**できる機能で、長時間実行されるタスクに対して細かな制御を提供します。

### Q2: Aspose.PSD for Java ライブラリはどこで入手できますか？

A2: **[こちらからダウンロード](https://releases.aspose.com/psd/java/)** できます。

### Q3: Aspose.PSD for Java の無料トライアルはありますか？

A3: はい、**[こちら](https://releases.aspose.com/)** から無料トライアルをご利用いただけます。

### Q4: Aspose.PSD for Java のサポートはどこで受けられますか？

A4: Aspose.PSD for Java のサポートフォーラムは **[こちら](https://forum.aspose.com/c/psd/34)** です。

### Q5: Aspose.PSD for Java のライセンスはどこで購入できますか？

A5: **[こちら](https://purchase.aspose.com/buy)** からライセンスをご購入いただけます。

---

**最終更新日:** 2025-12-25  
**テスト環境:** Aspose.PSD 24.11 for Java  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}