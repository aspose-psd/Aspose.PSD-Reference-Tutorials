---
date: 2026-03-21
description: 學習如何使用 ICC 配置檔轉換色彩配置檔、套用 ICC 配置檔設定，並在使用 Aspose.PSD for Java 建立 PSD 圖像時設定
  RGB 配置檔。
linktitle: Color Conversion using ICC Profiles
second_title: Aspose.PSD Java API
title: 如何在 Aspose.PSD 中使用 ICC 配置檔進行色彩轉換
url: /zh-hant/java/psd-conversion/color-conversion-icc-profiles/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Aspose.PSD 中使用 ICC 配置檔進行色彩轉換

## 介紹
如果你想 **如何使用 ICC** 配置檔以確保跨裝置的顏色精確，恭喜你來對地方了。在本教學中，我們將示範如何轉換色彩配置檔、套用 ICC 配置檔，以及在使用 Aspose.PSD for Java **建立 PSD 圖像** 時設定 RGB 配置檔。無論你是構建批次處理管線或是單張圖像編輯器，以下步驟都能為你提供穩固、可投入生產的基礎。

## 快速問答
- **ICC 配置檔的主要目的為何？** 它定義了在特定裝置或色彩空間上應如何詮釋顏色。  
- **哪個類別代表 Aspose.PSD 中的 PSD 圖像？** `PsdImage`。  
- **我可以同時變更 RGB 與 CMYK 配置檔嗎？** 可以 – 使用 `setRgbColorProfile` 與 `setCmykColorProfile`。  
- **開發時需要授權嗎？** 免費試用可用於測試；正式上線需購買授權。  
- **哪種輸出格式支援 YCCK？** 使用 `JpegCompressionColorMode.Ycck` 的 JPEG。

## 什麼是 ICC 色彩轉換？
ICC（International Color Consortium）配置檔是標準化的資料集合，用於描述裝置（螢幕、印表機、掃描器）的色彩特性。透過 **convert color profile** 從一個色彩空間轉換到另一個，你可以確保圖像在任何觀看環境下的視覺外觀保持一致。

## 為何在 Aspose.PSD 中使用 ICC 配置檔？
- **精確的色彩再現** – 對於品牌與印刷工作流程至關重要。  
- **跨平台一致性** – 同一圖像在 Windows、macOS 以及行動裝置上呈現相同。  
- **內建 API 支援** – Aspose.PSD 讓你只需幾行 Java 代碼即可 **apply icc profile** 與 **set rgb profile**。

## 前置條件
在開始之前，請確保已具備以下項目：

