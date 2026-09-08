---
date: 2026-09-08
description: Aspose.PSD for Java का उपयोग करके PSD फ़ाइलों में java graphics draw
  line कैसे करें सीखें। यह गाइड स्पष्ट चरणों और कोड उदाहरणों के साथ draw lines java
  दिखाता है।
keywords:
- java graphics draw line
- draw lines java
- how to draw lines java
lastmod: 2026-09-08
linktitle: Java में Drawing Lines
og_description: Aspose.PSD का उपयोग करके Java में java graphics draw line कैसे खोजें।
  PSD फ़ाइलों में draw lines java को जल्दी से करने के लिए चरण‑दर‑चरण निर्देशों का
  पालन करें।
og_image_alt: Screenshot of Java code drawing lines in a PSD file using Aspose.PSD
og_title: Aspose.PSD के साथ Java में java graphics draw line कैसे करें
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to java graphics draw line in PSD files using Aspose.PSD
    for Java. This guide shows draw lines java with clear steps and code examples.
  headline: How to java graphics draw line in Java
  type: TechArticle
- questions:
  - answer: Aspose.PSD for Java.
    question: What library is required?
  - answer: java graphics draw line.
    question: Which primary keyword does this tutorial target?
  - answer: Yes – a free trial license is available.
    question: Do I need a license to try it?
  - answer: The library works on Windows, Linux, and macOS.
    question: Can I run this on any OS?
  - answer: About 10‑15 minutes for a basic line drawing.
    question: How long does the implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- PSD line drawing
- Java image processing
title: Java में java graphics draw line कैसे करें
url: /hi/java/java-graphics-drawing/drawing-lines/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# जावा में रेखाएँ बनाना

## परिचय
इस ट्यूटोरियल में आप सीखेंगे कि **java graphics draw line** को PSD फ़ाइलों में Aspose.PSD for Java का उपयोग करके कैसे ड्रॉ किया जाता है। प्रोग्रामेटिक रूप से रेखाएँ बनाना आपको ग्राफ़िक्स निर्माण को स्वचालित करने, एनोटेशन जोड़ने, या फ़ोटोशॉप खोले बिना डिज़ाइन एसेट्स जेनरेट करने की अनुमति देता है। गाइड के अंत तक आप केवल कुछ Java कोड लाइनों से डॉटेड और सॉलिड दोनों प्रकार की रेखाएँ ड्रॉ कर पाएँगे।

## त्वरित उत्तर
- **कौन सी लाइब्रेरी आवश्यक है?** Aspose.PSD for Java.  
- **इस ट्यूटोरियल का मुख्य कीवर्ड क्या है?** java graphics draw line.  
- **क्या इसे आज़माने के लिए लाइसेंस चाहिए?** हाँ – एक फ्री ट्रायल लाइसेंस उपलब्ध है।  
- **क्या मैं इसे किसी भी OS पर चला सकता हूँ?** लाइब्रेरी Windows, Linux, और macOS पर काम करती है।  
- **इम्प्लीमेंटेशन में कितना समय लगेगा?** बेसिक लाइन ड्रॉइंग के लिए लगभग 10‑15 मिनट।

## java graphics draw line क्या है?
`java graphics draw line` शब्द Java‑आधारित ग्राफ़िक्स API का उपयोग करके इमेज कैनवास पर सीधी रेखा प्रिमिटिव्स को रेंडर करने की प्रक्रिया को दर्शाता है। इस ट्यूटोरियल में Aspose.PSD लाइब्रेरी `Graphics` क्लास प्रदान करती है, जिसमें `drawLine` मेथड है जो `Pen` और कोऑर्डिनेट वैल्यूज़ लेता है और रेखा बनाता है।

## लाइन ड्रॉइंग के लिए Aspose.PSD क्यों उपयोग करें?
Aspose.PSD एक मजबूत, मेमोरी‑कुशल इंजन प्रदान करता है जो Java कोड से सीधे Photoshop फ़ाइलों को संभालता है। यह 70 से अधिक इमेज और डॉक्यूमेंट फ़ॉर्मेट्स को सपोर्ट करता है, 2 GB तक की PSD फ़ाइलों को पूरी तरह लोड किए बिना काम कर सकता है, और हाई‑परफ़ॉर्मेंस ड्रॉइंग ऑपरेशन्स देता है, जिससे बैच प्रोसेसिंग और ऑटोमेटेड ग्राफ़िक्स जेनरेशन के लिए यह आदर्श है।

## आवश्यकताएँ
- Java प्रोग्रामिंग भाषा का बेसिक ज्ञान।  
- आपके सिस्टम पर JDK (Java Development Kit) इंस्टॉल होना चाहिए।  
- Aspose.PSD for Java लाइब्रेरी डाउनलोड करके आपके डेवलपमेंट एनवायरनमेंट में सेट अप हो।

