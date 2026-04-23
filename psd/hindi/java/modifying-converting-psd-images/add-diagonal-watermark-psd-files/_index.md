---
date: 2026-03-04
description: जाने कैसे जावा में ग्राफ़िक्स ऑब्जेक्ट बनाएं और Aspose.PSD का उपयोग करके
  PSD फ़ाइलों में तिरछा वॉटरमार्क जोड़ें। यह चरण‑दर‑चरण गाइड जावा इमेज वॉटरमार्क लाइब्रेरी
  के उपयोग को कवर करता है।
linktitle: Add Diagonal Watermark to PSD Files with Java
second_title: Aspose.PSD Java API
title: ग्राफ़िक्स ऑब्जेक्ट जावा बनाएं – पीएसडी के लिए तिरछा वॉटरमार्क
url: /hi/java/modifying-converting-psd-images/add-diagonal-watermark-psd-files/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Add Diagonal Watermark to PSD Files with Java

## Introduction
इस ट्यूटोरियल में आप **create graphics object java** बनाएँगे और इसका उपयोग करके PSD फ़ाइलों में तिरछा वॉटरमार्क जोड़ेंगे। चाहे आप एक डिज़ाइनर हों जो अपने काम की सुरक्षा करना चाहते हैं या एक मार्केटर हों जो इमेजेज़ पर ब्रांडिंग करना चाहते हैं, एक साफ़ वॉटरमार्क आपके काम को पेशेवर और सुरक्षित दिखा सकता है। हम प्रत्येक चरण को स्पष्ट व्याख्याओं के साथ बताएँगे, ताकि आप इस तकनीक को अपने प्रोजेक्ट्स में जल्दी से लागू कर सकें।

## Quick Answers
- **कौन सी लाइब्रेरी चाहिए?** Aspose.PSD for Java (एक मजबूत java इमेज वॉटरमार्क लाइब्रेरी)।  
- **इस ट्यूटोरियल में मुख्य कीवर्ड क्या है?** create graphics object java।  
- **क्या लाइसेंस चाहिए?** परीक्षण के लिए मुफ्त ट्रायल चलती है; प्रोडक्शन के लिए व्यावसायिक लाइसेंस आवश्यक है।  
- **क्या मैं वॉटरमार्क टेक्स्ट और स्टाइल बदल सकता हूँ?** हाँ – आप फ़ॉन्ट, रंग, अपारदर्शिता और घुमाव को कस्टमाइज़ कर सकते हैं।  
- **कौन‑से आउटपुट फॉर्मेट सपोर्टेड हैं?** उदाहरण PNG में सेव करता है, लेकिन Aspose.PSD PSD, JPEG, BMP और अधिक फॉर्मेट में एक्सपोर्ट कर सकता है।

## What is a Graphics Object in Java?
एक **Graphics** ऑब्जेक्ट इमेज के लिए ड्रॉइंग सतह को दर्शाता है। ग्राफ़िक्स ऑब्जेक्ट बनाकर आप उन मेथड्स तक पहुँच प्राप्त करते हैं जो आपको टेक्स्ट, शैप्स और अन्य विज़ुअल एलिमेंट्स को सीधे बिटमैप या PSD कैनवास पर रेंडर करने की अनुमति देते हैं। यही मुख्य अवधारणा है जो प्राथमिक कीवर्ड **create graphics object java** के पीछे है।

## Why Use Aspose.PSD for Watermarking?
Aspose.PSD एक समर्पित **java image watermark library** है जो Adobe Photoshop के बिना काम करती है। यह आपको लेयर्स, टेक्स्ट रेंडरिंग और इमेज ट्रांसफ़ॉर्मेशन पर पूर्ण नियंत्रण देती है, जिससे यह सर्वर‑साइड प्रोसेसिंग या बैच ऑपरेशन्स के लिए आदर्श बनती है।

## Prerequisites
कोड में प्रवेश करने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

### 1. Java Development Environment
नवीनतम JDK को [Java website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) से इंस्टॉल करें।

