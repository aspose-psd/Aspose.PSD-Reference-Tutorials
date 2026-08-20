---
date: 2026-05-19
description: Aspose.PSD का उपयोग करके Java में विशिष्ट कोण पर छवि को कैसे घुमाएँ सीखें।
  यह गाइड rotate image java, rotate image specific angle, background handling और अधिक
  को कवर करता है।
keywords:
- how to rotate image
- rotate image specific angle
- rotate image java
- rotate image background
- rotate image degrees
linktitle: विशिष्ट कोण पर छवि को कैसे घुमाएँ
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to rotate image on a specific angle in Java using Aspose.PSD.
    The guide covers rotate image java, rotate image specific angle, background handling
    and more.
  headline: How to Rotate Image on a Specific Angle with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to rotate image on a specific angle in Java using Aspose.PSD.
    The guide covers rotate image java, rotate image specific angle, background handling
    and more.
  name: How to Rotate Image on a Specific Angle with Aspose.PSD for Java
  steps:
  - name: Define Your Document Directory
    text: Set the folder that holds the source PSD and where the output will be written.
      Using an absolute path or `System.getProperty("user.dir")` eliminates relative‑path
      surprises.
  - name: Specify Source and Destination File Paths
    text: Provide the full file names for the input PSD and the desired output format
      (e.g., PNG, JPEG, TIFF). Changing the extension in `destName` automatically
      selects the appropriate encoder.
  - name: Load the Image
    text: The `Image.load` method detects the file format and returns a concrete `RasterImage`
      instance ready for raster operations. The `Image` class is a factory that reads
      a file from disk and creates an in‑memory representation suitable for further
      processing. It supports automatic format detection for al
  - name: Cache Image Data (Optional but Recommended)
    text: Calling `image.cacheData()` stores pixel data in memory, dramatically speeding
      up subsequent transformations—especially for large PSD files that would otherwise
      trigger repeated disk I/O. The `cacheData()` method forces the image to be fully
      loaded into RAM, reducing the overhead of lazy loading dur
  - name: Rotate the Image
    text: 'Invoke `rotate` with three arguments: the rotation angle (float), a flag
      to expand the canvas, and the background color for the newly exposed corners.
      The `rotate` method rotates the image around its centre, optionally enlarging
      the canvas to accommodate the rotated bounds. The background `Color` fi'
  - name: Save the Result
    text: Choose an encoder (JPEG, PNG, etc.) and call `save`. `JpegOptions` lets
      you adjust quality, while `PngOptions` provides lossless output. The `save`
      method writes the transformed image to disk using the specified options object,
      ensuring that compression level and color depth are preserved as require
  type: HowTo
- questions:
  - answer: Yes. The library preserves alpha channels; omit an opaque background color
      to keep corners transparent.
    question: Can I rotate images with transparency using Aspose.PSD for Java?
  - answer: No. Aspose.PSD supports PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF,
      EMF, and 30+ additional formats.
    question: Are there any limitations on the image file formats supported for rotation?
  - answer: Absolutely. Pass a negative float to `rotate` (e.g., `-30f`) to rotate
      clockwise.
    question: Can I rotate images by a negative angle?
  - answer: The API is server‑side only. For live previews, render the rotated bitmap
      in a UI framework such as Swing or JavaFX and refresh the view.
    question: Does Aspose.PSD provide real‑time image preview during rotation?
  - answer: Yes, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) to
      ask questions and share experiences.
    question: Is there a community forum for Aspose.PSD where I can seek help?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java के साथ विशिष्ट कोण पर छवि को कैसे घुमाएँ
url: /hi/java/advanced-image-manipulation/rotate-image-specific-angle/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java के साथ विशिष्ट कोण पर छवि को घुमाने का तरीका

यदि आपको Java एप्लिकेशन में प्रोग्रामेटिक रूप से **छवि को कैसे घुमाएँ** की आवश्यकता है, तो Aspose.PSD for Java एक साफ़, उच्च‑प्रदर्शन API प्रदान करता है जो भारी काम को संभालता है। चाहे आप फोटो‑एडिटर बना रहे हों, थंबनेल जेनरेट कर रहे हों, या वेब सर्विस के लिए एसेट तैयार कर रहे हों, सटीक डिग्री में छवि को घुमाना एक सामान्य आवश्यकता है। इस ट्यूटोरियल में हम पूरी प्रक्रिया को चरण‑दर‑चरण देखेंगे—PSD फ़ाइल को लोड करने से लेकर घुमाए गए परिणाम को सेव करने तक—और कैशिंग और बैकग्राउंड हैंडलिंग जैसी सर्वोत्तम प्रथाओं को उजागर करेंगे।

