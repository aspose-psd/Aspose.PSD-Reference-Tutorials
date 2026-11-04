---
date: 2026-11-04
description: Aspose.PSD for Java का उपयोग करके invert adjustment layer लागू करना,
  PSD इमेजेज को बैच प्रोसेस करना, और नेगेटिव इमेज PSD फ़ाइलें बनाना सीखें।
keywords:
- how to use aspose
- batch process psd images
- create negative image psd
- image processing java library
- apply multiple adjustment layers
lastmod: 2026-11-04
linktitle: Invert Adjustment Layer
og_description: Aspose.PSD for Java का उपयोग करके invert adjustment layer जोड़ें,
  PSD इमेजेज को बैच प्रोसेस करें, और नेगेटिव इमेज PSD बनाएं। चरण‑दर‑चरण गाइड का पालन
  करें।
og_image_alt: Screenshot showing Aspose.PSD Java code adding an invert adjustment
  layer
og_title: Java में Aspose.PSD का उपयोग करके invert adjustment layer कैसे जोड़ें
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to use Aspose.PSD for Java to apply an invert adjustment
    layer, batch process PSD images, and create negative image PSD files.
  headline: How to use Aspose.PSD to add an invert adjustment layer in Java
  type: TechArticle
- questions:
  - answer: Yes, it supports Java 6.0 and later, including Java 8, 11, and 17.
    question: Is Aspose.PSD compatible with all Java versions?
  - answer: Absolutely. After adding the invert layer you can call `addBrightnessAdjustmentLayer()`,
      `addHueSaturationAdjustmentLayer()`, etc., to stack effects.
    question: Can I apply multiple adjustment layers in a single operation?
  - answer: The complete documentation is available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find the full API reference?
  - answer: Yes, you can download a trial version [Aspose.PSD trial download](https://releases.aspose.com/).
    question: Is there a free trial for Aspose.PSD?
  - answer: Request a temporary license [temporary license request page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for testing?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- aspose psd
- java image processing
- invert adjustment layer
- batch psd processing
title: Java में Aspose.PSD का उपयोग करके invert adjustment layer कैसे जोड़ें
url: /hi/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD का उपयोग करके जावा में इनवर्ट एडजस्टमेंट लेयर जोड़ना

## परिचय

यदि आप एक मजबूत **image processing java library** की तलाश में हैं, तो Aspose.PSD for Java बाजार में उपलब्ध सबसे बहुमुखी विकल्पों में से एक है। इस ट्यूटोरियल में आप देखेंगे **Aspose** का उपयोग करके PSD फ़ाइल में **Invert Adjustment Layer** कैसे डालें, इसे अन्य एडजस्टमेंट्स के साथ स्टैक करें, और यहाँ तक कि इस ऑपरेशन को दर्जनों फ़ाइलों पर चलाएँ। चाहे आप एक बैच‑प्रोसेसिंग टूल, सर्वर‑साइड इमेज सर्विस, या सिंगल‑इमेज एडिटर बना रहे हों, नीचे दिए गए चरण आपको स्रोत PSD से पूरी‑तरह से संपादन योग्य नेगेटिव इमेज कुछ ही मिनटों में प्राप्त करने में मदद करेंगे।

## त्वरित उत्तर
- **Invert Adjustment Layer क्या करता है?** यह चयनित क्षेत्र में प्रत्येक RGB मान को उलट देता है, जिससे इमेज फ़ोटोग्राफ़िक नेगेटिव में बदल जाती है।  
- **यह सुविधा कौन सी लाइब्रेरी प्रदान करती है?** Aspose.PSD, एक प्रमुख **image processing java library**।  
- **क्या इसे अन्य एडजस्टमेंट्स के साथ स्टैक किया जा सकता है?** हाँ – आप **multiple adjustment layers** जैसे Brightness/Contrast, Hue/Saturation आदि को लागू कर सकते हैं।  
- **क्या विकास के लिए लाइसेंस की आवश्यकता है?** एक फ्री ट्रायल उपलब्ध है; उत्पादन उपयोग के लिए लाइसेंस आवश्यक है।  
- **इम्प्लीमेंटेशन में कितना समय लगेगा?** सामान्यतः बेसिक केस के लिए 10 मिनट से कम।

## Invert Adjustment Layer क्या है?

Invert Adjustment Layer एक non‑destructive एडिट है जो प्रभावित प्रत्येक पिक्सेल के रंग मानों को उलट देता है। क्योंकि यह लेयर स्टैक के ऊपर स्थित होता है, आप इसकी विज़िबिलिटी टॉगल कर सकते हैं या इसे पुनः क्रमित कर सकते हैं बिना मूल इमेज डेटा को स्थायी रूप से बदले। यह **negative image PSD** फ़ाइलें बनाने या क्लासिक फ़िल्म‑नेगेटिव लुक हासिल करने का सबसे तेज़ तरीका है।

## Aspose.PSD को अपने image processing java library के रूप में क्यों चुनें?

Aspose.PSD **200+ PSD फीचर्स** का समर्थन करता है, Photoshop फ़ाइलों को बिना Photoshop के पढ़ और लिख सकता है, और 500 MB से कम हीप मेमोरी का उपयोग करके सैकड़ों‑पृष्ठ दस्तावेज़ प्रोसेस करता है। यह किसी भी Java runtime (Java 6+) पर चलता है, जिससे यह **batch process psd images** के लिए Windows, Linux, या macOS सर्वरों पर आदर्श बनता है।

## पूर्वापेक्षाएँ

शुरू करने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित हों:

1. **Aspose.PSD for Java** – आधिकारिक साइट से नवीनतम JAR डाउनलोड करें [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/)।  
2. **Java Development Kit** – JDK 6.0 या बाद का संस्करण स्थापित हो और `PATH` में कॉन्फ़िगर हो।  

अब आप कोड लिखने के लिए तैयार हैं।

## पैकेज इम्पोर्ट करें

`PsdImage` क्लास मेमोरी में पूरे Photoshop दस्तावेज़ का प्रतिनिधित्व करता है, जबकि एडजस्टमेंट‑लेयर क्लासेज `com.aspose.psd.layers.adjustments` पैकेज में स्थित हैं।

`PsdImage` क्लास Aspose.PSD की टॉप‑लेवल ऑब्जेक्ट है जो PSD फ़ाइल की संरचना और पिक्सेल डेटा को एन्कैप्सुलेट करती है। नेमस्पेस इम्पोर्ट करें, फिर आप PSD फ़ाइलों को लोड, एडिट और सेव कर पाएँगे।

## चरण 1: दस्तावेज़ डायरेक्टरी सेट करें

उस फ़ोल्डर को परिभाषित करें जिसमें आपका स्रोत PSD फ़ाइल है और जहाँ आउटपुट सेव किया जाएगा। पूर्ण पाथ का उपयोग करने से `NullPointerException` से बचा जा सकता है जब वर्किंग डायरेक्टरी बदलती है।

## चरण 2: PSD फ़ाइल लोड करें

स्रोत फ़ाइल को `PsdImage` ऑब्जेक्ट में लोड करें। यह ऑब्जेक्ट मेमोरी में पूरी लेयर हायरार्की रखता है, जिससे non‑destructive एडिट संभव होते हैं।

`PsdImage` क्लास एक स्टैटिक `load` मेथड प्रदान करता है जो फ़ाइल हेडर पढ़ता है, फ़ॉर्मेट वैलिडेट करता है, और इन‑मेमोरी प्रतिनिधित्व बनाता है जो आगे की मैनिपुलेशन के लिए तैयार है।

## चरण 3: इनवर्ट एडजस्टमेंट लेयर जोड़ें

बिल्ट‑इन मेथड को कॉल करके वर्तमान लेयर स्टैक के शीर्ष पर Invert Adjustment Layer डालें। बाद में आप अधिक लेयर्स (जैसे Brightness, Hue) जोड़ सकते हैं **multiple adjustment layers** को एक ही वर्कफ़्लो में लागू करने के लिए।

`addInvertAdjustmentLayer()` PSD की लेयर कलेक्शन में एक Invert Adjustment Layer जोड़ता है।

## चरण 4: आउटपुट सेव करें

परिवर्तित PSD को डिस्क पर स्थायी रूप से लिखें।  

`save()` निर्दिष्ट पाथ पर सभी लेयर्स और मेटाडेटा सहित PSD फ़ाइल लिखता है।

सेविंग वही `save` मेथड उपयोग करता है जो पूर्ण दस्तावेज़, सभी एडजस्टमेंट लेयर्स, मास्क और मेटाडेटा को निर्दिष्ट फ़ॉर्मेट में लिखता है।

### क्या हुआ अभी?

PSD फ़ाइल को `PsdImage` ऑब्जेक्ट में लोड किया गया, एक `InvertAdjustmentLayer` बनाया गया और शीर्षmost लेयर के रूप में जोड़ा गया, और दस्तावेज़ को सेव किया गया। यह क्रम मूल इमेज डेटा को संरक्षित रखता है जबकि एक non‑destructive इनवर्ट इफ़ेक्ट जोड़ता है जिसे बाद में टॉगल या रीऑर्डर किया जा सकता है।

आपने अब सफलतापूर्वक Aspose.PSD, एक **image processing java library**, का उपयोग करके PSD फ़ाइल को मैनिपुलेट किया है।

## इनवर्ट एडजस्टमेंट के साथ PSD इमेजेज़ को बैच प्रोसेस कैसे करें?

`for` लूप के भीतर प्रत्येक फ़ाइल लोड करें, वही चरण लागू करें, और प्रत्येक इटरेशन के बाद `save` कॉल करें। चूँकि Aspose.PSD फ़ाइलों को स्ट्रीमिंग फ़ैशन में प्रोसेस करता है, आप **hundreds of PSDs** को 300 MB से कम मेमोरी उपयोग में संभाल सकते हैं, बस वही `PsdImage` इंस्टेंस पुन: उपयोग करके।

## PSD को नेगेटिव इमेज में कैसे बदलें?

Invert Adjustment Layer को शीर्षmost आइटम के रूप में जोड़ें और दस्तावेज़ को सेव करें – यह ऑपरेशन **convert PSD to negative** के बराबर है। आप बाद में लेयर को डिसेबल या डिलीट करके मूल रूप में वापस आ सकते हैं बिना स्रोत फ़ाइल को फिर से लोड किए।

## सामान्य समस्याएँ एवं टिप्स

| समस्या | कारण | समाधान |
|-------|-------|----------|
| **`Image.load` पर NullPointerException** | गलत फ़ाइल पाथ या फ़ाइल अनुपलब्ध | `dataDir` और फ़ाइल नाम की जाँच करें; परीक्षण के लिए पूर्ण पाथ उपयोग करें |
| **लेयर क्रम अपेक्षित नहीं है** | मौजूदा लेयर्स के बाद लेयर जोड़ने से स्टैक बदल जाता है | इनवर्ट लेयर को अन्य एडजस्टमेंट्स से पहले डालें, या `psdImage.getLayers().move()` से पुनः क्रमित करें |
| **बड़ी PSDs पर प्रदर्शन धीमा** | बहुत बड़ी फ़ाइलें मेमोरी में लोड हो रही हैं | JVM हीप बढ़ाएँ (`-Xmx2g`) या `psdImage.getPages().get(0).getResources().setMemoryOptimized(true)` का उपयोग करके फ़ाइलों को चंक्स में प्रोसेस करें |

## अक्सर पूछे जाने वाले प्रश्न

**प्रश्न: क्या Aspose.PSD सभी Java संस्करणों के साथ संगत है?**  
उत्तर: हाँ, यह Java 6.0 और बाद के संस्करणों, जिसमें Java 8, 11, और 17 शामिल हैं, को सपोर्ट करता है।

**प्रश्न: क्या मैं एक ही ऑपरेशन में कई एडजस्टमेंट लेयर्स लागू कर सकता हूँ?**  
उत्तर: बिल्कुल। इनवर्ट लेयर जोड़ने के बाद आप `addBrightnessAdjustmentLayer()`, `addHueSaturationAdjustmentLayer()` आदि को कॉल करके इफ़ेक्ट्स को स्टैक कर सकते हैं।

**प्रश्न: पूर्ण API रेफ़रेंस कहाँ मिल सकता है?**  
उत्तर: पूरी डॉक्यूमेंटेशन उपलब्ध है [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/)।

**प्रश्न: क्या Aspose.PSD का फ्री ट्रायल उपलब्ध है?**  
उत्तर: हाँ, आप ट्रायल संस्करण डाउनलोड कर सकते हैं [Aspose.PSD trial download](https://releases.aspose.com/)।

**प्रश्न: परीक्षण के लिए अस्थायी लाइसेंस कैसे प्राप्त करें?**  
उत्तर: अस्थायी लाइसेंस के लिए अनुरोध करें [temporary license request page](https://purchase.aspose.com/temporary-license/)।

---

**अंतिम अपडेट:** 2026-11-04  
**टेस्टेड विद:** Aspose.PSD 24.12 for Java  
**लेखक:** Aspose  









```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

```java
String dataDir = "Your Document Directory";
```

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

```java
im.addInvertAdjustmentLayer();
```

```java
im.save(outputPath);
```

## संबंधित ट्यूटोरियल

- [Add Level Adjustment Layer to PSD Files with Aspose.PSD for Java](/psd/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/)
- [How to Add Adjustment Layer – Channel Mixer in PSD (Java)](/psd/java/modifying-converting-psd-images/add-channel-mixer-adjustment-layer-psd/)
- [How to Edit PSD - Add Curves Adjustment Layer Using Java](/psd/java/modifying-converting-psd-images/add-curves-adjustment-layer-psd/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}