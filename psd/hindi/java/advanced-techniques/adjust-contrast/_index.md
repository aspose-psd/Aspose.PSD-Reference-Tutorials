---
date: 2026-07-27
description: Aspose.PSD for Java, एक प्रमुख जावा इमेज मैनिपुलेशन लाइब्रेरी, का उपयोग
  करके PSD को TIFF में कैसे बदलें और इमेज कंट्रास्ट समायोजन कैसे करें, सीखें।
keywords:
- convert psd to tiff
- java image processing
- improve image contrast
lastmod: 2026-07-27
linktitle: PSD को TIFF में बदलें और कंट्रास्ट समायोजित करें
og_description: Aspose.PSD for Java का उपयोग करके कंट्रास्ट समायोजन के साथ PSD को
  TIFF में बदलें। यह गाइड स्टेप‑बाय‑स्टेप कोड, परफॉर्मेंस टिप्स, और हाई‑क्वालिटी TIFF
  आउटपुट के लिए एक्सपोर्ट विकल्प दिखाता है।
og_image_alt: 'Guide: Convert PSD to TIFF and adjust contrast using Aspose.PSD for
  Java'
og_title: PSD को TIFF में बदलें & कंट्रास्ट समायोजित करें – Aspose.PSD Java
schemas:
- author: Aspose
  dateModified: '2026-07-27'
  description: Learn how to convert PSD to TIFF and perform image contrast adjustment
    using Aspose.PSD for Java, a leading java image manipulation library.
  headline: Convert PSD to TIFF and Adjust Contrast with Aspose.PSD for Java
  type: TechArticle
- questions:
  - answer: It changes the difference between the darkest and brightest pixels, making
      details pop.
    question: What does “adjust contrast” mean?
  - answer: Aspose.PSD for Java – a full‑featured image processing toolkit.
    question: Which library handles this?
  - answer: A **temporary Aspose license** works for testing; a full license is required
      for production.
    question: Do I need a license?
  - answer: Absolutely – we’ll use `TiffOptions` to export the processed image.
    question: Can I convert PSD to TIFF?
  - answer: For a typical 30 MB PSD the whole pipeline runs under one second on a
      modern CPU.
    question: How fast is the conversion?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert psd
- Aspose.PSD
- Java image manipulation
- tiff export options
title: Aspose.PSD for Java के साथ PSD को TIFF में बदलें और कंट्रास्ट समायोजित करें
url: /hi/java/advanced-techniques/adjust-contrast/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java के साथ PSD को TIFF में बदलना और कंट्रास्ट समायोजित करना

## परिचय

यदि आपको **convert PSD to TIFF** के साथ-साथ अपने ग्राफिक्स की दृश्य गुणवत्ता को बारीकी से समायोजित करने की आवश्यकता है, तो आप सही जगह पर हैं। इस ट्यूटोरियल में हम Aspose.PSD for Java—एक मजबूत **java image manipulation** लाइब्रेरी—का उपयोग करके संपूर्ण वर्कफ़्लो को चरण-दर-चरण देखेंगे। आप सीखेंगे कि **image contrast adjustment** को कैसे बढ़ाया जाए, प्रदर्शन के लिए बड़े रास्टर डेटा को कैश किया जाए, और अंत में **save the image as TIFF** करके डाउनस्ट्रीम प्रोसेसिंग के लिए छवि को सहेजा जाए। चलिए शुरू करते हैं!