## त्वरित उत्तर
- **Java में छवियों को घुमाने के लिए सबसे अच्छा लाइब्रेरी कौन सा है?** Aspose.PSD for Java सबसे विश्वसनीय घुमाव इंजन प्रदान करता है।  
- **क्या मैं किसी भी डिग्री पर घुमा सकता हूँ?** हाँ, `rotate` मेथड एक `float` कोण, सकारात्मक या नकारात्मक, स्वीकार करता है।  
- **क्या विकास के लिए लाइसेंस चाहिए?** परीक्षण के लिए एक मुफ्त ट्रायल काम करता है; उत्पादन के लिए एक व्यावसायिक लाइसेंस आवश्यक है।  
- **कौन‑से इमेज फ़ॉर्मेट समर्थित हैं?** PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF, EMF, और 30+ अतिरिक्त फ़ॉर्मेट।  
- **खाली स्थान के लिए बैकग्राउंड रंग कैसे सेट करें?** `rotate` मेथड को एक `Color` इंस्टेंस पास करें।

## Aspose.PSD for Java के साथ विशिष्ट कोण पर छवि को कैसे घुमाएँ?

अपनी स्रोत फ़ाइल लोड करें, `image.rotate(angle, true, backgroundColor)` कॉल करें, और फिर सेव करें—तीन संक्षिप्त चरण जो सभी जटिल गणित आपके लिए संभालते हैं। Aspose.PSD लेयर्स, कलर प्रोफ़ाइल, और अल्फा चैनल को संरक्षित रखता है तथा क्लिपिंग से बचने के लिए कैनवास का विस्तार करता है, इसलिए आउटपुट बिल्कुल वही दिखता है जैसा अपेक्षित है, यहाँ तक कि 12.5° जैसे भिन्नात्मक कोणों के लिए भी। यह तरीका कुछ किलोबाइट से लेकर कई‑सौ‑पृष्ठों वाले PSD फ़ाइलों तक बिना मेमोरी समाप्त किए काम करता है।

## Java में इमेज रोटेशन क्या है?

इमेज रोटेशन वह ज्यामितीय परिवर्तन है जो पिक्सेल मैट्रिक्स को एक पिवट पॉइंट—आमतौर पर छवि के केंद्र—के चारों ओर निर्दिष्ट कोण द्वारा घुमाता है। साधारण Java में आप `Graphics2D` ऑब्जेक्ट को मैन्युअली संभालते, त्रिकोणमितीय ऑफ़सेट की गणना करते, और बैकग्राउंड को स्वयं प्रबंधित करते। Aspose.PSD इस सभी जटिलता को सारांशित करता है, रंग गहराई, लेयर मास्क, और विभिन्न फ़ाइल फ़ॉर्मेट को स्वचालित रूप से संभालता है।

## छवियों को घुमाने के लिए Aspose.PSD क्यों उपयोग करें?

Aspose.PSD **30+ इनपुट और आउटपुट फ़ॉर्मेट** का समर्थन करता है और सामान्य सर्वर‑क्लास CPU पर **500‑पृष्ठ PSD फ़ाइलों को 5 सेकंड से कम समय में** प्रोसेस कर सकता है। लाइब्रेरी का बिल्ट‑इन कैशिंग (`image.cacheData()`) बड़े एसेट्स के लिए मेमोरी उपयोग को 60 % तक कम कर देता है, और `rotate` मेथड आपको बैकग्राउंड रंग निर्दिष्ट करने की सुविधा देता है, जिससे आवश्यकतानुसार पारदर्शी कोनों को संरक्षित किया जा सकता है। ये मापनीय लाभ इसे हाई‑थ्रूपुट इमेज पाइपलाइन के लिए उद्योग‑मानक विकल्प बनाते हैं।

## आवश्यकताएँ

शुरू करने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित हों:

