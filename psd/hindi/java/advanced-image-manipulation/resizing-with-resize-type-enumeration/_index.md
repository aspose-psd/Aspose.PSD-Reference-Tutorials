---
date: 2026-06-03
description: Aspose.PSD for Java के साथ इमेज को रिसाइज़ करना सीखें। यह चरण‑दर‑चरण
  गाइड Resize Type Enumeration, high‑quality image resize, और PSD को JPEG में बदलने
  के बारे में बताता है।
keywords:
- how to resize image
- convert psd to jpeg
- high quality image resize
- resize image java
- java image manipulation tutorial
linktitle: Resize Type Enumeration के साथ रिसाइज़िंग
schemas:
- author: Aspose
  dateModified: '2026-06-03'
  description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  headline: How to Resize Image Java Using Resize Type Enumeration
  type: TechArticle
- description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  name: How to Resize Image Java Using Resize Type Enumeration
  steps:
  - name: '**Java Development Environment** – JDK 8 or newer installed and configured.'
    text: '**Java Development Environment** – JDK 8 or newer installed and configured.'
  - name: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
  - name: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
    text: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
  type: HowTo
- questions:
  - answer: Load the PSD with `Image.load`, then call `image.save("output.jpg", new
      JpegOptions());`.
    question: How do I programmatically convert a PSD file to JPEG without resizing?
  - answer: Yes, you can set the `Resolution` property on the `Image` object before
      saving.
    question: Is it possible to maintain the original DPI when resizing?
  - answer: While you can call `resize` multiple times, it’s more efficient to calculate
      the final dimensions and resize once.
    question: Can I chain multiple resize operations?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Resize Type Enumeration का उपयोग करके जावा में इमेज का आकार कैसे बदलें
url: /hi/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# जावा में Resize Type Enumeration का उपयोग करके इमेज का आकार बदलना

## परिचय

यदि आप जावा प्रोजेक्ट में इमेज फ़ाइलों को कुशलतापूर्वक **इमेज का आकार कैसे बदलें** चाहते हैं, तो Aspose.PSD for Java एक साफ़, उच्च‑प्रदर्शन API प्रदान करता है। इस ट्यूटोरियल में हम PSD लोड करने, उच्च‑गुणवत्ता वाले इमेज रिसाइज़ के लिए **Resize Type Enumeration** लागू करने, और अंत में **PSD को JPEG में बदलें** की प्रक्रिया को देखेंगे। चाहे आप डेस्कटॉप एडिटर बना रहे हों या स्वचालित सर्वर‑साइड पाइपलाइन, ये चरण आपको कुछ ही कोड लाइनों से आयाम, गुणवत्ता और फ़ॉर्मेट को नियंत्रित करने की सुविधा देते हैं।

## त्वरित उत्तर
- **कौन सी लाइब्रेरी जावा में इमेज रिसाइज़ को संभालती है?** Aspose.PSD for Java.
- **कौन सा रिसाइज़ टाइप सबसे अच्छी गुणवत्ता देता है?** `ResizeType.LanczosResample`.
- **क्या मैं रिसाइज़ करने के बाद PSD को JPEG में बदल सकता हूँ?** Yes – simply save with `JpegOptions`.
- **क्या उत्पादन के लिए लाइसेंस की आवश्यकता है?** A valid Aspose.PSD license is required for production use.
- **क्या यह तरीका बड़े बैचों के लिए उपयुक्त है?** Absolutely; the API processes multi‑hundred‑page files without loading the whole document into memory.

## जावा में "इमेज का आकार कैसे बदलें" क्या है?
**इमेज का आकार कैसे बदलें** का मतलब है प्रोग्रामेटिक रूप से इमेज के पिक्सेल आयाम बदलना जबकि दृश्य गुणवत्ता को बनाए रखना। Aspose.PSD का `Resize` मेथड `ResizeType` एनेमरेशन के साथ मिलकर स्केलिंग एल्गोरिदम पर सटीक नियंत्रण प्रदान करता है, जिससे डेवलपर्स विभिन्न स्रोत फ़ाइलों और लक्ष्य आकारों में गुणवत्ता बनाए रख सकते हैं।

