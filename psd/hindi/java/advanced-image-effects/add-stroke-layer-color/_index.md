---
date: 2026-10-24
description: Aspose.PSD for Java के साथ Java में स्ट्रोक लेयर बनाना सीखें। यह चरण‑दर‑चरण
  गाइड आपको स्ट्रोक लेयर जोड़ना, उसका रंग बदलना, अपारदर्शिता समायोजित करना, और PSD
  को सहेजना दिखाता है।
keywords:
- create stroke layer java
- change stroke color java
- modify stroke opacity
- apply stroke effect
- psd stroke tutorial
lastmod: 2026-10-24
linktitle: स्ट्रोक लेयर का रंग जोड़ें
og_description: Aspose.PSD for Java का उपयोग करके Java में स्ट्रोक लेयर बनाएं। इस
  संक्षिप्त ट्यूटोरियल का पालन करें ताकि आप स्ट्रोक लेयर जोड़ सकें, उसका रंग बदल सकें,
  अपारदर्शिता समायोजित कर सकें, और PSD फ़ाइल निर्यात कर सकें।
og_image_alt: Screenshot of a Java IDE showing Aspose.PSD code that creates and modifies
  a stroke layer in a PSD file
og_title: Aspose.PSD के साथ Java में स्ट्रोक लेयर बनाएं – त्वरित गाइड
schemas:
- author: Aspose
  dateModified: '2026-10-24'
  description: Learn how to create stroke layer Java with Aspose.PSD for Java. This
    step‑by‑step guide shows you how to add a stroke layer, change its color, adjust
    opacity, and save the PSD.
  headline: How to create stroke layer Java using Aspose.PSD
  type: TechArticle
