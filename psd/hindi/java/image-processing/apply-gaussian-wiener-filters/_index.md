---
date: 2026-07-17
description: Aspose.PSD का उपयोग करके Java इमेज प्रोसेसिंग ट्यूटोरियल, जिसमें Gaussian
  और Wiener फ़िल्टर को चरण‑दर‑चरण लागू करके शानदार दृश्य परिणाम प्राप्त किए जा सकते
  हैं।
keywords:
- java image processing tutorial
- export png java
- gaussian filter java
- wiener filter java
lastmod: 2026-07-17
linktitle: Gaussian और Wiener फ़िल्टर लागू करें
og_description: Java इमेज प्रोसेसिंग ट्यूटोरियल में Aspose.PSD for Java के साथ Gaussian
  और Wiener फ़िल्टर लागू करने का प्रदर्शन किया गया है, जिसमें PNG और अन्य फ़ॉर्मैट
  में निर्यात शामिल है।
og_image_alt: 'Developer guide: Apply Gaussian and Wiener filters to images in Java
  using Aspose.PSD'
og_title: Java इमेज प्रोसेसिंग ट्यूटोरियल – Gaussian और Wiener फ़िल्टर लागू करें
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Java image processing tutorial using Aspose.PSD learn how to apply
    Gaussian and Wiener filters step‑by‑step for stunning visual results.
  headline: Java Image Processing Tutorial – Apply Gaussian & Wiener Filters
  type: TechArticle
- questions:
  - answer: It smooths an image by averaging neighboring pixels, reducing high‑frequency
      noise.
    question: What does the Gaussian filter do?
  - answer: It performs adaptive smoothing, preserving edges while diminishing noise.
    question: What is the Wiener filter?
  - answer: Aspose.PSD for Java provides built‑in support for both filters.
    question: Which library is used?
  - answer: A trial works for testing, but a commercial license is required for production.
    question: Do I need a license?
  - answer: Yes—Aspose.PSD supports PNG, JPEG, BMP, and many more.
    question: Can I output formats other than GIF?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- Aspose.PSD
- gaussian filter
- wiener filter
- export png java
title: Java इमेज प्रोसेसिंग ट्यूटोरियल – Gaussian और Wiener फ़िल्टर लागू करें
url: /hi/java/image-processing/apply-gaussian-wiener-filters/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java इमेज प्रोसेसिंग ट्यूटोरियल – Gaussian और Wiener फ़िल्टर लागू करें Aspose.PSD

## परिचय

हमारे **java इमेज प्रोसेसिंग ट्यूटोरियल** में आपका स्वागत है जो दिखाता है कि Aspose.PSD for Java का उपयोग करके Gaussian और Wiener फ़िल्टर कैसे लागू करें। चाहे आप शोरयुक्त फ़ोटो को साफ़ कर रहे हों या वेब डिलीवरी के लिए ग्राफ़िक्स तैयार कर रहे हों, ये फ़िल्टर आपको स्मूद, प्रोफ़ेशनल‑लुकिंग परिणाम देते हैं। अगले कुछ मिनटों में आप पूरी वर्कफ़्लो देखेंगे—एक PSD फ़ाइल लोड करने से लेकर फ़िल्टर किया हुआ आउटपुट GIF के रूप में सहेजने तक।

## त्वरित उत्तर

- **Gaussian फ़िल्टर क्या करता है?** यह छवि को पड़ोसी पिक्सेल का औसत लेकर स्मूद करता है, जिससे हाई‑फ़्रीक्वेंसी शोर कम होता है।  
- **Wiener फ़िल्टर क्या है?** यह अनुकूली स्मूदिंग करता है, किनारों को संरक्षित रखते हुए शोर को घटाता है।  
- **कौन सा लाइब्रेरी उपयोग किया जाता है?** Aspose.PSD for Java दोनों फ़िल्टरों के लिए बिल्ट‑इन सपोर्ट प्रदान करता है।  
- **क्या मुझे लाइसेंस की आवश्यकता है?** परीक्षण के लिए ट्रायल काम करता है, लेकिन प्रोडक्शन के लिए एक कमर्शियल लाइसेंस आवश्यक है।  
- **क्या मैं GIF के अलावा अन्य फ़ॉर्मेट आउटपुट कर सकता हूँ?** हाँ—Aspose.PSD PNG, JPEG, BMP, और कई अन्य को सपोर्ट करता है।

