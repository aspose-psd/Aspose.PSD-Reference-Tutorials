---
date: 2026-07-08
description: 'Java इमेज एडिटिंग लाइब्रेरी ट्यूटोरियल: सीखें कैसे Crop Image Java का
  उपयोग करके Aspose.PSD for Java, Resize, Expand Canvas, और Convert PSD to JPEG.'
keywords:
- java image editing library
- java image processing tutorial
- how to crop image java
lastmod: 2026-07-08
linktitle: Expand और Crop Images
og_description: Java इमेज एडिटिंग लाइब्रेरी ट्यूटोरियल दिखाता है कैसे Crop, Expand
  Canvas, और Convert PSD to JPEG को Aspose.PSD for Java का उपयोग करके मिनटों में किया
  जा सकता है।
og_image_alt: 'Guide: Crop and expand images in Java with Aspose.PSD'
og_title: Java इमेज एडिटिंग लाइब्रेरी – Crop Image with Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-07-08'
  description: 'Java image editing library tutorial: learn how to crop image java
    using Aspose.PSD for Java, resize, expand canvas, and convert PSD to JPEG.'
  headline: Java Image Editing Library – Crop Image with Aspose.PSD
  type: TechArticle
- questions:
  - answer: Aspose.PSD for Java.
    question: What library handles crop image java?
  - answer: A free trial works for testing; a commercial license is required for production.
    question: Do I need a license for development?
  - answer: Yes, using `JpegOptions` together with a cropping rectangle.
    question: Can I convert PSD to JPEG while cropping?
  - answer: Aspose.PSD supports Java 8 and newer versions.
    question: Is Java 8 supported?
  - answer: Typically under 10 minutes for a basic crop operation.
    question: How long does the implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image editing
- Aspose.PSD
- image cropping
- PSD to JPEG
title: Java इमेज एडिटिंग लाइब्रेरी – Crop Image with Aspose.PSD
url: /hi/java/image-editing/expand-and-crop-images/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java इमेज एडिटिंग लाइब्रेरी: Aspose.PSD के साथ Java में इमेज क्रॉप करें

## परिचय

इस ट्यूटोरियल में आप सीखेंगे कि कैसे एक **java image editing library**—विशेष रूप से Aspose.PSD for Java—का उपयोग करके PSD फ़ाइलों को क्रॉप, विस्तारित और JPEG में परिवर्तित किया जाता है। चाहे आप वेब पोर्टल के लिए एसेट तैयार कर रहे हों या थंबनेल जेनरेशन को स्वचालित कर रहे हों, नीचे दिए गए चरण एक दोहराने योग्य, प्रोडक्शन‑रेडी वर्कफ़्लो प्रदान करते हैं जिसे आप किसी भी Java 8+ प्रोजेक्ट में एकीकृत कर सकते हैं।

## त्वरित उत्तर
- **Java में इमेज क्रॉप करने के लिए कौन सी लाइब्रेरी उपयोग होती है?** Aspose.PSD for Java.  
- **क्या विकास के लिए लाइसेंस की आवश्यकता है?** परीक्षण के लिए एक फ्री ट्रायल काम करता है; प्रोडक्शन के लिए एक वाणिज्यिक लाइसेंस आवश्यक है।  
- **क्या मैं क्रॉप करते समय PSD को JPEG में बदल सकता हूँ?** हाँ, `JpegOptions` को क्रॉपिंग रेक्टैंगल के साथ उपयोग करके।  
- **क्या Java 8 समर्थित है?** Aspose.PSD Java 8 और नए संस्करणों को समर्थन देता है।  
- **इम्प्लीमेंटेशन में कितना समय लगता है?** सामान्यतः बुनियादी क्रॉप ऑपरेशन के लिए 10 मिनट से कम।

## “crop image java” क्या है?

Crop image java का अर्थ है स्रोत चित्र के एक आयताकार क्षेत्र का चयन करना और उस क्षेत्र के बाहर की सभी सामग्री को हटाना। Aspose.PSD के साथ, आप एक `Rectangle` बनाते हैं जो क्षेत्र को परिभाषित करता है, इसे `RasterImage` पर लागू करते हैं, और फिर परिणाम को JPEG जैसे किसी भी समर्थित फ़ॉर्मेट में सहेजते हैं।

## Java इमेज क्रॉपिंग के लिए Aspose.PSD क्यों उपयोग करें?

