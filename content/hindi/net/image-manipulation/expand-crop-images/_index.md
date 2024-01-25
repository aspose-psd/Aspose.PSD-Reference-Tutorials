---
title: .NET के लिए Aspose.PSD में छवियों का विस्तार और क्रॉपिंग
linktitle: छवियों का विस्तार और काट-छाँट
second_title: Aspose.PSD .NET एपीआई
description: .NET के लिए Aspose.PSD का उपयोग करके छवियों को गतिशील रूप से विस्तारित और क्रॉप करना सीखें। निर्बाध छवि हेरफेर के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
type: docs
weight: 13
url: /hi/net/image-manipulation/expand-crop-images/
---
## परिचय

.NET के लिए Aspose.PSD एक व्यापक इमेजिंग लाइब्रेरी है जो डेवलपर्स को उनके .NET अनुप्रयोगों में विभिन्न छवि प्रारूपों के साथ काम करने की अनुमति देती है। इसकी असाधारण विशेषताओं में से एक छवियों में आसानी से हेरफेर करने की क्षमता है। इस ट्यूटोरियल में, हम छवियों के विस्तार और क्रॉपिंग पर ध्यान केंद्रित करेंगे, जो आपको Aspose.PSD का उपयोग करके इन कार्यों को प्राप्त करने के लिए एक व्यावहारिक मार्गदर्शिका प्रदान करेंगे।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

-  .NET लाइब्रेरी के लिए Aspose.PSD: सुनिश्चित करें कि आपके पास .NET लाइब्रेरी के लिए Aspose.PSD स्थापित है। आप इसे यहां से डाउनलोड कर सकते हैं[.NET दस्तावेज़ीकरण के लिए Aspose.PSD](https://reference.aspose.com/psd/net/).

- नमूना छवि: एक नमूना छवि फ़ाइल तैयार करें (उदाहरण के लिए, "example1.psd") जिसे आप ट्यूटोरियल के लिए उपयोग करेंगे।

अब, आइए चरण-दर-चरण मार्गदर्शिका के साथ शुरुआत करें।

## नामस्थान आयात करें

.NET के लिए Aspose.PSD द्वारा प्रदान की गई कार्यक्षमताओं का लाभ उठाने के लिए आवश्यक नामस्थान आयात करके शुरुआत करें। अपने कोड में निम्नलिखित नामस्थान जोड़ें:

```csharp
using Aspose.PSD.ImageOptions;
```

## चरण 1: प्रोजेक्ट सेट करें

 सुनिश्चित करें कि आपके पास .NET एकीकृत के लिए Aspose.PSD के साथ एक प्रोजेक्ट सेटअप है। यदि नहीं, तो अनुसरण करें[प्रलेखन](https://reference.aspose.com/psd/net/) दिशा - निर्देश के लिए।

## चरण 2: छवि लोड करें

निम्नलिखित कोड का उपयोग करके नमूना छवि लोड करें:

```csharp
string dataDir = RunExamples.GetDataDir_DrawingAndFormattingImages();
string sourceFile = dataDir + @"example1.psd";

// छवि लोड करें
using (RasterImage rasterImage = (RasterImage)Image.Load(sourceFile))
{
    // छवि प्रसंस्करण के लिए अतिरिक्त कोड यहां जाएगा
}
```

## चरण 3: छवि डेटा कैश करें

प्रदर्शन को अनुकूलित करने के लिए छवि डेटा को कैश करें:

```csharp
rasterImage.CacheData();
```

## चरण 4: गंतव्य आयत को परिभाषित करें

आयत वर्ग का एक उदाहरण बनाएं और आयत के X, Y, चौड़ाई और ऊँचाई को परिभाषित करें। यह वह क्षेत्र होगा जहां छवि का विस्तार या क्रॉप किया जाएगा।

```csharp
Rectangle destRect = new Rectangle { X = -200, Y = -200, Width = 300, Height = 300 };
```

## चरण 5: आउटपुट छवि सहेजें

आउटपुट छवि को निर्दिष्ट विकल्पों और गंतव्य आयत के साथ सहेजें:

```csharp
string destName = dataDir + @"jpeg_out.jpg";
rasterImage.Save(destName, new JpegOptions(), destRect);
```

## निष्कर्ष

बधाई हो! आपने .NET के लिए Aspose.PSD का उपयोग करके छवियों को विस्तारित और क्रॉप करना सफलतापूर्वक सीख लिया है। यह शक्तिशाली लाइब्रेरी आपके .NET अनुप्रयोगों में छवि हेरफेर के लिए संभावनाओं की दुनिया खोलती है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.PSD PSD के अलावा अन्य छवि प्रारूपों को संभाल सकता है?

A1: हां, Aspose.PSD JPEG, PNG, GIF और अन्य सहित छवि प्रारूपों की एक विस्तृत श्रृंखला का समर्थन करता है।

### Q2: मुझे Aspose.PSD के लिए समर्थन कहां मिल सकता है?

 A2: आप यहां समर्थन पा सकते हैं और समुदाय के साथ जुड़ सकते हैं[Aspose.PSD फोरम](https://forum.aspose.com/c/psd/34).

### Q3 क्या .NET के लिए Aspose.PSD का कोई निःशुल्क परीक्षण उपलब्ध है?

 उ3: हां, आप यहां उपलब्ध निःशुल्क परीक्षण के साथ सुविधाओं का पता लगा सकते हैं[Aspose.PSD निःशुल्क परीक्षण](https://releases.aspose.com/).

### Q4: मैं Aspose.PSD के लिए अस्थायी लाइसेंस कैसे प्राप्त करूं?

 A4: आप यहां से अस्थायी लाइसेंस प्राप्त कर सकते हैं[Aspose.PSD अस्थायी लाइसेंस](https://purchase.aspose.com/temporary-license/).

### Q5: मैं .NET के लिए Aspose.PSD कहां से खरीद सकता हूं?

 A5: आप लाइब्रेरी यहां से खरीद सकते हैं[Aspose.PSD खरीद पृष्ठ](https://purchase.aspose.com/buy).