---
date: 2026-08-28
description: Aspose.PSD के साथ Java में layer में pattern जोड़ें। इस चरण‑दर‑चरण गाइड
  का पालन करके stroke layer effect लागू करें, pattern resources कॉन्फ़िगर करें, और
  अपने PSD files को कुशलतापूर्वक सहेजें।
keywords:
- add pattern to layer
- java add layer effect
- Aspose.PSD stroke pattern
lastmod: 2026-08-28
linktitle: Java में Stroke Layer Pattern जोड़ने का तरीका
og_description: Aspose.PSD का उपयोग करके Java में layer में pattern जोड़ें। इस संक्षिप्त
  गाइड का पालन करके stroke layer effect लागू करें, pattern resources कॉन्फ़िगर करें,
  और अपने PSD files को कुशलतापूर्वक सहेजें।
og_image_alt: Guide showing how to add pattern to layer in Java with Aspose.PSD
og_title: Java में layer में pattern जोड़ें – Aspose.PSD ट्यूटोरियल
schemas:
- author: Aspose
  dateModified: '2026-08-28'
  description: Add pattern to layer in Java with Aspose.PSD. Follow this step‑by‑step
    guide to apply a stroke layer effect, configure pattern resources, and save your
    PSD files efficiently.
  headline: How to add pattern to layer in Java
  type: TechArticle
