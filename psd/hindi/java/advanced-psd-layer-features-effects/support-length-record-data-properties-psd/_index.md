---
date: 2026-02-20
description: Aspose.PSD for Java का उपयोग करके लंबाई रिकॉर्ड गुणों को समर्थन देना
  और PSD फ़ाइलों को बैच में प्रोसेस करना सीखें। कोड उदाहरणों के साथ चरण‑दर‑चरण गाइड।
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: लंबाई रिकॉर्ड गुणों का समर्थन – PSD वेक्टर आकारों को संशोधित करें (Java)
url: /hi/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# समर्थन लंबाई रिकॉर्ड प्रॉपर्टीज़ – PSD वेक्टर शैप्स को संशोधित करें (Java)

## परिचय
यदि आपको प्रोग्रामेटिक रूप से **PSD वेक्टर शैप्स को संशोधित** करने की आवश्यकता है, तो Aspose.PSD for Java लाइब्रेरी आपको आपके Java कोड से सीधे Photoshop फ़ाइलों पर पूर्ण नियंत्रण देती है। इस ट्यूटोरियल में हम आपको **लंबाई रिकॉर्ड प्रॉपर्टीज़ को समर्थन** करने के बारे में सब कुछ बताएँगे—वेक्टर शैप लेयर्स को संपादित करने का एक आवश्यक कदम। अंत तक, आप एक PSD खोल सकेंगे, उसके वेक्टर शैप प्रॉपर्टीज़ को समायोजित कर सकेंगे, और अपडेटेड फ़ाइल को अपने IDE से बाहर निकले बिना सहेज सकेंगे। चलिए शुरू करते हैं!

## त्वरित उत्तर
- **“PSD वेक्टर शैप्स को संशोधित” का क्या अर्थ है?** PSD फ़ाइल के भीतर वेक्टर‑आधारित लेयर्स की ज्यामिति, पाथ ऑपरेशन्स, या अन्य प्रॉपर्टीज़ को समायोजित करना।  
- **कौन सी लाइब्रेरी यह संभालती है?** Aspose.PSD for Java।  
- **क्या मुझे लाइसेंस चाहिए?** मूल्यांकन के लिए एक मुफ्त ट्रायल काम करता है; उत्पादन के लिए एक व्यावसायिक लाइसेंस आवश्यक है।  
- **इम्प्लीमेंटेशन में कितना समय लगेगा?** बुनियादी शैप‑संशोधन स्क्रिप्ट के लिए लगभग 10‑15 मिनट।  
- **मुख्य पूर्वापेक्षाएँ क्या हैं?** Java JDK, Aspose.PSD for Java, और एक नमूना PSD फ़ाइल।

## “समर्थन लंबाई रिकॉर्ड प्रॉपर्टीज़” क्या है?
समर्थन लंबाई रिकॉर्ड प्रॉपर्टीज़ का अर्थ है उन `LengthRecord` ऑब्जेक्ट्स तक पहुँच और उन्हें अपडेट करना जो PSD के भीतर प्रत्येक वेक्टर पाथ का वर्णन करते हैं। इन रिकॉर्ड्स को बदलने से आप नियंत्रित कर सकते हैं कि शैप्स कैसे मिलते, प्रतिच्छेदित होते या एक-दूसरे से घटते हैं।

## क्यों Aspose.PSD for Java का उपयोग करें ताकि लंबाई रिकॉर्ड प्रॉपर्टीज़ को समर्थन दिया जा सके?
- **Photoshop की आवश्यकता नहीं** – किसी भी सर्वर पर सीधे PSD फ़ाइलों के साथ काम करें।  
- **समृद्ध API** – लेयर्स, रिसोर्सेज़, और वेक्टर डेटा तक सशक्त टाइप्ड क्लासेज़ के साथ पहुँचें।  
- **क्रॉस‑प्लेटफ़ॉर्म** – Windows, Linux, या macOS पर किसी भी JDK के साथ चलाएँ।  
- **प्रदर्शन‑उन्मुख** – कुशल मेमोरी हैंडलिंग और तेज़ सहेजने की क्रियाएँ।  

