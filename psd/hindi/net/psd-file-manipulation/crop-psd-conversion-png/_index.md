---
title: .NET के लिए Aspose.PSD में PNG में कनवर्ट करते समय PSD फ़ाइलों को क्रॉप करना
linktitle: PNG में कनवर्ट करते समय PSD फ़ाइलों को क्रॉप करना
second_title: Aspose.PSD .NET एपीआई
description: .NET के लिए Aspose.PSD का उपयोग करके PSD फ़ाइलों को आसानी से क्रॉप करना सीखें। PNG में सहज रूपांतरण के लिए हमारे चरण-दर-चरण मार्गदर्शिका का पालन करें।
weight: 18
url: /hi/net/psd-file-manipulation/crop-psd-conversion-png/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET के लिए Aspose.PSD में PNG में कनवर्ट करते समय PSD फ़ाइलों को क्रॉप करना

## परिचय
.NET विकास के क्षेत्र में, छवियों में हेरफेर करना और उन्हें परिवर्तित करना एक सामान्य कार्य है। .NET के लिए Aspose.PSD इस प्रक्रिया को सरल बनाने के लिए उपकरणों का एक शक्तिशाली सेट प्रदान करता है। एक लगातार आवश्यकता PSD फ़ाइलों को PNG में बदलने से पहले उन्हें क्रॉप करना है। इस चरण-दर-चरण ट्यूटोरियल में, हम .NET के लिए Aspose.PSD का उपयोग करके प्रक्रिया में गहराई से जाएँगे।
## आवश्यक शर्तें
इससे पहले कि हम इस यात्रा पर निकलें, सुनिश्चित करें कि आपके पास निम्नलिखित चीजें हैं:
-  Aspose.PSD for .NET लाइब्रेरी: लाइब्रेरी को डाउनलोड करें और इंस्टॉल करें[.NET के लिए Aspose.PSD दस्तावेज़ीकरण](https://reference.aspose.com/psd/net/).
- नमूना PSD फ़ाइल: प्रयोग के लिए एक PSD फ़ाइल तैयार रखें। यदि आपके पास एक नहीं है, तो आप ट्यूटोरियल में दिए गए नमूने का उपयोग कर सकते हैं।
- .NET वातावरण: सुनिश्चित करें कि आपके पास एक कार्यशील .NET विकास वातावरण स्थापित है।
- दस्तावेज़ निर्देशिका: कोड में अपनी दस्तावेज़ निर्देशिका का पथ निर्दिष्ट करें।
## नामस्थान आयात करें
अपने .NET प्रोजेक्ट में, .NET के लिए Aspose.PSD हेतु आवश्यक नामस्थान शामिल करें:
```csharp
using Aspose.PSD.ImageOptions;
```
## चरण 1: PSD छवि लोड करें
```csharp
// दस्तावेज़ निर्देशिका का पथ.
string dataDir = "Your Document Directory";
string srcPath = dataDir + @"sample.psd";
// मौजूदा PSD छवि लोड करें
using (RasterImage image = (RasterImage)Image.Load(srcPath))
{
    // आगे के चरणों के लिए आपका कोड यहां जाएगा
}
```
## चरण 2: क्रॉपिंग आयत को परिभाषित करें
```csharp
// x, y, चौड़ाई और ऊँचाई पास करके Rectangle वर्ग का एक उदाहरण बनाएँ
Rectangle cropRectangle = new Rectangle(0, 0, 350, 450);
```
## चरण 3: छवि को क्रॉप करें
```csharp
// इमेज क्लास की क्रॉप विधि को कॉल करें और आयत क्लास इंस्टेंस को पास करें
image.Crop(cropRectangle);
```
## चरण 4: PNG विकल्प निर्दिष्ट करें
```csharp
// PngOptions वर्ग का एक उदाहरण बनाएँ
PngOptions pngOptions = new PngOptions();
```
## चरण 5: क्रॉप की गई छवि को PNG के रूप में सहेजें
```csharp
// PSD फ़ाइल को PNG में बदलने और आउटपुट को सेव करने के लिए सेव विधि को कॉल करें, आउटपुट पथ और PngOptions प्रदान करें
string destName = dataDir + @"export.png";
image.Save(destName, pngOptions);
```
## निष्कर्ष

बधाई हो! आपने सफलतापूर्वक सीख लिया है कि Aspose.PSD for .NET का उपयोग करके PSD फ़ाइलों को PNG में परिवर्तित करते समय उन्हें कैसे क्रॉप किया जाए। यह क्षमता विभिन्न छवि प्रसंस्करण परिदृश्यों में अमूल्य हो सकती है।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: क्या मैं इस लाइब्रेरी का उपयोग व्यावसायिक परियोजना में कर सकता हूँ?

 A1: हाँ, Aspose.PSD for .NET व्यावसायिक उपयोग के लिए उपलब्ध है। देखें[Aspose.PSD लाइसेंसिंग](https://purchase.aspose.com/buy) जानकारी के लिए।

### प्रश्न 2: क्या कोई निःशुल्क परीक्षण उपलब्ध है?

A2: बिल्कुल! आप इसका निःशुल्क परीक्षण संस्करण देख सकते हैं[यहाँ](https://releases.aspose.com/).

### प्रश्न 3: मैं .NET के लिए Aspose.PSD का समर्थन कहां पा सकता हूं?

 A3: पर जाएँ[Aspose.PSD फ़ोरम](https://forum.aspose.com/c/psd/34) किसी भी सहायता या प्रश्न के लिए.

### प्रश्न 4: मैं अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूँ?

 A4: यदि आपको अस्थायी लाइसेंस की आवश्यकता है, तो आप इसे प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).

### प्रश्न 5: क्या दस्तावेज़ में कोई उदाहरण या ट्यूटोरियल उपलब्ध हैं?

 A5: हां, आप व्यापक दस्तावेज और उदाहरण पा सकते हैं[यहाँ](https://reference.aspose.com/psd/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
