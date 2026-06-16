---
date: 2026-04-12
description: 學習如何使用 Aspose.PSD for Java 保存包含字型的 PSD 並強制字型快取，以提升影像效能並有效處理缺失的字型。
keywords:
- save psd with fonts
- java thread sleep
- improve image performance
- load psd image
- handle missing fonts
linktitle: 強制字型快取
second_title: Aspose.PSD Java API
title: 儲存含字型的 PSD 並強制字型快取 – Aspose.PSD Java
url: /zh-hant/java/advanced-image-manipulation/force-font-cache/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.PSD for Java 保存 PSD 並強制字型快取

## 介紹

如果您需要快速 **保存 PSD 並保留字型**，同時確保正確的字型可用，這裡就是您的最佳去處。字型快取可以顯著 **提升影像效能**，尤其在重複處理大型 Photoshop 文件時更為明顯。在本教學中，我們將逐步說明如何強制更新字型快取、**載入 PSD 影像** 檔案，最後使用 Aspose.PSD for Java **保存 PSD 並保留字型**。

## 快速答覆
- **強制字型快取會做什麼？** 會迫使 Aspose.PSD 重新掃描系統字型，使新安裝的字型即時被辨識。  
- **字型安裝需要等多久？** 範例程式會暫停 **2 分鐘**，通常足以完成手動安裝。  
- **這能套用在任何 PSD 檔案嗎？** 可以，只要檔案可存取且系統已安裝所需字型。  
- **執行此程式碼需要授權嗎？** 生產環境需要臨時或正式授權；免費試用版可用於評估。  
- **支援哪些 Java 版本？** Aspose.PSD for Java 支援 JDK 8 及以上版本。

## 什麼是「保存 PSD 並保留字型」以及為何重要？

在對圖層、文字或字型進行操作後，將 PSD 檔案儲存下來是讓變更永久化的最後一步。若字型快取未即時更新，儲存的檔案可能會退回使用預設字型，導致視覺不一致。先強制更新快取，可確保 **保存 PSD 並保留字型** 的操作會嵌入正確的字型。

## 為何要使用 Aspose.PSD 強制字型快取？

- **效能提升** – 減少重複的字型查詢。  
- **可靠性** – 確保儲存的 PSD 檔案在任何機器上都能如預期呈現。  
- **簡易性** – 只需呼叫一次方法 (`OpenTypeFontsCache.updateCache()`) 即可完成繁重工作。

## 前置條件

開始之前，請確保您已具備：

- 已安裝 Java Development Kit (JDK) 8 或更新版本。  
- Aspose.PSD for Java 套件（可從官方 [download link](https://releases.aspose.com/psd/java/) 下載）。  
- 一個範例 PSD 檔案（`sample.psd`），放置於程式碼可參照的資料夾中。  

所有準備就緒後，讓我們深入實作。

## 匯入套件

首先，匯入處理 PSD 影像與字型快取所需的類別，將以下程式碼放在 Java 類別的最上方：

```java
import com.aspose.psd.Image;
import com.aspose.psd.OpenTypeFontsCache;

import com.aspose.psd.fileformats.psd.PsdImage;
import java.io.Console;
import java.util.concurrent.TimeUnit;
```

## 步驟說明

### 步驟 1：載入 PSD 影像（How to load PSD image）

我們先載入原始 PSD 檔案，取得基礎的影像物件，之後在更新字型快取後再重新儲存。

```java
String dataDir = "Your Document Directory";

PsdImage image = (PsdImage)Image.load(dataDir + "sample.psd");
image.save(dataDir + "NoFont.psd");
```

- **說明：**  
  - `Image.load` 會將檔案讀入記憶體。  
  - `image.save` 會產生一個名為 **NoFont.psd** 的副本，反映 **字型尚未更新** 前的狀態。  
  - 此步驟可用於比較，確保後續的快取更新真的會改變輸出結果。

### 步驟 2：等待字型安裝（java thread sleep – improve image performance）

現在給使用者時間手動安裝所需字型。實務上您可能會自動化此步驟，但此暫停可示範快取重新整理的機制。

```java
System.out.println("You have 2 minutes to install the font");
Thread.sleep(2 * 60 * 1000);
OpenTypeFontsCache.updateCache();
```

- **說明：**  
  - `Thread.sleep`（即 **java thread sleep**）會使執行暫停 **2 分鐘**（2 × 60 × 1000 ms）。  
  - `OpenTypeFontsCache.updateCache()` 會強制 Aspose.PSD 重新掃描系統的 OpenType 字型，使新安裝的字型立即可供渲染。  
  - 這段暫停有助於 **提升影像效能**，確保快取在下一次載入前已反映最新字型。

### 步驟 3：載入更新後的 PSD 影像並 **保存 PSD 並保留字型**

快取重新整理完成後，我們再次載入原始 PSD。此時字型資訊已是最新的，便可正確 **保存 PSD 並保留字型**。

```java
PsdImage image1 = (PsdImage)Image.load(dataDir + "sample.psd");
image1.save(dataDir + "HasFont.psd");
```

- **說明：**  
  - 第二次載入會取得剛安裝的字型。  
  - 儲存為 **HasFont.psd** 後，檔案將包含正確的字型渲染，證明快取更新已生效。

## 常見問題與解決方案

| 問題 | 原因 | 解決方式 |
|------|------|----------|
| 儲存的 PSD 仍顯示預設字型 | 字型未安裝在系統掃描的路徑 | 將字型安裝至系統字型資料夾（例如 Windows 的 `C:\Windows\Fonts`），再重新執行 `updateCache()`。 |
| `Thread.sleep` 拋出 `InterruptedException` | 方法簽章未處理受檢例外 | 在 `main` 方法上加入 `throws InterruptedException`，或將呼叫包在 try‑catch 區塊中。 |
| `OpenTypeFontsCache.updateCache()` 沒有作用 | 在無字型設定的無頭伺服器上執行 | 確認伺服器已安裝所需字型，且 Java 行程有讀取權限。 |
| **處理缺少的字型** – PSD 以備用字型呈現 | 字型檔案損毀或無法存取 | 檢查字型檔案完整性，並確保 Java 行程具備讀取權限。 |

## 常見問答

**Q: Aspose.PSD 是否相容所有 Java 版本？**  
A: Aspose.PSD for Java 支援 JDK 8 及以上版本，涵蓋大多數現代 Java 應用。

**Q: 我可以將 Aspose.PSD 用於商業專案嗎？**  
A: 可以。商業環境需要正式授權，您可於 [purchase page](https://purchase.aspose.com/buy) 取得。

**Q: 有免費試用版嗎？**  
A: 當然！可從 [releases page](https://releases.aspose.com/) 下載試用版。

**Q: 我該去哪裡取得社群支援？**  
A: 歡迎加入 [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) 交流技巧與除錯經驗。

**Q: 如何取得測試用的臨時授權？**  
A: 前往 [temporary license page](https://purchase.aspose.com/temporary-license/) 申請短期授權。

## 結論

現在您已學會在強制更新字型快取後 **保存 PSD 並保留字型**，確保每次輸出的 PSD 都使用正確的字型。此技巧是 **影像處理最佳化** 中簡單卻強大的環節，亦可整合至需要可靠高效 PSD 操作的更大型工作流程中。

---

**最後更新：** 2026-04-12  
**測試環境：** Aspose.PSD for Java 24.12（撰寫時最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}