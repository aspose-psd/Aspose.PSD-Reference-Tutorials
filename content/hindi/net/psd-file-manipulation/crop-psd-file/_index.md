---
title: .NET के लिए Aspose.PSD के साथ PSD फ़ाइलें क्रॉप करना
linktitle: .NET के लिए Aspose.PSD के साथ PSD फ़ाइलें क्रॉप करना
second_title: Aspose.PSD .NET एपीआई
description: Aspose.PSD, एक बहुमुखी टूलकिट के साथ .NET में PSD फ़ाइल क्रॉपिंग की कला का अन्वेषण करें। अपने छवि हेरफेर खेल को सहजता से उन्नत करें।
type: docs
weight: 19
url: /hi/net/psd-file-manipulation/crop-psd-file/
---
## परिचय
.NET विकास के क्षेत्र में, Aspose.PSD PSD (फ़ोटोशॉप दस्तावेज़) फ़ाइलों को निर्बाध रूप से संभालने के लिए एक शक्तिशाली टूलकिट के रूप में सामने आता है। जब छवियों में हेरफेर करने की बात आती है, तो क्रॉप करना एक मौलिक ऑपरेशन है, और Aspose.PSD .NET डेवलपर्स के लिए इस प्रक्रिया को सरल बनाता है। इस ट्यूटोरियल में, हम आपको चरण-दर-चरण मार्गदर्शिका प्रदान करते हुए, .NET के लिए Aspose.PSD का उपयोग करके PSD फ़ाइलों को क्रॉप करने का तरीका जानेंगे।
## आवश्यक शर्तें
ट्यूटोरियल में गहराई से जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित शर्तें हैं:
-  .NET के लिए Aspose.PSD: सुनिश्चित करें कि आपके पास लाइब्रेरी स्थापित है। आप इसे यहां से डाउनलोड कर सकते हैं[.NET दस्तावेज़ीकरण के लिए Aspose.PSD](https://reference.aspose.com/psd/net/).
- विकास परिवेश: विज़ुअल स्टूडियो या किसी पसंदीदा IDE सहित अपना .NET विकास परिवेश सेट करें।
## नामस्थान आयात करें
अपने प्रोजेक्ट में आवश्यक नामस्थान आयात करके प्रारंभ करें:
```csharp
using Aspose.PSD.FileFormats.Png;
using Aspose.PSD.ImageOptions;
```
## चरण 1: अपना प्रोजेक्ट सेट करें
एक नया .NET प्रोजेक्ट बनाएं या अपनी पसंदीदा IDE में मौजूदा प्रोजेक्ट खोलें।
## चरण 2: Aspose.PSD लाइब्रेरी शामिल करें
 अपने प्रोजेक्ट में Aspose.PSD लाइब्रेरी का संदर्भ जोड़ें। आप यहां से लाइब्रेरी डाउनलोड करके ऐसा कर सकते हैं[Aspose.PSD डाउनलोड पृष्ठ](https://releases.aspose.com/psd/net/).
## चरण 3: Aspose.PSD को प्रारंभ करें
अपने कोड में, PSD फ़ाइल लोड करके Aspose.PSD प्रारंभ करें:
```csharp
string dataDir = "Your Document Directory";
string sourceFileName = dataDir + "1.psd";
using (RasterImage image = Image.Load(sourceFileName) as RasterImage)
{
    // आपका कोड यहाँ
}
```
## चरण 4: PSD फ़ाइल को क्रॉप करें
PSD फ़ाइलों के लिए सही क्रॉप विधि लागू करें। रेक्टेंगल ऑब्जेक्ट का उपयोग करके क्रॉपिंग पैरामीटर निर्दिष्ट करें:
```csharp
image.Crop(new Rectangle(10, 30, 100, 100));
```
अपनी क्रॉपिंग आवश्यकताओं के अनुसार रेक्टेंगल कंस्ट्रक्टर में मानों को समायोजित करें।
## चरण 5: कटी हुई छवि को सहेजें
क्रॉप की गई छवि को PSD और PNG दोनों प्रारूपों में सहेजें:
```csharp
string exportPathPsd = dataDir + "CropTest.psd";
string exportPathPng = dataDir + "CropTest.png";
image.Save(exportPathPsd, new PsdOptions());
image.Save(exportPathPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
```
## निष्कर्ष

बधाई हो! आपने सफलतापूर्वक सीख लिया है कि .NET के लिए Aspose.PSD का उपयोग करके PSD फ़ाइलों को कैसे क्रॉप किया जाए। कुशल छवि हेरफेर के लिए इस सरल लेकिन शक्तिशाली प्रक्रिया को आपके .NET अनुप्रयोगों में निर्बाध रूप से एकीकृत किया जा सकता है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.PSD नवीनतम .NET फ्रेमवर्क के साथ संगत है?

A1: हां, नवीनतम .NET फ्रेमवर्क के साथ अनुकूलता सुनिश्चित करने के लिए Aspose.PSD को नियमित रूप से अपडेट किया जाता है।

### Q2: क्या मैं व्यावसायिक परियोजनाओं के लिए Aspose.PSD का उपयोग कर सकता हूँ?

 ए2: बिल्कुल! Aspose.PSD व्यावसायिक उपयोग के लिए उपलब्ध है। आप इसे खरीद सकते हैं[यहाँ](https://purchase.aspose.com/buy).

### Q3: क्या कोई निःशुल्क परीक्षण उपलब्ध है?

 उ3: हां, आप नि:शुल्क परीक्षण के साथ Aspose.PSD का पता लगा सकते हैं। इसे डाउनलोड करें[यहाँ](https://releases.aspose.com/).

### Q4: मुझे Aspose.PSD के लिए समर्थन कहां मिल सकता है?

 उ4: किसी भी प्रश्न या सहायता के लिए, पर जाएँ[Aspose.PSD फोरम](https://forum.aspose.com/c/psd/34).

### Q5: क्या मुझे परीक्षण उद्देश्यों के लिए अस्थायी लाइसेंस की आवश्यकता है?

 A5: हाँ, यदि आपको अस्थायी लाइसेंस की आवश्यकता है, तो आप एक प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).