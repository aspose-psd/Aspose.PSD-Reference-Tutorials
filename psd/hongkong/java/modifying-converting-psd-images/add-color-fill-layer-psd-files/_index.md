---
date: 2026-03-02
description: 了解如何使用 Java 與 Aspose.PSD 在 PSD 檔案中建立顏色填充圖層來添加填充。跟隨我們的逐步指南，快速設定填充圖層顏色。
linktitle: Add Color Fill Layer to PSD Files using Java
second_title: Aspose.PSD Java API
title: 如何添加填充：使用 Java 為 PSD 檔案添加顏色填充圖層
url: /zh-hant/java/modifying-converting-psd-images/add-color-fill-layer-psd-files/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Java 為 PSD 檔案新增顏色填充圖層

## 介紹
有沒有曾經需要以程式方式操作 Photoshop 檔案，或許是想為設計加入一抹顏色？如果你在尋找 **如何為 PSD 加入填充**，你來對地方了。在本教學中，我們將示範如何使用 Java 以及 Aspose.PSD 函式庫為 PSD（Photoshop Document）檔案新增顏色填充圖層。把你的 PSD 想像成一塊數位畫布——完成後，你將知道如何建立顏色填充圖層、設定填充圖層顏色，並僅用幾行程式碼儲存更新後的檔案。

## 快速回答
- **需要的函式庫是什麼？** Aspose.PSD for Java  
- **主要使用情境？** 以程式方式新增或變更 PSD 填充顏色  
- **實作需要多長時間？** 基本情境大約 10‑15 分鐘  
- **需要授權嗎？** 免費試用可用於評估；正式環境需購買商業授權  
- **支援的 Java 版本？** Java 8 及以上  

## 什麼是顏色填充圖層？
顏色填充圖層是一種實心顏色的覆蓋層，位於 Photoshop 文件中的其他圖層之上。它常用於加入背景顏色、建立遮罩，或在不編輯單一像素的情況下快速變更設計的視覺主題。

## 為什麼要以程式碼新增顏色填充圖層？
- **自動化：** 在大量檔案中產生一致的品牌資產。  
- **批次處理：** 只需數秒即可更新數十個 PSD，免於手動操作。  
- **動態設計：** 可根據使用者輸入或資料來源即時變更顏色。  

## 先決條件
在深入程式碼之前，先確保你已具備以下所有項目：

1. **Java Development Kit (JDK)** – 已安裝 JDK 8 或更新版本。  
2. **Aspose.PSD Library** – 從 [Aspose Releases page](https://releases.aspose.com/psd/java/) 下載最新的 JAR。  
3. **IDE** – IntelliJ IDEA、Eclipse、NetBeans，或任何你偏好的編輯器。  
4. **基本的 Java 知識** – 熟悉物件、迴圈與例外處理。  

## 匯入套件
現在基礎已備妥，讓我們匯入必要的類別。這些匯入讓我們能夠處理 PSD 以及填充圖層的操作。

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IColorFillSettings;
```

## 如何新增填充 – 步驟指南

### 步驟 1：設定環境
定義原始 PSD 的位置以及編輯後檔案的儲存路徑，然後載入文件。

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ColorFillLayer.psd";
String exportPath     = dataDir + "ColorFillLayer_output.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- `dataDir` 指向包含 PSD 的資料夾。  
- `sourceFileName` 為你將要修改的原始檔案。  
- `exportPath` 為寫入新增 **顏色填充圖層** 後新檔案的位置。  

### 步驟 2：遍歷圖層
我們需要找出所有現有的填充圖層，以便修改它們或建立新圖層。

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof FillLayer) {
        FillLayer fillLayer = (FillLayer) im.getLayers()[i];
```

- `for` 迴圈會遍歷 PSD 中的每一個圖層。  
- `instanceof FillLayer` 檢查確保我們只處理填充圖層。  

### 步驟 3：驗證填充類型
在嘗試變更顏色之前，先確認找到的圖層是 **顏色填充圖層**。

```java
if (fillLayer.getFillSettings().getFillType() != FillType.Color) {
    throw new Exception("Wrong Fill Layer");
}
```

如果填充類型不是 `FillType.Color`，我們會中止操作，以免意外更改漸層或圖案填充。

### 步驟 4：設定填充顏色
這裡是 **設定填充圖層顏色** 的地方。範例將圖層改為紅色，但你可以將 `Color.getRed()` 替換為任何其他需要的 `Color`（例如 `Color.getBlue()`、`new Color(255, 165, 0)` 代表橙色）。

```java
IColorFillSettings settings = (IColorFillSettings) fillLayer.getFillSettings();
settings.setColor(Color.getRed());
fillLayer.update();
```

- `settings.setColor(...)` 會變更實際的填充顏色。  
- `fillLayer.update()` 會重新整理圖層，使新顏色生效。  

### 步驟 5：儲存變更
最後，將修改過的 PSD 寫回磁碟。

```java
im.save(exportPath);
break;
```

- `break` 會在第一個符合條件的填充圖層更新後跳出迴圈，這通常是你只需要 **變更 PSD 填充顏色** 一次時的預期行為。  

## 常見問題與技巧
- **未找到 FillLayer：** 若你的 PSD 不含填充圖層，需要使用 `new FillLayer(im)` 建立一個，並將其加入 `im.getLayers()`。  
- **顏色未更新：** 設定顏色後務必呼叫 `fillLayer.update()`。  
- **檔案未儲存：** 確認 `exportPath` 指向可寫入的目錄，且你具備寫入權限。  

## 常見問答

**Q: 什麼是 Aspose.PSD？**  
A: Aspose.PSD 是一套功能強大的 Java 函式庫，讓你在不需 Adobe Photoshop 的情況下建立、編輯與轉換 Photoshop PSD 檔案。

**Q: 可以免費使用 Aspose.PSD 嗎？**  
A: 可以，免費試用版可在 [Aspose Releases page](https://releases.aspose.com/) 取得。  

**Q: 除了 PSD，還支援哪些檔案格式？**  
A: Aspose.PSD 支援 PSD、PSB、BMP、JPEG、PNG、GIF、TIFF 等多種格式。

**Q: 若遇到問題，如何取得支援？**  
A: 你可以在 [Aspose Support Forum](https://forum.aspose.com/c/psd/34) 提問。  

**Q: 哪裡可以購買完整授權？**  
A: 授權可透過 [Aspose Purchase page](https://purchase.aspose.com/buy) 購買。

## 結論
現在你已了解如何以 Java 程式方式 **為 Photoshop 文件新增填充**。透過建立或定位顏色填充圖層、設定其顏色，並儲存結果，你可以自動化重複的設計工作、產生動態資產，或將 PSD 操作整合到更大的 Java 應用程式中。試試看吧——嘗試不同的顏色、加入多個填充圖層，或將此技巧與其他 Aspose.PSD 功能結合，打造強大的影像處理管線。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-03-02  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose