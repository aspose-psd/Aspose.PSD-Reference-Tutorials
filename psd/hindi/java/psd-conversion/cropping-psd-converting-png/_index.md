---
date: 2026-03-21
description: Aspose.PSD for Java का उपयोग करके PSD को PNG में कैसे बदलें और PSD फ़ाइलों
  को कैसे क्रॉप करें, सीखें। यह गाइड जावा एप्लिकेशनों में चरण‑दर‑चरण इमेज प्रोसेसिंग
  दिखाता है।
linktitle: Cropping PSD when Converting to PNG
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java का उपयोग करके क्रॉपिंग करते हुए PSD को PNG में कैसे बदलें
url: /hi/java/psd-conversion/cropping-psd-converting-png/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java के साथ क्रॉपिंग करते हुए PSD को PNG में कैसे बदलें

## Introduction
Java विकास की गतिशील दुनिया में, कुशल इमेज प्रोसेसिंग में महारत हासिल करना अत्यंत महत्वपूर्ण है। इस ट्यूटोरियल में आप **psd को png में कैसे बदलें** और एक ही वर्कफ़्लो में इमेज को क्रॉप करना सीखेंगे, यह सब शक्तिशाली Aspose.PSD for Java लाइब्रेरी का उपयोग करके। इस चरण‑दर‑चरण गाइड के अंत तक, आप अपने PNG निर्यात में सटीक क्रॉपिंग जोड़ पाएँगे और अपने Java एप्लिकेशन को PSD एसेट्स को आत्मविश्वास के साथ संभालने में सक्षम बनाएँगे।

## Quick Answers
- **What does the code do?** एक PSD लोड करता है, एक आयत को क्रॉप करता है, और उसे PNG के रूप में सहेजता है।  
- **Which library is required?** Aspose.PSD for Java (नवीनतम संस्करण)।  
- **Do I need a license?** हाँ, प्रोडक्शन उपयोग के लिए एक कमर्शियल लाइसेंस आवश्यक है।  
- **Can I define any crop region?** बिल्कुल – आप आवश्यक X, Y, चौड़ाई और ऊँचाई सेट कर सकते हैं।  
- **Is this approach fast for large files?** हाँ, Aspose.PSD उच्च‑प्रदर्शन प्रोसेसिंग के लिए अनुकूलित है।

## What is convert psd to png?
PSD को PNG में बदलना का मतलब है एक लेयर्ड Photoshop डॉक्यूमेंट को फ्लैटन करके एक लॉसलेस PNG इमेज में परिवर्तित करना। यह फ़ॉर्मेट वेब डिलीवरी, थंबनेल या किसी भी स्थिति के लिए आदर्श है जहाँ आपको मूल लेयर्स के बिना एक रास्टर इमेज चाहिए।

## Why crop PSD before converting to PNG?
क्रॉपिंग आपको डिज़ाइन के केवल आवश्यक भाग को निकालने की अनुमति देती है, जिससे फ़ाइल आकार घटता है और प्रासंगिक विज़ुअल कंटेंट पर ध्यान केंद्रित होता है। यह थंबनेल, UI एसेट्स बनाने या रिस्पॉन्सिव लेआउट्स के लिए इमेज तैयार करने में विशेष रूप से उपयोगी है।

## Prerequisites
ट्यूटोरियल शुरू करने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित प्री‑रिक्विज़िट्स मौजूद हैं:
- Java प्रोग्रामिंग का बेसिक ज्ञान।  
- आपके सिस्टम पर Java Development Kit (JDK) स्थापित हो।  
- Aspose.PSD for Java लाइब्रेरी डाउनलोड करके अपने प्रोजेक्ट में जोड़ी गई हो।  
- प्रयोग के लिए एक सैंपल PSD फ़ाइल।

