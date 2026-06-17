---
date: 2026-04-22
description: जानेँ कैसे इमेज प्रोसेसिंग जावा लाइब्रेरी Aspose.PSD का उपयोग करके कई
  एडजस्टमेंट लेयर्स, जिसमें इनवर्ट एडजस्टमेंट लेयर भी शामिल है, लागू करें, ताकि PSD
  को सहजता से मैनिपुलेट किया जा सके।
keywords:
- image processing java library
- how to add invert
- invert colors psd
- batch process psd images
- apply multiple adjustment layers
linktitle: समायोजन लेयर को उलटें
second_title: Aspose.PSD Java API
title: 'इमेज प्रोसेसिंग जावा लाइब्रेरी: Aspose.PSD का उपयोग करके लेयर उलटें'
url: /hi/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java में इनवर्ट एडजस्टमेंट लेयर

## परिचय

यदि आप एक मजबूत **image processing java library** की तलाश में हैं, तो Aspose.PSD for Java बाजार में सबसे बहुमुखी विकल्पों में से एक है। इस ट्यूटोरियल में हम बताएँगे कि कैसे एक **Invert Adjustment Layer** को PSD फ़ाइल में जोड़ा जाए, एक तकनीक जिसे आप अन्य एडजस्टमेंट लेयर्स के साथ मिलाकर परिष्कृत दृश्य प्रभाव प्राप्त कर सकते हैं। चाहे आप बैच‑प्रोसेसिंग टूल, सर्वर‑साइड इमेज सर्विस, या सिंगल‑इमेज एडिटर बना रहे हों, यह गाइड आपको स्पष्ट, चरण‑दर‑चरण मार्ग प्रदान करता है जिससे आप काम जल्दी और भरोसेमंद तरीके से पूरा कर सकते हैं।

## त्वरित उत्तर

- **Invert Adjustment Layer क्या करता है?** यह चयनित क्षेत्र में सभी रंग मानों को उलट देता है, जिससे एक नेगेटिव‑इमेज प्रभाव बनता है (अर्थात यह **convert PSD to negative** करता है)।  
- **यह सुविधा कौन सी लाइब्रेरी प्रदान करती है?** Aspose.PSD, एक प्रमुख **image processing java library**।  
- **क्या मैं इसे अन्य एडजस्टमेंट्स के साथ स्टैक कर सकता हूँ?** हाँ – आप **apply multiple adjustment layers** जैसे Brightness/Contrast, Hue/Saturation, आदि जोड़ सकते हैं।  
- **क्या विकास के लिए मुझे लाइसेंस चाहिए?** एक मुफ्त ट्रायल उपलब्ध है; उत्पादन उपयोग के लिए लाइसेंस आवश्यक है।  
- **इम्प्लीमेंटेशन में कितना समय लगता है?** सामान्यतः बुनियादी उपयोग‑केस के लिए 10 मिनट से कम।

## Invert Adjustment Layer क्या है?

Invert Adjustment Layer एक नॉन‑डिस्ट्रक्टिव एडिट है जो प्रभावित प्रत्येक पिक्सेल के RGB मानों को उलट देता है। क्योंकि यह लेयर स्टैक के शीर्ष पर स्थित होता है, आप इसकी दृश्यता को टॉगल कर सकते हैं या इसे पुनः क्रमित कर सकते हैं बिना मूल इमेज डेटा को स्थायी रूप से बदलें। यह **invert colors PSD** फ़ाइलों को उलटने या फ़ोटोग्राफ़िक नेगेटिव बनाने का सबसे आसान तरीका है।

## Aspose.PSD को अपने Image Processing Java Library के रूप में क्यों उपयोग करें?

- **Full PSD support** – Photoshop फ़ाइलों को पढ़ना, संपादित करना और लिखना बिना Photoshop स्थापित किए।  
- **Cross‑platform** – किसी भी Java runtime (Java 6+) पर काम करता है।  
- **Rich adjustment features** – कई सामान्य संपादनों के लिए बिल्ट‑इन मेथड्स शामिल हैं, जिससे एक ही वर्कफ़्लो में **apply multiple adjustment layers** करना आसान हो जाता है।  
- **Performance‑optimized** – बड़े फ़ाइलों को कुशलता से संभालता है, जो **batch process psd images** के लिए आवश्यक है।  

