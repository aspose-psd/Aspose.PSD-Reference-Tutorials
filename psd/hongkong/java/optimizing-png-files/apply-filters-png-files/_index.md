---
date: 2026-03-15
description: 學習如何使用 Aspose.PSD for Java 來過濾 PNG 圖像。此一步一步的指南涵蓋 Java PNG 優化以及使用過濾類型將
  PSD 轉換為 PNG。
linktitle: How to Filter PNG Files in Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: 如何在 Aspose.PSD for Java 中過濾 PNG 檔案
url: /zh-hant/java/optimizing-png-files/apply-filters-png-files/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Aspose.PSD for Java 中過濾 PNG 檔案

## 介紹
如果你正在尋找 **如何過濾 PNG** 圖片的 Java 解決方案，你已經來對地方了。在本教學中，我們將示範如何使用 Aspose.PSD for Java 套件套用 PNG 過濾類型，該套件同時支援 **將 PSD 轉換為 PNG** 以及執行 **java png optimization**。完成後，你將能微調壓縮、提升視覺品質，並將此流程整合至任何 Java 專案。

## 快速回答
- **哪個函式庫支援 Java 中的 PNG 過濾？** Aspose.PSD for Java。  
- **哪種過濾器在大多數影像上提供最佳壓縮？** Paeth 過濾器（本範例使用）。  
- **執行程式碼是否需要授權？** 免費試用可供評估；正式上線需購買授權。  
- **可以在同一工作流程中將 PSD 轉換為 PNG 嗎？** 可以 – 載入 PSD 後以所需過濾器儲存為 PNG。  
- **需要哪個 Java 版本？** Java 8 或更新版本。

## 「how to filter png」實務上是什麼？
過濾 PNG 檔案是指在壓縮前選擇一種前處理演算法，以準備像素資料。過濾類型會影響檔案大小以及 PNG 儲存後的色彩保留程度。Aspose.PSD 透過 `PngOptions.setFilterType` 方法讓你直接控制此步驟。

## 為什麼使用 Aspose.PSD for Java 進行 PNG 最佳化？
- **完整的 PSD 支援：** 開啟、編輯、匯出 PSD 圖層，且不失真。  
- **內建過濾器選擇：** 可從 Paeth、Sub、Up、Average 或 None 中挑選。  
- **跨平台：** 在 Windows、Linux、macOS 上皆可執行，使用任何標準 JDK。  
- **無外部原生相依性：** 純 Java 實作，簡化部署。

## 前置條件
1. **Java Development Kit (JDK) 8+** – 確認 `java -version` 顯示 1.8 或更高。  
2. **IDE (IntelliJ IDEA、Eclipse 或 VS Code)** – 任一你熟悉的開發環境。  
3. **Aspose.PSD for Java 套件** – 從 [此處](https://releases.aspose.com/psd/java/) 下載。  
4. **基本的 Java 知識** – 了解類別、方法與檔案 I/O。

## 匯入套件
首先，將所需的 Aspose.PSD 類別匯入你的 Java 檔案：

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngFilterType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

> **小技巧：** 將 Aspose.PSD JAR 加入專案的建置路徑或 Maven/Gradle 相依性，讓匯入能順利解析。

## 步驟 1：設定文件目錄
定義存放來源 PSD 與過濾後 PNG 的資料夾路徑。

```java
String dataDir = "Your Document Directory"; // Adjust this path
```

將 `"Your Document Directory"` 替換為你機器上的絕對或相對路徑。

## 步驟 2：載入 PSD 圖像
開啟要處理的 PSD 檔案。將其轉型為 `PsdImage` 可取得 PSD 專屬功能。

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "sample.psd");
```

若檔案不存在，`Image.load` 會拋出例外 – 請確認路徑正確。

## 步驟 3：建立 PNG 選項（Java PNG 最佳化）
設定 PNG 匯出參數，包含直接回應 **how to filter png** 的過濾類型。

```java
PngOptions options = new PngOptions();
options.setFilterType(PngFilterType.Paeth);
```

你可以嘗試其他過濾類型（`Sub`、`Up`、`Average`、`None`），觀察其對檔案大小與品質的影響。此步驟同時說明 **java png optimization**，因為所選過濾器會影響壓縮效率。

## 步驟 4：儲存 PNG 圖像
最後，使用先前定義的選項將處理後的圖像寫回磁碟。

```java
psdImage.save(dataDir + "ApplyFilterMethod_out.png", options);
```

產生的檔案 `ApplyFilterMethod_out.png` 即為已過濾的 PNG，可直接用於網站或桌面應用。

## 常見問題與解決方案
| 症狀 | 可能原因 | 解決方式 |
|------|----------|----------|
| `FileNotFoundException` | `dataDir` 路徑不正確 | 確認目錄字串以分隔符 (`/` 或 `\\`) 結尾。 |
| 看不到過濾效果 | 使用了 `PngFilterType.None` | 改為 `Paeth` 或其他過濾類型。 |
| 大型 PSD 記憶體不足 | 未使用串流直接載入巨檔 | 使用 `PsdImage` 搭配 `loadOptions` 限制記憶體使用量。 |

## 常見問答

**Q: 什麼是 Aspose.PSD for Java？**  
A: Aspose.PSD for Java 是一套功能完整的 API，讓開發者能讀取、編輯、轉換 PSD 檔案、套用過濾器，並在不需要 Adobe Photoshop 的情況下執行影像最佳化。

**Q: 我要如何下載 Aspose.PSD for Java？**  
A: 可從 Aspose 釋出頁面 [此處](https://releases.aspose.com/psd/java/) 下載。

**Q: 可以免費試用 Aspose.PSD 嗎？**  
A: 可以，免費試用版可於 [此處](https://releases.aspose.com/) 取得。

**Q: 我可以對 PNG 圖片套用哪些類型的過濾器？**  
A: Aspose.PSD 支援 Paeth、Sub、Up、Average 與 None。依需求選擇最能平衡檔案大小與視覺保真度的過濾器。

**Q: 哪裡可以取得 Aspose.PSD 的支援？**  
A: 可前往 Aspose 論壇 [此處](https://forum.aspose.com/c/psd/34) 取得協助。

## 結論
現在你已掌握 **如何過濾 PNG** 檔案的技巧，並了解如何使用 Aspose.PSD for Java **將 PSD 轉換為 PNG**，以及透過不同過濾類型執行 **java png optimization**。試著玩弄各種過濾器，將此工作流程整合到你的影像處理管線，享受更小且高品質的 PNG 資產。

---

**最後更新：** 2026-03-15  
**測試環境：** Aspose.PSD for Java 24.10  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}