---
date: 2026-08-01
description: Aspose.PSD के साथ Java image processing में gamma को कैसे समायोजित करें,
  PSD को TIFF में बदलें, और संक्षिप्त ट्यूटोरियल में फीके हुए चित्रों को ठीक करें।
keywords:
- how to adjust gamma
- fix washed out image
- java image processing
- convert psd to tiff
- server side image processing
lastmod: 2026-08-01
linktitle: एक छवि का Gamma समायोजित करें
og_description: Aspose.PSD का उपयोग करके Java image processing में gamma को कैसे समायोजित
  करें – एक तेज़, server‑side लाइब्रेरी जो फीके हुए चित्रों को ठीक करती है और कुछ
  ही कोड लाइनों में PSD को TIFF में बदल देती है।
og_image_alt: 'Guide: Adjust gamma in Java images with Aspose.PSD, convert PSD to
  TIFF'
og_title: Gamma कैसे समायोजित करें – Java processing with Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  headline: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  type: TechArticle
- description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  name: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  steps:
  - name: '**Java Development Environment** – Java 8 or later installed.'
    text: '**Java Development Environment** – Java 8 or later installed.'
  - name: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
  - name: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
    text: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
  type: HowTo
- questions:
  - answer: Yes – the `adjustGamma` method accepts separate float values for red,
      green, and blue channels.
    question: Can I apply different gamma values to each colour channel?
  - answer: Absolutely. You can perform resizing, cropping, or colour corrections
      sequentially on the same `RasterImage` instance.
    question: Is it possible to chain multiple image adjustments before saving?
  - answer: Yes, each layer can be accessed and processed individually.
    question: Does Aspose.PSD support multi‑page PSD files?
  - answer: Aspose.PSD supports PNG, JPEG, BMP, and many other formats via their respective
      options classes.
    question: What format can I export to besides TIFF?
  - answer: Start with a moderate gamma (around 2.0) and preview the result; adjust
      downwards if the image looks too bright.
    question: How do I avoid a washed‑out image after gamma correction?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- adjust gamma
- Aspose.PSD
- Java image processing
- PSD to TIFF
- server side processing
title: Aspose.PSD के साथ Java Image Processing में Gamma कैसे समायोजित करें
url: /hi/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD के साथ जावा इमेज प्रोसेसिंग में गामा कैसे समायोजित करें

## परिचय

यदि आप **java image processing** पर काम कर रहे हैं, तो **how to adjust gamma** सीखना एक मूलभूत तकनीक है जो विवरण खोए बिना चमक और कंट्रास्ट को सुधारती है। इस ट्यूटोरियल में हम देखेंगे कि **Aspose.PSD for Java** का उपयोग करके PSD फ़ाइल पर गामा करेक्शन कैसे लागू किया जाए, **convert PSD to TIFF**, और **washed‑out image** से बचा जाए। आप देखेंगे कि यह तरीका तेज़, विश्वसनीय और **server‑side image processing** पाइपलाइनों के लिए उपयुक्त क्यों है।

## त्वरित उत्तर
- **What does gamma correction do?** यह ल्यूमिनेंस मानों को पुनः मैप करता है ताकि अंधेरे क्षेत्रों को उज्ज्वल किया जा सके या उज्ज्वल क्षेत्रों को गहरा किया जा सके, जबकि कुल मिलाकर विवरण संरक्षित रहता है।  
- **Which library handles the processing?** Aspose.PSD for Java रास्टर इमेजेज़ के लिए एक समर्पित `adjustGamma` मेथड प्रदान करता है।  
- **Can I convert PSD to TIFF in the same flow?** हाँ – गामा समायोजन के बाद आप इमेज को सीधे `TiffOptions` का उपयोग करके TIFF में सहेज सकते हैं।  
- **Do I need a license for development?** परीक्षण के लिए एक फ्री ट्रायल काम करता है; उत्पादन उपयोग के लिए एक वाणिज्यिक लाइसेंस आवश्यक है।  
- **What Java version is supported?** Aspose.PSD Java 8 और बाद के संस्करणों को समर्थन देता है।

