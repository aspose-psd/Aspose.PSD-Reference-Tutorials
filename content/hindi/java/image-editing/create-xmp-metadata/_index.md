---
title: Java के लिए Aspose.PSD के साथ XMP मेटाडेटा बनाएँ
linktitle: XMP मेटाडेटा बनाएँ
second_title: Aspose.PSD जावा एपीआई
description: Aspose.PSD के साथ अपने Java एप्लिकेशन को बेहतर बनाएँ। बिना किसी परेशानी के XMP मेटाडेटा बनाना सीखें। अभी हमारे चरण-दर-चरण गाइड का पालन करें।
type: docs
weight: 12
url: /hi/java/image-editing/create-xmp-metadata/
---
## परिचय

जावा विकास के क्षेत्र में, छवि मेटाडेटा का प्रबंधन और हेरफेर विभिन्न अनुप्रयोगों के लिए महत्वपूर्ण है। Aspose.PSD for Java PSD फ़ाइलों को संभालने के लिए एक शक्तिशाली उपकरण के रूप में सामने आता है, और इस ट्यूटोरियल में, हम इस मजबूत लाइब्रेरी का उपयोग करके XMP मेटाडेटा बनाने में गहराई से उतरेंगे।

## आवश्यक शर्तें

इससे पहले कि हम इस ट्यूटोरियल को शुरू करें, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

- जावा डेवलपमेंट एनवायरनमेंट: आपके सिस्टम पर जावा इंस्टॉल हो, तथा जावा प्रोग्रामिंग की बुनियादी समझ हो।
-  Aspose.PSD लाइब्रेरी: Java के लिए Aspose.PSD लाइब्रेरी डाउनलोड करें और सेट अप करें। आप लाइब्रेरी और विस्तृत दस्तावेज़ पा सकते हैं[यहाँ](https://reference.aspose.com/psd/java/).
- आपकी दस्तावेज़ निर्देशिका: वह निर्देशिका निर्धारित करें जहाँ आपकी दस्तावेज़ फ़ाइलें संग्रहीत हैं।

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

## चरण 2: एक नई छवि बनाएँ

```java
// नमूना प्रयोजनों के लिए एक बिल्कुल नई छवि बनाएँ
PsdImage image = new PsdImage(rect.getWidth(), rect.getHeight());
```

## चरण 3: XMP हेडर बनाएं

```java
// XMP-Header का एक उदाहरण बनाएँ
XmpHeaderPi xmpHeader = new XmpHeaderPi();
xmpHeader.setGuid("Your Document Directory");
```

## चरण 4: XMP ट्रेलर बनाएं

```java
// Xmp-TrailerPi का एक उदाहरण बनाएँ
XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## चरण 5: XMP मेटाडेटा बनाएँ

```java
// विभिन्न विशेषताओं को सेट करने के लिए XMPmeta वर्ग का एक उदाहरण बनाएँ
XmpMeta xmpMeta = new XmpMeta();
xmpMeta.addAttribute("Author", "Mr Smith");
xmpMeta.addAttribute("Description", "The fake metadata value");
```

## चरण 6: XMP पैकेट रैपर बनाएं

```java
// XmpPacketWrapper का एक इंस्टेंस बनाएं जिसमें सभी मेटाडेटा शामिल हों
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

## चरण 8: XMP मेटाडेटा में फ़ोटोशॉप पैकेज जोड़ें

```java
// XMP मेटाडेटा में फ़ोटोशॉप पैकेज जोड़ें
xmpData.addPackage(photoshopPackage);
```

## चरण 9: डबलिनकोर विशेषताएँ सेट करें

```java
// DublinCore पैकेज का एक उदाहरण बनाएं और DublinCore विशेषताएँ सेट करें
DublinCorePackage dublinCorePackage = new DublinCorePackage();
dublinCorePackage.setAuthor("Charles Bukowski");
dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
dublinCorePackage.addValue("dc:movie", "Barfly");
```

## चरण 10: XMP मेटाडेटा में DublinCore पैकेज जोड़ें

```java
// XMP मेटाडेटा में DublinCore पैकेज जोड़ें
xmpData.addPackage(dublinCorePackage);
```

## चरण 11: XMP मेटाडेटा को छवि में अपडेट करें

```java
//छवि में XMP मेटाडेटा अपडेट करें
image.setXmpData(xmpData);
```

## चरण 12: छवि सहेजें

```java
// छवि को डिस्क या मेमोरी स्ट्रीम में सहेजें
image.save("Your Document Directory" + "create_XMP_Metadata.psd");
```

## निष्कर्ष

बधाई हो! आपने Aspose.PSD for Java का उपयोग करके किसी छवि के लिए सफलतापूर्वक XMP मेटाडेटा बनाया है। इस ट्यूटोरियल ने आपको अपने Java अनुप्रयोगों में मेटाडेटा को सहजता से बढ़ाने और प्रबंधित करने के लिए आवश्यक चरणों से सुसज्जित किया है।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: क्या Aspose.PSD विभिन्न छवि प्रारूपों के साथ संगत है?

A1: हां, Aspose.PSD विभिन्न छवि प्रारूपों का समर्थन करता है, विभिन्न फ़ाइल प्रकारों को संभालने में बहुमुखी प्रतिभा प्रदान करता है।

### प्रश्न 2: क्या मैं Aspose.PSD का उपयोग करके मौजूदा मेटाडेटा में हेरफेर कर सकता हूं?

A2: बिल्कुल, Aspose.PSD आपको छवियों के भीतर मौजूदा मेटाडेटा को संशोधित और अद्यतन करने की अनुमति देता है।

### प्रश्न 3: क्या Aspose.PSD द्वारा संभाले जा सकने वाले छवि आकार पर कोई सीमाएं हैं?

A3: Aspose.PSD को विभिन्न आकारों की छवियों को संभालने के लिए डिज़ाइन किया गया है, जो आपकी परियोजनाओं के लिए मापनीयता सुनिश्चित करता है।

### प्रश्न 4: क्या Aspose.PSD के लिए कोई परीक्षण संस्करण उपलब्ध है?

 A4: हाँ, आप एक निःशुल्क परीक्षण प्राप्त करके Aspose.PSD की क्षमताओं का पता लगा सकते हैं[यहाँ](https://releases.aspose.com/).

### प्रश्न 5: मैं Aspose.PSD-संबंधित प्रश्नों के लिए सहायता कहां से प्राप्त कर सकता हूं?

 A5: किसी भी सहायता या प्रश्न के लिए, पर जाएँ[Aspose.PSD फ़ोरम](https://forum.aspose.com/c/psd/34).