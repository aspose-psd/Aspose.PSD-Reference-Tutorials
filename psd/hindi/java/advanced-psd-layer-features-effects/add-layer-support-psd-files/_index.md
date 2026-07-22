---
date: 2026-07-22
description: Aspose.PSD for Java का उपयोग करके PSD लेयर्स को निकालना और उन्हें PNG
  में बदलना सीखें। मजबूत ग्राफ़िक्स मैनिपुलेशन की आवश्यकता वाले डेवलपर्स के लिए आदर्श।
keywords:
- extract psd layers
- how to extract psd
- convert psd to png
lastmod: 2026-07-22
linktitle: Aspose.PSD Java का उपयोग करके PSD फ़ाइलों के लिए लेयर समर्थन जोड़ें और
  PSD लेयर्स निकालें
og_description: Aspose.PSD for Java के साथ PSD लेयर्स निकालें और उन्हें PNG में बदलें।
  लेयर निष्कर्षण और इमेज रूपांतरण को स्वचालित करने के लिए इस चरण‑दर‑चरण गाइड का पालन
  करें।
og_image_alt: Developer guide showing Java code to extract PSD layers and save as
  PNG using Aspose.PSD
og_title: Aspose.PSD Java का उपयोग करके PSD लेयर्स निकालें – PSD फ़ाइलों के लिए लेयर
  समर्थन जोड़ें
schemas:
- author: Aspose
  dateModified: '2026-07-22'
  description: Learn how to extract PSD layers and convert PSD layers to PNG using
    Aspose.PSD for Java. Ideal for developers needing robust graphics manipulation.
  headline: Extract PSD Layers and Add Layer Support for PSD Files using Aspose.PSD
    Java
  type: TechArticle
