---
date: 2026-01-27
description: हमारे चरण‑दर‑चरण ट्यूटोरियल के साथ Aspose.PSD for Java (asp) का उपयोग
  करके PSD छवियों से विशिष्ट EXIF टैग कैसे पढ़ें, सीखें। अपनी इमेज प्रोसेसिंग कौशल
  को बढ़ाएँ।
linktitle: Read Specific EXIF Tags Information in Java
second_title: Aspose.PSD Java API
title: Aspose (asp) के साथ जावा में विशिष्ट EXIF टैग जानकारी पढ़ें
url: /hi/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose (asp) के साथ जावा में विशिष्ट EXIF टैग जानकारी पढ़ें

## परिचय
क्या आप जावा **asp लाइब्रेरी (Aspose.PSD)** का उपयोग करके PSD फ़ाइलों को संभालने की दुनिया में डुबकी लगाना चाहते हैं? इस ट्यूटोरियल में आप सीखेंगे कि **EXIF डेटा Java‑स्टाइल** से PSD इमेज से कैसे निकालें, केवल आवश्यक टैग पढ़ें, और उन्हें कंसोल पर प्रिंट करें। हम विकास पर्यावरण सेटअप से लेकर WhiteBalance, ISO speed, और focal length जैसे मेटाडेटा निकालने तक सब कुछ कवर करेंगे। चलिए शुरू करते हैं!

## तुरंत जवाब
- **जावा में PSD से EXIF डेटा पढ़ने वाली लाइब्रेरी कौन सी है?** Aspose.PSD (asp)  
- **कौन से टैग निकाले जा सकते हैं?** WhiteBalance, PixelXDimension, PixelYDimension, ISOSpeed, FocalLength, आदि।  
- **उत्पादन के लिए लाइसेंस चाहिए?** हाँ, एक वाणिज्यिक लाइसेंस आवश्यक है; एक फ्री ट्रायल उपलब्ध है।  
- **क्या इसे अन्य इमेज फ़ॉर्मेट्स के साथ उपयोग कर सकते हैं?** वही API PNG, JPEG, TIFF को `java image metadata extraction` के माध्यम से सपोर्ट करता है।  
- **इम्प्लीमेंटेशन में कितना समय लगेगा?** बेसिक रीड‑ओनली परिदृश्य के लिए लगभग 10‑15 मिनट।

## **asp** (Java के लिए Aspose.PSD) क्या है?
Aspose.PSD for Java एक शक्तिशाली, **pure‑Java** लाइब्रेरी है जो डेवलपर्स को Adobe Photoshop फ़ाइलों (PSD, PSB) के साथ बिना Photoshop इंस्टॉल किए काम करने देती है। यह लेयर्स, रिसोर्सेज, और मेटाडेटा—जिसमें EXIF टैग भी शामिल हैं—पर पूरी पहुँच प्रदान करती है, जिससे **java image metadata extraction** कार्य आसान हो जाता है।

## EXIF ​​निकालने के लिए Aspose.PSD (asp) का इस्तेमाल क्यों करें?
- **नेटीव Photoshop की आवश्यकता नहीं** – जावा चलाने वाले किसी भी प्लेटफ़ॉर्म पर काम करता है।  
- **उच्च‑फ़िडेलिटी मेटाडेटा एक्सेस** – फ़ाइल में संग्रहीत सटीक कैमरा सेटिंग्स प्राप्त करें।  
- **सरल API** – साफ़, ऑब्जेक्ट‑ओरिएंटेड मेथड्स कोड को पठनीय बनाते हैं।  
- **विस्तृत फ़ॉर्मेट सपोर्ट** – PSD, PSB को संभालें और PNG/JPEG/TIFF में आसानी से कन्वर्ट करें।

## ज़रूरी शर्तें
कोड में डुबकी लगाने से पहले आपको निम्नलिखित चीज़ें चाहिए होंगी:

