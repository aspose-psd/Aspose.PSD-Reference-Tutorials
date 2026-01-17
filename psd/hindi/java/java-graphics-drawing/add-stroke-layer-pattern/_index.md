---
date: 2026-01-17
description: Aspose.PSD for Java के साथ स्ट्रोक पैटर्न जावा कैसे जोड़ें, सीखें। अपने
  PSD इमेज को जल्दी से बेहतर बनाने के लिए इस चरण‑दर‑चरण गाइड का पालन करें।
linktitle: How to Add Stroke Layer Pattern in Java
second_title: Aspose.PSD Java API
title: Aspose.PSD का उपयोग करके जावा में स्ट्रोक पैटर्न कैसे जोड़ें
url: /hi/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD का उपयोग करके Stroke Pattern Java कैसे जोड़ें

## Introduction
यदि आपको एक Photoshop फ़ाइल में **add stroke pattern java** जोड़ने की आवश्यकता है, तो Aspose.PSD for Java इसे आश्चर्यजनक रूप से सरल बनाता है। चाहे आप एक ग्राफिक‑डिज़ाइन टूल बना रहे हों, बैच संपादन को स्वचालित कर रहे हों, या लेयर इफ़ेक्ट्स के साथ प्रयोग कर रहे हों, यह ट्यूटोरियल आपको हर चरण के माध्यम से ले जाता है—PSD लोड करने से लेकर नए पैटर्न को सत्यापित करने तक। आइए शुरू करें और देखें कि आप अपनी छवियों को कितनी जल्दी सुधार सकते हैं।

## Quick Answers
- **मुझे कौन सी लाइब्रेरी चाहिए?** Aspose.PSD for Java  
- **कौन सा Java संस्करण समर्थित है?** JDK 8 or later  
- **परीक्षण के लिए क्या मुझे लाइसेंस चाहिए?** A free trial works for development; a license is required for production  
- **इम्प्लीमेंटेशन में कितना समय लगेगा?** Roughly 10‑15 minutes for a basic pattern stroke  
- **क्या मैं पैटर्न को कई लेयर्स पर पुन: उपयोग कर सकता हूँ?** Yes, just assign the same `PattResource` to other layers  

## What is add stroke pattern java?
Java में stroke pattern जोड़ना मतलब लेयर के stroke इफ़ेक्ट पर एक कस्टम फ़िल (अक्सर दोहराया जाने वाला bitmap) लागू करना है। यह तकनीक आपको स्टाइलिश आउटलाइन बनाने देती है—जैसे डैश्ड लाइन, ईंट की बनावट, या कस्टम ग्राफिक बॉर्डर—सीधे PSD फ़ाइल के भीतर Photoshop खोले बिना।

## Why Use Aspose.PSD for add stroke pattern java?
- **पूर्ण PSD फ़िडेलिटी** – सभी लेयर इफ़ेक्ट्स, रिसोर्सेज, और ब्लेंडिंग मोड्स संरक्षित रहते हैं।  
- **नेटीव Photoshop की आवश्यकता नहीं** – JDK वाले किसी भी OS पर काम करता है।  
- **प्रोग्रामेटिक नियंत्रण** – बैच प्रोसेसिंग को ऑटोमेट करें या सर्वर‑साइड सर्विसेज़ में इंटीग्रेट करें।  
- **रिच API** – ग्लोबल रिसोर्सेज, पैटर्न फ़िल्स, और ब्लेंड मोड्स तक एक ही फ़्लुएंट इंटरफ़ेस में पहुँच।