## Java इमेज प्रोसेसिंग ट्यूटोरियल क्या है?

एक Java इमेज प्रोसेसिंग ट्यूटोरियल डेवलपर्स को छवि लोड करने, फ़िल्टर या रिसाइज़ जैसे ट्रांसफ़ॉर्मेशन लागू करने, और अंत में इच्छित फ़ॉर्मेट में परिणाम सहेजने के आवश्यक चरणों से परिचित कराता है। स्पष्ट कोड उदाहरण और व्याख्याएँ प्रदान करके, यह आपको इमेज‑मैनीपुलेशन क्षमताओं को सीधे Java एप्लिकेशन में एकीकृत करने में मदद करता है, जिससे बाहरी टूल्स की आवश्यकता कम हो जाती है।

## Gaussian और Wiener फ़िल्टर क्यों उपयोग करें?

अपनी छवि लोड करें, संयुक्त Gaussian‑Wiener फ़िल्टर लागू करें, और आप दानेदारपन में नाटकीय कमी देखेंगे जबकि प्रमुख किनारे तेज़ रहेंगे—वेब के लिए ग्राफ़िक्स तैयार करने या अभिलेखीय स्कैन के लिए आदर्श। Gaussian भाग हाई‑फ़्रीक्वेंसी शोर को हटाता है, और Wiener भाग स्थानीय वैरिएंस के अनुसार अनुकूलित होता है, जहाँ सबसे ज़्यादा महत्व है वहाँ विवरण को संरक्षित करता है।

## पूर्वापेक्षाएँ

