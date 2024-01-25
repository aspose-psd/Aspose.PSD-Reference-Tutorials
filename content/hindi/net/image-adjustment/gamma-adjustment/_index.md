---
title: .NET के लिए Aspose.PSD में गामा समायोजन लागू करना
linktitle: गामा समायोजन लागू करना
second_title: Aspose.PSD .NET एपीआई
description: गामा समायोजन को लागू करने पर हमारी चरण-दर-चरण मार्गदर्शिका के साथ .NET के लिए Aspose.PSD की शक्ति का अन्वेषण करें। छवि की चमक और कंट्रास्ट को सहजता से ठीक करें।
type: docs
weight: 12
url: /hi/net/image-adjustment/gamma-adjustment/
---
## परिचय

.NET के लिए Aspose.PSD में गामा समायोजन लागू करने पर इस व्यापक मार्गदर्शिका में आपका स्वागत है! गामा समायोजन एक महत्वपूर्ण छवि प्रसंस्करण तकनीक है जो आपको किसी छवि की चमक और कंट्रास्ट को ठीक करने की अनुमति देती है। इस ट्यूटोरियल में, हम आपको .NET के लिए शक्तिशाली Aspose.PSD लाइब्रेरी का उपयोग करके प्रक्रिया के बारे में बताएंगे।

## आवश्यक शर्तें

कार्यान्वयन में उतरने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ हैं:

-  .NET लाइब्रेरी के लिए Aspose.PSD: सुनिश्चित करें कि आपके पास .NET के लिए Aspose.PSD लाइब्रेरी स्थापित है। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/psd/net/).

- .NET फ्रेमवर्क: यह ट्यूटोरियल मानता है कि आपको .NET विकास की बुनियादी समझ है और आपने .NET फ्रेमवर्क स्थापित कर लिया है।

- एकीकृत विकास पर्यावरण (आईडीई): .NET विकास के लिए अपना पसंदीदा आईडीई चुनें, जैसे कि विजुअल स्टूडियो।

## नामस्थान आयात करें

अपने .NET प्रोजेक्ट में, Aspose.PSD के साथ काम करने के लिए आवश्यक नेमस्पेस आयात करके शुरुआत करें:

```csharp
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

## चरण 1: अपना प्रोजेक्ट सेट करें

अपने चुने हुए IDE में एक नया .NET प्रोजेक्ट बनाएं। Aspose.PSD लाइब्रेरी में संदर्भ जोड़ना सुनिश्चित करें।

## चरण 2: दस्तावेज़ निर्देशिका को परिभाषित करें

```csharp
string dataDir = "Your Document Directory";
```

## चरण 3: छवि लोड करें

```csharp
string sourceFile = dataDir + @"sample.psd";
using (var image = Image.Load(sourceFile))
{
    // इसके अंदर ब्लॉक का उपयोग करके अतिरिक्त कदम उठाए जाएंगे।
}
```

## चरण 4: RasterImage और Cache डेटा पर कास्ट करें

```csharp
RasterImage rasterImage = (RasterImage)image;
if (!rasterImage.IsCached)
{
    rasterImage.CacheData();
}
```

## चरण 5: गामा समायोजित करें

```csharp
rasterImage.AdjustGamma(2.2f, 2.2f, 2.2f);
```

## चरण 6: टिफ़ऑप्शंस बनाएं और सहेजें

```csharp
string destName = dataDir + @"AdjustGamma_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.BitsPerSample = new ushort[] { 8, 8, 8 };
tiffOptions.Photometric = TiffPhotometrics.Rgb;
rasterImage.Save(destName, tiffOptions);
```

## निष्कर्ष

बधाई हो! आपने .NET के लिए Aspose.PSD का उपयोग करके गामा समायोजन को सफलतापूर्वक कार्यान्वित किया है। यह शक्तिशाली लाइब्रेरी इमेज प्रोसेसिंग के लिए मजबूत क्षमताएं प्रदान करती है, जो इसे .NET डेवलपर्स के लिए एक मूल्यवान टूल बनाती है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: मुझे Aspose.PSD दस्तावेज़ कहां मिल सकता है?

 A1: आप दस्तावेज़ का संदर्भ ले सकते हैं[यहाँ](https://reference.aspose.com/psd/net/).

### Q2: मैं .NET के लिए Aspose.PSD कैसे डाउनलोड करूं?

 A2: आप लाइब्रेरी डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/psd/net/).

### Q3: क्या कोई निःशुल्क परीक्षण उपलब्ध है?

 उ3: हाँ, आप निःशुल्क परीक्षण प्राप्त कर सकते हैं[यहाँ](https://releases.aspose.com/).

### Q4: मुझे Aspose.PSD के लिए समर्थन कहाँ से मिल सकता है?

 उ4: आप सहायता मंच पर जा सकते हैं[यहाँ](https://forum.aspose.com/c/psd/34).

### Q5: क्या मुझे अस्थायी लाइसेंस की आवश्यकता है?

 A5: यदि आवश्यक हो, तो आप अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).