## जावा गामा करेक्शन क्या है?

Gamma correction एन्कोडेड पिक्सेल मानों और प्रदर्शित चमक के बीच के गैर-रेखीय संबंध को बदलता है। गामा कर्व को समायोजित करके आप **fix washed out image** समस्याओं को हल कर सकते हैं या शैडोज़ में विवरण को बढ़ा सकते हैं बिना हाइलाइट्स को अधिक उज्ज्वल किए। यह प्रत्येक पिक्सेल पर पावर‑लॉ फ़ंक्शन लागू करके काम करता है, जो अंधेरे टोन को उज्ज्वल करता है और हाइलाइट्स को संपीड़ित करता है, जिससे अधिक प्राकृतिक दृश्य रूप मिलता है।

## गामा करेक्शन के लिए Aspose.PSD का उपयोग क्यों करें?

Aspose.PSD एक **java image processing library** है जो PSD फ़ॉर्मेट की जटिलताओं को सरल बनाता है। यह 2 GB तक की फ़ाइलों को प्रोसेस कर सकता है, 50 से अधिक विभिन्न इमेज फ़ॉर्मेट को संभालता है, और एक सरल `adjustGamma` कॉल प्रदान करता है, जिससे यह **java gamma correction** और **convert PSD to TIFF** वर्कफ़्लो के लिए आदर्श बनता है।

## आवश्यकताएँ

