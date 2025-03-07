---
title: .NET के लिए Aspose.PSD में गामा समायोजन लागू करना
linktitle: गामा समायोजन का कार्यान्वयन
second_title: Aspose.PSD .NET एपीआई
description: गामा समायोजन को लागू करने के बारे में हमारे चरण-दर-चरण गाइड के साथ .NET के लिए Aspose.PSD की शक्ति का अन्वेषण करें। आसानी से छवि की चमक और कंट्रास्ट को बेहतर बनाएँ।
weight: 12
url: /hi/net/image-adjustment/gamma-adjustment/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET के लिए Aspose.PSD में गामा समायोजन लागू करना

## परिचय

.NET के लिए Aspose.PSD में गामा समायोजन को लागू करने के बारे में इस व्यापक गाइड में आपका स्वागत है! गामा समायोजन एक महत्वपूर्ण छवि प्रसंस्करण तकनीक है जो आपको किसी छवि की चमक और कंट्रास्ट को ठीक करने की अनुमति देती है। इस ट्यूटोरियल में, हम आपको .NET के लिए शक्तिशाली Aspose.PSD लाइब्रेरी का उपयोग करके प्रक्रिया के माध्यम से चलेंगे।

## आवश्यक शर्तें

कार्यान्वयन में उतरने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

-  .NET के लिए Aspose.PSD लाइब्रेरी: सुनिश्चित करें कि आपके पास .NET के लिए Aspose.PSD लाइब्रेरी स्थापित है। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/psd/net/).

- .NET फ्रेमवर्क: यह ट्यूटोरियल मानता है कि आपको .NET डेवलपमेंट की बुनियादी समझ है और आपके पास .NET फ्रेमवर्क स्थापित है।

- एकीकृत विकास वातावरण (IDE): .NET विकास के लिए अपना पसंदीदा IDE चुनें, जैसे कि Visual Studio.

## नामस्थान आयात करें

अपने .NET प्रोजेक्ट में, Aspose.PSD के साथ काम करने के लिए आवश्यक नेमस्पेस आयात करके शुरुआत करें:

```csharp
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

## चरण 1: अपना प्रोजेक्ट सेट करें

अपने चुने हुए IDE में एक नया .NET प्रोजेक्ट बनाएँ। Aspose.PSD लाइब्रेरी में संदर्भ जोड़ना सुनिश्चित करें।

## चरण 2: दस्तावेज़ निर्देशिका निर्धारित करें

```csharp
string dataDir = "Your Document Directory";
```

## चरण 3: छवि लोड करें

```csharp
string sourceFile = dataDir + @"sample.psd";
using (var image = Image.Load(sourceFile))
{
    // इस using ब्लॉक के अंदर अतिरिक्त चरण निष्पादित किए जाएंगे।
}
```

## चरण 4: RasterImage और कैश डेटा पर कास्ट करें

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

## चरण 6: TiffOptions बनाएं और सहेजें

```csharp
string destName = dataDir + @"AdjustGamma_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.BitsPerSample = new ushort[] { 8, 8, 8 };
tiffOptions.Photometric = TiffPhotometrics.Rgb;
rasterImage.Save(destName, tiffOptions);
```

## निष्कर्ष

बधाई हो! आपने .NET के लिए Aspose.PSD का उपयोग करके गामा समायोजन को सफलतापूर्वक लागू किया है। यह शक्तिशाली लाइब्रेरी इमेज प्रोसेसिंग के लिए मजबूत क्षमताएं प्रदान करती है, जो इसे .NET डेवलपर्स के लिए एक मूल्यवान उपकरण बनाती है।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: मैं Aspose.PSD दस्तावेज़ कहां पा सकता हूं?

 A1: आप दस्तावेज़ देख सकते हैं[यहाँ](https://reference.aspose.com/psd/net/).

### प्रश्न 2: मैं .NET के लिए Aspose.PSD कैसे डाउनलोड करूं?

 A2: आप लाइब्रेरी डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/psd/net/).

### प्रश्न 3: क्या कोई निःशुल्क परीक्षण उपलब्ध है?

 A3: हाँ, आप निःशुल्क परीक्षण प्राप्त कर सकते हैं[यहाँ](https://releases.aspose.com/).

### प्रश्न 4: मुझे Aspose.PSD के लिए समर्थन कहां मिल सकता है?

 A4: आप सहायता फ़ोरम पर जा सकते हैं[यहाँ](https://forum.aspose.com/c/psd/34).

### प्रश्न 5: क्या मुझे अस्थायी लाइसेंस की आवश्यकता है?

 A5: यदि आवश्यक हो, तो आप एक अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