Aspose.PSD एक **java image editing library** प्रदान करता है जो PSD फ़ाइलों को मूल रूप से संभालता है, 100 से अधिक लेयर सुविधाओं का समर्थन करता है, और 10 000 × 10 000 पिक्सेल तक की छवियों को प्रोसेस कर सकता है जबकि मेमोरी उपयोग 500 MB से कम रहता है। यह JPEG, PNG, BMP आदि में बिल्ट‑इन रूपांतरण भी प्रदान करता है, बिना किसी बाहरी टूल की आवश्यकता के। इससे बल्क‑प्रोसेसिंग पाइपलाइन तेज़, विश्वसनीय और रखरखाव में आसान बनती है।

## आवश्यकताएँ

1. **Java Development Kit (JDK)** – Java 8 या बाद का संस्करण स्थापित हो।  
2. **Aspose.PSD for Java** – आधिकारिक साइट से लाइब्रेरी डाउनलोड करें **[यहाँ](https://releases.aspose.com/psd/java/)**।  

> **Pro tip:** `ClassNotFoundException` से बचने के लिए Aspose.PSD JAR को अपने प्रोजेक्ट के क्लासपाथ या Maven/Gradle डिपेंडेंसीज़ में जोड़ें।

## पैकेज इम्पोर्ट करें

अपने Java स्रोत फ़ाइल में आवश्यक इम्पोर्ट जोड़ें। ये क्लासेज़ आपको इमेज लोडिंग, रास्टर मैनिपुलेशन, रेक्टैंगल परिभाषा, और JPEG एक्सपोर्ट विकल्पों तक पहुंच प्रदान करती हैं।

## Aspose.PSD का उपयोग करके Java में इमेज कैसे क्रॉप करें?

`RasterImage` के साथ स्रोत PSD लोड करें, एक `Rectangle` परिभाषित करें जो क्रॉप क्षेत्र को दर्शाता है (नकारात्मक निर्देशांक कैनवास को विस्तारित कर सकते हैं), और अंत में `JpegOptions` के साथ परिणाम सहेजें। यह तीन‑स्टेप प्रक्रिया दोनों क्रॉपिंग और फ़ॉर्मेट रूपांतरण को एक ही पास में संभालती है, जिससे मध्यवर्ती फ़ाइलों की आवश्यकता समाप्त हो जाती है।

## चरण 1: अपना डॉक्यूमेंट डायरेक्टरी सेट करें

उस फ़ोल्डर को निर्दिष्ट करें जिसमें स्रोत PSD फ़ाइल मौजूद है। प्लेसहोल्डर को अपने मशीन पर वास्तविक पाथ से बदलें।

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

## चरण 2: स्रोत और गंतव्य पाथ निर्दिष्ट करें

निर्धारित करें कि PSD को कहाँ से पढ़ना है और क्रॉप किया हुआ JPEG कहाँ लिखना है।

```java
String dataDir = "Your Document Directory";
```

## चरण 3: इमेज लोड करें और कैश करें

`RasterImage` मेमोरी में PSD फ़ाइल का रास्टराइज़्ड संस्करण दर्शाता है।  
PSD को एक `RasterImage` ऑब्जेक्ट में लोड करें। कैशिंग क्रॉपिंग जैसे बाद के ऑपरेशन्स के लिए प्रदर्शन को बेहतर बनाता है।

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## चरण 4: क्रॉपिंग के लिए रेक्टैंगल बनाएं

`Rectangle` क्रॉपिंग क्षेत्र के X, Y निर्देशांक और चौड़ाई/ऊँचाई को परिभाषित करता है।  
एक `Rectangle` बनाएं जो उस क्षेत्र को वर्णित करता है जिसे आप रखना चाहते हैं। निर्देशांक नकारात्मक हो सकते हैं ताकि क्रॉप करने से पहले कैनवास **विस्तारित** हो सके, जो मूल इमेज के चारों ओर बॉर्डर जोड़ने में उपयोगी है।

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

> **नकारात्मक निर्देशांक क्यों उपयोग करें?**  
> नकारात्मक X/Y मान क्रॉप क्षेत्र को बाएँ/ऊपर शिफ्ट करते हैं, जिससे अंतिम क्रॉप से पहले मूल सामग्री के चारों ओर खाली जगह (विस्तार) जोड़ दी जाती है।

## चरण 5: क्रॉप की गई इमेज सहेजें

`JpegOptions` JPEG आउटपुट के लिए सेटिंग्स निर्दिष्ट करता है, जैसे क्वालिटी और कम्प्रेशन।  
अंत में, `JpegOptions` का उपयोग करके परिणामी इमेज सहेजें। यह चरण **convert psd jpeg** को भी दर्शाता है जबकि क्रॉपिंग रेक्टैंगल लागू किया जाता है।

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

> **परिणाम:** `jpeg_out.jpg` अब एक 300 × 300 पिक्सेल इमेज रखता है जिसे प्रत्येक पक्ष पर 200 px द्वारा विस्तारित किया गया था और फिर परिभाषित रेक्टैंगल में क्रॉप किया गया।

बधाई हो! आपने सफलतापूर्वक **java image cropping** किया, कैनवास विस्तारित किया, और एक PSD फ़ाइल को JPEG में परिवर्तित किया—सभी कुछ संक्षिप्त कोड लाइनों में।

## सामान्य उपयोग केस

- **वेब के लिए एसेट तैयार करना** – अपलोड करने से पहले स्क्रीनशॉट या डिज़ाइन को क्रॉप और रिसाइज़ करें।  
- **थंबनेल जनरेट करना** – प्रीव्यू के लिए बड़े PSD से एक विशिष्ट क्षेत्र निकालें।  
- **ऑटोमेटेड बैच प्रोसेसिंग** – PSD फ़ाइलों के फ़ोल्डर के माध्यम से लूप करें, प्रत्येक पर समान क्रॉप रेक्टैंगल लागू करें।

## समस्या निवारण और टिप्स

| समस्या | सुझावित समाधान |
|-------|----------------|
| `OutOfMemoryError` जब बड़े PSD लोड किए जा रहे हों | `rasterImage.cacheData()` को जल्दी कॉल करें और JVM हीप साइज (`-Xmx`) बढ़ाने पर विचार करें। |
| क्रॉप किया गया क्षेत्र केंद्र से हटकर है | रेक्टैंगल के X/Y ऑफ़सेट की जाँच करें; याद रखें नकारात्मक मान कैनवास को विस्तारित करते हैं। |
| आउटपुट JPEG धुंधला दिख रहा है | `JpegOptions` की क्वालिटी सेटिंग को समायोजित करें (जैसे, `new JpegOptions { Quality = 90 }`). |

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.PSD विभिन्न Java संस्करणों के साथ संगत है?
A1: हाँ, Aspose.PSD Java 8, 11, 17 और नए रिलीज़ को समर्थन देता है, जिससे विकास वातावरण में व्यापक संगतता सुनिश्चित होती है।

### Q2: क्या मैं Aspose.PSD को वाणिज्यिक प्रोजेक्ट्स में उपयोग कर सकता हूँ?
A2: बिल्कुल, Aspose.PSD डेवलपर्स के लिए वाणिज्यिक लाइसेंस प्रदान करता है, जिससे इसे व्यक्तिगत और वाणिज्यिक दोनों एप्लिकेशन में उपयोग किया जा सकता है।

### Q3: क्या समर्थित इमेज फ़ाइल फ़ॉर्मेट्स पर कोई सीमाएँ हैं?
A3: Aspose.PSD 30+ इमेज फ़ॉर्मेट्स को समर्थन देता है, जिसमें PSD, JPEG, PNG, BMP, TIFF आदि शामिल हैं। पूरी सूची के लिए [डॉक्यूमेंटेशन](https://reference.aspose.com/psd/java/) देखें।

### Q4: Aspose.PSD‑संबंधी प्रश्नों के लिए समर्थन कैसे प्राप्त करूँ?
A4: समुदाय या Aspose समर्थन टीम से सहायता प्राप्त करने के लिए [Aspose.PSD फ़ोरम](https://forum.aspose.com/c/psd/34) पर जाएँ।

### Q5: क्या कोई फ्री ट्रायल उपलब्ध है?
A5: हाँ, आप Aspose.PSD को फ्री ट्रायल के साथ एक्सप्लोर कर सकते हैं। इसे [यहाँ](https://releases.aspose.com/) डाउनलोड करें।

---

**अंतिम अपडेट:** 2026-07-08  
**परीक्षित संस्करण:** Aspose.PSD for Java 24.12  
**लेखक:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

## संबंधित ट्यूटोरियल

- [Aspose.PSD के साथ सरल आकार बदलना – Java Image Manipulation Library](/psd/java/basic-image-operations/simple-resizing/)
- [Aspose.PSD for Java के साथ इमेज को 270 डिग्री घुमाएँ](/psd/java/advanced-image-manipulation/rotate-image/)
- [Aspose.PSD के साथ Java इमेज प्रोसेसिंग में गामा कैसे समायोजित करें](/psd/java/advanced-techniques/adjust-gamma/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}