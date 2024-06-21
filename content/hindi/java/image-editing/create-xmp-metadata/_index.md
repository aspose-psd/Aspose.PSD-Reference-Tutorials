---
title: जावा के लिए Aspose.PSD के साथ XMP मेटाडेटा बनाएं
linktitle: एक्सएमपी मेटाडेटा बनाएं
second_title: Aspose.PSD जावा एपीआई
description: Aspose.PSD के साथ अपने जावा एप्लिकेशन को बेहतर बनाएं। आसानी से XMP मेटाडेटा बनाना सीखें। अभी हमारे चरण-दर-चरण मार्गदर्शिका का पालन करें।
type: docs
weight: 12
url: /hi/java/image-editing/create-xmp-metadata/
---
## परिचय

जावा विकास के क्षेत्र में, विभिन्न अनुप्रयोगों के लिए छवि मेटाडेटा का प्रबंधन और हेरफेर करना महत्वपूर्ण है। जावा के लिए Aspose.PSD, PSD फ़ाइलों को संभालने के लिए एक शक्तिशाली उपकरण के रूप में खड़ा है, और इस ट्यूटोरियल में, हम इस मजबूत लाइब्रेरी का उपयोग करके XMP मेटाडेटा बनाने में गहराई से उतरेंगे।

## आवश्यक शर्तें

इससे पहले कि हम इस ट्यूटोरियल को शुरू करें, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

