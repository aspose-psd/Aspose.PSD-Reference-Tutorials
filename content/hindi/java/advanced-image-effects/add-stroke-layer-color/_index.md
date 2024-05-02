---
title: Java के लिए Aspose.PSD में स्ट्रोक लेयर कलर जोड़ें
linktitle: स्ट्रोक परत रंग जोड़ें
second_title: Aspose.PSD जावा एपीआई
description: स्ट्रोक लेयर रंग जोड़ने पर हमारी चरण-दर-चरण मार्गदर्शिका के साथ जावा के लिए Aspose.PSD की शक्ति का अन्वेषण करें। अपने ग्राफ़िक डिज़ाइन को सहजता से उन्नत करें।
type: docs
weight: 14
url: /hi/java/advanced-image-effects/add-stroke-layer-color/
---
## परिचय

Aspose.PSD के साथ अपने जावा एप्लिकेशन के ग्राफ़िक डिज़ाइन की क्षमता को अनलॉक करें। इस ट्यूटोरियल में, हम जावा के लिए Aspose.PSD का उपयोग करके स्ट्रोक लेयर रंग जोड़ने की आकर्षक दुनिया के बारे में जानेंगे। पॉप स्ट्रोक्स के साथ अपने ग्राफ़िक्स को बेहतर बनाएं और सहजता से आकर्षक डिज़ाइन बनाएं।

## आवश्यक शर्तें

इस रचनात्मक यात्रा को शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित शर्तें हैं:

-  Aspose.PSD लाइब्रेरी: निम्नलिखित का पालन करके Aspose.PSD लाइब्रेरी डाउनलोड करें और सेट करें[प्रलेखन](https://reference.aspose.com/psd/java/).

- जावा डेवलपमेंट किट (जेडीके): सुनिश्चित करें कि आपके सिस्टम पर जावा स्थापित है।

- एकीकृत विकास पर्यावरण (आईडीई): अपनी पसंद का एक आईडीई चुनें; एक्लिप्स या IntelliJ लोकप्रिय विकल्प हैं।

## पैकेज आयात करें

आइए Aspose.PSD को जादुई बनाने के लिए आवश्यक पैकेजों को आयात करके शुरुआत करें।

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

अपनी पसंदीदा आईडीई में एक नया जावा प्रोजेक्ट बनाकर शुरुआत करें। सुनिश्चित करें कि Aspose.PSD लाइब्रेरी आपके प्रोजेक्ट में जोड़ी गई है।

## चरण 2: PSD फ़ाइल लोड करें

Aspose.PSD का उपयोग करके PSD फ़ाइल लोड करें, जिससे प्रभाव संसाधनों की लोडिंग सक्षम हो सके।

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## चरण 3: स्ट्रोक परत तक पहुंचें

PSD फ़ाइल के भीतर स्ट्रोक प्रभाव परत तक पहुंचें।

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## चरण 4: स्ट्रोक गुणों को मान्य करें

सुनिश्चित करें कि स्ट्रोक गुण अपेक्षा के अनुरूप हैं।

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

## चरण 5: रंग और अपारदर्शिता सेट करें

स्ट्रोक परत के रंग और अपारदर्शिता को संशोधित करें।

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

## चरण 6: संशोधित PSD सहेजें

संशोधित PSD फ़ाइल को नए जोड़े गए स्ट्रोक लेयर रंग के साथ सहेजें।

```java
im.save(exportPath);
```

## निष्कर्ष

बधाई हो! आपने जावा के लिए Aspose.PSD का उपयोग करके सफलतापूर्वक अपनी PSD फ़ाइल में स्ट्रोक लेयर रंग जोड़ा है। अपने ग्राफ़िक डिज़ाइन को जीवंत बनाने के लिए विभिन्न रंगों और सेटिंग्स के साथ प्रयोग करें।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं अन्य जावा ग्राफ़िक लाइब्रेरीज़ के साथ Aspose.PSD का उपयोग कर सकता हूँ?

A1: हाँ, Aspose.PSD को उन्नत कार्यक्षमता के लिए अन्य जावा ग्राफ़िक लाइब्रेरीज़ के साथ एकीकृत किया जा सकता है।

### Q2: क्या Aspose.PSD नवीनतम PSD फ़ाइल स्वरूप के साथ संगत है?

ए2: बिल्कुल! Aspose.PSD अनुकूलता सुनिश्चित करते हुए नवीनतम PSD फ़ाइल प्रारूप विनिर्देशों के साथ तालमेल रखता है।

### Q3: Aspose.PSD का उपयोग करते समय मैं अपवादों को कैसे संभालूं?

 A3: का संदर्भ लें[सहयता मंच](https://forum.aspose.com/c/psd/34) अपवादों से निपटने और समस्या निवारण में सहायता के लिए।

### Q4: क्या मैं खरीदने से पहले Aspose.PSD आज़मा सकता हूँ?

 ए4: निश्चित रूप से! एक पकड़ो[मुफ्त परीक्षण](https://releases.aspose.com/) प्रतिबद्धता बनाने से पहले Aspose.PSD की विशेषताओं का पता लगाना।

### Q5: मुझे Aspose.PSD के लिए अस्थायी लाइसेंस कहां मिल सकता है?

 ए5: ए प्राप्त करें[अस्थायी लाइसेंस](https://purchase.aspose.com/temporary-license/) आपकी परियोजनाओं में Aspose.PSD की क्षमताओं का मूल्यांकन करने के लिए।