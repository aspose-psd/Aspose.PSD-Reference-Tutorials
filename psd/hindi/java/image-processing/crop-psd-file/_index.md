---
date: 2026-08-17
description: Aspose.PSD for Java के साथ जावा में PSD फ़ाइल को कैसे क्रॉप करें, सीखें
  – यह आपके Java एप्लिकेशन में Photoshop दस्तावेज़ों को तेज़ और सटीक रूप से ट्रिम
  करने का तरीका है।
keywords:
- crop psd file java
- aspose.psd java
- java image cropping
lastmod: 2026-08-17
linktitle: PSD फ़ाइल को क्रॉप करें
og_description: Aspose.PSD for Java का उपयोग करके जावा में PSD फ़ाइल को क्रॉप करें।
  यह गाइड आपको चरण‑दर‑चरण दिखाता है कि Photoshop फ़ाइलों को कुशलतापूर्वक कैसे ट्रिम
  किया जाए, कोड‑फ्री व्याख्याओं और सर्वोत्तम‑प्रैक्टिस टिप्स के साथ।
og_image_alt: Guide showing how to crop a PSD file in Java using Aspose.PSD
og_title: Aspose.PSD के साथ जावा में PSD फ़ाइल को क्रॉप करें – तेज़ इमेज क्रॉपिंग
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to crop psd file java with Aspose.PSD for Java – a fast,
    precise way to trim Photoshop documents in your Java applications.
  headline: Crop psd file java using Aspose.PSD
  type: TechArticle
- description: Learn how to crop psd file java with Aspose.PSD for Java – a fast,
    precise way to trim Photoshop documents in your Java applications.
  name: Crop psd file java using Aspose.PSD
  steps:
  - name: set document directory
    text: Replace “Your Document Directory” with the absolute or relative path that
      contains the PSD you want to process.
  - name: load PSD file
    text: The `RasterImage` class is Aspose.PSD’s entry point for raster‑based operations
      on a PSD file. Loading the file creates an in‑memory representation that you
      can manipulate.
  - name: define crop area
    text: '`Rectangle` defines the X and Y coordinates together with width and height
      of the region to keep. This class is part of the standard Java AWT package and
      is used by Aspose.PSD to specify cropping bounds.'
  - name: save cropped PSD
    text: After applying the crop, you can persist the result back to PSD format.
      The library writes only the cropped pixels, keeping the original color mode
      and bit depth.
  - name: save cropped image as PNG
    text: If you need a web‑friendly version, export the cropped raster to PNG. Aspose.PSD
      provides PNG save options that let you control compression level and interlacing.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java.
    question: What library handles PSD cropping in Java?
  - answer: Two API calls after loading the image.
    question: How many lines of code are required for a basic crop?
  - answer: Yes, using the built‑in PNG save options.
    question: Can I export the cropped area as PNG?
  - answer: A commercial license is needed beyond the trial period.
    question: Is a license required for production use?
  - answer: Java 8 and later, including Java 11, 17, and 21.
    question: What Java versions are supported?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- crop psd
- aspose.psd
- java image processing
title: Aspose.PSD का उपयोग करके जावा में PSD फ़ाइल को क्रॉप करें
url: /hi/java/image-processing/crop-psd-file/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD का उपयोग करके जावा में PSD फ़ाइल को क्रॉप करें

## परिचय

यदि आपको प्रोग्रामेटिक रूप से फ़ोटोशॉप दस्तावेज़ों को ट्रिम करने की आवश्यकता है, **crop psd file java** जावा डेवलपर्स के लिए एक सामान्य कार्य है जो ग्राफ़िक्स पाइपलाइन, एसेट पाइपलाइन, या स्वचालित डिज़ाइन वर्कफ़्लो पर काम करते हैं। Aspose.PSD for Java एक समर्पित API प्रदान करता है जो आपको कुछ पंक्तियों के कोड में एक आयत परिभाषित करने और आवश्यक क्षेत्र निकालने की अनुमति देता है। इस ट्यूटोरियल में आप सीखेंगे कि लाइब्रेरी उच्च‑प्रदर्शन क्रॉपिंग के लिए क्यों बनाई गई है, अपने वातावरण को कैसे सेटअप करें, और PSD और PNG दोनों परिणाम उत्पन्न करने के सटीक चरण।