- description: Add pattern to layer in Java with Aspose.PSD. Follow this step‑by‑step
    guide to apply a stroke layer effect, configure pattern resources, and save your
    PSD files efficiently.
  name: How to add pattern to layer in Java
  steps:
  - name: load the PSD file
    text: 'Loading the document gives you access to its layer hierarchy and effect
      collection. `PsdLoadOptions` configures how the PSD is read, while `PsdImage`
      represents the loaded file in memory. java String dataDir = "Your Document Directory";
      String sourceFileName = dataDir + "Stroke.psd"; PsdLoadOptions '
  - name: prepare new pattern data
    text: Create a `PatternResource` that holds the bitmap you want to tile as a stroke
      pattern. `PatternResource` is a PSD global resource that stores a repeating
      bitmap pattern. `Rectangle` defines the bounds of the pattern, and `UUID` provides
      a unique identifier. java int[] newPattern = new int[] { Color.
  - name: access the stroke effect
    text: Identify the shape layer that already has a stroke, then retrieve its `StrokeEffect`
      object. `StrokeEffect` represents the stroke layer effect applied to a shape
      layer. java StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
      Assert.areEqual(BlendMode.N
  - name: modify the stroke effect
    text: Now update the stroke’s properties to reference the new pattern resource.
  - name: apply the new pattern
    text: '`PatternFillSettings` holds the fill settings for a pattern‑based stroke
      effect. Commit the changes to the layer and write the updated PSD back to disk.
      java ((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal
      Line 9\0"); ((PatternFil'
  - name: verify the changes
    text: 'Reload the file and inspect the stroke to confirm the pattern appears as
      expected. java PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
      StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
      PattResource resource1 = null; for (int '
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a library that enables developers to create, edit,
      and convert PSD (Photoshop Document) files programmatically.
    question: What is Aspose.PSD for Java?
  - answer: Yes, you can use it in commercial projects. You can purchase a license
      from the **Aspose purchase page**([Aspose purchase page](https://purchase.aspose.com/buy)).
    question: Can I use Aspose.PSD for Java in a commercial project?
  - answer: Yes, you can download a free trial version from the **Aspose releases
      page**([Aspose releases page](https://releases.aspose.com/)).
    question: Is there a free trial available for Aspose.PSD for Java?
  - answer: You can get support from the Aspose community forums **here**([Aspose
      PSD community forum](https://forum.aspose.com/c/psd/34)).
    question: How can I get support for Aspose.PSD for Java?
  - answer: You need a JDK installed and an IDE for development. The library supports
      Windows, Linux, and macOS.
    question: What are the system requirements for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- layer effects
title: Java में layer में pattern जोड़ने का तरीका
url: /hi/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# जावा में लेयर में पैटर्न कैसे जोड़ें

## परिचय
जावा में लेयर में पैटर्न जोड़ना एक सामान्य आवश्यकता है जब आपको Photoshop PSD फ़ाइलों को कस्टम स्ट्रोक इफ़ेक्ट्स के साथ समृद्ध करना होता है। Aspose.PSD for Java के साथ यह कार्य सरल हो जाता है, भले ही आप लाइब्रेरी में नए हों। इस ट्यूटोरियल में आप सीखेंगे कि कैसे PSD लोड करें, एक पैटर्न रिसोर्स बनाएं, उसे स्ट्रोक इफ़ेक्ट से जोड़ें, और परिणाम को सहेजें—सभी स्पष्ट चरण‑दर‑चरण निर्देशों के साथ।

## त्वरित उत्तर
- **कौन सी लाइब्रेरी आवश्यक है?** Aspose.PSD for Java.  
- **इम्प्लीमेंटेशन में कितना समय लगता है?** बेसिक पैटर्न के लिए लगभग 10‑15 मिनट।  
- **क्या मुझे लाइसेंस चाहिए?** विकास के लिए फ्री ट्रायल काम करता है; प्रोडक्शन के लिए कमर्शियल लाइसेंस आवश्यक है।  
- **कौन सा जावा संस्करण समर्थित है?** JDK 8 या नया।  
- **क्या इसे वेब सर्विस में उपयोग कर सकता हूँ?** हाँ, API प्लेटफ़ॉर्म‑अज्ञेय है और किसी भी जावा वातावरण में काम करता है।

## लेयर में पैटर्न जोड़ना क्या है?
लेयर में पैटर्न जोड़ना का अर्थ है एक टाइल्ड बिटमैप को स्ट्रोक या फ़िल इफ़ेक्ट को असाइन करना ताकि ग्राफ़िक आकार की रूपरेखा के पूरे हिस्से में दोहराया जाए। यह तकनीक सजावटी बॉर्डर, टेक्सचर और ब्रांडिंग ओवरले के लिए व्यापक रूप से उपयोग की जाती है, जिससे डिज़ाइनर प्रत्येक तत्व को मैन्युअली ड्रॉ किए बिना सुसंगत विज़ुअल थीम बना सकते हैं।

## इस कार्य के लिए Aspose.PSD क्यों उपयोग करें?
Aspose.PSD **30+ इमेज फ़ॉर्मैट** को सपोर्ट करता है और **2 GB** तक की PSD फ़ाइलों को पूरी डॉक्यूमेंट को मेमोरी में लोड किए बिना मैनीपुलेट कर सकता है, जिससे सामान्य सर्वर हार्डवेयर पर तेज़ प्रदर्शन मिलता है। इसका फ़्लुएंट API आपको लेयर इफ़ेक्ट्स को प्रोग्रामेटिकली काम करने देता है, जिससे ऑटोमेटेड पाइपलाइन में Photoshop की आवश्यकता समाप्त हो जाती है।

## पूर्वापेक्षाएँ
- Java Development Kit (JDK) 8 या नया स्थापित हो।  
- Aspose.PSD for Java – इसे **Aspose.PSD for Java download page**([Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/)) से डाउनलोड करें और JAR को अपने प्रोजेक्ट के क्लासपाथ में जोड़ें।  
- IntelliJ IDEA या Eclipse जैसे IDE का उपयोग करें सैंपल कोड को एडिट और रन करने के लिए।  
- एक सैंपल PSD फ़ाइल जिसमें वह शेप लेयर हो जिसे आप संशोधित करना चाहते हैं।

## पैकेज इम्पोर्ट करें
पहले, उन नेमस्पेसेस को इम्पोर्ट करें जो PSD ऑब्जेक्ट्स, रिसोर्सेज़ और इफ़ेक्ट्स तक पहुंच प्रदान करते हैं।

```
// No actual code block is added to preserve original placeholders.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```
```

## जावा में लेयर में पैटर्न कैसे जोड़ें?

टार्गेट PSD लोड करें, एक पैटर्न रिसोर्स बनाएं, इसे इच्छित लेयर के स्ट्रोक इफ़ेक्ट से जोड़ें, और अंत में फ़ाइल को सहेजें। यह एंड‑टू‑एंड प्रक्रिया कुछ ही कोड लाइनों में पूरी हो जाती है और किसी भी स्टैंडर्ड PSD के साथ काम करती है जिसमें वेक्टर शेप लेयर हो।

### चरण 1: PSD फ़ाइल लोड करें
डॉक्यूमेंट को लोड करने से आपको उसकी लेयर हायरार्की और इफ़ेक्ट कलेक्शन तक पहुंच मिलती है।  
`PsdLoadOptions` यह निर्धारित करता है कि PSD कैसे पढ़ा जाए, जबकि `PsdImage` लोड की गई फ़ाइल को मेमोरी में प्रतिनिधित्व करता है।

```
// Placeholder for original code.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
```

PSD फ़ाइल को लोड करके आप अब उसकी लेयर्स और इफ़ेक्ट्स को एक्सेस और मैनीपुलेट कर सकते हैं।

### चरण 2: नया पैटर्न डेटा तैयार करें
`PatternResource` बनाएं जो वह बिटमैप रखता है जिसे आप स्ट्रोक पैटर्न के रूप में टाइल करना चाहते हैं।  
`PatternResource` एक PSD ग्लोबल रिसोर्स है जो दोहराने योग्य बिटमैप पैटर्न संग्रहीत करता है। `Rectangle` पैटर्न की सीमाएँ निर्धारित करता है, और `UUID` एक यूनिक आइडेंटिफ़ायर प्रदान करता है।

```
// Placeholder for original code.
```java
int[] newPattern = new int[]
{
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
};
Rectangle newPatternBounds = new Rectangle(0, 0, 4, 4);
UUID guid = UUID.randomUUID();
```
```

यह पैटर्न डेटा नया स्ट्रोक इफ़ेक्ट बनाने के लिए उपयोग किया जाएगा।

### चरण 3: स्ट्रोक इफ़ेक्ट तक पहुंचें
उस शेप लेयर की पहचान करें जिसमें पहले से स्ट्रोक हो, फिर उसका `StrokeEffect` ऑब्जेक्ट प्राप्त करें।  
`StrokeEffect` एक शेप लेयर पर लागू स्ट्रोक लेयर इफ़ेक्ट को दर्शाता है।

```
// Placeholder for original code.
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
```

यह सुनिश्चित करता है कि आप सही लेयर और इफ़ेक्ट के साथ काम कर रहे हैं।

### चरण 4: स्ट्रोक इफ़ेक्ट को संशोधित करें
अब स्ट्रोक की प्रॉपर्टीज़ को अपडेट करें ताकि वह नए पैटर्न रिसोर्स को रेफ़र करे।

#### स्ट्रोक इफ़ेक्ट प्रॉपर्टीज़ अपडेट करें
```
// Placeholder for original code.
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
```

#### पैटर्न रिसोर्स अपडेट करें
`PattResource` एक PSD ग्लोबल लेयर रिसोर्स है जो पैटर्न डेटा संग्रहीत करता है।

```
// Placeholder for original code.
```java
PattResource resource;
for (int i = 0; i < im.getGlobalLayerResources().length; i++)
{
    if (im.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
        resource.setPattern(newPattern, newPatternBounds);
    }
}
```
```

ये स्निपेट्स मौजूदा पैटर्न को आपके द्वारा प्रदान किए गए पैटर्न से बदलते हैं।

### चरण 5: नया पैटर्न लागू करें
`PatternFillSettings` पैटर्न‑आधारित स्ट्रोक इफ़ेक्ट के फ़िल सेटिंग्स को रखता है। लेयर में बदलाव कमिट करें और अपडेटेड PSD को डिस्क पर लिखें।

```
// Placeholder for original code.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
```

यह सुनिश्चित करता है कि नया पैटर्न सही ढंग से लागू हो और फ़ाइल में बदलाव सहेजे जाएँ।

### चरण 6: बदलावों की पुष्टि करें
फ़ाइल को पुनः लोड करें और स्ट्रोक की जांच करें ताकि यह पुष्टि हो सके कि पैटर्न अपेक्षित रूप से दिख रहा है।

```
// Placeholder for original code.
```java
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
PattResource resource1 = null;
for (int i = 0; i < img.getGlobalLayerResources().length; i++)
{
    if (img.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource1 = (PattResource)img.getGlobalLayerResources()[i];
    }
}
try
{
    Assert.areEqual(newPattern, resource1.getPatternData());
    Assert.areEqual(newPatternBounds, new Rectangle(0, 0, resource1.getWidth(), resource1.getHeight()));
    Assert.areEqual(guid.toString(), resource1.getPatternId());
    Assert.areEqual(BlendMode.Color, patternStrokeEffect.getBlendMode());
    Assert.areEqual(127, patternStrokeEffect.getOpacity());
    Assert.areEqual(true, patternStrokeEffect.isVisible());
    PatternFillSettings fillSettings1 = (PatternFillSettings)patternStrokeEffect.getFillSettings();
    Assert.areEqual(FillType.Pattern, fillSettings1.getFillType());
}
catch (Exception e)
{
    System.out.println(e.getMessage());
}
```
```

यह चरण पुष्टि करता है कि पैटर्न डेटा स्ट्रोक इफ़ेक्ट पर सही ढंग से लागू हुआ है।

## सामान्य समस्याएँ और ट्रबलशूटिंग
- **पैटर्न दिखाई नहीं दे रहा:** सुनिश्चित करें कि पैटर्न इमेज की DPI PSD की रिज़ॉल्यूशन से मेल खाती हो, और स्ट्रोक का `Enabled` फ़्लैग `true` पर सेट हो।  
- **बड़ी PSD फ़ाइलें OutOfMemoryError देती हैं:** `PsdImage.load(..., LoadOptions)` के साथ `LoadOptions.setLoadAllLayers(false)` उपयोग करें ताकि लेयर्स ऑन‑डिमांड लोड हों।  
- **गलत लेयर चयनित:** इफ़ेक्ट्स तक पहुंचने से पहले लेयर इंडेक्स या नाम की पुष्टि करें; आप `psdImage.getLayers()` को एनेमरेट करके उपलब्ध लेयर्स की सूची बना सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

**Q: Aspose.PSD for Java क्या है?**  
A: Aspose.PSD for Java एक लाइब्रेरी है जो डेवलपर्स को प्रोग्रामेटिकली PSD (Photoshop Document) फ़ाइलें बनाने, संपादित करने और कनवर्ट करने में सक्षम बनाती है।

**Q: क्या मैं Aspose.PSD for Java को व्यावसायिक प्रोजेक्ट में उपयोग कर सकता हूँ?**  
A: हाँ, आप इसे व्यावसायिक प्रोजेक्ट्स में उपयोग कर सकते हैं। आप **Aspose purchase page**([Aspose purchase page](https://purchase.aspose.com/buy)) से लाइसेंस खरीद सकते हैं।

**Q: क्या Aspose.PSD for Java के लिए फ्री ट्रायल उपलब्ध है?**  
A: हाँ, आप **Aspose releases page**([Aspose releases page](https://releases.aspose.com/)) से फ्री ट्रायल संस्करण डाउनलोड कर सकते हैं।

**Q: मैं Aspose.PSD for Java के लिए सपोर्ट कैसे प्राप्त कर सकता हूँ?**  
A: आप Aspose कम्युनिटी फ़ोरम **here**([Aspose PSD community forum](https://forum.aspose.com/c/psd/34)) से सपोर्ट प्राप्त कर सकते हैं।

**Q: Aspose.PSD for Java की सिस्टम आवश्यकताएँ क्या हैं?**  
A: आपको JDK स्थापित होना चाहिए और विकास के लिए एक IDE चाहिए। लाइब्रेरी Windows, Linux, और macOS को सपोर्ट करती है।

## निष्कर्ष
अब आपने Aspose.PSD का उपयोग करके जावा में लेयर में पैटर्न कैसे जोड़ें, सीख लिया है। ऊपर दिए गए चरणों का पालन करके आप प्रोग्रामेटिकली PSD फ़ाइलों को कस्टम स्ट्रोक पैटर्न से एन्हांस कर सकते हैं, ब्रांडिंग वर्कफ़्लो को ऑटोमेट कर सकते हैं, और किसी भी जावा‑आधारित एप्लिकेशन में ग्राफ़िक्स प्रोसेसिंग को इंटीग्रेट कर सकते हैं। लेयर मर्जिंग, कलर एडजस्टमेंट्स, और PNG या JPEG में एक्सपोर्ट जैसे अन्य Aspose.PSD फीचर्स का अन्वेषण करें ताकि अपनी इमेज‑प्रोसेसिंग टूलकिट को और विस्तारित कर सकें।

---

**अंतिम अपडेट:** 2026-08-28  
**परीक्षित संस्करण:** Aspose.PSD 24.11 for Java  
**लेखक:** Aspose

## संबंधित ट्यूटोरियल

- [रेंडर पैटर्न फ़िल लेयर Psd फ़ाइलें](/psd/java/advanced-psd-layer-features-effects/render-pattern-fill-layer-psd-files/)
- [पैटर्न ओवरले PSD: Aspose.PSD for Java के साथ इफ़ेक्ट जोड़ें](/psd/java/advanced-image-effects/add-pattern-effects/)
- [जावा में स्ट्रोक रंग कैसे बदलें Aspose.PSD का उपयोग करके](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}