---
title: .NET के लिए Aspose.PSD में XMP मेटाडेटा बनाना
linktitle: एक्सएमपी मेटाडेटा बनाना
second_title: Aspose.PSD .NET एपीआई
description: .NET के लिए Aspose.PSD में XMP मेटाडेटा निर्माण का अन्वेषण करें। निर्बाध हेरफेर के साथ छवि संगठन को बढ़ाएं।
type: docs
weight: 10
url: /hi/net/file-and-font-handling/create-xmp-metadata/
---
## परिचय

.NET विकास की गतिशील दुनिया में, छवियों में सटीकता के साथ हेरफेर करना कई अनुप्रयोगों का एक महत्वपूर्ण पहलू है। यह ट्यूटोरियल .NET के लिए Aspose.PSD में XMP मेटाडेटा के निर्माण की पड़ताल करता है, जो एक शक्तिशाली लाइब्रेरी है जो इमेज प्रोसेसिंग कार्यों को सरल बनाती है। एक्सएमपी (एक्स्टेंसिबल मेटाडेटा प्लेटफ़ॉर्म) आपको छवि फ़ाइलों के भीतर मेटाडेटा एम्बेड करने में सक्षम बनाता है, जिससे कुशल संगठन और छवियों से जुड़ी जानकारी की पुनर्प्राप्ति की सुविधा मिलती है।

## आवश्यक शर्तें

ट्यूटोरियल में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