## त्वरित उत्तर
- **“adjust contrast” का क्या अर्थ है?** यह सबसे गहरे और सबसे उज्ज्वल पिक्सेल के बीच का अंतर बदलता है, जिससे विवरण उभर कर दिखते हैं।  
- **यह कौन सी लाइब्रेरी संभालती है?** Aspose.PSD for Java – एक पूर्ण‑विशेषताओं वाला इमेज प्रोसेसिंग टूलकिट।  
- **क्या मुझे लाइसेंस चाहिए?** एक **temporary Aspose license** परीक्षण के लिए काम करता है; उत्पादन के लिए पूर्ण लाइसेंस आवश्यक है।  
- **क्या मैं PSD को TIFF में बदल सकता हूँ?** बिल्कुल – हम प्रोसेस की गई छवि को निर्यात करने के लिए `TiffOptions` का उपयोग करेंगे।  
- **परिवर्तन की गति कितनी है?** एक सामान्य 30 MB PSD के लिए पूरी पाइपलाइन आधुनिक CPU पर एक सेकंड से कम समय में चलती है।

## इमेज कंट्रास्ट समायोजन क्या है?

कंट्रास्ट समायोजन एक छवि की टोनल रेंज को बदलता है, प्रकाश और अंधेरे क्षेत्रों के बीच अंतर को बढ़ाता है। यह विशेष रूप से तब उपयोगी होता है जब स्कैन करने के बाद छवियां सपाट दिखती हैं या प्रिंट के लिए ग्राफिक्स तैयार करते समय। यह पिक्सेल तीव्रता के हिस्टोग्राम को खींचकर या संकुचित करके काम करता है, जिससे छायाएं गहरी और हाइलाइट्स उज्ज्वल हो जाते हैं, जो अनुभूत गहराई और विवरण को बढ़ाता है।

## Aspose.PSD for Java का उपयोग क्यों करें?

Aspose.PSD एक उच्च‑प्रदर्शन, फीचर‑समृद्ध इंजन प्रदान करता है जो **50+ raster और vector formats** को संभाल सकता है, 500 MB तक की फाइलें पूरी मेमोरी लोड किए बिना प्रोसेस कर सकता है, और TIFF में निर्यात करते समय bits‑per‑sample और photometric interpretation पर सटीक नियंत्रण देता है। ये मापनीय क्षमताएं इसे एंटरप्राइज़‑ग्रेड इमेज पाइपलाइनों के लिए शीर्ष विकल्प बनाती हैं।

## पूर्वापेक्षाएँ

