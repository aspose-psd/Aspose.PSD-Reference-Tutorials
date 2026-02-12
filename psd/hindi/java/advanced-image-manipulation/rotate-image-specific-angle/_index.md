---
date: 2026-02-12
description: Aspose.PSD का उपयोग करके जावा में किसी विशिष्ट कोण पर छवि को घुमाना सीखें।
  यह गाइड दिखाता है कि छवि को कैसे घुमाया जाए, डिग्री के अनुसार छवि को कैसे घुमाया
  जाए, और पृष्ठभूमि रंगों को कैसे संभाला जाए।
linktitle: How to Rotate Image on a Specific Angle
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java के साथ किसी विशिष्ट कोण पर छवि को कैसे घुमाएँ
url: /hi/java/advanced-image-manipulation/rotate-image-specific-angle/
weight: 20
---

 final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java के साथ विशिष्ट कोण पर छवि को कैसे घुमाएँ

## Introduction

यदि आपको Java एप्लिकेशन में प्रोग्रामेटिक रूप से **how to rotate image** करने की आवश्यकता है, तो Aspose.PSD for Java एक साफ़, उच्च‑प्रदर्शन API प्रदान करता है जो भारी काम को संभालता है। चाहे आप फोटो‑एडिटर बना रहे हों, थंबनेल जेनरेट कर रहे हों, या वेब सर्विस के लिए एसेट तैयार कर रहे हों, सटीक डिग्री में छवि को घुमाना एक सामान्य आवश्यकता है। इस ट्यूटोरियल में हम पूरी प्रक्रिया—PSD फ़ाइल लोड करने से लेकर घुमाए गए परिणाम को सहेजने तक—पर चलेंगे, साथ ही कैशिंग और बैकग्राउंड हैंडलिंग जैसी सर्वोत्तम प्रथाओं को उजागर करेंगे।

## Quick Answers
- **Java में छवियों को घुमाने के लिए सबसे अच्छा लाइब्रेरी कौन सा है?** Aspose.PSD for Java.  
- **क्या मैं किसी भी डिग्री से घुमा सकता हूँ?** हाँ, `rotate` मेथड एक `float` कोण (पॉज़िटिव या नेगेटिव) स्वीकार करता है।  
- **क्या विकास के लिए लाइसेंस चाहिए?** परीक्षण के लिए एक फ्री ट्रायल काम करता है; उत्पादन के लिए लाइसेंस आवश्यक है।  
- **कौन से इमेज फ़ॉर्मेट समर्थित हैं?** PSD, JPEG, PNG, TIFF, GIF, BMP, और कई अन्य।  
- **खाली स्थान के लिए बैकग्राउंड रंग कैसे सेट करें?** `rotate` मेथड में एक `Color` इंस्टेंस पास करें।

## What is Image Rotation in Java?

इमेज रोटेशन का मतलब है पिक्सेल मैट्रिक्स को एक पिवट पॉइंट (आमतौर पर केंद्र) के चारों ओर दिए गए कोण से घुमाना। Java में, आप इसे `Graphics2D` के साथ मैन्युअली कर सकते हैं, लेकिन Aspose.PSD गणित को एब्स्ट्रैक्ट करता है, विभिन्न कलर डेप्थ को संभालता है, और PSD फ़ाइलों के साथ काम करते समय लेयर जानकारी को संरक्षित रखता है।

## Why Use Aspose.PSD for Rotating Images?

- **सटीकता:** किसी भी अंशीय डिग्री से बिना गुणवत्ता खोए घुमाएँ।  
- **प्रदर्शन:** बिल्ट‑इन कैशिंग (`image.cacheData()`) बड़े फ़ाइलों को तेज़ बनाती है।  
- **बैकग्राउंड नियंत्रण:** रोटेशन से उत्पन्न गैप्स को भरने के लिए बैकग्राउंड रंग निर्दिष्ट करें।  
- **फ़ॉर्मेट लचीलापन:** PSD लोड करें, JPEG, PNG, या कोई भी समर्थित फ़ॉर्मेट आउटपुट करें।

