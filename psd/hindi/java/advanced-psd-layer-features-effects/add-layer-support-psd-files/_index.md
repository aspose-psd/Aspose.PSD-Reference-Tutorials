---
date: 2025-12-10
description: Aspose.PSD for Java का उपयोग करके PSD लेयर्स को निकालना और उन्हें PNG
  में बदलना सीखें। यह उन डेवलपर्स के लिए आदर्श है जिन्हें मजबूत ग्राफ़िक्स मैनिपुलेशन
  की आवश्यकता है।
linktitle: Extract PSD Layers and Add Layer Support for PSD Files using Aspose.PSD
  Java
second_title: Aspose.PSD Java API
title: Aspose.PSD जावा का उपयोग करके PSD लेयर्स निकालें और PSD फ़ाइलों के लिए लेयर
  समर्थन जोड़ें
url: /hi/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD Java का उपयोग करके PSD लेयर्स निकालें और PSD फ़ाइलों के लिए लेयर सपोर्ट जोड़ें

## परिचय
Photoshop Document (PSD) फ़ाइलों के साथ काम करना ग्राफ़िक डिज़ाइनरों और डेवलपर्स दोनों के लिए रोज़मर्रा की वास्तविकता है। सबसे सामान्य कार्यों में से एक **PSD लेयर्स निकालना** है ताकि उन्हें संपादित, पुन: उपयोग या PNG जैसे अन्य फ़ॉर्मेट में परिवर्तित किया जा सके। Java एप्लिकेशनों में, Aspose.PSD इस प्रक्रिया को सरल और कोड‑फ़्रेंडली बनाता है। इस ट्यूटोरियल में हम उन सटीक चरणों को देखेंगे जो PSD लेयर्स निकालने, लेयर सपोर्ट सक्षम करने, और **PSD लेयर्स को PNG में बदलने** के लिए आवश्यक हैं—सभी स्पष्ट व्याख्याओं और व्यावहारिक टिप्स के साथ।

## त्वरित उत्तर
- **“extract PSD layers” का क्या अर्थ है?** इसका मतलब है PSD फ़ाइल को लोड करना और प्रत्येक व्यक्तिगत लेयर तक पहुँच प्राप्त करना ताकि उसे संशोधित या निर्यात किया जा सके।  
- **Java में यह कौन सी लाइब्रेरी संभालती है?** Aspose.PSD for Java पूरी‑फ़ीचर PSD प्रोसेसिंग प्रदान करता है बिना Photoshop की आवश्यकता के।  
- **क्या मैं एक ही बार में PSD लेयर्स को PNG में बदल सकता हूँ?** हाँ—फ़ाइल को उचित विकल्पों के साथ लोड करके और PNG विकल्पों के साथ सहेजकर जो ट्रांसपैरेंसी को बनाए रखते हैं।  
- **क्या उत्पादन उपयोग के लिए लाइसेंस चाहिए?** उत्पादन के लिए एक वाणिज्यिक लाइसेंस आवश्यक है; मूल्यांकन के लिए एक मुफ्त ट्रायल उपलब्ध है।  
- **कौन सा Java संस्करण आवश्यक है?** JDK 8 या उससे ऊपर (ट्यूटोरियल में उदाहरण के रूप में JDK 11 का उपयोग किया गया है)।

## “extract PSD layers” क्या है?
PSD लेयर्स निकालना का अर्थ है PSD फ़ाइल की आंतरिक संरचना को पढ़ना और प्रत्येक लेयर को एक स्वतंत्र इमेज ऑब्जेक्ट के रूप में प्राप्त करना। यह आपको लेयर्स को व्यक्तिगत रूप से संपादित, छिपाने, पुनः क्रमित करने या निर्यात करने की सुविधा देता है—बिल्कुल वही जो डिज़ाइनर Photoshop में करते हैं, लेकिन प्रोग्रामेटिक रूप से।

## क्यों PSD लेयर्स निकालें और उन्हें PNG में बदलें?
- **संपत्तियों का पुन: उपयोग:** मैन्युअल निर्यात के बिना मास्टर PSD से आइकन, बटन या UI तत्व निकालें।  
- **ऑटोमेशन:** थंबनेल या वेब‑तैयार इमेजेज तुरंत उत्पन्न करें।  
- **ट्रांसपैरेंसी बनाए रखें:** PNG अल्फा चैनल को बनाए रखता है, जिससे यह वेब ग्राफिक्स के लिए उपयुक्त बनता है।

