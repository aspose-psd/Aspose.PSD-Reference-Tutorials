---
date: 2026-01-01
description: XMP मेटाडेटा बनाना, PSD फ़ाइलों में XMP जोड़ना, और Aspose.PSD for Java
  के साथ इमेज मेटाडेटा अपडेट करना सीखें। इस चरण‑दर‑चरण गाइड को अभी फ़ॉलो करें।
linktitle: Create XMP Metadata
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java के साथ XMP मेटाडेटा बनाएं
url: /hi/java/image-editing/create-xmp-metadata/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java के साथ XMP मेटाडेटा बनाएं

## परिचय

इमेज मेटाडेटा का प्रबंधन उन जावा डेवलपर्स के लिए एक सामान्य आवश्यकता है जो फ़ोटोशॉप (PSD) फ़ाइलों के साथ काम करते हैं। इस ट्यूटोरियल में आप Aspose.PSD लाइब्रेरी का उपयोग करके **XMP मेटाडेटा कैसे बनाएं**, PSD इमेज में XMP जोड़ना, और प्रोग्रामेटिक रूप से इमेज मेटाडेटा अपडेट करना सीखेंगे। हम प्रत्येक चरण को विस्तार से देखेंगे, समझाएंगे कि प्रत्येक भाग क्यों महत्वपूर्ण है, और आपको व्यावहारिक टिप्स देंगे जिन्हें आप वास्तविक प्रोजेक्ट्स में लागू कर सकते हैं।

## त्वरित उत्तर
- **XMP मेटाडेटा क्या है?** इमेज फ़ाइलों के भीतर वर्णनात्मक जानकारी (लेखक, कीवर्ड आदि) एम्बेड करने के लिए एक मानकीकृत फ़ॉर्मेट।  
- **Aspose.PSD क्यों उपयोग करें?** यह फ़ोटोशॉप के बिना PSD फ़ाइलों को बनाने, पढ़ने और संपादित करने के लिए एक शुद्ध‑जावा API प्रदान करता है।  
- **क्या मैं मौजूदा PSD में XMP जोड़ सकता हूँ?** हाँ – आप `setXmpData` का उपयोग करके तुरंत इमेज मेटाडेटा अपडेट कर सकते हैं।  
- **मुख्य चरण क्या हैं?** इमेज साइज सेट करें, हेडर/ट्रेलर बनाएं, XMP पैकेज बनाएं, उन्हें अटैच करें, और सेव करें।  
- **क्या मुझे लाइसेंस चाहिए?** विकास के लिए एक फ्री ट्रायल काम करता है; प्रोडक्शन के लिए एक कमर्शियल लाइसेंस आवश्यक है।

## जावा में “XMP मेटाडेटा बनाना” क्या है?

XMP मेटाडेटा बनाना का मतलब है एक XMP पैकेट (हेडर, बॉडी, ट्रेलर) बनाना जो इमेज का विवरण देता है और फिर उस पैकेट को PSD फ़ाइल में एम्बेड करना। Aspose.PSD लाइब्रेरी लो‑लेवल विवरणों को एब्स्ट्रैक्ट करती है, जिससे आप उस सामग्री पर ध्यान केंद्रित कर सकते हैं जिसे आप स्टोर करना चाहते हैं।

## PSD फ़ाइलों में XMP क्यों जोड़ें?

- **सर्चेबिलिटी:** लेखक, शीर्षक, या कस्टम टैग्स के आधार पर शक्तिशाली एसेट‑मैनेजमेंट सर्च को सक्षम करता है।  
- **इंटरऑपरेबिलिटी:** XMP को एडोब प्रोडक्ट्स, लाइटरूम, और कई DAM सिस्टम द्वारा पहचाना जाता है।  
- **वर्ज़न कंट्रोल:** प्रोसेसिंग इतिहास (जैसे, शहर, कलर मोड) को सीधे फ़ाइल के अंदर स्टोर करें।

## आवश्यकताएँ

