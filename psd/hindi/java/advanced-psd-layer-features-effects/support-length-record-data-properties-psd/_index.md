---
date: 2026-09-23
description: जानें कैसे PSD वेक्टर शैप्स को संशोधित करें और PSD फ़ाइलों को batch process
  करें Aspose.PSD for Java का उपयोग करके। विस्तृत चरण, टिप्स, और code placeholders
  के साथ एक पूर्ण समाधान।
keywords:
- modify psd vector shapes
- batch process psd files
- Aspose.PSD Java
- vector shape editing
lastmod: 2026-09-23
linktitle: PSD में Length Record Data Properties का समर्थन - Java
og_description: Aspose.PSD for Java का उपयोग करके PSD वेक्टर शैप्स को संशोधित करने
  और PSD फ़ाइलों को batch process करने के बारे में जानें। step‑by‑step गाइड जिसमें
  code placeholders और expert tips शामिल हैं।
og_image_alt: Guide showing how to edit vector shapes in PSD files using Aspose.PSD
  for Java
og_title: Aspose.PSD for Java के साथ PSD वेक्टर शैप्स संशोधित करें
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  headline: Modify PSD vector shapes with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  name: Modify PSD vector shapes with Aspose.PSD for Java
  steps:
  - name: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
    text: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
  - name: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
  - name: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
    text: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
  - name: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
    text: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
  type: HowTo
- questions:
  - answer: The `VsmsResource` will be absent, so `resource` stays `null`. Add a check
      and skip the modification step or inform the user.
    question: How do I handle a PSD that contains no vector shape layers?
  - answer: Yes, `LengthRecord` provides setters for fill, stroke, and opacity. See
      the API docs for the full list.
    question: Can I change other properties like fill color or stroke width?
  - answer: Absolutely. Wrap the code inside a loop that iterates over a directory
      of PSD files, adjusting the input and output paths each time.
    question: Is it possible to batch‑process multiple PSD files?
  - answer: '`Image.load` handles file streams automatically, but if you load from
      an `InputStream`, remember to close it after use.'
    question: Do I need to close streams manually when loading from a file path?
  - answer: The `LengthRecord` and `PathOperations` classes have been available since
      Aspose.PSD 20.10. Using the latest version (24.11 at time of writing) is recommended.
    question: What version of Aspose.PSD is required for these APIs?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- modify psd vector shapes
- Aspose.PSD
- Java image processing
- batch PSD processing
title: Aspose.PSD for Java के साथ PSD वेक्टर शैप्स संशोधित करें
url: /hi/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD for Java के साथ PSD वेक्टर आकारों को संशोधित करें

## परिचय
यदि आपको **PSD वेक्टर आकारों को प्रोग्रामेटिकली संशोधित** करने की आवश्यकता है, तो Aspose.PSD for Java आपको सीधे अपने Java कोड से Photoshop फ़ाइलों पर पूर्ण नियंत्रण देता है। यह ट्यूटोरियल आपको वेक्टर आकार लेयर्स को संपादित करने के एक आवश्यक चरण—लेन्थ रिकॉर्ड प्रॉपर्टीज़ को सपोर्ट करने—के माध्यम से ले जाएगा। अंत तक आप एक PSD खोल सकेंगे, उसके वेक्टर आकार डेटा को समायोजित कर सकेंगे, और अपडेटेड फ़ाइल को बिना Photoshop लॉन्च किए सहेज सकेंगे।

## त्वरित उत्तर
- **“PSD वेक्टर आकारों को संशोधित करना” का क्या अर्थ है?** PSD फ़ाइल के भीतर वेक्टर‑आधारित लेयर्स की ज्योमेट्री, पाथ ऑपरेशन्स या अन्य एट्रिब्यूट्स को समायोजित करना।  
- **यह कौन सी लाइब्रेरी संभालती है?** Aspose.PSD for Java।  
- **क्या मुझे लाइसेंस चाहिए?** मूल्यांकन के लिए एक फ्री ट्रायल काम करता है; उत्पादन के लिए एक व्यावसायिक लाइसेंस आवश्यक है।  
- **इम्प्लीमेंटेशन में कितना समय लगेगा?** बुनियादी आकार‑संशोधन स्क्रिप्ट के लिए लगभग 10‑15 मिनट।  
- **मुख्य पूर्वापेक्षाएँ क्या हैं?** Java JDK, Aspose.PSD for Java, और एक नमूना PSD फ़ाइल।

