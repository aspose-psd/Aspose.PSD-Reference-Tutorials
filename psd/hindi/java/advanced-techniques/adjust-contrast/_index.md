---
date: 2026-02-25
description: Aspose.PSD for Java, एक प्रमुख जावा इमेज मैनिपुलेशन लाइब्रेरी, का उपयोग
  करके PSD को TIFF में कैसे बदलें और इमेज कंट्रास्ट एडजस्टमेंट कैसे करें, सीखें।
linktitle: Convert PSD to TIFF and Adjust Contrast
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java के साथ PSD को TIFF में कैसे बदलें और कंट्रास्ट समायोजित
  करें
url: /hi/java/advanced-techniques/adjust-contrast/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java के साथ PSD को TIFF में बदलना और कंट्रास्ट समायोजित करना

## Introduction

यदि आपको **PSD को TIFF में बदलना** है और साथ ही अपने ग्राफ़िक्स की दृश्य गुणवत्ता को बारीकी से समायोजित करना है, तो आप सही जगह पर हैं। इस ट्यूटोरियल में हम Aspose.PSD for Java—एक मजबूत **java image manipulation** लाइब्रेरी—का उपयोग करके पूरी वर्कफ़्लो को समझेंगे। आप सीखेंगे कि **image contrast adjustment** को कैसे बढ़ाया जाए, बड़े रास्टर डेटा को कैश करके प्रदर्शन कैसे सुधारा जाए, और अंत में **save image as TIFF** करके डाउनस्ट्रीम प्रोसेसिंग के लिए तैयार किया जाए। चलिए शुरू करते हैं!

## Quick Answers
- **What does “adjust contrast” mean?** यह सबसे गहरे और सबसे उज्ज्वल पिक्सेल के बीच अंतर को बदलता है, जिससे विवरण उभर कर सामने आते हैं।  
- **Which library handles this?** Aspose.PSD for Java – एक पूर्ण‑विशेषताओं वाला इमेज प्रोसेसिंग टूलकिट।  
- **Do I need a license?** एक **temporary aspose license** परीक्षण के लिए काम करती है; उत्पादन के लिए पूर्ण लाइसेंस आवश्यक है।  
- **Can I **convert PSD to TIFF**?** बिल्कुल—हम प्रोसेस्ड इमेज को एक्सपोर्ट करने के लिए `TiffOptions` का उपयोग करेंगे।  
- **How long does the code take to run?** आधुनिक हार्डवेयर पर मानक‑साइज़ PSD फ़ाइलों के लिए आमतौर पर एक सेकंड से कम समय लेता है।

## What is Image Contrast Adjustment?
कंट्रास्ट समायोजन इमेज की टोनल रेंज को बदलता है, प्रकाश और अंधेरे क्षेत्रों के बीच अंतर को बढ़ाता है। यह तब उपयोगी होता है जब स्कैनिंग के बाद इमेज सपाट दिखती है या प्रिंट के लिए ग्राफ़िक्स तैयार करते समय।

## Why Use Aspose.PSD for Java?
- **Rich format support** – खोलें, संपादित करें, और **save image as TIFF**, PNG, JPEG और कई अन्य फ़ॉर्मेट में सहेजें।  
- **High performance** – कैशिंग और रास्टर‑इमेज ऑप्टिमाइज़ेशन मेमोरी ओवरहेड को कम करते हैं, जो बड़े PSD फ़ाइलों के लिए महत्वपूर्ण है।  
- **Straight‑forward API** – `adjustContrast` जैसी सिंगल‑मेथड कॉल्स कोड को पढ़ने योग्य और रखरखाव योग्य बनाती हैं।  
- **Comprehensive java image manipulation** क्षमताएँ जो सरल स्क्रिप्ट से लेकर एंटरप्राइज़‑ग्रेड एप्लिकेशन तक सभी को कवर करती हैं।

## Prerequisites

शुरू करने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित हों:

- Java प्रोग्रामिंग का बुनियादी ज्ञान।  
- Aspose.PSD for Java लाइब्रेरी स्थापित हो। आप इसे [here](https://releases.aspose.com/psd/java/) से डाउनलोड कर सकते हैं।

## Import Packages

अपने Java क्लास में आवश्यक इम्पोर्ट जोड़ें:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Step 1: Load the Image

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

हम स्रोत PSD फ़ाइल (`sample.psd`) को एक `Image` ऑब्जेक्ट में लोड करते हैं, जो आगे की सभी प्रोसेसिंग का एंट्री पॉइंट है।

## Step 2: Cast to RasterImage and Cache Data

```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

`RasterImage` में कास्ट करने से हमें पिक्सेल‑लेवल ऑपरेशन्स का एक्सेस मिलता है। कैशिंग प्रदर्शन को सुधारती है, विशेषकर बड़े फ़ाइलों के लिए।

## How to Adjust Contrast of an Image

```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

`adjustContrast` मेथड एक पूर्णांक लेता है जो प्रतिशत परिवर्तन दर्शाता है। इस उदाहरण में हम कंट्रास्ट को **50 %** तक बढ़ाते हैं।

## Convert PSD to TIFF Using Aspose.PSD

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Save the resultant image to TIFF format
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

यहाँ हम `TiffOptions` (बिट्स पर सैंपल, फोटोमेट्रिक इंटरप्रिटेशन) को कॉन्फ़िगर करते हैं और **save image as TIFF** करते हैं। यह चरण **convert PSD to TIFF** वर्कफ़्लो को पूरा करता है।

## Common Issues and Solutions
- **Image not cached:** बड़े PSD फ़ाइलों के लिए हमेशा `cacheData()` कॉल करें ताकि `OutOfMemoryError` से बचा जा सके।  
- **Unexpected color shift:** सुनिश्चित करें कि `setPhotometric` आपके लक्ष्य कलर स्पेस (RGB बनाम CMYK) से मेल खाता हो।  
- **File not found:** पुष्टि करें कि `dataDir` सही फ़ोल्डर की ओर इशारा कर रहा है और फ़ाइल नाम सही लिखा गया है।

## Frequently Asked Questions

### Q1: Is Aspose.PSD compatible with different image formats?

A1: हाँ, Aspose.PSD विभिन्न इमेज फ़ॉर्मेट्स को सपोर्ट करता है, जिससे आपके प्रोजेक्ट्स में लचीलापन आता है।

### Q2: How can I obtain a temporary license for Aspose.PSD?

A2: आप एक अस्थायी लाइसेंस [here](https://purchase.aspose.com/temporary-license/) से प्राप्त कर सकते हैं।

### Q3: Where can I find Aspose.PSD documentation?

A3: दस्तावेज़ीकरण [here](https://reference.aspose.com/psd/java/) उपलब्ध है।

### Q4: What support options are available for Aspose.PSD?

A4: सहायता के लिए, [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) पर जाएँ।

### Q5: Can I purchase Aspose.PSD?

A5: हाँ, आप Aspose.PSD को [here](https://purchase.aspose.com/buy) से खरीद सकते हैं।

## Conclusion

अब आप **how to convert PSD to TIFF** और Aspose.PSD for Java का उपयोग करके **image contrast adjustment** करना जानते हैं। ये कदम आपको इमेज क्वालिटी पर सूक्ष्म नियंत्रण देते हैं जबकि कोड को साफ़ और रखरखाव योग्य रखते हैं। अपनी विशिष्ट आवश्यकताओं के अनुसार `adjustBrightness` या `adjustGamma` जैसे अन्य समायोजन मेथड्स के साथ प्रयोग करने में संकोच न करें।

---

**Last Updated:** 2026-02-25  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}