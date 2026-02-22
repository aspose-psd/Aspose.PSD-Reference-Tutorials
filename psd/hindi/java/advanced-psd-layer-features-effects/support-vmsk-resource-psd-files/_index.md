---
date: 2026-02-22
description: Aspose.PSD for Java का उपयोग करके जावा में वेक्टर मास्क बनाना सीखें,
  वेक्टर मास्क PSD जोड़ें, और प्रोग्रामेटिक रूप से Vmsk संसाधनों को नियंत्रित करें।
linktitle: Create Vector Mask Java – Vmsk Resource in PSD Files
second_title: Aspose.PSD Java API
title: वेक्टर मास्क जावा बनाएं – PSD फ़ाइलों में Vmsk संसाधन
url: /hi/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

 craft.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# वेक्टर मास्क जावा बनाएं – PSD फ़ाइलों में Vmsk रिसोर्स

## परिचय
यदि आपको Photoshop (PSD) फ़ाइलों के भीतर **वेक्टर मास्क** (Vmsk) रिसोर्स बनाने की आवश्यकता है, तो Aspose.PSD for Java आपको इसे करने का एक साफ़, प्रोग्रामेटिक तरीका प्रदान करता है। चाहे आप एक डिज़ाइन‑ऑटोमेशन टूल बना रहे हों या मौजूदा ग्राफ़िक्स पाइपलाइन में कस्टम मास्क सपोर्ट जोड़ रहे हों, यह ट्यूटोरियल आपको हर चरण से गुज़राता है—PSD लोड करना, Vmsk रिसोर्स पढ़ना, उसकी प्रॉपर्टीज़ को समायोजित करना, और परिणाम को सेव करना। अंत तक, आप वेक्टर मास्क को संभालने, PSD को PNG में बदलने, और फ़ाइल को अतिरिक्त वेक्टर डेटा के साथ विस्तारित करने में सहज हो जाएंगे—सभी **create vector mask java** तकनीकों के साथ।

## त्वरित उत्तर
- **Vmsk रिसोर्स क्या है?** यह PSD फ़ाइल के भीतर संग्रहीत वेक्टर मास्क डेटा है, जो लेयर के लिए जटिल वेक्टर आकार निर्धारित करता है।  
- **कौन सी लाइब्रेरी इसे सपोर्ट करती है?** Aspose.PSD for Java Vmsk रिसोर्स के पूर्ण पढ़ने/लिखने की पहुँच प्रदान करता है।  
- **क्या मुझे लाइसेंस चाहिए?** एक मुफ्त ट्रायल उपलब्ध है; उत्पादन उपयोग के लिए एक व्यावसायिक लाइसेंस आवश्यक है।  
- **क्या मैं संपादित PSD को PNG में बदल सकता हूँ?** हाँ—एक बार सेव होने के बाद, आप PSD को लोड करके उसी API के साथ PNG में एक्सपोर्ट कर सकते हैं।  
- **क्या Maven सपोर्ट उपलब्ध है?** बिल्कुल; Aspose.PSD को Maven डिपेंडेंसी के रूप में जोड़ा जा सकता है (देखें “aspose psd maven” कीवर्ड)।

## वेक्टर मास्क (Vmsk रिसोर्स) क्या है?
एक वेक्टर मास्क (Vmsk) एक गैर‑पिक्सेल‑आधारित मास्क है जो Bézier कर्व्स और पाथ रिकॉर्ड्स का उपयोग करके लेयर पर पारदर्शी और अपारदर्शी क्षेत्रों को परिभाषित करता है। चूँकि यह वेक्टर‑आधारित है, यह गुणवत्ता खोए बिना स्केल होता है—उच्च‑रिज़ॉल्यूशन ग्राफ़िक्स के लिए आदर्श।

## Aspose.PSD के साथ वेक्टर मास्क क्यों बनाएं?
- **ऑटोमेशन:** Photoshop खोले बिना प्रोग्रामेटिक रूप से मास्क जोड़ें या संशोधित करें।  
- **संगतता:** सुनिश्चित करें कि आप द्वारा उत्पन्न प्रत्येक PSD समान मास्क नियमों का पालन करता है।  
- **क्रॉस‑प्लेटफ़ॉर्म:** किसी भी OS पर काम करता है जो Java को सपोर्ट करता है।  
- **इंटीग्रेशन:** अन्य Aspose API (जैसे PSD → PNG रूपांतरण) के साथ मिलाकर एंड‑टू‑एंड वर्कफ़्लो बनाएं।  
- **स्केलेबिलिटी:** वेक्टर मास्क किसी भी आकार पर स्पष्ट रहते हैं, जिससे वे रिस्पॉन्सिव डिज़ाइनों के लिए उपयुक्त होते हैं।

## यह जावा डेवलपर्स के लिए क्यों महत्वपूर्ण है
**create vector mask java** तकनीकों का उपयोग करके आप जटिल ग्राफ़िक्स लॉजिक को सीधे बैक‑एंड सर्विसेज, CI पाइपलाइन, या डेस्कटॉप यूटिलिटीज़ में एम्बेड कर सकते हैं। अब आपको डिज़ाइनर की आवश्यकता नहीं रहेगी जो मैन्युअली मास्क जोड़ता हो; आपका कोड ऑन‑द‑फ़्लाई इन्हें जेनरेट या एडजस्ट कर सकता है, जिससे समय बचता है और मानव त्रुटियों में कमी आती है।