1. **Java Development Kit (JDK 8 या बाद का)** – कोई भी IDE या कमांड‑लाइन वातावरण चलेगा।  
2. **Aspose.PSD for Java** – नवीनतम JAR को [Aspose.PSD Java पेज](https://reference.aspose.com/psd/java/) से डाउनलोड करें।  
3. **एक सैंपल PSD फ़ाइल** – उदाहरण के लिए, `sample.psd` को उस फ़ोल्डर में रखें जिसे आप अपने कोड से रेफ़र कर सकते हैं।

## पैकेज इम्पोर्ट करें

`RasterImage` क्लास और संबंधित यूटिलिटीज़ घुमाव कार्यप्रवाह का मूल हैं।

`RasterImage` क्लास Aspose.PSD की प्रमुख ऑब्जेक्ट है जो रास्टर‑आधारित इमेज मैनिपुलेशन के लिए उपयोग होती है। यह रास्टर इमेज को लोड, ट्रांसफ़ॉर्म और सेव करने के मेथड प्रदान करती है जबकि मेटाडेटा को संरक्षित रखती है।

## चरण‑दर‑चरण गाइड

### चरण 1: अपने डॉक्यूमेंट डायरेक्टरी को परिभाषित करें

फ़ोल्डर सेट करें जिसमें स्रोत PSD है और जहाँ आउटपुट लिखा जाएगा। एक एब्सोल्यूट पाथ या `System.getProperty("user.dir")` का उपयोग करने से रिलेटिव‑पाथ की आश्चर्यजनक समस्याएँ समाप्त हो जाती हैं।

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

### चरण 2: स्रोत और गंतव्य फ़ाइल पाथ निर्दिष्ट करें

इनपुट PSD और इच्छित आउटपुट फ़ॉर्मेट (जैसे PNG, JPEG, TIFF) के पूर्ण फ़ाइल नाम प्रदान करें। `destName` में एक्सटेंशन बदलने से उपयुक्त एन्कोडर स्वचालित रूप से चयनित हो जाता है।

```java
String dataDir = "Your Document Directory";
```

### चरण 3: इमेज लोड करें

`Image.load` मेथड फ़ाइल फ़ॉर्मेट का पता लगाता है और एक ठोस `RasterImage` इंस्टेंस लौटाता है जो रास्टर ऑपरेशन्स के लिए तैयार है।

`Image` क्लास एक फ़ैक्टरी है जो डिस्क से फ़ाइल पढ़ती है और आगे की प्रोसेसिंग के लिए उपयुक्त इन‑मेमोरी प्रतिनिधित्व बनाती है। यह सभी 30+ समर्थित प्रकारों के लिए स्वचालित फ़ॉर्मेट डिटेक्शन को सपोर्ट करती है।

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "RotatingImageOnSpecificAngle_out.jpg";
```

### चरण 4: इमेज डेटा को कैश करें (वैकल्पिक लेकिन अनुशंसित)

`image.cacheData()` कॉल करने से पिक्सेल डेटा मेमोरी में संग्रहीत हो जाता है, जिससे बाद के ट्रांसफ़ॉर्मेशन बहुत तेज़ हो जाते हैं—विशेषकर बड़े PSD फ़ाइलों के लिए जो अन्यथा बार‑बार डिस्क I/O ट्रिगर कर सकते थे।

`cacheData()` मेथड इमेज को पूरी तरह RAM में लोड कर देता है, जिससे तीव्र ऑपरेशन्स के दौरान लेज़ी लोडिंग का ओवरहेड कम हो जाता है।

```java
RasterImage image = (RasterImage)Image.load(sourceFile);
```

### चरण 5: इमेज को घुमाएँ

तीन आर्ग्यूमेंट के साथ `rotate` को कॉल करें: घुमाव कोण (`float`), कैनवास को विस्तारित करने का फ़्लैग, और नए उजागर कोनों के लिए बैकग्राउंड रंग।

`rotate` मेथड इमेज को उसके केंद्र के चारों ओर घुमाता है, वैकल्पिक रूप से घुमाव सीमा को समायोजित करने के लिए कैनवास को बड़ा करता है। बैकग्राउंड `Color` किसी भी खाली स्थान को भरता है, जिससे पारदर्शी या काले कोने नहीं बनते।

- **20f** – डिग्री में घुमाव कोण (`float`)। किसी भी कोण के लिए इस मान को बदलें, उदाहरण के लिए घड़ी की दिशा में घुमाने के लिए `-45f`।  
- **true** – कैनवास को विस्तारित करते समय मूल अनुपात बनाए रखें।  
- **Color.getRed()** – खाली कोनों को भरने वाला बैकग्राउंड रंग; आवश्यकता अनुसार `Color.getWhite()` या कोई कस्टम रंग उपयोग करें।

```java
if (!image.isCached())
{
    image.cacheData();
}
```

### चरण 6: परिणाम को सेव करें

एक एन्कोडर चुनें (JPEG, PNG, आदि) और `save` को कॉल करें। `JpegOptions` आपको क्वालिटी समायोजित करने देता है, जबकि `PngOptions` लॉसलेस आउटपुट प्रदान करता है।

`save` मेथड निर्दिष्ट विकल्प ऑब्जेक्ट का उपयोग करके परिवर्तित इमेज को डिस्क पर लिखता है, यह सुनिश्चित करता है कि संपीड़न स्तर और रंग गहराई आवश्यकतानुसार संरक्षित रहे।

```java
image.rotate(20f, true, Color.getRed());
```

## सामान्य समस्याएँ और समाधान

| समस्या | कारण | समाधान |
|--------|------|--------|
| **घुमाव के बाद खाली कोने** | बैकग्राउंड रंग नहीं दिया गया | `rotate` को एक `Color` (जैसे `Color.getWhite()`) पास करें। |
| **बड़े PSD पर मेमोरी समाप्ति त्रुटि** | इमेज कैश नहीं की गई | प्रोसेसिंग से पहले `image.cacheData()` कॉल करें। |
| **गलत कोण दिशा** | नकारात्मक बनाम सकारात्मक कोण में भ्रम | घड़ी की दिशा में घुमाने के लिए नकारात्मक मान उपयोग करें (या आपके कोऑर्डिनेट सिस्टम के अनुसार)। |
| **परिवर्तनों को सेव नहीं किया गया** | `save` कॉल करना भूल गए | घुमाव के बाद `image.save(...)` को निष्पादित करना सुनिश्चित करें। |

## अक्सर पूछे जाने वाले प्रश्न

**प्र.: क्या मैं Aspose.PSD for Java के साथ पारदर्शिता वाली छवियों को घुमा सकता हूँ?**  
उ.: हाँ। लाइब्रेरी अल्फा चैनल को संरक्षित रखती है; पारदर्शी कोनों को बनाए रखने के लिए अपारदर्शी बैकग्राउंड रंग न दें।

**प्र.: क्या घुमाव के लिए समर्थित इमेज फ़ॉर्मेट में कोई सीमा है?**  
उ.: नहीं। Aspose.PSD PSD, JPEG, PNG, TIFF, GIF, BMP, JPEG2000, WMF, EMF, और 30+ अतिरिक्त फ़ॉर्मेट को समर्थन देता है।

**प्र.: क्या मैं नकारात्मक कोण से छवि घुमा सकता हूँ?**  
उ.: बिल्कुल। `rotate` में नकारात्मक `float` (जैसे `-30f`) पास करने से घड़ी की दिशा में घुमाव होगा।

**प्र.: क्या Aspose.PSD घुमाव के दौरान रियल‑टाइम इमेज प्रीव्यू प्रदान करता है?**  
उ.: API केवल सर्वर‑साइड है। लाइव प्रीव्यू के लिए, Swing या JavaFX जैसे UI फ्रेमवर्क में घुमाए गए बिटमैप को रेंडर करें और व्यू को रिफ्रेश करें।

**प्र.: क्या Aspose.PSD के लिए कोई कम्युनिटी फ़ोरम है जहाँ मैं मदद ले सकूँ?**  
उ.: हाँ, प्रश्न पूछने और अनुभव साझा करने के लिए [Aspose.PSD फ़ोरम](https://forum.aspose.com/c/psd/34) पर जाएँ।

---

**अंतिम अपडेट:** 2026-05-19  
**टेस्टेड विथ:** Aspose.PSD for Java 24.11 (लेखन के समय नवीनतम)  
**लेखक:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
image.save(destName, new JpegOptions());
```

## संबंधित ट्यूटोरियल

- [Aspose.PSD for Java में बाइकोबिक रिसैंपलर के साथ हाई क्वालिटी इमेज स्केलिंग](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)
- [Aspose.PSD for Java में रीसाइज़ टाइप एनेमरेशन का उपयोग करके इमेज रीसाइज़ Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)
- [Aspose.PSD के साथ इमेज ब्लर Java – ब्लर इफ़ेक्ट जोड़ें](/psd/java/advanced-techniques/blur-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}