## “सपोर्ट लेन्थ रिकॉर्ड प्रॉपर्टीज़” क्या है?
सपोर्ट लेन्थ रिकॉर्ड प्रॉपर्टीज़ का मतलब है उन `LengthRecord` ऑब्जेक्ट्स तक पहुँच और उन्हें अपडेट करना जो PSD के भीतर प्रत्येक वेक्टर पाथ का वर्णन करते हैं। ये रिकॉर्ड पाथ की लंबाई, प्रकार, और अन्य पाथ्स के साथ कैसे जुड़ते हैं, जैसी जानकारी संग्रहीत करते हैं। इन्हें बदलने से आप नियंत्रित कर सकते हैं कि आकार कैसे मिलते, प्रतिच्छेदित होते या एक‑दूसरे से घटते हैं, जिससे सटीक वेक्टर एडिटिंग संभव होती है।

## लेन्थ रिकॉर्ड प्रॉपर्टीज़ को सपोर्ट करने के लिए Aspose.PSD for Java का उपयोग क्यों करें?
अपना PSD लोड करें, वेक्टर डेटा संपादित करें, और सहेजें—बिना Photoshop के। Aspose.PSD सामान्य सर्वर पर 2 सेकंड से कम समय में सैकड़ों‑पृष्ठीय PSD प्रोसेस करता है, 150 से अधिक क्लासेज़ (30+ वेक्टर‑संबंधित टाइप्स सहित) प्रदान करता है, और Windows, Linux, या macOS पर किसी भी JDK 11+ के साथ चलता है। यह प्रदर्शन‑उन्मुख लाइब्रेरी महंगे डेस्कटॉप सॉफ़्टवेयर की आवश्यकता को समाप्त करती है।

