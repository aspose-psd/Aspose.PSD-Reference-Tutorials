---
date: 2025-12-18
description: Aspose.PSD for Java का उपयोग करके PSD फ़ाइलों में वेक्टर मास्क (Vmsk
  रिसोर्स) कैसे बनाएं, सीखें। यह चरण‑दर‑चरण ट्यूटोरियल आपको वेक्टर मास्क जोड़ना, PSD
  को PNG में बदलना और अधिक दिखाता है।
linktitle: Create Vector Mask (Vmsk Resource) in PSD Files with Java
second_title: Aspose.PSD Java API
title: जावा के साथ PSD फ़ाइलों में वेक्टर मास्क (Vmsk रिसोर्स) बनाएं
url: /hi/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java के साथ PSD फ़ाइलों में वेक्टर मास्क (Vmsk रिसोर्स) बनाएं

## परिचय
यदि आपको Photoshop (PSD) फ़ाइलों के अंदर **वेक्टर मास्क** (Vmsk) रिसोर्स बनाना है, तो Aspose.PSD for Java आपको एक साफ़, प्रोग्रामेटिक तरीका प्रदान करता है। चाहे आप एक डिज़ाइन‑ऑटोमेशन टूल बना रहे हों या मौजूदा ग्राफ़िक्स पाइपलाइन में कस्टम मास्क सपोर्ट जोड़ रहे हों, यह ट्यूटोरियल आपको हर कदम से गुज़राता है—PSD लोड करना, Vmsk रिसोर्स पढ़ना, उसकी प्रॉपर्टीज़ को ट्यून करना, और परिणाम को सेव करना। अंत तक, आप वेक्टर मास्क को हैंडल करने, PSD को PNG में कनवर्ट करने, और फ़ाइल में अतिरिक्त वेक्टर डेटा जोड़ने में सहज हो जाएंगे।

## हाजिर जवाब
- **Vmsk रिसोर्स क्या है?** यह PSD फ़ाइल के अंदर संग्रहीत वेक्टर मास्क डेटा है, जो लेयर के लिए जटिल वेक्टर शैप्स को परिभाषित करता है।  
- **कौन सी लाइब्रेरी इसे सपोर्ट करती है?** Aspose.PSD for Java पूर्ण पढ़ने/लिखने की पहुँच प्रदान करती है।  
- **क्या मुझे लाइसेंस चाहिए?** एक फ्री ट्रायल उपलब्ध है; प्रोडक्शन उपयोग के लिए व्यावसायिक लाइसेंस आवश्यक है।  
- **क्या मैं संपादित PSD को PNG में कनवर्ट कर सकता हूँ?** हाँ—सेव करने के बाद, आप PSD को लोड करके उसी API से PNG में एक्सपोर्ट कर सकते हैं।  
- **क्या Maven सपोर्ट उपलब्ध है?** बिल्कुल; Aspose.PSD को Maven डिपेंडेंसी के रूप में जोड़ा जा सकता है (देखें “aspose psd maven” कीवर्ड)।

## वेक्टर मास्क (Vmsk रिसोर्स) क्या है?
वेक्टर मास्क (Vmsk) एक नॉन‑पिक्सेल‑आधारित मास्क है जो Bézier कर्व्स और पाथ रिकॉर्ड्स का उपयोग करके लेयर पर ट्रांसपेरेंट और ओपैक क्षेत्रों को परिभाषित करता है। चूँकि यह वेक्टर‑आधारित है, यह क्वालिटी खोए बिना स्केल होता है—उच्च‑रिज़ॉल्यूशन ग्राफ़िक्स के लिए परफेक्ट।

## Aspose.PSD के साथ वेक्टर मास्क क्यों बनाएं?
- **Automation:** Photoshop खोले बिना प्रोग्रामेटिक रूप से मास्क जोड़ें या संशोधित करें।  
- **Consistency:** सुनिश्चित करें कि आप द्वारा जेनरेट किया गया हर PSD समान मास्क नियमों का पालन करता है।  
- **Cross‑platform:** किसी भी OS पर काम करता है जो Java सपोर्ट करता है।  
- **Integration:** अन्य Aspose APIs (जैसे PSD → PNG कनवर्ज़न) के साथ मिलाकर एंड‑टू‑एंड वर्कफ़्लो बनाएं।

## पूर्वापेक्षाएँ
कोड में डुबकी लगाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

