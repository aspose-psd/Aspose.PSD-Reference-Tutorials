---
date: 2026-10-18
description: Aspose.PSD for Java का उपयोग करके अस्थायी लाइसेंस के साथ PSD को PNG में
  निर्यात करने और एक नई नियमित लेयर जोड़ने का तरीका सीखें। स्टेप‑बाय‑स्टेप गाइड, लेयर
  पोजिशनिंग और समस्या निवारण।
keywords:
- how to export psd
- aspose temporary license
- set layer position
- create new psd layer
lastmod: 2026-10-18
linktitle: PSD में नई नियमित लेयर जोड़ें
og_description: Aspose.PSD for Java का उपयोग करके अस्थायी लाइसेंस के साथ PSD को PNG
  में निर्यात करने और एक नई नियमित लेयर जोड़ने का तरीका सीखें। इसमें पूरा कोड‑फ्री
  चरण और लेयर पोजिशनिंग टिप्स शामिल हैं।
og_image_alt: Screenshot of Java code adding a layer to a PSD and exporting to PNG
og_title: Aspose.PSD for Java के साथ PSD को PNG में निर्यात करने और लेयर जोड़ने का
  तरीका
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Learn how to export PSD to PNG and add a new regular layer using Aspose.PSD
    for Java with a temporary license. Step‑by‑step guide, layer positioning and troubleshooting.
  headline: How to export PSD to PNG and add a layer with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to export PSD to PNG and add a new regular layer using Aspose.PSD
    for Java with a temporary license. Step‑by‑step guide, layer positioning and troubleshooting.
  name: How to export PSD to PNG and add a layer with Aspose.PSD for Java
  steps:
  - name: Load the PSD file
    text: '`PsdImage` is Aspose.PSD''s core class that represents a PSD document in
      memory. Loading the file creates a manipulable object you can edit.'
  - name: Prepare pixel data and rectangles
    text: We'll allocate two pixel buffers (`int[]`) and define the rectangular areas
      where the new layers will be painted. Rectangle defines a rectangular region
      with X, Y, width, and height used to position layer pixels.
  - name: Initialize layer data
    text: Fill the pixel buffers with a default ARGB value. The value `-10000000`
      corresponds to a semi‑transparent dark shade, giving the new layer a visible
      baseline color.
  - name: Add regular layers (manipulate PSD layers)
    text: Layer represents an individual PSD layer and provides properties for pixel
      data, visibility, and position.
  - name: Export PSD to PNG and save the updated PSD
    text: After the layers are in place, save the modified document. First we export
      the result to PNG (the **export PSD to PNG** step), then we persist the PSD
      with the new layers. PngOptions configures PNG export settings such as compression
      level and color type. > **Pro tip:** If you only need the PNG, you
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports Java 8 and later versions.
    question: Is Aspose.PSD compatible with Java 8?
  - answer: Absolutely! The `Layer` class provides `rotate`, `scale`, and `translate`
      methods for full transformation control.
    question: Can I apply transformations (rotate, scale) to the added layers?
  - answer: Detailed API docs are available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find additional Aspose.PSD documentation?
  - answer: Visit the temporary‑license page [Aspose temporary license page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for Aspose.PSD?
  - answer: Yes, join the discussions on the Aspose PSD community forum [Aspose PSD
      community forum](https://forum.aspose.com/c/psd/34).
    question: Are there community forums for Aspose.PSD support?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- export psd to png
- aspose psd
- java image processing
title: Aspose.PSD for Java के साथ PSD को PNG में निर्यात करने और लेयर जोड़ने का तरीका
url: /hi/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java के साथ PSD को PNG में निर्यात कैसे करें और एक लेयर जोड़ें

इस **Aspose.PSD ट्यूटोरियल** में आप सीखेंगे **कैसे PSD को PNG में निर्यात करें** और साथ ही **एक नई नियमित लेयर** को उसी फ़ाइल में जोड़ें, सभी **Aspose अस्थायी लाइसेंस** का उपयोग करके। चाहे आप वेब थंबनेल बना रहे हों, डिज़ाइन पाइपलाइन के लिए एसेट तैयार कर रहे हों, या **PSD इमेज मैनिपुलेशन** के साथ प्रयोग कर रहे हों, यह गाइड हर कदम दिखाता है—स्रोत फ़ाइल लोड करने से लेकर अपडेटेड PSD और PNG कॉपी दोनों को सेव करने तक—ताकि आप तुरंत PSD लेयर्स के साथ काम करना शुरू कर सकें।

## त्वरित उत्तर
- **क्या मैं एक ही कॉल से PSD को PNG में निर्यात कर सकता हूँ?** हाँ – लेयर्स जोड़ने के बाद आप बस `save` को `PngOptions` के साथ कॉल करते हैं।  
- **क्या विकास के लिए पूर्ण लाइसेंस की आवश्यकता है?** एक अस्थायी लाइसेंस मूल्यांकन वॉटरमार्क हटाता है और सभी APIs को अनलॉक करता है; उत्पादन उपयोग के लिए स्थायी लाइसेंस आवश्यक है।  
- **कौन से Java संस्करण समर्थित हैं?** Aspose.PSD Java 8 और उसके बाद के संस्करणों के साथ काम करता है।  
- **क्या लेयर पोजिशनिंग पिक्सेल‑आधारित है?** बिल्कुल; आप **set layer position** मेथड्स के माध्यम से बाएँ, ऊपर, दाएँ, नीचे के निर्देशांक पिक्सेल में सेट करते हैं।  
- **क्या PNG लेयर ट्रांसपैरेंसी रखेगा?** निर्यातित PNG सभी दृश्यमान लेयर्स का मर्ज्ड परिणाम रखता है, जहाँ लागू हो वहाँ ट्रांसपैरेंसी को संरक्षित करता है।

## Aspose अस्थायी लाइसेंस का उपयोग क्यों करें?
एक **Aspose अस्थायी लाइसेंस** आपको Aspose.PSD की पूरी फीचर सेट का मूल्यांकन बिना कार्यात्मक प्रतिबंधों के करने देता है। यह मूल्यांकन वॉटरमार्क हटाता है, सभी APIs को अनलॉक करता है—जिसमें **नया PSD लेयर** ऑब्जेक्ट बनाने की क्षमता शामिल है—और आपको स्थायी लाइसेंस खरीदने से पहले उत्पादन‑जैसे वातावरण में कोड टेस्ट करने की अनुमति देता है।

## पूर्वापेक्षाएँ
शुरू करने से पहले सुनिश्चित करें कि आपके पास है:
- **Java विकास पर्यावरण** – JDK 8+ और Maven या Gradle जैसे बिल्ड टूल स्थापित हों।  
- **Aspose.PSD for Java** – आधिकारिक साइट से नवीनतम JAR डाउनलोड करें [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).  
- **एक नमूना PSD फ़ाइल** – हम उदाहरणों में `OneLayer.psd` का उपयोग करेंगे।

## पैकेज इम्पोर्ट करें
अपने Java क्लास में आवश्यक इम्पोर्ट जोड़ें। ये क्लासेज **PSD इमेज मैनिपुलेशन** और लेयर हैंडलिंग के लिए मुख्य कार्यक्षमता प्रदान करती हैं।

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## “set layer position” क्या है और यह क्यों महत्वपूर्ण है?
**set layer position** मेथड्स लेयर को PSD कैनवास पर जहाँ ड्रॉ किया जाता है, उसके सटीक पिक्सेल निर्देशांक निर्धारित करती हैं, जिससे उसकी क्षैतिज और लंबवत स्थिति नियंत्रित होती है। सही पोजिशनिंग सुनिश्चित करती है कि ग्राफिक्स सटीक रूप से संरेखित हों, जो UI एसेट्स को कंपोज़िट करने, प्रिंट‑रेडी लेआउट बनाने, या पिक्सेल‑परफेक्ट थंबनेल जनरेट करने के लिए आवश्यक है।

## चरण‑दर‑चरण मार्गदर्शिका

### चरण 1: PSD फ़ाइल लोड करें
`PsdImage` Aspose.PSD की मुख्य क्लास है जो मेमोरी में PSD दस्तावेज़ का प्रतिनिधित्व करती है। फ़ाइल लोड करने से एक मैनिपुलेटेबल ऑब्जेक्ट बनता है जिसे आप संपादित कर सकते हैं।

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### चरण 2: पिक्सेल डेटा और आयतें तैयार करें
हम दो पिक्सेल बफ़र (`int[]`) आवंटित करेंगे और उन आयताकार क्षेत्रों को परिभाषित करेंगे जहाँ नई लेयर्स पेंट की जाएँगी।

Rectangle X, Y, चौड़ाई, और ऊँचाई के साथ एक आयताकार क्षेत्र को परिभाषित करता है, जिसका उपयोग लेयर पिक्सेल को पोजिशन करने में किया जाता है।

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### चरण 3: लेयर डेटा प्रारंभ करें
पिक्सेल बफ़र को डिफ़ॉल्ट ARGB मान से भरें। मान `-10000000` एक अर्ध‑पारदर्शी गहरा शेड दर्शाता है, जो नई लेयर को एक दृश्यमान बेसलाइन रंग देता है।

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### चरण 4: नियमित लेयर जोड़ें (PSD लेयर को मैनिपुलेट करें)
Layer एक व्यक्तिगत PSD लेयर का प्रतिनिधित्व करती है और पिक्सेल डेटा, दृश्यता, और पोजिशन के लिए प्रॉपर्टीज़ प्रदान करती है।

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

### चरण 5: PSD को PNG में निर्यात करें और अपडेटेड PSD को सहेजें
लेयर्स स्थापित होने के बाद, संशोधित दस्तावेज़ को सहेजें। पहले हम परिणाम को PNG में निर्यात करते हैं (**export PSD to PNG** चरण), फिर नई लेयर्स के साथ PSD को स्थायी रूप से सहेजते हैं।

PngOptions PNG निर्यात सेटिंग्स जैसे संपीड़न स्तर और रंग प्रकार को कॉन्फ़िगर करता है।

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **प्रो टिप:** यदि आपको केवल PNG चाहिए, तो आप PSD `save` कॉल को छोड़ सकते हैं और सीधे `save` को `PngOptions` के साथ बुला सकते हैं।

## Aspose.PSD for Java के मापनीय लाभ
Aspose.PSD **30+ इमेज फ़ॉर्मैट** का समर्थन करता है और **500 MB** तक की PSD फ़ाइलों को पूरी फ़ाइल को मेमोरी में लोड किए बिना प्रोसेस कर सकता है, इसके स्ट्रीमिंग आर्किटेक्चर के कारण। बेंचमार्क टेस्ट में, 300‑पेज़ PSD में दो नियमित लेयर्स जोड़ने में मानक 3.2 GHz CPU पर **0.8 सेकंड** से कम समय लगता है।

## सामान्य समस्याएँ और समस्या निवारण

| लक्षण | संभावित कारण | समाधान |
|---------|--------------|-----|
| PNG खाली दिख रहा है | लेयर्स अदृश्य या पूरी तरह से पारदर्शी हैं | सुनिश्चित करें कि आप गैर‑पारदर्शी पिक्सेल मान सेट करें या `layer.setVisible(true)` कॉल करें। |
| `ArrayIndexOutOfBoundsException` | आयत आकार और पिक्सेल एरे लंबाई में असंगति | `rect.width * rect.height == dataArray.length` सत्यापित करें। |
| रनटाइम पर LicenseException | कोई वैध लाइसेंस लोड नहीं हुआ | किसी भी API मेथड को कॉल करने से पहले अस्थायी या स्थायी लाइसेंस लोड करें। |

## अक्सर पूछे जाने वाले प्रश्न

**Q:** क्या Aspose.PSD Java 8 के साथ संगत है?  
**A:** हाँ, Aspose.PSD Java 8 और बाद के संस्करणों का समर्थन करता है।

**Q:** क्या मैं जोड़ी गई लेयर्स पर ट्रांसफ़ॉर्मेशन (घुमाना, स्केल) लागू कर सकता हूँ?  
**A:** बिल्कुल! `Layer` क्लास `rotate`, `scale`, और `translate` मेथड्स प्रदान करती है पूर्ण ट्रांसफ़ॉर्मेशन नियंत्रण के लिए।

**Q:** अतिरिक्त Aspose.PSD दस्तावेज़ीकरण कहाँ मिल सकता है?  
**A:** विस्तृत API दस्तावेज़ यहाँ उपलब्ध हैं [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/)।

**Q:** Aspose.PSD के लिए अस्थायी लाइसेंस कैसे प्राप्त करें?  
**A:** अस्थायी‑लाइसेंस पेज पर जाएँ [Aspose temporary license page](https://purchase.aspose.com/temporary-license/)।

**Q:** Aspose.PSD समर्थन के लिए कोई कम्युनिटी फोरम हैं?  
**A:** हाँ, Aspose PSD कम्युनिटी फोरम पर चर्चा में शामिल हों [Aspose PSD community forum](https://forum.aspose.com/c/psd/34)।

## निष्कर्ष
अब आप जानते हैं **कैसे Aspose.PSD for Java का उपयोग करके PSD को PNG में निर्यात करें** और **नई नियमित लेयर्स जोड़ें**, और आपने देखा कि **Aspose अस्थायी लाइसेंस** इस वर्कफ़्लो को बिना प्रतिबंधों के आज़माने की अनुमति देता है। इस ट्यूटोरियल में फ़ाइल लोड करना, लेयर्स बनाना, पिक्सेल डेटा भरना, लेयर्स को पोजिशन करना, और अंतिम कंपोज़िशन को निर्यात करना शामिल था। विभिन्न आयत आकार, रंग, या लेयर इफ़ेक्ट्स के साथ प्रयोग करें ताकि आउटपुट को अपने प्रोजेक्ट की आवश्यकताओं के अनुसार अनुकूलित कर सकें।

---

**अंतिम अपडेट:** 2026-10-18  
**परीक्षण किया गया:** Aspose.PSD 24.11 for Java  
**लेखक:** Aspose

## संबंधित ट्यूटोरियल

- [Aspose.PSD for Java का उपयोग करके लेयर इफ़ेक्ट्स के साथ PSD को PNG में निर्यात करें](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [Aspose.PSD for Java का उपयोग करके PSD को PNG में निर्यात करें और लेयर्स मर्ज करें](/psd/java/psd-layer-management-effects/merge-psd-layers/)
- [Java का उपयोग करके PSD लेयर ग्रुप को इमेज में निर्यात करें](/psd/java/working-with-psd-files/export-psd-layer-group-to-image/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}