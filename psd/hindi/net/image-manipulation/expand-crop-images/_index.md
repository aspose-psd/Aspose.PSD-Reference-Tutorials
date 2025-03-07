---
title: .NET के लिए Aspose.PSD में छवियों का विस्तार और क्रॉपिंग
linktitle: छवियों का विस्तार और क्रॉप करना
second_title: Aspose.PSD .NET एपीआई
description: .NET के लिए Aspose.PSD का उपयोग करके गतिशील रूप से छवियों को विस्तारित और क्रॉप करना सीखें। सहज छवि हेरफेर के लिए हमारे चरण-दर-चरण मार्गदर्शिका का पालन करें।
weight: 13
url: /hi/net/image-manipulation/expand-crop-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET के लिए Aspose.PSD में छवियों का विस्तार और क्रॉपिंग

## परिचय

Aspose.PSD for .NET एक व्यापक इमेजिंग लाइब्रेरी है जो डेवलपर्स को उनके .NET अनुप्रयोगों में विभिन्न छवि प्रारूपों के साथ काम करने की अनुमति देती है। इसकी एक खास विशेषता यह है कि यह आसानी से छवियों में हेरफेर करने में सक्षम है। इस ट्यूटोरियल में, हम छवियों को विस्तारित करने और क्रॉप करने पर ध्यान केंद्रित करेंगे, जिससे आपको Aspose.PSD का उपयोग करके इन कार्यों को पूरा करने के लिए एक व्यावहारिक मार्गदर्शिका मिलेगी।

## आवश्यक शर्तें

ट्यूटोरियल में शामिल होने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

-  Aspose.PSD for .NET लाइब्रेरी: सुनिश्चित करें कि आपके पास Aspose.PSD for .NET लाइब्रेरी स्थापित है। आप इसे यहाँ से डाउनलोड कर सकते हैं[.NET के लिए Aspose.PSD दस्तावेज़](https://reference.aspose.com/psd/net/).

- नमूना छवि: एक नमूना छवि फ़ाइल तैयार करें (उदाहरण के लिए, "example1.psd") जिसका उपयोग आप ट्यूटोरियल के लिए करेंगे।

अब, आइए चरण-दर-चरण मार्गदर्शिका से शुरुआत करें।

## नामस्थान आयात करें

.NET के लिए Aspose.PSD द्वारा प्रदान की गई कार्यक्षमताओं का लाभ उठाने के लिए आवश्यक नामस्थानों को आयात करके शुरू करें। अपने कोड में निम्नलिखित नामस्थान जोड़ें:

```csharp
using Aspose.PSD.ImageOptions;
```

## चरण 1: प्रोजेक्ट सेट अप करें

 सुनिश्चित करें कि आपके पास Aspose.PSD for .NET एकीकृत के साथ एक प्रोजेक्ट सेटअप है। यदि नहीं, तो अनुसरण करें[प्रलेखन](https://reference.aspose.com/psd/net/) दिशा - निर्देश के लिए।

## चरण 2: छवि लोड करें

निम्नलिखित कोड का उपयोग करके नमूना छवि लोड करें:

```csharp
string dataDir = RunExamples.GetDataDir_DrawingAndFormattingImages();
string sourceFile = dataDir + @"example1.psd";

// छवि लोड करें
using (RasterImage rasterImage = (RasterImage)Image.Load(sourceFile))
{
    // छवि प्रसंस्करण के लिए अतिरिक्त कोड यहां दिया जाएगा
}
```

## चरण 3: छवि डेटा कैश करें

प्रदर्शन को अनुकूलित करने के लिए छवि डेटा कैश करें:

```csharp
rasterImage.CacheData();
```

## चरण 4: गंतव्य आयत परिभाषित करें

Rectangle क्लास का एक उदाहरण बनाएँ और आयत का X, Y, चौड़ाई और ऊँचाई निर्धारित करें। यह वह क्षेत्र होगा जहाँ तक छवि का विस्तार या क्रॉप किया जाएगा।

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

बधाई हो! आपने सफलतापूर्वक सीख लिया है कि .NET के लिए Aspose.PSD का उपयोग करके छवियों को कैसे विस्तारित और क्रॉप किया जाए। यह शक्तिशाली लाइब्रेरी आपके .NET अनुप्रयोगों के भीतर छवि हेरफेर के लिए संभावनाओं की एक दुनिया खोलती है।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: क्या Aspose.PSD PSD के अलावा अन्य छवि प्रारूपों को भी संभाल सकता है?

A1: हां, Aspose.PSD JPEG, PNG, GIF, और अधिक सहित छवि प्रारूपों की एक विस्तृत श्रृंखला का समर्थन करता है।

### प्रश्न 2: मैं Aspose.PSD के लिए समर्थन कहां पा सकता हूं?

 A2: आप यहां पर समर्थन पा सकते हैं और समुदाय के साथ जुड़ सकते हैं[Aspose.PSD फ़ोरम](https://forum.aspose.com/c/psd/34).

### प्रश्न 3 क्या .NET के लिए Aspose.PSD का निःशुल्क परीक्षण उपलब्ध है?

 A3: हाँ, आप यहाँ उपलब्ध निःशुल्क परीक्षण के साथ सुविधाओं का पता लगा सकते हैं[Aspose.PSD निःशुल्क परीक्षण](https://releases.aspose.com/).

### प्रश्न 4: मैं Aspose.PSD के लिए अस्थायी लाइसेंस कैसे प्राप्त करूं?

 A4: आप यहाँ से अस्थायी लाइसेंस प्राप्त कर सकते हैं[Aspose.PSD अस्थायी लाइसेंस](https://purchase.aspose.com/temporary-license/).

### प्रश्न 5: मैं .NET के लिए Aspose.PSD कहां से खरीद सकता हूं?

 A5: आप लाइब्रेरी को यहां से खरीद सकते हैं[Aspose.PSD खरीद पृष्ठ](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
