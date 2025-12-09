---
date: 2025-12-02
description: इमेज प्रोसेसिंग जावा लाइब्रेरी Aspose.PSD का उपयोग करके कई एडजस्टमेंट
  लेयर्स, जिसमें इनवर्ट एडजस्टमेंट लेयर भी शामिल है, को लागू करना सीखें, ताकि PSD
  को सहजता से मैनिपुलेट किया जा सके।
linktitle: Invert Adjustment Layer
second_title: Aspose.PSD Java API
title: 'इमेज प्रोसेसिंग जावा लाइब्रेरी: Aspose.PSD के साथ लेयर को उलटें'
url: /hi/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java में Invert Adjustment Layer

## Introduction

यदि आप एक मजबूत **image processing java library** की तलाश में हैं, तो Aspose.PSD for Java बाजार में सबसे बहुमुखी विकल्पों में से एक है। इस ट्यूटोरियल में हम बताएँगे कि कैसे एक **Invert Adjustment Layer** को PSD फ़ाइल में जोड़ा जाए, ऐसी तकनीक जिसे आप अन्य एडजस्टमेंट लेयर्स के साथ मिलाकर जटिल विज़ुअल इफ़ेक्ट्स प्राप्त कर सकते हैं। चाहे आप बैच‑प्रोसेसिंग टूल बना रहे हों या सिंगल‑इमेज एडिटर, यह गाइड आपको स्पष्ट, चरण‑दर‑चरण मार्ग प्रदान करता है जिससे आप जल्दी काम पूरा कर सकें।

## Quick Answers
- **Invert Adjustment Layer क्या करता है?** यह चयनित क्षेत्र में सभी रंग मानों को उलट देता है, जिससे नकारात्मक‑इमेज प्रभाव बनता है।  
- **यह सुविधा कौन सी लाइब्रेरी प्रदान करती है?** Aspose.PSD, एक प्रमुख **image processing java library**।  
- **क्या मैं इसे अन्य एडजस्टमेंट्स के साथ स्टैक कर सकता हूँ?** हाँ – आप **apply multiple adjustment layers** जैसे Brightness/Contrast, Hue/Saturation, आदि लागू कर सकते हैं।  
- **क्या विकास के लिए लाइसेंस चाहिए?** एक मुफ्त ट्रायल उपलब्ध है; उत्पादन उपयोग के लिए लाइसेंस आवश्यक है।  
- **इम्प्लीमेंटेशन में कितना समय लगता है?** आम तौर पर बुनियादी उपयोग‑केस के लिए 10 मिनट से कम।

## What is the Invert Adjustment Layer?

Invert Adjustment Layer एक नॉन‑डिस्ट्रक्टिव एडिट है जो प्रभावित प्रत्येक पिक्सेल के RGB मानों को उलट देता है। क्योंकि यह लेयर स्टैक के ऊपर स्थित होता है, आप इसकी विज़िबिलिटी टॉगल कर सकते हैं या इसे पुनः क्रमित कर सकते हैं बिना मूल इमेज डेटा को स्थायी रूप से बदलें।

## Why Use Aspose.PSD as Your Image Processing Java Library?

- **Full PSD support** – Photoshop इंस्टॉल किए बिना Photoshop फ़ाइलों को पढ़ें, संपादित करें और लिखें।  
- **Cross‑platform** – किसी भी Java runtime (Java 6+) पर काम करता है।  
- **Rich adjustment features** – कई सामान्य एडिट्स के लिए बिल्ट‑इन मेथड्स शामिल हैं, जिससे एक ही वर्कफ़्लो में **apply multiple adjustment layers** करना आसान हो जाता है।  
- **Performance‑optimized** – बड़े फ़ाइलों को कुशलता से संभालता है, जो बैच प्रोसेसिंग के लिए आवश्यक है।

## Prerequisites