## पूर्वापेक्षाएँ

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1. **Aspose.PSD Library** – इसे आधिकारिक साइट [here](https://releases.aspose.com/psd/java/) से डाउनलोड करें।  
2. **Java Development Environment** – JDK 6.0 या बाद का स्थापित और कॉन्फ़िगर किया हुआ।  

अब, चलिए कोड में डुबकी लगाते हैं।

## पैकेज आयात करें

आवश्यक क्लासेस को इम्पोर्ट करके शुरू करें। ये इम्पोर्ट्स आपको कोर image‑handling APIs और PSD‑विशिष्ट कार्यक्षमता तक पहुँच प्रदान करते हैं।

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

## चरण 1: दस्तावेज़ डायरेक्टरी सेट अप करें

उस फ़ोल्डर को परिभाषित करें जिसमें आपका स्रोत PSD फ़ाइल है और जहाँ आउटपुट सहेजा जाएगा।

```java
String dataDir = "Your Document Directory";
```

## चरण 2: PSD फ़ाइल लोड करें

स्रोत फ़ाइल को `PsdImage` ऑब्जेक्ट में लोड करें। यह ऑब्जेक्ट मेमोरी में पूरे PSD दस्तावेज़ का प्रतिनिधित्व करता है।

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

## चरण 3: Invert Adjustment Layer जोड़ें

वर्तमान लेयर स्टैक के शीर्ष पर Invert Adjustment Layer डालने के लिए बिल्ट‑इन मेथड को कॉल करें। आप बाद में अधिक लेयर्स (जैसे Brightness, Hue) जोड़ सकते हैं ताकि **apply multiple adjustment layers** किया जा सके।

```java
im.addInvertAdjustmentLayer();
```

## चरण 4: आउटपुट सहेजें

परिवर्तित PSD को डिस्क पर सहेजें। सहेजी गई फ़ाइल अब Invert Adjustment Layer शामिल करती है और इसे Photoshop या किसी भी PSD‑संगत व्यूअर में खोला जा सकता है।

```java
im.save(outputPath);
```

### क्या हुआ अभी?

- PSD मेमोरी में लोड किया गया।  
- एक Invert Adjustment Layer शीर्षmost लेयर के रूप में जोड़ा गया।  
- इमेज सहेजी गई, नॉन‑डिस्ट्रक्टिव एडिट को संरक्षित रखते हुए।

आपने अब सफलतापूर्वक Aspose.PSD, एक **image processing java library**, का उपयोग करके PSD फ़ाइल को संशोधित किया है।

## इनवर्ट एडजस्टमेंट के साथ PSD इमेजेज़ का बैच प्रोसेसिंग

यदि आपको दर्जनों या सैकड़ों फ़ाइलों पर समान इनवर्ट इफ़ेक्ट लागू करना है, तो आप ऊपर दिया गया कोड एक सरल लूप में रख सकते हैं जो PSDs की डायरेक्टरी पर इटररेट करता है। क्योंकि लाइब्रेरी **performance‑optimized** है, बड़े बैचों को प्रोसेस करना तेज़ रहता है, और आप उसी लूप में इनवर्ट स्टेप को अन्य एडजस्टमेंट्स (जैसे brightness, hue) के साथ जोड़ सकते हैं।

## PSD को नेगेटिव इमेज में बदलना

Invert Adjustment Layer मूलतः **convert PSD to negative** ऑपरेशन है। इस लेयर को शीर्षmost आइटम के रूप में जोड़कर, आप पूर्ण‑नेगेटिव प्रभाव प्राप्त करते हैं बिना मूल पिक्सेल डेटा को स्थायी रूप से बदले। आप बाद में लेयर को हटा या डिसेबल कर मूल रूप में वापस जा सकते हैं।

## सामान्य समस्याएँ और टिप्स

| समस्या | कारण | समाधान |
|-------|-------|----------|
| **NullPointerException on `Image.load`** | गलत फ़ाइल पथ या फ़ाइल अनुपलब्ध | `dataDir` और फ़ाइल नाम की जाँच करें; परीक्षण के लिए पूर्ण पथ (absolute paths) का उपयोग करें। |
| **Layer order not as expected** | मौजूदा लेयर्स के बाद लेयर्स जोड़ने से स्टैकिंग बदलती है | `im.addInvertAdjustmentLayer()` को अन्य एडजस्टमेंट्स जोड़ने से पहले उपयोग करें, या `im.getLayers()` के माध्यम से लेयर्स को पुनः क्रमित करें। |
| **Performance slowdown on large PSDs** | बहुत बड़ी फ़ाइलों को मेमोरी में लोड करना | पृष्ठों को भागों में प्रोसेस करने पर विचार करें या JVM हीप साइज (`-Xmx2g`) बढ़ाएँ। |

## अक्सर पूछे जाने वाले प्रश्न

**Q: क्या Aspose.PSD सभी Java संस्करणों के साथ संगत है?**  
A: Aspose.PSD Java 6.0 और बाद के संस्करणों को सपोर्ट करता है।

**Q: क्या मैं एक ही ऑपरेशन में कई एडजस्टमेंट लेयर्स लागू कर सकता हूँ?**  
A: हाँ, आप कई एडजस्टमेंट लेयर्स—जैसे Invert, Brightness, और Hue/Saturation—को स्टैक करके जटिल प्रभाव प्राप्त कर सकते हैं।

**Q: Aspose.PSD के लिए अतिरिक्त दस्तावेज़ीकरण कहाँ मिल सकता है?**  
A: व्यापक गाइड्स और API रेफ़रेंसेज़ के लिए दस्तावेज़ीकरण [here](https://reference.aspose.com/psd/java/) देखें।

**Q: क्या Aspose.PSD के लिए मुफ्त ट्रायल उपलब्ध है?**  
A: हाँ, आप मुफ्त ट्रायल [here](https://releases.aspose.com/) का अन्वेषण कर सकते हैं।

**Q: मैं Aspose.PSD के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूँ?**  
A: आप अस्थायी लाइसेंस [here](https://purchase.aspose.com/temporary-license/) प्राप्त कर सकते हैं।

---

**अंतिम अपडेट:** 2026-04-22  
**परीक्षित संस्करण:** Aspose.PSD 24.12 for Java  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}