- Java विकास पर्यावरण (JDK 8 या नया)।  
- Aspose.PSD for Java लाइब्रेरी। आप इसे **[here](https://releases.aspose.com/psd/java/)** से डाउनलोड कर सकते हैं।  
- Java सिंटैक्स और ऑब्जेक्ट‑ओरिएंटेड अवधारणाओं की बुनियादी परिचितता।

## पैकेज आयात करें

इम्पोर्ट स्टेटमेंट्स Aspose.PSD क्लासेज़ को स्कोप में लाते हैं ताकि आप रास्टर इमेजेज़, फ़िल्टर विकल्पों, और आउटपुट फ़ॉर्मेट्स के साथ काम कर सकें।

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.GaussWienerFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

ये इम्पोर्ट्स आपको इमेज लोडिंग, रास्टर मैनिपुलेशन, फ़िल्टर विकल्पों, और आउटपुट फ़ॉर्मेट्स तक पहुँच प्रदान करते हैं।

## चरण 1: छवि लोड करें

`RasterImage` क्लास एक रास्टर‑आधारित इमेज का प्रतिनिधित्व करता है जिसे पिक्सेल‑दर‑पिक्सेल प्रोसेस किया जा सकता है।

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);
RasterImage rasterImage = (RasterImage)image;
```

## चरण 2: RasterImage जांचें

एक सुरक्षा जांच पुष्टि करती है कि लोड की गई फ़ाइल रास्टर‑आधारित है; अन्यथा रूटीन सुगमता से बाहर निकल जाता है।

```java
if (rasterImage == null) {
    return;
}
```

## चरण 3: फ़िल्टर विकल्प कॉन्फ़िगर करें

`GaussWienerFilterOptions` क्लास आपको एक ही ऑब्जेक्ट में Gaussian और Wiener दोनों पैरामीटर को फाइन‑ट्यून करने की अनुमति देती है।

```java
GaussWienerFilterOptions options = new GaussWienerFilterOptions(12, 3);
options.setGrayscale(true);
```

- पहला आर्ग्यूमेंट (`12`) Gaussian कर्नेल के लिए रेडियस साइज निर्धारित करता है।  
- दूसरा आर्ग्यूमेंट (`3`) Wiener एल्गोरिद्म द्वारा उपयोग किए जाने वाले स्मूद वैल्यू को सेट करता है।  
- `setGrayscale(true)` फ़िल्टर को ग्रेस्केल में काम करने के लिए बताता है, जो अक्सर शोर घटाने के लिए साफ़ परिणाम देता है।

## चरण 4: फ़िल्टर लागू करें और सहेजें

`filter` मेथड कॉन्फ़िगर किए गए Gaussian‑Wiener संयोजन को पूरी इमेज की सीमाओं पर लागू करता है। अंत में, हम `GifOptions` का उपयोग करके प्रोसेस्ड इमेज को GIF के रूप में सहेजते हैं। आप `GifOptions` को `PngOptions`, `JpegOptions` आदि से बदल सकते हैं, ताकि **PNG Java निर्यात** या अन्य फ़ॉर्मेट्स प्राप्त कर सकें।

```java
rasterImage.filter(image.getBounds(), options);
String destName = dataDir + "gauss_wiener_out.gif";
image.save(destName, new GifOptions());
```

## सामान्य समस्याएँ और टिप्स

- **Null RasterImage:** सुनिश्चित करें कि स्रोत फ़ाइल PSD या कोई अन्य रास्टर‑संगत फ़ॉर्मेट हो।  
- **Performance:** बड़े इमेजेज़ को प्रोसेस करने में अधिक समय लग सकता है; रेडियस कम करने या पहले स्केल‑डाउन कॉपी प्रोसेस करने पर विचार करें।  
- **Color vs. Grayscale:** यदि आपको रंग रखना है, तो `options.setGrayscale(false)` सेट करें।

## अक्सर पूछे जाने वाले प्रश्न

**Q1: क्या मैं इन फ़िल्टरों को PSD के अलावा अन्य फ़ॉर्मेट की इमेजेज़ पर लागू कर सकता हूँ?**  
A1: हाँ, Aspose.PSD for Java PSD के अलावा PNG, JPEG, BMP, और GIF जैसे विभिन्न इमेज फ़ॉर्मेट्स को सपोर्ट करता है।

**Q2: क्या Aspose.PSD for Java के ट्रायल संस्करण में कोई प्रतिबंध हैं?**  
A2: ट्रायल संस्करण आउटपुट साइज को सीमित करता है और वॉटरमार्क जोड़ता है। पूर्ण क्षमताओं को अनलॉक करने के लिए, एक वैध लाइसेंस प्राप्त करें।

**Q3: मैं Aspose.PSD for Java के लिए समर्थन कैसे प्राप्त कर सकता हूँ?**  
A3: समुदाय सहायता और आधिकारिक उत्तरों के लिए **[Aspose.PSD Forum](https://forum.aspose.com/c/psd/34)** पर जाएँ।

**Q4: क्या परीक्षण उद्देश्यों के लिए एक अस्थायी लाइसेंस उपलब्ध है?**  
A4: हाँ, आप अस्थायी लाइसेंस **[here](https://purchase.aspose.com/temporary-license/)** से प्राप्त कर सकते हैं।

**Q5: मैं Aspose.PSD for Java के विस्तृत दस्तावेज़ कहाँ पा सकता हूँ?**  
A5: विस्तृत API रेफ़रेंसेज़ और अतिरिक्त उदाहरणों के लिए **[documentation](https://reference.aspose.com/psd/java/)** देखें।

## निष्कर्ष

आपने अब एक पूर्ण **java इमेज प्रोसेसिंग ट्यूटोरियल** पूरा कर लिया है जो दिखाता है कि Aspose.PSD for Java का उपयोग करके **Gaussian** और Wiener फ़िल्टर कैसे लागू करें। विभिन्न रेडियस और स्मूद वैल्यू के साथ प्रयोग करें, ग्रेस्केल टॉगल करें, और PNG जैसे अन्य आउटपुट फ़ॉर्मेट्स आज़माएँ ताकि देखें कि फ़िल्टर आपके इमेजेज़ को कैसे प्रभावित करते हैं। कोडिंग का आनंद लें!

---

**अंतिम अपडेट:** 2026-07-17  
**परीक्षण किया गया:** Aspose.PSD for Java 23.12 (लेखन के समय नवीनतम)  
**लेखक:** Aspose

## संबंधित ट्यूटोरियल

- [स्टेप बाय स्टेप फ़िल्टर - Aspose.PSD for Java का उपयोग करके मोशन Wiener फ़िल्टर लागू करें](/psd/java/image-processing/apply-motion-wiener-filters/)
- [स्टेप बाय स्टेप फ़िल्टर - Median & Wiener फ़िल्टर लागू करें (Java)](/psd/java/image-processing/apply-median-wiener-filters/)
- [Aspose.PSD for Java में PNG फ़ाइलों को फ़िल्टर कैसे करें](/psd/java/optimizing-png-files/apply-filters-png-files/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}