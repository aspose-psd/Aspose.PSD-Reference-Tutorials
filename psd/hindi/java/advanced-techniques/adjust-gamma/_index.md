---
date: 2026-02-27
description: Aspose.PSD के साथ जावा इमेज प्रोसेसिंग में गामा कैसे समायोजित करें, PSD
  को TIFF में बदलें, और धुंधले चित्रों को ठीक करें, इस संक्षिप्त ट्यूटोरियल में सीखें।
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: Aspose.PSD के साथ जावा इमेज प्रोसेसिंग में गामा कैसे समायोजित करें
url: /hi/java/advanced-techniques/adjust-gamma/
weight: 23
---

-backtop-button >}}

Now produce final content with translations.

Need to ensure Hindi text is correct.

Let's craft.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD के साथ जावा इमेज प्रोसेसिंग में गामा कैसे समायोजित करें

## परिचय

यदि आप **java image processing** पर काम कर रहे हैं, तो **गामा कैसे समायोजित करें** सीखना एक बुनियादी तकनीक है जो विवरण खोए बिना चमक और कंट्रास्ट को बेहतर बनाती है। इस ट्यूटोरियल में हम देखेंगे कि **Aspose.PSD for Java** का उपयोग करके PSD फ़ाइल पर गामा करेक्शन कैसे लागू करें, **PSD को TIFF में बदलें**, और **धुंधली छवि** से बचें। आप देखेंगे कि यह तरीका तेज़, भरोसेमंद, और सर्वर‑साइड इमेज पाइपलाइन के लिए परफेक्ट क्यों है।

## त्वरित उत्तर
- **गामा करेक्शन क्या करता है?** यह ल्यूमिनेंस मानों को पुनः मैप करता है ताकि अंधेरे क्षेत्रों को उज्जवल या उज्ज्वल क्षेत्रों को गहरा बनाया जा सके, जबकि कुल मिलाकर विवरण बरकरार रहे।  
- **कौनसी लाइब्रेरी प्रोसेसिंग संभालती है?** Aspose.PSD for Java रास्टर इमेज के लिए एक समर्पित `adjustGamma` मेथड प्रदान करती है।  
- **क्या मैं उसी फ्लो में PSD को TIFF में बदल सकता हूँ?** हाँ – गामा समायोजन के बाद आप `TiffOptions` का उपयोग करके इमेज को सीधे TIFF में सहेज सकते हैं।  
- **क्या विकास के लिए लाइसेंस चाहिए?** परीक्षण के लिए एक फ्री ट्रायल काम करता है; प्रोडक्शन उपयोग के लिए एक कमर्शियल लाइसेंस आवश्यक है।  
- **कौनसा Java संस्करण समर्थित है?** Aspose.PSD Java 8 और बाद के संस्करणों को सपोर्ट करता है।

## जावा इमेज प्रोसेसिंग में गामा कैसे समायोजित करें
गामा समायोजन किसी भी **java image processing tutorial** का मूल भाग है जो चमक या कंट्रास्ट से संबंधित है। नीचे हम चरणों को तोड़ते हैं, प्रत्येक लाइन क्यों महत्वपूर्ण है समझाते हैं, और दिखाते हैं कि इस प्रक्रिया को आपके मौजूदा कोडबेस में कैसे इंटीग्रेट करें।

## जावा गामा करेक्शन क्या है?
गामा करेक्शन एन्कोडेड पिक्सेल मानों और प्रदर्शित चमक के बीच के गैर‑रेखीय संबंध को बदलता है। गामा कर्व को ट्यून करके आप **धुंधली छवि** की समस्याओं को ठीक कर सकते हैं या शैडोज़ में विवरण बढ़ा सकते हैं बिना हाइलाइट्स को अधिक उज्ज्वल किए।

## गामा करेक्शन के लिए Aspose.PSD क्यों उपयोग करें?
Aspose.PSD एक शक्तिशाली **java image processing library** है जो PSD फ़ॉर्मेट की जटिलताओं को सरल बनाती है। यह कलर प्रोफ़ाइल, कैशिंग को संभालती है, और एक सरल `adjustGamma` कॉल प्रदान करती है, जिससे यह **java gamma correction** और **convert PSD to TIFF** वर्कफ़्लो के लिए आदर्श बनती है।

## पूर्वापेक्षाएँ

