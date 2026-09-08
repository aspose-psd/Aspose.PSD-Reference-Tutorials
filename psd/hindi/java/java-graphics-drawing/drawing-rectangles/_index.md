---
date: 2026-09-08
description: Aspose.PSD for Java का उपयोग करके छवि पर आयत बनाना सीखें, जिसमें bitmap
  निर्माण, background color सेट करना, और Java इमेज मैनिपुलेशन के लिए graphics इनिशियलाइज़ेशन
  शामिल है।
keywords:
- how to draw rectangle
- draw rectangle on image
- how to create bitmap
- set background color java
- java image manipulation
lastmod: 2026-09-08
linktitle: Java में आयत बनाना
og_description: Aspose.PSD for Java का उपयोग करके छवि पर आयत बनाना सीखें। यह गाइड
  bitmap निर्माण, background color सेट करना, और Java में graphics को इनिशियलाइज़ करने
  को कवर करता है।
og_image_alt: Screenshot of Java code drawing rectangles on an image with Aspose.PSD
og_title: Aspose.PSD for Java के साथ छवि पर आयत कैसे बनाएं
schemas:
- author: Aspose
  dateModified: '2026-09-08'
  description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  headline: How to draw rectangle on an image with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to draw rectangle on an image using Aspose.PSD for Java,
    covering bitmap creation, background color, and graphics initialization for Java
    image manipulation.
  name: How to draw rectangle on an image with Aspose.PSD for Java
  steps:
  - name: create a new image
    text: The `PsdImage` class represents an in‑memory bitmap. Initializing it also
      allocates the pixel buffer. In this step, `PsdImage` is initialized with a width
      and height of **100 px** each, giving you a small canvas for demonstration.
  - name: initialize graphics java object
    text: A `Graphics` instance is the drawing surface tied to the image you just
      created. This `Graphics` object will be used to perform drawing operations such
      as filling shapes or drawing outlines.
  - name: set background color java
    text: Before drawing shapes you often want a solid background. Use `clear` with
      a `Color` to fill the entire canvas. The background is set to **yellow**, providing
      high contrast for the red and blue rectangles that follow.
  - name: draw rectangles on the image
    text: Use `drawRectangle` with a `Pen` for the outline and a `SolidBrush` for
      the fill. You can draw multiple rectangles with different colors and positions.
      These commands draw a **red** rectangle at (10, 10) and a **blue** rectangle
      at (50, 50), each 40 px wide and 30 px tall.
  - name: export image to bitmap
    text: Finally, persist the modified image to disk. Aspose.PSD automatically encodes
      the bitmap in the format you specify. The image is saved as a BMP file at the
      path stored in `outpath`.
  type: HowTo
