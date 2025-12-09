---
date: 2025-12-01
description: 了解如何使用 Aspose.PSD for Java 保存 PSD 檔案、強制字型快取，並提升影像效能。一步一步的影像處理優化指南。
linktitle: Force Font Cache
second_title: Aspose.PSD Java API
title: 如何使用 Aspose.PSD for Java 儲存 PSD 檔案並強制字型快取
url: /zh-hant/java/advanced-image-manipulation/force-font-cache/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.PSD for Java 儲存 PSD 檔案並強制字型快取

## 簡介

如果您需要快速 **save PSD file** 物件，同時確保正確的字型已可用，您來對地方了。字型快取可以大幅 **improve image performance**，尤其在重複處理大型 Photoshop 文件時更為顯著。在本教學中，我們將逐步說明如何強制字型快取、載入 PSD 圖像，最後使用 Aspose.PSD for Java 以新安裝的字型 **save PSD file**。

## 快速答覆
- **強制字型快取會做什麼？** 它會迫使 Aspose.PSD 重新掃描系統字型，使新安裝的字型立即被識別。  
- **字型安裝需要等多久？** 範例程式會暫停 **2 分鐘**，通常足以完成手動安裝。  
- **這可以套用在任何 PSD 檔案嗎？** 可以——只要檔案可存取且系統已安裝所需字型。  
- **執行此程式碼需要授權嗎？** 生產環境需要臨時或正式授權；免費試用版可用於評估。  
- **支援哪些 Java 版本？** Aspose.PSD for Java 支援 JDK 8 及更新版本。

## 什麼是 “save PSD file” 為何重要？

在對圖層、文字或字型進行操作後，儲存 PSD 檔案是將變更永久寫入的最後一步。若字型快取未即時更新，儲存的檔案可能會退回使用預設字型，造成視覺不一致。先強制更新快取，可確保 **save PSD file** 動作嵌入正確的字型。

## 為什麼要使用 Aspose.PSD 強制字型快取？

- **效能提升** – 減少重複的字型查找。  
- **可靠性** – 保證儲存的 PSD 檔案在任何機器上都能如預期呈現。  
- **簡易性** – 單一方法呼叫 (`OpenTypeFontsCache.updateCache()`) 即可完成繁重工作。

## 前置條件

在開始之前，請確保您已具備：

- 已安裝 Java Development Kit (JDK) 8 或更新版本。  
- Aspose.PSD for Java 程式庫（可從官方 [download link](https://releases.aspose.com/psd/java/) 下載）。  
- 一個範例 PSD 檔案（`sample.psd`），放置於程式碼可參考的資料夾中。  

一切就緒後，讓我們深入實作。

## 匯入套件

首先，匯入操作 PSD 圖像與字型快取所需的類別。將以下語句放在 Java 類別的最上方：

```java
import com.aspose.psd.Image;
import com.aspose.psd.OpenTypeFontsCache;

import com.aspose.psd.fileformats.psd.PsdImage;
import java.io.Console;
import java.util.concurrent.TimeUnit;
```

### 步驟 1：載入 PSD 圖像（How to load PSD）

我們先載入原始 PSD 檔案，取得基礎的圖像物件，之後在字型快取更新後再重新儲存。

```java
String dataDir = "Your Document Directory";

PsdImage image = (PsdImage)Image.load(dataDir + "sample.psd");
image.save(dataDir + "NoFont.psd");
```

- **說明：**  
  - `Image.load` 會將檔案讀入記憶體。  
  - `image.save` 會產生一個名為 **NoFont.psd** 的副本，反映 **在任何新字型可用之前** 的狀態。  
  - 此步驟可用於比較，確保後續的快取更新真的會改變輸出結果。

### 步驟 2：等待字型安裝（Improve image performance）

現在給使用者時間手動安裝所需字型。實務上您可能會自動化此步驟，但此暫停可示範快取刷新機制。

```java
System.out.println("You have 2 minutes to install the font");
Thread.sleep(2 * 60 * 1000);
OpenTypeFontsCache.updateCache();
```

- **說明：**  
  - `Thread.sleep` 會暫停執行 **2 分鐘**（2 × 60 × 1000 ms）。  
  - `OpenTypeFontsCache.updateCache()` 會迫使 Aspose.PSD 重新掃描系統的 OpenType 字型，使任何新安裝的字型立即可供渲染。

### 步驟 3：載入更新後的 PSD 圖像（Load PSD image）並 **save PSD file**

快取刷新後，我們再次載入原始 PSD。此時字型資訊已是最新的，我們即可 **save PSD file** 並嵌入正確的字型。

```java
PsdImage image1 = (PsdImage)Image.load(dataDir + "sample.psd");
image1.save(dataDir + "HasFont.psd");
```

- **說明：**  
  - 第二次載入會取得新安裝的字型。  
  - 儲存為 **HasFont.psd** 後，檔案將包含正確的字型渲染，證明快取更新已生效。

## 常見問題與解決方案

| 問題 | 原因 | 解決方案 |
|------|------|----------|
| 儲存的 PSD 仍顯示預設字型 | 字型未安裝在系統掃描的路徑 | 將字型安裝至系統字型資料夾（例如 Windows 的 `C:\Windows\Fonts`），再重新執行 `updateCache()`。 |
| `Thread.sleep` 拋出 `InterruptedException` | 方法簽章未處理受檢查例外 | 在 `main` 方法上加入 `throws InterruptedException`，或將呼叫包在 try‑catch 區塊中。 |
| `OpenTypeFontsCache.updateCache()` 無效 | 在無字型設定的無頭伺服器上執行 | 確認伺服器已安裝所需字型，且 Java 行程有讀取權限。 |

## 常見問答

**Q: Aspose.PSD 是否相容所有 Java 版本？**  
A: Aspose.PSD for Java 支援 JDK 8 及更新版本，涵蓋大多數現代 Java 應用。

**Q: 我可以在商業專案中使用 Aspose.PSD 嗎？**  
A: 可以。生產環境必須購買商業授權。您可於 [purchase page](https://purchase.aspose.com/buy) 取得。

**Q: 有免費試用版嗎？**  
A: 當然！可從 [releases page](https://releases.aspose.com/) 下載試用版。

**Q: 我該去哪裡尋求社群支援？**  
A: 加入 [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) 交流技巧與除錯經驗。

**Q: 如何取得測試用的臨時授權？**  
A: 前往 [temporary license page](https://purchase.aspose.com/temporary-license/) 申請短期授權。

## 結論

現在您已學會在強制字型快取後 **save PSD file**，確保每次輸出的 PSD 都使用正確的字型。此技巧是 **image processing optimization** 中簡單卻強大的環節，可整合至需要可靠高效 PSD 操作的更大型工作流程中。

---

**最後更新：** 2025-12-01  
**測試環境：** Aspose.PSD for Java 24.12（撰寫時的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}