## Prerequisites

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1. **Java Development Kit (JDK 8 या बाद का)** – एक कार्यशील Java IDE या कमांड‑लाइन सेटअप।  
2. **Aspose.PSD for Java** – नवीनतम JAR को [Aspose.PSD Java page](https://reference.aspose.com/psd/java/) से डाउनलोड करें।  
3. **Sample PSD file** – उदाहरण के लिए, `sample.psd` को उस फ़ोल्डर में रखें जिसे आप अपने कोड से रेफ़र कर सकते हैं।

## Import Packages

पहले, उन क्लासेज़ को इम्पोर्ट करें जिनकी हमें आवश्यकता होगी। ये इम्पोर्ट्स आप जिस भी रोटेशन एंगल को चुनें, समान रहेंगे।

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Step‑by‑Step Guide

### Step 1: Define Your Document Directory

उस फ़ोल्डर को सेट करें जिसमें स्रोत PSD है और जहाँ आउटपुट लिखा जाएगा।

```java
String dataDir = "Your Document Directory";
```

> **Pro tip:** सापेक्ष‑पाथ की आश्चर्यजनक स्थितियों से बचने के लिए एक एब्सोल्यूट पाथ या `System.getProperty("user.dir")` का उपयोग करें।

### Step 2: Specify Source and Destination File Paths

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "RotatingImageOnSpecificAngle_out.jpg";
```

`destName` को अपने आउटपुट की आवश्यकता के अनुसार किसी भी समर्थित एक्सटेंशन (`.png`, `.tiff`, आदि) में बदल सकते हैं।

### Step 3: Load the Image

```java
RasterImage image = (RasterImage)Image.load(sourceFile);
```

`Image.load` स्वचालित रूप से फ़ाइल फ़ॉर्मेट का पता लगाता है और रास्टर‑आधारित ऑपरेशन्स के लिए एक ठोस `RasterImage` लौटाता है।

### Step 4: Cache Image Data (Optional but Recommended)

```java
if (!image.isCached())
{
    image.cacheData();
}
```

कैशिंग इमेज पिक्सेल को मेमोरी में संग्रहीत करता है, जिससे बाद के ट्रांसफ़ॉर्मेशन तेज़ होते हैं—विशेषकर बड़े PSD फ़ाइलों के लिए उपयोगी।

### Step 5: Rotate the Image

```java
image.rotate(20f, true, Color.getRed());
```

- **20f** – डिग्री में रोटेशन एंगल (float)। इस मान को बदलकर किसी भी कोण से घुमा सकते हैं, उदाहरण के लिए, `-45f` काउंटर‑क्लॉकवाइज़ के लिए।  
- **true** – घुमाई गई इमेज को फिट करने के लिए कैनवास को विस्तारित करते हुए मूल आस्पेक्ट रेशियो बनाए रखें।  
- **Color.getRed()** – रोटेशन से उत्पन्न खाली कोनों को भरने वाला बैकग्राउंड रंग। आवश्यकता अनुसार `Color.getWhite()` या कोई भी कस्टम रंग से बदलें।

#### Rotate Image by Degrees in Java

`rotate` मेथड कोई भी फ्लोटिंग‑पॉइंट वैल्यू स्वीकार करता है, इसलिए आप **rotate image by degrees** जैसे `30f`, `90f`, या `-15f` से घुमा सकते हैं। पॉज़िटिव मान घड़ी की दिशा में घुमाते हैं, जबकि नेगेटिव मान काउंटर‑क्लॉकवाइज़ घुमाते हैं।

#### Rotate Image Specific Angle Using Aspose.PSD

क्योंकि मेथड `float` के साथ काम करता है, आप **rotate image specific angle** जैसे `22.5f` को ग्राफ़िक‑डिज़ाइन वर्कफ़्लो में सटीक नियंत्रण के लिए निर्दिष्ट कर सकते हैं।

#### Rotate Image Java Example Summary

ऊपर के सभी चरण एक पूर्ण **rotate image java** वर्कफ़्लो दर्शाते हैं—फ़ाइल लोड करने से लेकर घुमाए गए आउटपुट को सहेजने तक।

### Step 6: Save the Result

```java
image.save(destName, new JpegOptions());
```

`JpegOptions` आपको क्वालिटी, कम्प्रेशन, और अन्य JPEG‑विशिष्ट सेटिंग्स को नियंत्रित करने देता है। लॉसलेस आउटपुट के लिए, इसे `PngOptions` से बदलें।

## Common Issues and Solutions

| Issue | कारण | समाधान |
|-------|------|--------|
| **Blank corners after rotation** | बैकग्राउंड रंग नहीं दिया गया | `rotate` में एक `Color` (उदा., `Color.getWhite()`) पास करें। |
| **Out‑of‑memory error on large PSDs** | इमेज कैश नहीं हुई | प्रोसेसिंग से पहले `image.cacheData()` कॉल करें। |
| **Incorrect angle direction** | नेगेटिव बनाम पॉज़िटिव एंगल में भ्रम | घड़ी की दिशा में रोटेशन के लिए नेगेटिव वैल्यू उपयोग करें (या आपके कोऑर्डिनेट सिस्टम के अनुसार उल्टा)। |
| **Unsaved changes** | `save` कॉल करना भूल जाना | रोटेशन के बाद `image.save(...)` को निष्पादित करना सुनिश्चित करें। |

## Frequently Asked Questions

**Q: क्या मैं Aspose.PSD for Java का उपयोग करके ट्रांसपैरेंसी वाली छवियों को घुमा सकता हूँ?**  
A: हाँ। लाइब्रेरी अल्फा चैनल को संरक्षित रखती है; यदि आप ट्रांसपेरेंट कोर्नर चाहते हैं तो ओपेक बैकग्राउंड रंग निर्दिष्ट न करें।

**Q: रोटेशन के लिए समर्थित इमेज फ़ाइल फ़ॉर्मेट पर कोई सीमा है?**  
A: नहीं। Aspose.PSD PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF, EMF, और कई अन्य को सपोर्ट करता है।

**Q: क्या मैं छवियों को नेगेटिव एंगल से घुमा सकता हूँ?**  
A: बिल्कुल। घड़ी की दिशा में रोटेट करने के लिए `rotate` में नेगेटिव फ़्लोट पास करें (उदा., `-30f`)।

**Q: क्या Aspose.PSD रोटेशन के दौरान रियल‑टाइम इमेज प्रीव्यू प्रदान करता है?**  
A: API केवल सर्वर‑साइड है। लाइव प्रीव्यू के लिए, घुमाए गए बिटमैप को UI फ्रेमवर्क (Swing, JavaFX) में इंटीग्रेट करें और व्यू को रिफ्रेश करें।

**Q: क्या Aspose.PSD के लिए कोई कम्युनिटी फ़ोरम है जहाँ मैं मदद ले सकूँ?**  
A: हाँ, प्रश्न पूछने और अनुभव साझा करने के लिए [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) पर जाएँ।

## Conclusion

अब आप जानते हैं कि Aspose.PSD for Java का उपयोग करके विशिष्ट कोण पर **how to rotate image** फ़ाइलों को कैसे घुमाएँ। कैशिंग, बैकग्राउंड कलर कंट्रोल, और लचीले आउटपुट विकल्पों का उपयोग करके आप किसी भी Java‑आधारित इमेज वर्कफ़्लो में सटीक रोटेशन फ़ंक्शनैलिटी को इंटीग्रेट कर सकते हैं।

---

**Last Updated:** 2026-02-12  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}