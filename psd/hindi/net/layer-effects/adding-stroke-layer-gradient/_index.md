---
title: .NET के लिए Aspose.PSD में ग्रेडिएंट के साथ स्ट्रोक लेयर जोड़ना
linktitle: ग्रेडिएंट के साथ स्ट्रोक लेयर जोड़ना
second_title: Aspose.PSD .NET एपीआई
description: जानें कि .NET के लिए Aspose.PSD में ग्रेडिएंट स्ट्रोक लेयर कैसे जोड़ें। इस व्यापक ट्यूटोरियल के साथ अपनी छवि हेरफेर कौशल को बढ़ाएं।
weight: 12
url: /hi/net/layer-effects/adding-stroke-layer-gradient/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET के लिए Aspose.PSD में ग्रेडिएंट के साथ स्ट्रोक लेयर जोड़ना

## परिचय

यदि आप अपने .NET एप्लीकेशन को शानदार ग्राफिक इफ़ेक्ट के साथ बेहतर बनाना चाहते हैं, तो Aspose.PSD for .NET आपके लिए सबसे अच्छा उपाय है। इस ट्यूटोरियल में, हम Aspose.PSD for .NET का उपयोग करके ग्रेडिएंट के साथ स्ट्रोक लेयर जोड़ने की प्रक्रिया के बारे में जानेंगे। यह चरण-दर-चरण मार्गदर्शिका आपको अपनी छवियों की दृश्य अपील को आसानी से बढ़ाने में सक्षम बनाएगी।

## आवश्यक शर्तें

इससे पहले कि हम इस यात्रा पर निकलें, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

- C# और .NET विकास का कार्यसाधक ज्ञान।
-  Aspose.PSD for .NET लाइब्रेरी स्थापित है। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/psd/net/).
- दिए गए उदाहरणों को क्रियान्वित करने के लिए एक कोड संपादक, जैसे कि विजुअल स्टूडियो।

## नामस्थान आयात करें

काम शुरू करने के लिए, आइए अपने प्रोजेक्ट में आवश्यक नेमस्पेस आयात करें। ये नेमस्पेस .NET के लिए Aspose.PSD की कार्यक्षमताओं का लाभ उठाने के लिए महत्वपूर्ण हैं।

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using System;
using Aspose.PSD.FileFormats.Core.Blending;
```

## चरण 1: दस्तावेज़ निर्देशिका सेट करें

कोड में अपने दस्तावेज़ निर्देशिका का पथ परिभाषित करके शुरू करें। यह सुनिश्चित करता है कि आवश्यक फ़ाइलें सही स्थान से लोड और सहेजी गई हैं।

```csharp
string dataDir = "Your Document Directory";
```

## चरण 2: PSD फ़ाइल लोड करें

.NET के लिए Aspose.PSD का उपयोग करके स्रोत PSD फ़ाइल लोड करें। सुनिश्चित करें कि परतों को प्रभावी ढंग से हेरफेर करने के लिए प्रभाव संसाधन लोड किया गया है।

```csharp
string sourceFileName = dataDir + "Stroke.psd";
string exportPath = dataDir + "StrokeGradientChanged.psd";

var loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true
};

using (var im = (PsdImage)Image.Load(sourceFileName, loadOptions))
{
    // PSD फ़ाइल को संभालने के लिए कोड यहाँ आता है
}
```

## चरण 3: ग्रेडिएंट स्ट्रोक सेटिंग्स सत्यापित करें

ब्लेंड मोड, अपारदर्शिता और दृश्यता जैसी विभिन्न सेटिंग्स की जांच करके सुनिश्चित करें कि ग्रेडिएंट के साथ स्ट्रोक परत सही ढंग से कॉन्फ़िगर की गई है।

```csharp
var gradientStroke = (StrokeEffect)im.Layers[2].BlendingOptions.Effects[0];

// ग्रेडिएंट स्ट्रोक सेटिंग्स के लिए अभिकथन जाँच
AssertIsTrue(gradientStroke.BlendMode == BlendMode.Normal);
AssertIsTrue(gradientStroke.Opacity == 255);
AssertIsTrue(gradientStroke.IsVisible);

// भरण सेटिंग के लिए अधिक अभिकथन जाँच
// ...
```

रंग बिंदुओं और पारदर्शिता बिंदुओं सहित अन्य भरण सेटिंग्स के लिए अभिकथन जांच को लागू करना जारी रखें।

## चरण 4: ग्रेडिएंट स्ट्रोक सेटिंग संपादित करें

अब, ग्रेडिएंट स्ट्रोक सेटिंग में कुछ बदलाव करते हैं। वांछित दृश्य प्रभाव प्राप्त करने के लिए रंग, अपारदर्शिता, मिश्रण मोड और ग्रेडिएंट प्रकार जैसे मापदंडों को संशोधित करें।

```csharp
// ग्रेडिएंट स्ट्रोक सेटिंग संशोधित करने के लिए कोड
// ...
```

## चरण 5: संपादित PSD फ़ाइल को सहेजें

संपादित PSD फ़ाइल को निर्दिष्ट निर्यात पथ पर सहेजें.

```csharp
im.Save(exportPath);
```

## निष्कर्ष

बधाई हो! आपने .NET के लिए Aspose.PSD का उपयोग करके ग्रेडिएंट के साथ एक स्ट्रोक लेयर सफलतापूर्वक जोड़ ली है। इस ट्यूटोरियल ने आपको प्रोग्रामेटिक रूप से अपनी छवियों को बेहतर बनाने के लिए ज्ञान से लैस किया है।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: क्या मैं अन्य .NET फ्रेमवर्क के साथ .NET के लिए Aspose.PSD का उपयोग कर सकता हूं?

A1: हां, .NET के लिए Aspose.PSD विभिन्न .NET फ्रेमवर्क के साथ संगत है।

### प्रश्न 2: क्या .NET के लिए Aspose.PSD का निःशुल्क परीक्षण उपलब्ध है?

 A2: हां, आप निःशुल्क परीक्षण का लाभ उठा सकते हैं[यहाँ](https://releases.aspose.com/).

### प्रश्न 3: मैं .NET के लिए Aspose.PSD का समर्थन कैसे प्राप्त कर सकता हूं?

 A3: पर जाएँ[Aspose.PSD फ़ोरम](https://forum.aspose.com/c/psd/34) सामुदायिक समर्थन के लिए.

### प्रश्न 4: मैं .NET के लिए Aspose.PSD हेतु व्यापक दस्तावेज़ कहां पा सकता हूं?

 A4: देखें[प्रलेखन](https://reference.aspose.com/psd/net/) विस्तृत जानकारी के लिए.

### प्रश्न 5: मैं .NET के लिए Aspose.PSD का लाइसेंस कैसे खरीदूं?

 A5: आप लाइसेंस खरीद सकते हैं[यहाँ](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
