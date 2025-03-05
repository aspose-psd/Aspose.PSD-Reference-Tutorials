---
title: .NET के लिए Aspose.PSD में रंग संतुलन समायोजन लागू करना
linktitle: रंग संतुलन समायोजन लागू करना
second_title: Aspose.PSD .NET एपीआई
description: Aspose.PSD for .NET के कलर बैलेंस एडजस्टमेंट फीचर के साथ PSD इमेज के रंगों को आसानी से निखारें। शानदार नतीजों के लिए हमारी चरण-दर-चरण गाइड का पालन करें।
type: docs
weight: 14
url: /hi/net/image-adjustment/color-balance-adjustment/
---
## परिचय

.NET के लिए Aspose.PSD में रंग संतुलन समायोजन लागू करने पर इस व्यापक गाइड में आपका स्वागत है! Aspose.PSD एक शक्तिशाली .NET लाइब्रेरी है जो डेवलपर्स को PSD फ़ाइलों के साथ कुशलतापूर्वक काम करने की अनुमति देती है। इस ट्यूटोरियल में, हम रंग संतुलन समायोजन सुविधा पर ध्यान केंद्रित करेंगे, जिससे आप आसानी से अपनी PSD छवियों के रंग संतुलन को बढ़ा सकते हैं।

## आवश्यक शर्तें

इससे पहले कि हम ट्यूटोरियल में आगे बढ़ें, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

-  Aspose.PSD for .NET लाइब्रेरी: लाइब्रेरी को डाउनलोड करें और इंस्टॉल करें[Aspose.PSD वेबसाइट](https://releases.aspose.com/psd/net/).
- विकास वातावरण: सुनिश्चित करें कि आपके मशीन पर एक कार्यशील .NET विकास वातावरण स्थापित है।
- PSD फ़ाइल: एक PSD फ़ाइल तैयार रखें जिस पर आप रंग संतुलन समायोजन लागू करना चाहते हैं।

## नामस्थान आयात करें

अपने .NET प्रोजेक्ट में, Aspose.PSD सुविधाओं का उपयोग करने के लिए आवश्यक नामस्थान शामिल करें। अपने कोड में निम्न पंक्तियाँ जोड़ें:

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

## चरण 3: समायोजित छवि को सहेजें

```csharp
im.Save(outputPath);
```

अब, आपने .NET के लिए Aspose.PSD का उपयोग करके अपनी PSD फ़ाइल पर रंग संतुलन समायोजन सफलतापूर्वक लागू कर दिया है!

## निष्कर्ष

बधाई हो! आपने Aspose.PSD for .NET के साथ अपने PSD इमेज के रंग संतुलन को बढ़ाने का तरीका सीख लिया है। वांछित दृश्य प्रभाव प्राप्त करने के लिए विभिन्न संतुलन मानों के साथ प्रयोग करें।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: क्या मैं एकाधिक परतों पर रंग संतुलन समायोजन लागू कर सकता हूँ?

A1: हां, आप अपनी PSD फ़ाइल में सभी परतों के माध्यम से पुनरावृति कर सकते हैं और आवश्यकतानुसार रंग संतुलन समायोजित कर सकते हैं।

### प्रश्न 2: क्या .NET के लिए Aspose.PSD PSD फ़ाइलों के बैच प्रसंस्करण के लिए उपयुक्त है?

A2: बिल्कुल! Aspose.PSD PSD फ़ाइलों के लिए कुशल बैच प्रसंस्करण क्षमता प्रदान करता है।

### प्रश्न 3: मैं .NET के लिए Aspose.PSD का अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?

 A3: विजिट करें[Aspose.PSD अस्थायी लाइसेंस](https://purchase.aspose.com/temporary-license/) अस्थायी लाइसेंस के लिए आवेदन करें।

### प्रश्न 4: मुझे और अधिक उदाहरण एवं दस्तावेज कहां मिल सकते हैं?

 A4: अन्वेषण करें[Aspose.PSD दस्तावेज़ीकरण](https://reference.aspose.com/psd/net/) विस्तृत उदाहरण और मार्गदर्शन के लिए.

### प्रश्न 5: .NET के लिए Aspose.PSD के लिए कौन से समर्थन विकल्प उपलब्ध हैं?

 A5: पर जाएँ[Aspose.PSD फ़ोरम](https://forum.aspose.com/c/psd/34) सामुदायिक समर्थन और चर्चा के लिए।
