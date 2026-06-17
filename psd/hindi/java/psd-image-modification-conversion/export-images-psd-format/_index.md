---
date: 2026-03-23
description: Aspose.PSD for Java का उपयोग करके इमेज को PSD के रूप में सहेजना सीखें।
  PSD कलर मोड सेट करने, बिटमैप को PSD में बदलने और प्रोग्रामेटिकली इमेज एक्सपोर्ट
  करने के लिए चरण‑दर‑चरण गाइड।
linktitle: Export Images to PSD Format with Java
second_title: Aspose.PSD Java API
title: जावा का उपयोग करके Aspose.PSD के साथ इमेज को PSD के रूप में कैसे सहेजें
url: /hi/java/psd-image-modification-conversion/export-images-psd-format/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# जावा का उपयोग करके Aspose.PSD के साथ इमेज को PSD के रूप में कैसे सहेजें

## जावा के साथ इमेज को PSD के रूप में कैसे सहेजें

इस ट्यूटोरियल में, आप जावा और Aspose.PSD लाइब्रेरी का उपयोग करके **how to save image as PSD** सीखेंगे। लेयर्ड Photoshop फ़ाइलों के साथ काम करना कई ग्राफिक‑डिज़ाइन डेवलपर्स के लिए रोज़मर्रा का काम है, और PSD फ़ाइलों के निर्माण को स्वचालित करने से वर्कफ़्लो बहुत तेज़ हो सकता है। हम PSD कलर मोड सेट करने, एक bitmap बनाने, और उस bitmap को PSD फ़ाइल में बदलने की प्रक्रिया को देखेंगे—शुरू करने के लिए आपको जो कुछ भी चाहिए। चलिए शुरू करते हैं!

## त्वरित उत्तर
- **कौन सी लाइब्रेरी चाहिए?** Aspose.PSD for Java (downloadable from the official site).  
- **क्या मैं कलर मोड सेट कर सकता हूँ?** Yes – use `PsdOptions.setColorMode()` to choose RGB, CMYK, etc.  
- **क्या bitmap को PSD में बदलना समर्थित है?** Absolutely; create a `PsdImage` from dimensions or an existing bitmap and save it.  
- **क्या उत्पादन के लिए लाइसेंस चाहिए?** A commercial license is required for non‑trial use.  
- **कौन सा Java संस्करण आवश्यक है?** Java 8 or higher.

## “save image as PSD” क्या है?

इमेज को PSD के रूप में सहेजना मतलब रास्टर ग्राफिक को Adobe Photoshop के मूल लेयर्ड फ़ॉर्मेट में एक्सपोर्ट करना है। इससे डाउनस्ट्रीम टूल्स (Photoshop, GIMP, आदि) लेयर्स, चैनल्स और एडिटेबिलिटी को बनाए रख सकते हैं। Aspose.PSD के साथ आप प्रोग्रामेटिक रूप से PSD फ़ाइलें बना सकते हैं बिना Photoshop खोले।

## जावा के लिए Aspose.PSD क्यों उपयोग करें?

- **पूर्ण नियंत्रण** रंग मोड, संपीड़न, और Photoshop संस्करण संगतता पर।  
- **कोई बाहरी निर्भरताएँ नहीं** – शुद्ध Java, सर्वर‑साइड रेंडरिंग के लिए आदर्श।  
- **उच्च प्रदर्शन** – हजारों इमेजों की बैच प्रोसेसिंग के लिए उपयुक्त।  

## आवश्यकताएँ