- **जावा डेवलपमेंट एनवायरनमेंट:** JDK 8 या उससे ऊपर स्थापित हो और जावा की बुनियादी समझ हो।  
- **Aspose.PSD लाइब्रेरी:** Aspose.PSD for Java लाइब्रेरी डाउनलोड करें और सेटअप करें। आप लाइब्रेरी और विस्तृत दस्तावेज़ीकरण [यहाँ](https://reference.aspose.com/psd/java/) पा सकते हैं।  
- **आपका डॉक्यूमेंट डायरेक्टरी:** तय करें कि आप अपने सिस्टम पर PSD फ़ाइलें कहाँ पढ़ेंगे/लिखेंगे।

## पैकेज इम्पोर्ट करें

In your Java project, import the necessary packages to leverage Aspose.PSD functionalities:

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

## चरण 1: इमेज साइज निर्दिष्ट करें

First, define the canvas dimensions for the new PSD image.

```java
// Specify the size of the image by defining a Rectangle
Rectangle rect = new Rectangle(0, 0, 100, 200);
```

## चरण 2: एक नई इमेज बनाएं

Create a blank PSD image that we will later enrich with XMP metadata.

```java
// Create a brand new image for sample purposes
PsdImage image = new PsdImage(rect.getWidth(), rect.getHeight());
```

## चरण 3: XMP हेडर बनाएं

The header contains the opening XML processing instruction and a GUID that identifies the document.

```java
// Create an instance of XMP-Header
XmpHeaderPi xmpHeader = new XmpHeaderPi();
xmpHeader.setGuid("Your Document Directory");
```

## चरण 4: XMP ट्रेलर बनाएं

The trailer marks the end of the XMP packet. Setting the `true` flag writes the closing processing instruction.

```java
// Create an instance of Xmp-TrailerPi 
XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## चरण 5: XMP मेटाडेटा बनाएं

Add generic attributes such as author and description to the core XMP metadata object.

```java
// Create an instance of XMPmeta class to set different attributes
XmpMeta xmpMeta = new XmpMeta();
xmpMeta.addAttribute("Author", "Mr Smith");
xmpMeta.addAttribute("Description", "The fake metadata value");
```

## चरण 6: XMP पैकेट रैपर बनाएं

Wrap the header, trailer, and core metadata into a single packet that can be attached to the image.

```java
// Create an instance of XmpPacketWrapper that contains all metadata
XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## चरण 7: Photoshop एट्रिब्यूट सेट करें

Populate Photoshop‑specific fields (city, country, color mode) that many Adobe tools expect.

```java
// Create an instance of Photoshop package and set Photoshop attributes
PhotoshopPackage photoshopPackage = new PhotoshopPackage();
photoshopPackage.setCity("London");
photoshopPackage.setCountry("England");
photoshopPackage.setColorMode(ColorMode.Rgb);
```

## चरण 8: XMP मेटाडेटा में Photoshop पैकेज जोड़ें

Attach the Photoshop package to the XMP packet.

```java
// Add Photoshop package into XMP metadata
xmpData.addPackage(photoshopPackage);
```

## चरण 9: DublinCore एट्रिब्यूट सेट करें

Add Dublin Core metadata such as author, title, and a custom movie tag.

```java
// Create an instance of DublinCore package and set DublinCore attributes
DublinCorePackage dublinCorePackage = new DublinCorePackage();
dublinCorePackage.setAuthor("Charles Bukowski");
dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
dublinCorePackage.addValue("dc:movie", "Barfly");
```

## चरण 10: XMP मेटाडेटा में DublinCore पैकेज जोड़ें

Combine the Dublin Core package with the existing XMP packet.

```java
// Add DublinCore Package into XMP metadata
xmpData.addPackage(dublinCorePackage);
```

## चरण 11: इमेज में XMP मेटाडेटा अपडेट करें

Now embed the complete XMP packet into the PSD image.

```java
// Update XMP metadata into the image
image.setXmpData(xmpData);
```

## चरण 12: इमेज सेव करें

Finally, write the PSD file to disk (or a memory stream) so the metadata is persisted.

```java
// Save the image on the disk or in a memory stream
image.save("Your Document Directory" + "create_XMP_Metadata.psd");
```

## सामान्य समस्याएँ और समाधान

| समस्या | क्यों होता है | समाधान |
|-------|----------------|-----|
| **`NullPointerException` on `setXmpData`** | XMP पैकेट पूरी तरह से नहीं बना था (हेडर/ट्रेलर गायब)। | `setXmpData` कॉल करने से पहले सुनिश्चित करें कि आपने `XmpHeaderPi`, `XmpTrailerPi` बनाए हैं और सभी पैकेज जोड़ें। |
| **Metadata Photoshop में दिखाई नहीं देता** | Photoshop को XMP पैकेट सही ढंग से रैप्ड चाहिए। | `XmpTrailerPi(true)` उपयोग किया गया है और पैकेट इमेज के साथ सेव हुआ है, यह सुनिश्चित करें। |
| **फ़ाइल पाथ त्रुटियाँ** | उचित अनुमतियों के बिना रिलेटिव पाथ का उपयोग। | एब्सॉल्यूट पाथ उपयोग करें या सुनिश्चित करें कि एप्लिकेशन को लक्ष्य फ़ोल्डर में लिखने की अनुमति है। |

## अक्सर पूछे जाने वाले प्रश्न

**प्रश्न:** क्या Aspose.PSD विभिन्न इमेज फ़ॉर्मेट्स के साथ संगत है?  
**उत्तर:** हाँ, Aspose.PSD PSD, PSB, BMP, GIF, JPEG, PNG, TIFF आदि फ़ॉर्मेट्स को सपोर्ट करता है, जिससे आपको विभिन्न फ़ॉर्मेट्स में लचीलापन मिलता है।

**प्रश्न:** क्या मैं Aspose.PSD का उपयोग करके मौजूदा मेटाडेटा को बदल सकता हूँ?  
**उत्तर:** बिल्कुल। आप मौजूदा PSD लोड कर सकते हैं, `getXmpData()` से उसका XMP डेटा प्राप्त कर सकते हैं, पैकेट को संशोधित कर सकते हैं, और उसे फिर से सेव कर सकते हैं।

**प्रश्न:** क्या Aspose.PSD द्वारा संभाली जा सकने वाली इमेज साइज पर कोई सीमाएँ हैं?  
**उत्तर:** Aspose.PSD बड़े इमेज (कई गीगापिक्सेल तक) के साथ काम करने के लिए डिज़ाइन किया गया है, जिसकी सीमा केवल उपलब्ध मेमोरी पर निर्भर करती है।

**प्रश्न:** क्या Aspose.PSD का ट्रायल संस्करण उपलब्ध है?  
**उत्तर:** हाँ, आप Aspose.PSD की क्षमताओं को एक फ्री ट्रायल प्राप्त करके देख सकते हैं [यहाँ](https://releases.aspose.com/)।

**प्रश्न:** Aspose.PSD से संबंधित प्रश्नों के लिए मैं कहाँ सहायता ले सकता हूँ?  
**उत्तर:** किसी भी सहायता या प्रश्नों के लिए, [Aspose.PSD फ़ोरम](https://forum.aspose.com/c/psd/34) पर जाएँ।

## निष्कर्ष

अब आप **XMP मेटाडेटा कैसे बनाएं**, PSD में XMP जोड़ना, और Aspose.PSD for Java का उपयोग करके इमेज मेटाडेटा अपडेट करना पूरी तरह से समझ गए हैं। ये चरण आपको अपनी इमेज में एम्बेडेड वर्णनात्मक जानकारी पर पूर्ण नियंत्रण देते हैं, जिससे वे सर्चेबल बनते हैं और डाउनस्ट्रीम वर्कफ़्लो के लिए तैयार होते हैं। अतिरिक्त XMP स्कीमा के साथ प्रयोग करने या इस कोड को बड़े इमेज‑प्रोसेसिंग पाइपलाइन में इंटीग्रेट करने में संकोच न करें।

---

**Last Updated:** 2026-01-01  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}