## पूर्वापेक्षाएँ
शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1. **Java Development Environment** – JDK स्थापित है। आप इसे [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) से डाउनलोड कर सकते हैं।  
2. **Aspose.PSD for Java** – आधिकारिक डाउनलोड पेज से नवीनतम लाइब्रेरी प्राप्त करें [here](https://releases.aspose.com/psd/java/).  
3. **Basic Java knowledge** – Java प्रोग्राम को संकलित और चलाने की परिचितता।  
4. **IDE** – IntelliJ IDEA, Eclipse, या कोई भी एडिटर जो आप पसंद करते हैं।  
5. **A PSD file** – आपके पास कोई भी PSD उपयोग करें, या परीक्षण के लिए एक सैंपल PSD डाउनलोड करें।  

इन सबको तैयार करने के बाद, आप PSD लेयर्स निकालना शुरू करने के लिए तैयार हैं।

## पैकेज इम्पोर्ट करें
सबसे पहले, Aspose.PSD लाइब्रेरी से उन क्लासेज़ को इम्पोर्ट करें जिनकी हमें आवश्यकता होगी।

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
```

## चरण 1: अपने डायरेक्टरीज़ निर्धारित करें
सोर्स PSD और आउटपुट PNG के पाथ सेट करें। `dataDir` को उस फ़ोल्डर की ओर इंगित करने के लिए समायोजित करें जहाँ आपकी फ़ाइलें स्थित हैं।

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "layers.psd";
String output = dataDir + "layers.png";
```

- `dataDir` – `"Your Document Directory"` को अपने वास्तविक फ़ोल्डर पाथ से बदलें।  
- `sourceFileName` – उस PSD का पूर्ण पाथ जिसे आप प्रोसेस करना चाहते हैं।  
- `output` – निकाली गई लेयर्स वाले PNG का गंतव्य पाथ।

## चरण 2: लोड विकल्प सेट करें
`PsdLoadOptions` को कॉन्फ़िगर करने से सभी लेयर इफ़ेक्ट्स और रिसोर्सेज़ सही ढंग से लोड होते हैं, जो **PSD लेयर्स निकालते** समय आवश्यक है।

```java
PsdLoadOptions imageLoadOptions = new PsdLoadOptions();
imageLoadOptions.setLoadEffectsResource(true);
imageLoadOptions.setUseDiskForLoadEffectsResource(true);
```

- `setLoadEffectsResource(true)` – लेयर्स से जुड़े अतिरिक्त इफ़ेक्ट्स (जैसे ड्रॉप शैडो) लोड करता है।  
- `setUseDiskForLoadEffectsResource(true)` – भारी रिसोर्सेज़ को डिस्क पर ऑफलोड करता है, जिससे मेमोरी पर दबाव कम होता है।

## चरण 3: PSD फ़ाइल लोड करें
अब हम ऊपर परिभाषित विकल्पों का उपयोग करके PSD को `PsdImage` ऑब्जेक्ट में लोड करते हैं।

```java
PsdImage image = (PsdImage) Image.load(sourceFileName, imageLoadOptions);
```

इस चरण पर, `image` में सभी लेयर्स, मास्क और इफ़ेक्ट्स होते हैं, जो निकासी के लिए तैयार हैं।

## चरण 4: सेव विकल्प सेट करें
PNG को कैसे सेव किया जाएगा, इसे कॉन्फ़िगर करें। `TruecolorWithAlpha` का उपयोग करने से मूल लेयर्स की ट्रांसपैरेंसी बनी रहती है।

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
```

## चरण 5: इमेज सेव करें (PSD लेयर्स को PNG में बदलें)
लोड किए गए PSD (सभी लेयर्स के साथ) को एक सिंगल PNG फ़ाइल में एक्सपोर्ट करें। यह चरण प्रभावी रूप से एक ही ऑपरेशन में **psd लेयर्स को png में बदलता** है।

```java
image.save(output, saveOptions);
```

यदि आपको प्रत्येक लेयर को अलग PNG के रूप में चाहिए, तो आप `image.getLayers()` पर इटरेट कर सकते हैं—परन्तु कई उपयोग मामलों में एक मर्ज्ड PNG पर्याप्त है।

## चरण 6: समाप्त करें
एक दोस्ताना कंसोल संदेश जोड़ें ताकि आप जान सकें कि प्रक्रिया सफल रही।

```java
System.out.println("PSD Layers have been successfully converted to PNG!");
```

## सामान्य समस्याएँ और टिप्स
- **Out‑of‑Memory Errors:** यदि आप बहुत बड़े PSD प्रोसेस कर रहे हैं, तो `setUseDiskForLoadEffectsResource(true)` को सक्षम रखें ताकि टेम्पररी डेटा डिस्क पर ऑफलोड हो सके।  
- **Missing Effects:** सुनिश्चित करें कि `setLoadEffectsResource(true)` सेट है; अन्यथा कुछ लेयर इफ़ेक्ट्स अनदेखे रह सकते हैं।  
- **Path Problems:** प्लेटफ़ॉर्म‑इंडिपेंडेंट पाथ हैंडलिंग के लिए `java.nio.file` से `Paths.get(...)` का उपयोग करें।

## अक्सर पूछे जाने वाले प्रश्न

**Q: Aspose.PSD for Java क्या है?**  
A: Aspose.PSD for Java एक लाइब्रेरी है जो आपको Photoshop स्थापित किए बिना PSD फ़ाइलों को मैनीपुलेट करने की अनुमति देती है।

**Q: क्या मैं Aspose.PSD को अन्य फ़ाइल फ़ॉर्मेट्स के लिए उपयोग कर सकता हूँ?**  
A: हाँ! जबकि मुख्य रूप से PSD फ़ाइलों के लिए है, Aspose विभिन्न अन्य फ़ॉर्मेट्स के लिए भी लाइब्रेरीज़ प्रदान करता है।

**Q: क्या कोई ट्रायल संस्करण उपलब्ध है?**  
A: बिल्कुल! आप एक मुफ्त ट्रायल संस्करण [here](https://releases.aspose.com/) से डाउनलोड कर सकते हैं।

**Q: यदि मुझे मदद चाहिए तो मैं समर्थन कहाँ प्राप्त कर सकता हूँ?**  
A: आप Aspose फ़ोरम में समर्थन प्राप्त कर सकते हैं [here](https://forum.aspose.com/c/psd/34)।

**Q: क्या मैं PNG को वापस PSD में बदल सकता हूँ?**  
A: Aspose.PSD लाइब्रेरी अधिकतर PSD फ़ाइलों को पढ़ने और मैनीपुलेट करने पर केंद्रित है, न कि अन्य फ़ॉर्मेट्स को वापस PSD में बदलने पर।

**Q: मैं प्रत्येक लेयर को अलग PNG के रूप में कैसे निकालूँ?**  
A: `image.getLayers()` पर इटरेट करें, प्रत्येक लेयर के लिए नया `Bitmap` बनाएं, और इसे अपने `PngOptions` के साथ सेव करें। इससे आपको प्रत्येक लेयर के लिए अलग PNG फ़ाइलें मिलेंगी।

## निष्कर्ष
अब आपने सीख लिया है कि **PSD लेयर्स निकालें**, पूर्ण लेयर सपोर्ट सक्षम करें, और Aspose.PSD for Java का उपयोग करके **PSD लेयर्स को PNG में बदलें**। चाहे आप एक ऑटोमेटेड एसेट पाइपलाइन बना रहे हों या डेस्कटॉप एप्लिकेशन में ग्राफ़िक्स क्षमताएँ जोड़ रहे हों, यह तरीका आपको Photoshop फ़ाइलों पर बारीकी से नियंत्रण देता है बिना Photoshop की आवश्यकता के। आगे भी अन्वेषण करने के लिए स्वतंत्र महसूस करें—जैसे फ़िल्टर लागू करना, प्रोग्रामेटिक रूप से लेयर्स को मर्ज करना, या प्रत्येक लेयर को अलग‑अलग एक्सपोर्ट करना।

---

**अंतिम अपडेट:** 2025-12-10  
**परीक्षित संस्करण:** Aspose.PSD for Java 24.11 (लेखन के समय नवीनतम)  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}