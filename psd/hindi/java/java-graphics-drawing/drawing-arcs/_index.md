---
date: 2026-09-03
description: Aspose.PSD for Java का उपयोग करके java graphics draw arc सीखें। चरण‑दर‑चरण
  मार्गदर्शिका जिसमें कोड स्निपेट्स के साथ PSD फ़ाइलों में आर्क बनाने की प्रक्रिया
  बताई गई है।
keywords:
- java graphics draw arc
- how to draw arcs java
- Aspose.PSD arc drawing
lastmod: 2026-09-03
linktitle: Java में आर्क बनाना
og_description: Aspose.PSD for Java के साथ java graphics draw arc सीखें। यह ट्यूटोरियल
  आवश्यकताएँ, कोड चरण, और PSD फ़ाइलों में आर्क बनाने के टिप्स दिखाता है।
og_image_alt: Screenshot of a Java program drawing an arc using Aspose.PSD
og_title: Java में java graphics draw arc कैसे करें – Aspose.PSD गाइड
schemas:
- author: Aspose
  dateModified: '2026-09-03'
  description: Learn how to java graphics draw arc using Aspose.PSD for Java. Step‑by‑step
    guide with code snippets for creating arcs in PSD files.
  headline: How to java graphics draw arc in Java
  type: TechArticle
- description: Learn how to java graphics draw arc using Aspose.PSD for Java. Step‑by‑step
    guide with code snippets for creating arcs in PSD files.
  name: How to java graphics draw arc in Java
  steps:
  - name: set up your Java project
    text: Create a new Java project in your favourite IDE and add the Aspose.PSD JAR
      to the build path. Ensure the JAR is referenced correctly so the compiler can
      locate the library classes.
  - name: import required packages
    text: 'To begin, import the necessary packages from Aspose.PSD for Java: The `Pen`
      class defines the colour, width, and style of the line used to draw the arc.
      These imports expose the `PsdImage`, `Graphics`, `Pen`, and colour classes needed
      for arc drawing.'
  - name: initialise image and graphics objects
    text: 'Create an instance of `PsdImage` and obtain a `Graphics` object to draw
      on: Replace `"Your Document Directory"` with the folder where you want the output
      files saved.'
  - name: define arc parameters
    text: 'Set the geometry and style of the arc—its bounding rectangle, start angle,
      sweep angle, colour, and thickness: Adjust the values to match the visual design
      you need; for example, a 200 px radius arc starting at 45° and sweeping 270°.'
  - name: draw the arc and save the image
    text: 'Invoke `drawArc` on the `Graphics` object and persist the PSD (or export
      to another format): The `drawArc` method of the `Graphics` class renders an
      arc defined by a bounding rectangle, start angle, and sweep angle using the
      specified `Pen`. The snippet draws the arc on the canvas and saves it as a '
  type: HowTo
- questions:
  - answer: Yes, the library can draw rectangles, ellipses, lines, polygons, and custom
      paths using the same `Graphics` API.
    question: Can Aspose.PSD for Java handle other shapes besides arcs?
  - answer: Create a `Pen` with the desired `Color` and width, then pass that `Pen`
      instance to `drawArc`.
    question: How do I change the arc colour and thickness?
  - answer: Absolutely. Aspose.PSD supports PNG, JPEG, TIFF, GIF and many more – just
      change the file extension in the `save` method.
    question: Is it possible to export the PSD to a format other than BMP?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) for tutorials,
      code samples, and assistance from other developers.
    question: Where can I find more examples and community support?
  - answer: Yes, it can process files up to 2 GB and render arcs without loading the
      entire document into memory, thanks to its streaming architecture.
    question: Does the library work with large PSD files?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- arc drawing
- PSD manipulation
title: Java में java graphics draw arc कैसे बनाएं
url: /hi/java/java-graphics-drawing/drawing-arcs/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java में ग्राफ़िक्स आर्क कैसे बनाएं

## परिचय
इस ट्यूटोरियल में आप **java graphics draw arc** को Aspose.PSD for Java लाइब्रेरी का उपयोग करके सीखेंगे। प्रोग्रामेटिक रूप से आर्क बनाना कस्टम UI कॉम्पोनेन्ट्स, डेटा विज़ुअलाइज़ेशन और ग्राफ़िक‑रिच रिपोर्ट्स के लिए सामान्य आवश्यकता है। Aspose.PSD for Java आपको PSD (Photoshop Document) फ़ाइलों पर पूर्ण नियंत्रण देता है, जिससे आप Photoshop स्थापित किए बिना इमेज बना, संपादित और एक्सपोर्ट कर सकते हैं।

