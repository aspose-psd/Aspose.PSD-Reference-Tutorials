---
title: .NET के लिए Aspose.PSD में छवियों में ग्रेडिएंट प्रभाव जोड़ना
linktitle: छवियों में ग्रेडिएंट प्रभाव जोड़ना
second_title: Aspose.PSD .NET एपीआई
description: .NET के लिए Aspose.PSD का उपयोग करके मनमोहक ग्रेडिएंट प्रभावों के साथ अपनी छवियों को बेहतर बनाएँ। रचनात्मक दृश्य परिवर्तनों के लिए हमारे चरण-दर-चरण ट्यूटोरियल का पालन करें।
type: docs
weight: 11
url: /hi/net/image-manipulation/adding-gradient-effects/
---
## परिचय

ग्रेडिएंट इफ़ेक्ट के साथ इमेज को बेहतर बनाना आपके विज़ुअल कंटेंट में एक आकर्षक आयाम जोड़ सकता है। .NET के लिए Aspose.PSD आपकी इमेज में ग्रेडिएंट ओवरले को शामिल करने के लिए एक शक्तिशाली प्लेटफ़ॉर्म प्रदान करता है। इस ट्यूटोरियल में, हम आपको .NET के लिए Aspose.PSD का उपयोग करके ग्रेडिएंट इफ़ेक्ट जोड़ने की प्रक्रिया के बारे में बताएंगे।

## आवश्यक शर्तें

ट्यूटोरियल में शामिल होने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

-  Aspose.PSD for .NET लाइब्रेरी: लाइब्रेरी को डाउनलोड करें और इंस्टॉल करें[.NET के लिए Aspose.PSD दस्तावेज़ीकरण](https://reference.aspose.com/psd/net/).
- .NET वातावरण: सुनिश्चित करें कि आपके मशीन पर कार्यशील .NET वातावरण स्थापित है।

## नामस्थान आयात करें

अपने प्रोजेक्ट में आवश्यक नामस्थानों को आयात करके आरंभ करें:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using System;
using Aspose.PSD.FileFormats.Core.Blending;
using System.IO;
```

## चरण 1: छवि लोड करें और पथ परिभाषित करें

```csharp
// दस्तावेज़ निर्देशिका का पथ.
string SourceDir = "Your Document Directory";
string OutputDir = "Your Output Directory";

string sourceFileName = Path.Combine(SourceDir, "GradientOverlay.psd");
string exportPath = Path.Combine(OutputDir, "GradientOverlayChanged.psd");

var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};
```

## चरण 2: प्रारंभिक सेटिंग्स का दावा करें

सुनिश्चित करें कि ग्रेडिएंट ओवरले की प्रारंभिक सेटिंग्स अपेक्षा के अनुरूप हैं:

```csharp
using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    var gradientOverlay = (GradientOverlayEffect)im.Layers[1].BlendingOptions.Effects[0];

    // प्रारंभिक सेटिंग्स के लिए अभिकथन जाँच
    // ...

    // रंग बिंदु
    // ...

    //पारदर्शिता बिंदु
    // ...
}
```

## चरण 3: ग्रेडिएंट ओवरले सेटिंग्स संशोधित करें

अपनी पसंद के अनुसार ग्रेडिएंट ओवरले सेटिंग्स समायोजित करें:

```csharp
// परीक्षण संपादन
settings.Color = Color.Green;

gradientOverlay.Opacity = 193;
gradientOverlay.BlendMode = BlendMode.Lighten;

settings.AlignWithLayer = false;
settings.GradientType = GradientType.Radial;
settings.Angle = 45;
settings.Dither = true;
settings.HorizontalOffset = 15;
settings.VerticalOffset = 11;
settings.Reverse = true;

// नया रंग बिंदु जोड़ें
// ...

// पिछले बिंदु का स्थान बदलें
// ...

// नया पारदर्शिता बिंदु जोड़ें
// ...

// पिछले पारदर्शिता बिंदु का स्थान बदलें
// ...

im.Save(exportPath);
```

## चरण 4: संपादित फ़ाइल को मान्य करें

जाँचें कि क्या संशोधन सफलतापूर्वक लागू किए गए:

```csharp
// संपादन के बाद फ़ाइल का परीक्षण करें
using (var im = (PsdImage)Image.Load(exportPath, loadOptions))
{
    var gradientOverlay = (GradientOverlayEffect)im.Layers[1].BlendingOptions.Effects[0];
    try
    {
        // संशोधित सेटिंग्स के लिए अभिकथन जाँच
        // ...
    }
    catch (Exception e)
    {
        string ex = e.StackTrace;
    }
}
```

## निष्कर्ष

.NET के लिए Aspose.PSD का उपयोग करके छवियों में ग्रेडिएंट प्रभाव जोड़ना रचनात्मक संभावनाओं की एक दुनिया खोलता है। अपनी छवियों में वांछित दृश्य प्रभाव प्राप्त करने के लिए विभिन्न सेटिंग्स के साथ प्रयोग करें।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: क्या मैं एक साथ कई परतों पर ग्रेडिएंट प्रभाव लागू कर सकता हूँ?

A1: हां, आप प्रत्येक परत पर पुनरावृत्ति करके और वांछित सेटिंग्स लागू करके कई परतों पर ग्रेडिएंट प्रभाव लागू कर सकते हैं।

### प्रश्न 2: Aspose.PSD for .NET किस फ़ाइल स्वरूप का समर्थन करता है?

A2: .NET के लिए Aspose.PSD PSD, PNG, JPEG, BMP, और GIF सहित विभिन्न छवि फ़ाइल स्वरूपों का समर्थन करता है।

### प्रश्न 3: क्या .NET के लिए Aspose.PSD का कोई परीक्षण संस्करण उपलब्ध है?

A3: हाँ, आप यहाँ से निःशुल्क परीक्षण डाउनलोड करके .NET के लिए Aspose.PSD की क्षमताओं का पता लगा सकते हैं।[यहाँ](https://releases.aspose.com/).

### प्रश्न 4: मैं .NET के लिए Aspose.PSD का समर्थन कैसे प्राप्त कर सकता हूं?

 A4: किसी भी सहायता या प्रश्न के लिए, पर जाएँ[Aspose.PSD for .NET समर्थन फ़ोरम](https://forum.aspose.com/c/psd/34).

### प्रश्न 5: मैं .NET के लिए Aspose.PSD कहां से खरीद सकता हूं?

 A5: आप लाइब्रेरी को यहाँ से खरीद सकते हैं[Aspose.PSD for .NET खरीद पृष्ठ](https://purchase.aspose.com/buy).