---
date: 2026-03-18
description: Aspose.PSD for Java के साथ PSD को PNG में बदलते हुए PNG बिट डेप्थ बदलना
  सीखें – कोड नमूनों के साथ चरण‑दर‑चरण गाइड।
linktitle: Specify PNG Bit Depth in Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Aspose.PSD for Java का उपयोग करके निर्दिष्ट बिट डेप्थ के साथ PSD को PNG में
  कैसे बदलें
url: /hi/java/optimizing-png-files/specify-png-bit-depth/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java का उपयोग करके निर्दिष्ट बिट डेप्थ के साथ PSD को PNG में बदलें

## Introduction
यदि आपको **convert psd to png** करना है और सटीक PNG बिट डेप्थ को नियंत्रित करना है, तो आप सही जगह पर हैं। इस ट्यूटोरियल में हम बताएँगे कि Aspose.PSD for Java के साथ PSD फ़ाइल को PNG इमेज के रूप में सहेजते समय png बिट डेप्थ कैसे बदलें। चाहे आप बैच‑प्रोसेसिंग टूल, वेब सर्विस, या डेस्कटॉप यूटिलिटी बना रहे हों, **save png with options** जैसे ग्रेस्केल कलर टाइप और कस्टम बिट डेप्थ को सेट करने से आपको इमेज क्वालिटी और फ़ाइल साइज पर सूक्ष्म नियंत्रण मिलता है।

## Quick Answers
- **क्या मैं PNG बिट डेप्थ बदल सकता हूँ?** हाँ – `PngOptions.setBitDepth()` का उपयोग करके 1, 2, 4, 8, या 16 बिट्स निर्दिष्ट करें।  
- **कौन से कलर टाइप समर्थित हैं?** Grayscale, TrueColor, Indexed, और अन्य `PngColorType` के माध्यम से।  
- **क्या मुझे Aspose.PSD के लिए लाइसेंस चाहिए?** विकास के लिए एक फ्री ट्रायल काम करता है; प्रोडक्शन के लिए एक कमर्शियल लाइसेंस आवश्यक है।  
- **कौन सा Java संस्करण आवश्यक है?** Java 8+ (लाइब्रेरी नए JDKs के साथ संगत है)।  
- **क्या कोड जैसा है वैसा ही चलाया जा सकता है?** हाँ – केवल प्लेसहोल्डर पाथ को अपने फ़ोल्डर से बदलें।

## What is “convert psd to png” with custom bit depth?
Photoshop PSD फ़ाइल को PNG इमेज में बदलना एक सामान्य कार्य है जब आपको वेब‑फ्रेंडली फ़ॉर्मेट चाहिए। बिट डेप्थ सेट करके **adjust png quality** करने की क्षमता जोड़ने से आप विज़ुअल फ़िडेलिटी और फ़ाइल साइज के बीच संतुलन बना सकते हैं, जो थंबनेल, आइकन, या सीमित बैंडविड्थ के मामलों में विशेष रूप से उपयोगी है।

## Why use Aspose.PSD for Java?
Aspose.PSD for Java एक हाई‑लेवल API प्रदान करता है जो PSD फ़ॉर्मेट की जटिलता को एब्स्ट्रैक्ट करता है। यह आपको **create grayscale png**, **save png with options**, और लो‑लेवल बाइट मैनिपुलेशन के बिना कलर प्रोफ़ाइल संभालने की सुविधा देता है। लाइब्रेरी पूरी तरह मैनेज्ड, क्रॉस‑प्लेटफ़ॉर्म है, और नियमित अपडेट प्राप्त करती है।

