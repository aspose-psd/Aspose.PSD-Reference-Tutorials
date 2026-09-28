---
date: 2026-09-28
description: Java इमेज प्रोसेसिंग ट्यूटोरियल दिखाता है कि कैसे Aspose.PSD for Java
  का उपयोग करके इमेज की ब्राइटनेस समायोजित की जाए। चरण‑दर‑चरण कोड का पालन करें ताकि
  PSD या TIFF फ़ाइलों को load, modify, और save किया जा सके।
keywords:
- java image processing
- aspose psd java
- java image manipulation
- adjust brightness java
lastmod: 2026-09-28
linktitle: इमेज की ब्राइटनेस समायोजित करें
og_description: Java इमेज प्रोसेसिंग ट्यूटोरियल दिखाता है कि कैसे Aspose.PSD for Java
  का उपयोग करके इमेज की ब्राइटनेस समायोजित की जाए। चरण‑दर‑चरण कोड का पालन करें ताकि
  PSD या TIFF फ़ाइलों को load, modify, और save किया जा सके।
og_image_alt: Guide to adjusting image brightness in Java using Aspose.PSD
og_title: 'Java इमेज प्रोसेसिंग: Aspose.PSD के साथ ब्राइटनेस समायोजित करें'
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  headline: 'Java image processing: adjust brightness with Aspose.PSD'
  type: TechArticle