## त्वरित उत्तर
- **Java में PSD क्रॉपिंग को संभालने वाली लाइब्रेरी कौन सी है?** Aspose.PSD for Java.
- **बेसिक क्रॉप के लिए कितनी पंक्तियों का कोड आवश्यक है?** इमेज लोड करने के बाद दो API कॉल्स।
- **क्या मैं क्रॉप किए गए क्षेत्र को PNG के रूप में एक्सपोर्ट कर सकता हूँ?** हाँ, बिल्ट‑इन PNG सेव ऑप्शन का उपयोग करके।
- **क्या प्रोडक्शन उपयोग के लिए लाइसेंस आवश्यक है?** ट्रायल अवधि के बाद एक वाणिज्यिक लाइसेंस आवश्यक है।
- **कौन से Java संस्करण समर्थित हैं?** Java 8 और उसके बाद के संस्करण, जिसमें Java 11, 17, और 21 शामिल हैं।

## crop psd file java क्या है?

Crop psd file java उस प्रक्रिया को दर्शाता है जिसमें जावा कोड का उपयोग करके फ़ोटोशॉप डॉक्यूमेंट (.psd) से आयताकार क्षेत्र को प्रोग्रामेटिक रूप से काटा जाता है। Aspose.PSD के साथ आप यह ऑपरेशन फ़ोटोशॉप लॉन्च किए बिना कर सकते हैं, जिससे यह सर्वर‑साइड इमेज पाइपलाइन के लिए आदर्श बन जाता है।

## Aspose.PSD for Java का उपयोग क्यों करें?

Aspose.PSD **30+ इनपुट और आउटपुट फॉर्मेट** का समर्थन करता है और अपनी स्ट्रीमिंग आर्किटेक्चर के कारण पूरे दस्तावेज़ को मेमोरी में लोड किए बिना **500 MB** तक की PSD फ़ाइलों को प्रोसेस कर सकता है। लाइब्रेरी लेयर्स, मास्क और कलर प्रोफ़ाइल को संरक्षित रखती है, जिससे प्राप्त क्रॉप्ड परिणाम फ़ोटोशॉप के मूल आउटपुट से मेल खाता है। यह मापी गई प्रदर्शन आपको कम लागत वाले हार्डवेयर पर बैच जॉब्स को पूर्वानुमानित मेमोरी उपयोग के साथ संभालने की अनुमति देता है।

## आवश्यकताएँ

- **Java विकास वातावरण** – JDK 8 या नया स्थापित और कॉन्फ़िगर किया हुआ।
- **Aspose.PSD for Java** – नवीनतम JAR और दस्तावेज़ डाउनलोड करें [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).
- **सैंपल PSD फ़ाइल** – .psd फ़ाइल को अपने प्रोजेक्ट डायरेक्टरी में रखें ताकि कोड उसे खोज सके।

## जावा में PSD फ़ाइल को कैसे क्रॉप करें?

सोर्स फ़ाइल को लोड करें, वह आयत परिभाषित करें जिसे आप रखना चाहते हैं, क्रॉप लागू करें, और अंत में परिणाम को इच्छित फॉर्मेट में सहेजें। पूरा वर्कफ़्लो केवल पाँच सरल चरणों में पूरा होता है, प्रत्येक को एक प्लेसहोल्डर के साथ दर्शाया गया है जहाँ आप अपना कोड डालेंगे।

### चरण 1: दस्तावेज़ डायरेक्टरी सेट करें

