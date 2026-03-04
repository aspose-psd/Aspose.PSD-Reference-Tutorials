---
date: 2026-03-04
description: Aspose.PSD for Java का उपयोग करके फ़िल लेयर जोड़कर प्रोग्रामेटिक रूप
  से PSD लेयर को संशोधित करना सीखें। अपने डिज़ाइनों को जल्दी सुधारने के लिए इस चरण‑दर‑चरण
  गाइड का पालन करें।
linktitle: Modify PSD Layers Programmatically – Add Fill Layers (Java)
second_title: Aspose.PSD Java API
title: PSD लेयर्स को प्रोग्रामेटिकली संशोधित करें – फ़िल लेयर्स जोड़ें (Java)
url: /hi/java/modifying-converting-psd-images/add-fill-layers-psd-files/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD लेयर्स को प्रोग्रामेटिकली संशोधित करें – फ़िल लेयर जोड़ें (Java)

यदि आप **PSD लेयर्स को प्रोग्रामेटिकली संशोधित** करना चाहते हैं, तो फ़िल लेयर जोड़ना आपके Photoshop दस्तावेज़ों को बिना Photoshop खोले समृद्ध करने का सबसे तेज़ तरीका है। इस ट्यूटोरियल में हम उन सटीक चरणों को दिखाएंगे जिनकी आपको नई PSD बनाने, रंग, ग्रेडिएंट और पैटर्न फ़िल लेयर डालने, और फिर परिणाम को सहेजने के लिए आवश्यकता होगी—सभी Aspose.PSD for Java का उपयोग करके।

## त्वरित उत्तर
- **मैं क्या हासिल कर सकता हूँ?** PSD फ़ाइल में प्रोग्रामेटिकली रंग, ग्रेडिएंट और पैटर्न फ़िल लेयर जोड़ें।  
- **कौन सी लाइब्रेरी आवश्यक है?** Aspose.PSD for Java (latest release).  
- **क्या मुझे लाइसेंस चाहिए?** परीक्षण के लिए एक मुफ्त ट्रायल काम करता है; उत्पादन के लिए एक व्यावसायिक लाइसेंस आवश्यक है।  
- **इम्प्लीमेंटेशन में कितना समय लगेगा?** बुनियादी उदाहरण के लिए लगभग 10‑15 मिनट।  
- **कौन सा Java संस्करण समर्थित है?** JDK 11 या बाद का।

## “PSD लेयर्स को प्रोग्रामेटिकली संशोधित” क्या है?
PSD लेयर्स को प्रोग्रामेटिकली संशोधित करना मतलब कोड का उपयोग करके Photoshop दस्तावेज़ के भीतर लेयर्स को बनाना, संपादित करना या हटाना, जिससे आपको डिज़ाइन वर्कफ़्लो पर पूरी नियंत्रण मिलती है बिना मैन्युअल UI इंटरैक्शन के।

## Aspose.PSD के साथ फ़िल लेयर क्यों जोड़ें?
- **ऑटोमेशन** – बैच जॉब में दर्जनों PSD उत्पन्न करें।  
- **संगति** – कई फ़ाइलों में बिल्कुल वही रंग, ग्रेडिएंट या पैटर्न लागू करें।  
- **गति** – Photoshop में समय‑साध्य मैन्युअल चरणों को छोड़ें।  
- **क्रॉस‑प्लेटफ़ॉर्म** – किसी भी OS पर काम करता है जो Java का समर्थन करता है।