## त्वरित उत्तर
- **कौन सी लाइब्रेरी Java में आर्क ड्रॉ करने का समर्थन करती है?** Aspose.PSD for Java.  
- **प्रोडक्शन उपयोग के लिए लाइसेंस चाहिए?** हाँ, गैर‑ट्रायल डिप्लॉयमेंट के लिए एक कमर्शियल लाइसेंस आवश्यक है।  
- **मैं किन फ़ाइल फ़ॉर्मैट्स में एक्सपोर्ट कर सकता हूँ?** BMP, PNG, JPEG, TIFF, GIF और अधिक।  
- **क्या मैं आर्क की मोटाई और रंग बदल सकता हूँ?** हाँ, `drawArc` को पास किए गए `Pen` ऑब्जेक्ट के माध्यम से।  
- **क्या API Java 8 और बाद के संस्करणों के साथ संगत है?** Java 8‑21 के साथ पूरी तरह संगत।

## Java ग्राफ़िक्स ड्रॉ आर्क क्या है?
`java graphics draw arc` का अर्थ है Java की ड्रॉइंग API का उपयोग करके ग्राफ़िक्स सतह पर एक कर्व्ड लाइन सेगमेंट—आर्क—को रेंडर करना। Aspose.PSD के संदर्भ में, यह ऑपरेशन एक `Graphics` ऑब्जेक्ट पर किया जाता है जो PSD फ़ाइल के भीतर एक लेयर का प्रतिनिधित्व करता है।

## आर्क बनाने के लिए Aspose.PSD for Java का उपयोग क्यों करें?
Aspose.PSD **50+** इमेज और डॉक्यूमेंट फ़ॉर्मैट्स को सपोर्ट करता है, **2 GB** तक के PSD फ़ाइलों को संभाल सकता है, और पूरी फ़ाइल को मेमोरी में लोड किए बिना सैकड़ों पेज वाले डॉक्यूमेंट्स को प्रोसेस करता है। यह परफ़ॉर्मेंस सर्वर‑साइड ग्राफ़िक्स जेनरेशन के लिए आदर्श बनाता है जहाँ गति और मेमोरी उपयोग महत्वपूर्ण होते हैं।

