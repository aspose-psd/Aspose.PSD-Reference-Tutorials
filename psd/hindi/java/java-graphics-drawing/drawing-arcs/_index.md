---
date: 2026-01-17
description: Aspose.PSD for Java का उपयोग करके जावा ग्राफ़िक्स में आर्क कैसे बनाएं,
  सीखें। ग्राफ़िकल एप्लिकेशन के लिए कोड उदाहरणों के साथ चरण‑दर‑चरण ट्यूटोरियल।
linktitle: Java Graphics Draw Arc with Aspose.PSD
second_title: Aspose.PSD Java API
title: जावा ग्राफिक्स में Aspose.PSD के साथ आर्क ड्रॉ करना – चरण-दर-चरण गाइड
url: /hi/java/java-graphics-drawing/drawing-arcs/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java Graphics Draw Arc with Aspose.PSD

## Introduction
इस ट्यूटोरियल में आप **java graphics draw arc** को Aspose.PSD for Java लाइब्रेरी के साथ कैसे उपयोग किया जाता है, यह जानेंगे। प्रोग्रामेटिक रूप से आर्क ड्रॉ करना कस्टम UI कॉम्पोनेन्ट्स, डेटा विज़ुअलाइज़ेशन, या किसी भी ग्राफ़िक के लिए उपयोगी है जहाँ सटीक कर्व कंट्रोल की आवश्यकता होती है। हम प्रोजेक्ट सेटअप से लेकर आर्क रेंडर करने और परिणाम सहेजने तक हर कदम को विस्तार से बताएँगे—ताकि आप इस क्षमता को तुरंत अपने Java एप्लिकेशन में जोड़ सकें।

## Quick Answers
- **कौन सी लाइब्रेरी Java में आसानी से आर्क ड्रॉ करने देती है?** Aspose.PSD for Java.  
- **क्या विकास के लिए लाइसेंस की आवश्यकता है?** परीक्षण के लिए एक फ्री ट्रायल चल सकता है; प्रोडक्शन के लिए लाइसेंस आवश्यक है।  
- **कौन‑से आउटपुट फ़ॉर्मेट समर्थित हैं?** BMP, PNG, JPEG, TIFF, GIF, और कई अन्य।  
- **क्या मैं आर्क की मोटाई या रंग बदल सकता हूँ?** हाँ—`Pen` ऑब्जेक्ट की प्रॉपर्टीज़ को समायोजित करें।  
- **क्या कोड Java 8+ के साथ संगत है?** बिल्कुल, API Java 8 और उसके बाद के संस्करणों को टारगेट करती है।

## What is “java graphics draw arc”?
यह वाक्यांश Java कोड का उपयोग करके ग्राफ़िक्स कैनवास पर एक वक्र खंड (आर्क) रेंडर करने को दर्शाता है। Aspose.PSD के साथ, आप एक हाई‑लेवल `Graphics` क्लास प्राप्त करते हैं जो ड्रॉइंग ऑपरेशन्स को सरल बनाता है, रंग प्रबंधन, एंटी‑एलियासिंग, और फ़ाइल एक्सपोर्ट को बैकग्राउंड में संभालता है।

## Why use Aspose.PSD for arc drawing?
- **Full PSD support** – Photoshop इंस्टॉल किए बिना Photoshop फ़ाइलें बनाएं या संपादित करें।  
- **Rich drawing API** – `drawArc` जैसे मेथड्स आपको आकार, कोण, और स्टाइलिंग एक ही कॉल में निर्दिष्ट करने देते हैं।  
- **Cross‑format export** – कुछ ही लाइनों के कोड से अपना आर्क BMP, PNG, JPEG आदि में सहेजें।  
- **Performance‑focused** – बड़े इमेज और बैच प्रोसेसिंग के लिए ऑप्टिमाइज़्ड।

