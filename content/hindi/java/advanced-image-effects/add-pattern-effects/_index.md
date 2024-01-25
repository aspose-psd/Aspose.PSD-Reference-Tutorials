---
title: जावा के लिए Aspose.PSD में पैटर्न प्रभाव जोड़ें
linktitle: पैटर्न प्रभाव जोड़ें
second_title: Aspose.PSD जावा एपीआई
description: जावा के लिए Aspose.PSD के साथ अपने जावा छवि पैटर्न को आसानी से बढ़ाएं। मनमोहक पैटर्न प्रभाव जोड़ने के लिए हमारे चरण-दर-चरण ट्यूटोरियल का पालन करें।
type: docs
weight: 12
url: /hi/java/advanced-image-effects/add-pattern-effects/
---
## परिचय

जावा विकास की दुनिया में, छवि पैटर्न को बढ़ाना एक सामान्य कार्य है, और जावा के लिए Aspose.PSD इसके लिए एक मजबूत समाधान प्रदान करता है। यह ट्यूटोरियल आपको Aspose.PSD का उपयोग करके पैटर्न प्रभाव जोड़ने की प्रक्रिया के माध्यम से मार्गदर्शन करेगा, यह सुनिश्चित करते हुए कि आपकी छवियां अद्वितीय ओवरले और संवर्द्धन के साथ खड़ी होंगी।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

- आपके सिस्टम पर जावा डेवलपमेंट किट (जेडीके) स्थापित है।
-  जावा लाइब्रेरी के लिए Aspose.PSD डाउनलोड किया गया और आपके प्रोजेक्ट में जोड़ा गया। आप इसे यहां से डाउनलोड कर सकते हैं[Aspose.PSD वेबसाइट](https://releases.aspose.com/psd/java/).

## पैकेज आयात करें

अपने जावा प्रोजेक्ट में, Aspose.PSD के साथ काम करने के लिए आवश्यक पैकेज आयात करें। अपनी जावा क्लास की शुरुआत में निम्नलिखित कोड शामिल करें:

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

अपने प्रोजेक्ट में "YourImagePath" और "YourExportPath" को वास्तविक पथों से बदलना सुनिश्चित करें।

## चरण 2: पैटर्न ओवरले जानकारी निकालें

```java
// पैटर्न ओवरले के बारे में जानकारी निकालें
PatternOverlayEffect patternOverlay = (PatternOverlayEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## चरण 3: पैटर्न ओवरले सेटिंग्स को संशोधित करें

```java
// पैटर्न ओवरले सेटिंग्स संशोधित करें
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

## चरण 5: संपादित छवि सहेजें

```java
// संपादित छवि सहेजें
settings.setPatternName(newPatternName);
settings.setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

## चरण 6: परिवर्तनों को सत्यापित करें

```java
// संपादित फ़ाइल में परिवर्तन सत्यापित करें
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
PatternOverlayEffect patternOverlayEffect = (PatternOverlayEffect)img.getLayers()[1].getBlendingOptions().getEffects()[0];

// यह सुनिश्चित करने के लिए दावे जोड़ें कि परिवर्तन सफलतापूर्वक लागू किए गए हैं
```

## निष्कर्ष

बधाई हो! आपने जावा के लिए Aspose.PSD का उपयोग करके पैटर्न प्रभाव जोड़ने का तरीका सफलतापूर्वक सीख लिया है। यह शक्तिशाली लाइब्रेरी आपको अनुकूलित पैटर्न के साथ दिखने में आकर्षक छवियां बनाने की अनुमति देती है, जो आपके जावा-आधारित प्रोजेक्टों के लिए अनंत संभावनाएं प्रदान करती है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं अन्य जावा इमेज प्रोसेसिंग लाइब्रेरी के साथ जावा के लिए Aspose.PSD का उपयोग कर सकता हूँ?

A1: जावा के लिए Aspose.PSD को स्वतंत्र रूप से काम करने के लिए डिज़ाइन किया गया है, लेकिन ज़रूरत पड़ने पर आप इसे अन्य जावा लाइब्रेरी के साथ एकीकृत कर सकते हैं।

### Q2: मैं जावा के लिए Aspose.PSD के लिए विस्तृत दस्तावेज़ कहां पा सकता हूं?

 A2: देखें[जावा दस्तावेज़ीकरण के लिए Aspose.PSD](https://reference.aspose.com/psd/java/) विस्तृत जानकारी के लिए.

### Q3: क्या Java के लिए Aspose.PSD का निःशुल्क परीक्षण उपलब्ध है?

 उ3: हाँ, आप नि:शुल्क परीक्षण का उपयोग कर सकते हैं[यहाँ](https://releases.aspose.com/).

### Q4: मैं जावा के लिए Aspose.PSD के लिए समर्थन कैसे प्राप्त कर सकता हूं?

 A4: पर जाएँ[Aspose.PSD फोरम](https://forum.aspose.com/c/psd/34) सामुदायिक सहायता के लिए या एक सहायता योजना खरीदने पर विचार करें।

### Q5: क्या मैं जावा के लिए Aspose.PSD के लिए अस्थायी लाइसेंस प्राप्त कर सकता हूँ?

A5: हाँ, आप अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).