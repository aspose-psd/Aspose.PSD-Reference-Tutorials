---
title: .NET के लिए Aspose.PSD में ग्रेडिएंट ओवरले इफ़ेक्ट का समर्थन करना
linktitle: ग्रेडिएंट ओवरले प्रभाव का समर्थन करना
second_title: Aspose.PSD .NET एपीआई
description: Aspose.PSD के साथ .NET में ग्राफ़िक्स बढ़ाएँ। यह ट्यूटोरियल ग्रेडिएंट ओवरले इफेक्ट्स का समर्थन करने में आपका मार्गदर्शन करता है।
type: docs
weight: 18
url: /hi/net/image-manipulation/supporting-gradient-overlay-effect/
---
## परिचय

.NET के लिए Aspose.PSD में ग्रेडिएंट ओवरले इफ़ेक्ट का समर्थन करने पर इस व्यापक ट्यूटोरियल में आपका स्वागत है! यदि आप अपने .NET एप्लिकेशन की ग्राफिक क्षमताओं को बढ़ाना चाहते हैं, तो यह चरण-दर-चरण मार्गदर्शिका आपकी सहायता के लिए यहां है। हम Aspose.PSD, एक शक्तिशाली लाइब्रेरी जो छवि प्रसंस्करण को सरल बनाती है, का उपयोग करके एक परत में ग्रेडिएंट ओवरले इफ़ेक्ट बनाने और संपादित करने की जटिलताओं को समझेंगे।

## आवश्यक शर्तें

इससे पहले कि हम इस यात्रा पर निकलें, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

- C# और .NET प्रोग्रामिंग की बुनियादी समझ।
-  .NET के लिए Aspose.PSD स्थापित। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/psd/net/).
- आपके पसंदीदा आईडीई के साथ एक विकास वातावरण स्थापित किया गया है।

## नामस्थान आयात करें

आरंभ करने के लिए, आइए आपके C# कोड में आवश्यक नामस्थान आयात करें:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using System;
using System.IO;
using Aspose.PSD.FileFormats.Core.Blending;
```

अब जब हमने मूल बातें कवर कर ली हैं, तो आइए प्रत्येक चरण को विस्तार से देखें:

## चरण 1: PSD छवि लोड करें

```csharp
// दस्तावेज़ निर्देशिका का पथ.
string SourceDir = "Your Document Directory";
string OutputDir = "Your Output Directory";

string sourceFilePath = Path.Combine(SourceDir, "psdnet256.psd");
string outputFilePath = Path.Combine(OutputDir, "psdnet256.psd_output.psd");

using (var psdImage = (PsdImage)Image.Load(sourceFilePath, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    // अगले चरणों के लिए कोड यहां दिया गया है...
}
```

## चरण 2: एक्सेस लेयर ब्लेंडिंग विकल्प

```csharp
BlendingOptions layerBlendOptions = psdImage.Layers[1].BlendingOptions;
```

## चरण 3: ग्रेडिएंट ओवरले प्रभाव ढूंढें या बनाएं

```csharp
GradientOverlayEffect gradientOverlayEffect = null;

foreach (ILayerEffect effect in layerBlendOptions.Effects)
{
    gradientOverlayEffect = effect as GradientOverlayEffect;
    if (gradientOverlayEffect != null)
    {
        break;
    }
}

if (gradientOverlayEffect == null)
{
    gradientOverlayEffect = layerBlendOptions.AddGradientOverlay();
}
```

## चरण 4: ग्रेडिएंट ओवरले प्रभाव कॉन्फ़िगर करें

```csharp
gradientOverlayEffect.Opacity = 200;
gradientOverlayEffect.BlendMode = BlendMode.Hue;

GradientFillSettings settings = gradientOverlayEffect.Settings;

settings.ColorPoints = new IGradientColorPoint[]
{
    new GradientColorPoint(Color.GreenYellow, 0, 50),
    new GradientColorPoint(Color.BlueViolet, 4096, 50),
};

settings.Angle = 80;
settings.Scale = 150;
settings.GradientType = GradientType.Linear;

settings.TransparencyPoints[0].Opacity = 100;
settings.TransparencyPoints[1].Opacity = 100;
```

## चरण 5: संशोधित छवि सहेजें

```csharp
psdImage.Save(outputFilePath);
```

इतना ही! आपने .NET के लिए Aspose.PSD का उपयोग करके एक परत में ग्रेडिएंट ओवरले इफ़ेक्ट सफलतापूर्वक जोड़ दिया है।

## निष्कर्ष

इस ट्यूटोरियल में, हमने .NET के लिए Aspose.PSD में ग्रेडिएंट ओवरले इफ़ेक्ट का समर्थन करने की प्रक्रिया का पता लगाया। चरण-दर-चरण मार्गदर्शिका का पालन करके, आप इस सुविधा को अपने .NET अनुप्रयोगों में सहजता से एकीकृत कर सकते हैं, जिससे आपकी छवियों की दृश्य अपील बढ़ जाएगी।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.PSD .NET के सभी संस्करणों के साथ संगत है?

A1: .NET के लिए Aspose.PSD .NET फ्रेमवर्क और .NET कोर के साथ संगत है।

### Q2: क्या मैं एक ही परत पर अनेक प्रभाव लागू कर सकता हूँ?

उ2: हाँ, आप ग्रेडिएंट ओवरले सहित विभिन्न प्रभावों को एक ही परत पर लागू कर सकते हैं।

### Q3: मुझे और अधिक उदाहरण और दस्तावेज़ कहां मिल सकते हैं?

 A3: पर जाएँ[प्रलेखन](https://reference.aspose.com/psd/net/) विस्तृत उदाहरणों और दिशानिर्देशों के लिए।

### Q4: क्या कोई निःशुल्क परीक्षण उपलब्ध है?

 उ4: हाँ, आप निःशुल्क परीक्षण का उपयोग कर सकते हैं[यहाँ](https://releases.aspose.com/).

### Q5: मैं Aspose.PSD के लिए समर्थन कैसे प्राप्त कर सकता हूं?

 A5: पर जाएँ[Aspose.PSD फोरम](https://forum.aspose.com/c/psd/34) सामुदायिक समर्थन के लिए.