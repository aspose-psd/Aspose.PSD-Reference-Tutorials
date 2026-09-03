---
date: 2026-09-03
description: Aspose.PSD for Java का उपयोग करके PSD फ़ाइलों में gradient stroke java
  बनाने और stroke gradients को कस्टमाइज़ करना सीखें। डेवलपर्स के लिए चरण‑दर‑चरण गाइड।
keywords:
- create gradient stroke java
- add gradient stroke psd
- Aspose.PSD Java
- PSD gradient stroke
lastmod: 2026-09-03
linktitle: Java में Gradient Stroke लेयर कैसे बनाएं
og_description: Aspose.PSD for Java के साथ मिनटों में gradient stroke java बनाएं।
  यह ट्यूटोरियल दिखाता है कि कैसे PSD फ़ाइलों में gradient strokes जोड़ें और कस्टमाइज़
  करें, साथ ही कोड स्निपेट्स और बेस्ट प्रैक्टिसेज़ शामिल हैं।
og_image_alt: Screenshot of a PSD file showing a gradient stroke applied via Aspose.PSD
  Java API
og_title: ग्रेडिएंट स्ट्रोक java बनाएं – Aspose.PSD ट्यूटोरियल गाइड
schemas:
- author: Aspose
  dateModified: '2026-09-03'
  description: Learn how to create gradient stroke java and customize stroke gradients
    in PSD files using Aspose.PSD for Java. Step‑by‑step guide for developers.
  headline: Create gradient stroke java – Aspose.PSD tutorial guide
  type: TechArticle