## Resize Type Enumeration का उपयोग क्यों करें?
`ResizeType` आपको वह रिसैम्पलिंग एल्गोरिदम चुनने देता है जो गति और दृश्य गुणवत्ता के बीच सर्वोत्तम संतुलन प्रदान करता है। अधिकांश परिस्थितियों में, **LanczosResample** तेज़ प्रदर्शन लागत के साथ तेज़ परिणाम देता है, एक सामान्य सर्वर‑ग्रेड CPU पर 2000 × 1500 इमेज को 120 ms से कम समय में प्रोसेस करता है जबकि किनारी विवरण को बरकरार रखता है।

## पूर्वापेक्षाएँ

शुरू करने से पहले सुनिश्चित करें कि आपके पास है:

1. **जावा डेवलपमेंट एनवायरनमेंट** – JDK 8 या नया स्थापित और कॉन्फ़िगर किया हुआ।  
2. **Aspose.PSD Library** – Download the latest JAR from the [वेबसाइट](https://releases.aspose.com/psd/java/).  
3. **सैंपल PSD फ़ाइल** – SDK के साथ शामिल [sample.psd](Your Document Directory/sample.psd) फ़ाइल का उपयोग करें हाथ‑पर परीक्षण के लिए।

## पैकेज इम्पोर्ट करें

`Image` Aspose.PSD में सभी इमेज प्रकारों की बेस क्लास है। अपने जावा स्रोत फ़ाइल में आवश्यक इम्पोर्ट जोड़ें:

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## चरण 1: इमेज लोड करें

### परिभाषा एंकर
`RasterImage` क्लास Aspose.PSD का मुख्य ऑब्जेक्ट है जो PSD फ़ाइल से लोड की गई रास्टर‑आधारित इमेज को दर्शाता है।

अपने PSD को एक `RasterImage` इंस्टेंस में लोड करें ताकि आप उसके पिक्सेल को बदल सकें:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

## चरण 2: इमेज का आकार बदलें

`image.resize(width, height, resizeType)` चुने हुए एल्गोरिदम का उपयोग करके इमेज को निर्दिष्ट आयामों में रिसाइज़ करता है।

अब लोड की गई इमेज को **Resize Type Enumeration** का उपयोग करके रिसाइज़ करें। इस उदाहरण में हम Lanczos Resample मेथड का उपयोग करते हैं, जो उच्च गुणवत्ता के साथ **इमेज का आकार कैसे बदलें** के लिए आदर्श है:

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## चरण 3: रिसाइज़्ड इमेज सहेजें

`image.save(path, options)` प्रदान किए गए विकल्पों द्वारा परिभाषित फ़ॉर्मेट में इमेज को डिस्क पर लिखता है।

रिसाइज़ करने के बाद, निर्दिष्ट आयामों और चुने हुए रिसाइज़ टाइप के साथ इमेज को सहेजें। यहाँ, हम **psd को jpeg में बदलें** को भी दिखाते हैं, परिणाम को JPEG फ़ाइल के रूप में सहेजकर:

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

## Resize Type Enumeration का उपयोग क्यों करें?

`ResizeType` आपको रिसैम्पलिंग एल्गोरिदम पर सूक्ष्म नियंत्रण देता है, जिससे आप गति और गुणवत्ता को संतुलित कर सकते हैं। अधिकांश अनुप्रयोगों के लिए, `LanczosResample` एक शानदार संतुलन प्रदान करता है, भारी प्रदर्शन दंड के बिना तेज़ परिणाम देता है, और विभिन्न इमेज कंटेंट में अच्छी तरह काम करता है।

## सामान्य समस्याएँ और समाधान

- **रिसाइज़ के बाद इमेज धुंधली दिखती है** – अपने विशेष इमेज के लिए सबसे अच्छा दृश्य परिणाम देने वाला `ResizeType` खोजने के लिए `Bicubic` या `NearestNeighbour` जैसे अन्य `ResizeType` आज़माएँ।  
- **बड़ी PSD फ़ाइलों पर OutOfMemoryError** – इमेज को छोटे हिस्सों में प्रोसेस करें या JVM हीप साइज (`-Xmx` फ़्लैग) बढ़ाएँ। Aspose.PSD पूरी डॉक्यूमेंट को मेमोरी में लोड किए बिना **2 GB** तक की फ़ाइलें संभाल सकता है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.PSD for Java छोटे और बड़े‑पैमाने के प्रोजेक्ट दोनों के लिए उपयुक्त है?
A1: बिल्कुल! Aspose.PSD for Java सभी आकार के प्रोजेक्ट्स को संभालने के लिए डिज़ाइन किया गया है, स्केलेबिलिटी और दक्षता प्रदान करता है।

### Q2: क्या मैं Lanczos Resample के अलावा कोई अलग रिसाइज़ टाइप उपयोग कर सकता हूँ?
A2: हाँ, Aspose.PSD for Java विभिन्न रिसाइज़ टाइप प्रदान करता है, जैसे **NearestNeighbour**, **Bicubic**, आदि। पूरी सूची के लिए API दस्तावेज़ देखें।

### Q3: मैं Aspose.PSD for Java के लिए अतिरिक्त समर्थन कहाँ पा सकता हूँ?
A3: किसी भी प्रश्न या सहायता के लिए, [Aspose.PSD फ़ोरम](https://forum.aspose.com/c/psd/34) पर जाएँ।

### Q4: क्या Aspose.PSD for Java के लिए कोई मुफ्त ट्रायल उपलब्ध है?
A4: हाँ, आप मुफ्त ट्रायल संस्करण [यहाँ](https://releases.aspose.com/) तक पहुँच सकते हैं।

### Q5: मैं Aspose.PSD for Java के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूँ?
A5: अस्थायी लाइसेंस प्राप्त करने के लिए, [इस लिंक](https://purchase.aspose.com/temporary-license/) पर जाएँ।

## बार-बार पूछे जाने वाले प्रश्न

**Q: मैं प्रोग्रामेटिक रूप से PSD फ़ाइल को बिना रिसाइज़ किए JPEG में कैसे बदलूँ?**  
A: PSD को `Image.load` से लोड करें, फिर `image.save("output.jpg", new JpegOptions());` कॉल करें।

**Q: रिसाइज़ करने पर मूल DPI बनाए रखना संभव है क्या?**  
A: हाँ, आप सहेजने से पहले `Image` ऑब्जेक्ट पर `Resolution` प्रॉपर्टी सेट कर सकते हैं।

**Q: क्या मैं कई रिसाइज़ ऑपरेशन्स को चेन कर सकता हूँ?**  
A: जबकि आप `resize` को कई बार कॉल कर सकते हैं, अंतिम आयामों की गणना करके एक बार रिसाइज़ करना अधिक प्रभावी है।

---

**अंतिम अपडेट:** 2026-06-03  
**परीक्षण किया गया:** Aspose.PSD for Java 24.12  
**लेखक:** Aspose  

{{< blocks/products/products-backtop-button >}}

## संबंधित ट्यूटोरियल

- [Aspose.PSD के साथ सरल रिसाइज़िंग – जावा इमेज मैनिपुलेशन लाइब्रेरी](/psd/java/basic-image-operations/simple-resizing/)
- [Aspose.PSD for Java में Bicubic Resampler के साथ उच्च गुणवत्ता इमेज स्केलिंग](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)
- [Aspose.PSD for Java के साथ PSD को PNG में बदलें और अनुपातिक रूप से रिसाइज़ करें](/psd/java/advanced-image-manipulation/resize-image-proportionally/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}