---
title: .NET के लिए Aspose.PSD में छवियों का सरल आकार परिवर्तन
linktitle: छवियों का सरल आकार परिवर्तन
second_title: Aspose.PSD .NET एपीआई
description: .NET के लिए Aspose.PSD के साथ मास्टर इमेज आकार बदलना। कुशल, सहज और शक्तिशाली। अपने .NET प्रोजेक्ट को आसानी से आगे बढ़ाएँ।
weight: 17
url: /hi/net/image-manipulation/simple-resizing/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET के लिए Aspose.PSD में छवियों का सरल आकार परिवर्तन

## परिचय

.NET विकास के गतिशील क्षेत्र में, छवियों में हेरफेर करना एक सामान्य आवश्यकता है। .NET के लिए Aspose.PSD अपनी शक्तिशाली क्षमताओं के साथ बचाव के लिए आता है, जो छवि आकार बदलने के लिए एक सहज अनुभव प्रदान करता है। इस ट्यूटोरियल में, हम .NET के लिए Aspose.PSD का उपयोग करके छवियों का आकार बदलने की सरल लेकिन महत्वपूर्ण प्रक्रिया में तल्लीन होंगे। अपनी छवि प्रसंस्करण कौशल को बढ़ाने के लिए एक यात्रा शुरू करने के लिए तैयार हो जाइए।

## आवश्यक शर्तें

इससे पहले कि हम ट्यूटोरियल में आगे बढ़ें, आइए सुनिश्चित करें कि आपके पास सुचारू अनुभव के लिए सब कुछ सेट है:

## नामस्थान आयात करें

सुनिश्चित करें कि आपने .NET के लिए Aspose.PSD की कार्यक्षमताओं तक पहुँचने के लिए आवश्यक नामस्थानों को आयात किया है:

```csharp
using Aspose.PSD.ImageOptions;
```

अब, आइए छवियों का आकार बदलने की प्रक्रिया को कई चरणों में विभाजित करें:

## चरण 1: अपनी दस्तावेज़ निर्देशिका सेट करें

अपने दस्तावेज़ निर्देशिका का पथ सेट करके आरंभ करें:

```csharp
string dataDir = "Your Document Directory";
```

## चरण 2: छवि लोड करें

RasterImage वर्ग के एक उदाहरण में एक मौजूदा छवि लोड करें:

```csharp
string sourceFile = dataDir + @"sample.psd";
using (Image image = Image.Load(sourceFile))
{
    // आपका कोड यहाँ
}
```

## चरण 3: छवि का आकार बदलें

 किसी छवि का आकार बदलना उतना ही सरल है जितना कि`Resize` छवि ऑब्जेक्ट पर विधि:

```csharp
image.Resize(300, 300);
```

## चरण 4: पुनःआकारित छवि को सहेजें

अपने पसंदीदा प्रारूप और विकल्पों के साथ आकार बदले गए चित्र को सहेजें। इस उदाहरण में, हम इसे JPEG के रूप में सहेज रहे हैं:

```csharp
string destName = dataDir + @"SimpleResizing_out.jpg";
image.Save(destName, new JpegOptions());
```

और बस! आपने .NET के लिए Aspose.PSD का उपयोग करके सफलतापूर्वक एक छवि का आकार बदल दिया है।

## निष्कर्ष

छवि का आकार बदलने में महारत हासिल करना किसी भी .NET डेवलपर के टूलकिट में एक बुनियादी कौशल है। .NET के लिए Aspose.PSD के साथ, यह प्रक्रिया न केवल कुशल बल्कि आनंददायक भी बन जाती है। अब, इस ज्ञान से लैस होकर, आगे बढ़ें और अपने .NET प्रोजेक्ट में अपनी छवि हेरफेर क्षमताओं को बढ़ाएँ।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: क्या मैं .NET के लिए Aspose.PSD का उपयोग करके छवियों का आकार एक विशिष्ट पहलू अनुपात में बदल सकता हूँ?

उत्तर 1: हां, आप छवियों का आकार बदलते समय चौड़ाई या ऊंचाई को समायोजित करके एक विशिष्ट पहलू अनुपात बनाए रख सकते हैं।

### प्रश्न 2: क्या .NET के लिए Aspose.PSD JPEG के अलावा अन्य छवि प्रारूपों का समर्थन करता है?

A2: बिल्कुल! .NET के लिए Aspose.PSD PNG, GIF, BMP, और अधिक सहित विभिन्न छवि प्रारूपों का समर्थन करता है।

### प्रश्न 3: क्या .NET के लिए Aspose.PSD हेतु कोई अस्थायी लाइसेंस उपलब्ध है?

A3: हाँ, आप खरीदारी करने से पहले इसकी क्षमताओं का मूल्यांकन करने के लिए .NET के लिए Aspose.PSD का एक अस्थायी लाइसेंस प्राप्त कर सकते हैं।

### प्रश्न 4: मैं .NET के लिए Aspose.PSD हेतु व्यापक दस्तावेज़ कहां पा सकता हूं?

 A4: विस्तृत दस्तावेज़ देखें[.NET के लिए Aspose.PSD दस्तावेज़ीकरण](https://reference.aspose.com/psd/net/).

### प्रश्न 5: मैं Aspose.PSD for .NET के लिए समर्थन कैसे प्राप्त कर सकता हूं या समुदाय से कैसे जुड़ सकता हूं?

 A5: पर जाएँ[.NET फ़ोरम के लिए Aspose.PSD](https://forum.aspose.com/c/psd/34) सामुदायिक समर्थन और चर्चा के लिए।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