## पूर्वापेक्षाएँ
कोड में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1. **Java Development Kit (JDK)** – JDK 11 या नया स्थापित करें। आप इसे [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) से डाउनलोड कर सकते हैं।  
2. **Aspose.PSD for Java** – आधिकारिक डाउनलोड पेज से नवीनतम लाइब्रेरी प्राप्त करें [here](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, या कोई भी एडिटर जो आप पसंद करते हैं।  
4. **Basic Java knowledge** – क्लास और मेथड्स की परिचितता मददगार होगी, लेकिन ट्यूटोरियल सब कुछ चरण‑दर‑चरण समझाता है।

## पैकेज इम्पोर्ट करें
PSD फ़ाइलों के साथ काम शुरू करने के लिए आपको संबंधित Aspose.PSD क्लासेस इम्पोर्ट करने की आवश्यकता है:

```java
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
```

ये इम्पोर्ट्स आपको `PsdImage` ऑब्जेक्ट (दस्तावेज़ स्वयं) और विभिन्न `FillLayer` प्रकारों तक पहुँच प्रदान करते हैं जिन्हें हम उपयोग करेंगे।

## PSD लेयर्स को प्रोग्रामेटिकली संशोधित करने का चरण‑दर‑चरण मार्गदर्शक

### चरण 1: अपना आउटपुट डायरेक्टरी सेट करें
परिणामी PSD को कहाँ सहेजना है, यह निर्धारित करें ताकि आप बाद में उसे ढूँढ सकें।

```java
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "output.psd";
```

`"Your Document Directory"` को अपने मशीन पर एक पूर्ण या सापेक्ष पथ से बदलें।

### चरण 2: नया Photoshop दस्तावेज़ बनाएं
एक खाली कैनवास बनाएं जो फ़िल लेयर को होस्ट करेगा।

```java
PsdImage psdImage = new PsdImage(100, 100);
```

`100, 100` पैरामीटर पिक्सेल में चौड़ाई और ऊँचाई दर्शाते हैं। इन्हें अपनी डिज़ाइन आवश्यकताओं के अनुसार समायोजित करें।

### चरण 3: एक रंग फ़िल लेयर जोड़ें
एक सॉलिड‑कलर फ़िल लेयर बनाएं और उसे एक उपयुक्त नाम दें।

```java
FillLayer colorFillLayer = FillLayer.createInstance(FillType.Color);
colorFillLayer.setDisplayName("Color Fill Layer");
psdImage.addLayer(colorFillLayer);
```

आप बाद में लेयर की फ़िल सेटिंग्स तक पहुँच कर वास्तविक रंग बदल सकते हैं (संक्षिप्तता के लिए यहाँ नहीं दिखाया गया)।

### चरण 4: एक ग्रेडिएंट फ़िल लेयर जोड़ें
ग्रेडिएंट फ़िल लेयर गहराई और दृश्य आकर्षण जोड़ते हैं।

```java
FillLayer gradientFillLayer = FillLayer.createInstance(FillType.Gradient);
gradientFillLayer.setDisplayName("Gradient Fill Layer");
psdImage.addLayer(gradientFillLayer);
```

लेयर की सेटिंग्स के माध्यम से रैखिक या रेडियल ग्रेडिएंट के साथ प्रयोग करने के लिए स्वतंत्र महसूस करें।

### चरण 5: एक पैटर्न फ़िल लेयर जोड़ें
पैटर्न फ़िल लेयर आपको लेयर पर छवियों या टेक्सचर को टाइल करने की अनुमति देते हैं।

```java
FillLayer patternFillLayer = FillLayer.createInstance(FillType.Pattern);
patternFillLayer.setDisplayName("Pattern Fill Layer");
patternFillLayer.setOpacity((byte)50);
psdImage.addLayer(patternFillLayer);
```

ऑपेसिटी को 50 % सेट करने से पैटर्न नीचे की लेयर्स के साथ सुगमता से मिश्रित हो जाता है।

### चरण 6: अपना PSD फ़ाइल सहेजें
परिवर्तनों को डिस्क पर सहेजें।

```java
psdImage.save(outPsdFilePath);
```

सहेजी गई फ़ाइल को Photoshop या किसी भी PSD व्यूअर में खोलें ताकि आप तीन नई फ़िल लेयर देख सकें।

### चरण 7: संसाधनों को साफ़ करें
नेटीव मेमोरी मुक्त करने के लिए हमेशा `PsdImage` ऑब्जेक्ट को डिस्पोज़ करें।

```java
psdImage.dispose();
```

## सामान्य समस्याएँ और सुझाव
- **अमान्य आउटपुट पथ** – सुनिश्चित करें कि डायरेक्टरी मौजूद है और आपके पास लिखने की अनुमति है।  
- **मेमोरी उपयोग** – बहुत बड़े कैनवास के लिए, इमेज के साथ काम समाप्त होते ही `psdImage.dispose()` कॉल करें।  
- **लेयर क्रम** – डिफ़ॉल्ट रूप से लेयर्स स्टैक के शीर्ष पर जोड़ी जाती हैं; यदि आपको विशिष्ट क्रम चाहिए तो `psdImage.insertLayer(layer, index)` उपयोग करें।

## अक्सर पूछे जाने वाले प्रश्न

**Q: Aspose.PSD for Java का उपयोग करके मैं कौन‑से प्रकार की फ़िल लेयर जोड़ सकता हूँ?**  
A: आप रंग, ग्रेडिएंट और पैटर्न फ़िल लेयर जोड़ सकते हैं।

**Q: क्या Aspose.PSD अन्य इमेज फ़ॉर्मेट्स को सपोर्ट करता है?**  
A: हाँ, यह BMP, JPEG, PNG और कई अन्य फ़ॉर्मेट्स के साथ काम करता है।

**Q: क्या मैं Aspose.PSD को मुफ्त में उपयोग कर सकता हूँ?**  
A: आप Aspose.PSD for Java का मुफ्त ट्रायल [here](https://releases.aspose.com/) पर देख सकते हैं।

**Q: Aspose.PSD के बारे में अधिक दस्तावेज़ीकरण कहाँ मिल सकता है?**  
A: आप पूर्ण दस्तावेज़ीकरण [here](https://reference.aspose.com/psd/java/) पर प्राप्त कर सकते हैं।

**Q: क्या Aspose.PSD के लिए कोई सपोर्ट कम्युनिटी है?**  
A: हाँ, आप Aspose फ़ोरम पर कम्युनिटी से मदद ले सकते हैं [here](https://forum.aspose.com/c/psd/34)।

## निष्कर्ष
आपने अब सीखा कि Aspose.PSD for Java का उपयोग करके विभिन्न फ़िल लेयर जोड़कर **PSD लेयर्स को प्रोग्रामेटिकली संशोधित** कैसे किया जाता है। यह तरीका आपका समय बचाता है, प्रोजेक्ट्स में संगति सुनिश्चित करता है, और शक्तिशाली बैच‑प्रोसेसिंग परिदृश्यों के द्वार खोलता है। विभिन्न रंग, ग्रेडिएंट और पैटर्न के साथ प्रयोग करें और देखें कि आप स्वचालित डिज़ाइन निर्माण को कितनी दूर तक ले जा सकते हैं।

---

**अंतिम अपडेट:** 2026-03-04  
**परीक्षित संस्करण:** Aspose.PSD for Java (latest release)  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}