- Java प्रोग्रामिंग का बुनियादी ज्ञान।  
- Aspose.PSD for Java लाइब्रेरी स्थापित। आप इसे [here](https://releases.aspose.com/psd/java/) से डाउनलोड कर सकते हैं।

## इम्पोर्ट पैकेज

अपने Java क्लास में आवश्यक इम्पोर्ट जोड़ें:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## चरण 1: छवि लोड करें

`Image` क्लास Aspose.PSD का एंट्री पॉइंट है जो मेमोरी में किसी भी समर्थित रास्टर इमेज का प्रतिनिधित्व करता है।  

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

हम स्रोत PSD फ़ाइल (`sample.psd`) को एक `Image` ऑब्जेक्ट में लोड करते हैं, जो आगे की सभी प्रोसेसिंग के लिए एंट्री पॉइंट के रूप में कार्य करता है।

## चरण 2: RasterImage में कास्ट करें और डेटा कैश करें

`RasterImage` सीधे पिक्सेल‑स्तर की पहुंच प्रदान करता है और बड़े फ़ाइलों के लिए कैशिंग सक्षम करता है।  

```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

`RasterImage` में कास्ट करने से हमें पिक्सेल‑स्तर के ऑपरेशन्स तक पहुंच मिलती है। कैशिंग प्रदर्शन को सुधारती है, विशेष रूप से बड़े फ़ाइलों के लिए।

## छवि का कंट्रास्ट कैसे समायोजित करें

`adjustContrast` मेथड एक सरल API कॉल है जो छवि कंट्रास्ट को प्रतिशत मान से बदलता है।  

```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

`adjustContrast` मेथड एक पूर्णांक लेता है जो प्रतिशत परिवर्तन को दर्शाता है। इस उदाहरण में हम कंट्रास्ट को **50 %** तक बढ़ाते हैं।

## Aspose.PSD का उपयोग करके PSD को TIFF में बदलें

`TiffOptions` आपको TIFF‑विशिष्ट सेटिंग्स जैसे bits per sample, compression type, और photometric interpretation निर्दिष्ट करने की अनुमति देता है।  

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Save the resultant image to TIFF format
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

यहां हम `TiffOptions` (bits per sample, photometric interpretation) को कॉन्फ़िगर करते हैं और **save image as TIFF** करते हैं। यह चरण **convert PSD to TIFF** वर्कफ़्लो को पूरा करता है।

## सामान्य समस्याएँ और समाधान
- **छवि कैश नहीं हुई:** हमेशा बड़े PSDs के लिए `cacheData()` कॉल करें ताकि `OutOfMemoryError` से बचा जा सके।  
- **अनपेक्षित रंग परिवर्तन:** `setPhotometric` आपके लक्ष्य रंग स्थान (RGB बनाम CMYK) से मेल खाता है, यह सुनिश्चित करें।  
- **फ़ाइल नहीं मिली:** सुनिश्चित करें कि `dataDir` सही फ़ोल्डर की ओर इशारा कर रहा है और फ़ाइल नाम सही लिखा गया है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.PSD विभिन्न इमेज फ़ॉर्मैट्स के साथ संगत है?
A1: हाँ, Aspose.PSD **50+ इनपुट और आउटपुट फ़ॉर्मैट्स** का समर्थन करता है, जिसमें PSD, TIFF, PNG, JPEG, BMP, और GIF शामिल हैं, जो आपको प्रोजेक्ट्स में लचीलापन देता है।

### Q2: मैं Aspose.PSD के लिए एक अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूँ?
A2: आप एक अस्थायी लाइसेंस [here](https://purchase.aspose.com/temporary-license/) से प्राप्त कर सकते हैं।

### Q3: मैं Aspose.PSD दस्तावेज़ीकरण कहाँ पा सकता हूँ?
A3: दस्तावेज़ीकरण [here](https://reference.aspose.com/psd/java/) पर उपलब्ध है।

### Q4: Aspose.PSD के लिए कौन से समर्थन विकल्प उपलब्ध हैं?
A4: समर्थन के लिए, [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) पर जाएँ।

### Q5: क्या मैं Aspose.PSD खरीद सकता हूँ?
A5: हाँ, आप Aspose.PSD [here](https://purchase.aspose.com/buy) से खरीद सकते हैं।

## निष्कर्ष

अब आप जानते हैं **PSD को TIFF में कैसे बदलें** और Aspose.PSD for Java का उपयोग करके **इमेज कंट्रास्ट समायोजन** कैसे किया जाता है। ये चरण आपको इमेज क्वालिटी पर सूक्ष्म नियंत्रण देते हैं जबकि कोड को साफ़ और रखरखाव योग्य रखते हैं। अपने विशिष्ट आवश्यकताओं के अनुसार `adjustBrightness` या `adjustGamma` जैसे अन्य समायोजन मेथड्स के साथ प्रयोग करने में संकोच न करें।

---

**अंतिम अपडेट:** 2026-07-27  
**परीक्षण किया गया संस्करण:** Aspose.PSD for Java 24.12  
**लेखक:** Aspose

## संबंधित ट्यूटोरियल

- [Java इमेज प्रोसेसिंग ट्यूटोरियल - Aspose.PSD for Java के साथ छवि की चमक समायोजित करना](/psd/java/advanced-techniques/adjust-brightness/)
- [Aspose.PSD के साथ Java इमेज प्रोसेसिंग में गामा कैसे समायोजित करें](/psd/java/advanced-techniques/adjust-gamma/)
- [Aspose.PSD for Java के साथ PSD को रास्टर इमेज फ़ॉर्मैट्स में बदलें](/psd/java/advanced-techniques/convert-psd-to-raster-forms/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}