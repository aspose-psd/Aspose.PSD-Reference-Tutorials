---
date: 2026-09-08
description: Aspose.PSD for Java का उपयोग करके Java में bezier curves बनाना सीखें।
  चरण‑दर‑चरण निर्देश, आवश्यकताएँ, और कोड‑फ्री उदाहरणों का पालन करें।
keywords:
- how to draw bezier
- how to use pen
- bezier curve example java
- java graphics draw curve
lastmod: 2026-09-08
linktitle: Java में Bezier Curves बनाना
og_description: Aspose.PSD का उपयोग करके Java में bezier curves कैसे बनाएं। यह गाइड
  आवश्यकताएँ, चरण‑दर‑चरण ड्रॉइंग, और उच्च‑रिज़ॉल्यूशन इमेजेज के लिए टिप्स को कवर करता
  है।
og_image_alt: Screenshot of a Java application rendering a Bezier curve with Aspose.PSD
og_title: Aspose.PSD लाइब्रेरी के साथ Java में bezier curves कैसे बनाएं
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to draw bezier curves in Java using Aspose.PSD for Java.
    Follow step‑by‑step instructions, prerequisites, and code‑free examples.
  headline: How to draw bezier curves in Java with Aspose.PSD library
  type: TechArticle
- description: Learn how to draw bezier curves in Java using Aspose.PSD for Java.
    Follow step‑by‑step instructions, prerequisites, and code‑free examples.
  name: How to draw bezier curves in Java with Aspose.PSD library
  steps:
  - name: create an image instance
    text: 'The `PsdImage` class is Aspose.PSD''s top‑level object that represents
      a single PSD file in memory. First, you need to create an instance of the `PsdImage`
      class, which represents a PSD image in memory. Explanation: - `PsdImage` is
      instantiated with width and height parameters (100 × 100 pixels in th'
  - name: initialize graphics context
    text: 'The `Graphics` class provides drawing capabilities on a `PsdImage`. Next,
      initialize an instance of the `Graphics` class to perform drawing operations
      on the image. Explanation: - `Graphics` object is initialized with the `image`
      instance, allowing drawing operations.'
  - name: clear the graphics surface
    text: 'The `clear()` method sets the background colour of the graphics surface.
      Clear the graphics surface using a specific background colour, here `Color.getYellow()`.
      Explanation: - `clear()` method sets the background colour of the graphics surface.'
  - name: initialize pen for drawing
    text: 'The `Pen` object defines stroke attributes such as colour and width. Set
      up a `Pen` object with properties like colour and width to define how the curve
      will be drawn. Explanation: - `Pen` is initialized with black colour and 3‑pixel
      width.'
  - name: define bezier curve parameters
    text: 'Control points determine the curvature. Specify the control points and
      end points for the Bezier curve. Explanation: - `startX`, `startY`: Starting
      point of the curve. - `controlX1`, `controlY1`: First control point. - `controlX2`,
      `controlY2`: Second control point. - `endX`, `endY`: Ending point of'
  - name: draw the bezier curve
    text: 'The `drawBezier()` method renders the curve using the supplied `Pen` and
      points. Use the `drawBezier()` method to draw the Bezier curve onto the image
      using the previously defined `Pen` and control points. Explanation: - `drawBezier()`
      method draws the curve with specified parameters using the `blac'
  - name: save the image
    text: Saving the image persists the drawing to disk. Save the drawn image to a
      BMP file format.
  type: HowTo
- questions:
  - answer: Yes, repeat the `drawBezier()` call inside a loop, updating the control
      points for each curve.
    question: Can I draw multiple Bezier curves in the same image?
  - answer: Modify the `Pen` object's colour property (`Color.getBlack()` in the example)
      before invoking `drawBezier()`.
    question: How can I change the colour of the Bezier curve?
  - answer: Yes, Aspose.PSD for Java supports high‑resolution images with efficient
      memory management, handling files larger than 500 MB without loading the entire
      file into memory.
    question: Is Aspose.PSD for Java suitable for high‑resolution images?
  - answer: Yes, Aspose.PSD for Java supports exporting to PNG, JPEG, TIFF, and many
      other raster formats.
    question: Can I export the image to formats other than BMP?
  - answer: Visit the [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/)
      for comprehensive guides and code samples.
    question: Where can I find more examples and documentation?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- drawing bezier
- Aspose.PSD
- Java graphics
- curve drawing
title: Aspose.PSD लाइब्रेरी के साथ Java में bezier curves कैसे बनाएं
url: /hi/java/java-graphics-drawing/drawing-bezier-curves/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java में Aspose.PSD लाइब्रेरी के साथ बीज़ियर कर्व कैसे बनाएं

## परिचय
यदि आपको Java डेस्कटॉप या सर्वर एप्लिकेशन में **बीज़ियर कैसे बनाएं** आकारों के बारे में जानना है, तो Aspose.PSD for Java आपको एक साफ़, मेमोरी‑कुशल API प्रदान करता है। इस ट्यूटोरियल में आप देखेंगे कि PSD कैनवास कैसे बनाएं, ड्राइंग पेन को कॉन्फ़िगर करें, कंट्रोल पॉइंट्स निर्धारित करें, और एक स्मूथ बीज़ियर कर्व रेंडर करें—बिना किसी लो‑लेवल पिक्सेल मैनिपुलेशन कोड के।

## त्वरित उत्तर
- **ड्राइंग को कौन सी लाइब्रेरी संभालती है?** Aspose.PSD for Java.
- **कोड की कितनी पंक्तियों की आवश्यकता है?** लगभग दस संक्षिप्त स्टेटमेंट्स।
- **क्या मैं कर्व का रंग बदल सकता हूँ?** हाँ, `Pen` colour प्रॉपर्टी को समायोजित करके।
- **क्या हाई‑रेज़ोल्यूशन आउटपुट समर्थित है?** हाँ, 500 MB तक की फाइलें बिना पूरी मेमोरी लोड किए।
- **क्या मुझे व्यावसायिक लाइसेंस चाहिए?** विकास के लिए फ्री ट्रायल काम करता है; उत्पादन के लिए लाइसेंस आवश्यक है।

## बीज़ियर कर्व क्या है?
बीज़ियर कर्व एक गणितीय रूप से परिभाषित स्मूथ लाइन है जिसे दो या अधिक बिंदुओं द्वारा नियंत्रित किया जाता है। यह वेक्टर ग्राफ़िक्स, एनीमेशन, और UI डिज़ाइन में एलेगेंट, स्केलेबल आकार बनाने के लिए व्यापक रूप से उपयोग किया जाता है। कर्व का आकार उसके स्टार्ट पॉइंट, एंड पॉइंट, और एक या अधिक कंट्रोल पॉइंट्स द्वारा निर्धारित होता है, जो कर्वेचर को प्रभावित करते हैं, जिससे डिज़ाइनर सरल पैरामीटर्स के साथ जटिल पाथ मॉडल कर सकते हैं।

## बीज़ियर कर्व ड्रॉ करने के लिए Aspose.PSD क्यों उपयोग करें?
Aspose.PSD **30+ इमेज फॉर्मैट्स** को सपोर्ट करता है और **सैकड़ों‑पेज PSD फाइल्स** को पूरी RAM में लोड किए बिना प्रोसेस कर सकता है। लाइब्रेरी का `drawBezier()` मेथड ऑटोमैटिकली एंटी‑एलियासिंग और कलर मैनेजमेंट को हैंडल करता है, जिससे सामान्य 100 × 100 कैनवास के लिए एक सेकंड से भी कम समय में पिक्सेल‑परफेक्ट रिज़ल्ट मिलते हैं।

## पूर्वापेक्षाएँ
1. **Java Development Kit (JDK)** – कोई भी नवीनतम संस्करण (8 या बाद का) स्थापित और कॉन्फ़िगर किया हुआ।  
2. **Aspose.PSD for Java JAR** – Aspose.PSD for Java लाइब्रेरी को [Aspose.PSD Java download](https://releases.aspose.com/psd/java/) से डाउनलोड करें और इसे अपने प्रोजेक्ट के classpath में जोड़ें।  
3. **Integrated Development Environment (IDE)** – जैसे Eclipse, IntelliJ IDEA, या NetBeans, जो JDK के साथ सेट अप हो।

## पैकेज इम्पोर्ट करें
निम्नलिखित इम्पोर्ट्स Aspose.PSD क्लासेज़ को लाते हैं जो इमेज निर्माण और ड्राइंग के लिए आवश्यक हैं।
```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```

## Java में बीज़ियर कर्व कैसे बनाएं?
एक खाली `PsdImage` लोड करें, एक `Graphics` ऑब्जेक्ट बनाएं, एक `Pen` कॉन्फ़िगर करें, स्टार्ट, कंट्रोल और एंड पॉइंट्स निर्धारित करें, `drawBezier()` कॉल करें, और अंत में इमेज को सेव करें। यह क्रम एक स्मूथ कर्व बनाता है और किसी मैनुअल पिक्सेल गणना की आवश्यकता नहीं होती।

### चरण 1: इमेज इंस्टेंस बनाएं
`PsdImage` क्लास Aspose.PSD की टॉप‑लेवल ऑब्जेक्ट है जो मेमोरी में एकल PSD फ़ाइल का प्रतिनिधित्व करती है। सबसे पहले, आपको `PsdImage` क्लास का एक इंस्टेंस बनाना होगा, जो मेमोरी में एक PSD इमेज का प्रतिनिधित्व करता है।
```java
String dataDir = "Your Document Directory";
Image image = new PsdImage(100, 100);
```
व्याख्या:
- `PsdImage` को चौड़ाई और ऊँचाई पैरामीटर (इस उदाहरण में 100 × 100 पिक्सेल) के साथ इंस्टैंशिएट किया जाता है।

### चरण 2: ग्राफ़िक्स कॉन्टेक्स्ट इनिशियलाइज़ करें
`Graphics` क्लास `PsdImage` पर ड्राइंग क्षमताएँ प्रदान करती है। अब, इमेज पर ड्राइंग ऑपरेशन्स करने के लिए `Graphics` क्लास का एक इंस्टेंस इनिशियलाइज़ करें।
```java
Graphics graphics = new Graphics(image);
```
व्याख्या:
- `Graphics` ऑब्जेक्ट को `image` इंस्टेंस के साथ इनिशियलाइज़ किया जाता है, जिससे ड्राइंग ऑपरेशन्स संभव होते हैं।

### चरण 3: ग्राफ़िक्स सतह को साफ़ करें
`clear()` मेथड ग्राफ़िक्स सतह का बैकग्राउंड रंग सेट करता है। यहाँ `Color.getYellow()` का उपयोग करके ग्राफ़िक्स सतह को एक विशिष्ट बैकग्राउंड रंग से साफ़ करें।
```java
graphics.clear(Color.getYellow());
```
व्याख्या:
- `clear()` मेथड ग्राफ़िक्स सतह का बैकग्राउंड रंग सेट करता है।

### चरण 4: ड्राइंग के लिए पेन इनिशियलाइज़ करें
`Pen` ऑब्जेक्ट स्ट्रोक एट्रिब्यूट्स जैसे रंग और चौड़ाई को परिभाषित करता है। कर्व को ड्रॉ करने के लिए रंग और चौड़ाई जैसी प्रॉपर्टीज़ के साथ `Pen` ऑब्जेक्ट सेट अप करें।
```java
Pen blackPen = new Pen(Color.getBlack(), 3);
```
व्याख्या:
- `Pen` को काले रंग और 3‑पिक्सेल चौड़ाई के साथ इनिशियलाइज़ किया जाता है।

### चरण 5: बीज़ियर कर्व पैरामीटर परिभाषित करें
कंट्रोल पॉइंट्स कर्वेचर को निर्धारित करते हैं। बीज़ियर कर्व के लिए कंट्रोल पॉइंट्स और एंड पॉइंट्स निर्दिष्ट करें।
```java
float startX = 10, startY = 25;
float controlX1 = 20, controlY1 = 5;
float controlX2 = 55, controlY2 = 10;
float endX = 90, endY = 25;
```
व्याख्या:
- `startX`, `startY`: कर्व का प्रारंभ बिंदु।  
- `controlX1`, `controlY1`: पहला कंट्रोल पॉइंट।  
- `controlX2`, `controlY2`: दूसरा कंट्रोल पॉइंट।  
- `endX`, `endY`: कर्व का समाप्ति बिंदु।

### चरण 6: बीज़ियर कर्व ड्रॉ करें
`drawBezier()` मेथड निर्दिष्ट पैरामीटरों के साथ `blackPen` का उपयोग करके कर्व ड्रॉ करता है। पहले परिभाषित `Pen` और कंट्रोल पॉइंट्स का उपयोग करके इमेज पर बीज़ियर कर्व ड्रॉ करने के लिए `drawBezier()` मेथड का उपयोग करें।
```java
graphics.drawBezier(blackPen, startX, startY, controlX1, controlY1, controlX2, controlY2, endX, endY);
```
व्याख्या:
- `drawBezier()` मेथड निर्दिष्ट पैरामीटरों के साथ `blackPen` का उपयोग करके कर्व ड्रॉ करता है।

### चरण 7: इमेज सहेजें
इमेज को सेव करने से ड्रॉ किया गया कंटेंट डिस्क पर स्थायी रूप से लिखा जाता है। BMP फॉर्मैट में ड्रॉ की गई इमेज को सेव करें।
```java
String outpath = dataDir + "Bezier.bmp";
BmpOptions saveOptions = new BmpOptions();
image.save(outpath, saveOptions);
```

## सामान्य समस्याएँ और समाधान
- **कर्व सपाट दिख रहा है** – सुनिश्चित करें कि कंट्रोल पॉइंट्स प्रारंभ और समाप्ति बिंदुओं के साथ कोलाइनियर नहीं हैं। थोड़ा सा ऑफ़सेट करके कर्वेचर बनाएं।  
- **रंग नहीं बदल रहा है** – `drawBezier()` कॉल करने से पहले `Pen` का रंग बदलना सुनिश्चित करें।  
- **बड़े कैनवास पर मेमोरी समाप्ति त्रुटियाँ** – स्ट्रीमिंग सक्षम करने वाले `PsdImage` कंस्ट्रक्टर्स का उपयोग करें, या ड्राइंग को टाइल्स में विभाजित करें।

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या मैं एक ही इमेज में कई बीज़ियर कर्व ड्रॉ कर सकता हूँ?**  
A: हाँ, लूप के भीतर `drawBezier()` कॉल को दोहराएँ, प्रत्येक कर्व के लिए कंट्रोल पॉइंट्स को अपडेट करें।

**Q: मैं बीज़ियर कर्व का रंग कैसे बदल सकता हूँ?**  
A: `drawBezier()` को कॉल करने से पहले `Pen` ऑब्जेक्ट की colour प्रॉपर्टी (`Color.getBlack()` उदाहरण में) को बदलें।

**Q: क्या Aspose.PSD for Java हाई‑रेज़ोल्यूशन इमेज के लिए उपयुक्त है?**  
A: हाँ, Aspose.PSD for Java कुशल मेमोरी प्रबंधन के साथ हाई‑रेज़ोल्यूशन इमेज को सपोर्ट करता है, 500 MB से बड़े फाइलों को पूरी फ़ाइल को मेमोरी में लोड किए बिना संभालता है।

**Q: क्या मैं इमेज को BMP के अलावा अन्य फॉर्मैट में एक्सपोर्ट कर सकता हूँ?**  
A: हाँ, Aspose.PSD for Java PNG, JPEG, TIFF और कई अन्य रास्टर फॉर्मैट में एक्सपोर्ट करने का समर्थन करता है।

**Q: मैं अधिक उदाहरण और दस्तावेज़ीकरण कहाँ पा सकता हूँ?**  
A: व्यापक गाइड और कोड सैंपल के लिए [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/) देखें।

---

**अंतिम अपडेट:** 2026-09-08  
**परीक्षण किया गया:** Aspose.PSD for Java 24.11  
**लेखक:** Aspose

## संबंधित ट्यूटोरियल

- [Aspose.PSD for Java के साथ इमेज रिसाइज़ करें – शैप्स ड्रॉ करें और बेसिक इमेज ऑपरेशन्स](/psd/java/basic-image-operations/)
- [Aspose.PSD for Java का उपयोग करके PSD में रेक्टैंगल ड्रॉ और सेव करें](/psd/java/basic-image-operations/simple-drawing/)
- [Aspose.PSD का उपयोग करके Java में स्ट्रोक रंग कैसे बदलें](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}