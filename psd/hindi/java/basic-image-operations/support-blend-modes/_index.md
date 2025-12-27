---
date: 2025-12-27
description: Aspose.PSD for Java के साथ लेयर अपारदर्शिता सेट करना, PSD को PNG में
  निर्यात करना, और शानदार प्रभावों के लिए ब्लेंड मोड का उपयोग करना सीखें।
linktitle: Support Blend Modes
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java में लेयर की अपारदर्शिता सेट करें और ब्लेंड मोड्स का समर्थन
  करें
url: /hi/java/basic-image-operations/support-blend-modes/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Set Layer Opacity and Support Blend Modes in Aspose.PSD for Java

## Introduction

इस ट्यूटोरियल में आप **लेयर की अपारदर्शिता (opacity) सेट करने** के बारे में जानेंगे, जबकि आप Aspose.PSD for Java का उपयोग करके ब्लेंड मोड्स के साथ काम करेंगे। चाहे आपको आकर्षक कॉम्पोज़िट बनाने हों या सिर्फ़ लेयर की ट्रांसपेरेंसी को समायोजित करना हो, `set layer opacity` फीचर को महारत हासिल करने से आप अपने PSD फ़ाइलों में हर विज़ुअल एलिमेंट को बारीकी से ट्यून कर सकते हैं। हम PSD फ़ाइलें लोड करने, अपारदर्शिता लागू करने, और परिणाम को PNG में एक्सपोर्ट करने की प्रक्रिया को स्पष्ट, प्रोडक्शन‑रेडी कोड के साथ दिखाएंगे।

## Quick Answers
- **लेयर की ट्रांसपेरेंसी बदलने का मुख्य तरीका क्या है?** इच्छित लेयर पर `setOpacity(byte)` मेथड का उपयोग करें।  
- **अपारदर्शिता बदलने के बाद क्या मैं PSD को एक्सपोर्ट कर सकता हूँ?** हाँ – `PngOptions` के साथ इमेज को सेव करके PNG कॉपी प्राप्त कर सकते हैं।  
- **कौन सा Aspose प्रोडक्ट ब्लेंड मोड्स को सपोर्ट करता है?** Aspose.PSD for Java पूर्ण ब्लेंड‑मोड और अपारदर्शिता नियंत्रण प्रदान करता है।  
- **क्या इस कोड के लिए लाइसेंस चाहिए?** प्रोडक्शन उपयोग के लिए एक टेम्पररी या फुल लाइसेंस आवश्यक है।  
- **क्या API Java 8 और बाद के संस्करणों के साथ संगत है?** बिल्कुल, यह सभी आधुनिक Java संस्करणों के साथ काम करता है।

## What is **set layer opacity**?
`set layer opacity` किसी विशिष्ट लेयर के अल्फा चैनल को समायोजित करता है, जिससे यह नियंत्रित होता है कि नीचे की इमेज का कितना हिस्सा दिखेगा। अपारदर्शिता का मान 0 (पूरी तरह से ट्रांसपेरेंट) से 255 (पूरी तरह से अपारदर्शी) तक होता है। यह ऑपरेशन तब आवश्यक होता है जब आप लेयर्स को सूक्ष्मता से ब्लेंड करना चाहते हैं या फेड‑इन इफ़ेक्ट बनाना चाहते हैं।

## Why use Aspose.PSD for Java blend modes?
- **Full PSD spec support** – सभी मानक Photoshop ब्लेंड मोड उपलब्ध हैं।  
- **Programmatic control** – मैन्युअल एडिटिंग के बिना अपारदर्शिता, ब्लेंड मोड बदलें और एक्सपोर्ट करें।  
- **Cross‑platform** – किसी भी OS पर काम करता है जहाँ Java चलता है, सर्वर‑साइड इमेज पाइपलाइन के लिए आदर्श।  
- **No external dependencies** – लाइब्रेरी PNG कन्वर्ज़न और कलर मैनेजमेंट को आंतरिक रूप से संभालती है।

## Prerequisites