## Prerequisites
कोड में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1. **Java Development Kit (JDK)** – इसे [Oracle’s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) से डाउनलोड करें।  
2. **Aspose.PSD for Java** – नवीनतम JAR [this link](https://releases.aspose.com/psd/java/) से प्राप्त करें।  
3. **Basic Java knowledge** – आपको क्लासेज़, मेथड्स, और एक्सेप्शन हैंडलिंग में सहज होना चाहिए।  
4. **An IDE** जैसे IntelliJ IDEA या Eclipse (वैकल्पिक लेकिन अनुशंसित)।  
5. **A sample PSD file** – इसे उस फ़ोल्डर में रखें जिसका आप कोड में संदर्भ लेंगे।

सब कुछ तैयार है? बढ़िया – चलिए आवश्यक पैकेज इम्पोर्ट करते हैं।

## Import Packages
अब जब हमारे प्री‑रिक्विज़िट्स तैयार हैं, तो अपने जावा एप्लिकेशन में संबंधित पैकेज इम्पोर्ट करके अपना वातावरण सेटअप करने का समय है। अपना कोडिंग एनवायरनमेंट शुरू करें और अपने जावा फ़ाइल के शीर्ष पर निम्नलिखित इम्पोर्ट स्टेटमेंट्स जोड़ें:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

ये स्टेटमेंट्स उन क्लासेज़ को इम्पोर्ट करते हैं जिन्हें हम ट्यूटोरियल में पूरे समय उपयोग करेंगे, जिससे हम PSD फ़ाइलें लोड कर सकेंगे और निर्दिष्ट बिट डेप्थ के साथ उन्हें PNG इमेज के रूप में सहेज सकेंगे।

## Step 1: Set Up Your Document Directory
इमेज प्रोसेसिंग में कूदने से पहले, चलिए एक डायरेक्टरी परिभाषित करते हैं जहाँ हमारी इमेजेज़ संग्रहीत होंगी। यह एक क्राफ्ट प्रोजेक्ट शुरू करने से पहले आपके आर्ट सप्लाईज़ के लिए फ़ोल्डर बनाने जैसा है।

```java
String dataDir = "Your Document Directory";
```

## Step 2: Load the PSD Image
अगला कदम, हमें वह PSD इमेज फ़ाइल लोड करनी है जिसे आप बदलना चाहते हैं। इसे उस कैनवास को खोलने जैसा समझें जहाँ आप अपना सारा काम करेंगे।

```java
PsdImage psdImage = (PsdImage)Image.load(dataDir + "sample.psd");
```

यहाँ, हम `Image.load()` मेथड का उपयोग करके अपने सैंपल PSD फ़ाइल को पढ़ रहे हैं और उसे `PsdImage` में कास्ट कर रहे हैं ताकि PSD‑विशिष्ट प्रॉपर्टीज़ तक पहुँच सकें।

## Step 3: Create PNG Options
एक बार हमारा कैनवास खुल जाने पर, हमें इमेज को कैसे सहेजना है, इसके लिए विकल्पों का एक सेट चाहिए। यह मूल रूप से पेंटिंग शुरू करने से पहले आपके रंग और ब्रश स्टाइल चुनने जैसा है।

```java
PngOptions options = new PngOptions();
```

इस चरण में, हम `PngOptions` का एक इंस्टेंस इनिशियलाइज़ कर रहे हैं, जो हमें हमारे PNG आउटपुट के पैरामीटर्स निर्दिष्ट करने की अनुमति देता है।

## Step 4: Set the Desired Color Type
अब हम तय करते हैं कि अंतिम PNG इमेज में किस प्रकार के रंग चाहिए। क्या आप रंगीन पैलेट चाहते हैं या मोनोक्रोमैटिक स्टाइल? चलिए यह निर्णय लेते हैं!

```java
options.setColorType(PngColorType.Grayscale);
```

इस उदाहरण में, हमने कलर टाइप को ग्रेस्केल सेट किया है। यदि आप फुल‑कलर इमेज चाहते हैं तो आप `PngColorType.TrueColor` भी चुन सकते हैं। यही वह भाग है जहाँ हम **create grayscale png** करते हैं।

## Step 5: Specify the Bit Depth
अब, चलिए बिट डेप्थ निर्दिष्ट करते हैं। यह आपके प्रिंटर को बताने जैसा है कि उसे आपकी इमेज कितनी बारीकी से प्रिंट करनी चाहिए – जितने अधिक बिट्स, उतनी अधिक डिटेल!

```java
options.setBitDepth((byte)1);
```

यहाँ, हमने बिट डेप्थ **1 bit** सेट किया है, जो साधारण ग्रेस्केल इमेज के लिए उपयुक्त है। आप अपनी क्वालिटी आवश्यकताओं के अनुसार इसे 2, 4, 8, या 16 में बदल सकते हैं – यह **change png bit depth** करने का एक क्लासिक उदाहरण है।

## Step 6: Save the PNG Image
अंत में, अब अपनी कृति को सहेजने का समय है! यह चरण हमारे प्रोजेक्ट को समाप्त करता है क्योंकि हम प्रभावी रूप से अपने कार्य को एडिटिंग कैनवास से गैलरी दीवार पर ट्रांसफ़र करते हैं।

```java
psdImage.save(dataDir + "SpecifyBitDepth_out.png", options);
```

`PsdImage` की `save()` मेथड का उपयोग करके, हम परिवर्तित फ़ाइल को सहेजते हैं, जिसमें हमने परिभाषित विकल्प लागू होते हैं। वॉयला! हमारी इमेज अब कस्टम बिट डेप्थ के साथ सहेजी गई है।

## Common Issues and Solutions
- **`NullPointerException` जब PSD लोड हो रहा हो** – सुनिश्चित करें कि `dataDir` सही फ़ोल्डर की ओर इशारा कर रहा है और `sample.psd` मौजूद है।  
- **Unsupported bit depth** – Aspose.PSD PNG के लिए 1, 2, 4, 8, और 16 बिट्स को सपोर्ट करता है। किसी अन्य मान का उपयोग करने पर `IllegalArgumentException` फेंका जाएगा।  
- **Color type mismatch** – यदि आप ऐसा बिट डेप्थ सेट करते हैं जो चुने गए `PngColorType` के साथ संगत नहीं है, तो लाइब्रेरी स्वचालित रूप से निकटतम समर्थित सेटिंग पर समायोजित हो जाएगी।

## Frequently Asked Questions

**Q: Aspose.PSD for Java क्या है?**  
A: Aspose.PSD for Java जावा एप्लिकेशन्स में PSD फ़ाइलों के साथ काम करने के लिए एक लाइब्रेरी है, जिससे आप इमेजेज़ को मैनिपुलेट और कनवर्ट कर सकते हैं।

**Q: मैं विभिन्न बिट डेप्थ कैसे निर्दिष्ट करूँ?**  
A: आप `options.setBitDepth((byte)n)` मेथड का उपयोग करके बिट डेप्थ सेट कर सकते हैं, जहाँ `n` को अपनी इच्छित डेप्थ से बदलें।

**Q: क्या मैं Aspose.PSD को मुफ्त में उपयोग कर सकता हूँ?**  
A: हाँ, आप लाइब्रेरी को एक फ्री ट्रायल के साथ आज़मा सकते हैं, जिसे आप [here](https://releases.aspose.com/) पर पा सकते हैं।

**Q: मैं Aspose के लिए सपोर्ट लाइसेंस कहाँ प्राप्त कर सकता हूँ?**  
A: एक टेम्पररी लाइसेंस के लिए, आप [here](https://purchase.aspose.com/temporary-license/) पर आवेदन कर सकते हैं।

**Q: मैं किस प्रकार की इमेजेज़ को कनवर्ट कर सकता हूँ?**  
A: Aspose.PSD मुख्यतः PSD फ़ाइलों के साथ काम करता है, लेकिन यह PNG, JPEG, और TIFF जैसे विभिन्न फ़ॉर्मेट में कनवर्ज़न को सपोर्ट करता है।

## Conclusion
अब आपने सीखा है कि Aspose.PSD for Java का उपयोग करके **convert psd to png** कैसे करें और PNG बिट डेप्थ को नियंत्रित करें। `PngOptions` को समायोजित करके आप **adjust png quality**, **grayscale png** बना सकते हैं, और किसी भी परिदृश्य के लिए फ़ाइल साइज को फाइन‑ट्यून कर सकते हैं। विभिन्न कलर टाइप्स और बिट डेप्थ के साथ प्रयोग करें ताकि आपके एप्लिकेशन के लिए परफेक्ट बैलेंस मिल सके।

---

**अंतिम अपडेट:** 2026-03-18  
**परीक्षण किया गया:** Aspose.PSD for Java 24.11 (लेखन के समय नवीनतम)  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}