“Your Document Directory” को उस पूर्ण या सापेक्ष पाथ से बदलें जिसमें वह PSD हो जो आप प्रोसेस करना चाहते हैं।

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.xmp.types.complex.colorant.ColorType;
```

### चरण 2: PSD फ़ाइल लोड करें

`RasterImage` क्लास Aspose.PSD का एंट्री पॉइंट है जो PSD फ़ाइल पर रास्टर‑आधारित ऑपरेशन्स के लिए उपयोग होता है। फ़ाइल को लोड करने से एक इन‑मेमोरी प्रतिनिधित्व बनता है जिसे आप संशोधित कर सकते हैं।

```java
String dataDir = "Your Document Directory";
```

### चरण 3: क्रॉप क्षेत्र परिभाषित करें

`Rectangle` X और Y निर्देशांक के साथ-साथ रखे जाने वाले क्षेत्र की चौड़ाई और ऊँचाई को परिभाषित करता है। यह क्लास स्टैंडर्ड Java AWT पैकेज का हिस्सा है और Aspose.PSD द्वारा क्रॉपिंग बाउंड्स निर्दिष्ट करने के लिए उपयोग की जाती है।

```java
String sourceFileName = dataDir + "1.psd";
RasterImage image = (RasterImage)Image.load(sourceFileName);
```

### चरण 4: क्रॉप किया गया PSD सहेजें

क्रॉप लागू करने के बाद, आप परिणाम को फिर से PSD फॉर्मेट में सहेज सकते हैं। लाइब्रेरी केवल क्रॉप किए गए पिक्सेल लिखती है, मूल कलर मोड और बिट डेप्थ को बरकरार रखती है।

```java
image.crop(new Rectangle(10, 30, 100, 100));
```

### चरण 5: क्रॉप की गई इमेज को PNG के रूप में सहेजें

यदि आपको वेब‑फ़्रेंडली संस्करण चाहिए, तो क्रॉप किए गए रास्टर को PNG में एक्सपोर्ट करें। Aspose.PSD PNG सेव ऑप्शन प्रदान करता है जो आपको कम्प्रेशन लेवल और इंटरलेसिंग को नियंत्रित करने देता है।

```java
String exportPathPsd = dataDir + "CropTest.psd";
image.save(exportPathPsd, new PsdOptions());
```

## सामान्य समस्याएँ और समाधान

- **गलत आयत निर्देशांक** – सुनिश्चित करें कि X/Y मान शीर्ष‑बाएँ कोने के लिए 0 से शुरू हों; नकारात्मक मान `ArgumentException` उत्पन्न करेंगे।
- **बड़ी फ़ाइलों पर मेमोरी स्पाइक** – जब आपको छिपी लेयर्स की आवश्यकता न हो तो मेमोरी कम करने के लिए `loadOptions.setLoadOnlyVisibleLayers(true)` विकल्प का उपयोग करें।
- **कलर प्रोफ़ाइल का नुकसान** – क्रॉप करने से पहले `image.getColorProfile()` कॉल करके मूल ICC प्रोफ़ाइल को संरक्षित रखें और ऑपरेशन के बाद उसे पुनः असाइन करें।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: क्या मैं Aspose.PSD for Java का उपयोग अन्य फॉर्मेट में इमेज क्रॉप करने के लिए कर सकता हूँ?

A1: Aspose.PSD मुख्यतः PSD फ़ाइलों को लक्षित करता है, लेकिन यह BMP, GIF, JPEG, PNG, TIFF और कई अन्य रास्टर फॉर्मेट को इनपुट और आउटपुट दोनों के लिए भी समर्थन देता है।

### प्रश्न 2: क्या Aspose.PSD for Java बड़े‑पैमाने पर इमेज प्रोसेसिंग के लिए उपयुक्त है?

A2: हाँ। लाइब्रेरी की स्ट्रीमिंग आर्किटेक्चर कई‑सौ‑पृष्ठीय PSD फ़ाइलों को 100 MB से कम मेमोरी फुटप्रिंट के साथ प्रोसेस करती है, जिससे यह बैच जॉब्स के लिए आदर्श है।

### प्रश्न 3: Aspose.PSD for Java के उपयोग के लिए कोई लाइसेंस संबंधी विचार हैं?

A3: प्रोडक्शन डिप्लॉयमेंट के लिए एक वाणिज्यिक लाइसेंस आवश्यक है। विवरण [Aspose.PSD for Java purchase page](https://purchase.aspose.com/buy) पर उपलब्ध हैं।

### प्रश्न 4: Aspose.PSD for Java‑संबंधित मुद्दों के लिए समर्थन कैसे प्राप्त करूँ?

A4: समर्थन के लिए [Aspose.PSD for Java forum](https://forum.aspose.com/c/psd/34) पर जाएँ, जहाँ आप प्रश्न पूछ सकते हैं, कोड स्निपेट साझा कर सकते हैं, और समुदाय व प्रोडक्ट इंजीनियर्स से मदद प्राप्त कर सकते हैं।

### प्रश्न 5: क्या मैं Aspose.PSD for Java को खरीदने से पहले आज़मा सकता हूँ?

A5: हाँ, एक पूरी तरह कार्यात्मक फ्री ट्रायल [Aspose.PSD free trial download](https://releases.aspose.com/) से डाउनलोड किया जा सकता है।

{{< blocks/products/products-backtop-button >}}

```java
String exportPathPng = dataDir + "CropTest.png";
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
image.save(exportPathPng, options);
```

## संबंधित ट्यूटोरियल

- [Aspose.PSD for Java में आयत द्वारा इमेज क्रॉप करें](/psd/java/image-editing/crop-image-by-rectangle/)
- [Aspose.PSD for Java में शिफ्ट्स द्वारा इमेज क्रॉप करें](/psd/java/image-editing/crop-image-by-shifts/)
- [Aspose.PSD के साथ जावा में इमेज कैसे घुमाएँ](/psd/java/advanced-image-manipulation/rotate-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}