- description: Learn how to extract PSD layers and convert PSD layers to PNG using
    Aspose.PSD for Java. Ideal for developers needing robust graphics manipulation.
  name: Extract PSD Layers and Add Layer Support for PSD Files using Aspose.PSD Java
  steps:
  - name: '**Java Development Environment** – JDK installed. You can download it from
      the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Environment** – JDK installed. You can download it from
      the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java** – Grab the latest library from the official download
      page [here](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – Grab the latest library from the official download
      page [here](https://releases.aspose.com/psd/java/).'
  - name: '**Basic Java knowledge** – Familiarity with compiling and running Java
      programs.'
    text: '**Basic Java knowledge** – Familiarity with compiling and running Java
      programs.'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
  - name: '**A PSD file** – Use any PSD you have, or download a sample PSD for testing.'
    text: '**A PSD file** – Use any PSD you have, or download a sample PSD for testing.'
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a library that allows you to manipulate PSD files
      without having Photoshop installed.
    question: What is Aspose.PSD for Java?
  - answer: Yes! While primarily for PSD files, Aspose offers libraries for a wide
      range of formats, including AI, PDF, and SVG.
    question: Can I use Aspose.PSD for other file formats?
  - answer: Absolutely! You can download a free trial version [here](https://releases.aspose.com/).
    question: Is a trial version available?
  - answer: Access the Aspose forum for PSD‑related questions [here](https://forum.aspose.com/c/psd/34).
    question: Where can I get support if I run into problems?
  - answer: Iterate over `image.getLayers()`, create a new `Bitmap` for each layer,
      and save it with its own `PngOptions`. This yields individual PNG files per
      layer.
    question: Can I convert each layer to a separate PNG?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- extract psd
- Aspose.PSD
- Java image processing
title: Aspose.PSD Java का उपयोग करके PSD फ़ाइलों के लिए लेयर समर्थन जोड़ें और PSD
  लेयर्स निकालें
url: /hi/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD Java का उपयोग करके PSD फ़ाइलों के लिए लेयर समर्थन जोड़ें और PSD लेयर्स निकालें

## परिचय
Photoshop Document (PSD) फ़ाइलों के साथ काम करना ग्राफ़िक डिज़ाइनरों और डेवलपर्स दोनों के लिए रोज़मर्रा की वास्तविकता है, और **extract psd layers** अक्सर एसेट्स को पुनः उपयोग करने या इमेज पाइपलाइन को स्वचालित करने की पहली कदम होती है। इस ट्यूटोरियल में आप सीखेंगे कि कैसे एक PSD से व्यक्तिगत लेयर्स को निकाला जाए, पूर्ण लेयर समर्थन सक्षम किया जाए, और Aspose.PSD for Java का उपयोग करके **convert PSD layers to PNG** किया जाए। हम पर्यावरण सेटअप से लेकर सर्वोत्तम प्रैक्टिस टिप्स तक सब कुछ कवर करेंगे, ताकि आप इस वर्कफ़्लो को किसी भी Java एप्लिकेशन में मिनटों में एकीकृत कर सकें।

## त्वरित उत्तर
- **What does “extract PSD layers” mean?** इसका अर्थ है PSD फ़ाइल को लोड करना और प्रत्येक व्यक्तिगत लेयर तक पहुंच प्राप्त करना ताकि उसे संशोधित या निर्यात किया जा सके।  
- **Which library handles this in Java?** Aspose.PSD for Java पूर्ण‑विशेषताओं वाला PSD प्रोसेसिंग प्रदान करता है बिना Photoshop की आवश्यकता के।  
- **Can I convert PSD layers to PNG in one go?** हाँ—फ़ाइल को उचित विकल्पों के साथ लोड करके और PNG विकल्पों के साथ सहेजकर जो पारदर्शिता को बनाए रखते हैं।  
- **Do I need a license for production use?** उत्पादन के लिए एक वाणिज्यिक लाइसेंस आवश्यक है; मूल्यांकन के लिए एक मुफ्त ट्रायल उपलब्ध है।  
- **What Java version is required?** JDK 8 या उससे ऊपर (ट्यूटोरियल में उदाहरण के रूप में JDK 11 उपयोग किया गया है)।

## Aspose.PSD for Java का उपयोग करके PSD लेयर्स कैसे निकालें?
PSD को लोड करें, लेयर इफ़ेक्ट्स सक्षम करें, और केवल कुछ लाइनों के Java कोड में परिणाम को PNG के रूप में सहेजें। यह सीधा तरीका सर्वर पर Photoshop की आवश्यकता को समाप्त करता है और Java 8+ को सपोर्ट करने वाले किसी भी प्लेटफ़ॉर्म पर काम करता है। आप `PsdLoadOptions` ऑब्जेक्ट को `setLoadEffectsResource(true)` और `setUseDiskForLoadEffectsResource(true)` के साथ बनाते हैं, फिर `PsdImage.load(path, options)` से फ़ाइल लोड करते हैं। लोड करने के बाद, आप `image.save(outputPath, new PngOptions())` से लेयर्स को मर्ज कर सकते हैं या `image.getLayers()` के माध्यम से प्रत्येक लेयर को अलग‑अलग निर्यात कर सकते हैं, जिससे सभी इफ़ेक्ट्स बरकरार रहते हैं और मेमोरी उपयोग कम रहता है।

## PSD लेयर्स निकालने और उन्हें PNG में बदलने का कारण क्या है?
लेयर्स को निकालने से आप **एसेट्स को पुनः उपयोग** कर सकते हैं, **थंबनेल जेनरेशन को स्वचालित** कर सकते हैं, और वेब‑तैयार ग्राफ़िक्स के लिए **पारदर्शिता को संरक्षित** रख सकते हैं। Aspose.PSD **50+ इनपुट और आउटपुट फ़ॉर्मेट** का समर्थन करता है और डिस्क‑आधारित रिसोर्स हैंडलिंग के कारण कई‑सौ‑पृष्ठीय PSD फ़ाइलों को पूरी फ़ाइल को मेमोरी में लोड किए बिना प्रोसेस कर सकता है।

## पूर्वापेक्षाएँ
शुरू करने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1. **Java Development Environment** – JDK स्थापित है। आप इसे [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) से डाउनलोड कर सकते हैं।  
2. **Aspose.PSD for Java** – आधिकारिक डाउनलोड पेज से नवीनतम लाइब्रेरी प्राप्त करें [here](https://releases.aspose.com/psd/java/)।  
3. **Basic Java knowledge** – Java प्रोग्राम को संकलित और चलाने की मूलभूत समझ।  
4. **IDE** – IntelliJ IDEA, Eclipse, या कोई भी एडिटर जो आप पसंद करते हैं।  
5. **A PSD file** – कोई भी PSD फ़ाइल उपयोग करें, या परीक्षण के लिए एक सैंपल PSD डाउनलोड करें।

इन सभी को तैयार करने के बाद, आप PSD लेयर्स निकालने के लिए तैयार हैं।

## पैकेज आयात करें
`PsdImage`, `PsdLoadOptions`, और `PngOptions` क्लासेज़ इस वर्कफ़्लो के मुख्य घटक हैं।  

`PsdImage` Aspose.PSD का टॉप‑लेवल ऑब्जेक्ट है जो मेमोरी में एकल PSD फ़ाइल का प्रतिनिधित्व करता है।  

`PsdLoadOptions` आपको लेयर इफ़ेक्ट्स जैसी रिसोर्सेज़ को कैसे लोड किया जाए, इसे नियंत्रित करने की सुविधा देता है।  

`PngOptions` PNG फ़ाइल के आउटपुट फ़ॉर्मेट और पारदर्शिता हैंडलिंग को परिभाषित करता है।

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## चरण 1: अपनी डायरेक्टरीज़ निर्धारित करें
स्रोत PSD और आउटपुट PNG के पाथ सेट करें। `dataDir` को उस फ़ोल्डर की ओर इंगित करने के लिए समायोजित करें जहाँ आपकी फ़ाइलें स्थित हैं।

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "layers.psd";
String output = dataDir + "layers.png";
```

- `dataDir` – `"Your Document Directory"` को अपने वास्तविक फ़ोल्डर पाथ से बदलें।  
- `sourceFileName` – उस PSD का पूर्ण पाथ जिसे आप प्रोसेस करना चाहते हैं।  
- `output` – PNG का लक्ष्य पाथ जहाँ निकाली गई लेयर्स संग्रहीत होंगी।

## चरण 2: लोड विकल्प सेट करें
`PsdLoadOptions` को कॉन्फ़िगर करने से सभी लेयर इफ़ेक्ट्स और रिसोर्सेज़ सही ढंग से लोड होते हैं, जो **extract PSD layers** करने के लिए आवश्यक है।

```java
PsdLoadOptions imageLoadOptions = new PsdLoadOptions();
imageLoadOptions.setLoadEffectsResource(true);
imageLoadOptions.setUseDiskForLoadEffectsResource(true);
```

- `setLoadEffectsResource(true)` – लेयर्स से जुड़े अतिरिक्त इफ़ेक्ट्स (जैसे ड्रॉप शैडो) लोड करता है।  
- `setUseDiskForLoadEffectsResource(true)` – भारी रिसोर्सेज़ को डिस्क पर ऑफलोड करता है, जिससे मेमोरी पर दबाव कम होता है।

## चरण 3: PSD फ़ाइल लोड करें
अब हम ऊपर परिभाषित विकल्पों का उपयोग करके `PsdImage` ऑब्जेक्ट में PSD लोड करते हैं।

```java
PsdImage image = (PsdImage) Image.load(sourceFileName, imageLoadOptions);
```

इस बिंदु पर, `image` में सभी लेयर्स, मास्क, और इफ़ेक्ट्स मौजूद हैं, जो निकासी के लिए तैयार हैं।

## चरण 4: सेव विकल्प सेट करें
PNG को कैसे सहेजा जाएगा, इसे कॉन्फ़िगर करें। `TruecolorWithAlpha` का उपयोग करने से मूल लेयर्स की पारदर्शिता संरक्षित रहती है।

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

## चरण 5: इमेज सहेजें (PSD लेयर्स को PNG में बदलें)
लोड किए गए PSD (सभी लेयर्स सहित) को एकल PNG फ़ाइल में निर्यात करें। यह कदम प्रभावी रूप से **convert psd layers png** को एक ही ऑपरेशन में करता है।

```java
image.save(output, saveOptions);
```

यदि आपको प्रत्येक लेयर को अलग‑अलग PNG के रूप में चाहिए, तो आप `image.getLayers()` पर इटररेट कर सकते हैं—परंतु कई उपयोग‑केसों में मर्ज्ड PNG पर्याप्त होता है।

## चरण 6: समाप्त करें
एक मित्रवत कंसोल संदेश जोड़ें ताकि आप जान सकें कि प्रक्रिया सफल रही।

```java
System.out.println("PSD Layers have been successfully converted to PNG!");
```

## सामान्य समस्याएँ और सुझाव
- **Out‑of‑Memory Errors:** यदि आप बहुत बड़े PSD प्रोसेस कर रहे हैं, तो `setUseDiskForLoadEffectsResource(true)` को सक्षम रखें ताकि अस्थायी डेटा डिस्क पर ऑफलोड हो सके।  
- **Missing Effects:** सुनिश्चित करें कि `setLoadEffectsResource(true)` सेट है; अन्यथा कुछ लेयर इफ़ेक्ट्स अनदेखे रह सकते हैं।  
- **Path Problems:** प्लेटफ़ॉर्म‑स्वतंत्र पाथ हैंडलिंग के लिए `java.nio.file` से `Paths.get(...)` का उपयोग करें।

## अक्सर पूछे जाने वाले प्रश्न

**Q: What is Aspose.PSD for Java?**  
A: Aspose.PSD for Java एक लाइब्रेरी है जो आपको Photoshop स्थापित किए बिना PSD फ़ाइलों को मैनीपुलेट करने की सुविधा देती है।

**Q: Can I use Aspose.PSD for other file formats?**  
A: हाँ! मुख्यतः PSD फ़ाइलों के लिए जबकि Aspose विभिन्न फ़ॉर्मेट्स के लिए लाइब्रेरीज़ प्रदान करता है, जिसमें AI, PDF, और SVG शामिल हैं।

**Q: Is a trial version available?**  
A: बिल्कुल! आप एक मुफ्त ट्रायल संस्करण [here](https://releases.aspose.com/) से डाउनलोड कर सकते हैं।

**Q: Where can I get support if I run into problems?**  
A: PSD‑संबंधित प्रश्नों के लिए Aspose फ़ोरम [here](https://forum.aspose.com/c/psd/34) तक पहुँचें।

**Q: Can I convert each layer to a separate PNG?**  
A: `image.getLayers()` पर इटररेट करें, प्रत्येक लेयर के लिए नया `Bitmap` बनाएं, और अपने स्वयं के `PngOptions` के साथ सहेजें। इससे प्रत्येक लेयर के लिए अलग‑अलग PNG फ़ाइलें मिलेंगी।

## निष्कर्ष
आपने अब **extract PSD layers**, पूर्ण लेयर समर्थन सक्षम करना, और Aspose.PSD for Java का उपयोग करके **convert PSD layers to PNG** करना सीख लिया है। चाहे आप एक स्वचालित एसेट पाइपलाइन बना रहे हों या डेस्कटॉप एप्लिकेशन में ग्राफ़िक्स क्षमताएँ जोड़ रहे हों, यह दृष्टिकोण आपको Photoshop की आवश्यकता के बिना Photoshop फ़ाइलों पर सूक्ष्म नियंत्रण देता है। फ़िल्टर लागू करने, प्रोग्रामेटिक रूप से लेयर्स मर्ज करने, या प्रत्येक लेयर को अलग‑अलग निर्यात करने जैसे आगे के प्रयोगों के साथ इस वर्कफ़्लो का अन्वेषण करें।

---

**अंतिम अपडेट:** 2026-07-22  
**परीक्षण किया गया:** Aspose.PSD for Java 24.11 (लेखन के समय नवीनतम)  
**लेखक:** Aspose

## संबंधित ट्यूटोरियल

- [Export PSD to PNG & Add a New Regular Layer using Aspose.PSD for Java](/psd/java/advanced-image-effects/add-new-regular-layer/)
- [Export PSD to PNG with Layer Mask Support in Java](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [Convert PSD to Image in Java – Apply Adjustment Layers with Aspose.PSD](/psd/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}