## पैकेज इम्पोर्ट करें
निम्न इम्पोर्ट्स आवश्यक Aspose.PSD क्लासेज़ को इमेज क्रिएशन, ग्राफ़िक्स हैंडलिंग, और कलर मैनेजमेंट के लिए लाते हैं।
```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import static com.aspose.psd.GraphicsUnit.Point;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Point;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## चरण 1: अपना प्रोजेक्ट सेट अप करें
अपने IDE में एक नया Java प्रोजेक्ट बनाकर Aspose.PSD for Java को डिपेंडेंसीज़ में जोड़ें। आप लाइब्रेरी को यहाँ से डाउनलोड कर सकते हैं: [Aspose.PSD for Java Download](https://releases.aspose.com/psd/java/)।

## चरण 2: psd इमेज को इनिशियलाइज़ करें
`PsdImage` क्लास एक Photoshop डॉक्यूमेंट को दर्शाता है और आपको निर्दिष्ट डाइमेंशन के साथ नया ब्लैंक PSD कैनवास बनाने की अनुमति देता है।
```java
String dataDir = "Your Document Directory";
String outpath = dataDir + "Lines.psd";
Image image = new PsdImage(100, 100);
```

## चरण 3: ग्राफ़िक्स ऑब्जेक्ट को इनिशियलाइज़ करें
`Graphics` Aspose.PSD की कोर क्लास है जो PSD कैनवास पर शैप्स, टेक्स्ट, और रेखाएँ ड्रॉ करने के लिए उपयोग होती है।  
Graphics क्लास का एक इंस्टेंस बनाएं और ग्राफ़िक्स सरफेस को क्लियर करें:
```java
Graphics graphic = new Graphics(image);
graphic.clear(Color.getYellow());
```

## जावा में java graphics draw line कैसे करें?
एक PSD कैनवास लोड या बनाएं, उसका `Graphics` ऑब्जेक्ट प्राप्त करें, और कॉन्फ़िगर किए गए `Pen` के साथ `drawLine` मेथड को कॉल करें। यह सिंगल‑कॉल अप्रोच तुरंत एक सीधी रेखा ड्रॉ करता है, एंटी‑एलियासिंग और कलर ब्लेंडिंग को ऑटोमैटिकली हैंडल करता है। आप विभिन्न कोऑर्डिनेट्स के साथ कॉल दोहरा कर कई रेखाएँ बना सकते हैं।

## चरण 4: विकर्ण डॉटेड रेखाएँ बनाएं
`Pen` ऑब्जेक्ट रेखा का कलर, चौड़ाई, और डैश स्टाइल निर्धारित करता है, और इसे `drawLine` मेथड को पास किया जाता है ताकि रेखा रेंडर हो सके।
```java
graphic.drawLine(new Pen(Color.getBlue()), 9, 9, 90, 90);
graphic.drawLine(new Pen(Color.getBlue()), 9, 90, 90, 9);
```

## चरण 5: निरंतर रेखाएँ बनाएं
`SolidBrush` पेन के लिए सॉलिड फ़िल कलर प्रदान करता है, जिससे आप आसानी से रेखा का कलर सेट कर सकते हैं।
```java
graphic.drawLine(new Pen(new SolidBrush(Color.getRed())), new Point(9, 9), new Point(9, 90));
graphic.drawLine(new Pen(new SolidBrush(Color.getAqua())), new Point(9, 90), new Point(90, 90));
graphic.drawLine(new Pen(new SolidBrush(Color.getBlack())), new Point(90, 90), new Point(90, 9));
graphic.drawLine(new Pen(new SolidBrush(Color.getWhite())), new Point(90, 9), new Point(9, 9));
```

## चरण 6: इमेज को सहेजें
`Image` ऑब्जेक्ट पर `save` मेथड को कॉल करने से संशोधित PSD फ़ाइल निर्दिष्ट पाथ पर डिस्क में लिखी जाती है।
```java
image.save(outpath);
```

## निष्कर्ष
इन चरणों का पालन करके आपने Aspose.PSD for Java का उपयोग करके PSD फ़ाइल में सफलतापूर्वक रेखाएँ ड्रॉ की हैं। इस ट्यूटोरियल में PSD इमेज को इनिशियलाइज़ करना, ग्राफ़िक्स सेट अप करना, विभिन्न प्रकार की रेखाएँ ड्रॉ करना, और परिणामी इमेज को सेव करना शामिल था। अब आपके पास Java में ग्राफ़िक्स निर्माण को ऑटोमेट करने की एक ठोस नींव है।

## अक्सर पूछे जाने वाले प्रश्न
### Aspose.PSD for Java क्या है?
Aspose.PSD for Java एक शक्तिशाली Java लाइब्रेरी है जो प्रोग्रामेटिक रूप से PSD फ़ाइलों के साथ काम करने के लिए बनाई गई है।

### Aspose.PSD for Java की डॉक्यूमेंटेशन कहाँ मिल सकती है?
आप डॉक्यूमेंटेशन Aspose.PSD Java API रेफ़रेंस पेज पर पा सकते हैं: [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/)।

### क्या मैं Aspose.PSD for Java को खरीदने से पहले ट्राय कर सकता हूँ?
हाँ, आप Aspose रिलीज़ पेज से फ्री ट्रायल प्राप्त कर सकते हैं: [Aspose releases page](https://releases.aspose.com/)।

### Aspose.PSD for Java के लिए तकनीकी सपोर्ट कैसे प्राप्त करूँ?
तकनीकी सपोर्ट के लिए, [Aspose.PSD फोरम](https://forum.aspose.com/c/psd/34) पर जाएँ।

### Aspose.PSD for Java के लिए टेम्पररी लाइसेंस कहाँ प्राप्त करूँ?
आप Aspose खरीद पोर्टल पर टेम्पररी लाइसेंस प्राप्त कर सकते हैं: [Aspose temporary license page](https://purchase.aspose.com/temporary-license/)।

**अंतिम अपडेट:** 2026-09-08  
**परीक्षण किया गया:** Aspose.PSD for Java 24.12  
**लेखक:** Aspose

## संबंधित ट्यूटोरियल

- [Resize Image with Aspose.PSD for Java – Draw Shapes & Basic Image Operations](/psd/java/basic-image-operations/)
- [Draw and Save a Rectangle in a PSD using Aspose.PSD for Java](/psd/java/basic-image-operations/simple-drawing/)
- [Add Signature to Image – Draw Image on Canvas with Aspose.PSD for Java](/psd/java/advanced-image-effects/add-signature-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}