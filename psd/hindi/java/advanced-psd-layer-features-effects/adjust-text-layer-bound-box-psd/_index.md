---
date: 2026-02-14
description: Aspose PSD Java का उपयोग करके PSD फ़ाइल में टेक्स्ट बाउंड बॉक्स को प्राप्त
  करने और समायोजित करने का तरीका सीखें। जावा कोड के साथ चरण-दर-चरण गाइड।
linktitle: Adjust Text Layer Bound Box in PSD using Java
second_title: Aspose.PSD Java API
title: 'aspose psd java: PSD में टेक्स्ट लेयर बाउंड बॉक्स को समायोजित करें'
url: /hi/java/advanced-psd-layer-features-effects/adjust-text-layer-bound-box-psd/
weight: 25
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD को कैसे संपादित करें: जावा में टेक्स्ट लेयर बाउंड बॉक्स को समायोजित करें

## Introduction
यदि आप प्रोग्रामेटिक रूप से **PSD फ़ाइलों को कैसे संपादित करें** के बारे में सोच रहे हैं—विशेष रूप से जब आपको **Photoshop टेक्स्ट लेयर** गुणों को **संपादित** करने की आवश्यकता हो—तो जावा के लिए Aspose.PSD लाइब्रेरी बहुत उपयोगी है। यह ट्यूटोरियल आपको **टेक्स्ट बाउंड बॉक्स को समायोजित करने** और **टेक्स्ट बाउंड बॉक्स** जानकारी को **aspose psd java** का उपयोग करके प्राप्त करने के सटीक चरणों से परिचित कराएगा। चाहे आप एक अनुभवी डेवलपर हों या जावा में अभी शुरुआत कर रहे हों, आपको स्पष्ट, संवादात्मक मार्गदर्शन मिलेगा जो PSD हेरफेर को सरल और सुलभ बनाता है। चलिए शुरू करते हैं!

## Quick Answers
- **Java में PSD फ़ाइलों को संपादित करने में कौन सी लाइब्रेरी मदद करती है?** Aspose.PSD for Java.  
- **क्या मैं टेक्स्ट लेयर के बाउंड बॉक्स को समायोजित कर सकता हूँ?** हाँ—`getTextBoundBox()` और संबंधित साइज मेथड्स का उपयोग करें।  
- **क्या मुझे Photoshop स्थापित करने की आवश्यकता है?** नहीं, Aspose.PSD Adobe Photoshop से स्वतंत्र रूप से काम करता है।  
- **मुख्य पूर्वापेक्षाएँ क्या हैं?** JDK, एक IDE, और Aspose.PSD for Java लाइब्रेरी।  
- **बेसिक इम्प्लीमेंटेशन में कितना समय लगता है?** सैंपल कोड चलाने में लगभग 10‑15 मिनट।

## What is “how to edit psd” with Aspose.PSD?
प्रोग्रामेटिक रूप से PSD को संपादित करना मतलब फ़ाइल को खोलना, उसकी लेयर्स तक पहुँच बनाना, और आकार, स्थिति, या टेक्स्ट सामग्री जैसे गुणों को संशोधित करना—बिना Photoshop लॉन्च किए। Aspose.PSD एक समृद्ध API प्रदान करता है जो जटिल PSD फ़ॉर्मेट को एब्स्ट्रैक्ट करता है, जिससे आप अपनी आवश्यक लॉजिक पर ध्यान केंद्रित कर सकते हैं।

## Why use Aspose.PSD for Java?
- **Photoshop की आवश्यकता नहीं** – किसी भी सर्वर या डेस्कटॉप वातावरण में काम करता है।  
- **पूर्ण लेयर समर्थन** – रास्टर, वेक्टर, और टेक्स्ट लेयर्स को पढ़ा या संशोधित किया जा सकता है।  
- **उच्च प्रदर्शन** – बड़े फ़ाइलों और बैच प्रोसेसिंग के लिए अनुकूलित।  
- **क्रॉस‑प्लेटफ़ॉर्म** – वही कोड उपयोग करके Windows, Linux, या macOS पर चलाएँ।