### जिसकी आपको जरूरत है
- Java Development Kit (JDK): सुनिश्चित करें कि आपके मशीन पर JDK इंस्टॉल है। यदि नहीं, तो इसे [Oracle वेबसाइट](https://www.oracle.com/java/technologies/javase-downloads.html) से डाउनलोड कर सकते हैं।  
- Aspose.PSD for Java Library: PSD फ़ाइलों को मैनेज करने के लिए यह एक पावरफ़ुल लाइब्रेरी है। इसे आप [Aspose रिलीज़ पेज](https://releases.aspose.com/psd/java/) से डाउनलोड कर सकते हैं। जो लोग खरीदने से पहले ट्राय करना चाहते हैं, उनके लिए [फ्री ट्रायल](https://releases.aspose.com/) भी उपलब्ध है।  
- एक IDE: Java के लिए कोई भी IDE (जैसे IntelliJ IDEA, Eclipse, आदि) इस प्रोजेक्ट के लिए काम करेगा।

### अपना वर्कस्पेस सेट अप करना
1. **एक नया Java प्रोजेक्ट बनाएं** – अपने पसंदीदा IDE को खोलें और एक नया प्रोजेक्ट शुरू करें।
2. **Aspose Library जोड़ें** – Aspose JAR डाउनलोड करने के बाद, उसे अपने प्रोजेक्ट के बिल्ड पाथ में जोड़ें ताकि आप सभी PSD‑संबंधित क्लासेज़ तक पहुँच सकें।

पर्यावरण तैयार होने पर, चलिए वास्तविक इम्प्लीमेंटेशन की ओर बढ़ते हैं।

## Java के साथ PSD फ़ाइलों में वेक्टर मास्क कैसे बनाएं
नीचे चरण‑दर‑चरण गाइड दिया गया है। कोड ब्लॉक्स मूल ट्यूटोरियल से अपरिवर्तित हैं; हमने प्रत्येक कदम को स्पष्ट करने के लिए व्याख्यात्मक टेक्स्ट जोड़ा है।

## पैकेज आयात करें
PSD फ़ाइलों पर काम करने से पहले, हमें Aspose.PSD लाइब्रेरी से आवश्यक क्लासेज़ इम्पोर्ट करने होंगे।

```java
import com.aspose.psd.Image;
import com.aspose.psd.Point;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VmskResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.BezierKnotRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.InitialFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathType;
```

अब जब हमने सेटअप कर लिया है, चलिए प्रत्येक ऑपरेशन को देखते हैं।

## स्टेप 1: अपनी PSD फ़ाइल लोड करें
सबसे पहले आपको अपना PSD फ़ाइल लोड करना होगा। यहीं से सब कुछ शुरू होता है।

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- हम `dataDir` को आपके PSD फ़ाइल की डायरेक्टरी पर सेट करते हैं।  
- हम `sourceFileName` स्ट्रिंग बनाते हैं, जिसमें डायरेक्टरी और PSD फ़ाइल का नाम जोड़ा जाता है।  
- अंत में, `Image.load()` का उपयोग करके PSD फ़ाइल को `PsdImage` ऑब्जेक्ट में लोड करते हैं।

## स्टेप 2: Vmsk रिसोर्स रिट्रीव करें
अब जब हमारा PSD इमेज लोड हो गया है, चलिए Vmsk रिसोर्स को प्राप्त करते हैं।

```java
VmskResource resource = getVmskResource(im);
```

- हम `getVmskResource()` मेथड को कॉल करते हैं, जो इमेज से Vmsk रिसोर्स को खोजता और रिट्रीव करता है।

## स्टेप 3: Vmsk रिसोर्स प्रॉपर्टीज़ को वैलिडेट करें
संशोधन करने से पहले, यह सुनिश्चित करना आवश्यक है कि हमारा Vmsk रिसोर्स अपेक्षित स्थिति में है।

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- यहाँ हम Vmsk रिसोर्स की विभिन्न प्रॉपर्टीज़ की जाँच कर रहे हैं। हमें यह पुष्टि करनी है कि यह डिसेबल्ड, इनवर्टेड या अनलिंक्ड नहीं है, और इसमें सही संख्या में पाथ्स हैं।

## स्टेप 4: हर पाथ को एक्सेस करें और वैलिडेट करें
आइए थोड़ा और गहराई में जाएँ और Vmsk रिसोर्स के भीतर पाथ्स को इंस्पेक्ट करें।

```java
PathFillRuleRecord pathFillRule = (PathFillRuleRecord) resource.getPaths()[0];
InitialFillRuleRecord initialFillRule = (InitialFillRuleRecord) resource.getPaths()[1];
LengthRecord subpathLength = (LengthRecord) resource.getPaths()[2];
if (pathFillRule.getType() != VectorPathType.PathFillRuleRecord ||
	initialFillRule.getType() != VectorPathType.InitialFillRuleRecord ||
	initialFillRule.isFillStartsWithAllPixels() != false ||
	subpathLength.getType() != VectorPathType.ClosedSubpathLengthRecord ||
	subpathLength.isClosed() != true) {
	throw new RuntimeException("VmskResource paths were read wrong");
}
```

- हम तीन विशिष्ट पाथ रिकॉर्ड्स को एक्सट्रैक्ट कर रहे हैं और उनके टाइप व प्रॉपर्टीज़ को वैलिडेट कर रहे हैं ताकि वे हमारी शर्तों को पूरा करें।

## स्टेप 5: Vmsk रिसोर्स को एडिट करें
अब हम संशोधन भाग में प्रवेश कर रहे हैं! आप अपनी आवश्यकता अनुसार Vmsk रिसोर्स की प्रॉपर्टीज़ को ट्यून कर सकते हैं।

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- इस ब्लॉक में हम Vmsk रिसोर्स की विभिन्न प्रॉपर्टीज़ को `true` सेट कर रहे हैं, जिससे हम मास्क के व्यवहार को नियंत्रित कर सकते हैं।

## स्टेप 6: बेज़ियर नॉट पॉइंट्स को मॉडिफ़ाई करें
Bezier नॉट्स वेक्टर पाथ्स के लिए महत्वपूर्ण होते हैं। चलिए यहाँ कुछ वैल्यू बदलते हैं।

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- हम विशिष्ट `BezierKnotRecord` पाथ्स को एक्सेस कर उनके पॉइंट्स को बदल रहे हैं, जिससे वेक्टर मास्क का आकार बदल सकता है।

## स्टेप 7: मॉडिफाइड PSD फ़ाइल सेव करें
सभी एडिट्स पूर्ण होने के बाद, संशोधित PSD फ़ाइल को सेव करने का समय है।

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- हम एक्सपोर्टेड PSD फ़ाइल का पाथ सेट करते हैं और फिर `im.save()` को कॉल करके इस नई फ़ाइल में बदलाव लिखते हैं।

## स्टेप 8: रिसोर्स साफ़ करें
अंत में, हमें इमेज को डिस्पोज़ करके रिसोर्सेज़ को फ्री करना चाहिए।

```java
im.dispose();
```

- किसी भी रिसोर्स को डिस्पोज़ करना एक अच्छी प्रैक्टिस है, जिससे आपके एप्लिकेशन में मेमोरी लीक्स से बचा जा सके।

## निष्कर्ष
बधाई हो! आपने Aspose.PSD for Java का इस्तेमाल करके PSD सेक्शन में **वेक्टर मास्क** (Vmsk) रिसोर्स बनाने की विस्तृत प्रक्रिया पूरी कर ली है। इमेज लोड करने, Vmsk रिसोर्स को रिट्रीव और वैलिडेट करने, उसके प्रॉपर्टीज़ को एडिट करने, और अधिकृत PSD को सेव करने तक, अब आपके पास<extra_id_1> मास्क इंडेक्स को ऑटोमेट करने की ठोस नींव है। इन तकनीकों का इस्तेमाल करके आप अपनी डिज़ाइन पाइपलाइनों को समृद्ध कर सकते हैं, अन्य Aspose APIs (जैसे PSD को PNG में कनवर्ट करना) के साथ इंटीग्रेट कर सकते हैं, या कस्टम ग्राफ़िक्स टूल बना सकते हैं।

## अक्सर पूछे जाने वाले सवाल
**Q: मैं किसी मौजूदा लेयर में नया वेक्टर मास्क कैसे जोड़ूँ?**
A: `VmskResource` बनाएँ, आवश्यक पाथ रिकॉर्ड्स (जैसे `BezierKnotRecord`) से पॉपुलेट करें, और इसे लेयर की रिसोर्सेज़ कलेक्शन में अटैच करें।

**Q: क्या मैं एडिट किए गए PSD को Photoshop खोले बिना सीधे PNG में बदल सकता हूँ?**
A: हाँ—PSD को सेव करने के बाद, `Image.load()` से फिर लोड करें और `im.save("output.png")` के साथ PNG फ़ॉर्मैट लिंक करके एक्सपोर्ट करें।

**Q: क्या CI/CD पाइपलाइन में इसे ऑटोमेट करने का कोई तरीका है?**
A: बिल्कुल। प्रोसेस पूरी तरह Java में है, आप इसे Maven/Gradle Build, Docker कंटेनर, या किसी भी Java सपोर्ट करने वाले CI सिस्टम में एम्बेड कर सकते हैं।

**Q: Aspose.PSD के कौन से वर्शन Java 11+ के साथ कम्पैटिबल हैं?**
A: सभी बचे हुए रिलीज़ (2024‑2025) Java 8 और ऊपर, जिसमें Java 11, 17, और नए LTS वर्ज़न शामिल हैं, को सपोर्ट करती हैं।

**Q: क्या मुझे डेवलपमेंट बिल्ड के लिए लाइसेंस चाहिए?**
A: डेवलपमेंट और टेस्टिंग के लिए फ्री इवैल्यूएशन लाइसेंस काम करता है। प्रोडक्शन डिप्लॉयमेंट के लिए प्रोफेशनल लाइसेंस ज़रूरी है।
---

**Last Updated:** 2025-12-18  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
