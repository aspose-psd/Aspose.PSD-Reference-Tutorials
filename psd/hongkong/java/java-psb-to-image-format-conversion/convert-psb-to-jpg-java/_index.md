---
title: 在Java中將PSB轉換為JPG
linktitle: 在Java中將PSB轉換為JPG
second_title: Aspose.PSD Java API
description: 使用 Aspose.PSD 在 Java 中輕鬆將 PSB 轉換為 JPG。請遵循我們的詳細指南進行無縫影像轉換。下載、試用併購買 Aspose.PSD。
weight: 10
url: /zh-hant/java/java-psb-to-image-format-conversion/convert-psb-to-jpg-java/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在Java中將PSB轉換為JPG

## 介紹
歡迎來到我們關於使用 Aspose.PSD for Java 將 PSB 檔案轉換為 JPG 格式的綜合指南！如果您正在處理 PSB 檔案（那些大型的分層 Photoshop 檔案）並且需要將它們轉換為更普遍支援的 JPG 格式，那麼您來對地方了。在本教程中，我們將逐步引導您完成該過程。最後，您將能夠輕鬆地將 PSB 檔案無縫轉換為 JPG。
## 先決條件
在深入學習本教程之前，我們先介紹一下先決條件。以下是您開始使用時所需的：
-  Java 開發工具包 (JDK)：確保您的系統上安裝了 JDK。您可以從[甲骨文網站](https://www.oracle.com/java/technologies/javase-downloads.html).
-  Aspose.PSD for Java 函式庫：從下列位置下載 Aspose.PSD for Java 函式庫：[下載頁面](https://releases.aspose.com/psd/java/).
- 開發環境：IntelliJ IDEA、Eclipse 等 IDE 或您選擇的任何文字編輯器。
- PSB 檔案：您要轉換的 PSB 檔案。
## 導入包
首先，讓我們導入必要的套件。這些導入對於使用 Aspose.PSD 庫和處理圖像轉換至關重要。
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.JpegOptions;
```
## 第 1 步：設定您的項目
在開始編碼之前，請設定您的 Java 專案。在 IDE 中建立新項目，並將 Aspose.PSD for Java 庫新增至專案的建置路徑。這將使您能夠使用 Aspose.PSD 提供的類別和方法。
## 第 2 步：載入 PSB 文件
要載入 PSB 文件，您需要指定文件的路徑並使用`PsdLoadOptions`配置載入過程。操作方法如下：
```java
String dataDir = "Your Document Directory"; //替換為您的目錄路徑
String sourceFileName = dataDir + "Simple.psb";
PsdLoadOptions options = new PsdLoadOptions();
PsdImage image = (PsdImage) Image.load(sourceFileName, options);
```
在此步驟中，我們將設定 PSB 檔案所在的目錄並將該檔案載入到`PsdImage`物件使用`PsdLoadOptions`.
## 步驟 3：配置 JPG 選項
現在您的 PSB 檔案已加載，您需要設定 JPG 轉換的選項。這包括指定 JPG 輸出的品質。
```java
JpegOptions jpgOptions = new JpegOptions();
jpgOptions.setQuality(95);
```
在這裡，我們正在創建一個`JpegOptions`物件並將品質設為 95。
## 步驟 4：將影像儲存為 JPG
設定選項後，您就可以將 PSB 檔案另存為 JPG。這是實際轉換發生的地方。
```java
image.save(dataDir + "Simple_output.jpg", jpgOptions);
```
此命令將載入的 PSB 影像以 JPG 格式儲存在指定目錄中，並使用定義的品質設定。
## 步驟 5：將影像另存為 PSB（可選）
如果您還想將修改後的映像另存為 PSB 文件，可以使用類似的命令來執行此操作：
```java
image.save(dataDir + "Simple_output.psb");
```
此步驟是可選的，但如果您需要保留原始 PSB 檔案的分層格式以及轉換後的 JPG，則非常有用。
## 結論
恭喜！您已使用 Aspose.PSD for Java 成功將 PSB 檔案轉換為 JPG。本教學引導您完成專案設定、載入 PSB 檔案、配置 JPG 選項以及儲存轉換後的映像。透過執行以下步驟，您可以在 Java 應用程式中輕鬆處理 PSB 到 JPG 的轉換。
無論您是從事影像處理應用程式的開發人員還是只是偶爾需要轉換 PSB 文件，Aspose.PSD for Java 都能為您的需求提供強大的解決方案。
## 常見問題解答
### 什麼是 Java 版 Aspose.PSD？
Aspose.PSD for Java 是一個函式庫，允許開發人員在 Java 應用程式中操作和轉換 PSD 和 PSB 檔案。它支援各種功能，包括載入、編輯和保存 Photoshop 檔案。
### 我可以在購買前試用 Aspose.PSD for Java 嗎？
是的，您可以從以下位置下載 Aspose.PSD for Java 的免費試用版：[下載頁面](https://releases.aspose.com/)。這使您可以在購買之前評估該庫及其功能。
### 如何取得 Aspose.PSD for Java 的臨時授權？
您可以從以下機構獲得臨時許可證[臨時許可證頁面](https://purchase.aspose.com/temporary-license/)。這將允許您在有限的時間內使用該庫的全部功能。
### 如果我遇到問題可以獲得支援嗎？
絕對地！您可以透過以下方式獲得支持[Aspose.PSD 支援論壇](https://forum.aspose.com/c/psd/34)。支援團隊反應迅速，隨時準備協助您解決可能遇到的任何問題。
### 我可以調整 JPG 輸出的品質嗎？
是的，您可以透過設定來調整 JPG 輸出的質量`Quality`財產在`JpegOptions`目的。值範圍從 0 到 100，數值越高表示品質越好，壓縮率越低。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