## Prerequisites
- **Java Development Kit (JDK)** – सुनिश्चित करें कि JDK 8 या नया स्थापित है।  
- **Aspose.PSD for Java** – लाइब्रेरी को [here](https://releases.aspose.com/psd/java/) से डाउनलोड करें और JAR को अपने प्रोजेक्ट के classpath में जोड़ें।  
- **IDE** – IntelliJ IDEA, Eclipse, या कोई भी एडिटर जो आप पसंद करते हैं।

## Import Packages
सबसे पहले, उन क्लासेज़ को इम्पोर्ट करें जिनकी आपको PSD फ़ाइलों, रंगों, आयतों, और stroke इफ़ेक्ट्स को संभालने के लिए आवश्यकता होगी।

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

## Step 1: Load the PSD File
स्रोत PSD को लोड करें ताकि आप उसकी लेयर्स और रिसोर्सेज़ के साथ काम कर सकें।

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Step 2: Prepare New Pattern Data
एक सरल 4 × 4 पिक्सेल पैटर्न बनाएं जो stroke के लिए उपयोग किया जाएगा।

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

## Step 3: Access the Stroke Effect
टार्गेट लेयर पर stroke इफ़ेक्ट खोजें (इस उदाहरण में, चौथी लेयर)।

```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```

## Step 4: Modify the Stroke Effect
### Stroke Effect प्रॉपर्टीज़ अपडेट करें
नए पैटर्न के दृश्य प्रभाव को देखने के लिए opacity और blend mode को समायोजित करें।

```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```

### पैटर्न रिसोर्स अपडेट करें
मौजूदा ग्लोबल पैटर्न रिसोर्स को उस नए बनाए गए रिसोर्स से बदलें।

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

## Step 5: Apply the New Pattern
अपडेटेड पैटर्न रिसोर्स को stroke इफ़ेक्ट से बाइंड करें और PSD को सेव करें।

```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

## Step 6: Verify the Changes
फ़ाइल को पुनः लोड करें और पुष्टि करें कि नया पैटर्न, opacity, और blend mode सही ढंग से लागू हुए हैं।

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

## Common Issues and Solutions
| समस्या | कारण | समाधान |
|-------|-------|-----|
| पैटर्न नहीं दिख रहा है | गलत `PatternId` रेफ़रेंस | सुनिश्चित करें कि `PattResource` पर सेट किया गया `PatternId` `PatternFillSettings` में उपयोग किए गए से मेल खाता हो। |
| सेव करने के बाद Stroke गायब हो जाता है | Opacity 0 पर सेट है या इफ़ेक्ट छिपा हुआ है | जाँचें कि `setOpacity` 0‑255 के बीच है और `isVisible()` `true` लौटाता है। |
| अप्रत्याशित रंग | Blend mode मेल नहीं खाता | अपने डिज़ाइन इरादे के अनुसार `BlendMode.Color` (या कोई अन्य मोड) उपयोग करें। |

## FAQ's
### Aspose.PSD for Java क्या है?
Aspose.PSD for Java एक लाइब्रेरी है जो डेवलपर्स को प्रोग्रामेटिकली PSD (Photoshop Document) फ़ाइलें बनाने, संपादित करने और कनवर्ट करने की अनुमति देती है।

### क्या मैं Aspose.PSD for Java को एक व्यावसायिक प्रोजेक्ट में उपयोग कर सकता हूँ?
हाँ, आप इसे व्यावसायिक प्रोजेक्ट्स में उपयोग कर सकते हैं। आप लाइसेंस [here](https://purchase.aspose.com/buy) से खरीद सकते हैं।

### क्या Aspose.PSD for Java के लिए कोई फ्री ट्रायल उपलब्ध है?
हाँ, आप फ्री ट्रायल संस्करण [here](https://releases.aspose.com/) से डाउनलोड कर सकते हैं।

### मैं Aspose.PSD for Java के लिए सपोर्ट कैसे प्राप्त कर सकता हूँ?
आप Aspose कम्युनिटी फ़ोरम्स से सपोर्ट प्राप्त कर सकते हैं [here](https://forum.aspose.com/c/psd/34)।

### Aspose.PSD for Java की सिस्टम आवश्यकताएँ क्या हैं?
आपको JDK स्थापित होना चाहिए और विकास के लिए एक IDE चाहिए। यह लाइब्रेरी कई ऑपरेटिंग सिस्टम्स को सपोर्ट करती है, जिसमें Windows, Linux, और macOS शामिल हैं।

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-17  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose