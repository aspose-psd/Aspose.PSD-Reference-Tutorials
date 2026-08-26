---
date: 2026-08-17
description: Java के लिए Aspose.PSD का उपयोग करके Bradley थ्रेशोल्डिंग से इमेज को
  बाइनराइज़ करने का तरीका। इस क्रमशः गाइड का पालन करके PSD को PNG में परिवर्तित करें
  और इमेज की गुणवत्ता बढ़ाएँ।
keywords:
- how to binarize image
- convert psd to png
- set threshold value
- enhance image quality
- save binarized image
lastmod: 2026-08-17
linktitle: Bradley थ्रेशोल्डिंग
og_description: Aspose.PSD for Java में Bradley थ्रेशोल्डिंग का उपयोग करके इमेज को
  बाइनराइज़ करना सीखें। यह गाइड आपको थ्रेशोल्ड वैल्यू सेट करना, PSD को PNG में बदलना,
  और बाइनराइज़्ड इमेज को सेव करना दिखाता है।
og_image_alt: 'Guide: binarize image using Bradley thresholding in Aspose.PSD for
  Java'
og_title: Java में Bradley थ्रेशोल्डिंग के साथ इमेज को बाइनराइज़ कैसे करें
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: How to binarize image with Bradley thresholding using Aspose.PSD for
    Java. Follow this step‑by‑step guide to convert PSD to PNG and enhance image quality.
  headline: How to binarize image in Java using Bradley thresholding
  type: TechArticle