- description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  name: 'Java image processing: adjust brightness with Aspose.PSD'
  steps:
  - name: Load the image
    text: The `RasterImage` class represents a rasterized version of a PSD or TIFF
      file in memory. It provides direct pixel access for color‑correction operations.
      In this step, we load the target image and cast it to a `RasterImage` for further
      processing.
  - name: Adjust brightness
    text: '`adjustBrightness(int value)` changes the lightness of every pixel by the
      specified integer value. Positive numbers brighten the image; negative numbers
      darken it. The method processes the image in‑place, so no additional object
      creation is required. Here, we use the `adjustBrightness` method to mod'
  - name: Set TiffOptions
    text: '`TiffOptions` specifies the encoding parameters for TIFF output, such as
      bits per sample and photometric interpretation. It lets you control how the
      resulting file is encoded. Configure the `TiffOptions` for saving the adjusted
      image. Adjust the `bitsPerSample` and `photometric` properties based on '
  - name: Save the resultant image
    text: Calling `save` writes the processed raster data to a file using the previously
      defined options. The operation is atomic and guarantees that the output file
      is a valid TIFF image. Finally, save the modified image using the specified
      `TiffOptions`.
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD for Java supports JPEG, PNG, BMP, GIF, and many other
      raster formats in addition to PSD and TIFF.
    question: Can I adjust brightness in other image formats besides PSD?
  - answer: Wrap the processing code in a try‑catch block and catch `IOException`
      or `ImageProcessingException` to manage file‑access and raster‑operation errors.
    question: How can I handle errors during the image adjustment process?
  - answer: The method accepts integer values from –255 to +255; values outside this
      range are clamped to the nearest limit.
    question: Is there a limit to the range of brightness adjustment?
  - answer: Yes, a commercial license is required for production use. Purchase a license
      [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD for Java in commercial projects?
  - answer: Yes, you can explore the library with a free trial from [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose psd
- java image manipulation
title: 'Java इमेज प्रोसेसिंग: Aspose.PSD के साथ ब्राइटनेस समायोजित करें'
url: /hi/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java के साथ छवि की चमक समायोजित करें

## परिचय

इस **java image processing** ट्यूटोरियल में आप सीखेंगे कि जावा कोड से सीधे चित्र की चमक कैसे समायोजित की जाए। चमक समायोजन ग्राफिक डिज़ाइनरों, फ़ोटोग्राफ़रों और किसी भी व्यक्ति के लिए एक सामान्य कार्य है जो इमेज‑प्रोसेसिंग पाइपलाइन बनाता है। इस **java image manipulation** गाइड में हम पूरी कार्यप्रणाली—PSD/TIFF लोड करना, चमक ऑफ़सेट लागू करना, और परिणाम सहेजना—को Aspose.PSD for Java लाइब्रेरी का उपयोग करके दिखाएंगे।

## त्वरित उत्तर
- **कौन सी लाइब्रेरी चमक संभालती है?** Aspose.PSD for Java।  
- **कौन सा मेथड चमक बदलता है?** `RasterImage.adjustBrightness()`।  
- **क्या मैं PSD और TIFF फ़ाइलों के साथ काम कर सकता हूँ?** हाँ, API दोनों फ़ॉर्मैट और 10+ अतिरिक्त इमेज टाइप्स को सपोर्ट करता है।  
- **उत्पादन के लिए लाइसेंस चाहिए?** गैर‑इवैल्यूएशन उपयोग के लिए एक कमर्शियल लाइसेंस आवश्यक है।  
- **इम्प्लीमेंटेशन में कितना समय लगेगा?** बेसिक समायोजन के लिए आमतौर पर 10 मिनट से कम।

## java image processing क्या है?
`Java image processing` उन तकनीकों का समूह है जो आपको जावा का उपयोग करके प्रोग्रामेटिक रूप से इमेज डेटा को पढ़ने, बदलने और लिखने की अनुमति देता है। चमक समायोजन वह मुख्य ऑपरेशन है जो प्रत्येक पिक्सेल की समग्र प्रकाशता को बदलता है, जिससे अंधेरे क्षेत्रों को उज्ज्वल या उज्ज्वल क्षेत्रों को धुंधला किया जाता है।

## Aspose.PSD for Java क्यों उपयोग करें?
Aspose.PSD for Java एक व्यापक, शुद्ध‑जावा समाधान प्रदान करता है जो रास्टर और वेक्टर फ़ॉर्मैट्स की विस्तृत श्रृंखला को सपोर्ट करता है, नेटिव डिपेंडेंसीज़ को समाप्त करता है, और बड़े फ़ाइलों के लिए हाई‑परफ़ॉर्मेंस कैशिंग प्रदान करता है। इसका विस्तृत API डेवलपर्स को न्यूनतम कोड के साथ जटिल कलर‑करेक्शन और लेयर‑आधारित संपादन करने देता है, जिससे यह साधारण समायोजन और उन्नत इमेज‑प्रोसेसिंग पाइपलाइन दोनों के लिए आदर्श बनता है।

- **10+ रास्टर और वेक्टर फ़ॉर्मैट्स को सपोर्ट करता है** – PSD, TIFF, JPEG, PNG, BMP, GIF, और अधिक।  
- **शुद्ध‑जावा इम्प्लीमेंटेशन** – कोई नेटिव DLL या बाहरी डिपेंडेंसी नहीं, इसलिए यह किसी भी JVM पर काम करता है।  
- **हाई‑परफ़ॉर्मेंस कैशिंग** – रास्टर डेटा को कैश किया जा सकता है, जिससे बड़े फ़ाइलों पर दोहराए गए एडिट्स 2× तेज़ हो जाते हैं।  
- **समृद्ध API सतह** – कलर करेक्शन, लेयर हैंडलिंग, मास्क, और कंपोज़िटिंग के लिए 150 से अधिक मेथड्स।

## पूर्वापेक्षाएँ

ट्यूटोरियल शुरू करने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ हों:

- Aspose.PSD for Java लाइब्रेरी: लाइब्रेरी को [Aspose.PSD for Java दस्तावेज़](https://reference.aspose.com/psd/java/) से डाउनलोड और इंस्टॉल करें।  
- Java Development Kit (JDK) 8 या उससे ऊपर आपके मशीन पर स्थापित हो।  
- एक विकास वातावरण (IDE) जैसे IntelliJ IDEA, Eclipse, या VS Code।

## पैकेज इम्पोर्ट करें

शुरू करने के लिए, आवश्यक पैकेजों को अपने जावा प्रोजेक्ट में इम्पोर्ट करें। इस उदाहरण में, हम निम्नलिखित का उपयोग करेंगे:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

अब, छवि की चमक समायोजित करने की प्रक्रिया को सरल चरणों में विभाजित करते हैं:

## Aspose.PSD का उपयोग करके चमक कैसे समायोजित करें?

अपने स्रोत चित्र को लोड करें, चमक ऑफ़सेट लागू करें, सेव ऑप्शन कॉन्फ़िगर करें, और परिणाम को डिस्क पर लिखें—सभी चार संक्षिप्त चरणों में। नीचे के सेक्शन एक स्पष्ट, चरण‑दर‑चरण walkthrough प्रदान करते हैं जिसे आप अपने प्रोजेक्ट में कॉपी कर सकते हैं। यह दृष्टिकोण सुनिश्चित करता है कि प्रत्येक ऑपरेशन कुशलता से किया जाए और अंतिम छवि मूल गुणवत्ता को बनाए रखते हुए इच्छित चमक परिवर्तन को दर्शाए।

### चरण 1: छवि लोड करें

`RasterImage` क्लास मेमोरी में PSD या TIFF फ़ाइल का रास्टराइज़्ड संस्करण दर्शाता है। यह कलर‑करेक्शन ऑपरेशन्स के लिए सीधे पिक्सेल एक्सेस प्रदान करता है।

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage) image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

इस चरण में, हम लक्ष्य छवि को लोड करते हैं और आगे की प्रोसेसिंग के लिए इसे `RasterImage` में कास्ट करते हैं।

### चरण 2: चमक समायोजित करें

`adjustBrightness(int value)` प्रत्येक पिक्सेल की लाइटनेस को निर्दिष्ट पूर्णांक मान से बदलता है। सकारात्मक संख्या छवि को उज्ज्वल करती है; नकारात्मक संख्या इसे धुंधला करती है। यह मेथड इमेज को इन‑प्लेस प्रोसेस करता है, इसलिए अतिरिक्त ऑब्जेक्ट निर्माण की आवश्यकता नहीं होती।

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

यहाँ, हम `adjustBrightness` मेथड का उपयोग करके छवि की चमक बदलते हैं। इस उदाहरण में, हम चमक को 50 यूनिट घटाते हैं, लेकिन आप अपनी आवश्यकता के अनुसार इस मान को कस्टमाइज़ कर सकते हैं।

### चरण 3: TiffOptions सेट करें

`TiffOptions` TIFF आउटपुट के एन्कोडिंग पैरामीटर निर्दिष्ट करता है, जैसे बिट्स पर सैंपल और फोटोमेट्रिक इंटरप्रिटेशन। यह आपको परिणाम फ़ाइल के एन्कोडिंग को नियंत्रित करने की अनुमति देता है।

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

समायोजित छवि को सहेजने के लिए `TiffOptions` को कॉन्फ़िगर करें। अपनी विशिष्ट आवश्यकताओं के आधार पर `bitsPerSample` और `photometric` प्रॉपर्टीज़ को समायोजित करें।

### चरण 4: परिणामी छवि सहेजें

`save` को कॉल करने से प्रोसेस्ड रास्टर डेटा को पहले परिभाषित विकल्पों के साथ फ़ाइल में लिखा जाता है। यह ऑपरेशन एटॉमिक है और सुनिश्चित करता है कि आउटपुट फ़ाइल एक वैध TIFF इमेज हो।

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

अंत में, निर्दिष्ट `TiffOptions` के साथ संशोधित छवि को सहेजें।

## सामान्य समस्याएँ और समाधान

| समस्या | कारण | समाधान |
|-------|--------|----------|
| **`ClassCastException` जब Image को कास्ट किया जाता है** | फ़ाइल रास्टर इमेज नहीं है (जैसे, वेक्टर PSD)। | स्रोत फ़ाइल फ़ॉर्मैट सत्यापित करें या कास्ट करने से पहले `image instanceof RasterImage` जांचें। |
| **चमक परिवर्तन का कोई प्रभाव नहीं** | समायोजन से पहले इमेज कैश नहीं हुई थी। | चरण 1 में दिखाए अनुसार `rasterImage.cacheData()` कॉल करें। |
| **सहेजी गई फ़ाइल भ्रष्ट दिखती है** | `TiffOptions` कॉन्फ़िगरेशन गलत है। | सुनिश्चित करें कि `bitsPerSample` स्रोत इमेज की डेप्थ (आमतौर पर 8‑बिट प्रति चैनल) से मेल खाता है। |

## अक्सर पूछे जाने वाले प्रश्न

**प्रश्न: क्या मैं PSD के अलावा अन्य इमेज फ़ॉर्मैट्स में भी चमक समायोजित कर सकता हूँ?**  
उत्तर: हाँ, Aspose.PSD for Java JPEG, PNG, BMP, GIF, और कई अन्य रास्टर फ़ॉर्मैट्स को PSD और TIFF के अतिरिक्त सपोर्ट करता है।

**प्रश्न: इमेज समायोजन प्रक्रिया के दौरान त्रुटियों को कैसे संभालूँ?**  
उत्तर: प्रोसेसिंग कोड को try‑catch ब्लॉक में रखें और `IOException` या `ImageProcessingException` को कैच करके फ़ाइल‑एक्सेस और रास्टर‑ऑपरेशन त्रुटियों को प्रबंधित करें।

**प्रश्न: चमक समायोजन की रेंज पर कोई सीमा है?**  
उत्तर: मेथड –255 से +255 तक के पूर्णांक मान स्वीकार करता है; इस रेंज से बाहर के मान निकटतम सीमा पर क्लैंप हो जाते हैं।

**प्रश्न: क्या मैं Aspose.PSD for Java को व्यावसायिक प्रोजेक्ट्स में उपयोग कर सकता हूँ?**  
उत्तर: हाँ, उत्पादन उपयोग के लिए एक कमर्शियल लाइसेंस आवश्यक है। लाइसेंस [यहाँ](https://purchase.aspose.com/buy) खरीदें।

**प्रश्न: क्या कोई फ्री ट्रायल उपलब्ध है?**  
उत्तर: हाँ, आप [यहाँ](https://releases.aspose.com/) से फ्री ट्रायल के साथ लाइब्रेरी का अन्वेषण कर सकते हैं।

**प्रश्न: क्या `adjustBrightness` मेथड लेयर विज़िबिलिटी को प्रभावित करता है?**  
उत्तर: यह मेथड रास्टराइज़्ड कॉम्पोज़िट इमेज पर काम करता है, इसलिए छिपी हुई लेयर्स रास्टराइज़ेशन के दौरान अनदेखी रहती हैं, जिससे इच्छित विज़ुअल परिणाम बना रहता है।

**प्रश्न: क्या मैं कई समायोजन (जैसे, कॉन्ट्रास्ट, सैचुरेशन) को एक साथ चेन कर सकता हूँ?**  
उत्तर: बिल्कुल। चमक समायोजित करने के बाद, आप उसी `RasterImage` इंस्टेंस पर `adjustContrast`, `adjustSaturation`, या अन्य कलर‑करेक्शन मेथड्स को कॉल कर सकते हैं।

---

**अंतिम अपडेट:** 2026-09-28  
**टेस्टेड विद:** Aspose.PSD for Java 24.12 (लेखन समय पर नवीनतम)  
**लेखक:** Aspose

## संबंधित ट्यूटोरियल

- [Image Processing Java Library: Aspose.PSD के साथ लेयर इनवर्ट करें](/psd/java/advanced-image-manipulation/invert-adjustment-layer/)
- [Aspose.PSD for Java का उपयोग करके इमेज को ग्रेस्केल में बदलें](/psd/java/advanced-techniques/grayscale-image/)
- [Aspose.PSD for Java के साथ विशिष्ट कोण पर इमेज घुमाएँ](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}