-  .NET लाइब्रेरी के लिए Aspose.PSD: लाइब्रेरी को डाउनलोड और इंस्टॉल करें[Aspose.PSD दस्तावेज़ीकरण](https://reference.aspose.com/psd/net/).

- विकास परिवेश: विज़ुअल स्टूडियो या अपने पसंदीदा IDE के साथ एक .NET विकास परिवेश स्थापित करें।

- बुनियादी .NET ज्ञान: अपने आप को बुनियादी .NET अवधारणाओं से परिचित कराएं, क्योंकि यह ट्यूटोरियल .NET विकास की मूलभूत समझ मानता है।

## नामस्थान आयात करें

अपने .NET प्रोजेक्ट में, Aspose.PSD कार्यक्षमता तक पहुँचने के लिए आवश्यक नामस्थान शामिल करें:

```csharp
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.Xmp;
using Aspose.PSD.Xmp.Schemas.DublinCore;
using Aspose.PSD.Xmp.Schemas.Photoshop;
using System;
using System.IO;
```

अब, आइए एक्सएमपी मेटाडेटा बनाने की प्रक्रिया को व्यापक चरणों की एक श्रृंखला में विभाजित करें।

## चरण 1: छवि का आकार और आयत निर्दिष्ट करें

```csharp
// दस्तावेज़ निर्देशिका का पथ.
string dataDir = RunExamples.GetDataDir_DrawingAndFormattingImages();

//आयत को परिभाषित करके छवि का आकार निर्दिष्ट करें
Rectangle rect = new Rectangle(0, 0, 100, 200);
```

## चरण 2: एक नई छवि बनाएं

```csharp
// नमूना उद्देश्यों के लिए बिल्कुल नई छवि बनाएं
using (var image = new PsdImage(rect.Width, rect.Height))
{
    // छवि हेरफेर कोड यहां जाता है...
}
```

## चरण 3: एक्सएमपी-हेडर और एक्सएमपी-ट्रेलर बनाएं

```csharp
// एक्सएमपी-हेडर का एक उदाहरण बनाएं
XmpHeaderPi xmpHeader = new XmpHeaderPi(Guid.NewGuid().ToString());

// विभिन्न विशेषताओं को सेट करने के लिए XMP-TrailerPi, XMPmeta क्लास का एक उदाहरण बनाएं
XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
XmpMeta xmpMeta = new XmpMeta();
```

## चरण 4: XMP विशेषताएँ सेट करें

```csharp
// उदाहरण के लिए, XMP विशेषताएँ सेट करें:
xmpMeta.AddAttribute("Author", "Mr Smith");
xmpMeta.AddAttribute("Description", "The fake metadata value");
```

## चरण 5: एक्सएमपी पैकेट रैपर बनाएं

```csharp
// XmpPacketWrapper का एक उदाहरण बनाएं जिसमें सभी मेटाडेटा शामिल हों
XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## चरण 6: फ़ोटोशॉप पैकेज बनाएं और विशेषताएँ सेट करें

```csharp
// फ़ोटोशॉप पैकेज का एक उदाहरण बनाएं और फ़ोटोशॉप विशेषताएँ सेट करें
PhotoshopPackage photoshopPackage = new PhotoshopPackage();
photoshopPackage.SetCity("London");
photoshopPackage.SetCountry("England");
photoshopPackage.SetColorMode(ColorMode.Rgb);
photoshopPackage.SetCreatedDate(DateTime.UtcNow);
```

## चरण 7: फ़ोटोशॉप पैकेज को XMP मेटाडेटा में जोड़ें

```csharp
// XMP मेटाडेटा में फ़ोटोशॉप पैकेज जोड़ें
xmpData.AddPackage(photoshopPackage);
```

## चरण 8: डबलिनकोर पैकेज बनाएं और विशेषताएँ सेट करें

```csharp
// डबलिनकोर पैकेज का एक उदाहरण बनाएं और डबलिनकोर विशेषताएँ सेट करें
DublinCorePackage dublinCorePackage = new DublinCorePackage();
dublinCorePackage.SetAuthor("Mudassir Fayyaz");
dublinCorePackage.SetTitle("Confessions of a Man Insane Enough to Live With the Beasts");
dublinCorePackage.AddValue("dc:movie", "Barfly");
```

## चरण 9: एक्सएमपी मेटाडेटा में डबलिनकोर पैकेज जोड़ें

```csharp
// XMP मेटाडेटा में डबलिनकोर पैकेज जोड़ें
xmpData.AddPackage(dublinCorePackage);
```

## चरण 10: एक्सएमपी मेटाडेटा अपडेट करें और छवि सहेजें

```csharp
using (var ms = new MemoryStream())
{
    // छवि में XMP मेटाडेटा अपडेट करें और छवि को डिस्क पर या मेमोरी स्ट्रीम में सहेजें
    image.XmpData = xmpData;
    image.Save(ms);
    image.Save(dataDir + "ee.psd");
    ms.Seek(0, System.IO.SeekOrigin.Begin);
}
```

## चरण 11: छवि लोड करें और मेटाडेटा पढ़ें

```csharp
// मेटाडेटा पढ़ने/प्राप्त करने के लिए छवि को मेमोरी स्ट्रीम या डिस्क से लोड करें
using (var img = (PsdImage)Image.Load(ms))
{
    // एक्सएमपी मेटाडेटा प्राप्त करना
    XmpPacketWrapper imgXmpData = img.XmpData;
    foreach (XmpPackage package in imgXmpData.Packages)
    {
        // पैकेज डेटा का उपयोग करें...
    }
}
```

## निष्कर्ष

बधाई हो! आपने .NET के लिए Aspose.PSD में XMP मेटाडेटा सफलतापूर्वक बना लिया है। यह शक्तिशाली क्षमता आपकी छवि प्रसंस्करण क्षमताओं को बढ़ाती है, जिससे कुशल संगठन और महत्वपूर्ण जानकारी की पुनर्प्राप्ति की अनुमति मिलती है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या .NET के लिए Aspose.PSD सभी छवि प्रारूपों के साथ संगत है?

A1: Aspose.PSD मुख्य रूप से PSD (एडोब फोटोशॉप) फ़ाइल प्रारूप पर केंद्रित है लेकिन विभिन्न अन्य प्रारूपों का समर्थन करता है।

### Q2: क्या मैं .NET के लिए Aspose.PSD का उपयोग करके मौजूदा XMP मेटाडेटा में हेरफेर कर सकता हूँ?

A2: हाँ, Aspose.PSD आपको मौजूदा XMP मेटाडेटा को पढ़ने और संशोधित करने की अनुमति देता है।

### Q3: क्या .NET के लिए Aspose.PSD का उपयोग करते समय छवि आकार पर कोई सीमाएँ हैं?

A3: Aspose.PSD विभिन्न आकारों की छवियों को संभाल सकता है, लेकिन बहुत बड़ी छवियों के लिए अतिरिक्त विचारों की आवश्यकता हो सकती है।

### Q4: .NET के लिए Aspose.PSD को कितनी बार अपडेट किया जाता है?

A4: नवीनतम .NET फ्रेमवर्क संस्करणों और उद्योग मानकों के साथ अनुकूलता सुनिश्चित करने के लिए अपडेट नियमित रूप से जारी किए जाते हैं।

### Q5: क्या Aspose.PSD समर्थन के लिए कोई सामुदायिक मंच है?

 उत्तर: हाँ, आप इस पर समर्थन और चर्चाएँ पा सकते हैं[Aspose.PSD फोरम](https://forum.aspose.com/c/psd/34).