1. **Aspose.PSD for Java** – 從 [releases](https://releases.aspose.com/psd/java/) 頁面下載最新的函式庫。  
2. **Java 開發環境** – JDK 8 以上以及你喜愛的 IDE。  
3. **ICC 配置檔** – 本範例使用 `eciRGB_v2.icc`（RGB）與 `ISOcoated_v2_FullGamut4.icc`（CMYK）。可從可信賴的色彩管理來源取得。

## 匯入套件
將所需的 Aspose.PSD 命名空間加入專案。這些匯入讓你能存取圖像處理、JPEG 選項與串流來源。

```java
import com.aspose.psd.Color;
import com.aspose.psd.fileformats.jpeg.JpegCompressionColorMode;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.JpegOptions;
import com.aspose.psd.sources.StreamSource;
import java.io.File;
import java.io.FileInputStream;
import java.io.FileNotFoundException;
```

## 如何使用 ICC 配置檔進行色彩轉換
以下是一個逐步指南，說明在 **creating a PSD image** 時如何使用 ICC 配置檔 **how to convert color**。

### 步驟 1：建立新圖像（Create PSD Image）
首先，實例化一個空的 `PsdImage`。這會提供一個畫布讓你填入像素資料。

```java
String dataDir = "Your Document Directory";
PsdImage image = new PsdImage(500, 500);
```

### 步驟 2：填入圖像資料
以原始 ARGB 像素值填充圖像。在實務情境中，你可能會從其他來源載入像素資料，但此處僅示範此流程。

```java
int count = image.getWidth() * image.getHeight();
int[] pixels = new int[count];
int r = 0, g = 0, b = 0, channel = 0;
for (int i = 0; i < count; i++) {
    // Fill pixels with color values.
    // ...
}
// Save the newly created pixels.
image.saveArgb32Pixels(image.getBounds(), pixels);
```

### 步驟 3：使用預設 ICC 配置檔儲存圖像
此時儲存會使用函式庫的預設色彩配置檔寫入圖像。此步驟可讓你在之後套用自訂配置檔前，先觀察差異。

```java
image.save(dataDir + "Default_profiles.jpg");
```

### 步驟 4：更新色彩配置檔（Apply ICC Profile & Set RGB Profile）
載入外部 ICC 檔案並指派給圖像。這就是我們 **apply icc profile** 與 **set rgb profile** 的地方。

```java
File rgbFile = new File(dataDir + "eciRGB_v2.icc");
FileInputStream rgbInputStream = new FileInputStream(rgbFile);
StreamSource rgbprofile = new StreamSource(rgbInputStream);
File cmykFile = new File(dataDir + "ISOcoated_v2_FullGamut4.icc");
FileInputStream cmykInputStream = new FileInputStream(cmykFile);
StreamSource cmykprofile = new StreamSource(cmykInputStream);
image.setRgbColorProfile(rgbprofile);
image.setCmykColorProfile(cmykprofile);
```

### 步驟 5：使用新 YCCK 配置檔儲存圖像
最後，將圖像以 JPEG 格式匯出，使用 YCCK 色彩模式，該模式會遵循剛剛設定的 CMYK 配置檔。

```java
JpegOptions options = new JpegOptions();
options.setColorType(JpegCompressionColorMode.Ycck);
image.save(dataDir + "Ycck_profiles.jpg", options);
```

透過上述步驟，你已 **converted the color profile** 了一個 PSD 圖像、**applied ICC profiles**，並 **set the RGB profile** 以達到精確的呈現。

## 常見問題與解決方案
| 問題 | 原因 | 解決方式 |
|-------|--------|-----|
| 轉換後顏色看起來黯淡 | 指定了錯誤的配置檔或缺少配置檔資料 | 確認 ICC 檔案與來源圖像的色彩空間相符。 |
| 載入 ICC 檔案時出現 `FileNotFoundException` | `dataDir` 路徑不正確 | 使用絕對路徑或確保檔案放置於指定目錄中。 |
| JPEG 儲存時未使用 YCCK 色彩 | `JpegOptions` 未設定為 `Ycck` | 在儲存前呼叫 `options.setColorType(JpegCompressionColorMode.Ycck)`。 |

## 常見問答
**Q: 我可以在 Aspose.PSD for Java 中使用自訂 ICC 配置檔嗎？**  
A: 可以，只需將提供的 ICC 檔案換成自己的，並將 `StreamSource` 指向新檔案即可。

**Q: 我該如何處理最終圖像的色差問題？**  
A: 微調 ICC 配置檔或使用 Aspose.PSD 的色彩調整 API，在轉換後調整亮度、對比度或伽瑪。

**Q: Aspose.PSD 適合批次處理圖像嗎？**  
A: 絕對適合。你可以遍歷資料夾中的 PSD 檔案，套用相同的配置檔邏輯，並有效率地儲存結果。

**Q: 哪裡可以取得更多用於色彩管理的 ICC 配置檔？**  
A: 可參考 ICC 官方網站、Adobe 的色彩資源頁面，或供應商提供的裝置專屬配置檔庫。

**Q: 在色彩轉換中使用 ICC 配置檔有什麼好處？**  
A: 它們確保不同裝置間的色彩一致，簡化工作流程自動化，並減少手動配色的工作量。

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**最後更新：** 2026-03-21  
**測試環境：** Aspose.PSD for Java (latest)  
**作者：** Aspose