1. **Java Development Environment** – Java 8 या बाद का संस्करण स्थापित हो।  
2. **Aspose.PSD Library** – JAR को डाउनलोड करके अपने प्रोजेक्ट में जोड़ें। आधिकारिक [दस्तावेज़ीकरण](https://reference.aspose.com/psd/java/) देखें।  
3. **Sample Image** – वह PSD फ़ाइल जिसे आप प्रोसेस करना चाहते हैं (उदाहरण के लिए `sample.psd`)।

## पैकेज इम्पोर्ट करें

शुरू करने से पहले, आवश्यक नेमस्पेसेज़ इम्पोर्ट करें जो आपको रास्टर हैंडलिंग और फ़ाइल‑फ़ॉर्मेट विकल्पों तक पहुँच प्रदान करते हैं।

## चरण 1: इमेज लोड करें

`RasterImage` क्लास PSD लेयर के रास्टराइज़्ड पिक्सेल डेटा को मेमोरी में दर्शाती है। इमेज को एक बार लोड करके और कैश करके आप बाद के समायोजनों के लिए मेमोरी चर्न को कम कर सकते हैं।

## चरण 2: गामा समायोजित करें

`new RasterImage("sample.psd")` से अपना PSD लोड करें और `rasterImage.adjustGamma(2.0f)` कॉल करें — यह एक ही लाइन सभी कलर चैनलों पर 2.0 का गामा लागू करती है, जिससे शैडोज़ उज्ज्वल होते हैं जबकि हाइलाइट्स अपरिवर्तित रहते हैं। यदि चैनल‑विशिष्ट समायोजन आवश्यक हो तो आप रेड, ग्रीन और ब्लू के लिए अलग मान भी पास कर सकते हैं।

## चरण 3: TiffOptions बनाएं

`TiffOptions` आपको कंप्रेशन, बिट्स पर सैंपल, और अन्य TIFF‑विशिष्ट सेटिंग्स को नियंत्रित करने देता है। 8‑बिट सैंपल (`{8,8,8}`) सेट करने से TIFF फ़ाइल का आकार उचित रहता है जबकि रंग की सटीकता बनी रहती है।

## चरण 4: परिणामी इमेज सहेजें

`rasterImage.save("output.tif", tiffOptions)` कॉल करके प्रोसेस्ड इमेज को डिस्क पर लिखें। सहेजने के बाद, आप TIFF को प्रिंट सर्विसेज़ या वेब API जैसे डाउनस्ट्रीम सिस्टम में फीड कर सकते हैं।

## सामान्य उपयोग केस

- **Automated graphics pipelines** – थंबनेल जनरेट करने से पहले गामा को रीयल‑टाइम में समायोजित करें।  
- **Batch conversion tools** – बड़े PSD आर्काइव्स को TIFF में बदलें जबकि ब्राइटनेस को सामान्यीकृत करें।  
- **Web services** – एक एन्डपॉइंट एक्सपोज़ करें जो PSD प्राप्त करता है, गामा करेक्शन लागू करता है, और क्लाइंट उपयोग के लिए TIFF लौटाता है।

## सामान्य समस्याएँ और समाधान

| समस्या | कारण | समाधान |
|-------|----------------|------------|
| **Image appears washed out** | गामा मान बहुत अधिक (उदा., > 2.5) | गामा फ़ैक्टर को 1.8 और 2.2 के बीच के मान तक कम करें। |
| **`rasterImage.isCached()` returns false** | इमेज अभी मेमोरी में लोड नहीं हुई है | गामा समायोजित करने से पहले `rasterImage.cacheData()` कॉल करें। |
| **TIFF file size is large** | बिट्स पर सैंपल 16‑बिट सेट है | उदाहरण में दिखाए अनुसार 8‑बिट सैंपल (`{8,8,8}`) उपयोग करें। |

## अक्सर पूछे जाने वाले प्रश्न

**Q: Can I apply different gamma values to each colour channel?**  
A: हाँ – `adjustGamma` मेथड रेड, ग्रीन और ब्लू चैनलों के लिए अलग-अलग फ़्लोट मान स्वीकार करता है।

**Q: Is it possible to chain multiple image adjustments before saving?**  
A: बिल्कुल। आप उसी `RasterImage` इंस्टेंस पर क्रमिक रूप से रिसाइज़िंग, क्रॉपिंग, या कलर करेक्शन कर सकते हैं।

**Q: Does Aspose.PSD support multi‑page PSD files?**  
A: हाँ, प्रत्येक लेयर को अलग‑अलग एक्सेस और प्रोसेस किया जा सकता है।

**Q: What format can I export to besides TIFF?**  
A: Aspose.PSD PNG, JPEG, BMP, और कई अन्य फ़ॉर्मेट को उनके संबंधित ऑप्शन क्लासेज़ के माध्यम से सपोर्ट करता है।

**Q: How do I avoid a washed‑out image after gamma correction?**  
A: गामा करेक्शन के बाद एक washed‑out इमेज से बचने के लिए, मध्यम गामा (लगभग 2.0) से शुरू करें और परिणाम का प्रीव्यू लें; यदि इमेज बहुत उज्ज्वल दिखे तो गामा को नीचे की ओर समायोजित करें।

## निष्कर्ष

बधाई हो! आपने **how to adjust gamma** को **java image processing** वर्कफ़्लो में सफलतापूर्वक सीख लिया है, एक PSD को TIFF में बदल दिया है, और **washed‑out image** जैसी सामान्य समस्याओं से बचा है। यह पैटर्न आपको ब्राइटनेस और कंट्रास्ट पर सूक्ष्म नियंत्रण देता है, जिससे यह ऑटोमेटेड ग्राफ़िक्स पाइपलाइन, वेब सर्विसेज़, या डेस्कटॉप यूटिलिटीज़ के लिए आदर्श बनता है।

---

**अंतिम अपडेट:** 2026-08-01  
**परीक्षित संस्करण:** Aspose.PSD 24.11 for Java  
**लेखक:** Aspose  

{{< blocks/products/products-backtop-button >}}

## संबंधित ट्यूटोरियल्स

- [जावा इमेज प्रोसेसिंग ट्यूटोरियल - Aspose.PSD for Java के साथ इमेज की ब्राइटनेस समायोजित करें](/psd/java/advanced-techniques/adjust-brightness/)
- [कैसे PSD को TIFF में बदलें और Aspose.PSD for Java के साथ कंट्रास्ट समायोजित करें](/psd/java/advanced-techniques/adjust-contrast/)
- [जावा में PSD को इमेज में बदलें – Aspose.PSD के साथ एडजस्टमेंट लेयर्स लागू करें](/psd/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);

// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```