1. **Java Development Kit (JDK):** सुनिश्चित करें कि आपके मशीन पर JDK इंस्टॉल है। आप इसे [Oracle JDK वेबसाइट](https://www.oracle.com/java/technologies/javase-downloads.html) से डाउनलोड कर सकते हैं।  
2. **Aspose.PSD for Java:** लाइब्रेरी को [यहाँ](https://releases.aspose.com/psd/java/) से डाउनलोड करें।  
3. **Integrated Development Environment (IDE):** IntelliJ IDEA, Eclipse, या NetBeans जैसे IDE कोडिंग को सुविधाजनक बनाते हैं।  
4. **PSD फ़ाइल:** EXIF डेटा वाली एक PSD फ़ाइल। आप इस ट्यूटोरियल में प्रदान किए गए सैंपल का उपयोग कर सकते हैं या कोई भी EXIF टैग वाली PSD फ़ाइल ले सकते हैं।

## पैकेज इंपोर्ट करें
सबसे पहले, आपको आवश्यक Aspose.PSD पैकेजों को अपने जावा प्रोजेक्ट में इम्पोर्ट करना होगा। इसे सेटअप करने का तरीका नीचे दिया गया है।

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## स्टेप 1: PSD इमेज लोड करें
शुरू करने के लिए, अपने PSD फ़ाइल को एप्लिकेशन में लोड करें। सुनिश्चित करें कि फ़ाइल पाथ सही ढंग से निर्दिष्ट है।

```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```

इस चरण में हम `Image.load()` मेथड का उपयोग करके PSD फ़ाइल लोड करते हैं। `PsdImage` क्लास PSD इमेज को प्रतिनिधित्व करती है, और हम लोडेड इमेज को इस क्लास में कास्ट करके PSD‑विशिष्ट कार्यक्षमताओं तक पहुँचते हैं।

## स्टेप 2: इमेज रिसोर्स पर इटरेट करें
अब हमें इमेज रिसोर्सेज़ पर इटररेट करना है ताकि थंबनेल रिसोर्स मिले, जिसमें आमतौर पर EXIF डेटा होता है।

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || 
        image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // Further processing will be done here
    }
}
```

हम `for` लूप के ज़रिए इमेज रिसोर्सेज़ को पार करते हैं। लक्ष्य यह पहचानना है कि कौन से रिसोर्स `ThumbnailResource` या `Thumbnail4Resource` के इंस्टेंस हैं, क्योंकि ये ही EXIF डेटा रखते हैं।

## स्टेप 3: EXIF ​​डेटा एक्सट्रेक्ट करें
एक बार थंबनेल रिसोर्स पहचान लेने के बाद, हम EXIF डेटा निकालते हैं और उसे कंसोल पर प्रिंट करते हैं।

```java
if (image.getImageResources()[i] instanceof ThumbnailResource) {
    JpegExifData exif = ((ThumbnailResource) image.getImageResources()[i]).getJpegOptions().getExifData();
    if (exif != null) {
        System.out.println("Exif WhiteBalance: " + exif.getWhiteBalance());
        System.out.println("Exif PixelXDimension: " + exif.getPixelXDimension());
        System.out.println("Exif PixelYDimension: " + exif.getPixelYDimension());
        System.out.println("Exif ISOSpeed: " + exif.getISOSpeed());
        System.out.println("Exif FocalLength: " + exif.getFocalLength());
    }
}
```

हम `if` स्टेटमेंट से जाँचते हैं कि रिसोर्स `ThumbnailResource` का इंस्टेंस है या नहीं। यदि है, तो उसे कास्ट करके उसके `JpegOptions` से `ExifData` प्राप्त करते हैं। अंत में WhiteBalance, Pixel Dimensions, ISOSpeed, और FocalLength जैसे विभिन्न EXIF टैग प्रिंट करते हैं।

## आम दिक्कतें और टिप्स
- **Null EXIF ​​डेटा:** कुछ PSD फाइलों में थंबनेल रिसोर्स के साथ EXIF ​​जानकारी नहीं होती। टैग वैल्यूज़ एक्सेस करने से पहले हमेशा `null` चेक करें।

- **फ़ाइल पाथ एररयाँ:** एब्सोल्यूट पाथ का इस्तेमाल करें या यह पक्का करें कि वर्किंग डायरेक्टरी आपके PSD फ़ाइल वाले फ़ोल्डर की ओर इशारा कर रही है।

- **लाइसेंस रेस्ट्रिक्शन:** फ्री ट्रायल प्रोसेस किए जा चुकीं पेजों की संख्या लिमिटेड करता है; अनलिमिटेड इस्तेमाल के लिए पूरा लाइसेंस अपग्रेड करें।

## अक्सर पूछे जाने वाले सवाल
### EXIF ​​डेटा क्या है?

EXIF (एक्सचेंजेबल इमेज फ़ाइल फ़ॉर्मेट) डेटा वह मेटाडेटा है जो इमेज फाइलों में एम्बेड होता है, जिसमें कैमरा सेटिंग्स, डेट-टाइम, और इमेज डाइमेंशन जैसी जानकारी शामिल होती है।

### क्या मैं Aspose.PSD का इस्तेमाल करके EXIF ​​डेटा एडिट कर सकता हूँ?

हाँ, Aspose.PSD आपको EXIF ​​डेटा पढ़ने और प्रमाणीकरण करने दोनों की अनुमति देता है। आप टैग अपडेट कर सकते हैं और जेनरेट को इमेज फ़ाइल में सेव कर सकते हैं।

### क्या Aspose.PSD जावा के लिए मुफ़्त है?
Aspose.PSD एक मुफ़्त ट्रायल संस्करण प्रदान करता है जिसे आप [यहाँ](https://releases.aspose.com/) से डाउनलोड कर सकते हैं। पूर्ण फीचर्स के लिए आपको लाइसेंस खरीदना होगा।

### Aspose.PSD कौन से अन्य प्रारूपों का समर्थन करता है?
Aspose.PSD विभिन्न Adobe Photoshop फ़ॉर्मेट्स को सपोर्ट करता है, जैसे PSD, PSB, आदि। यह इन फ़ॉर्मेट्स को PNG, JPEG, TIFF आदि में कन्वर्ट करने के विकल्प भी देता है।

### मुझे Aspose.PSD के लिए समर्थन कैसे मिलता है?
आप Aspose.PSD के [फ़ॉर्म](https://forum.aspose.com/c/psd/34) के माध्यम से समर्थन प्राप्त कर सकते हैं।

### यह **java इमेज मेटाडेटा एक्सट्रैक्शन** में कैसे मदद करता है?

`JpegExifData` ऑब्जेक्ट का इस्तेमाल करके आप प्रोग्रामेटिक रूप से किसी भी ज़रूरी EXIF ​​टैग को निकाल सकते हैं, जिससे इमेज फ़ॉर्मेट्स में बड़े पैमाने पर मेटाडेटा एक्सट्रैक्शन टास्क के लिए एक ठोस आधार बनता है।

## निष्कर्ष
इन चरणों का पालन करके आपने Aspose.PSD (asp) का उपयोग करके PSD इमेज से **EXIF डेटा Java‑स्टाइल** में निकालना सीख लिया है। इस प्रक्रिया में इमेज लोड करना, उसके रिसोर्सेज़ पर इटररेट करना, थंबनेल रिसोर्स पहचानना, और आवश्यक EXIF टैग पढ़ना शामिल है। अब आप इस ज्ञान का उपयोग करके अपने जावा एप्लिकेशन्स में विस्तृत इमेज मेटाडेटा शामिल कर सकते हैं, जिससे फोटो‑मैनेजमेंट, एनालिटिक्स, या ऑटोमेटेड प्रोसेसिंग पाइपलाइन अधिक समृद्ध बनेंगे।

---

**Last Updated:** 2026-01-27  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}