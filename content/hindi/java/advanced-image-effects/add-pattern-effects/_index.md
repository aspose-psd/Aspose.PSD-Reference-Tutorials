---
title: Java के लिए Aspose.PSD में पैटर्न प्रभाव जोड़ें
linktitle: पैटर्न प्रभाव जोड़ें
second_title: Aspose.PSD जावा एपीआई
description: Aspose.PSD for Java के साथ अपने Java इमेज पैटर्न को आसानी से बेहतर बनाएँ। आकर्षक पैटर्न प्रभाव जोड़ने के लिए हमारे चरण-दर-चरण ट्यूटोरियल का पालन करें।
type: docs
weight: 12
url: /hi/java/advanced-image-effects/add-pattern-effects/
---
## परिचय

जावा डेवलपमेंट की दुनिया में, इमेज पैटर्न को बेहतर बनाना एक आम काम है, और जावा के लिए Aspose.PSD इसके लिए एक मज़बूत समाधान प्रदान करता है। यह ट्यूटोरियल आपको Aspose.PSD का उपयोग करके पैटर्न इफ़ेक्ट जोड़ने की प्रक्रिया के माध्यम से मार्गदर्शन करेगा, यह सुनिश्चित करते हुए कि आपकी छवियाँ अद्वितीय ओवरले और संवर्द्धन के साथ अलग दिखाई दें।

## आवश्यक शर्तें

ट्यूटोरियल में शामिल होने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

- आपके सिस्टम पर जावा डेवलपमेंट किट (JDK) स्थापित है।
-  Aspose.PSD for Java लाइब्रेरी डाउनलोड हो गई है और आपके प्रोजेक्ट में जोड़ दी गई है। आप इसे यहाँ से डाउनलोड कर सकते हैं[Aspose.PSD वेबसाइट](https://releases.aspose.com/psd/java/).

## पैकेज आयात करें

अपने जावा प्रोजेक्ट में, Aspose.PSD के साथ काम करने के लिए आवश्यक पैकेज आयात करें। अपने जावा क्लास की शुरुआत में निम्नलिखित कोड शामिल करें:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.PatternOverlayEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;

import java.util.UUID;
```

## चरण 1: छवि लोड करें

```java
// PSD छवि लोड करें
String sourceFileName = "YourImagePath/PatternOverlay.psd";
String exportPath = "YourExportPath/PatternOverlayChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

सुनिश्चित करें कि "YourImagePath" और "YourExportPath" को आपके प्रोजेक्ट में वास्तविक पथों से प्रतिस्थापित किया गया है।

## चरण 2: पैटर्न ओवरले जानकारी निकालें

```java
// पैटर्न ओवरले के बारे में जानकारी निकालें
PatternOverlayEffect patternOverlay = (PatternOverlayEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## चरण 3: पैटर्न ओवरले सेटिंग्स संशोधित करें

```java
// पैटर्न ओवरले सेटिंग संशोधित करें
PatternFillSettings settings = patternOverlay.getSettings();
settings.setColor(Color.getGreen());
patternOverlay.setOpacity((byte)193);
patternOverlay.setBlendMode(BlendMode.Difference);
settings.setHorizontalOffset(15);
settings.setVerticalOffset(11);
```

## चरण 4: पैटर्न डेटा संपादित करें

```java
// पैटर्न डेटा संपादित करें
PattResource resource;
UUID guid = UUID.randomUUID();
String newPatternName = "$$/Presets/Patterns/Pattern=Some new pattern name\0";

for (int i = 0; i < im.getGlobalLayerResources().length; i++) {
    if (im.getGlobalLayerResources()[i] instanceof PattResource) {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName(newPatternName);
        resource.setPattern(new int[]{Color.getAqua().toArgb(), Color.getRed().toArgb(),
                        Color.getRed().toArgb(), Color.getAqua().toArgb(),
                        Color.getAqua().toArgb(), Color.getWhite().toArgb(),
                        Color.getWhite().toArgb(), Color.getAqua().toArgb()}, new Rectangle(0, 0, 4, 2));
    }
}
```

## चरण 5: संपादित छवि को सहेजें

```java
// संपादित छवि सहेजें
settings.setPatternName(newPatternName);
settings.setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

## चरण 6: परिवर्तनों को सत्यापित करें

```java
// संपादित फ़ाइल में किए गए परिवर्तनों को सत्यापित करें
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
PatternOverlayEffect patternOverlayEffect = (PatternOverlayEffect)img.getLayers()[1].getBlendingOptions().getEffects()[0];

// यह सुनिश्चित करने के लिए दावे जोड़ें कि परिवर्तन सफलतापूर्वक लागू हो गए हैं
```

## निष्कर्ष

बधाई हो! आपने सफलतापूर्वक सीख लिया है कि Java के लिए Aspose.PSD का उपयोग करके पैटर्न प्रभाव कैसे जोड़ें। यह शक्तिशाली लाइब्रेरी आपको अनुकूलित पैटर्न के साथ नेत्रहीन आकर्षक छवियां बनाने की अनुमति देती है, जो आपके Java-आधारित प्रोजेक्ट्स के लिए अनंत संभावनाएं प्रदान करती है।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: क्या मैं अन्य Java इमेज प्रोसेसिंग लाइब्रेरीज़ के साथ Java के लिए Aspose.PSD का उपयोग कर सकता हूँ?

A1: Java के लिए Aspose.PSD को स्वतंत्र रूप से काम करने के लिए डिज़ाइन किया गया है, लेकिन यदि आवश्यक हो तो आप इसे अन्य Java लाइब्रेरीज़ के साथ एकीकृत कर सकते हैं।

### प्रश्न 2: मैं Java के लिए Aspose.PSD के लिए विस्तृत दस्तावेज़ कहां पा सकता हूं?

 A2: देखें[Aspose.PSD for Java दस्तावेज़ीकरण](https://reference.aspose.com/psd/java/) विस्तृत जानकारी के लिए.

### प्रश्न 3: क्या Java के लिए Aspose.PSD का निःशुल्क परीक्षण उपलब्ध है?

 A3: हां, आप निःशुल्क परीक्षण का लाभ उठा सकते हैं[यहाँ](https://releases.aspose.com/).

### प्रश्न 4: मैं Java के लिए Aspose.PSD का समर्थन कैसे प्राप्त कर सकता हूं?

 A4: पर जाएँ[Aspose.PSD फ़ोरम](https://forum.aspose.com/c/psd/34) सामुदायिक सहायता के लिए संपर्क करें या सहायता योजना खरीदने पर विचार करें।

### प्रश्न 5: क्या मैं Java के लिए Aspose.PSD हेतु अस्थायी लाइसेंस प्राप्त कर सकता हूँ?

A5: हां, आप अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).