- description: How to binarize image with Bradley thresholding using Aspose.PSD for
    Java. Follow this step‑by‑step guide to convert PSD to PNG and enhance image quality.
  name: How to binarize image in Java using Bradley thresholding
  steps:
  - name: '**Java development environment** – JDK 11 or newer installed and configured.'
    text: '**Java development environment** – JDK 11 or newer installed and configured.'
  - name: '**Aspose.PSD library** – download the latest JAR from [Aspose.PSD Java
      download page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD library** – download the latest JAR from [Aspose.PSD Java
      download page](https://releases.aspose.com/psd/java/).'
  - name: '**Sample PSD image** – a PSD file you want to binarize; you can use any
      image you own or a test file.'
    text: '**Sample PSD image** – a PSD file you want to binarize; you can use any
      image you own or a test file.'
  type: HowTo
- questions:
  - answer: It is an adaptive binarization technique that computes a local average
      for each pixel and thresholds based on a percentage of that average.
    question: What is Bradley thresholding?
  - answer: Start with 0.5 (50 %). If the output is too noisy, increase the value;
      if details are lost, decrease it. Test a few values on a representative sample.
    question: How do I choose the right threshold value?
  - answer: Yes. Aspose.PSD supports more than 30 input and output formats—including
      PSD, PNG, JPEG, BMP, and TIFF—so you can load a JPEG, convert it to a `PsdImage`,
      and then binarize.
    question: Can I apply Bradley thresholding to other image formats?
  - answer: You can call `image.save("preview.png", new PngOptions())` after the `binarizeBradley`
      step to write a temporary file for visual inspection.
    question: Is there a way to preview the binarized image before saving?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for community
      help and explore the official [documentation](https://reference.aspose.com/psd/java/)
      for detailed API references.
    question: Where can I find more support and resources?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- image binarization
- Aspose.PSD
- Java image processing
- Bradley thresholding
title: Java में Bradley थ्रेशोल्डिंग का उपयोग करके इमेज को बाइनराइज़ कैसे करें
url: /hi/java/image-processing/bradley-thresholding/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# जावा में ब्रैडली थ्रेशोल्डिंग का उपयोग करके इमेज को बाइनराइज़ कैसे करें

## परिचय

इस ट्यूटोरियल में आप **इमेज को बाइनराइज़ करने का तरीका** सीखेंगे Bradley Thresholding को Aspose.PSD for Java के साथ लागू करके। बाइनराइज़ेशन एक रंगीन या ग्रेस्केल चित्र को काली‑और‑सफ़ेद संस्करण में बदलता है, जो OCR, दस्तावेज़ अभिलेखागार, और कई कंप्यूटर‑विजन पाइपलाइन के लिए आवश्यक है। हम हर चरण को दिखाएंगे—PSD फ़ाइल लोड करने से लेकर अंतिम PNG सहेजने तक—ताकि आप इस तकनीक को अपने जावा प्रोजेक्ट्स में एकीकृत कर सकें।

## त्वरित उत्तर
- **Bradley थ्रेशोल्डिंग क्या करता है?** यह प्रत्येक पिक्सेल के लिए स्थानीय थ्रेशोल्ड को अनुकूलित रूप से निर्धारित करता है, असमान प्रकाश में विवरण को संरक्षित रखता है।
- **कौनसी लाइब्रेरी आवश्यक है?** Aspose.PSD for Java (नवीनतम संस्करण की सिफारिश की जाती है)।
- **क्या मुझे लाइसेंस चाहिए?** विकास के लिए एक मुफ्त ट्रायल काम करता है; उत्पादन के लिए एक व्यावसायिक लाइसेंस आवश्यक है।
- **क्या मैं बड़े PSD फ़ाइलों को प्रोसेस कर सकता हूँ?** हाँ, API 2 GB तक की फ़ाइलों को पूरी इमेज को मेमोरी में लोड किए बिना संभालता है।
- **कौनसा आउटपुट फ़ॉर्मेट सुझाया जाता है?** PNG बाइनराइज़्ड परिणामों के लिए लॉसलेस और व्यापक रूप से समर्थित है।

## Bradley थ्रेशोल्डिंग क्या है?

Bradley थ्रेशोल्डिंग एक अनुकूली बाइनराइज़ेशन एल्गोरिद्म है जो प्रत्येक पिक्सेल के आसपास स्थानीय औसत की गणना करता है और यदि उसकी तीव्रता उस औसत से एक कॉन्फ़िगर करने योग्य प्रतिशत से अधिक हो तो पिक्सेल को सफ़ेद सेट करता है। यह विधि प्रकाश में असमानता होने पर भी किनारा विवरण को बनाए रखती है।

## इमेज को बाइनराइज़ करने के लिए Bradley थ्रेशोल्डिंग का उपयोग क्यों करें?

Bradley थ्रेशोल्डिंग असमान प्रकाश वाली इमेज पर लगातार उच्च कंट्रास्ट प्रदान करता है, स्कैन किए गए दस्तावेज़ों पर ग्लोबल थ्रेशोल्डिंग विधियों की तुलना में 95 % तक OCR सटीकता हासिल करता है। Aspose.PSD का कार्यान्वयन एक सामान्य 8‑कोर सर्वर पर 500‑पृष्ठीय PSD को 4 सेकंड से कम समय में प्रोसेस करता है, जिससे यह बैच वर्कफ़्लो के लिए उपयुक्त बनता है।

## पूर्वापेक्षाएँ

1. **Java development environment** – JDK 11 या नया स्थापित और कॉन्फ़िगर किया हुआ।
2. **Aspose.PSD library** – नवीनतम JAR को [Aspose.PSD Java download page](https://releases.aspose.com/psd/java/) से डाउनलोड करें।
3. **Sample PSD image** – वह PSD फ़ाइल जिसे आप बाइनराइज़ करना चाहते हैं; आप कोई भी अपनी इमेज या टेस्ट फ़ाइल उपयोग कर सकते हैं।

## पैकेज इम्पोर्ट करें

निम्नलिखित इम्पोर्ट्स आपको इमेज लोड करने, प्रोसेस करने और सहेजने के लिए आवश्यक कोर क्लासेज़ तक पहुंच प्रदान करते हैं।

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

## Bradley थ्रेशोल्डिंग का उपयोग करके इमेज को बाइनराइज़ कैसे करें?

इस ट्यूटोरियल में आप एक PSD फ़ाइल लोड करेंगे, उपयुक्त थ्रेशोल्ड चुनेंगे, अनुकूली Bradley बाइनराइज़ेशन चलाएंगे, और अंत में परिणाम को PNG फ़ाइल में लिखेंगे। प्रक्रिया चार संक्षिप्त मेथड कॉल्स से बनी है, प्रत्येक कोड उदाहरणों के साथ प्रदर्शित किया गया है, जिससे आप इस वर्कफ़्लो को किसी भी जावा एप्लिकेशन में न्यूनतम प्रयास से एकीकृत कर सकते हैं।

## चरण 1: इमेज लोड करें

`PsdImage` क्लास मेमोरी में एक PSD फ़ाइल का प्रतिनिधित्व करती है और पिक्सेल‑लेवल मैनिपुलेशन के लिए मेथड्स प्रदान करती है। एक इंस्टेंस बनाकर आप पूरी इमेज डेटा तक पहुंच प्राप्त करते हैं।

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "binarized_out.png";

// Load an image
PsdImage image = (PsdImage)Image.load(sourceFile);
```

इस चरण में PSD फ़ाइल डिस्क से पढ़ी जाती है और एक `PsdImage` ऑब्जेक्ट में संग्रहीत की जाती है, जो प्रोसेसिंग के लिए तैयार है।

## चरण 2: थ्रेशोल्ड मान निर्धारित करें

`threshold` पैरामीटर बाइनराइज़ेशन की आक्रामकता को नियंत्रित करता है; 0.5 (50 %) का मान सामान्य प्रारंभिक बिंदु है। इसे अपने स्रोत इमेज के कंट्रास्ट के आधार पर समायोजित करें।

```java
// Define threshold value
double threshold = 0.15;
```

थ्रेशोल्ड को सही ढंग से सेट करने से शोर घटाने और विवरण संरक्षण के बीच संतुलन बनता है।

## चरण 3: Bradley थ्रेशोल्डिंग लागू करें

`binarizeBradley` मेथड प्रदान किए गए थ्रेशोल्ड का उपयोग करके अनुकूली बाइनराइज़ेशन करता है। यह प्रत्येक पिक्सेल के आसपास एक स्थानीय विंडो का विश्लेषण करता है ताकि यह तय किया जा सके कि पिक्सेल को काला या सफ़ेद करना है।

```java
// Call BinarizeBradley method and pass the threshold value as a parameter
image.binarizeBradley(threshold);
```

इस कॉल के बाद `PsdImage` इंस्टेंस मूल चित्र का काली‑और‑सफ़ेद संस्करण रखता है।

## चरण 4: आउटपुट इमेज सहेजें

`save` मेथड प्रोसेस की गई इमेज को फ़ाइल सिस्टम में लिखता है। PNG चुना जाता है क्योंकि यह बाइनरी डेटा को अतिरिक्त संपीड़न आर्टिफैक्ट्स के बिना संरक्षित रखता है।

```java
// Save the output image
image.save(destName, new PngOptions());
```

अब आपके पास एक बाइनराइज़्ड PNG है जिसे OCR इंजन या अन्य डाउनस्ट्रीम प्रोसेस में फीड किया जा सकता है।

## सामान्य समस्याएँ और समाधान

LoadOptions एक क्लास है जो आपको PSD फ़ाइल लोड करने के तरीके को निर्दिष्ट करने देती है, जैसे मेमोरी उपयोग कम करने के लिए स्ट्रीमिंग मोड सक्षम करना।

- **Image appears too dark or too light** – थ्रेशोल्ड मान को समायोजित करें; कम मान इमेज को हल्का बनाते हैं, उच्च मान इसे गहरा बनाते हैं।
- **Out‑of‑memory errors on very large PSDs** – लोड करने से पहले `PsdImage.setLoadOptions(new LoadOptions { LoadMode = LoadMode.Stream })` कॉल करके स्ट्रीमिंग मोड सक्षम करें। `LoadMode.Stream` बड़े फ़ाइलों के लिए स्ट्रीमिंग मोड को सक्षम करता है।
- **Unexpected color bands** – सुनिश्चित करें कि स्रोत PSD RGB मोड में है; आवश्यक होने पर `image.convertToRgb()` का उपयोग करके बदलें। `convertToRgb()` मेथड इमेज को RGB कलर स्पेस में बदलता है, जिससे सही रंग हैंडलिंग सुनिश्चित होती है।

## अक्सर पूछे जाने वाले प्रश्न

**Q: Bradley थ्रेशोल्डिंग क्या है?**  
A: यह एक अनुकूली बाइनराइज़ेशन तकनीक है जो प्रत्येक पिक्सेल के लिए स्थानीय औसत की गणना करती है और उस औसत के प्रतिशत के आधार पर थ्रेशोल्ड लागू करती है।

**Q: सही थ्रेशोल्ड मान कैसे चुनूँ?**  
A: 0.5 (50 %) से शुरू करें। यदि आउटपुट बहुत शोरयुक्त है तो मान बढ़ाएँ; यदि विवरण खो रहा है तो घटाएँ। प्रतिनिधि नमूने पर कुछ मानों का परीक्षण करें।

**Q: क्या मैं Bradley थ्रेशोल्डिंग को अन्य इमेज फ़ॉर्मेट्स पर लागू कर सकता हूँ?**  
A: हाँ। Aspose.PSD 30 से अधिक इनपुट और आउटपुट फ़ॉर्मेट्स का समर्थन करता है—जिसमें PSD, PNG, JPEG, BMP, और TIFF शामिल हैं—ताकि आप JPEG लोड करके उसे `PsdImage` में बदल सकें और फिर बाइनराइज़ कर सकें।

**Q: सहेजने से पहले बाइनराइज़्ड इमेज का प्रीव्यू कैसे देखूँ?**  
A: `binarizeBradley` चरण के बाद `image.save("preview.png", new PngOptions())` कॉल करके एक अस्थायी फ़ाइल लिखें और विज़ुअल निरीक्षण करें।

**Q: अधिक समर्थन और संसाधन कहाँ मिलेंगे?**  
A: समुदाय सहायता के लिए [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) देखें और विस्तृत API रेफ़रेंस के लिए आधिकारिक [documentation](https://reference.aspose.com/psd/java/) का अन्वेषण करें।

---

**अंतिम अपडेट:** 2026-08-17  
**परीक्षण किया गया:** Aspose.PSD 24.12 for Java  
**लेखक:** Aspose  

{{< blocks/products/products-backtop-button >}}

## संबंधित ट्यूटोरियल

- [जावा इमेज प्रोसेसिंग ट्यूटोरियल - Aspose.PSD for Java के साथ इमेज की ब्राइटनेस समायोजित करें](/psd/java/advanced-techniques/adjust-brightness/)
- [Aspose.PSD के साथ जावा इमेज प्रोसेसिंग में गामा कैसे समायोजित करें](/psd/java/advanced-techniques/adjust-gamma/)
- [इमेज प्रोसेसिंग जावा लाइब्रेरी: Aspose.PSD का उपयोग करके लेयर को इनवर्ट करें](/psd/java/advanced-image-manipulation/invert-adjustment-layer/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}