- description: Learn how to create gradient stroke java and customize stroke gradients
    in PSD files using Aspose.PSD for Java. Step‑by‑step guide for developers.
  name: Create gradient stroke java – Aspose.PSD tutorial guide
  steps:
  - name: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      website](https://www.oracle.com/java/technologies/javase-downloads.html).'
    text: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      website](https://www.oracle.com/java/technologies/javase-downloads.html).'
  - name: '**Aspose.PSD for Java** – Download the library from the [Aspose.PSD download
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – Download the library from the [Aspose.PSD download
      page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or NetBeans.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or NetBeans.'
  - name: '**License** – Obtain a [temporary license](https://purchase.aspose.com/temporary-license/)
      if you don’t have a full commercial license.'
    text: '**License** – Obtain a [temporary license](https://purchase.aspose.com/temporary-license/)
      if you don’t have a full commercial license.'
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a pure‑Java library that lets developers create,
      edit, convert, and render Photoshop PSD files without requiring Adobe Photoshop.
    question: What is Aspose.PSD for Java?
  - answer: Yes, a valid license is required for production use. You can obtain a
      [temporary license](https://purchase.aspose.com/temporary-license/) for evaluation.
    question: Do I need a license to use Aspose.PSD for Java?
  - answer: Absolutely. Aspose.PSD provides APIs to build a new PSD document, add
      layers, apply effects, and save the file entirely programmatically.
    question: Can I create PSD files from scratch with this library?
  - answer: Yes, you can apply shadows, glows, bevels, and many other layer effects
      using the same effect‑based API.
    question: Is it possible to apply other effects besides gradient strokes?
  - answer: The official documentation is available in the [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find the full reference documentation?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- gradient stroke
- Aspose.PSD
- Java graphics
title: ग्रेडिएंट स्ट्रोक java बनाएं – Aspose.PSD ट्यूटोरियल गाइड
url: /hi/java/java-graphics-drawing/add-stroke-layer-gradient/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD के साथ ग्रेडिएंट स्ट्रोक जावा कैसे बनाएं

## परिचय
यदि आपको Photoshop खोले बिना **create gradient stroke java** इफ़ेक्ट्स बनाने की आवश्यकता है, तो आप सही जगह पर आए हैं। इस ट्यूटोरियल में आप सीखेंगे कि Aspose.PSD for Java—एक शुद्ध‑Java लाइब्रेरी—का उपयोग करके PSD फ़ाइलों पर पूर्ण प्रोग्रामेटिक नियंत्रण कैसे प्राप्त करें। हम PSD लोड करने, लेयर के स्ट्रोक इफ़ेक्ट तक पहुंचने, ग्रेडिएंट फ़िल को कॉन्फ़िगर करने, और अंत में परिणाम को सहेजने की प्रक्रिया को चरणबद्ध करेंगे। अंत तक आप कुछ ही कोड लाइनों में आकार या टेक्स्ट पर प्रोफ़ेशनल‑ग्रेड ग्रेडिएंट आउटलाइन जोड़ सकेंगे।

## त्वरित उत्तर
- **मुख्य लक्ष्य क्या है?** Java का उपयोग करके PSD फ़ाइल पर एक ग्रेडिएंट स्ट्रोक लेयर बनाएं।  
- **कौन सी लाइब्रेरी API प्रदान करती है?** Aspose.PSD for Java (supports Java 8 +).  
- **क्या उत्पादन के लिए लाइसेंस की आवश्यकता है?** हाँ – एक वैध या अस्थायी लाइसेंस आवश्यक है।  
- **एक बुनियादी कार्यान्वयन में कितना समय लगता है?** लगभग 10‑15 मिनट एक साधारण स्ट्रोक के लिए।  
- **क्या मैं ग्रेडिएंट प्रकार को कस्टमाइज़ कर सकता हूँ?** बिल्कुल – रैखिक, रेडियल, और कोण‑आधारित ग्रेडिएंट सभी समर्थित हैं।

## ग्रेडिएंट स्ट्रोक लेयर क्या है?
ग्रेडिएंट स्ट्रोक लेयर एक वेक्टर रूपरेखा है जिसका रंग दो या अधिक शेड्स के बीच सुगमता से बदलता है। इसे आकार, टेक्स्ट, या PSD फ़ाइल के भीतर किसी भी वेक्टर मास्क पर लागू किया जा सकता है, जिससे डिज़ाइनरों को रास्टराइज़ किए बिना एक गतिशील दृश्य प्रभाव मिलता है।

## Aspose.PSD for Java का उपयोग क्यों करें?
Aspose.PSD for Java **full PSD support** प्रदान करता है, जिसमें 100 से अधिक सुविधाएँ शामिल हैं—लेयर्स, मास्क, एडजस्टमेंट लेयर्स, और लेयर इफ़ेक्ट्स—और यह पूरी दस्तावेज़ को मेमोरी में लोड किए बिना 2 GB तक की फ़ाइलों को प्रोसेस कर सकता है। यह लाइब्रेरी किसी भी ऑपरेटिंग सिस्टम पर चलती है जो Java का समर्थन करता है, इसमें कोई नेटिव डिपेंडेंसी नहीं है, और नवीनतम Photoshop फ़ाइल विनिर्देशों के साथ संगत रहने के लिए मासिक रूप से अपडेट होती रहती है।

## पूर्वापेक्षाएँ
1. **Java Development Kit (JDK)** – नवीनतम JDK को [Oracle's website](https://www.oracle.com/java/technologies/javase-downloads.html) से इंस्टॉल करें।  
2. **Aspose.PSD for Java** – लाइब्रेरी को [Aspose.PSD download page](https://releases.aspose.com/psd/java/) से डाउनलोड करें।  
3. **IDE** – IntelliJ IDEA, Eclipse, या NetBeans।  
4. **License** – यदि आपके पास पूर्ण वाणिज्यिक लाइसेंस नहीं है तो एक [temporary license](https://purchase.aspose.com/temporary-license/) प्राप्त करें।

## पैकेज आयात करें
`import` स्टेटमेंट आवश्यक क्लासेज़ को स्कोप में लाते हैं।

```text
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```
```

अब चलिए प्रक्रिया को स्पष्ट चरणों में विभाजित करते हैं।

## चरण 1: PSD फ़ाइल लोड करें
स्रोत फ़ाइल को लोड करना पहला चरण है; आपको प्रभाव संसाधनों को सक्षम करना होगा ताकि स्ट्रोक जानकारी संपादन के लिए उपलब्ध हो। **PsdLoadOptions** यह निर्धारित करता है कि PSD फ़ाइल कैसे लोड की जाती है, जिससे आप विशिष्ट संसाधनों को सक्षम या अक्षम कर सकते हैं।

```text
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```
```

## चरण 2: स्ट्रोक इफ़ेक्ट तक पहुंचें
**StrokeEffect** लेयर पर लागू आउटलाइन स्टाइलिंग को दर्शाता है, जिसमें चौड़ाई, रंग, और ग्रेडिएंट फ़िल शामिल हैं।

```text
```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```
```

## चरण 3: स्ट्रोक इफ़ेक्ट गुणों की पुष्टि करें
किसी भी परिवर्तन से पहले, मौजूदा गुणों को पढ़ना एक अच्छी प्रथा है। यह आपको वर्तमान कॉन्फ़िगरेशन समझने और अनजाने में महत्वपूर्ण सेटिंग्स को ओवरराइट करने से बचने में मदद करता है। **GradientFillSettings** स्ट्रोक इफ़ेक्ट के लिए ग्रेडिएंट फ़िल कॉन्फ़िगरेशन रखता है।

```text
```java
Assert.areEqual(BlendMode.Normal, gradientStroke.getBlendMode());
Assert.areEqual(255, gradientStroke.getOpacity());
Assert.areEqual(true, gradientStroke.isVisible());
GradientFillSettings fillSettings = (GradientFillSettings) gradientStroke.getFillSettings();
Assert.areEqual(Color.getBlack(), fillSettings.getColor());
Assert.areEqual(FillType.Gradient, fillSettings.getFillType());
Assert.areEqual(true, fillSettings.getAlignWithLayer());
Assert.areEqual(GradientType.Linear, fillSettings.getGradientType());
Assert.isTrue(Math.abs(90 - fillSettings.getAngle()) < 0.001, "Angle is incorrect");
Assert.areEqual(false, fillSettings.getDither());
Assert.isTrue(Math.abs(0 - fillSettings.getHorizontalOffset()) < 0.001, "Horizontal offset is incorrect");
Assert.isTrue(Math.abs(0 - fillSettings.getVerticalOffset()) < 0.001, "Vertical offset is incorrect");
Assert.areEqual(false, fillSettings.getReverse());
```
```

## चरण 4: ग्रेडिएंट फ़िल सेटिंग्स संशोधित करें
`GradientFill` निर्धारित करता है कि स्ट्रोक के पार रंग कैसे ट्रांज़िशन करते हैं। आप इसका प्रकार (linear, radial), कोण, और ब्लेंड मोड बदल सकते हैं, फिर नए रंग और ट्रांसपेरेंसी पॉइंट असाइन कर सकते हैं।

```text
```java
fillSettings.setColor(Color.getGreen());
gradientStroke.setOpacity((byte) 127);
gradientStroke.setBlendMode(BlendMode.Color);
fillSettings.setAlignWithLayer(false);
fillSettings.setGradientType(GradientType.Radial);
fillSettings.setAngle(45);
fillSettings.setDither(true);
fillSettings.setHorizontalOffset(15);
fillSettings.setVerticalOffset(11);
fillSettings.setReverse(true);
```
```

## चरण 5: रंग और ट्रांसपेरेंसी पॉइंट जोड़ें और संशोधित करें
एक ग्रेडिएंट कई रंग‑स्टॉप और अपारदर्शिता‑स्टॉप पॉइंट्स से बनता है। **GradientColorPoint** ग्रेडिएंट में एक रंग स्टॉप को परिभाषित करता है, जिसमें उसका रंग और स्थिति निर्दिष्ट होती है। **GradientTransparencyPoint** ग्रेडिएंट में एक अपारदर्शिता स्टॉप को परिभाषित करता है, जिसमें उसकी अपारदर्शिता और स्थिति निर्दिष्ट होती है। इन पॉइंट्स को जोड़ने या समायोजित करने से आप स्ट्रोक के दृश्य प्रवाह को आकार दे सकते हैं।

```text
```java
// Add new color point
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Change location of previous point
fillSettings.getColorPoints()[1].setLocation(1899);
// Add new transparency point
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Change location of previous transparency point
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```
```

## चरण 6: संशोधित PSD फ़ाइल सहेजें
सभी समायोजन करने के बाद, अपडेटेड दस्तावेज़ को डिस्क पर वापस लिखें। Aspose.PSD स्वचालित रूप से सभी अन्य लेयर्स और संसाधनों को संरक्षित रखता है।

```text
```java
im.save(exportPath);
```
```

## चरण 7: संशोधनों की पुष्टि करें
सहेजी गई फ़ाइल को पुनः लोड करें और यह सुनिश्चित करें कि स्ट्रोक के ग्रेडिएंट गुण आपके द्वारा सेट किए गए मानों से मेल खाते हों। यह सत्यापन चरण स्वचालित पाइपलाइन के लिए आवश्यक है। **Assert** रनटाइम में शर्तों की पुष्टि करने के लिए सरल टेस्ट असर्शन प्रदान करता है।

```text
```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// Check color points
Assert.areEqual(3, fillSetting.getColorPoints().length);
IGradientColorPoint point = fillSetting.getColorPoints()[0];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getBlack(), point.getColor());
Assert.areEqual(0, point.getLocation());
point = fillSettings.getColorPoints()[1];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getWhite(), point.getColor());
Assert.areEqual(1899, point.getLocation());
point = fillSettings.getColorPoints()[2];
Assert.areEqual(75, point.getMedianPointLocation());
Assert.areEqual(Color.getGreen(), point.getColor());
Assert.areEqual(4096, point.getLocation());
// Check transparency points
Assert.areEqual(3, fillSettings.getTransparencyPoints().length);
IGradientTransparencyPoint transparencyPoint1 = fillSettings.getTransparencyPoints()[0];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(0, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[1];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(2411, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[2];
Assert.areEqual(25, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(25, transparencyPoint1.getOpacity());
Assert.areEqual(4096, transparencyPoint1.getLocation());
```
```

## सामान्य समस्याएँ और समस्या निवारण टिप्स
- **Missing license error** – यदि आपको लाइसेंसिंग एक्सेप्शन दिखता है, तो किसी भी API कॉल से पहले यह दोबारा जांचें कि अस्थायी लाइसेंस फ़ाइल सही ढंग से लोड हुई है।  
- **Gradient not visible** – सुनिश्चित करें कि लक्ष्य लेयर का `strokeEnabled` फ़्लैग `true` पर सेट है; अन्यथा रेंडरिंग के दौरान इफ़ेक्ट को अनदेखा किया जाएगा।  
- **Performance on large files** – 500 MB से बड़ी PSD फ़ाइलों के लिए, `PsdImage.load(..., LoadOptions)` को `loadResources = false` के साथ उपयोग करने पर विचार करें और केवल आवश्यक संसाधनों को सक्षम करें।

## अक्सर पूछे जाने वाले प्रश्न

**Q: Aspose.PSD for Java क्या है?**  
A: Aspose.PSD for Java एक शुद्ध‑Java लाइब्रेरी है जो डेवलपर्स को Adobe Photoshop की आवश्यकता के बिना Photoshop PSD फ़ाइलों को बनाना, संपादित करना, परिवर्तित करना और रेंडर करना सक्षम करती है।

**Q: Aspose.PSD for Java का उपयोग करने के लिए क्या मुझे लाइसेंस चाहिए?**  
A: हाँ, उत्पादन उपयोग के लिए एक वैध लाइसेंस आवश्यक है। आप मूल्यांकन के लिए एक [temporary license](https://purchase.aspose.com/temporary-license/) प्राप्त कर सकते हैं।

**Q: क्या मैं इस लाइब्रेरी से शून्य से PSD फ़ाइलें बना सकता हूँ?**  
A: बिल्कुल। Aspose.PSD APIs प्रदान करता है जिससे आप नया PSD दस्तावेज़ बना सकते हैं, लेयर्स जोड़ सकते हैं, इफ़ेक्ट्स लागू कर सकते हैं, और पूरी तरह प्रोग्रामेटिक रूप से फ़ाइल सहेज सकते हैं।

**Q: क्या ग्रेडिएंट स्ट्रोक के अलावा अन्य इफ़ेक्ट्स लागू करना संभव है?**  
A: हाँ, आप समान इफ़ेक्ट‑आधारित API का उपयोग करके शैडोज़, ग्लो, बिवेल और कई अन्य लेयर इफ़ेक्ट्स लागू कर सकते हैं।

**Q: पूर्ण रेफ़रेंस दस्तावेज़ीकरण कहाँ मिल सकता है?**  
A: आधिकारिक दस्तावेज़ीकरण [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/) में उपलब्ध है।

## निष्कर्ष
अब आपके पास Aspose.PSD का उपयोग करके PSD फ़ाइलों में **create gradient stroke java** इफ़ेक्ट्स बनाने का एक पूर्ण, अंत‑से‑अंत समाधान है। एक PSD लोड करके, स्ट्रोक इफ़ेक्ट तक पहुंचकर, ग्रेडिएंट फ़िल को कॉन्फ़िगर करके, और फ़ाइल को सहेजकर, आप जटिल ग्राफ़िक्स वर्कफ़्लो को स्वचालित कर सकते हैं, जो अन्यथा Photoshop में मैन्युअल कार्य की आवश्यकता होती। विभिन्न ग्रेडिएंट प्रकारों, ब्लेंड मोड्स, और अपारदर्शिता स्टॉप्स के साथ प्रयोग करें ताकि आप अपने एप्लिकेशन के लिए आवश्यक सटीक लुक प्राप्त कर सकें।

---

**अंतिम अपडेट:** 2026-09-03  
**परीक्षित संस्करण:** Aspose.PSD for Java 24.11  
**लेखक:** Aspose

## संबंधित ट्यूटोरियल

- [Aspose.PSD का उपयोग करके जावा के साथ ग्रेडिएंट फ़िल PSD बनाएं – ग्रेडिएंट फ़िल लेयर जोड़ें](/psd/java/psd-image-modification-conversion/add-gradient-fill-layer-psd-files/)
- [Aspose.PSD for Java में रेडियल ग्रेडिएंट इफ़ेक्ट्स कैसे बनाएं](/psd/java/advanced-image-effects/add-gradient-effects/)
- [Aspose.PSD का उपयोग करके जावा में स्ट्रोक रंग कैसे बदलें](/psd/java/advanced-image-effects/add-stroke-layer-color/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}