## Import Packages
अपने Java प्रोजेक्ट में Aspose.PSD कार्यक्षमताओं के लिए आवश्यक पैकेज इम्पोर्ट करना न भूलें:
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;
import com.aspose.psd.imageoptions.PngOptions;
```

## Step 1: Set Up Your Project
एक Java प्रोजेक्ट बनाकर उसमें Aspose.PSD for Java लाइब्रेरी को प्रोजेक्ट के क्लासपाथ में जोड़ें। इससे आपको सभी इमेज‑प्रोसेसिंग क्लासेज़ तक पहुँच मिलेगी जो आपको आवश्यक होंगी।

## Step 2: Load PSD Image
```java
String dataDir = "Your Document Directory";
String srcPath = dataDir + "sample.psd";
// Load an existing PSD image
RasterImage image = (RasterImage)Image.load(srcPath);
```
*यहाँ हम स्रोत PSD फ़ाइल को एक `RasterImage` ऑब्जेक्ट में लोड करते हैं, जो क्रॉपिंग जैसी रास्टर‑आधारित ऑपरेशन्स प्रदान करता है।*

## Step 3: Define Crop Region
```java
// Create an instance of Rectangle class by passing x, y, width, and height
Rectangle cropRegion = new Rectangle(0, 0, 350, 450);
```
*`Rectangle` वह क्षेत्र परिभाषित करता है जिसे आप रखना चाहते हैं। अपने डिज़ाइन के अनुसार `x`, `y`, `width`, और `height` मानों को समायोजित करें। यह चरण सीधे “define crop region” कीवर्ड का उत्तर देता है।*

## Step 4: Crop PSD Image
```java
// Call the crop method of Image class and pass the Rectangle instance
image.crop(cropRegion);
```
*`crop` को कॉल करने से इमेज मेमोरी में संशोधित होती है, और निर्दिष्ट आयत के बाहर की सभी सामग्री हट जाती है।*

## Step 5: Set PNG Export Options
```java
// Create an instance of PngOptions class
PngOptions pngOptions = new PngOptions();
```
*`PngOptions` आपको PNG‑विशिष्ट सेटिंग्स जैसे कम्प्रेशन लेवल, कलर टाइप, आदि को नियंत्रित करने की सुविधा देता है।*

## Step 6: Save Cropped Image as PNG
```java
// Provide output path and PngOptions to convert the PSD file to PNG and save the output
String destName = dataDir + "export.png";
image.save(destName, pngOptions);
```
*`save` मेथड **psd को png में बदलने** की प्रक्रिया को निष्पादित करता है, जबकि आपने जो क्रॉप परिभाषित किया है उसे संरक्षित रखता है।*

## Common Pitfalls & Tips
- **Incorrect rectangle dimensions:** सुनिश्चित करें कि चौड़ाई और ऊँचाई मूल इमेज के आकार से अधिक न हों, अन्यथा एक एक्सेप्शन फेंका जाएगा।  
- **Memory usage with large PSDs:** सहेजने के बाद `RasterImage` ऑब्जेक्ट (`image.dispose()`) को डिस्पोज़ कर दें ताकि नेटिव रिसोर्सेज़ मुक्त हो सकें।  
- **License not set:** यदि आप कोड को वैध लाइसेंस के बिना चलाते हैं, तो आउटपुट PNG पर वॉटरमार्क दिखाई देगा।

## Frequently Asked Questions
### Can I crop PSD files with irregular shapes using Aspose.PSD for Java?
हाँ, Aspose.PSD for Java आपको एक कस्टम क्रॉप रीजन परिभाषित करने की अनुमति देता है, जिससे आप इमेज को विभिन्न आकारों में क्रॉप कर सकते हैं।

### Is Aspose.PSD for Java suitable for large‑scale image processing tasks?
बिल्कुल! Aspose.PSD बड़े इमेज को कुशलता से संभालने के लिए डिज़ाइन किया गया है, जिससे यह व्यापक इमेज प्रोसेसिंग आवश्यकताओं वाले प्रोजेक्ट्स के लिए आदर्श बनता है।

### Do I need a license for Aspose.PSD for Java?
हाँ, कमर्शियल उपयोग के लिए एक वैध लाइसेंस आवश्यक है। आप इसे [Aspose Purchase](https://purchase.aspose.com/buy) से प्राप्त कर सकते हैं।

### How can I seek help or report issues with Aspose.PSD for Java?
सहायता के लिए [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) पर जाएँ, अपने अनुभव साझा करें और किसी भी समस्या की रिपोर्ट करें।

### Can I try Aspose.PSD for Java before purchasing?
निश्चित रूप से! लाइब्रेरी की सुविधाओं को मुफ्त ट्रायल के साथ आज़माएँ, जो [here](https://releases.aspose.com/) उपलब्ध है।

---

**Last Updated:** 2026-03-21  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}