---
title: .NET के लिए Aspose.PSD में परतों में स्ट्रोक प्रभाव जोड़ना
linktitle: परतों में स्ट्रोक प्रभाव जोड़ना
second_title: Aspose.PSD .NET एपीआई
description: .NET के लिए Aspose.PSD के साथ छवि सौंदर्य को बढ़ाएं। स्ट्रोक प्रभाव को चरण-दर-चरण जोड़ना सीखें। अभी डाउनलोड करें, खरीदें या निःशुल्क परीक्षण आज़माएँ।
type: docs
weight: 10
url: /hi/net/layer-effects/adding-stroke-effects/
---
## परिचय

.NET के लिए Aspose.PSD में परतों में स्ट्रोक प्रभाव जोड़ने पर इस चरण-दर-चरण ट्यूटोरियल में आपका स्वागत है। स्ट्रोक प्रभाव के साथ अपनी छवियों की दृश्य अपील को बढ़ाना बहुत आसान है, और Aspose.PSD इसे .NET डेवलपर्स के लिए सहज बनाता है। इस गाइड में, हम आपको इस प्रक्रिया के माध्यम से चलेंगे, इस शक्तिशाली सुविधा में महारत हासिल करने में आपकी मदद करने के लिए स्पष्ट कदम और उदाहरण प्रदान करेंगे।

## आवश्यक शर्तें

इससे पहले कि हम ट्यूटोरियल में आगे बढ़ें, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

- .NET के लिए Aspose.PSD: Aspose.PSD लाइब्रेरी को डाउनलोड करें और इंस्टॉल करें[वेबसाइट](https://releases.aspose.com/psd/net/).

- दस्तावेज़ निर्देशिका: उस PSD दस्तावेज़ की निर्देशिका तैयार करें जिसमें आप स्ट्रोक प्रभाव लागू करना चाहते हैं।

- आउटपुट निर्देशिका: स्ट्रोक प्रभाव वाले आउटपुट छवियों को संग्रहीत करने के लिए एक अलग निर्देशिका रखें।

- विज़ुअल स्टूडियो: सुनिश्चित करें कि आपके पास विज़ुअल स्टूडियो या कोई अन्य पसंदीदा .NET विकास वातावरण स्थापित है।

## नामस्थान आयात करें

अपने .NET प्रोजेक्ट में, Aspose.PSD कार्यक्षमता का लाभ उठाने के लिए आवश्यक नामस्थान शामिल करें:

```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using Aspose.PSD.ImageOptions;
```

## चरण 1: PSD दस्तावेज़ लोड करें

```csharp
string srcFile = Path.Combine(SourceDir, "AddStrokeEffect.psd");
string outputFilePng = Path.Combine(OutputDir, "AddStrokeEffect.png");

using (var psdImage = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    // PSD दस्तावेज़ लोड करने के लिए आपका कोड यहाँ है
}
```

## चरण 2: रंग स्ट्रोक प्रभाव जोड़ें

```csharp
// अंदर की स्थिति में रंग भरण जोड़ता है
strokeEffect = psdImage.Layers[1].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Inside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## चरण 3: बाहरी स्थिति

```csharp
// बाहरी स्थान पर रंग भरण जोड़ता है
strokeEffect = psdImage.Layers[2].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Outside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## चरण 4: केंद्र की स्थिति

```csharp
// केंद्र स्थिति पर रंग भरण जोड़ता है
strokeEffect = psdImage.Layers[3].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Center;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

ग्रेडिएंट और पैटर्न भरण के लिए समान चरणों को दोहराएं, तदनुसार सेटिंग्स समायोजित करें।

## निष्कर्ष

बधाई हो! आपने सफलतापूर्वक सीख लिया है कि .NET के लिए Aspose.PSD का उपयोग करके परतों में स्ट्रोक प्रभाव कैसे जोड़ें। अपनी छवियों में वांछित दृश्य प्रभाव प्राप्त करने के लिए विभिन्न सेटिंग्स के साथ प्रयोग करें।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: क्या मैं स्ट्रोक प्रभाव केवल विशिष्ट परतों पर ही लागू कर सकता हूँ?

A1: हां, आप कोड में लेयर इंडेक्स को समायोजित करके विशिष्ट लेयर्स को लक्षित कर सकते हैं।

### प्रश्न 2: क्या Aspose.PSD नवीनतम .NET फ्रेमवर्क के साथ संगत है?

A2: बिल्कुल! Aspose.PSD को नवीनतम .NET फ्रेमवर्क के साथ सहजता से एकीकृत करने के लिए डिज़ाइन किया गया है।

### प्रश्न 3: मैं स्ट्रोक रंग को कैसे अनुकूलित कर सकता हूं?

 A3: बस संशोधित करें`Color` वांछित स्ट्रोक रंग प्राप्त करने के लिए कोड में गुण का उपयोग करें।

### प्रश्न 4: क्या Aspose.PSD एकाधिक PSD फ़ाइलों के लिए बैच प्रोसेसिंग का समर्थन करता है?

A4: हां, आप एकाधिक PSD फ़ाइलों के माध्यम से लूप कर सकते हैं और समान दृष्टिकोण का उपयोग करके स्ट्रोक प्रभाव लागू कर सकते हैं।

### प्रश्न 5: क्या मैं Aspose.PSD खरीदने से पहले परीक्षण संस्करण का उपयोग कर सकता हूँ?

 A5: ज़रूर![मुफ्त परीक्षण](https://releases.aspose.com/) खरीदारी करने से पहले Aspose.PSD की क्षमताओं का पता लगाने के लिए।