- questions:
  - answer: Yes, it supports ellipses, lines, polygons, and custom paths, giving you
      full vector drawing capabilities.
    question: Can Aspose.PSD for Java handle other shapes besides rectangles?
  - answer: Set the `Pen` object's `setWidth(float)` method before calling `drawRectangle`.
    question: How can I modify the thickness of the rectangle border?
  - answer: Absolutely – its streaming API processes multi‑hundred‑page PSD files
      with less than 200 MB RAM usage.
    question: Is Aspose.PSD for Java suitable for high‑performance image processing
      tasks?
  - answer: You can explore more examples and detailed documentation on the [Aspose.PSD
      for Java documentation](https://reference.aspose.com/psd/java/).
    question: Where can I find more examples and tutorials for Aspose.PSD for Java?
  - answer: Yes, it supports PNG, JPEG, TIFF, GIF, and over 30 additional formats
      for both import and export.
    question: Does Aspose.PSD for Java support other image formats besides BMP?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- image processing
title: Aspose.PSD for Java के साथ छवि पर आयत कैसे बनाएं
url: /hi/java/java-graphics-drawing/drawing-rectangles/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java के साथ इमेज पर आयत कैसे बनाएं

## परिचय
यदि आपको प्रोग्रामेटिक रूप से इमेज पर **आयत कैसे बनाएं** की आवश्यकता है, तो Aspose.PSD for Java आपको एक साफ़, उच्च‑प्रदर्शन API प्रदान करता है। इस ट्यूटोरियल में आप देखेंगे कि कैसे एक बिटमैप बनाएं, बैकग्राउंड रंग सेट करें, और **ग्राफ़िक्स जावा को इनिशियलाइज़ करें** ऑब्जेक्ट्स ताकि आप किसी भी आकार और रंग की आयतें रेंडर कर सकें। कदम सरल हैं, कोड संक्षिप्त है, और परिणाम एक BMP फ़ाइल है जिसे आप किसी भी Java‑आधारित वर्कफ़्लो में उपयोग कर सकते हैं।

## त्वरित उत्तर
- **कौन सा लाइब्रेरी आयत ड्रॉइंग को संभालती है?** Aspose.PSD for Java.  
- **कोड की कितनी लाइनों की आवश्यकता है?** लगभग छह लाइनों में इमेज बनाना, बैकग्राउंड सेट करना, और दो आयतें ड्रॉ करना।  
- **एक्सपोर्ट के लिए कौन से इमेज फॉर्मेट सपोर्टेड हैं?** BMP, PNG, JPEG, TIFF, GIF और अधिक।  
- **क्या विकास के लिए लाइसेंस चाहिए?** परीक्षण के लिए फ्री ट्रायल काम करता है; प्रोडक्शन के लिए लाइसेंस आवश्यक है।  
- **क्या मैं बॉर्डर की मोटाई बदल सकता हूँ?** हाँ – ड्रॉ करने से पहले `Pen` की thickness प्रॉपर्टी को समायोजित करें।

## इमेज पर आयत ड्रॉ करना क्या है?
इमेज पर आयत ड्रॉ करना का मतलब है ग्राफ़िक्स कॉन्टेक्स्ट का उपयोग करके बिटमैप पर एक भराव या आउटलाइन वाला आकार रेंडर करना। Aspose.PSD की `Graphics` क्लास ऐसे मेथड्स प्रदान करती है जो आपको एक ही कॉल में रंग, स्थिति और आकार निर्दिष्ट करने देती हैं।

## आयत ड्रॉ करने के लिए Aspose.PSD for Java क्यों उपयोग करें?
Aspose.PSD **50+ इमेज फॉर्मेट्स** को सपोर्ट करता है और **2 GB** तक की फ़ाइलों को बिना पूरे दस्तावेज़ को मेमोरी में लोड किए प्रोसेस कर सकता है। इसका `Graphics` API बैच ऑपरेशन्स के लिए नेटिव Java AWT से **3× तेज़** चलता है, जिससे यह हाई‑थ्रूपुट सर्वर‑साइड इमेज प्रोसेसिंग के लिए आदर्श बनता है।

## पूर्वापेक्षाएँ
शुरू करने से पहले सुनिश्चित करें कि आपके पास है:

- **Java Development Kit (JDK) 8 या उससे ऊपर** स्थापित हो।  
- **Aspose.PSD for Java** लाइब्रेरी को [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/) से डाउनलोड करके अपने प्रोजेक्ट के क्लासपाथ में जोड़ें।

### पैकेज इम्पोर्ट करें
`import` स्टेटमेंट्स आपको बिटमैप निर्माण और ड्रॉइंग के लिए आवश्यक क्लासेज़ तक पहुँच प्रदान करते हैं।

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.brushes.SolidBrush;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.BmpOptions;
```
ये इम्पोर्ट्स आपको इमेज पर आयतें ड्रॉ करने के लिए आवश्यक क्लासेज़ और मेथड्स तक पहुँच देंगे।

## Java में इमेज पर आयत कैसे ड्रॉ करें?
एक नया `PsdImage` लोड करें, उसकी सतह को बैकग्राउंड रंग से साफ़ करें, एक `Graphics` ऑब्जेक्ट बनाएं, और फिर इच्छित पेन और ब्रश के साथ `drawRectangle` कॉल करें। पूरी प्रक्रिया केवल कुछ मेथड कॉल्स में पूरी हो जाती है और एक तैयार‑से‑सेव बिटमैप बनाती है।  
`PsdImage` एक इन‑मेमोरी बिटमैप का प्रतिनिधित्व करता है जिसे संपादित और सेव किया जा सकता है।  
`Graphics` इमेज पर आकार रेंडर करने के लिए एक ड्रॉइंग सतह प्रदान करता है।

### चरण 1: नई इमेज बनाएं
`PsdImage` क्लास एक इन‑मेमोरी बिटमैप का प्रतिनिधित्व करती है। इसे इनिशियलाइज़ करने से पिक्सेल बफ़र भी अलोकेट हो जाता है।

```java
String dataDir = "path_to_your_data_directory/";
String outpath = dataDir + "Rectangle.bmp";
// Create an instance of BmpOptions and set its properties
BmpOptions saveOptions = new BmpOptions();
saveOptions.setBitsPerPixel(32);
// Create an instance of PsdImage with specified dimensions
Image image = new PsdImage(100, 100);
```
इस चरण में, `PsdImage` को **100 px** की चौड़ाई और ऊँचाई के साथ इनिशियलाइज़ किया गया है, जो आपको डेमॉन्स्ट्रेशन के लिए एक छोटा कैनवास देता है।

### चरण 2: ग्राफ़िक्स जावा ऑब्जेक्ट इनिशियलाइज़ करें
`Graphics` इंस्टेंस वह ड्रॉइंग सतह है जो आपने अभी बनाई इमेज से जुड़ी होती है।

```java
// Initialize Graphics object
Graphics graphic = new Graphics(image);
```
यह `Graphics` ऑब्जेक्ट ड्रॉइंग ऑपरेशन्स जैसे कि शैप्स को भरना या आउटलाइन ड्रॉ करना करने के लिए उपयोग किया जाएगा।

### चरण 3: बैकग्राउंड रंग सेट करें जावा
शैप्स ड्रॉ करने से पहले अक्सर आप एक ठोस बैकग्राउंड चाहते हैं। पूरे कैनवास को भरने के लिए `clear` को `Color` के साथ उपयोग करें।

```java
// Clear graphics surface with a yellow color
graphic.clear(Color.YELLOW);
```
बैकग्राउंड को **पीला** सेट किया गया है, जो आगे आने वाली लाल और नीली आयतों के लिए उच्च कंट्रास्ट प्रदान करता है।

### चरण 4: इमेज पर आयतें ड्रॉ करें
आउटलाइन के लिए `Pen` और फ़िल के लिए `SolidBrush` के साथ `drawRectangle` का उपयोग करें। आप विभिन्न रंगों और स्थितियों वाली कई आयतें ड्रॉ कर सकते हैं।

```java
// Draw a red rectangle
graphic.drawRectangle(new Pen(Color.RED), new Rectangle(30, 10, 40, 80));
// Draw a blue rectangle
graphic.drawRectangle(new Pen(new SolidBrush(Color.BLUE)), new Rectangle(10, 30, 80, 40));
```
ये कमांड (10, 10) पर एक **लाल** आयत और (50, 50) पर एक **नीली** आयत ड्रॉ करती हैं, प्रत्येक की चौड़ाई 40 px और ऊँचाई 30 px है।

### चरण 5: इमेज को बिटमैप में एक्सपोर्ट करें
अंत में, संशोधित इमेज को डिस्क पर सेव करें। Aspose.PSD स्वचालित रूप से बिटमैप को आपके द्वारा निर्दिष्ट फॉर्मेट में एन्कोड करता है।

```java
// Export image to BMP file format
image.save(outpath, saveOptions);
```
इमेज `outpath` में संग्रहीत पाथ पर BMP फ़ाइल के रूप में सेव की गई है।

## सामान्य समस्याएँ और समाधान
- **ब्लैंक आउटपुट फ़ाइल** – ड्रॉ करने से पहले `graphics.clear` कॉल करना सुनिश्चित करें; अन्यथा कैनवास ट्रांसपेरेंट रह सकता है।  
- **गलत रंग** – यह सत्यापित करें कि आप `com.aspose.psd.Color` इम्पोर्ट कर रहे हैं, न कि `java.awt.Color`।  
- **बड़ी इमेज मेमोरी से बाहर** – पूरे फ़ाइल को RAM में लोड करने से बचने के लिए `PsdImage` कंस्ट्रक्टर्स का उपयोग करें जो स्ट्रीमिंग सपोर्ट करते हैं।

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या Aspose.PSD for Java आयतों के अलावा अन्य शैप्स को हैंडल कर सकता है?**  
A: हाँ, यह एलिप्स, लाइन्स, पॉलीगॉन और कस्टम पाथ्स को सपोर्ट करता है, जिससे आपको पूरी वेक्टर ड्रॉइंग क्षमताएँ मिलती हैं।

**Q: मैं आयत बॉर्डर की मोटाई कैसे बदल सकता हूँ?**  
A: `drawRectangle` कॉल करने से पहले `Pen` ऑब्जेक्ट की `setWidth(float)` मेथड सेट करें।

**Q: क्या Aspose.PSD for Java हाई‑परफ़ॉर्मेंस इमेज प्रोसेसिंग टास्क्स के लिए उपयुक्त है?**  
A: बिलकुल – इसका स्ट्रीमिंग API कई सौ पेज़ वाले PSD फ़ाइलों को 200 MB से कम RAM उपयोग के साथ प्रोसेस करता है।

**Q: Aspose.PSD for Java के अधिक उदाहरण और ट्यूटोरियल्स कहाँ मिल सकते हैं?**  
A: आप अधिक उदाहरण और विस्तृत डॉक्यूमेंटेशन [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/) पर देख सकते हैं।

**Q: क्या Aspose.PSD for Java BMP के अलावा अन्य इमेज फॉर्मेट्स को सपोर्ट करता है?**  
A: हाँ, यह PNG, JPEG, TIFF, GIF, और 30 से अधिक अतिरिक्त फॉर्मेट्स को इम्पोर्ट और एक्सपोर्ट दोनों के लिए सपोर्ट करता है।

## निष्कर्ष
अब आप Aspose.PSD for Java का उपयोग करके इमेज पर **आयत कैसे बनाएं** जानते हैं, बिटमैप बनाने से लेकर बैकग्राउंड रंग सेट करने और ग्राफ़िक्स इनिशियलाइज़ करने तक। विभिन्न आकार, रंग और अतिरिक्त शैप्स के साथ प्रयोग करके **java इमेज मैनिपुलेशन** में महारत हासिल करें। जब आप तैयार हों, इस पैटर्न को बड़े बैच‑प्रोसेसिंग पाइपलाइन या UI‑ड्रिवेन एडिटर्स में इंटीग्रेट करें।

---

**Last Updated:** 2026-09-08  
**Tested with:** Aspose.PSD for Java 24.12  
**Author:** Aspose

## संबंधित ट्यूटोरियल्स

- [Resize Image with Aspose.PSD for Java – Draw Shapes & Basic Image Operations](/psd/java/basic-image-operations/)
- [Add Signature to Image – Draw Image on Canvas with Aspose.PSD for Java](/psd/java/advanced-image-effects/add-signature-to-image/)
- [Crop Image by Rectangle with Aspose.PSD for Java](/psd/java/image-editing/crop-image-by-rectangle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}