### 2. Aspose.PSD Library
लाइब्रेरी को [Aspose Downloads page](https://releases.aspose.com/psd/java/) से डाउनलोड करें। JAR को Maven, Gradle या मैन्युअल क्लासपाथ इन्क्लूजन के माध्यम से अपने प्रोजेक्ट में जोड़ें।

### 3. Basic Understanding of Java
क्लासेज़, ऑब्जेक्ट्स और फ़ाइल I/O की मूल समझ होने से आप ट्यूटोरियल को आसानी से फॉलो कर पाएँगे।

### 4. IDE Setup
IntelliJ IDEA, Eclipse या NetBeans का उपयोग करके एक आरामदायक कोडिंग वातावरण बनाएं।

## Import Packages
PSD फ़ाइलों को मैनीपुलेट करने के लिए आवश्यक Aspose.PSD क्लासेज़ को इम्पोर्ट करें:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Font;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Matrix;
import com.aspose.psd.PointF;
import com.aspose.psd.RectangleF;
import com.aspose.psd.StringAlignment;
import com.aspose.psd.StringFormat;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

अब जब हमने प्री‑रिक्विज़िट्स को व्यवस्थित कर लिया है और आवश्यक पैकेज इम्पोर्ट कर लिये हैं, चलिए तिरछा वॉटरमार्क PSD फ़ाइल में जोड़ने के चरणों को देखते हैं।

## Step 1: Set Up Your Directory
```java
String dataDir = "Your Document Directory";
```
`"Your Document Directory"` को उस फ़ोल्डर पाथ से बदलें जहाँ आपका PSD स्रोत फ़ाइल स्थित है।

## Step 2: Load the PSD File
```java
PsdImage psdImage = (PsdImage)Image.load(dataDir + "layers.psd");
```
`Image.load` मेथड फ़ाइल को पढ़ता है और इसे `PsdImage` में कास्ट करता है ताकि हम PSD‑विशिष्ट फीचर्स का उपयोग कर सकें।

## Step 3: Create a Graphics Object
```java
Graphics graphics = new Graphics(psdImage);
```
यहाँ हम **create graphics object java** बनाते हैं—वह कैनवास जहाँ हम वॉटरमार्क ड्रॉ करेंगे।

## Step 4: Create a Font for the Watermark
```java
Font font = new Font("Arial", 20.0f);
```
कोई भी इंस्टॉल्ड फ़ॉन्ट चुनें; आकार वॉटरमार्क की प्रमुखता को नियंत्रित करता है।

## Step 5: Create a Brush for the Watermark
```java
SolidBrush brush = new SolidBrush(Color.fromArgb(50, 128, 128, 128));
```
`alpha` वैल्यू (पहला पैरामीटर) पारदर्शिता सेट करता है। 50 का अल्फा एक सूक्ष्म, अर्ध‑पारदर्शी लुक देता है।

## Step 6: Set Up the Transform Matrix
```java
graphics.setTransform(new Matrix());
graphics.getTransform().rotateAt(45, new PointF(psdImage.getWidth() / 2, psdImage.getHeight() / 2));
```
हम ड्रॉइंग सतह को इमेज के केंद्र के चारों ओर 45° घुमा देते हैं, जिससे तिरछा प्रभाव बनता है।

## Step 7: Define String Alignment
```java
StringFormat sf = new StringFormat();
sf.setAlignment(StringAlignment.Center);
```
सेंटर अलाइनमेंट सुनिश्चित करता है कि वॉटरमार्क घुमाए गए आयत के मध्य में ठीक बैठता है।

## Step 8: Draw the Watermark
```java
graphics.drawString("Some watermark text", font, brush, new RectangleF(0, psdImage.getHeight() / 2, psdImage.getWidth(), psdImage.getHeight() / 2), sf);
```
`"Some watermark text"` को अपने ब्रांड नाम या कॉपीराइट नोटिस से बदलें। आयत वह क्षेत्र निर्धारित करती है जहाँ टेक्स्ट रेंडर होगा।

## Step 9: Save the Image
```java
psdImage.save(dataDir + "AddDiagnolWatermark_output.png", new PngOptions());
```
आउटपुट PNG में सेव किया जाता है, लेकिन आप Aspose.PSD द्वारा सपोर्टेड किसी भी फॉर्मेट को चुन सकते हैं।

## Common Use Cases
- **ब्रांड सुरक्षा:** अनधिकृत पुन: उपयोग को रोकने के लिए अर्ध‑पारदर्शी लोगो जोड़ें।  
- **बैच प्रोसेसिंग:** सर्वर पर बड़ी इमेज लाइब्रेरी के लिए वॉटरमार्किंग को ऑटोमेट करें।  
- **क्रिएटिव प्रीव्यूज़:** क्लाइंट्स को वॉटरमार्केड ड्राफ्ट दिखाएँ जबकि मूल फ़ाइलें अपरिवर्तित रहें।

## Troubleshooting & Tips
- **पारदर्शिता दिखाई नहीं दे रही?** अधिक मजबूत वॉटरमार्क के लिए अल्फा वैल्यू बढ़ाएँ (जैसे `100`)।  
- **वॉटरमार्क ऑफ‑सेंटर लग रहा है?** सुनिश्चित करें कि रोटेशन पॉइंट इमेज की सटीक चौड़ाई/ऊँचाई विभाजन का उपयोग कर रहा है।  
- **परफ़ॉर्मेंस की चिंता?** लूप में कई इमेज प्रोसेस करते समय वही `Graphics` ऑब्जेक्ट पुनः उपयोग करें।

## FAQ's
### What is Aspose.PSD?
Aspose.PSD एक Java लाइब्रेरी है जो Adobe Photoshop की आवश्यकता के बिना PSD फ़ाइलों को काम करने और मैनीपुलेट करने के लिए उपयोग की जाती है।

### Can I use other fonts for watermarking?
हाँ, आप अपने सिस्टम में इंस्टॉल्ड किसी भी फ़ॉन्ट को वॉटरमार्किंग के लिए चुन सकते हैं।

### Is there a way to customize the watermark's transparency?
बिल्कुल! आप SolidBrush में अल्फा वैल्यू को बदलकर पारदर्शिता को समायोजित कर सकते हैं।

### Can I add multiple watermarks?
हाँ, आप विभिन्न पैरामीटर्स के साथ `drawString` मेथड को कई बार कॉल करके अधिक वॉटरमार्क जोड़ सकते हैं।

### Where can I find more information about Aspose.PSD?
आप दस्तावेज़ीकरण को [here](https://reference.aspose.com/psd/java/) पर देख सकते हैं।

---

**Last Updated:** 2026-03-04  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}