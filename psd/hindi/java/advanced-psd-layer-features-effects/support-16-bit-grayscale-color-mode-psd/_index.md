---
date: 2026-09-28
description: Aspose.PSD for Java का उपयोग करके PSD कलर मोड को 16‑बिट ग्रेस्केल पर
  सेट करते हुए PSD को PNG में एक्सपोर्ट करना सीखें। कोड उदाहरणों के साथ चरण‑दर‑चरण
  गाइड।
keywords:
- export psd as png
- how to convert psd to png
- 16-bit grayscale java
lastmod: 2026-09-28
linktitle: PSD को PNG में एक्सपोर्ट – 16‑बिट ग्रेस्केल – Java
og_description: Aspose.PSD for Java का उपयोग करके 16‑बिट ग्रेस्केल के साथ PSD को PNG
  में एक्सपोर्ट करें। 65,000 ग्रे शेड्स को संरक्षित करने के लिए इस चरण‑दर‑चरण ट्यूटोरियल
  का पालन करें।
og_image_alt: Guide showing how to export PSD as PNG with 16-bit grayscale using Aspose.PSD
  Java
og_title: Java में 16‑बिट ग्रेस्केल के साथ PSD को PNG में एक्सपोर्ट – Aspose.PSD गाइड
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  headline: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  type: TechArticle
- description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  name: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  steps:
  - name: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
  - name: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
    text: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
  - name: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
    text: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
  - name: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
    text: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
  type: HowTo