शुरू करने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1. **Aspose.PSD Library** – इसे आधिकारिक साइट [यहाँ](https://releases.aspose.com/psd/java/) से डाउनलोड करें।  
2. **Java Development Environment** – JDK 6.0 या बाद का संस्करण इंस्टॉल और कॉन्फ़िगर किया हुआ हो।  

अब, चलिए कोड में डुबकी लगाते हैं।

## Import Packages

आवश्यक क्लासेज़ को इम्पोर्ट करके शुरू करें। ये इम्पोर्ट्स आपको कोर इमेज‑हैंडलिंग API और PSD‑स्पेसिफिक फ़ंक्शनैलिटी तक पहुंच देते हैं।

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

## Step 1: Set Up Document Directory

उस फ़ोल्डर को परिभाषित करें जिसमें आपका स्रोत PSD फ़ाइल है और जहाँ आउटपुट सहेजा जाएगा।

```java
String dataDir = "Your Document Directory";
```

## Step 2: Load PSD File

स्रोत फ़ाइल को एक `PsdImage` ऑब्जेक्ट में लोड करें। यह ऑब्जेक्ट पूरी PSD डॉक्यूमेंट को मेमोरी में प्रतिनिधित्व करता है।

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

## Step 3: Add Invert Adjustment Layer

बिल्ट‑इन मेथड को कॉल करके वर्तमान लेयर स्टैक के ऊपर एक Invert Adjustment Layer डालें। आप बाद में अधिक लेयर्स (जैसे Brightness, Hue) जोड़कर **apply multiple adjustment layers** कर सकते हैं।

```java
im.addInvertAdjustmentLayer();
```

## Step 4: Save the Output

परिवर्तित PSD को डिस्क पर सहेजें। सहेजी गई फ़ाइल अब Invert Adjustment Layer शामिल करती है और इसे Photoshop या किसी भी PSD‑संगत व्यूअर में खोला जा सकता है।

```java
im.save(outputPath);
```

### What just happened?

- PSD मेमोरी में लोड किया गया।  
- Invert Adjustment Layer को सबसे ऊपर की लेयर के रूप में जोड़ा गया।  
- इमेज को सहेजा गया, जिससे नॉन‑डिस्ट्रक्टिव एडिट संरक्षित रहा।

आपने अब सफलतापूर्वक Aspose.PSD, एक **image processing java library**, का उपयोग करके PSD फ़ाइल को मैनिपुलेट किया है।

## Common Issues & Tips

| समस्या | कारण | समाधान |
|-------|-------|----------|
| **`Image.load` पर NullPointerException** | गलत फ़ाइल पथ या फ़ाइल अनुपलब्ध | `dataDir` और फ़ाइल नाम की जाँच करें; परीक्षण के लिए पूर्ण पथ उपयोग करें |
| **लेयर क्रम अपेक्षित नहीं** | मौजूदा लेयर्स के बाद लेयर्स जोड़ने से स्टैकिंग बदलती है | अन्य एडजस्टमेंट्स जोड़ने से पहले `im.addInvertAdjustmentLayer()` उपयोग करें, या `im.getLayers()` के माध्यम से लेयर्स को पुनः क्रमित करें |
| **बड़े PSDs पर प्रदर्शन में गिरावट** | बहुत बड़ी फ़ाइलों को मेमोरी में लोड करना | पृष्ठों को भागों में प्रोसेस करने या JVM हीप आकार (`-Xmx2g`) बढ़ाने पर विचार करें |

## Frequently Asked Questions

**Q: क्या Aspose.PSD सभी Java संस्करणों के साथ संगत है?**  
A: Aspose.PSD Java 6.0 और बाद के संस्करणों को समर्थन देता है।

**Q: क्या मैं एक ही ऑपरेशन में कई एडजस्टमेंट लेयर्स लागू कर सकता हूँ?**  
A: हाँ, आप कई एडजस्टमेंट लेयर्स—जैसे Invert, Brightness, और Hue/Saturation—को स्टैक कर सकते हैं ताकि जटिल प्रभाव प्राप्त हो सकें।

**Q: Aspose.PSD के अतिरिक्त दस्तावेज़ कहाँ मिल सकते हैं?**  
A: विस्तृत गाइड और API रेफ़रेंसेज़ के लिए दस्तावेज़ [यहाँ](https://reference.aspose.com/psd/java/) देखें।

**Q: क्या Aspose.PSD के लिए मुफ्त ट्रायल उपलब्ध है?**  
A: हाँ, आप मुफ्त ट्रायल [यहाँ](https://releases.aspose.com/) देख सकते हैं।

**Q: मैं Aspose.PSD के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूँ?**  
A: आप अस्थायी लाइसेंस [यहाँ](https://purchase.aspose.com/temporary-license/) प्राप्त कर सकते हैं।

**Last Updated:** 2025-12-02  
**Tested With:** Aspose.PSD 24.12 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}