---
date: 2025-12-30
description: Aspose.PSD का उपयोग करके दो छवियों को मिलाकर जावा में PSD फ़ाइल बनाना
  सीखें। तेज़ी से छवियों को PSD फ़ाइल में मर्ज करने के लिए हमारी चरण‑दर‑चरण गाइड का
  पालन करें।
linktitle: Combine Images
second_title: Aspose.PSD Java API
title: Java में PSD फ़ाइल कैसे बनाएं – Aspose.PSD के साथ छवियों को संयोजित करें
url: /hi/java/image-editing/combine-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Create PSD file Java – Combine Images using Aspose.PSD

## Introduction

यदि आपको **Java में PSD फ़ाइल बनानी है** कई चित्रों को मिलाकर, तो Aspose.PSD इस काम को सरल बनाता है। इस ट्यूटोरियल में हम दो इमेज को एक ही PSD कैनवास में जोड़ने की प्रक्रिया को दिखाएंगे, यह समझाएंगे कि यह तरीका क्यों उपयोगी है, और तैयार‑से‑चलाने वाला कोड देंगे। अंत में आप **Java शैली में दो इमेज को combine** कर एक प्रोफ़ेशनल‑लुकिंग लेयर्ड फ़ाइल बना पाएँगे।

## Quick Answers
- **क्या लाइब्रेरी इमेज को PSD में मर्ज करने के लिए सबसे अच्छी है?** Aspose.PSD for Java.  
- **इम्प्लीमेंटेशन में कितना समय लगेगा?** बेसिक combine के लिए लगभग 10‑15 मिनट.  
- **क्या लाइसेंस चाहिए?** टेस्टिंग के लिए फ्री ट्रायल चलती है; प्रोडक्शन के लिए कमर्शियल लाइसेंस आवश्यक है.  
- **क्या दो से अधिक इमेज जोड़ सकते हैं?** हाँ – प्रत्येक अतिरिक्त लेयर के लिए `drawImage` कॉल को दोहराएँ.  
- **कौन सा Java वर्ज़न सपोर्टेड है?** Java 8 और उसके बाद के संस्करण.

## Prerequisites

शुरू करने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1. **Aspose.PSD Library** – इसे [here](https://releases.aspose.com/psd/java/) से डाउनलोड करें।  
2. **Java Development Kit (JDK)** – Java 8+ की सलाह दी जाती है।  
3. **Document Directory** – आपके मशीन पर एक फ़ोल्डर जहाँ स्रोत इमेज और उत्पन्न PSD संग्रहीत होंगे.

## Import Packages

अपने प्रोजेक्ट में आवश्यक Aspose.PSD क्लासेज़ को इम्पोर्ट करें:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

## Step‑by‑Step Guide

### Step 1: Create PSD Options (prepare the file)

सबसे पहले हम एक `PsdOptions` इंस्टेंस बनाते हैं जो आउटपुट सेटिंग्स को रखेगा।

```java
PsdOptions imageOptions = new PsdOptions();
```

### Step 2: Set the FileCreateSource (define where the PSD will be saved)

ऑप्शन्स में एक `FileCreateSource` असाइन करें, जो इच्छित परिणाम फ़ाइल की ओर इशारा करेगा।

```java
imageOptions.setSource(new FileCreateSource(dataDir + "Two_images_result_out.psd", false));
```

### Step 3: Create Image Instance (initialize canvas size)

`Image` ऑब्जेक्ट को ऑप्शन्स के साथ बनाएं और 600 × 600 पिक्सेल का कैनवास निर्धारित करें।

```java
Image image = Image.create(imageOptions, 600, 600);
```

### Step 4: Initialize Graphics and draw the first picture

एक `Graphics` ऑब्जेक्ट हमें कैनवास पर पेंट करने देता है। हम बैकग्राउंड को सफ़ेद साफ़ करते हैं और पहले स्रोत इमेज को बाएँ आधे हिस्से में ड्रॉ करते हैं।

```java
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
graphics.drawImage(Image.load(dataDir + "example1.psd"), 0, 0, 300, 600);
```

### Step 5: Draw the second picture (complete the combine)

अब हम उसी कैनवास के दाएँ आधे हिस्से में दूसरी इमेज रखेंगे।

```java
graphics.drawImage(Image.load(dataDir + "example2.psd"), 300, 0, 300, 600);
```

### Step 6: Save the resulting PSD file

अंत में, संयुक्त कैनवास को डिस्क पर सेव करें।

```java
image.save();
```

बधाई हो! आपने सफलतापूर्वक **इमेज को PSD में मर्ज** किया और Java में एक PSD फ़ाइल बनाई।

## Why combine images with Aspose.PSD?

- **Layer‑aware** – प्रत्येक `drawImage` कॉल एक अलग लेयर जोड़ता है जिसे बाद में एडिट किया जा सकता है।  
- **Format flexibility** – PSD, PNG, JPEG, BMP, और कई अन्य फॉर्मैट सपोर्ट करता है।  
- **No native dependencies** – शुद्ध Java, किसी भी OS पर चलाने योग्य जहाँ JDK उपलब्ध है।  

## Common Issues and Solutions

| Issue | Cause | Fix |
|-------|-------|-----|
| `File not found` error when loading source images | Incorrect `dataDir` path | Verify `dataDir` points to the folder containing `example1.psd` and `example2.psd`. |
| Output PSD is blank | `graphics.clear` called after drawing | Ensure `graphics.clear(Color.getWhite())` is executed **before** any `drawImage` calls. |
| License exception at runtime | Missing or expired Aspose.PSD license | Apply a valid license using `License license = new License(); license.setLicense("Aspose.PSD.lic");` before any API call. |

## Frequently Asked Questions

### Q1: Is Aspose.PSD compatible with all image formats?
A1: Aspose.PSD primarily focuses on PSD file format. However, it supports various other formats for input and output.

### Q2: Can I perform additional modifications on the combined image?
A2: Absolutely! After combining images, you can further manipulate the resulting PSD using Aspose.PSD's extensive features.

### Q3: Are there any licensing requirements for using Aspose.PSD?
A3: Yes, a valid license is required for commercial use. Obtain it from [here](https://purchase.aspose.com/buy).

### Q4: Is there a free trial available for Aspose.PSD?
A4: Yes, you can explore Aspose.PSD with a free trial [here](https://releases.aspose.com/).

### Q5: Where can I find support for Aspose.PSD-related queries?
A5: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community support and discussions.

---

**Last Updated:** 2025-12-30  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}