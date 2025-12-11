---
date: 2025-12-09
description: 學習如何在 PSD 檔案中使用 Aspose.PSD for Java 連結圖層。此逐步教學將向您展示如何管理 PSD 圖層、解除圖層連結，並精通
  Aspose.PSD 教程。
linktitle: How to Link Layers in PSD Files Using Java
second_title: Aspose.PSD Java API
title: 如何使用 Java 連結 PSD 檔案中的圖層
url: /zh-hant/java/advanced-psd-layer-features-effects/add-linked-layer-support-psd-files/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}  
{{< blocks/products/pf/main-container >}}  
{{< blocks/products/pf/tutorial-page-section >}}  

# 如何在 PSD 檔案中使用 Java 連結圖層  

## 介紹  
Adobe Photoshop 的 `.PSD` 格式是層次化圖形的業界標準，許多開發人員需要以程式方式操作這些圖層。最強大的技巧之一是 **連結圖層**，它讓您可以將一組圖層作為單一單位移動或編輯，同時保留每個圖層的個別屬性。在本 **Aspose.PSD 教學** 中，我們將逐步說明 **如何在 PSD 檔案中使用 Java 連結圖層**，並展示如何 **管理 PSD 圖層**、**解除連結圖層 PSD**，以及將變更儲存回磁碟。無論您是建立設計自動化管線或是擴充桌面應用程式，這些步驟都能讓您完整掌控圖層之間的關係。  

## 快速解答  
- **「連結圖層」是什麼意思？** 它會建立一個邏輯群組，使圖層在移動時一起移動，且不會被合併。  
- **哪個函式庫負責此功能？** Aspose.PSD for Java 提供 `LinkedLayersManager` API。  
- **需要授權嗎？** 開發階段可使用免費試用版；正式環境需購買商業授權。  
- **之後可以解除連結嗎？** 可以——使用 `unlinkLayer` 或 `unlinkLayers` 方法。  
- **支援的 Java 版本？** Java 8 或以上。  

## 什麼是 PSD 檔案中的連結圖層？  
連結圖層是 Photoshop 的一項功能，可將多個圖層綁定在一起，使它們在變形、移動或樣式調整時表現為單一實體。底層資料仍保持分離，這意味著您之後可以 **解除連結圖層 PSD**，並獨立編輯每個圖層。  

## 為什麼要使用 Aspose.PSD for Java 來管理 PSD 圖層？  
- **功能完整的 API** – 在不啟動 Photoshop 的情況下存取所有 Photoshop 結構。  
- **跨平台** – 可在任何支援 Java 的作業系統上執行。  
- **無 UI 依賴** – 非常適合伺服器端批次處理或 CI 管線。  

## 前置條件  
在開始撰寫程式碼之前，請確保您已具備以下項目：  