शुरू करने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1. **बेसिक Java ज्ञान** – आपको Java प्रोग्राम को कंपाइल और रन करने में सहज होना चाहिए।  
2. **Aspose.PSD for Java लाइब्रेरी** – आप इसे [यहाँ डाउनलोड कर सकते हैं](https://releases.aspose.com/psd/java/).  
3. **Java Development Kit (JDK)** – आपके मशीन पर JDK 8 या नया स्थापित होना चाहिए।  
4. **IDE या टेक्स्ट एडिटर** – IntelliJ IDEA, Eclipse, VS Code, या कोई भी एडिटर जो आपको पसंद हो।  
5. **इमेज अवधारणाओं की समझ** – रंग मोड, संपीड़न, और bitmap की बुनियादी जानकारी मददगार है लेकिन अनिवार्य नहीं।

सब कुछ तैयार है? बढ़िया, अब आगे बढ़ते हैं।

## पैकेज इम्पोर्ट करें

पहले, Aspose.PSD लाइब्रेरी से आवश्यक क्लासेस को इम्पोर्ट करें:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
```

ये इम्पोर्ट्स हमें ड्रॉइंग यूटिलिटीज़, कलर हैंडलिंग, और PSD‑स्पेसिफिक ऑप्शन्स तक पहुँच देते हैं।

## चरण 1: अपने डॉक्यूमेंट डायरेक्टरी को इनिशियलाइज़ करें

निर्धारित करें कि जेनरेट की गई PSD फ़ाइल कहाँ सेव होगी:

```java
String dataDir = "Your Document Directory";
```

`"Your Document Directory"` को एक एब्सोल्यूट पाथ जैसे `"C:/Images/"` या आपके प्रोजेक्ट के अंदर एक रिलेटिव पाथ से बदलें।

## चरण 2: नई इमेज बनाएं (Bitmap को PSD में बदलें)

अब हम एक खाली bitmap बनाते हैं जिसे बाद में **convert bitmap to PSD** करके PSD ऑप्शन्स के साथ सेव करेंगे:

```java
PsdImage bmpImage = new PsdImage(300, 300);
```

ज़रूरत के अनुसार `300, 300` को अपने इच्छित डाइमेंशन में बदल सकते हैं।

## चरण 3: इमेज डेटा भरें

bitmap में कुछ ग्राफिक्स जोड़ें ताकि परिणामी PSD सिर्फ एक खाली कैनवास न रहे:

```java
Graphics graphics = new Graphics(bmpImage);
graphics.clear(Color.getWhite());
Pen pen = new Pen(Color.getBrown());
graphics.drawRectangle(pen, bmpImage.getBounds());
```

- `graphics.clear(Color.getWhite())` पूरे कैनवास को सफ़ेद रंग से भरता है।  
- भूरा पेन एक आयत बनाता है जो इमेज की सीमाओं को दर्शाता है।

## चरण 4: PSD ऑप्शन्स सेट करें (Set PSD Color Mode)

यहाँ हम फ़ाइल को कैसे सेव किया जाएगा, इसे कॉन्फ़िगर करते हैं। यही वह जगह है जहाँ हम **set PSD color mode** को RGB पर सेट करते हैं, संपीड़न चुनते हैं, और Photoshop संस्करण निर्दिष्ट करते हैं:

```java
PsdOptions psdOptions = new PsdOptions();
psdOptions.setColorMode(ColorModes.Rgb);
psdOptions.setCompressionMethod(CompressionMethod.Raw);
psdOptions.setVersion(4);
```

- `ColorModes.Rgb` – वेब और स्क्रीन ग्राफिक्स के लिए सबसे सामान्य।  
- `CompressionMethod.Raw` – अधिकतम गुणवत्ता के लिए बिना संपीड़न के पिक्सेल डेटा संग्रहीत करता है।  
- `setVersion(4)` – फ़ाइल को Photoshop 4.0 फ़ॉर्मेट में सहेजता है, जो व्यापक रूप से संगत है।

## चरण 5: इमेज को सेव करें

अंत में, bitmap को PSD फ़ाइल के रूप में एक्सपोर्ट करें—यह मुख्य **save image as PSD** ऑपरेशन है:

```java
bmpImage.save(dataDir + "ExportImageToPSD_output.psd", psdOptions);
```

फ़ाइल `ExportImageToPSD_output.psd` आपके द्वारा निर्दिष्ट डायरेक्टरी में दिखाई देगी।

## सामान्य उपयोग केस

- **स्वचालित रिपोर्ट जनरेशन** जहाँ चार्ट्स को Photoshop में संपादन योग्य होना चाहिए।  
- **बैच रूपांतरण** PNG/JPEG एसेट्स को PSD में बदलना उन डिज़ाइनरों के लिए जिन्हें लेयर्स चाहिए।  
- **सर्वर‑साइड इमेज कंपोज़िशन** वेब सेवाओं के लिए जो क्लाइंट्स को PSD टेम्प्लेट प्रदान करती हैं।

## सामान्य समस्याएँ और समाधान

| समस्या | समाधान |
|-------|----------|
| **File not found** त्रुटि जब सेव कर रहे हों | Verify that `dataDir` ends with a path separator (`/` or `\\`) and that the folder exists. |
| **Blank image** सेव करने के बाद | Ensure you called `graphics.clear()` and drew something before saving. |
| **असमर्थित कलर मोड** | Use `ColorModes.Cmyk` if you need CMYK output; remember to adjust your graphics accordingly. |
| **LicenseException** रनटाइम पर | Install a valid Aspose.PSD license or run in trial mode (evaluation watermark may appear). |

## अक्सर पूछे जाने वाले प्रश्न

**Q: Aspose.PSD for Java क्या है?**  
A: Aspose.PSD for Java एक मजबूत API है जो डेवलपर्स को Adobe Photoshop का उपयोग किए बिना Photoshop PSD फ़ाइलें बनाने, संपादित करने, कनवर्ट करने और रेंडर करने की सुविधा देता है।

**Q: क्या मैं मौजूदा PSD फ़ाइल को संशोधित कर सकता हूँ?**  
A: हाँ, आप `new PsdImage("input.psd")` से मौजूदा PSD खोल सकते हैं, बदलाव कर सकते हैं, और फिर उसे वापस सेव कर सकते हैं।

**Q: क्या कोई फ्री ट्रायल उपलब्ध है?**  
A: बिल्कुल! आप Aspose.PSD का फ्री ट्रायल [यहाँ](https://releases.aspose.com/) से डाउनलोड कर सकते हैं।

**Q: अधिक दस्तावेज़ीकरण कहाँ मिल सकता है?**  
A: आप विस्तृत [डॉक्यूमेंटेशन](https://reference.aspose.com/psd/java/) देख सकते हैं ताकि Aspose.PSD के उपयोग के बारे में और जानकारी प्राप्त कर सकें।

**Q: अगर समस्याएँ आएँ तो सपोर्ट कैसे प्राप्त करूँ?**  
A: सपोर्ट के लिए आप [Aspose फ़ोरम](https://forum.aspose.com/c/psd/34) पर जा सकते हैं।

## निष्कर्ष

अब आप जानते हैं कि जावा के साथ **save image as PSD** कैसे किया जाता है, **set PSD color mode** कैसे सेट किया जाता है, और Aspose.PSD का उपयोग करके **convert bitmap to PSD** कैसे किया जाता है। यह तरीका आपको Photoshop फ़ाइलों पर पूर्ण प्रोग्रामेटिक नियंत्रण देता है, जिससे स्वचालित डिज़ाइन पाइपलाइन, डायनामिक इमेज जनरेशन, और मौजूदा Java एप्लिकेशन्स के साथ सहज इंटीग्रेशन संभव होता है। विभिन्न कलर मोड, साइज, और ड्रॉइंग ऑपरेशन्स के साथ प्रयोग करें ताकि PSD फ़ाइलें आपकी ठीक‑ठीक जरूरतों को पूरा करें।

---

**Last Updated:** 2026-03-23  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}