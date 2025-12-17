---
date: 2025-12-17
description: Aspose.PSD for Java का उपयोग करके लंबाई रिकॉर्ड डेटा प्रॉपर्टीज़ को सपोर्ट
  करके PSD वेक्टर शैप्स को कैसे संशोधित करें, सीखें। कोड उदाहरणों के साथ चरण‑दर‑चरण
  गाइड।
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: PSD वेक्टर आकारों को कैसे संशोधित करें – जावा में सपोर्ट लंबाई रिकॉर्ड डेटा
  गुण
url: /hi/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# PSD में Length Record डेटा प्रॉपर्टीज़ का समर्थन - Java

## परिचय
यदि आपको प्रोग्रामेटिक रूप से **modify PSD vector shapes** करने की आवश्यकता है, तो Aspose.PSD for Java लाइब्रेरी आपको आपके Java कोड से सीधे Photoshop फ़ाइलों पर पूर्ण नियंत्रण देती है। इस ट्यूटोरियल में हम वह सब कुछ कवर करेंगे जो आपको length record डेटा प्रॉपर्टीज़ को सपोर्ट करने के लिए चाहिए—एक आवश्यक कदम जब आप वेक्टर शेप लेयर्स को एडिट करना चाहते हैं। अंत तक, आप एक PSD खोल सकेंगे, उसकी वेक्टर शेप प्रॉपर्टीज़ को समायोजित कर सकेंगे, और अपडेटेड फ़ाइल को अपने IDE से बाहर निकले बिना सेव कर सकेंगे। चलिए शुरू करते हैं!

## त्वरित उत्तर
- **“modify PSD vector shapes” का क्या अर्थ है?** PSD फ़ाइल के भीतर वेक्टर‑आधारित लेयर्स की ज्यामिति, पाथ ऑपरेशन्स, या अन्य प्रॉपर्टीज़ को समायोजित करना।  
- **कौन सी लाइब्रेरी इसे संभालती है?** Aspose.PSD for Java।  
- **क्या मुझे लाइसेंस चाहिए?** मूल्यांकन के लिए एक फ्री ट्रायल काम करता है; उत्पादन के लिए एक कमर्शियल लाइसेंस आवश्यक है।  
- **इम्प्लीमेंटेशन में कितना समय लगेगा?** बेसिक शेप‑मॉडिफिकेशन स्क्रिप्ट के लिए लगभग 10‑15 मिनट।  
- **मुख्य पूर्वापेक्षाएँ क्या हैं?** Java JDK, Aspose.PSD for Java, और एक सैंपल PSD फ़ाइल।

## “modify PSD vector shapes” क्या है?
PSD वेक्टर शेप्स को संशोधित करने में अंतर्निहित वेक्टर पाथ डेटा—जैसे length records और पाथ ऑपरेशन्स—को बदलना शामिल है, ताकि शेप्स की दृश्य उपस्थिति उसी अनुसार अपडेट हो सके। यह स्वचालित ग्राफिक्स पाइपलाइन, बैच प्रोसेसिंग, या कस्टम डिज़ाइन टूल्स के लिए विशेष रूप से उपयोगी है।

## PSD वेक्टर शेप्स को संशोधित करने के लिए Aspose.PSD for Java क्यों उपयोग करें?
- **No Photoshop required** – किसी भी सर्वर पर सीधे PSD फ़ाइलों के साथ काम करें।  
- **Rich API** – लेयर्स, रिसोर्सेज़, और वेक्टर डेटा तक स्ट्रॉन्गली टाइप्ड क्लासेज़ के साथ पहुंचें।  
- **Cross‑platform** – Windows, Linux, या macOS पर किसी भी JDK के साथ चलाएँ।  
- **Performance‑focused** – मेमोरी हैंडलिंग में कुशल और तेज़ सेव ऑपरेशन्स।