## आवश्यकताएँ
कोड में डुबकी लगाने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

### आपको क्या चाहिए
- **Java Development Kit (JDK):** सुनिश्चित करें कि आपके मशीन पर JDK इंस्टॉल है। यदि नहीं, तो आप इसे [Oracle website](https://www.oracle.com/java/technologies/javase-downloads.html) से डाउनलोड कर सकते हैं।  
- **Aspose.PSD for Java लाइब्रेरी:** PSD फ़ाइलों को मैनेज करने के लिए यह एक शक्तिशाली लाइब्रेरी है। आप इसे [Aspose release page](https://releases.aspose.com/psd/java/) से डाउनलोड कर सकते हैं। जो लोग खरीदने से पहले आज़माना चाहते हैं, उनके लिए [free trial](https://releases.aspose.com/) भी उपलब्ध है।  
- **एक IDE:** कोई भी Java IDE (जैसे IntelliJ IDEA, Eclipse, आदि) इस प्रोजेक्ट के लिए काम करेगी।

### अपने कार्यस्थल की सेटिंग
1. **नया Java प्रोजेक्ट बनाएं** – अपने पसंदीदा IDE को खोलें और एक नया प्रोजेक्ट शुरू करें।  
2. **Aspose लाइब्रेरी जोड़ें** – Aspose JAR डाउनलोड करने के बाद, उसे अपने प्रोजेक्ट के बिल्ड पाथ में जोड़ें ताकि आप सभी PSD‑संबंधित क्लासेज़ तक पहुँच सकें।

पर्यावरण तैयार होने पर, चलिए वास्तविक इम्प्लीमेंटेशन की ओर बढ़ते हैं।

## Java के साथ PSD फ़ाइलों में वेक्टर मास्क कैसे बनाएं
नीचे चरण‑दर‑चरण गाइड दिया गया है। कोड ब्लॉक्स मूल ट्यूटोरियल से अपरिवर्तित हैं; हमने प्रत्येक चरण को स्पष्ट करने के लिए व्याख्यात्मक टेक्स्ट जोड़ा है।

### पैकेज इम्पोर्ट करें
PSD फ़ाइलों पर काम करने से पहले हमें Aspose.PSD लाइब्रेरी से आवश्यक क्लासेज़ इम्पोर्ट करने होंगे।

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

अब जब हमने मंच तैयार कर लिया है, चलिए प्रत्येक ऑपरेशन को देखें।

### चरण 1: अपना PSD फ़ाइल लोड करें
सबसे पहले आपको अपना PSD फ़ाइल लोड करना होगा। यहीं से जादू शुरू होता है।

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- हम `dataDir` को आपके PSD फ़ाइल की डायरेक्टरी पर सेट करते हैं।  
- हम `sourceFileName` स्ट्रिंग बनाते हैं, जिसमें डायरेक्टरी और PSD फ़ाइल का नाम मिलाया जाता है।  
- अंत में, हम `Image.load()` का उपयोग करके PSD फ़ाइल को `PsdImage` ऑब्जेक्ट में लोड करते हैं।

### चरण 2: Vmsk रिसोर्स प्राप्त करें
अब जब हमारा PSD इमेज लोड हो गया है, चलिए Vmsk रिसोर्स को प्राप्त करते हैं।

```java
VmskResource resource = getVmskResource(im);
```

- हम `getVmskResource()` मेथड को कॉल करते हैं जो इमेज से Vmsk रिसोर्स को खोजता और रिट्रीव करता है।

### चरण 3: Vmsk रिसोर्स प्रॉपर्टीज़ को वैलिडेट करें
संशोधन करने से पहले यह सुनिश्चित करना आवश्यक है कि हमारा Vmsk रिसोर्स अपेक्षित स्थिति में है।

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- यहाँ हम Vmsk रिसोर्स की विभिन्न प्रॉपर्टीज़ की जाँच कर रहे हैं। हमें यह सुनिश्चित करना है कि यह डिसेबल्ड, इनवर्टेड या अनलिंक्ड नहीं है, और इसके पास सही संख्या में पाथ्स हैं।

### चरण 4: प्रत्येक पाथ तक पहुँचें और वैलिडेट करें
आइए थोड़ा गहराई में जाएँ और Vmsk रिसोर्स के भीतर पाथ्स का निरीक्षण करें।

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

- हम तीन विशिष्ट पाथ रिकॉर्ड्स को एक्सट्रैक्ट कर रहे हैं और उनके प्रकार व प्रॉपर्टीज़ को वैलिडेट कर रहे हैं ताकि वे हमारी मानदंडों को पूरा करें।

### चरण 5: Vmsk रिसोर्स को एडिट करें
अब हम संशोधन भाग में प्रवेश कर रहे हैं! आप Vmsk रिसोर्स की प्रॉपर्टीज़ को अपनी आवश्यकता अनुसार ट्यून कर सकते हैं।

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- इस ब्लॉक में हम Vmsk रिसोर्स की विभिन्न प्रॉपर्टीज़ को `true` सेट करके टॉगल कर रहे हैं, जिससे मास्क के व्यवहार को PSD फ़ाइल में नियंत्रित किया जा सकता है।

### चरण 6: Bezier Knot पॉइंट्स को संशोधित करें
Bezier नॉट्स वेक्टर पाथ्स के लिए महत्वपूर्ण होते हैं। चलिए यहाँ कुछ मान बदलते हैं।

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- हम विशिष्ट `BezierKnotRecord` पाथ्स तक पहुँच रहे हैं और उनके पॉइंट्स को बदल रहे हैं, जिससे वेक्टर मास्क का आकार संभावित रूप से बदल सकता है।

### चरण 7: संशोधित PSD फ़ाइल को सेव करें
सभी एडिट्स पूर्ण होने के बाद, संशोधित PSD फ़ाइल को सेव करने का समय है।

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- हम एक्सपोर्टेड PSD फ़ाइल के पाथ को सेट करते हैं और फिर `im.save()` को कॉल करके इन बदलावों को नई फ़ाइल में लिखते हैं।

### चरण 8: रिसोर्सेज़ को क्लीन अप करें
अंत में, हमें इमेज को सही तरीके से डिस्पोज़ करना चाहिए ताकि रिसोर्सेज़ मुक्त हो सकें।

```java
im.dispose();
```

- किसी भी रिसोर्स को डिस्पोज़ करना एक अच्छी प्रैक्टिस है, विशेषकर लम्बे‑चलाने वाले प्रोसेसेस में मेमोरी लीक्स से बचने के लिए।

## सामान्य समस्याएँ और समाधान
| समस्या | क्यों होता है | समाधान |
|-------|----------------|------------|
| **`VmskResource` नहीं मिला** | PSD में वेक्टर मास्क लेयर नहीं है। | सुनिश्चित करें कि स्रोत PSD में वेक्टर मास्क है या कोड चलाने से पहले Photoshop में मैन्युअली एक जोड़ें। |
| **पाथ एक्सेस पर `ArrayIndexOutOfBoundsException`** | अपेक्षित पाथ रिकॉर्ड्स की संख्या अलग है। | `resource.getPaths().length` की जाँच करें और इंडेक्स उपयोग को तदनुसार समायोजित करें। |
| **लाइसेंस एक्सेप्शन** | वैध Aspose.PSD लाइसेंस के बिना चलाया गया। | ट्रायल या खरीदा हुआ लाइसेंस लागू करें: `License license = new License(); license.setLicense("Aspose.PSD.lic");` |
| **मेमोरी लीक्स** | लम्बे‑चलाने वाले प्रोसेसेस में इमेज डिस्पोज़ नहीं हुई। | हमेशा `im.dispose()` को `finally` ब्लॉक में कॉल करें या यदि समर्थित हो तो try‑with‑resources का उपयोग करें। |

## अक्सर पूछे जाने वाले प्रश्न

**प्रश्न:** मैं मौजूदा लेयर में नया वेक्टर मास्क कैसे जोड़ूँ?  
**उत्तर:** एक `VmskResource` बनाएं, आवश्यक पाथ रिकॉर्ड्स (जैसे `BezierKnotRecord`) से इसे पॉप्युलेट करें, और इसे लेयर के रिसोर्सेज़ कलेक्शन में अटैच करें।

**प्रश्न:** क्या मैं संपादित PSD को सीधे PNG में बदल सकता हूँ बिना Photoshop खोले?  
**उत्तर:** हाँ—PSD को सेव करने के बाद, उसे फिर से `Image.load()` से लोड करें और `im.save("output.png")` के साथ PNG फॉर्मेट निर्दिष्ट करके एक्सपोर्ट करें।

**प्रश्न:** क्या इसे CI/CD पाइपलाइन में ऑटोमेट किया जा सकता है?  
**उत्तर:** बिल्कुल। चूँकि प्रक्रिया पूरी तरह Java में है, आप इसे Maven/Gradle बिल्ड, Docker कंटेनर, या किसी भी Java‑सपोर्टेड CI सिस्टम में एम्बेड कर सकते हैं।

**प्रश्न:** कौन‑से Aspose.PSD संस्करण Java 11+ के साथ संगत हैं?  
**उत्तर:** सभी हालिया रिलीज़ (2024‑2025) Java 8 और ऊपर, जिसमें Java 11, 17, और नए LTS संस्करण शामिल हैं, को सपोर्ट करती हैं।

**प्रश्न:** विकास बिल्ड्स के लिए लाइसेंस आवश्यक है क्या?  
**उत्तर:** विकास और परीक्षण के लिए एक मुफ्त एवाल्यूएशन लाइसेंस काम करता है। उत्पादन डिप्लॉयमेंट के लिए व्यावसायिक लाइसेंस आवश्यक है।

---

**अंतिम अपडेट:** 2026-02-22  
**परीक्षित संस्करण:** Aspose.PSD 24.11 for Java  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}