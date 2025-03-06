---
title: Java के लिए Aspose.PSD में स्ट्रोक लेयर रंग जोड़ें
linktitle: स्ट्रोक लेयर रंग जोड़ें
second_title: Aspose.PSD जावा एपीआई
description: स्ट्रोक लेयर कलर जोड़ने पर हमारे चरण-दर-चरण गाइड के साथ Java के लिए Aspose.PSD की शक्ति का अन्वेषण करें। अपने ग्राफ़िक डिज़ाइन को आसानी से बढ़ाएँ।
weight: 14
url: /hi/java/advanced-image-effects/add-stroke-layer-color/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java के लिए Aspose.PSD में स्ट्रोक लेयर रंग जोड़ें

## परिचय

Aspose.PSD के साथ अपने Java एप्लिकेशन के ग्राफ़िक डिज़ाइन की क्षमता को अनलॉक करें। इस ट्यूटोरियल में, हम Java के लिए Aspose.PSD का उपयोग करके स्ट्रोक लेयर कलर जोड़ने की आकर्षक दुनिया में उतरेंगे। अपने ग्राफ़िक्स को पॉप स्ट्रोक के साथ बढ़ाएँ, जिससे आसानी से आकर्षक डिज़ाइन बन सकें।

## आवश्यक शर्तें

इस रचनात्मक यात्रा पर निकलने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

-  Aspose.PSD लाइब्रेरी: नीचे दिए गए निर्देशों का पालन करके Aspose.PSD लाइब्रेरी को डाउनलोड करें और सेट अप करें।[प्रलेखन](https://reference.aspose.com/psd/java/).

- जावा डेवलपमेंट किट (JDK): सुनिश्चित करें कि आपके सिस्टम पर जावा स्थापित है।

- एकीकृत विकास वातावरण (आईडीई): अपनी पसंद का आईडीई चुनें; इक्लिप्स या इंटेलीज लोकप्रिय विकल्प हैं।

## पैकेज आयात करें

आइए Aspose.PSD को कारगर बनाने के लिए आवश्यक पैकेजों को आयात करके शुरुआत करें।

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

## चरण 1: अपना प्रोजेक्ट सेट करें

अपने पसंदीदा IDE में एक नया Java प्रोजेक्ट बनाकर शुरू करें। सुनिश्चित करें कि Aspose.PSD लाइब्रेरी आपके प्रोजेक्ट में जोड़ी गई है।

## चरण 2: PSD फ़ाइल लोड करें

Aspose.PSD का उपयोग करके PSD फ़ाइल लोड करें, जिससे प्रभाव संसाधनों को लोड करना सक्षम हो सके।

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## चरण 3: स्ट्रोक परत तक पहुँचें

PSD फ़ाइल के भीतर स्ट्रोक प्रभाव परत तक पहुँचें।

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## चरण 4: स्ट्रोक गुणों को मान्य करें

सुनिश्चित करें कि स्ट्रोक गुण अपेक्षित अनुसार हों।

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

## चरण 5: रंग और अपारदर्शिता सेट करें

स्ट्रोक परत का रंग और अपारदर्शिता संशोधित करें.

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

## चरण 6: संशोधित PSD को सहेजें

संशोधित PSD फ़ाइल को नए जोड़े गए स्ट्रोक परत रंग के साथ सहेजें।

```java
im.save(exportPath);
```

## निष्कर्ष

बधाई हो! आपने Aspose.PSD for Java का उपयोग करके अपनी PSD फ़ाइल में स्ट्रोक लेयर रंग सफलतापूर्वक जोड़ लिया है। अपने ग्राफ़िक डिज़ाइन को जीवंत बनाने के लिए अलग-अलग रंगों और सेटिंग्स के साथ प्रयोग करें।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: क्या मैं अन्य जावा ग्राफ़िक लाइब्रेरीज़ के साथ Aspose.PSD का उपयोग कर सकता हूँ?

A1: हाँ, Aspose.PSD को उन्नत कार्यक्षमता के लिए अन्य जावा ग्राफ़िक लाइब्रेरीज़ के साथ एकीकृत किया जा सकता है।

### प्रश्न 2: क्या Aspose.PSD नवीनतम PSD फ़ाइल प्रारूप के साथ संगत है?

A2: बिल्कुल! Aspose.PSD नवीनतम PSD फ़ाइल प्रारूप विनिर्देशों के साथ तालमेल बनाए रखता है, जिससे संगतता सुनिश्चित होती है।

### प्रश्न 3: Aspose.PSD का उपयोग करते समय मैं अपवादों को कैसे संभालूँ?

 A3: देखें[सहयता मंच](https://forum.aspose.com/c/psd/34) अपवादों से निपटने और समस्या निवारण में सहायता के लिए।

### प्रश्न 4: क्या मैं खरीदने से पहले Aspose.PSD आज़मा सकता हूँ?

 A4: ज़रूर![मुफ्त परीक्षण](https://releases.aspose.com/) प्रतिबद्धता बनाने से पहले Aspose.PSD की सुविधाओं का पता लगाने के लिए।

### प्रश्न 5: मैं Aspose.PSD के लिए अस्थायी लाइसेंस कहां से प्राप्त कर सकता हूं?

 A5: प्राप्त करें[अस्थायी लाइसेंस](https://purchase.aspose.com/temporary-license/) Aspose.PSD को अपनी परियोजनाओं में इसकी क्षमताओं का मूल्यांकन करने के लिए।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