- description: Learn how to create stroke layer Java with Aspose.PSD for Java. This
    step‑by‑step guide shows you how to add a stroke layer, change its color, adjust
    opacity, and save the PSD.
  name: How to create stroke layer Java using Aspose.PSD
  steps:
  - name: set up your project
    text: Create a new Java project, add the Aspose.PSD JAR to the build path, and
      verify the library loads without errors.
  - name: load the PSD file
    text: Enable loading of effect resources so the stroke information is available.
  - name: access the stroke effect layer
    text: '`StrokeEffect` is Aspose.PSD’s class that represents a vector outline applied
      to a layer. Retrieve the first stroke effect from the second layer (index 1).'
  - name: validate stroke properties
    text: '`ColorFillSettings` holds the color and opacity values for a stroke. Confirm
      the existing properties before making changes to avoid unexpected results.'
  - name: set color and opacity (how to change stroke color)
    text: Here we **change stroke color** to yellow and reduce opacity to 50 % (127
      / 255). `ColorFillSettings` also lets you specify blend mode and size.
  - name: save the modified PSD
    text: Write the updated image back to disk. The new file now contains the modified
      stroke.
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD can be combined with libraries such as Apache Commons
      Imaging or Java2D for extended functionality.
    question: Can I use Aspose.PSD with other Java graphic libraries?
  - answer: Absolutely. The library supports the newest Photoshop specifications and
      over 150 PSD features.
    question: Is Aspose.PSD compatible with the latest PSD file format?
  - answer: Wrap your code in try‑catch blocks and consult the [support forum](https://forum.aspose.com/c/psd/34)
      for detailed troubleshooting examples.
    question: How do I handle exceptions while using Aspose.PSD?
  - answer: Certainly! Grab a [free trial](https://releases.aspose.com/) to explore
      all features.
    question: Can I try Aspose.PSD before purchasing?
  - answer: Obtain a [temporary license](https://purchase.aspose.com/temporary-license/)
      to evaluate the library in your development environment.
    question: Where can I get a temporary license for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- create stroke layer
- Aspose.PSD
- Java image processing
title: Aspose.PSD का उपयोग करके Java में स्ट्रोक लेयर कैसे बनाएं
url: /hi/java/advanced-image-effects/add-stroke-layer-color/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD का उपयोग करके Java में स्ट्रोक लेयर कैसे बनाएं

## परिचय

यदि आपको प्रोग्रामेटिक रूप से Photoshop दस्तावेज़ में **create stroke layer Java** बनाने की आवश्यकता है, तो Aspose.PSD for Java आपको एक साफ़, कोड‑पहला दृष्टिकोण प्रदान करता है। इस ट्यूटोरियल में आप सीखेंगे कि नई स्ट्रोक लेयर कैसे जोड़ें, उसका रंग बदलें, अपारदर्शिता समायोजित करें, और परिणाम सहेजें—बिना Photoshop लॉन्च किए। अंत में आप यह भी जानेंगे कि मौजूदा लेयर की स्ट्रोक को कैसे संपादित करें, जिससे आप अपने Java एप्लिकेशन से सीधे पूर्ण रचनात्मक नियंत्रण प्राप्त कर सकें।

## त्वरित उत्तर

- **कौनसी लाइब्रेरी आवश्यक है?** Aspose.PSD for Java (latest version).  
- **क्या मैं स्ट्रोक का रंग बदल सकता हूँ?** हाँ – किसी भी `Color` को सेट करने के लिए `ColorFillSettings` का उपयोग करें।  
- **क्या मुझे लाइसेंस चाहिए?** एक अस्थायी लाइसेंस मूल्यांकन के लिए काम करता है; उत्पादन के लिए पूर्ण लाइसेंस आवश्यक है।  
- **कौनसा Java संस्करण समर्थित है?** Java 8 या नया।  
- **इम्प्लीमेंटेशन में कितना समय लगता है?** आमतौर पर एक बुनियादी स्ट्रोक परिवर्तन के लिए 10 मिनट से कम समय लगता है।

## PSD में स्ट्रोक लेयर क्या है?

स्ट्रोक लेयर एक वेक्टर इफ़ेक्ट है जो लेयर की सामग्री के चारों ओर एक रूपरेखा बनाता है। इसे रंग, मोटाई, अपारदर्शिता और ब्लेंड मोड के साथ अनुकूलित किया जा सकता है। इस इफ़ेक्ट को प्रोग्रामेटिक रूप से संशोधित करने से स्वचालित ब्रांडिंग, बैच प्रोसेसिंग, या डायनेमिक ग्राफ़िक्स जेनरेशन संभव होता है।

## स्ट्रोक का रंग बदलने के लिए Aspose.PSD का उपयोग क्यों करें?

Aspose.PSD **150+** PSD सुविधाओं का समर्थन करता है—जिसमें वेक्टर मास्क, स्मार्ट ऑब्जेक्ट्स, और लेयर इफ़ेक्ट्स शामिल हैं—और कई सौ पृष्ठों वाली फ़ाइलों को पूरी दस्तावेज़ को मेमोरी में लोड किए बिना प्रोसेस करता है। यह लाइब्रेरी किसी भी OS पर JVM के साथ चलती है, सामान्य एसेट्स के लिए सब‑सेकंड प्रदर्शन देती है, और Photoshop इंस्टॉलेशन की आवश्यकता नहीं होती।

## Java में स्ट्रोक लेयर कैसे बनाएं?

PSD लोड करें, स्ट्रोक इफ़ेक्ट जोड़ें, उसकी उपस्थिति कॉन्फ़िगर करें, और फ़ाइल सहेजें—सभी कुछ सरल लाइनों में। नीचे दिया गया उत्तर आपको बताता है कि चरण‑दर‑चरण walkthrough में जाने से पहले क्या करना है।

**सीधा उत्तर (40‑70 शब्द):**  
`PsdImage` एक PSD दस्तावेज़ का प्रतिनिधित्व करता है और फ़ाइलों को लोड और सहेजने के लिए मेथड प्रदान करता है। `PsdImage.load("input.psd", loadOptions)` के साथ अपना PSD लोड करके शुरू करें। एक नया `StrokeEffect` बनाएं, उसके `ColorFillSettings` को इच्छित `Color` पर सेट करें, अपारदर्शिता और आकार समायोजित करें, फिर इफ़ेक्ट को लक्ष्य लेयर के `BlendingOptions` में संलग्न करें। अंत में, `psd.save("output.psd", SaveFormat.PSD)` को कॉल करें। यह क्रम Java में Aspose.PSD के साथ स्ट्रोक लेयर बनाता है।

### आवश्यकताएँ

- **Aspose.PSD लाइब्रेरी** – [official documentation](https://reference.aspose.com/psd/java/) से डाउनलोड करें।  
- **Java Development Kit (JDK)** – संस्करण 8 या नया।  
- **IDE** – Eclipse, IntelliJ IDEA, या कोई भी Java‑संगत एडिटर।

### पैकेज आयात करें

पहले, उन क्लासों को आयात करें जिनकी आपको आवश्यकता होगी। यह आपके प्रोजेक्ट को PSD हैंडलिंग और स्ट्रोक‑इफ़ेक्ट API तक पहुंच देता है।

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

### चरण 1: अपना प्रोजेक्ट सेट अप करें

एक नया Java प्रोजेक्ट बनाएं, Aspose.PSD JAR को बिल्ड पाथ में जोड़ें, और सुनिश्चित करें कि लाइब्रेरी बिना त्रुटियों के लोड हो रही है।

### चरण 2: PSD फ़ाइल लोड करें

इफ़ेक्ट संसाधनों के लोडिंग को सक्षम करें ताकि स्ट्रोक जानकारी उपलब्ध हो सके।

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

### चरण 3: स्ट्रोक इफ़ेक्ट लेयर तक पहुंचें

`StrokeEffect` Aspose.PSD की क्लास है जो लेयर पर लागू वेक्टर रूपरेखा को दर्शाती है। दूसरे लेयर (इंडेक्स 1) से पहला स्ट्रोक इफ़ेक्ट प्राप्त करें।

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

### चरण 4: स्ट्रोक गुणों को मान्य करें

`ColorFillSettings` स्ट्रोक के रंग और अपारदर्शिता मान रखता है। परिवर्तन करने से पहले मौजूदा गुणों की पुष्टि करें ताकि अप्रत्याशित परिणाम न आएँ।

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

### चरण 5: रंग और अपारदर्शिता सेट करें (स्ट्रोक रंग कैसे बदलें)

यहाँ हम स्ट्रोक का रंग पीले में **change stroke color** करते हैं और अपारदर्शिता को 50 % (127 / 255) तक घटाते हैं। `ColorFillSettings` आपको ब्लेंड मोड और आकार भी निर्दिष्ट करने देता है।

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

### चरण 6: संशोधित PSD सहेजें

अपडेटेड इमेज को डिस्क पर लिखें। नई फ़ाइल में अब संशोधित स्ट्रोक शामिल है।

```java
im.save(exportPath);
```

## Java में स्ट्रोक रंग कैसे बदलें?

`Color` एक ARGB रंग मान को दर्शाता है। अपना PSD लोड करें, लक्ष्य लेयर खोजें, `ColorFillSettings` को नए `Color` से अपडेट करें, और फ़ाइल सहेजें। यह ऑपरेशन केवल कुछ लाइनों के कोड की आवश्यकता रखता है और सामान्य एसेट्स के लिए एक सेकंड से कम समय में पूरा हो जाता है, जिससे यह तेज़ और कुशल बनता है।

**सीधा उत्तर (40‑70 शब्द):**  
`layer.getEffects().getStrokeEffect()` का उपयोग करके मौजूदा स्ट्रोक प्राप्त करें, `stroke.getColorFillSettings().setColor(Color.getRed())` (या कोई भी आवश्यक `Color`) को कॉल करें, वैकल्पिक रूप से `setOpacity((byte)200)` से 78 % अपारदर्शिता सेट करें, फिर `psd.save("output.psd", SaveFormat.PSD)` से PSD सहेजें। परिवर्तन तुरंत लागू हो जाता है बिना पूरे दस्तावेज़ को पुनः‑रेंडर किए।

## स्ट्रोक अपारदर्शिता कैसे संशोधित करें?

यदि आपको केवल अपारदर्शिता समायोजित करनी है जबकि मूल रंग बना रहे, तो `ColorFillSettings` पर `setOpacity` मान (0‑255) बदलें। उदाहरण के लिए, `colorStroke.setOpacity((byte)200);` स्ट्रोक को लगभग 78 % अपारदर्शी बना देगा। अपारदर्शिता समायोजित करने से आप डिज़ाइन आवश्यकताओं के अनुसार सूक्ष्म रूपरेखा या पूरी तरह ठोस स्ट्रोक बना सकते हैं।

**सीधा उत्तर (40‑70 शब्द):**  
वांछित लेयर से `StrokeEffect` प्राप्त करें, फिर `stroke.getColorFillSettings().setOpacity((byte)desiredValue)` कॉल करें, जहाँ `desiredValue` 0 (पारदर्शी) से 255 (पूरी तरह अपारदर्शी) तक हो सकता है। PSD सहेजें और नई अपारदर्शिता तुरंत परिलक्षित होगी। यह विधि किसी भी मौजूदा स्ट्रोक पर काम करती है, चाहे उसका मूल रंग कुछ भी हो।

## स्ट्रोक इफ़ेक्ट कैसे लागू करें?

किसी लेयर में नया स्ट्रोक इफ़ेक्ट जोड़ने के लिए जो पहले से नहीं है, एक `StrokeEffect` इंस्टेंस बनाएं, उसके `ColorFillSettings` को कॉन्फ़िगर करें, और इसे लेयर के `BlendingOptions` में संलग्न करें। समान `setColor` और `setOpacity` मेथड्स का उपयोग करके समग्र रूप को परिभाषित किया जाता है।

**सीधा उत्तर (40‑70 शब्द):**  
`StrokeEffect newStroke = new StrokeEffect(); newStroke.getColorFillSettings().setColor(Color.getBlue()); newStroke.getColorFillSettings().setOpacity((byte)255); layer.getBlendingOptions().setEffect(newStroke);` को इंस्टैंशिएट करें। इफ़ेक्ट संलग्न करने के बाद, PSD सहेजें। यह आपके दस्तावेज़ में किसी भी मौजूदा लेयर में एक नया, पूरी तरह‑कस्टमाइज़ेबल स्ट्रोक लेयर जोड़ता है।

## स्ट्रोक रंग बदलने के सामान्य उपयोग केस

- **ब्रांडिंग ऑटोमेशन:** एकल बैच रन में सैकड़ों PSD एसेट्स में लोगो पर कॉर्पोरेट रंग लागू करें।  
- **डायनेमिक UI जेनरेशन:** वेब‑आधारित डिज़ाइन टूल में उपयोगकर्ता‑चयनित थीम के आधार पर स्ट्रोक रंग तुरंत बदलें।  
- **प्रि‑फ़्लाइट तैयारी:** फ़ाइलें प्रेस को भेजने से पहले सभी स्ट्रोक रंग प्रिंट स्पेसिफिकेशन को पूरा करते हैं, यह सुनिश्चित करें।

## सामान्य समस्याएँ और सुझाव

- **Null checks** – हमेशा सत्यापित करें कि `getEffects()` कास्ट करने से पहले non‑null एरे लौटाता है।  
- **Layer index** – PSD लेयर्स शून्य‑आधारित हैं; सुनिश्चित करें कि आप सही लेयर को लक्षित कर रहे हैं।  
- **Color format** – `Color.getYellow()` केवल एक उदाहरण है; आप `new Color(r, g, b)` से कस्टम रंग बना सकते हैं।  
- **Opacity range** – अपारदर्शिता एक बाइट है (0–255); 255 से ऊपर के मान क्लैंप हो जाएंगे।  
- **Resource loading** – यदि आप `loadOptions.setLoadEffectsResource(true)` भूल जाते हैं तो `null` इफ़ेक्ट्स एरे मिलेगा।

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या मैं Aspose.PSD को अन्य Java ग्राफ़िक लाइब्रेरियों के साथ उपयोग कर सकता हूँ?**  
A: हाँ, Aspose.PSD को Apache Commons Imaging या Java2D जैसी लाइब्रेरियों के साथ मिलाकर विस्तारित कार्यक्षमता प्राप्त की जा सकती है।

**Q: क्या Aspose.PSD नवीनतम PSD फ़ाइल फ़ॉर्मेट के साथ संगत है?**  
A: बिल्कुल। लाइब्रेरी नवीनतम Photoshop विशिष्टताओं और 150 से अधिक PSD सुविधाओं का समर्थन करती है।

**Q: Aspose.PSD का उपयोग करते समय अपवादों को कैसे संभालूँ?**  
A: अपने कोड को try‑catch ब्लॉक्स में रखें और विस्तृत ट्रबलशूटिंग उदाहरणों के लिए [support forum](https://forum.aspose.com/c/psd/34) देखें।

**Q: क्या मैं खरीदने से पहले Aspose.PSD को आज़मा सकता हूँ?**  
A: निश्चित रूप से! सभी सुविधाओं को एक्सप्लोर करने के लिए एक [free trial](https://releases.aspose.com/) प्राप्त करें।

**Q: Aspose.PSD के लिए अस्थायी लाइसेंस कहाँ प्राप्त कर सकता हूँ?**  
A: अपने विकास वातावरण में लाइब्रेरी का मूल्यांकन करने के लिए एक [temporary license](https://purchase.aspose.com/temporary-license/) प्राप्त करें।

**अंतिम अपडेट:** 2026-10-24  
**परीक्षण किया गया:** Aspose.PSD 24.11 for Java  
**लेखक:** Aspose

## संबंधित ट्यूटोरियल

- [Java में Aspose.PSD का उपयोग करके स्ट्रोक रंग कैसे बदलें](/psd/java/advanced-image-effects/add-stroke-layer-color/)
- [Java का उपयोग करके PSD में शैडो कैसे जोड़ें – उन्नत लेयर इफ़ेक्ट्स](/psd/java/advanced-psd-layer-features-effects/)
- [Pattern Overlay PSD: Aspose.PSD for Java के साथ इफ़ेक्ट्स जोड़ें](/psd/java/advanced-image-effects/add-pattern-effects/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}