## Prerequisites
1. **Java Development Kit (JDK)** – [Oracle वेबसाइट](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) से डाउनलोड करें।  
2. **Integrated Development Environment (IDE)** – Eclipse, IntelliJ IDEA, या NetBeans।  
3. **Aspose.PSD for Java लाइब्रेरी** – नवीनतम संस्करण [Aspose रिलीज़ पेज](https://releases.aspose.com/psd/java/) से प्राप्त करें।  
4. **बेसिक Java ज्ञान** – क्लासेस, ऑब्जेक्ट्स, और एरेज़ की परिचितता।

बहुत बढ़िया! इन सबके साथ, चलिए कोडिंग शुरू करते हैं।

## Import Packages
पहला कदम वह क्लासेस इम्पोर्ट करना है जिनकी आपको आवश्यकता होगी। इसे एक DIY प्रोजेक्ट शुरू करने से पहले सभी टूल्स इकट्ठा करने के रूप में सोचें।

```java
import com.aspose.psd.Image;
import com.aspose.psd.Size;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
```

ये इम्पोर्ट्स आपको इमेज हैंडलिंग, साइज मैनिपुलेशन, और `TextLayer` क्लास तक पहुँच प्रदान करते हैं, जिसके साथ हम काम करेंगे।

## Step 1: Set Up Your File Paths
निर्दिष्ट करें कि आपका PSD फ़ाइल कहाँ स्थित है। यह प्रदर्शन शुरू होने से पहले मंच तैयार करने जैसा है।

```java
String dataDir = "Your Document Directory"; 
String sourceFileName = dataDir + "LayerWithText.psd";
```

`"Your Document Directory"` को अपने मशीन पर वास्तविक फ़ोल्डर पाथ से बदलें।

## Step 2: Load the PSD File
अब हम PSD खोलते हैं ताकि हम उसकी लेयर्स के साथ इंटरैक्ट कर सकें।

```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

`Image.load` मेथड फ़ाइल को पढ़ता है और एक `PsdImage` ऑब्जेक्ट लौटाता है जो हेरफेर के लिए तैयार है।

## Step 3: Retrieve the Text Layer
उस विशिष्ट टेक्स्ट लेयर की पहचान करें जिसे आप समायोजित करना चाहते हैं। लेयर्स शून्य‑इंडेक्स्ड होती हैं, इसलिए `[1]` दूसरा लेयर दर्शाता है।

```java
TextLayer textLayer = (TextLayer) im.getLayers()[1];
```

सुनिश्चित करें कि आप सही लेयर को टार्गेट कर रहे हैं; अन्यथा आप गलत सामग्री को संशोधित कर सकते हैं।

## Step 4: Check the Size of the Layer
किसी भी परिवर्तन से पहले, वर्तमान साइज को सत्यापित करना एक अच्छा विचार है। यह एक सैनीटी चेक के रूप में कार्य करता है।

```java
Size correctOpticalSize = new Size(127, 45);
Size opticalSize = textLayer.getSize();
Assert.areEqual(correctOpticalSize, opticalSize);
```

यदि साइज मेल नहीं खाते, तो `Assert` एक अलर्ट उठाएगा, जिससे आपको पता चलेगा कि कुछ गड़बड़ है।

## Step 5: Get the Bound Box Size
अब हम **टेक्स्ट बाउंड बॉक्स** प्राप्त करते हैं—वह आयत जो रेंडर किए गए टेक्स्ट को घेरती है।

```java
Size correctBoundBox = new Size(172, 62);
Size boundBox = textLayer.getTextBoundBox();
Assert.areEqual(correctBoundBox, boundBox);
```

आप इस साइज की तुलना अपनी अपेक्षित डाइमेंशन से कर सकते हैं या आगे के समायोजन की गणना के लिए इसका उपयोग कर सकते हैं।

## How to retrieve text bound box using aspose psd java
जब आपको टेक्स्ट लेयर के सटीक आयाम चाहिए, तो `getTextBoundBox()` एक `Size` ऑब्जेक्ट लौटाता है जो बाउंडिंग आयत को दर्शाता है। यह मेथड उन परिस्थितियों में आवश्यक है जहाँ आपको अन्य डिज़ाइन एलिमेंट्स को संरेखित करना होता है या यह सुनिश्चित करना होता है कि टेक्स्ट पूर्वनिर्धारित क्षेत्र में फिट हो।

## How to adjust text bound box with aspose psd java
यदि प्राप्त बाउंड बॉक्स आपके डिज़ाइन आवश्यकताओं से मेल नहीं खाता, तो आप `setSize()` (यहाँ नहीं दिखाया गया) का उपयोग करके लेयर का साइज बदल सकते हैं या लेयर को रास्टराइज़ करने से पहले स्केलिंग ट्रांसफ़ॉर्मेशन लागू कर सकते हैं। बाउंड बॉक्स को समायोजित करने से यह सुनिश्चित होता है कि विज़ुअल लेआउट विभिन्न आउटपुट फ़ॉर्मेट्स में सुसंगत बना रहे।

## Common Use Cases
- **डायनामिक थंबनेल जनरेशन** – प्रीव्यू को रास्टराइज़ करने से पहले टेक्स्ट बाउंड्स को समायोजित करें।  
- **ऑटोमेटेड ब्रांडिंग** – प्रोग्रामेटिक रूप से लोगो टेक्स्ट बदलें और सुनिश्चित करें कि वह डिज़ाइन सीमाओं के भीतर फिट हो।  
- **बैच प्रोसेसिंग** – कई PSD फ़ाइलों पर इटरेट करके प्रोडक्ट लाइन में टेक्स्ट लेयर साइज को मानकीकृत करें।

## Troubleshooting & Tips
- **गलत लेयर इंडेक्स** – Photoshop में लेयर्स के क्रम को दोबारा जांचें; इंडेक्स आपके अनुमान से अलग हो सकता है।  
- **लाइसेंस समस्याएँ** – ट्रायल संस्करण कुछ ऑपरेशन्स को सीमित कर सकता है; उत्पादन के लिए सुनिश्चित करें कि आपके पास वैध लाइसेंस है।  
- **अप्रत्याशित साइज** – DPI सेटिंग्स साइज गणना को प्रभावित कर सकती हैं; यदि संख्याएँ गलत लगें तो PSD की रिज़ॉल्यूशन जांचें।

## Conclusion
आपने अब **PSD को कैसे संपादित करें** सीख लिया है, टेक्स्ट लेयर के बाउंड बॉक्स को प्राप्त करके और **aspose psd java** का उपयोग करके समायोजित करके। कुछ ही कोड लाइनों से आप एक PSD लोड कर सकते हैं, विशिष्ट लेयर को टार्गेट कर सकते हैं, उसके आयाम सत्यापित कर सकते हैं, और सुनिश्चित कर सकते हैं कि टेक्स्ट पूरी तरह फिट हो। अधिक गहरी खोज के लिए—जैसे टेक्स्ट सामग्री को संशोधित करना, इफ़ेक्ट्स लागू करना, या अन्य फ़ॉर्मेट्स में एक्सपोर्ट करना—पूरा Aspose.PSD दस्तावेज़ देखें [यहाँ](https://reference.aspose.com/psd/java/)।

## Frequently Asked Questions
### What is Aspose.PSD?
Aspose.PSD एक शक्तिशाली लाइब्रेरी है जो Adobe Photoshop फ़ाइलों को प्रोग्रामेटिक रूप से हेरफेर करने के लिए उपयोग होती है, जिससे डेवलपर्स PSD दस्तावेज़ बना, संपादित और कनवर्ट कर सकते हैं। यह **batch process psd files** को भी सपोर्ट करती है, जिससे यह बड़े‑पैमाने पर ऑटोमेशन के लिए आदर्श बनती है।

### Do I need Photoshop installed to use Aspose.PSD?
नहीं, Aspose.PSD Adobe Photoshop से स्वतंत्र रूप से काम करता है, जिससे आप सॉफ़्टवेयर स्थापित किए बिना PSD फ़ाइलों को हेरफेर कर सकते हैं।

### Can I use Aspose.PSD with other programming languages?
हाँ, Aspose.PSD विभिन्न प्लेटफ़ॉर्म के लिए उपलब्ध है, जिसमें .NET और Python भी शामिल हैं, साथ ही Java भी।

### Where can I find support for Aspose.PSD?
आप उनके [Aspose फ़ोरम](https://forum.aspose.com/c/psd/34) पर समर्थन और समुदाय चर्चा पा सकते हैं।

### Is there a trial version available for Aspose.PSD?
हाँ! आप एक मुफ्त ट्रायल संस्करण [Aspose वेबसाइट](https://releases.aspose.com/) से डाउनलोड कर सकते हैं।

---

**अंतिम अपडेट:** 2026-02-14  
**परीक्षित संस्करण:** Aspose.PSD for Java (latest)  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}