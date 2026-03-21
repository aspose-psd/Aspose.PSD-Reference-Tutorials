---
date: 2026-03-21
description: Aspose.PSD for Java を使用して画像をエクスポートし、PSD をラスタ画像に変換し、マルチスレッド環境で一時ファイルを削除する方法を学びましょう。パフォーマンスを向上させ、作業環境をクリーンに保ちます。
linktitle: Export Images in Multi‑Threaded Environment
second_title: Aspose.PSD Java API
title: マルチスレッド環境で画像をエクスポートする際に一時ファイルを削除する方法 – Aspose.PSD for Java
url: /ja/java/psd-conversion/export-images-multi-thread/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# マルチスレッド画像エクスポートチュートリアル – Aspose.PSD for Java  

Are you looking to **delete temporary files** while enhancing your Java application's image export capabilities in a multi‑threaded environment? Aspose.PSD for Java makes it easy to **convert PSD to raster**, work with **save pixels java**, and keep your file system tidy. In this tutorial we’ll walk you through a complete, production‑ready example that shows how to export images, manage threads safely, and clean up any leftover files automatically.

## クイック回答
- **Aspose.PSD は一時ファイルを自動的に削除できますか？** はい – 処理後にプログラムで削除できます。  
- **マルチスレッド画像処理はサポートされていますか？** もちろんです。ライブラリは同時エクスポートに対してスレッドセーフです。  
- **Java でピクセルデータを保存するメソッドはどれですか？** `RasterImage` インスタンスの `savePixels`。  
- **本番で使用するにはライセンスが必要ですか？** 有効な Aspose.PSD ライセンスが必要です。無料トライアルが利用可能です。  
- **対応している Java バージョンは何ですか？** Java 1.7 以降。

## 画像エクスポートにおける「delete temporary files」とは何ですか？
When you export images from a PSD file, you often create intermediate files (e.g., copies of the source PSD, temporary raster data). Deleting these temporary files prevents disk clutter, reduces storage costs, and avoids accidental reuse of stale data.

## マルチスレッド画像処理に Aspose.PSD を使用する理由
- **高性能:** ボトルネックなしで複数の PSD ファイルを並列に処理します。  
- **スレッドセーフ:** コア API は複数スレッドからのアクセスでも正しく動作するよう設計されています。  
- **豊富な機能セット:** PSD をラスタ形式に直接変換し、レイヤーを編集、**save pixels java** を細かく制御できます。  
- **組み込みクリーンアップ:** 一時ファイルを削除するタイミングと方法を自分で決められ、リソース管理を完全にコントロールできます。

## 前提条件
- Java プログラミングの基本知識。  
- Java 開発環境 (JDK 1.7 以上)。  
- Aspose.PSD for Java ライブラリをダウンロードしてインストールします。ダウンロードリンクは[here](https://releases.aspose.com/psd/java/)にあります。

## パッケージのインポート
Add the required imports to your Java class. These classes give you access to color handling, raster image manipulation, and stream‑based loading.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.StreamSource;
import com.aspose.psd.system.io.FileStream;
import java.io.File;
import java.io.FileInputStream;
import java.io.FileNotFoundException;
```

## 手順 1: ドキュメントディレクトリの設定  
Specify where your source PSD files live. Keeping the path in a variable makes it easy to reuse across threads.

```java
String dataDir = "Your Document Directory";
```

## 手順 2: PSD 画像の読み込み  
Open the PSD file as a stream and configure `PsdOptions` so Aspose.PSD knows where to read the data from.

```java
String imageDataPath = dataDir + "sample.psd";
FileInputStream fileStream = new FileInputStream(imageDataPath);
PsdOptions psdOptions = new PsdOptions();
psdOptions.setSource(new StreamSource(fileStream));
```

## 手順 3: 画像の処理 – Convert PSD to Raster と Save Pixels  
Create a `RasterImage` from the PSD options, modify a few pixels, and then save the raster data back to the file system. This demonstrates **convert psd to raster** and the **save pixels java** workflow.

```java
RasterImage image = (RasterImage)Image.create(psdOptions, 10, 10);
Color[] pixels = new Color[4];
for (int i = 0; i < 4; ++i) {
    pixels[i] = Color.fromArgb(40, 30, 20, 10);
}
image.savePixels(new Rectangle(0, 0, 2, 2), pixels);
image.save();
```

## 手順 4: クリーンアップ – Delete Temporary Files  
After the export finishes, it’s a best practice to delete any temporary files you created (including the original PSD if it was a copy). This is the core of our **delete temporary files** strategy.

```java
File f = new File(imageDataPath);
if (f.exists()) {
    f.delete();
}
```

> **プロのコツ:** クリーンアップコードを `finally` ブロックでラップするか、Java の try‑with‑resources を使用して、例外が発生した場合でも削除が保証されるようにします。

## よくある問題と解決策
| Issue | Reason | Fix |
|-------|--------|-----|
| `FileNotFoundException` on `FileInputStream` | パスが間違っているか、ファイル権限が不足しています。 | `dataDir` を確認し、アプリケーションに読み書き権限があることを確認してください。 |
| Images not saved correctly | `savePixels` 後に `image.save()` を呼び出していない | `image.save()` がピクセル変更後に実行されていることを確認してください。 |
| Temporary files remain after crash | クリーンアップコードに到達しない | シャットダウンフックまたは finally ブロックを使用して削除を保証してください。 |

## よくある質問

### Aspose.PSD はすべての Java バージョンと互換性がありますか？
Aspose.PSD は Java 1.7 以降のバージョンと互換性があります。

### Aspose.PSD を使用して複数の画像を同時に処理できますか？
はい、Aspose.PSD はマルチスレッドをサポートしており、複数の画像を同時に処理できます。

### Aspose.PSD の追加ドキュメントはどこで見つけられますか？
ドキュメントは[here](https://reference.aspose.com/psd/java/)をご参照ください。

### Aspose.PSD for Java の無料トライアルはありますか？
はい、無料トライアルは[here](https://releases.aspose.com/)から利用できます。

### Aspose.PSD の一時ライセンスはどのように取得できますか？
一時ライセンスは[this link](https://purchase.aspose.com/temporary-license/)から取得してください。

**Additional Q&A**

**Q:** What is the best way to manage a pool of worker threads for image export?  
**A:** Use `java.util.concurrent.ExecutorService` (e.g., `Executors.newFixedThreadPool`) to submit export tasks and let the framework handle thread lifecycle.

**Q:** Can I export to formats other than PSD?  
**A:** Yes, Aspose.PSD can save raster images to PNG, JPEG, BMP, and many other formats via the appropriate `ImageOptions` class.

**Q:** How do I ensure thread safety when sharing a `RasterImage` instance?  
**A:** Do not share the same `RasterImage` across threads; instantiate a separate image per task or synchronize access if sharing is unavoidable.

## 結論
In this tutorial we explored how to **delete temporary files** while exporting images with Aspose.PSD for Java in a **multi‑threaded** environment. You learned to **convert PSD to raster**, manipulate pixel data using **save pixels java**, and keep your workspace clean by programmatically removing temporary files. Apply these patterns to boost performance, reduce storage overhead, and build robust Java image‑processing pipelines.

---

**Last Updated:** 2026-03-21  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}