1. **Java Development Kit (JDK) 8+** – 建議使用最新 JDK。  
2. **Aspose.PSD for Java** – 從 [Aspose 釋出頁面](https://releases.aspose.com/psd/java/) 下載。  
3. **IDE 或編輯器** – Eclipse、IntelliJ IDEA、VS Code 等。  
4. **範例 PSD 檔案** – 可在 Photoshop 中自行建立，或取得免費測試樣本。  

## 匯入套件  
撰寫程式碼前，先匯入必要的 Aspose.PSD 類別：  

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
```  

這些匯入讓您可以存取核心影像處理、PSD 專屬功能以及圖層操作方法。  

## 步驟說明  

### 步驟 1：載入 PSD 檔案  
首先，開啟您要處理的 PSD 檔案。  

```java
String dataDir = "Your Document Directory"; // specify your document directory
PsdImage psd = (PsdImage) Image.load(dataDir + "LinkedLayerexample.psd");
```  

請確保路徑指向現有檔案；否則 `Image.load()` 會拋出例外。  

### 步驟 2：取得全部圖層（管理 PSD 圖層）  
抓取所有圖層，以便決定要將哪些圖層分組。  

```java
Layer[] layers = psd.getLayers();
```  

`layers` 陣列現在包含文件的完整圖層堆疊。  

### 步驟 3：連結圖層  
使用管理員 API 建立連結圖層群組。  

```java
short layersLinkGroupId = psd.getLinkedLayersManager().linkLayers(layers);
```  

此呼叫會回傳一個 **群組 ID**，唯一識別新建立的連結群組。  

### 步驟 4：驗證連結群組 ID  
再次確認回傳的 ID 與第一個圖層所儲存的 ID 相同。  

```java
short linkGroupId = psd.getLinkedLayersManager().getLinkGroupId(layers[0]);
if (layersLinkGroupId != linkGroupId) {
    throw new Exception("layersLinkGroupId and linkGroupId are not equal.");
}
```  

若 ID 不相符，表示連結過程發生錯誤。  

### 步驟 5：取得並解除連結圖層（解除連結圖層 PSD）  
當需要斷開關聯時，依群組 ID 取得連結圖層，並逐一解除連結。  

```java
Layer[] linkedLayers = psd.getLinkedLayersManager().getLayersByLinkGroupId(linkGroupId);
for (Layer linkedLayer : linkedLayers) {
    psd.getLinkedLayersManager().unlinkLayer(linkedLayer);
}
```  

每次迭代都會移除連結，同時保留圖層的原始資料。  

### 步驟 6：驗證解除連結流程  
確認群組中不再有任何圖層。  

```java
linkedLayers = psd.getLinkedLayersManager().getLayersByLinkGroupId(linkGroupId);
if (linkedLayers != null) {
    throw new Exception("The linkedLayers field is not NULL.");
}
```  

如果 `linkedLayers` 仍有內容，則解除連結操作失敗。  

### 步驟 7：儲存更新後的 PSD  
將修改過的文件寫回磁碟。  

```java
psd.save(dataDir + "LinkedLayerexample_output.psd");
```  

儲存會保留所有變更，包括新建立的連結群組或其移除。  

### 步驟 8：釋放 PSD 物件  
釋放原生資源以避免記憶體洩漏。  

```java
finally {
    psd.dispose();
}
```  

在大量檔案的迴圈處理中，呼叫 `dispose()` 是最佳實踐。  

## 常見問題與技巧  

- **檔案路徑不正確** – 請使用絕對路徑或先確認工作目錄。  
- **缺少授權** – 試用版可供評估使用，完整授權會移除評估浮水印。  
- **只連結部分圖層** – 若只需部份圖層，請在呼叫 `linkLayers` 前先建立只包含目標圖層的 `Layer[]`。  
- **執行緒安全** – `PsdImage` 實例非執行緒安全；每個執行緒應建立獨立實例。  

## 結論  
現在您已掌握使用 Aspose.PSD for Java **在 PSD 檔案中連結圖層** 的完整、可投入生產環境的工作流程。熟練這些 API 後，您可以自動化複雜的設計任務、打造自訂編輯器，或在任何 Java 應用程式中整合 Photoshop 風格的圖層處理。持續探索圖層效果、遮色片與智慧物件等其他功能，進一步擴充您的工具箱。  

## 常見問答  

### Aspose.PSD for Java 是什麼？  
Aspose.PSD for Java 是一套讓開發人員以程式方式操作 Photoshop PSD 檔案的函式庫。  

### 我可以在任何作業系統上使用 Aspose.PSD 嗎？  
可以，作為基於 Java 的函式庫，只要支援 Java 的平台皆可執行。  

### 有提供試用版嗎？  
有，您可以免費試用 Aspose.PSD for Java。請參閱 [免費試用連結](https://releases.aspose.com/)。  

### 哪裡可以找到更多文件？  
您可以在此處瀏覽完整文件 [here](https://reference.aspose.com/psd/java/)。  

### 若遇到問題該如何取得支援？  
若發生問題，可前往 [支援論壇](https://forum.aspose.com/c/psd/34) 尋求協助。  

---  

**最後更新：** 2025-12-09  
**測試環境：** Aspose.PSD 24.12 for Java  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}  

{{< /blocks/products/pf/main-container >}}  
{{< /blocks/products/pf/main-wrap-class >}}  

{{< blocks/products/products-backtop-button >}}