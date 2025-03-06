---
title: 在 Java 中將 AI 轉換為 PSD
linktitle: 在 Java 中將 AI 轉換為 PSD
second_title: Aspose.PSD Java API
description: 透過我們簡單的逐步指南，使用 Aspose.PSD 在 Java 中將 AI 轉換為 PSD。非常適合需要快速無縫文件轉換的開發人員。
weight: 14
url: /zh-hant/java/java-ai-to-image-format-conversion/convert-ai-to-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Java 中將 AI 轉換為 PSD

## 介紹
您是否希望使用 Java 將 AI (Adobe Illustrator) 檔案轉換為 PSD (Adobe Photoshop) 檔案？嗯，您來對地方了！今天，我們將探討如何使用強大的 Aspose.PSD for Java 程式庫來完成此任務。本指南將引導您完成您需要了解的所有內容，從先決條件到詳細的逐步說明。讓我們深入研究並無縫轉換您的設計文件。
## 先決條件
在我們開始之前，您需要準備好一些東西：
1. Java 開發工具包 (JDK)：確保您的系統上安裝了 JDK 8 或更高版本。
2.  Aspose.PSD for Java：從下列位置下載 Aspose.PSD for Java 函式庫[下載頁面](https://releases.aspose.com/psd/java/).
3. 整合開發環境 (IDE)：用於編寫和執行 Java 程式碼的 IDE（例如 IntelliJ IDEA 或 Eclipse）。
4. AI 檔案：要轉換的 Adobe Illustrator 檔案。
5.  Aspose 臨時許可證（可選）：要獲得無限制的完整功能，您可以獲得[臨時執照](https://purchase.aspose.com/temporary-license/).
## 導入包
首先，讓我們透過導入必要的套件來設定我們的專案。您需要在專案的類別路徑中包含 Aspose.PSD for Java。操作方法如下：
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.ai.AiImage;
import com.aspose.psd.imageoptions.PsdOptions;
```
或者，您可以從以下位置下載 JAR 檔案：[Aspose.PSD for Java 下載頁面](https://releases.aspose.com/psd/java/)並將其手動添加到您的項目中。
讓我們將這個過程分解為簡單、易於管理的步驟。
## 第 1 步：設定您的項目
首先，在您首選的 IDE 中設定您的專案。
### 建立一個新項目
1. 開啟 IDE 並建立新的 Java 專案。
2. 將您的專案命名為有意義的名稱，例如“AItoPSDConverter”。
### 新增Aspose.PSD庫
1. 如果您下載了 JAR 文件，請將其新增至專案的建置路徑。
2. 如果使用 Maven，請確保依賴項已正確新增至您的`pom.xml`.
## 第2步：載入AI文件
現在您的專案已設定完畢，讓我們載入要轉換的 AI 檔案。
```java
String dataDir = "Your Document Directory"; 
String sourceFileName = dataDir + "34992OStroke.ai";       
AiImage image = (AiImage) Image.load(sourceFileName);
```
## 第 3 步：設定 PSD 選項
接下來，我們需要設定 PSD 輸出的選項。
```java
PsdOptions options = new PsdOptions();
```
## 步驟 4：將 AI 檔案另存為 PSD
加載 AI 檔案並設定選項後，我們現在可以將其另存為 PSD 檔案。
```java
String outFileName = dataDir + "34992OStroke.psd";
image.save(outFileName, options);
```
## 結論
現在你就擁有了！您已使用 Aspose.PSD for Java 成功將 AI 檔案轉換為 PSD 檔案。這個功能強大的程式庫使您可以輕鬆地處理 Java 應用程式中的複雜檔案轉換。無論您是經驗豐富的開發人員還是剛入門，本指南都可以幫助您輕鬆將 AI 到 PSD 轉換功能整合到您的專案中。
## 常見問題解答
### 什麼是 Java 版 Aspose.PSD？
Aspose.PSD for Java 是一個強大的函式庫，可讓開發人員在 Java 應用程式中建立、編輯和轉換 Photoshop 檔案（PSD 和 PSB），而無需 Adobe Photoshop。
### 我可以免費使用 Aspose.PSD for Java 嗎？
 Aspose.PSD for Java 提供免費試用版，您可以從[免費試用頁面](https://releases.aspose.com/)。對於完整的功能，[執照](https://purchase.aspose.com/buy)是必須的。
### 如何取得 Aspose.PSD for Java 的臨時授權？
您可以從以下機構獲得臨時許可證[臨時許可證頁面](https://purchase.aspose.com/temporary-license/).
### 是否可以將 PSD 檔案轉換回 AI 檔案？
目前，Aspose.PSD for Java 不支援將 PSD 檔案轉換回 AI 檔案。它專注於處理 PSD 和 PSB 檔案。
### 在哪裡可以找到更多範例和文件？
您可以在以下位置找到全面的文件和範例[Aspose.PSD for Java 文件頁面](https://reference.aspose.com/psd/java/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
