---
title: .NET के लिए Aspose.PSD में पैटर्न के साथ स्ट्रोक लेयर जोड़ना
linktitle: पैटर्न के साथ स्ट्रोक लेयर जोड़ना
second_title: Aspose.PSD .NET एपीआई
description: .NET के लिए Aspose.PSD का उपयोग करके स्ट्रोक लेयर्स और पैटर्न के साथ अपनी PSD फ़ाइलों को बेहतर बनाएँ। सहज एकीकरण के लिए हमारे चरण-दर-चरण गाइड का पालन करें।
weight: 13
url: /hi/net/layer-effects/adding-stroke-layer-pattern/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET के लिए Aspose.PSD में पैटर्न के साथ स्ट्रोक लेयर जोड़ना

## परिचय

स्ट्रोक लेयर्स और पैटर्न के साथ अपनी PSD (फ़ोटोशॉप डॉक्यूमेंट) फ़ाइलों को बेहतर बनाने से आपके डिज़ाइन में एक गतिशील स्पर्श जोड़ा जा सकता है। इस ट्यूटोरियल में, हम यह पता लगाएंगे कि .NET के लिए Aspose.PSD का लाभ कैसे उठाया जाए ताकि आसानी से अपनी PSD फ़ाइलों में पैटर्न के साथ स्ट्रोक लेयर को जोड़ा जा सके। Aspose.PSD एक शक्तिशाली .NET लाइब्रेरी है जो PSD फ़ाइलों में हेरफेर करने के लिए व्यापक समर्थन प्रदान करती है, जिससे यह डेवलपर्स और डिज़ाइनरों दोनों के लिए एक अमूल्य उपकरण बन जाता है।

## आवश्यक शर्तें

ट्यूटोरियल में शामिल होने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

- C# प्रोग्रामिंग भाषा का बुनियादी ज्ञान।
- आपके मशीन पर Visual Studio स्थापित है.
-  Aspose.PSD for .NET लाइब्रेरी, जिसे आप डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/psd/net/).

## नामस्थान आयात करें

सुनिश्चित करें कि आपने अपने C# कोड में आवश्यक नामस्थान आयात किए हैं:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.FileFormats.Psd.Layers.LayerResources;
using Aspose.PSD.ImageLoadOptions;
using System;
using Aspose.PSD.FileFormats.Core.Blending;
using System.IO;
```

## चरण 1: अपना वातावरण सेट करें

अपने C# कोड में स्रोत और आउटपुट निर्देशिकाओं को परिभाषित करके प्रारंभ करें:

```csharp
string SourceDir = "Your Document Directory";
string OutputDir = "Your Output Directory";
```

## चरण 2: PSD फ़ाइल लोड करें

Aspose.PSD के PsdImage वर्ग का उपयोग करके PSD फ़ाइल लोड करें:

```csharp
var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

string sourceFileName = Path.Combine(SourceDir, "Stroke.psd");
using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    // PSD फ़ाइल को प्रोसेस करने के लिए आपका कोड यहाँ है
}
```

## चरण 3: नया पैटर्न डेटा तैयार करें

एक नया पैटर्न और उसकी सीमाएँ परिभाषित करें:

```csharp
var newPattern = new int[]
{
    // आपके पैटर्न के रंग यहां हैं
};

var newPatternBounds = new Rectangle(0, 0, 4, 4);
var guid = Guid.NewGuid();
```

## चरण 4: स्ट्रोक परत को संशोधित करें

स्ट्रोक परत तक पहुंचें और इसके गुणों को अपडेट करें:

```csharp
var patternStroke = (StrokeEffect)im.Layers[3].BlendingOptions.Effects[0];

// स्ट्रोक गुणधर्मों की जांच करें और उन्हें अपडेट करें
// ...

// अपारदर्शिता और मिश्रण मोड अपडेट करें
patternStroke.Opacity = 127;
patternStroke.BlendMode = BlendMode.Color;
```

## चरण 5: पैटर्न जानकारी अपडेट करें

PSD फ़ाइल में पैटर्न जानकारी अपडेट करें:

```csharp
foreach (var globalLayerResource in im.GlobalLayerResources)
{
    if (globalLayerResource is PattResource)
    {
        // पैटर्न जानकारी अपडेट करने के लिए आपका कोड यहां है
    }
}

// संशोधित PSD फ़ाइल सहेजें
im.Save(exportPath);
```

## चरण 6: परिवर्तनों को सत्यापित करें

संशोधित PSD फ़ाइल लोड करें और परिवर्तनों को सत्यापित करें:

```csharp
using (var im = (PsdImage)Image.Load(exportPath, loadOptions))
{
    var patternStroke = (StrokeEffect)im.Layers[3].BlendingOptions.Effects[0];

    // परिवर्तनों को सत्यापित करने के लिए आपका कोड यहां दिया गया है
}
```

## निष्कर्ष

बधाई हो! आपने सफलतापूर्वक सीख लिया है कि Aspose.PSD for .NET में पैटर्न के साथ स्ट्रोक लेयर कैसे जोड़ें। यह बहुमुखी लाइब्रेरी डेवलपर्स को आकर्षक डिज़ाइन बनाने और PSD फ़ाइलों की लचीलापन बढ़ाने में सक्षम बनाती है।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: क्या मैं Visual Studio के किसी भी संस्करण के साथ .NET के लिए Aspose.PSD का उपयोग कर सकता हूँ?

A1: हाँ, .NET के लिए Aspose.PSD Visual Studio के विभिन्न संस्करणों के साथ संगत है।

### प्रश्न 2: मैं Aspose.PSD के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?

 A2: विजिट करें[यहाँ](https://purchase.aspose.com/temporary-license/) अस्थायी लाइसेंस प्राप्त करने के लिए।

### प्रश्न 3: क्या परीक्षण के लिए कोई नमूना PSD फ़ाइलें उपलब्ध हैं?

 A3: आप दस्तावेज़ में नमूना PSD फ़ाइलें पा सकते हैं[यहाँ](https://reference.aspose.com/psd/net/).

### प्रश्न 4: क्या Aspose.PSD PSD फ़ाइलों के बैच प्रसंस्करण के लिए उपयुक्त है?

A4: बिल्कुल, .NET के लिए Aspose.PSD बैच प्रोसेसिंग के लिए मजबूत समर्थन प्रदान करता है।

### प्रश्न 5: मैं सहायता कहां प्राप्त कर सकता हूं या सामुदायिक चर्चा में कहां भाग ले सकता हूं?

 A5: पर जाएँ[Aspose.PSD फ़ोरम](https://forum.aspose.com/c/psd/34) समर्थन और सामुदायिक बातचीत के लिए।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