## पूर्वापेक्षाएँ
1. **Java Development Kit (JDK)** – डाउनलोड करें [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) या अपने पसंदीदा पैकेज मैनेजर का उपयोग करें।  
2. **Aspose.PSD for Java** – नवीनतम JAR प्राप्त करें [Aspose releases page](https://releases.aspose.com/psd/java/) से।  
3. **IDE** – IntelliJ IDEA, Eclipse, या कोई भी Java‑compatible एडिटर।  
4. **एक PSD फ़ाइल** – Photoshop में बनाएं या प्रयोग के लिए एक सैंपल PSD प्राप्त करें।  
5. **बेसिक Java नॉलेज** – क्लासेज़, ऑब्जेक्ट्स, और एक्सेप्शन हैंडलिंग से परिचित हों।

## पैकेज इम्पोर्ट करें
पहले उन क्लासेज़ को इम्पोर्ट करें जिनकी आपको PSD फ़ाइलों और वेक्टर शेप रिसोर्सेज़ के साथ काम करने के लिए आवश्यकता होगी।

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## चरण 1: अपने स्रोत और आउटपुट डायरेक्टरी सेट करें
परिभाषित करें कि मूल PSD कहाँ स्थित है और संशोधित फ़ाइल कहाँ सेव करनी है।

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## चरण 2: PSD फ़ाइल लोड करें
फ़ाइल खोलने के लिए `Image.load` का उपयोग करें और PSD‑विशिष्ट फीचर्स के लिए इसे `PsdImage` में कास्ट करें।

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## चरण 3: लेयर में Vsms रिसोर्स खोजें
वेक्टर शेप डेटा `VsmsResource` के अंदर रहता है। इसे खोजने के लिए दूसरे लेयर के रिसोर्सेज़ पर लूप करें।

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## चरण 4: Length Records तक पहुंचें
प्रत्येक `LengthRecord` एक अलग वेक्टर पाथ का प्रतिनिधित्व करता है। उन रिकॉर्ड्स को प्राप्त करें जिन्हें आप संशोधित करना चाहते हैं।

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## चरण 5: Path Operation प्रॉपर्टीज़ संशोधित करें
अब आप **modify PSD vector shapes** कर सकते हैं उनके `PathOperations` को बदलकर। यह निर्धारित करता है कि शेप्स कैसे इंटरैक्ट करते हैं (जैसे exclusion, intersection, subtraction)।

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## चरण 6: संशोधित PSD फ़ाइल सहेजें
अपनी बदलावों को एक नई फ़ाइल में सहेजें।

```java
psdImage.save(outPsdFilePath);
```

## चरण 7: रिसोर्सेज़ को साफ़ करें
मेमोरी मुक्त करने के लिए `PsdImage` को डिस्पोज़ करें।

```java
psdImage.dispose();
```

## सामान्य समस्याएँ और टिप्स
- **Null checks** – पाथ्स तक पहुंचने से पहले हमेशा सत्यापित करें कि `resource` `null` नहीं है।  
- **Path index bounds** – सुनिश्चित करें कि आप जिन इंडेक्स (`[2]`, `[7]`, `[11]`) का उपयोग कर रहे हैं, वे आपके विशिष्ट PSD में मौजूद हैं।  
- **License** – वैध लाइसेंस के बिना चलाने पर सेव्ड PSD में वॉटरमार्क एम्बेड हो जाएगा।  

## निष्कर्ष
आपके पास अब एक पूर्ण, एंड‑टू‑एंड उदाहरण है कि कैसे **modify PSD vector shapes** करके Aspose.PSD for Java के साथ length record डेटा प्रॉपर्टीज़ को सपोर्ट किया जा सकता है। चाहे आप एसेट पाइपलाइन को ऑटोमेट कर रहे हों या कस्टम डिज़ाइन टूल बना रहे हों, ये API आपको मैन्युअल Photoshop काम किए बिना वेक्टर लेयर्स को मैनीपुलेट करने की लचीलापन देती हैं। अन्य `PathOperations` के साथ प्रयोग करके या कई `LengthRecord` एडिट्स को मिलाकर जटिल शेप्स बनाकर आगे अन्वेषण करें।

## अक्सर पूछे जाने वाले प्रश्न
### Aspose.PSD for Java क्या है?
Aspose.PSD for Java एक लाइब्रेरी है जो डेवलपर्स को Java का उपयोग करके प्रोग्रामेटिक रूप से Photoshop PSD फ़ाइलों को मैनीपुलेट और काम करने की अनुमति देती है।

### क्या मैं Aspose.PSD को एक फ्री प्रोजेक्ट में उपयोग कर सकता हूँ?
हां, आप Aspose वेबसाइट पर उपलब्ध ट्रायल संस्करण का उपयोग करके लाइब्रेरी को मुफ्त में आज़मा सकते हैं।

### मैं PSD फ़ाइलों में कौन-कौन से संशोधन कर सकता हूँ?
आप लेयर्स, शेप्स, टेक्स्ट, पाथ ऑपरेशन्स, और PSD फ़ाइलों के भीतर बहुत कुछ मैनीपुलेट कर सकते हैं।

### क्या Aspose.PSD अन्य प्रोग्रामिंग भाषाओं के साथ संगत है?
हां, Aspose विभिन्न प्रोग्रामिंग भाषाओं के लिए लाइब्रेरी प्रदान करता है, जिसमें .NET और Python शामिल हैं।

### Aspose.PSD की डॉक्यूमेंटेशन कहाँ मिल सकती है?
आप पूरी डॉक्यूमेंटेशन [here](https://reference.aspose.com/psd/java/) पर एक्सेस कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

**Q: वह PSD कैसे हैंडल करूँ जिसमें कोई वेक्टर शेप लेयर नहीं है?**  
A: `VsmsResource` अनुपस्थित रहेगा, इसलिए `resource` `null` रहेगा। एक चेक जोड़ें और मॉडिफिकेशन स्टेप को स्किप करें या उपयोगकर्ता को सूचित करें।

**Q: क्या मैं फ़िल कलर या स्ट्रोक विड्थ जैसी अन्य प्रॉपर्टीज़ बदल सकता हूँ?**  
A: हां, `LengthRecord` फ़िल, स्ट्रोक और अपासिटी के लिए अतिरिक्त सेटर्स प्रदान करता है। पूर्ण विवरण के लिए API डॉक्यूमेंट देखें।

**Q: क्या कई PSD फ़ाइलों को बैच‑प्रोसेस करना संभव है?**  
A: बिल्कुल। कोड को एक लूप में रैप करें जो PSD फ़ाइलों की डायरेक्टरी पर इटररेट करे, प्रत्येक बार इनपुट और आउटपुट पाथ को समायोजित करे।

**Q: क्या फ़ाइल पाथ से लोड करते समय स्ट्रीम्स को मैन्युअली बंद करना पड़ता है?**  
A: `Image.load` मेथड फ़ाइल स्ट्रीम्स को आंतरिक रूप से हैंडल करता है, लेकिन यदि आप `InputStream` से लोड कर रहे हैं, तो उपयोग के बाद उसे बंद करना याद रखें।

**Q: इन API के लिए कौन सा Aspose.PSD संस्करण आवश्यक है?**  
A: `LengthRecord` और `PathOperations` क्लासेज़ Aspose.PSD 20.10 से उपलब्ध हैं। नवीनतम संस्करण का उपयोग करने की सलाह दी जाती है।

---

**Last Updated:** 2025-12-17  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}