- questions:
  - answer: It provides 65 536 shades of gray, delivering far more tonal detail than
      the standard 8‑bit (256 shades).
    question: What is 16‑bit grayscale color mode?
  - answer: Absolutely! Aspose.PSD supports RGB, CMYK, Lab, Indexed, and many other
      color modes.
    question: Can I use Aspose.PSD for non‑grayscale images?
  - answer: Yes, you can try a free trial version of Aspose.PSD. Just head to the
      [Aspose download page](https://releases.aspose.com/).
    question: Is there a trial version of Aspose.PSD?
  - answer: Check the official [documentation](https://reference.aspose.com/psd/java/)
      for in‑depth tutorials, API references, and sample projects.
    question: Where can I find more Aspose.PSD examples?
  - answer: You can buy a license by visiting the [Aspose purchase page](https://purchase.aspose.com/buy).
    question: How do I purchase a license for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert psd
- Aspose.PSD
- Java image processing
title: Java में 16‑बिट ग्रेस्केल कलर मोड के साथ PSD को PNG में एक्सपोर्ट कैसे करें
url: /hi/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java में 16‑बिट ग्रेस्केल कलर मोड के साथ PSD को PNG के रूप में निर्यात करें

## परिचय
PSD को PNG के रूप में निर्यात करते हुए 16‑बिट ग्रेस्केल कलर मोड बनाए रखने से आपको एक पेशेवर फ़ोटोग्राफ़ की गहराई और PNG की सार्वभौमिक संगतता मिलती है। इस गाइड में आप सीखेंगे कि **PSD कलर मोड को 16‑बिट ग्रेस्केल पर कैसे सेट करें** और फिर **Aspose.PSD for Java** का उपयोग करके PSD को PNG के रूप में निर्यात करें। ट्यूटोरियल में प्री‑रिक्विज़िट्स से लेकर ट्रबलशूटिंग तक सब कुछ कवर किया गया है, ताकि आप इस वर्कफ़्लो को किसी भी Java‑आधारित इमेज पाइपलाइन में एकीकृत कर सकें।

## त्वरित उत्तर
- **“PSD को PNG के रूप में निर्यात करना” क्या शामिल है?** एक PSD लोड करें, वैकल्पिक रूप से उसका कलर मोड बदलें, और इसे PNG फ़ाइल के रूप में सहेजें।  
- **कौन सा Aspose क्लास रूपांतरण संभालता है?** `PsdImage` PSD को लोड करता है और `PngOptions` PNG आउटपुट सेटिंग्स को परिभाषित करता है।  
- **क्या उत्पादन के लिए लाइसेंस चाहिए?** हाँ – परीक्षण के लिए ट्रायल काम करता है, लेकिन व्यावसायिक उपयोग के लिए भुगतान लाइसेंस आवश्यक है।  
- **क्या PNG में 16‑बिट डेप्थ बरकरार रखी जा सकती है?** बिल्कुल, `PngColorType.GrayscaleWithAlpha` का उपयोग करके।  
- **कौन से IDE समर्थित हैं?** कोई भी Java IDE – IntelliJ IDEA, Eclipse, VS Code, या NetBeans।

## PSD को PNG के रूप में निर्यात करना क्या है?
Export PSD as PNG वह प्रक्रिया है जिसमें Adobe Photoshop दस्तावेज़ (PSD) को Portable Network Graphics (PNG) फ़ाइल में परिवर्तित किया जाता है, जबकि इमेज के पिक्सेल डेटा और कलर डेप्थ को संरक्षित रखा जाता है। यह रूपांतरण आमतौर पर वेब पर उच्च‑गुणवत्ता वाले ग्रेस्केल एसेट्स को टोनल विवरण खोए बिना साझा करने के लिए उपयोग किया जाता है।

## 16‑बिट ग्रेस्केल के साथ PSD को PNG के रूप में निर्यात क्यों करें?
PNG में निर्यात करते समय 16‑बिट ग्रेस्केल बनाए रखने से 65 536 शेड्स ऑफ ग्रे संरक्षित रहते हैं, जो 8‑बिट इमेजेज़ की तुलना में बहुत अधिक टोनल समृद्धि प्रदान करता है। PNG का सार्वभौमिक समर्थन सुनिश्चित करता है कि फ़ाइलें ब्राउज़र, मोबाइल ऐप्स और डेस्कटॉप एडिटर्स में बिना किसी हानि के प्रदर्शित हो सकें, जबकि Aspose.PSD का लॉसलेस कम्प्रेशन गारंटी देता है कि कोई आर्टिफैक्ट नहीं जुड़ेंगे।

## पूर्वापेक्षाएँ
1. **Java Development Kit (JDK)** – नवीनतम JDK को [Oracle's site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) से इंस्टॉल करें।  
2. **Aspose.PSD for Java library** – JAR को [Aspose download page](https://releases.aspose.com/psd/java/) से डाउनलोड करें।  
3. **एक IDE** – IntelliJ IDEA, Eclipse, या Visual Studio Code पूरी तरह काम करता है।  
4. **बेसिक Java ज्ञान** – आपको क्लासेज़ बनाना, एक्सेप्शन हैंडल करना, और फ़ाइल पाथ्स के साथ काम करना सहज होना चाहिए।  
5. **एक सैंपल PSD फ़ाइल** – Adobe Photoshop में बनाएं या ऑनलाइन एक मुफ्त सैंपल प्राप्त करें।

## PSD को PNG के रूप में निर्यात करने के चरण-दर-चरण

## आप PSD कलर मोड को 16‑बिट ग्रेस्केल पर कैसे सेट करते हैं?
PsdImage Aspose.PSD क्लास है जो मेमोरी में PSD फ़ाइल को लोड और प्रतिनिधित्व करता है।  
ColorMode एक enumeration है जो PSD इमेज के कलर मोड को परिभाषित करता है।  

`PsdImage` से PSD लोड करें, `ColorMode` प्रॉपर्टी का उपयोग करके उसका कलर मोड बदलें, और फिर संशोधित फ़ाइल को सहेजें। यह ऑपरेशन पूरी तरह मेमोरी में चलता है, जिससे मध्यवर्ती फ़ाइलों की आवश्यकता समाप्त हो जाती है और रूपांतरण तेज़ और कुशल बनता है।

```java
import com.aspose.psd.*;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.system.Enum;
```

ये इम्पोर्ट्स आपको उन कार्यात्मकताओं तक पहुँच प्रदान करते हैं जिनका उपयोग आप PSD फ़ाइलों को मैनिपुलेट करने, कलर मोड सेट करने, और परिणाम को PNG के रूप में निर्यात करने के लिए करेंगे।

## स्रोत और आउटपुट डायरेक्टरी कैसे परिभाषित करें?
`File` java.io क्लास है जो फ़ाइल सिस्टम पर फ़ाइल या डायरेक्टरी पाथ को दर्शाता है।  

आपको प्रोग्राम को बताना होगा कि मूल PSD को कहाँ पढ़ना है और परिवर्तित PNG को कहाँ लिखना है। एब्सोल्यूट या रिलेटिव पाथ्स दोनों काम करेंगे, लेकिन पर्यावरणों में पाथ रेज़ोल्यूशन त्रुटियों से बचने के लिए उन्हें सुसंगत रखें।

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

प्लेसहोल्डर स्ट्रिंग्स को अपने मशीन पर वास्तविक पाथ्स से बदलें।

## पुन: उपयोग योग्य मेथड में रूपांतरण लॉजिक को कैसे एन्कैप्सुलेट करें?
`convertPsdToPng` एक कस्टम मेथड है जो PSD फ़ाइल को PNG में वैकल्पिक सेटिंग्स के साथ रूपांतरित करने के सभी चरणों को एन्कैप्सुलेट करता है।  

एक समर्पित मेथड बनाने से आप कई फ़ाइलों या विभिन्न सेटिंग्स के लिए समान रूपांतरण चरणों को पुन: उपयोग कर सकते हैं। स्रोत पाथ, डेस्टिनेशन फ़ोल्डर, और वैकल्पिक कम्प्रेशन लेवल जैसे पैरामीटर पास करें, जिससे वर्कफ़्लो लचीला और मेंटेनेबल बनता है।

```java
class LocalScopeExtension {
    void saveToPsdThenLoadAndSaveToPng(
        String file,
        short colorMode,
        short channelBitsCount,
        short channelsCount,
        short compression,
        int layerNumber) {
```

यह मेथड आपको **PSD कलर मोड सेट करने** और फिर **PSD को PNG के रूप में निर्यात करने** को एक ही प्रवाह में करने की अनुमति देता है।

## आप PSD को लोड करके 16‑बिट ग्रेस्केल मोड कैसे लागू करते हैं?
PsdImage Aspose.PSD क्लास है जो PSD फ़ाइल को मेमोरी में लोड करता है।  
ColorMode.GRAYSCALE_16 एक enumeration वैल्यू है जो इमेज को 16‑बिट ग्रेस्केल पर सेट करती है।  
`channelBitsCount` एक प्रॉपर्टी है जो प्रति चैनल बिट्स की संख्या निर्दिष्ट करती है।  

रूपांतरण मेथड के भीतर, पूर्ण फ़ाइल पाथ बनाएं, `PsdImage` का इंस्टैंसिएट करें, और उसका `ColorMode` को `ColorMode.GRAYSCALE_16` में बदलें। `channelBitsCount` प्रॉपर्टी को 16 पर सेट होना चाहिए ताकि हाई‑बिट डेप्थ बना रहे, जिससे इमेज सभी टोनल जानकारी को बरकरार रखे।

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

`postfix` आपको प्रत्येक निर्यातित फ़ाइल के लिए उपयोग की गई सेटिंग्स को ट्रैक करने में मदद करता है।

## इमेज पर सूक्ष्म बॉर्डर कैसे बनाएं (वैकल्पिक चरण)?
`Graphics` एक क्लास है जो `PsdImage` कैनवास पर ड्राइंग क्षमताएँ प्रदान करता है।  

आप वैकल्पिक रूप से इमेज के चारों ओर एक ग्रे रेक्टैंगल ड्रॉ कर सकते हैं ताकि परीक्षण के दौरान आउटपुट अधिक स्पष्ट दिखे। यह चरण लेयर्स और ग्राफ़िक्स ऑब्जेक्ट्स के साथ काम करने का प्रदर्शन करता है, और रेक्टैंगल डायनामिकली गणना किया जाता है ताकि इमेज साइज की परवाह किए बिना यह केंद्रित रहे।

```java
try {
    RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;
    // Draw a gray inner border around the perimeter of the layer
    Graphics graphics = new Graphics(raster);
    int width = raster.getWidth();
    int height = raster.getHeight();
    Rectangle rect = new Rectangle(
        width / 3,
        height / 3,
        width - (2 * (width / 3)) - 1,
        height - (2 * (height / 3)) - 1);
    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);
```

रेक्टैंगल डायनामिकली गणना किया जाता है ताकि इमेज साइज की परवाह किए बिना यह केंद्रित रहे।

## संशोधित PSD को नए कलर मोड के साथ कैसे सहेजें?
`PsdOptions` एक क्लास है जो नियंत्रित करता है कि PSD फ़ाइल कैसे सहेजी जाए, जिसमें कलर मोड और बिट डेप्थ सेटिंग्स शामिल हैं।  

ड्रॉइंग (या उस चरण को स्किप) के बाद, `PsdImage` इंस्टेंस पर `save` कॉल करें, और एक `PsdOptions` ऑब्जेक्ट पास करें जो 16‑बिट ग्रेस्केल कॉन्फ़िगरेशन को संरक्षित रखता है। इससे यह सुनिश्चित होता है कि सहेजा गया PSD वांछित कलर मोड को बिना किसी डेटा हानि के बरकरार रखे।

```java
    // Save a copy of PSD with specific characteristics
    PsdOptions psdOptions = new PsdOptions();
    psdOptions.setColorMode(colorMode);
    psdOptions.setChannelBitsCount(channelBitsCount);
    psdOptions.setChannelsCount(channelsCount);
    psdOptions.setCompressionMethod(compression);
    image.save(exportPath, psdOptions);
}
```

## PSD को PNG में रूपांतरित करते समय 16‑बिट डेप्थ को कैसे संरक्षित रखें?
`PngOptions` एक क्लास है जो PNG आउटपुट सेटिंग्स जैसे कलर टाइप और कम्प्रेशन लेवल को परिभाषित करता है।  
`PngColorType.GrayscaleWithAlpha` एक enumeration वैल्यू है जो 16‑बिट ग्रेस्केल डेटा को अल्फा चैनल के साथ संग्रहीत करती है।  

नए सहेजे गए PSD को लोड करें, `PngOptions` को `PngColorType.GrayscaleWithAlpha` के साथ कॉन्फ़िगर करें, और `save` कॉल करें। यह PNG फ़ाइल के भीतर 16‑बिट ग्रेस्केल डेटा को बरकरार रखता है, जिससे एक लॉसलेस, हाई‑क्वालिटी इमेज मिलती है जो आगे की प्रोसेसिंग या वितरण के लिए उपयुक्त है।

```java
finally {
    image.dispose();
}
// Load the saved PSD
PsdImage image1 = (PsdImage)Image.load(exportPath);
try {
    // Convert the saved PSD to a grayscale PNG image
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);
    image1.save(pngExportPath, pngOptions); // here should be no exception
}
finally {
    image1.dispose();
}
```

अब आपने सफलतापूर्वक **PSD को PNG के रूप में निर्यात** किया है जबकि हाई‑क्वालिटी 16‑बिट ग्रेस्केल डेटा को बरकरार रखा है।

## सामान्य समस्याएँ और समाधान
| Issue | Why it happens | Fix |
|-------|----------------|-----|
| **“Unsupported color type” exception** | एक असमर्थित चैनल कॉन्फ़िगरेशन वाले PSD को सहेजने का प्रयास करना। | `channelBitsCount` को वास्तविक बिट डेप्थ (16) से मिलाएँ और `channelsCount` को ग्रेस्केल (1) के लिए सही रखें। |
| **File not found** | गलत स्रोत डायरेक्टरी पाथ। | `sourceDir` स्ट्रिंग को दोबारा जांचें और सुनिश्चित करें कि उस स्थान पर PSD फ़ाइल मौजूद है। |
| **Output PNG appears black** | PNG को उचित अल्फा हैंडलिंग के बिना सहेजा गया। | ऊपर दिखाए अनुसार `PngColorType.GrayscaleWithAlpha` का उपयोग करें। |
| **Memory overflow on large PSDs** | पूरी फ़ाइल को मेमोरी में लोड करना। | `PsdImage.load(inputStream, new LoadOptions())` के माध्यम से स्ट्रीमिंग मोड सक्षम करें ताकि बड़े फ़ाइलों को कुशलता से प्रोसेस किया जा सके। |

## अक्सर पूछे जाने वाले प्रश्न

**प्र: 16‑बिट ग्रेस्केल कलर मोड क्या है?**  
**उ:** यह 65 536 शेड्स ऑफ ग्रे प्रदान करता है, जो मानक 8‑बिट (256 शेड्स) की तुलना में बहुत अधिक टोनल विवरण देता है।

**प्र: क्या मैं Aspose.PSD को गैर‑ग्रेस्केल इमेजेज़ के लिए उपयोग कर सकता हूँ?**  
**उ:** बिल्कुल! Aspose.PSD RGB, CMYK, Lab, Indexed, और कई अन्य कलर मोड्स को सपोर्ट करता है।

**प्र: क्या Aspose.PSD का ट्रायल संस्करण उपलब्ध है?**  
**उ:** हाँ, आप Aspose.PSD का मुफ्त ट्रायल संस्करण आज़मा सकते हैं। बस [Aspose download page](https://releases.aspose.com/) पर जाएँ।

**प्र: मैं अधिक Aspose.PSD उदाहरण कहाँ पा सकता हूँ?**  
**उ:** आधिकारिक [documentation](https://reference.aspose.com/psd/java/) देखें जिसमें विस्तृत ट्यूटोरियल, API रेफ़रेंसेज़, और सैंपल प्रोजेक्ट्स हैं।

**प्र: मैं Aspose.PSD का लाइसेंस कैसे खरीदूँ?**  
**उ:** आप लाइसेंस खरीदने के लिए [Aspose purchase page](https://purchase.aspose.com/buy) पर जा सकते हैं।

---

**अंतिम अपडेट:** 2026-09-28  
**परीक्षित संस्करण:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**लेखक:** Aspose

## संबंधित ट्यूटोरियल्स

- [Aspose.PSD for Java का उपयोग करके निर्दिष्ट बिट डेप्थ के साथ PSD को PNG में परिवर्तित करें](/psd/java/optimizing-png-files/specify-png-bit-depth/)
- [Aspose.PSD for Java का उपयोग करके लेयर इफ़ेक्ट्स के साथ PSD को PNG में निर्यात करें](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [Aspose.PSD Java के साथ PSD को JPEG के रूप में सहेजें और RGB कलर को सपोर्ट करें](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}