1. **Java Development Environment** – Java 8 या बाद का संस्करण स्थापित हो।  
2. **Aspose.PSD Library** – JAR को डाउनलोड करके अपने प्रोजेक्ट में जोड़ें। आधिकारिक [documentation](https://reference.aspose.com/psd/java/) देखें।  
3. **Sample Image** – वह PSD फ़ाइल जिसे आप प्रोसेस करना चाहते हैं (उदा., `sample.psd`)।  

## पैकेज इम्पोर्ट करें

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## चरण 1: इमेज लोड करें

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

**प्रो टिप:** रास्टर डेटा को एक बार कैश करने से मेमोरी चर्न कम होता है जब आप क्रमिक रूप से कई समायोजन लागू करते हैं।

## चरण 2: गामा समायोजित करें

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

यदि आपको चैनल‑विशिष्ट ट्यूनिंग चाहिए तो आप लाल, हरे और नीले चैनलों के लिए अलग-अलग मान पास कर सकते हैं।

## चरण 3: TiffOptions बनाएं

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

8‑बिट सैंपल (`{8,8,8}`) सेट करने से TIFF फ़ाइल का आकार उचित रहता है जबकि रंग की सटीकता बनी रहती है।

## चरण 4: परिणामस्वरूप इमेज सहेजें

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

सहेजने के बाद आप TIFF को प्रिंट सेवाओं या वेब API जैसी डाउनस्ट्रीम सिस्टम में फीड कर सकते हैं।

## सामान्य उपयोग केस

- **ऑटोमेटेड ग्राफ़िक्स पाइपलाइन** – थंबनेल जनरेट करने से पहले गामा को रियल‑टाइम में समायोजित करें।  
- **बैच कन्वर्ज़न टूल्स** – बड़े PSD आर्काइव को TIFF में बदलते समय चमक को सामान्यीकृत करें।  
- **वेब सर्विसेज** – एक एन्डपॉइंट एक्सपोज़ करें जो PSD प्राप्त करता है, गामा करेक्शन लागू करता है, और क्लाइंट के लिए TIFF लौटाता है।

## सामान्य समस्याएँ और समाधान

| Issue | Why it Happens | How to Fix |
|-------|----------------|------------|
| **Image appears washed out** | Gamma value बहुत अधिक (जैसे > 2.5) | गामा फ़ैक्टर को 1.8 से 2.2 के बीच घटाएँ। |
| **`rasterImage.isCached()` returns false** | इमेज अभी मेमोरी में लोड नहीं हुई | गामा समायोजित करने से पहले `rasterImage.cacheData()` कॉल करें। |
| **TIFF file size is large** | सैंपल बिट्स 16‑bit सेट हैं | उदाहरण में दिखाए अनुसार 8‑bit सैंपल (`{8,8,8}`) उपयोग करें। |

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या मैं प्रत्येक रंग चैनल के लिए अलग गामा मान लागू कर सकता हूँ?**  
A: हाँ – `adjustGamma` मेथड लाल, हरे और नीले चैनलों के लिए अलग‑अलग फ़्लोट मान स्वीकार करता है।

**Q: क्या सहेजने से पहले कई इमेज समायोजन को चेन किया जा सकता है?**  
A: बिल्कुल। आप उसी `RasterImage` इंस्टेंस पर क्रमिक रूप से रिसाइज़िंग, क्रॉपिंग या कलर करेक्शन कर सकते हैं।

**Q: क्या Aspose.PSD मल्टी‑पेज PSD फ़ाइलों को सपोर्ट करता है?**  
A: हाँ, प्रत्येक लेयर को अलग‑अलग एक्सेस करके प्रोसेस किया जा सकता है।

**Q: TIFF के अलावा मैं कौनसे फ़ॉर्मेट में एक्सपोर्ट कर सकता हूँ?**  
A: Aspose.PSD PNG, JPEG, BMP और कई अन्य फ़ॉर्मेट को उनके संबंधित ऑप्शन क्लासेज़ के माध्यम से सपोर्ट करता है।

**Q: गामा करेक्शन के बाद धुंधली छवि से कैसे बचें?**  
A: लगभग 2.0 के मध्यम गामा से शुरू करें और परिणाम का प्रीव्यू लें; यदि छवि बहुत उज्ज्वल दिखे तो मान को नीचे की ओर समायोजित करें।

## निष्कर्ष

बधाई हो! आपने **java image processing** वर्कफ़्लो में **गामा कैसे समायोजित करें** सीख लिया, PSD को TIFF में बदला, और **धुंधली छवि** जैसी सामान्य समस्याओं से बचा। यह पैटर्न आपको चमक और कंट्रास्ट पर सूक्ष्म नियंत्रण देता है, जिससे यह ऑटोमेटेड ग्राफ़िक्स पाइपलाइन, वेब सर्विसेज या डेस्कटॉप यूटिलिटीज़ के लिए आदर्श बनता है।

---

**Last Updated:** 2026-02-27  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}