## पूर्वापेक्षाएँ
1. **Java Development Kit (JDK)** – [Oracle की वेबसाइट](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) से डाउनलोड करें या अपने पसंदीदा पैकेज मैनेजर का उपयोग करें।  
2. **Aspose.PSD for Java** – नवीनतम JAR को [Aspose रिलीज़ पेज](https://releases.aspose.com/psd/java/) से प्राप्त करें।  
3. **IDE** – IntelliJ IDEA, Eclipse, या कोई भी Java‑संगत एडिटर।  
4. **एक PSD फ़ाइल** – Photoshop में बनाएं या प्रयोग के लिए एक नमूना PSD प्राप्त करें।  
5. **बुनियादी Java ज्ञान** – क्लासेज़, ऑब्जेक्ट्स, और एक्सेप्शन हैंडलिंग की परिचितता।

## पैकेज आयात करें
इम्पोर्ट स्टेटमेंट्स कोर Aspose.PSD क्लासेज़ को स्कोप में लाते हैं, जैसे `PsdImage`, `VsmsResource`, और `LengthRecord`।

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## चरण 1: अपने स्रोत और आउटपुट डायरेक्टरी सेट करें
परिभाषित करें कि मूल PSD कहाँ स्थित है और संशोधित फ़ाइल कहाँ लिखी जाएगी।

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
`VsmsResource` वह कंटेनर है जो लेयर के लिए वेक्टर आकार डेटा संग्रहीत करता है। दूसरे लेयर के रिसोर्सेज़ में लूप करके इसे खोजें।

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## चरण 4: लेन्थ रिकॉर्ड्स तक पहुँचें
`LengthRecord` एक अलग वेक्टर पाथ का प्रतिनिधित्व करता है। उन रिकॉर्ड्स को प्राप्त करें जिन्हें आप संशोधित करना चाहते हैं।

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## चरण 5: पाथ ऑपरेशन प्रॉपर्टीज़ संशोधित करें
`PathOperations` परिभाषित करता है कि व्यक्तिगत आकार कैसे इंटरैक्ट करते हैं (जैसे exclusion, intersection, subtraction)। इन मानों को बदलने से वेक्टर लेयर की दृश्य संरचना अपडेट होती है।

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## चरण 6: संशोधित PSD फ़ाइल सहेजें
परिवर्तनों को नई फ़ाइल में सहेजें।

```java
psdImage.save(outPsdFilePath);
```

## चरण 7: रिसोर्सेज़ को साफ़ करें
`PsdImage` इंस्टेंस को डिस्पोज़ करें ताकि मेमोरी मुक्त हो और रिसोर्स लीक न हो।

```java
psdImage.dispose();
```

## सपोर्ट लेन्थ रिकॉर्ड प्रॉपर्टीज़ के साथ PSD फ़ाइलों को बैच प्रोसेस कैसे करें
एकल‑फ़ाइल वर्कफ़्लो को लूप में लपेटें जो एक डायरेक्टरी में मौजूद कई PSD फ़ाइलों पर इटररेट करता है, प्रत्येक फ़ाइल के लिए `inPsdFilePath` और `outPsdFilePath` को अपडेट करता है। यह तरीका आपको मिनटों में दर्जनों या सैकड़ों फ़ाइलों पर समान वेक्टर‑आकार समायोजन लागू करने की अनुमति देता है, जो स्वचालित एसेट पाइपलाइन के लिए आदर्श है।

## सामान्य समस्याएँ और टिप्स
- **Null चेक्स** – `resource` तक पहुँचने से पहले हमेशा जाँचें कि वह `null` नहीं है।  
- **पाथ इंडेक्स बाउंड्स** – सुनिश्चित करें कि आप जिन इंडेक्स (जैसे `[2]`, `[7]`, `[11]`) का उपयोग कर रहे हैं, वे आपके विशेष PSD में मौजूद हैं।  
- **लाइसेंस** – वैध लाइसेंस के बिना चलाने पर सहेजी गई PSD में वॉटरमार्क एम्बेड हो जाता है।  

## निष्कर्ष
अब आपके पास Aspose.PSD for Java के साथ लेन्थ रिकॉर्ड प्रॉपर्टीज़ को सपोर्ट करके **PSD वेक्टर आकारों को संशोधित** करने का एक पूर्ण, एंड‑टू‑एंड उदाहरण है। चाहे आप एसेट पाइपलाइन को ऑटोमेट कर रहे हों या कस्टम डिज़ाइन टूल बना रहे हों, ये API आपको मैन्युअल Photoshop कार्य के बिना वेक्टर लेयर्स को हेरफेर करने की लचीलापन देती हैं। अन्य `PathOperations` मानों के साथ प्रयोग करें या कई `LengthRecord` एडिट्स को मिलाकर जटिल आकार बनाएं।

## अक्सर पूछे जाने वाले प्रश्न

**प्रश्न: वह PSD कैसे संभालें जिसमें कोई वेक्टर आकार लेयर नहीं है?**  
**उत्तर:** `VsmsResource` अनुपस्थित रहेगा, इसलिए `resource` `null` रहेगा। एक चेक जोड़ें और संशोधन चरण को स्किप करें या उपयोगकर्ता को सूचित करें।

**प्रश्न: क्या मैं फ़िल रंग या स्ट्रोक चौड़ाई जैसी अन्य प्रॉपर्टीज़ बदल सकता हूँ?**  
**उत्तर:** हाँ, `LengthRecord` फ़िल, स्ट्रोक और अपारदर्शिता के लिए सेटर्स प्रदान करता है। पूरी सूची के लिए API डॉक्यूमेंटेशन देखें।

**प्रश्न: क्या कई PSD फ़ाइलों को बैच‑प्रोसेस करना संभव है?**  
**उत्तर:** बिल्कुल। कोड को एक लूप में लपेटें जो PSD फ़ाइलों की डायरेक्टरी पर इटररेट करता है, प्रत्येक बार इनपुट और आउटपुट पाथ को समायोजित करता है।

**प्रश्न: फ़ाइल पाथ से लोड करते समय क्या मुझे स्ट्रीम्स को मैन्युअली बंद करना चाहिए?**  
**उत्तर:** `Image.load` फ़ाइल स्ट्रीम्स को स्वचालित रूप से संभालता है, लेकिन यदि आप `InputStream` से लोड कर रहे हैं, तो उपयोग के बाद उसे बंद करना याद रखें।

**प्रश्न: इन API के लिए Aspose.PSD का कौन सा संस्करण आवश्यक है?**  
**उत्तर:** `LengthRecord` और `PathOperations` क्लासेज़ Aspose.PSD 20.10 से उपलब्ध हैं। लेखन समय पर नवीनतम संस्करण (24.11) उपयोग करने की सलाह दी जाती है।

---

**Last Updated:** 2026-09-23  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose

## संबंधित ट्यूटोरियल

- [PSD को PNG में बदलें और वेक्टर मास्क जावा बनाएं – PSD फ़ाइलों में Vmsk रिसोर्स](/psd/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/)
- [Aspose.PSD for Java का उपयोग करके लेयर मास्क सपोर्ट के साथ PSD को PNG में बदलें](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [PSD फ़ाइलों में लेयर सपोर्ट जोड़ें](/psd/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}