## पूर्वापेक्षाएँ
1. **Java Development Kit (JDK)** – [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) से डाउनलोड करें या अपने पसंदीदा पैकेज मैनेजर का उपयोग करें।  
2. **Aspose.PSD for Java** – नवीनतम JAR को [Aspose releases page](https://releases.aspose.com/psd/java/) से प्राप्त करें।  
3. **IDE** – IntelliJ IDEA, Eclipse, या कोई भी Java‑संगत एडिटर।  
4. **एक PSD फ़ाइल** – Photoshop में बनाएं या प्रयोग के लिए एक नमूना PSD प्राप्त करें।  
5. **बेसिक Java ज्ञान** – क्लासेज़, ऑब्जेक्ट्स, और एक्सेप्शन हैंडलिंग की परिचितता।

## पैकेज इम्पोर्ट करें
पहले उन क्लासेज़ को इम्पोर्ट करें जिनकी आपको PSD फ़ाइलों और वेक्टर शैप रिसोर्सेज़ के साथ काम करने के लिए आवश्यकता होगी।

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## चरण 1: अपने स्रोत और आउटपुट डायरेक्टरी सेट करें
परिभाषित करें कि मूल PSD कहाँ स्थित है और संशोधित फ़ाइल कहाँ सहेजनी है।

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## चरण 2: PSD फ़ाइल लोड करें
फ़ाइल खोलने के लिए `Image.load` का उपयोग करें और PSD‑विशिष्ट सुविधाओं के लिए इसे `PsdImage` में कास्ट करें।

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## चरण 3: लेयर में Vsms रिसोर्स खोजें
वेक्टर शैप डेटा `VsmsResource` के अंदर रहता है। दूसरे लेयर के रिसोर्सेज़ में लूप करके इसे खोजें।

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## चरण 4: लंबाई रिकॉर्ड्स तक पहुँचें
प्रत्येक `LengthRecord` एक अलग वेक्टर पाथ का प्रतिनिधित्व करता है। उन रिकॉर्ड्स को प्राप्त करें जिन्हें आप संशोधित करना चाहते हैं।

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## चरण 5: पाथ ऑपरेशन प्रॉपर्टीज़ संशोधित करें
अब आप `PathOperations` को बदलकर **PSD वेक्टर शैप्स को संशोधित** कर सकते हैं। यह निर्धारित करता है कि शैप्स कैसे इंटरैक्ट करते हैं (जैसे, बहिष्करण, प्रतिच्छेदन, घटाव)।

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## चरण 6: संशोधित PSD फ़ाइल सहेजें
अपने बदलावों को नई फ़ाइल में सहेजें।

```java
psdImage.save(outPsdFilePath);
```

## चरण 7: रिसोर्सेज़ को साफ़ करें
मेमोरी मुक्त करने के लिए `PsdImage` को डिस्पोज़ करें।

```java
psdImage.dispose();
```

## समर्थन लंबाई रिकॉर्ड प्रॉपर्टीज़ के साथ PSD फ़ाइलों को बैच प्रोसेस कैसे करें
यदि आपको कई PSD फ़ाइलों पर समान वेक्टर‑शैप समायोजन लागू करने हैं, तो ऊपर दिए गए कोड को एक लूप में रखें जो फ़ाइलों की डायरेक्टरी पर इटररेट करता है। प्रत्येक इटररेशन के लिए `inPsdFilePath` और `outPsdFilePath` को अपडेट करें, और आप **PSD फ़ाइलों को बैच प्रोसेस** प्रभावी रूप से कर पाएँगे।

## सामान्य समस्याएँ और टिप्स
- **नल चेक्स** – पाथ्स तक पहुँचने से पहले हमेशा `resource` `null` नहीं है, यह सत्यापित करें।  
- **पाथ इंडेक्स सीमा** – सुनिश्चित करें कि आप जिन इंडेक्स (`[2]`, `[7]`, `[11]`) का उपयोग करते हैं, वे आपके विशिष्ट PSD में मौजूद हैं।  
- **लाइसेंस** – वैध लाइसेंस के बिना चलाने पर सहेजी गई PSD में वॉटरमार्क एम्बेड हो जाएगा।  

## निष्कर्ष
अब आपके पास Aspose.PSD for Java के साथ लंबाई रिकॉर्ड प्रॉपर्टीज़ को समर्थन देकर **PSD वेक्टर शैप्स को संशोधित** करने का एक पूर्ण, एंड‑टू‑एंड उदाहरण है। चाहे आप एसेट पाइपलाइन को ऑटोमेट कर रहे हों या एक कस्टम डिज़ाइन टूल बना रहे हों, ये API आपको मैन्युअल Photoshop कार्य के बिना वेक्टर लेयर्स को हेरफेर करने की लचीलापन देती हैं। अन्य `PathOperations` के साथ प्रयोग करके या जटिल शैप्स के लिए कई `LengthRecord` संपादन को मिलाकर आगे अन्वेषण करें।

## अक्सर पूछे जाने वाले प्रश्न

**प्रश्न: वह PSD कैसे संभालूँ जिसमें कोई वेक्टर शैप लेयर नहीं है?**  
उत्तर: `VsmsResource` अनुपस्थित रहेगा, इसलिए `resource` `null` रहेगा। एक चेक जोड़ें और संशोधन चरण को स्किप करें या उपयोगकर्ता को सूचित करें।

**प्रश्न: क्या मैं फ़िल कलर या स्ट्रोक चौड़ाई जैसी अन्य प्रॉपर्टीज़ बदल सकता हूँ?**  
उत्तर: हाँ, `LengthRecord` फ़िल, स्ट्रोक, और अपारदर्शिता के अतिरिक्त सेटर्स प्रदान करता है। पूर्ण विवरण के लिए API डॉक्यूमेंटेशन देखें।

**प्रश्न: क्या कई PSD फ़ाइलों को बैच‑प्रोसेस करना संभव है?**  
उत्तर: बिल्कुल। कोड को एक लूप में रखें जो PSD फ़ाइलों की डायरेक्टरी पर इटररेट करता है, और प्रत्येक बार इनपुट व आउटपुट पाथ को समायोजित करें।

**प्रश्न: फ़ाइल पाथ से लोड करते समय क्या मुझे स्ट्रीम्स को मैन्युअली बंद करना चाहिए?**  
उत्तर: `Image.load` मेथड फ़ाइल स्ट्रीम्स को आंतरिक रूप से संभालता है, लेकिन यदि आप `InputStream` से लोड करते हैं, तो उपयोग के बाद उसे बंद करना याद रखें।

**प्रश्न: इन API के लिए Aspose.PSD का कौन सा संस्करण आवश्यक है?**  
उत्तर: `LengthRecord` और `PathOperations` क्लासेज़ Aspose.PSD 20.10 से उपलब्ध हैं। नवीनतम संस्करण का उपयोग करने की सलाह दी जाती है।

---

**अंतिम अपडेट:** 2026-02-20  
**परीक्षित संस्करण:** Aspose.PSD for Java 24.11  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}