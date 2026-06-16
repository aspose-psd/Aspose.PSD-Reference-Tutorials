---
date: 2026-03-07
description: 學習如何使用 Java 與 Aspose.PSD 在執行時向 PSD 檔案加入文字。跟隨本步驟指南，快速在 PSD 中建立文字圖層。
linktitle: Add Text Layer on Runtime in PSD Files using Java
second_title: Aspose.PSD Java API
title: 使用 Java 在執行時向 PSD 檔案添加文字
url: /zh-hant/java/modifying-converting-psd-images/add-text-layer-runtime-psd-files/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Java 在執行時為 PSD 檔案加入文字

## 介紹
如果你曾經手動編輯過 Photoshop 文件，你就會知道圖層有多強大。假如你可以從 Java 應用程式自動 **add text to PSD** 檔案呢？使用 Aspose.PSD for Java 函式庫，你可以在執行時於 PSD 中建立文字圖層，開啟批次處理、動態圖形產生以及自動化品牌工作流程的大門。本教學將逐步說明整個流程，從專案設定到儲存更新後的檔案。

## 快速解答
- **需要哪個函式庫？** Aspose.PSD for Java.  
- **可以在既有 PSD 中加入文字嗎？** 可以 – 只要載入檔案、加入 `TextLayer`，然後儲存。  
- **正式環境需要授權嗎？** 非評估用途必須取得商業授權。  
- **支援哪個 Java 版本？** JDK 8 或以上（建議使用最新的 LTS 版）。  
- **適用於 Web 後端嗎？** 當然 – API 可在任何基於 Java 的伺服器環境中運作。

## 什麼是「add text to PSD」？
在 PSD 中加入文字指的是以程式方式在 Photoshop 文件內建立新的文字圖層。此圖層的行為與其他 Photoshop 文字圖層相同：可以移動、編輯內容、套用樣式——全部不需開啟 Photoshop。

## 為什麼要使用 Java 在 PSD 中建立文字圖層？
- **自動化** – 大量產生行銷素材、浮水印或產品標籤。  
- **一致性** – 確保數千個檔案使用相同的字型、大小與位置。  
- **整合** – 與其他 Java 服務（電商、報表、CI 流程）結合，即時產出圖形。

## 前置條件
在撰寫程式碼之前，請先確認你已具備以下項目：

1. **Java Development Kit (JDK)** – 安裝 JDK 8 或更新版本。你可以在此[下載](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)。
2. **Aspose.PSD for Java** – 從[Aspose 釋出頁面](https://releases.aspose.com/psd/java/)取得最新的 JAR。
3. **IDE（可選但有助）** – IntelliJ IDEA、Eclipse，或任何你偏好的編輯器。
4. **基本的 Java 知識** – 需要熟悉類別、物件與檔案 I/O。
5. **範例 PSD** – 本教學將使用 `OneLayer.psd`，放置於你自行選擇的資料夾中。

## 匯入套件
首先，匯入處理 PSD 檔案與文字圖層所需的類別。

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
```

這些匯入讓你能使用 Aspose.PSD 的核心功能。

## 步驟說明

### 步驟 1：設定文件目錄
定義存放來源 PSD 以及輸出檔案的資料夾。

```java
String dataDir = "Your Document Directory"; 
```

將 `"Your Document Directory"` 替換為你的檔案之絕對或相對路徑。

### 步驟 2：載入來源 PSD 檔案
使用 `Image.load()` 將既有 PSD 載入記憶體。

```java
String sourceFileName = dataDir + "OneLayer.psd"; 
Image img = Image.load(sourceFileName);
```

若路徑正確，`img` 便代表已載入的 Photoshop 文件。

### 步驟 3：轉型為 `PsdImage`
因為我們要使用 Photoshop 專屬功能，需將通用的 `Image` 轉型為 `PsdImage`。

```java
PsdImage im = (PsdImage)img;
```

此轉型即可使用 `addTextLayer()` 等方法。

### 步驟 4：定義文字圖層的矩形區域
指定新文字顯示的位置。矩形定義了座標 (x, y) 與尺寸 (寬度, 高度)。

```java
Rectangle rect = new Rectangle(
    (int)(im.getWidth() * 0.25),
    (int)(im.getHeight() * 0.25),
    (int)(im.getWidth() * 0.5),
    (int)(im.getHeight() * 0.5)
);
```

可自行調整計算式以符合版面需求。

### 步驟 5：加入文字圖層
在先前定義的矩形內建立實際的文字圖層。

```java
TextLayer layer = im.addTextLayer("Added text", rect);
```

將 `"Added text"` 替換為你想在 PSD 中顯示的任意字串。這裡即是以程式方式 **create text layer PSD**。

### 步驟 6：儲存更新後的 PSD 檔案
將修改後的文件寫入新檔，以免覆寫原始檔案。

```java
String psdPath = dataDir + "ImageWithTextLayer.psd";
im.save(psdPath);
```

執行完畢後，你會在目標資料夾看到 `ImageWithTextLayer.psd`，其中已包含新的文字圖層。

## 常見問題與解決方案
| Issue | Reason | Fix |
|-------|--------|-----|
| **`NullPointerException` on `im.addTextLayer`** | PSD 未正確載入（路徑錯誤）。 | 確認 `sourceFileName` 指向現有的 PSD 檔案。 |
| **Text not visible** | 矩形位於畫布外或圖層被隱藏。 | 調整矩形座標，或使用 `layer.setVisible(true)` 檢查圖層可見性。 |
| **LicenseException** | 在正式環境未使用有效授權即使用函式庫。 | 取得商業授權，並透過 `License license = new License(); license.setLicense("Aspose.PSD.lic");` 設定。 |

## 常見問答

**Q: 可以加入多個文字圖層嗎？**  
A: 可以 – 只要對每段要插入的文字重複步驟 4 與 5。

**Q: 如何設定文字樣式（字型、大小、顏色）？**  
A: `TextLayer` 類別提供 `getTextData()` 方法，可修改 `Font`、`FontSize`、`Color` 以及其他樣式屬性。請參考 Aspose.PSD API 文件取得完整說明。

**Q: 如果我的 PSD 已經有很多圖層怎麼辦？**  
A: Aspose.PSD 能處理複雜的圖層結構。你可以針對特定群組，或使用 `addTextLayer` 的多載版本在指定索引插入新文字圖層。

**Q: 這種做法適合用於 Web 應用程式嗎？**  
A: 絕對適合。只要伺服器執行 Java，即可即時產生或修改 PSD，並提供給用戶端。

**Q: 若遇到問題該向哪裡尋求協助？**  
A: 前往 [Aspose 支援論壇](https://forum.aspose.com/c/psd/34)，社群與 Aspose 工程師皆可提供協助。

## 結論
現在你已了解如何使用 Java 與 Aspose.PSD 在執行時輕鬆 **add text to PSD** 檔案。此技術讓你能自動化圖形產生、客製化資產，並將 Photoshop 級別的編輯整合至任何基於 Java 的解決方案。探索 Aspose.PSD API 的其他功能，加入形狀、點陣圖層，甚至套用濾鏡，以實現更豐富的自動化。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最後更新：** 2026-03-07  
**測試環境：** Aspose.PSD for Java 24.12（撰寫時的最新版本）  
**作者：** Aspose