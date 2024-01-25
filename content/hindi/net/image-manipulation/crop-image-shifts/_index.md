---
title: .NET के लिए Aspose.PSD में शिफ्ट द्वारा छवियाँ क्रॉप करना
linktitle: शिफ्ट द्वारा छवियाँ काटना
second_title: Aspose.PSD .NET एपीआई
description: .NET के लिए Aspose.PSD का उपयोग करके आसानी से छवियों को क्रॉप करना सीखें। सटीक छवि समायोजन के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
type: docs
weight: 12
url: /hi/net/image-manipulation/crop-image-shifts/
---
## परिचय

.NET विकास के क्षेत्र में, Aspose.PSD छवि प्रसंस्करण कार्यों के लिए एक शक्तिशाली टूलकिट के रूप में सामने आता है। इसकी उल्लेखनीय विशेषताओं में से एक छवियों को सटीकता के साथ क्रॉप करने की क्षमता है, जिसका श्रेय 'क्रॉपिंग बाय शिफ्ट्स' कार्यक्षमता को जाता है। इस चरण-दर-चरण मार्गदर्शिका में, हम आपको .NET के लिए Aspose.PSD का उपयोग करके छवियों को सहजता से क्रॉप करने की प्रक्रिया के बारे में बताएंगे।

## आवश्यक शर्तें

ट्यूटोरियल में गहराई से जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

-  .NET लाइब्रेरी के लिए Aspose.PSD: सुनिश्चित करें कि आपके पास लाइब्रेरी स्थापित है। यदि नहीं, तो आप इसे यहां से डाउनलोड कर सकते हैं[रिलीज पेज](https://releases.aspose.com/psd/net/).

- .NET वातावरण: सुनिश्चित करें कि आपकी मशीन पर एक .NET विकास वातावरण स्थापित है।

- नमूना छवि: PSD प्रारूप में एक नमूना छवि तैयार करें जिसके साथ आप काम करना चाहेंगे।

## नामस्थान आयात करें

अपने .NET प्रोजेक्ट में आवश्यक नामस्थान आयात करके प्रारंभ करें। ये नामस्थान Aspose.PSD कक्षाओं और छवि क्रॉपिंग के लिए आवश्यक विधियों तक पहुंच प्रदान करते हैं।

```csharp
using Aspose.PSD.ImageOptions;
```

## चरण 1: अपनी दस्तावेज़ निर्देशिका परिभाषित करें

अपनी दस्तावेज़ निर्देशिका के लिए पथ सेट करें जहां स्रोत और गंतव्य फ़ाइलें स्थित होंगी।

```csharp
string dataDir = "Your Document Directory";
```

## चरण 2: स्रोत छवि लोड करें

वह PSD छवि लोड करें जिसे आप क्रॉप करना चाहते हैं। अपनी स्रोत फ़ाइल के नाम के साथ "sample.psd" को बदलना सुनिश्चित करें।

```csharp
string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"CroppingByShifts_out.jpg";
```

## चरण 3: बेहतर प्रदर्शन के लिए छवि डेटा को कैश करें

बेहतर प्रदर्शन के लिए क्रॉप करने से पहले छवि डेटा को कैश करने की सलाह दी जाती है।

```csharp
using (RasterImage rasterImage = (RasterImage)Image.Load(sourceFile))
{
    if (!rasterImage.IsCached)
    {
        rasterImage.CacheData();
    }
```

## चरण 4: क्रॉपिंग के लिए शिफ्ट मान परिभाषित करें

छवि के बाएँ, दाएँ, ऊपर और नीचे के लिए शिफ्ट मान निर्दिष्ट करें। अपनी फसल संबंधी आवश्यकताओं के आधार पर इन मूल्यों को समायोजित करें।

```csharp
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

## चरण 5: क्रॉपिंग लागू करें और परिणाम सहेजें

 का उपयोग करें`Crop` निर्दिष्ट बदलावों को लागू करने और क्रॉप की गई छवि को गंतव्य फ़ाइल में सहेजने की विधि।

```csharp
rasterImage.Crop(leftShift, rightShift, topShift, bottomShift);
rasterImage.Save(destName, new JpegOptions());
}
```

## निष्कर्ष

बधाई हो! आपने .NET के लिए Aspose.PSD का उपयोग करके छवियों को शिफ्ट के अनुसार क्रॉप करना सफलतापूर्वक सीख लिया है। यह शक्तिशाली कार्यक्षमता आपको विभिन्न छवि प्रसंस्करण कार्यों के लिए आवश्यक सटीकता और नियंत्रण प्रदान करती है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या मैं केवल PSD ही नहीं, बल्कि विभिन्न प्रारूपों की छवियां क्रॉप कर सकता हूं?

A1: हां, Aspose.PSD विभिन्न छवि प्रारूपों का समर्थन करता है, जिससे आप JPEG, PNG और अन्य प्रारूपों में छवियों को क्रॉप कर सकते हैं।

### Q2: क्या .NET के लिए Aspose.PSD खरीदने से पहले कोई परीक्षण संस्करण उपलब्ध है?

 ए2: निश्चित रूप से! आप नि:शुल्क परीक्षण के साथ टूलकिट का अन्वेषण कर सकते हैं[यहाँ](https://releases.aspose.com/).

### Q3: मैं .NET के लिए Aspose.PSD के लिए अस्थायी लाइसेंस कैसे प्राप्त करूं?

 उ3: आप परीक्षण उद्देश्यों के लिए एक अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).

### Q4: मुझे Aspose.PSD से संबंधित अतिरिक्त समर्थन और चर्चाएँ कहाँ मिल सकती हैं?

 A4: पर जाएँ[Aspose.PSD फोरम](https://forum.aspose.com/c/psd/34) समर्थन और आकर्षक चर्चाओं के लिए।

### Q5: क्या मैं सीधे वेबसाइट से .NET के लिए Aspose.PSD खरीद सकता हूँ?

 A5: हाँ, आप लाइब्रेरी को सुरक्षित रूप से खरीद सकते हैं[खरीद पृष्ठ](https://purchase.aspose.com/buy).