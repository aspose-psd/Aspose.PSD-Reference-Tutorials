---
title: .NET के लिए Aspose.PSD के साथ अण्डाकार आकृतियाँ बनाना
linktitle: .NET के लिए Aspose.PSD के साथ अण्डाकार आकृतियाँ बनाना
second_title: Aspose.PSD .NET एपीआई
description: Aspose.PSD का उपयोग करके .NET में अण्डाकार आकृतियाँ बनाना सीखें। कोड उदाहरणों के साथ चरण-दर-चरण मार्गदर्शिका। आसानी से शानदार ग्राफ़िक्स बनाएँ।
weight: 13
url: /hi/net/psd-drawing-techniques/creating-elliptical-shapes/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET के लिए Aspose.PSD के साथ अण्डाकार आकृतियाँ बनाना

## परिचय

.NET के लिए Aspose.PSD का उपयोग करके अण्डाकार आकृतियाँ बनाने पर हमारी विस्तृत मार्गदर्शिका में आपका स्वागत है। Aspose.PSD एक शक्तिशाली .NET लाइब्रेरी है जो डेवलपर्स को Adobe Photoshop की आवश्यकता के बिना फ़ोटोशॉप फ़ाइलों में हेरफेर करने और उन्हें परिवर्तित करने की अनुमति देती है। इस ट्यूटोरियल में, हम आपको लाइब्रेरी का उपयोग करके अण्डाकार आकृतियाँ बनाने की प्रक्रिया से परिचित कराएँगे।

## आवश्यक शर्तें

इससे पहले कि हम ट्यूटोरियल में आगे बढ़ें, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

- .NET लाइब्रेरी के लिए Aspose.PSD: सुनिश्चित करें कि आपके .NET प्रोजेक्ट में Aspose.PSD लाइब्रेरी स्थापित है। आप इसे यहाँ से डाउनलोड कर सकते हैं।[.NET के लिए Aspose.PSD दस्तावेज़ीकरण](https://reference.aspose.com/psd/net/).

- .NET वातावरण: यह ट्यूटोरियल मानता है कि आपके पास .NET फ्रेमवर्क का कार्यात्मक ज्ञान है।

## नामस्थान आयात करें

आरंभ करने के लिए, अपने प्रोजेक्ट में आवश्यक नामस्थान आयात करें। यह सुनिश्चित करता है कि आपके पास अण्डाकार आकृतियाँ बनाने के लिए आवश्यक कक्षाओं और विधियों तक पहुँच है। यहाँ एक उदाहरण दिया गया है:

```csharp
using Aspose.PSD.Brushes;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageOptions;
```

अब, आइए अण्डाकार आकृतियाँ बनाने की प्रक्रिया को कई चरणों में विभाजित करें:

## चरण 1: दस्तावेज़ निर्देशिका सेट करें

```csharp
// दस्तावेज़ निर्देशिका का पथ.
string dataDir = "Your Document Directory";
```

## चरण 2: BmpOptions का एक इंस्टेंस बनाएँ

```csharp
// BmpOptions का एक उदाहरण बनाएं और इसके विभिन्न गुण सेट करें
string outpath = dataDir + "Ellipse.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.BitsPerPixel = 32;
```

## चरण 3: छवि का एक उदाहरण बनाएँ

```csharp
// छवि का एक उदाहरण बनाएँ
using (Image image = new PsdImage(100, 100))
{
    // ग्राफ़िक्स क्लास और क्लियर ग्राफ़िक्स सरफ़ेस का एक उदाहरण बनाएँ और आरंभ करें
    Graphics graphic = new Graphics(image);
    graphic.Clear(Color.Yellow);
```

## चरण 4: एक बिंदीदार दीर्घवृत्त आकार बनाएं

```csharp
    // पेन ऑब्जेक्ट को लाल रंग और उसके आसपास आयत निर्दिष्ट करके एक बिंदीदार दीर्घवृत्त आकार बनाएं
    graphic.DrawEllipse(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
```

## चरण 5: एक सतत दीर्घवृत्त आकार बनाएं

```csharp
    //नीले रंग के साथ एक ठोस ब्रश और एक आसपास के आयत वाले पेन ऑब्जेक्ट को निर्दिष्ट करके एक सतत दीर्घवृत्त आकार बनाएं
    graphic.DrawEllipse(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    // छवि को bmp फ़ाइल स्वरूप में निर्यात करें.
    image.Save(outpath, saveOptions);
}
```

## निष्कर्ष

बधाई हो! आपने .NET के लिए Aspose.PSD का उपयोग करके सफलतापूर्वक अण्डाकार आकृतियाँ बनाई हैं। इस ट्यूटोरियल में पर्यावरण की स्थापना से लेकर बिंदीदार और निरंतर दीर्घवृत्ताकार आकृतियाँ बनाने तक के आवश्यक चरणों को शामिल किया गया है।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: मैं .NET के लिए Aspose.PSD का दस्तावेज़ कहां पा सकता हूं?

 A1: दस्तावेज़ उपलब्ध है[यहाँ](https://reference.aspose.com/psd/net/).

### प्रश्न 2: मैं .NET के लिए Aspose.PSD कैसे डाउनलोड करूं?

 A2: आप इसे रिलीज़ पेज से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/psd/net/).

### प्रश्न 3: क्या कोई निःशुल्क परीक्षण उपलब्ध है?

 A3: हां, आप निःशुल्क परीक्षण का लाभ उठा सकते हैं[यहाँ](https://releases.aspose.com/).

### प्रश्न 4: मैं .NET के लिए Aspose.PSD का समर्थन कैसे प्राप्त कर सकता हूं?

 A4: सहायता फ़ोरम पर जाएँ[यहाँ](https://forum.aspose.com/c/psd/34).

### प्रश्न 5: क्या मुझे परीक्षण के लिए अस्थायी लाइसेंस की आवश्यकता है?

 A5: हां, आप एक अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