- **Java Development Environment** – JDK 8 या उससे नया इंस्टॉल और कॉन्फ़िगर किया हुआ।  
- **Aspose.PSD for Java Library** – [website](https://releases.aspose.com/psd/java/) से डाउनलोड करें और JAR को अपने प्रोजेक्ट की क्लासपाथ में जोड़ें।  
- **Document Directory** – आपके मशीन पर एक फ़ोल्डर जहाँ स्रोत PSD फ़ाइलें और जेनरेटेड PNGs रखे जाएंगे।

## Import Packages

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## Step‑by‑Step Guide

### Step 1: Load PSD Files  
हम PSD फ़ाइलों के संग्रह पर इटरेट करेंगे, प्रत्येक फ़ाइल को अपारदर्शिता समायोजन के लिए तैयार करेंगे।

```java
String dataDir = "Your Document Directory";
String[] files = new String[] {
   // List of PSD files
   // ...
};

for (int i=0; i< files.length; i++) {
    PsdImage im = (PsdImage)Image.load(dataDir + files[i] + ".psd");
    // Continue to the next steps...
}
```

### Step 2: Export to PNG (How to export PSD)  
PNG में एक्सपोर्ट करने से आप अपारदर्शिता बदलावों का विज़ुअल इम्पैक्ट देख सकते हैं। आवश्यकता अनुसार `PngOptions` को समायोजित करें।

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);

// Save as PNG with 100% opacity
String pngExportPath100 = dataDir + "BlendMode" + files[i] + "_Test100.png";
im.save(pngExportPath100, saveOptions);

// Continue to the next steps...
```

### Step 3: Set Opacity (How to set opacity)  
यहाँ हम दूसरी लेयर की अपारदर्शिता को 50 % (127 में से 255) पर सेट करते हैं। यह मुख्य `set layer opacity` ऑपरेशन को दर्शाता है।

```java
// Set opacity to 50%
im.getLayers()[1].setOpacity((byte)127);

// Save as PNG with 50% opacity
String pngExportPath50 = dataDir + "BlendMode" + files[i] + "_Test50.png";
im.save(pngExportPath50, saveOptions);

// Continue to the next steps...
```

> **Pro tip:** यदि आपको प्रत्येक लेयर पर अलग‑अलग ब्लेंड मोड लागू करने हैं, तो सेव करने से पहले `layer.setBlendMode(BlendMode.<ModeName>)` का उपयोग करें।

इन्हीं तीन चरणों को प्रत्येक ब्लेंड मोड के लिए दोहराएँ जिसे आप टेस्ट करना चाहते हैं, आवश्यकतानुसार ब्लेंड मोड और अपारदर्शिता मान बदलें।

## Common Issues and Solutions

| Issue | Solution |
|-------|----------|
| **Layers array index out of bounds** | PSD में वास्तविक लेयर्स की संख्या की जाँच करें और `im.getLayers()[1]` एक्सेस करने से पहले सुनिश्चित करें कि वह मौजूद है। |
| **Exported PNG appears blank** | सुनिश्चित करें कि `PngOptions.setColorType(PngColorType.TruecolorWithAlpha)` सेट किया गया है; यह अल्फा चैनल को संरक्षित रखता है। |
| **Performance slowdown on large files** | फ़ाइलों को एक‑एक करके लोड और प्रोसेस करें, और JVM हीप साइज (`-Xmx2g`) बढ़ाने पर विचार करें। |

## Frequently Asked Questions

**Q: क्या मैं Aspose.PSD for Java को अन्य Java इमेज प्रोसेसिंग लाइब्रेरीज़ के साथ उपयोग कर सकता हूँ?**  
A: हाँ, Aspose.PSD for Java को अन्य Java इमेज प्रोसेसिंग लाइब्रेरीज़ के साथ इंटीग्रेट करके एक व्यापक समाधान बनाया जा सकता है।

**Q: क्या Aspose.PSD for Java द्वारा संभाली जा सकने वाली PSD फ़ाइलों के आकार पर कोई प्रतिबंध है?**  
A: Aspose.PSD for Java बड़े PSD फ़ाइलों को प्रभावी ढंग से हैंडल करने के लिए डिज़ाइन किया गया है, लेकिन सटीक आकार सीमाओं के लिए आधिकारिक दस्तावेज़ देखें।

**Q: मैं Aspose.PSD for Java के लिए टेम्पररी लाइसेंस कैसे प्राप्त करूँ?**  
A: टेम्पररी लाइसेंस प्राप्त करने के लिए वेबसाइट पर [Temporary License](https://purchase.aspose.com/temporary-license/) पर जाएँ।

**Q: क्या Aspose.PSD for Java सपोर्ट के लिए कोई कम्युनिटी फ़ोरम है?**  
A: हाँ, आप कम्युनिटी सपोर्ट और चर्चा के लिए [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) पर जा सकते हैं।

**Q: क्या मैं अपने एप्लिकेशन की आवश्यकताओं के अनुसार ब्लेंड मोड्स को और कस्टमाइज़ कर सकता हूँ?**  
A: बिल्कुल! Aspose.PSD for Java लचीलापन प्रदान करता है, जिससे आप अपनी विशिष्ट जरूरतों के अनुसार ब्लेंड मोड्स को कस्टमाइज़ कर सकते हैं।

---

**Last Updated:** 2025-12-27  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}