## पूर्वापेक्षाएँ
1. **Java Development Environment** – Java को [Oracle की वेबसाइट](https://www.oracle.com/java/) से इंस्टॉल करें।  
2. **Aspose.PSD for Java Library** – नवीनतम JAR को [डाउनलोड पेज](https://releases.aspose.com/psd/java/) से डाउनलोड करें। प्रदान किए गए निर्देशों का पालन करके JAR को अपने प्रोजेक्ट के क्लासपाथ में जोड़ें।

## Java में ग्राफ़िक्स आर्क कैसे बनाएं?
एक नया `PsdImage` लोड करें, उसका `Graphics` सतह प्राप्त करें, इच्छित रंग और मोटाई के साथ `Pen` को कॉन्फ़िगर करें, और `drawArc` को कॉल करें। यह संक्षिप्त क्रम आर्क बनाता है और एक ही मेथड चेन में परिणाम सहेजता है। बाउंडिंग रेक्टैंगल और एंगल पैरामीटर्स को समायोजित करके आप आकार, स्थिति और स्विप को अपने डिज़ाइन आवश्यकताओं के अनुसार नियंत्रित कर सकते हैं।

### चरण 1: अपना Java प्रोजेक्ट सेट अप करें
अपने पसंदीदा IDE में एक नया Java प्रोजेक्ट बनाएं और Aspose.PSD JAR को बिल्ड पाथ में जोड़ें। सुनिश्चित करें कि JAR सही तरीके से रेफ़रेंस किया गया है ताकि कंपाइलर लाइब्रेरी क्लासेज़ को ढूँढ सके।

### चरण 2: आवश्यक पैकेज इम्पोर्ट करें
शुरू करने के लिए, Aspose.PSD for Java से आवश्यक पैकेज इम्पोर्ट करें:
`Pen` क्लास आर्क ड्रॉ करने के लिए उपयोग की जाने वाली लाइन का रंग, चौड़ाई और स्टाइल परिभाषित करती है।
```java
import com.aspose.psd.Color;
import static com.aspose.psd.ColorAdjustType.Pen;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```  
ये इम्पोर्ट्स `PsdImage`, `Graphics`, `Pen` और रंग क्लासेज़ को उजागर करते हैं जो आर्क ड्रॉ करने के लिए आवश्यक हैं।

### चरण 3: इमेज और ग्राफ़िक्स ऑब्जेक्ट्स को इनिशियलाइज़ करें
`PsdImage` का एक इंस्टेंस बनाएं और ड्रॉ करने के लिए एक `Graphics` ऑब्जेक्ट प्राप्त करें:
```java
String dataDir = "Your Document Directory";
// Initialize PsdImage object
PsdImage image = new PsdImage(100, 100);
// Initialize Graphics object and clear surface
Graphics graphics = new Graphics(image);
graphics.clear(Color.getYellow());
```  
`"Your Document Directory"` को उस फ़ोल्डर से बदलें जहाँ आप आउटपुट फ़ाइलें सहेजना चाहते हैं।

### चरण 4: आर्क पैरामीटर निर्धारित करें
आर्क की ज्योमेट्री और स्टाइल सेट करें—बाउंडिंग रेक्टैंगल, स्टार्ट एंगल, स्विप एंगल, रंग और मोटाई:
```java
int width = 100;
int height = 200;
int startAngle = 45;
int sweepAngle = 270;
```  
अपनी विज़ुअल डिज़ाइन के अनुसार मान समायोजित करें; उदाहरण के लिए, 45° पर शुरू होने वाला 200 px रेडियस वाला आर्क जो 270° तक स्विप करता है।

### चरण 5: आर्क बनाएं और इमेज सहेजें
`Graphics` ऑब्जेक्ट पर `drawArc` को इनवोक करें और PSD (या किसी अन्य फ़ॉर्मैट) में सहेजें:
`Graphics` क्लास का `drawArc` मेथड बाउंडिंग रेक्टैंगल, स्टार्ट एंगल और स्विप एंगल द्वारा परिभाषित आर्क को निर्दिष्ट `Pen` का उपयोग करके रेंडर करता है।
```java
// Draw arc with specified Pen object (black color) and parameters
graphics.drawArc(new Pen(Color.getBlack()), 0, 0, width, height, startAngle, sweepAngle);
// Save the image in BMP format
String outputPath = dataDir + "Arc.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
image.save(outputPath, saveOptions);
```  
यह स्निपेट कैनवास पर आर्क ड्रॉ करता है और इसे BMP फ़ाइल के रूप में सहेजता है। `outputPath` में फ़ाइल एक्सटेंशन बदलकर PNG, JPEG या TIFF में एक्सपोर्ट करें।

## आम समस्याएँ और ट्रबलशूटिंग
- **गलत एंगल यूनिट्स** – Aspose.PSD एंगल को डिग्री में अपेक्षित करता है, रैडियन नहीं। रैडियन देने से अप्रत्याशित परिणाम मिलेंगे।  
- **Pen की मोटाई बहुत बड़ी** – बहुत मोटी पेन से आर्क इमेज की सीमाओं से बाहर जा सकता है; मोटाई घटाएँ या कैनवास बड़ा करें।  
- **फ़ाइल पाथ समस्याएँ** – एब्सोल्यूट पाथ का उपयोग करें या सुनिश्चित करें कि वर्किंग डायरेक्टरी में लिखने की अनुमति हो, ताकि `IOException` से बचा जा सके।

## अक्सर पूछे जाने वाले प्रश्न

**प्रश्न: क्या Aspose.PSD for Java आर्क के अलावा अन्य शैप्स भी ड्रॉ कर सकता है?**  
उत्तर: हाँ, लाइब्रेरी `Graphics` API का उपयोग करके रेक्टैंगल, एलिप्स, लाइन, पॉलीगॉन और कस्टम पाथ्स भी ड्रॉ कर सकती है।

**प्रश्न: मैं आर्क का रंग और मोटाई कैसे बदलूँ?**  
उत्तर: इच्छित `Color` और चौड़ाई के साथ एक `Pen` बनाएं, फिर उस `Pen` इंस्टेंस को `drawArc` को पास करें।

**प्रश्न: क्या PSD को BMP के अलावा किसी अन्य फ़ॉर्मैट में एक्सपोर्ट करना संभव है?**  
उत्तर: बिल्कुल। Aspose.PSD PNG, JPEG, TIFF, GIF आदि को सपोर्ट करता है – बस `save` मेथड में फ़ाइल एक्सटेंशन बदल दें।

**प्रश्न: अधिक उदाहरण और कम्युनिटी सपोर्ट कहाँ मिल सकता है?**  
उत्तर: ट्यूटोरियल, कोड सैंपल और अन्य डेवलपर्स की मदद के लिए [Aspose.PSD फ़ोरम](https://forum.aspose.com/c/psd/34) देखें।

**प्रश्न: क्या लाइब्रेरी बड़े PSD फ़ाइलों के साथ काम करती है?**  
उत्तर: हाँ, यह 2 GB तक की फ़ाइलों को प्रोसेस कर सकती है और आर्क को बिना पूरे डॉक्यूमेंट को मेमोरी में लोड किए रेंडर करती है, इसके स्ट्रीमिंग आर्किटेक्चर के कारण।

---

**अंतिम अपडेट:** 2026-09-03  
**परीक्षित संस्करण:** Aspose.PSD for Java 24.11  
**लेखक:** Aspose

## संबंधित ट्यूटोरियल

- [Draw and Save a Rectangle in a PSD using Aspose.PSD for Java](/psd/java/basic-image-operations/simple-drawing/)
- [Resize Image with Aspose.PSD for Java – Draw Shapes & Basic Image Operations](/psd/java/basic-image-operations/)
- [How to Change Stroke Color Java Using Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}