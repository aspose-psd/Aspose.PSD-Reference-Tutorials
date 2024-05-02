---
title: .NET के लिए Aspose.PSD में रंग संतुलन समायोजन लागू करना
linktitle: रंग संतुलन समायोजन लागू करना
second_title: Aspose.PSD .NET एपीआई
description: .NET के रंग संतुलन समायोजन सुविधा के लिए Aspose.PSD के साथ PSD छवि रंगों को आसानी से बढ़ाएं। आश्चर्यजनक परिणामों के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
type: docs
weight: 14
url: /hi/net/image-adjustment/color-balance-adjustment/
---
## परिचय

.NET के लिए Aspose.PSD में रंग संतुलन समायोजन लागू करने पर इस व्यापक मार्गदर्शिका में आपका स्वागत है! Aspose.PSD एक शक्तिशाली .NET लाइब्रेरी है जो डेवलपर्स को PSD फ़ाइलों के साथ कुशलतापूर्वक काम करने की अनुमति देती है। इस ट्यूटोरियल में, हम रंग संतुलन समायोजन सुविधा पर ध्यान केंद्रित करेंगे, जिससे आप अपनी PSD छवियों के रंग संतुलन को आसानी से बढ़ा सकेंगे।

## आवश्यक शर्तें

इससे पहले कि हम ट्यूटोरियल में उतरें, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

-  .NET लाइब्रेरी के लिए Aspose.PSD: लाइब्रेरी को डाउनलोड और इंस्टॉल करें[Aspose.PSD वेबसाइट](https://releases.aspose.com/psd/net/).
- विकास परिवेश: सुनिश्चित करें कि आपकी मशीन पर एक कार्यशील .NET विकास परिवेश स्थापित है।
- PSD फ़ाइल: एक PSD फ़ाइल तैयार रखें जिसमें आप रंग संतुलन समायोजन लागू करना चाहते हैं।

## नामस्थान आयात करें

अपने .NET प्रोजेक्ट में, Aspose.PSD सुविधाओं का उपयोग करने के लिए आवश्यक नामस्थान शामिल करें। अपने कोड में निम्नलिखित पंक्तियाँ जोड़ें:

```csharp
using Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers;
```

अब, आइए रंग संतुलन समायोजन प्रक्रिया को कई चरणों में विभाजित करें:

## चरण 1: PSD फ़ाइल लोड करें

```csharp
string dataDir = "Your Document Directory";
var filePath = dataDir + "ColorBalance.psd";
var outputPath = dataDir + "ColorBalance_out.psd";

using (var im = (FileFormats.Psd.PsdImage)Image.Load(filePath))
{
    // रंग संतुलन समायोजन के लिए कोड निम्नलिखित चरणों में जोड़ा जाएगा।
}
```

## चरण 2: रंग संतुलन तक पहुंचें और समायोजित करें

```csharp
foreach (var layer in im.Layers)
{
    var cbLayer = layer as ColorBalanceAdjustmentLayer;
    if (cbLayer != null)
    {
        cbLayer.ShadowsCyanRedBalance = 30;
        cbLayer.ShadowsMagentaGreenBalance = -15;
        cbLayer.ShadowsYellowBlueBalance = 40;
        cbLayer.MidtonesCyanRedBalance = -90;
        cbLayer.MidtonesMagentaGreenBalance = -25;
        cbLayer.MidtonesYellowBlueBalance = 20;
        cbLayer.HighlightsCyanRedBalance = -30;
        cbLayer.HighlightsMagentaGreenBalance = 67;
        cbLayer.HighlightsYellowBlueBalance = -95;
        cbLayer.PreserveLuminosity = true;
    }
}
```

## चरण 3: समायोजित छवि सहेजें

```csharp
im.Save(outputPath);
```

अब, आपने .NET के लिए Aspose.PSD का उपयोग करके अपनी PSD फ़ाइल में रंग संतुलन समायोजन सफलतापूर्वक लागू कर दिया है!

## निष्कर्ष

बधाई हो! आपने सीखा है कि .NET के लिए Aspose.PSD के साथ अपनी PSD छवियों का रंग संतुलन कैसे बढ़ाया जाए। वांछित दृश्य प्रभाव प्राप्त करने के लिए विभिन्न संतुलन मूल्यों के साथ प्रयोग करें।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं कई परतों पर रंग संतुलन समायोजन लागू कर सकता हूँ?

A1: हाँ, आप अपनी PSD फ़ाइल में सभी परतों के माध्यम से पुनरावृति कर सकते हैं और आवश्यकतानुसार रंग संतुलन समायोजित कर सकते हैं।

### Q2: क्या .NET के लिए Aspose.PSD PSD फ़ाइलों के बैच प्रोसेसिंग के लिए उपयुक्त है?

ए2: बिल्कुल! Aspose.PSD PSD फ़ाइलों के लिए कुशल बैच प्रोसेसिंग क्षमताएं प्रदान करता है।

### Q3: मैं .NET के लिए Aspose.PSD के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?

 ए3: विजिट करें[Aspose.PSD अस्थायी लाइसेंस](https://purchase.aspose.com/temporary-license/) अस्थायी लाइसेंस के लिए.

### Q4: मुझे और अधिक उदाहरण और दस्तावेज़ कहां मिल सकते हैं?

 ए4: अन्वेषण करें[Aspose.PSD दस्तावेज़ीकरण](https://reference.aspose.com/psd/net/) विस्तृत उदाहरणों और मार्गदर्शिकाओं के लिए।

### Q5: .NET के लिए Aspose.PSD के लिए कौन से समर्थन विकल्प उपलब्ध हैं?

 A5: पर जाएँ[Aspose.PSD फोरम](https://forum.aspose.com/c/psd/34) सामुदायिक समर्थन और चर्चा के लिए।