- जावा विकास पर्यावरण: क्या आपके सिस्टम पर जावा स्थापित है, और जावा प्रोग्रामिंग की बुनियादी समझ है।
-  Aspose.PSD लाइब्रेरी: जावा के लिए Aspose.PSD लाइब्रेरी डाउनलोड करें और सेट करें। आप पुस्तकालय और विस्तृत दस्तावेज़ीकरण पा सकते हैं[यहाँ](https://reference.aspose.com/psd/java/).
- आपकी दस्तावेज़ निर्देशिका: उस निर्देशिका को परिभाषित करें जहाँ आपकी दस्तावेज़ फ़ाइलें संग्रहीत हैं।

## पैकेज आयात करें

अपने जावा प्रोजेक्ट में, Aspose.PSD कार्यक्षमताओं का लाभ उठाने के लिए आवश्यक पैकेज आयात करें:

```java
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.system.io.MemoryStream;
import com.aspose.psd.xmp.XmpHeaderPi;
import com.aspose.psd.xmp.XmpMeta;
import com.aspose.psd.xmp.XmpPacketWrapper;
import com.aspose.psd.xmp.XmpTrailerPi;
import com.aspose.psd.xmp.schemas.dublincore.DublinCorePackage;
import com.aspose.psd.xmp.schemas.photoshop.ColorMode;
import com.aspose.psd.xmp.schemas.photoshop.PhotoshopPackage;
```

## चरण 1: छवि का आकार निर्दिष्ट करें

```java
//आयत को परिभाषित करके छवि का आकार निर्दिष्ट करें
Rectangle rect = new Rectangle(0, 0, 100, 200);
```

## चरण 2: एक नई छवि बनाएं

```java
// नमूना उद्देश्यों के लिए एक बिल्कुल नई छवि बनाएं
PsdImage image = new PsdImage(rect.getWidth(), rect.getHeight());
```

## चरण 3: एक्सएमपी हेडर बनाएं

```java
// एक्सएमपी-हेडर का एक उदाहरण बनाएं
XmpHeaderPi xmpHeader = new XmpHeaderPi();
xmpHeader.setGuid("Your Document Directory");
```

## चरण 4: एक्सएमपी ट्रेलर बनाएं

```java
// Xmp-TrailerPi का एक उदाहरण बनाएं
XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## चरण 5: एक्सएमपी मेटाडेटा बनाएं

```java
// विभिन्न विशेषताएँ सेट करने के लिए XMPmeta क्लास का एक उदाहरण बनाएँ
XmpMeta xmpMeta = new XmpMeta();
xmpMeta.addAttribute("Author", "Mr Smith");
xmpMeta.addAttribute("Description", "The fake metadata value");
```

## चरण 6: एक्सएमपी पैकेट रैपर बनाएं

```java
// XmpPacketWrapper का एक उदाहरण बनाएं जिसमें सभी मेटाडेटा शामिल हों
XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## चरण 7: फ़ोटोशॉप विशेषताएँ सेट करें

```java
// फ़ोटोशॉप पैकेज का एक उदाहरण बनाएं और फ़ोटोशॉप विशेषताएँ सेट करें
PhotoshopPackage photoshopPackage = new PhotoshopPackage();
photoshopPackage.setCity("London");
photoshopPackage.setCountry("England");
photoshopPackage.setColorMode(ColorMode.Rgb);
```

## चरण 8: फ़ोटोशॉप पैकेज को XMP मेटाडेटा में जोड़ें

```java
// XMP मेटाडेटा में फ़ोटोशॉप पैकेज जोड़ें
xmpData.addPackage(photoshopPackage);
```

## चरण 9: डबलिनकोर विशेषताएँ सेट करें

```java
// डबलिनकोर पैकेज का एक उदाहरण बनाएं और डबलिनकोर विशेषताएँ सेट करें
DublinCorePackage dublinCorePackage = new DublinCorePackage();
dublinCorePackage.setAuthor("Charles Bukowski");
dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
dublinCorePackage.addValue("dc:movie", "Barfly");
```

## चरण 10: एक्सएमपी मेटाडेटा में डबलिनकोर पैकेज जोड़ें

```java
// XMP मेटाडेटा में डबलिनकोर पैकेज जोड़ें
xmpData.addPackage(dublinCorePackage);
```

## चरण 11: XMP मेटाडेटा को छवि में अपडेट करें

```java
//छवि में XMP मेटाडेटा अपडेट करें
image.setXmpData(xmpData);
```

## चरण 12: छवि सहेजें

```java
// छवि को डिस्क पर या मेमोरी स्ट्रीम में सहेजें
image.save("Your Document Directory" + "create_XMP_Metadata.psd");
```

## निष्कर्ष

बधाई हो! आपने जावा के लिए Aspose.PSD का उपयोग करके एक छवि के लिए सफलतापूर्वक XMP मेटाडेटा बनाया है। इस ट्यूटोरियल ने आपको आपके जावा अनुप्रयोगों में मेटाडेटा को निर्बाध रूप से बढ़ाने और प्रबंधित करने के लिए आवश्यक चरणों से सुसज्जित किया है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.PSD विभिन्न छवि प्रारूपों के साथ संगत है?

A1: हां, Aspose.PSD विभिन्न छवि प्रारूपों का समर्थन करता है, जो विभिन्न फ़ाइल प्रकारों को संभालने में बहुमुखी प्रतिभा प्रदान करता है।

### Q2: क्या मैं Aspose.PSD का उपयोग करके मौजूदा मेटाडेटा में हेरफेर कर सकता हूँ?

A2: बिल्कुल, Aspose.PSD आपको छवियों के भीतर मौजूदा मेटाडेटा को संशोधित और अद्यतन करने की अनुमति देता है।

### Q3: क्या छवि आकार पर कोई सीमाएँ हैं जिन्हें Aspose.PSD संभाल सकता है?

A3: Aspose.PSD को आपकी परियोजनाओं के लिए स्केलेबिलिटी सुनिश्चित करते हुए, विभिन्न आकारों की छवियों को संभालने के लिए डिज़ाइन किया गया है।

### Q4: क्या Aspose.PSD के लिए कोई परीक्षण संस्करण उपलब्ध है?

 उ4: हाँ, आप निःशुल्क परीक्षण प्राप्त करके Aspose.PSD की क्षमताओं का पता लगा सकते हैं।[यहाँ](https://releases.aspose.com/).

### Q5: मैं Aspose.PSD से संबंधित प्रश्नों के लिए सहायता कहाँ से प्राप्त कर सकता हूँ?

 A5: किसी भी सहायता या प्रश्न के लिए, पर जाएँ[Aspose.PSD फोरम](https://forum.aspose.com/c/psd/34).