## Prerequisites
1. **Java Development Environment** – Java (JDK 8 या बाद का) इंस्टॉल करें। इसे [ऑरैकल की वेबसाइट](https://www.oracle.com/java/) से डाउनलोड करें।  
2. **Aspose.PSD for Java** – लाइब्रेरी को [डाउनलोड पेज](https://releases.aspose.com/psd/java/) से प्राप्त करें और JAR को अपने प्रोजेक्ट की क्लासपाथ में जोड़ें।

## Import Packages
सबसे पहले, आवश्यक Aspose.PSD क्लासेज़ को इम्पोर्ट करें:

```java
import com.aspose.psd.Color;
import static com.aspose.psd.ColorAdjustType.Pen;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

इन इम्पोर्ट्स से आपको रंग परिभाषाएँ, ड्रॉइंग टूल्स, इमेज कंटेनर, और फ़ाइल‑सेविंग विकल्पों तक पहुँच मिलती है।

## Step‑by‑Step Guide

### Step 1: Set Up Your Java Project
एक नया Maven या Gradle प्रोजेक्ट बनाएं, Aspose.PSD JAR जोड़ें, और सुनिश्चित करें कि IDE इम्पोर्ट्स को बिना त्रुटि के रिज़ॉल्व कर रहा है।

### Step 2: Initialize Image and Graphics Objects
एक खाली `PsdImage` कैनवास और ड्रॉ करने के लिए `Graphics` इंस्टेंस बनाएं:

```java
String dataDir = "Your Document Directory";
// Initialize PsdImage object
PsdImage image = new PsdImage(100, 100);
// Initialize Graphics object and clear surface
Graphics graphics = new Graphics(image);
graphics.clear(Color.getYellow());
```

`"Your Document Directory"` को उस फ़ोल्डर पाथ से बदलें जहाँ आप आउटपुट फ़ाइल सहेजना चाहते हैं।

### Step 3: Define Arc Parameters
आर्क के आकार और कोण को निर्दिष्ट करें:

```java
int width = 100;
int height = 200;
int startAngle = 45;
int sweepAngle = 270;
```

इन संख्याओं को अपनी वांछित विज़ुअल स्टाइल के अनुसार समायोजित करें।

### Step 4: Draw and Save the Arc
`drawArc` मेथड का उपयोग करें, फिर इमेज को एक्सपोर्ट करें:

```java
// Draw arc with specified Pen object (black color) and parameters
graphics.drawArc(new Pen(Color.getBlack()), 0, 0, width, height, startAngle, sweepAngle);
// Save the image in BMP format
String outputPath = dataDir + "Arc.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
image.save(outputPath, saveOptions);
```

यह कोड पीले बैकग्राउंड पर एक काली आर्क रेंडर करता है और परिणाम `Arc.bmp` में लिखता है। यदि आप किसी अन्य फ़ॉर्मेट या क्वालिटी चाहते हैं तो `outputPath` और `BmpOptions` को बदलें।

## Common Issues & Solutions
- **File not found error** – सुनिश्चित करें कि `dataDir` के अंत में पाथ सेपरेटर (`/` या `\\`) हो और डायरेक्टरी मौजूद हो।  
- **Arc appears as a line** – जाँचें कि `width` और `height` शून्य से बड़े हों और `sweepAngle` 360° का गुणज न हो (जिससे पूरा एलिप्स बन जाएगा)।  
- **Color not applied** – `new Pen(Color.getRed())` का उपयोग करें या `pen.setWidth(2)` सेट करें ताकि प्रभाव स्पष्ट दिखे।

## Frequently Asked Questions

**Q: क्या Aspose.PSD for Java आर्क के अलावा अन्य शैप्स भी संभाल सकता है?**  
A: हाँ, यह रेक्टैंगल, एलिप्स, लाइन्स, और कस्टम पाथ्स को समान `Graphics` API के माध्यम से सपोर्ट करता है।

**Q: आर्क की मोटाई या रंग कैसे बदलें?**  
A: इच्छित `Color` और `Width` के साथ एक `Pen` बनाएं (उदा., `new Pen(Color.getBlue(), 3)`) और उसे `drawArc` को पास करें।

**Q: क्या BMP के अलावा अन्य फ़ॉर्मेट में एक्सपोर्ट करना संभव है?**  
A: बिल्कुल। `BmpOptions` की जगह `PngOptions`, `JpegOptions`, `TiffOptions` आदि का उपयोग करें।

**Q: अधिक उदाहरण और सपोर्ट कहाँ मिल सकता है?**  
A: समुदाय सहायता, आधिकारिक दस्तावेज़, और कोड सैंपल्स के लिए [Aspose.PSD फ़ोरम](https://forum.aspose.com/c/psd/34) देखें।

## Conclusion
अब आपके पास Aspose.PSD for Java का उपयोग करके **java graphics draw arc** करने का एक पूर्ण, प्रोडक्शन‑रेडी उदाहरण है। पैरामीटर्स, पेन सेटिंग्स, और आउटपुट विकल्पों को समायोजित करके आप किसी भी Java‑आधारित ग्राफ़िक्स वर्कफ़्लो में कस्टम आर्क्स को इंटीग्रेट कर सकते हैं।

---

**Last Updated:** 2026-01-17  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}