---
date: 2026-04-03
description: Aspose.PSD for Java का उपयोग करके PSD फ़ाइलों में शीट रंगों को हाइलाइट
  करना सीखें। अपनी इमेज मैनिपुलेशन कौशल को जावा में बेहतर बनाने के लिए हमारे चरण‑दर‑चरण
  गाइड का पालन करें।
keywords:
- highlight sheet color psd
- change psd layer color
- Aspose.PSD Java
linktitle: Aspire.PSD Java का उपयोग करके PSD फ़ाइलों में शीट रंग को हाइलाइट करें
second_title: Aspose.PSD Java API
title: Aspire.PSD Java का उपयोग करके PSD फ़ाइलों में शीट रंग को हाइलाइट करें
url: /hi/java/psd-layer-management-effects/highlight-sheet-color-psd-files/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.PSD Java का उपयोग करके PSD फ़ाइलों में शीट रंग को हाइलाइट करें

## परिचय

यदि आपको प्रोग्रामेटिक रूप से **highlight sheet color psd** फ़ाइलों को हाइलाइट करने की आवश्यकता है, तो आप सही जगह पर आए हैं। इस ट्यूटोरियल में हम एक पूर्ण, व्यावहारिक उदाहरण के माध्यम से दिखाएंगे कि Aspose.PSD for Java का उपयोग करके व्यक्तिगत लेयर्स के शीट रंग को कैसे बदलें। चाहे आप बैच‑प्रोसेसिंग टूल, कस्टम एडिटर बना रहे हों, या केवल दोहराए जाने वाले डिज़ाइन कार्यों को स्वचालित कर रहे हों, इस तकनीक में निपुण होने से आपको अपने PSD एसेट्स पर सूक्ष्म नियंत्रण मिलेगा।

## त्वरित उत्तर
- **What does “highlight sheet color” mean?** यह एक दृश्य संकेत है जो लेयर को असाइन किया जाता है और Photoshop के लेयर पैनल में एक रंगीन स्ट्राइप के रूप में दिखता है।  
- **Which library handles this in Java?** Aspose.PSD for Java `SheetColorHighlightEnum` और संबंधित API प्रदान करता है।  
- **Do I need a license to try it?** एक मुफ्त ट्रायल उपलब्ध है; उत्पादन उपयोग के लिए लाइसेंस आवश्यक है।  
- **Can I change multiple layers at once?** हाँ—`Layer[]` संग्रह के माध्यम से लूप करें और प्रत्येक लेयर का हाइलाइट सेट करें।  
- **What Java version is required?** JDK 8 या उससे ऊपर।

## “highlight sheet color psd” क्या है?

एक शीट‑कलर हाइलाइट एक मेटाडेटा एट्रिब्यूट है जो PSD फ़ाइल के भीतर संग्रहीत होता है और Photoshop (और संगत टूल्स) को लेयर नाम के बगल में एक रंगीन बार ड्रॉ करने के लिए बताता है। यह लेयर्स के समूहों को जल्दी पहचानने में उपयोगी है—इसे एक दृश्य टैग के रूप में सोचें जिसे वायलेट, ऑरेंज, येलो आदि जैसे रंगों में सेट किया जा सकता है।

## प्रोग्रामेटिक रूप से PSD लेयर रंग क्यों बदलें?

- **Automation:** मैन्युअल क्लिक के बिना सैकड़ों फ़ाइलों को प्रोसेस करें।  
- **Consistency:** डिज़ाइन सिस्टम में नामकरण/रंग योजना को लागू करें।  
- **Integration:** PSD हेरफेर को अन्य Java‑आधारित वर्कफ़्लोज़ (जैसे, मोबाइल ऐप्स के लिए एसेट्स जेनरेट करना) के साथ संयोजित करें।

## पूर्वापेक्षाएँ

कोड में डुबकी लगाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

- **Java Development Kit (JDK) 8+** – [Java website](https://www.oracle.com/java/technologies/javase-downloads.html) से डाउनलोड करें।  
- **IDE** – IntelliJ IDEA, Eclipse, या NetBeans (आपकी पसंद)।  
- **Aspose.PSD for Java library** – इसे [Aspose's website](https://releases.aspose.com/psd/java/) से प्राप्त करें।  
- **Sample PSD file** – `SheetColorHighlightExample.psd` (अपना बनाएं या ऑनलाइन एक सैंपल प्राप्त करें)।  
- **Basic Java knowledge** – आपको क्लासेज़, मेथड्स, और सरल फ़ाइल I/O में सहज होना चाहिए।

## पैकेज आयात करें

पहले, उन क्लासेज़ को आयात करें जिनकी हमें आवश्यकता होगी। ये इम्पोर्ट्स हमें कोर इमेज हैंडलिंग, लेयर मैनिपुलेशन, और शीट‑कलर हाइलाइट्स के लिए एनेमरेशन तक पहुंच प्रदान करते हैं।

```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.layerresources.SheetColorHighlightEnum;
```

## स्टेप‑बाय‑स्टेप गाइड

### स्टेप 1: PSD फ़ाइल लोड करें

#### 1.1 फ़ाइल पाथ्स निर्धारित करें

स्रोत और गंतव्य पाथ सेट करें। प्लेसहोल्डर को उस वास्तविक फ़ोल्डर से बदलें जिसमें आपकी PSD फ़ाइल स्थित है।

```java
String dataDir = "YOUR DOCUMENT DIRECTORY";

String sourceFileName = dataDir + "SheetColorHighlightExample.psd";
String exportPath = dataDir + "SheetColorHighlightExampleChanged.psd";
```

#### 1.2 PSD फ़ाइल लोड करें

`Image.load()` का उपयोग करें और परिणाम को `PsdImage` में कास्ट करें ताकि हम PSD‑विशिष्ट फीचर्स के साथ काम कर सकें।

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### स्टेप 2: लेयर्स तक पहुंचें और निरीक्षण करें

लेयर्स PSD की दृश्य सामग्री को रखती हैं। हम वर्तमान शीट‑कलर हाइलाइट्स को पढ़ेंगे ताकि प्रारंभिक स्थिति की पुष्टि हो सके।

#### 2.1 पहली लेयर तक पहुंचें

```java
Layer layer1 = im.getLayers()[0];
Assert.areEqual(SheetColorHighlightEnum.Violet, layer1.getSheetColorHighlight());
```

#### 2.2 दूसरी लेयर तक पहुंचें

```java
Layer layer2 = im.getLayers()[1];
Assert.areEqual(SheetColorHighlightEnum.Orange, layer2.getSheetColorHighlight());
```

### स्टेप 3: शीट कलर हाइलाइट संशोधित करें

अब हम पहली लेयर का हाइलाइट येलो में बदलेंगे, जिससे यह प्रदर्शित होगा कि **change psd layer color** को प्रोग्रामेटिक रूप से कैसे किया जाता है।

```java
layer1.setSheetColorHighlight(SheetColorHighlightEnum.Yellow);
```

### स्टेप 4: संशोधित PSD फ़ाइल सहेजें

परिवर्तनों को नई फ़ाइल में सहेजें ताकि मूल फ़ाइल अपरिवर्तित रहे।

```java
im.save(exportPath);
```

## सामान्य समस्याएँ और समाधान

| समस्या | क्यों होता है | समाधान |
|-------|----------------|-----|
| `Assert` fails | लेयर का मौजूदा हाइलाइट कोड की अपेक्षा के अनुरूप नहीं है (जैसे, अलग PSD)। | Photoshop में PSD खोलें और रंगों की पुष्टि करें, या अधिक लचीले स्क्रिप्ट के लिए `Assert` जांच हटाएँ। |
| `NullPointerException` on `im.getLayers()` | फ़ाइल सही ढंग से लोड नहीं हुई (गलत पाथ या भ्रष्ट फ़ाइल)। | `sourceFileName` को दोबारा जांचें और सुनिश्चित करें कि PSD वैध है। |
| Highlight doesn’t appear in Photoshop | Photoshop लेयर जानकारी को कैश करता है; आपको फ़ाइल को पुनः खोलने की आवश्यकता हो सकती है। | सहेजने के बाद PSD को बंद करके पुनः खोलें, या सहेजने से पहले `im.flush()` का उपयोग करें। |

## अक्सर पूछे जाने वाले प्रश्न

**Q: What is Aspose.PSD for Java?**  
A: Aspose.PSD for Java एक लाइब्रेरी है जो डेवलपर्स को Photoshop स्थापित किए बिना PSD फ़ाइलों को पढ़ने, संपादित करने और सहेजने की अनुमति देती है।

**Q: Can I use Aspose.PSD for Java with other file formats?**  
A: हाँ—BMP, PNG, JPEG, GIF, TIFF, आदि समर्थित हैं, जिससे PSD से और PSD में रूपांतरण संभव है।

**Q: Is it possible to undo changes made to a PSD file using Aspose.PSD for Java?**  
A: एक बार सहेजने के बाद, परिवर्तन स्थायी होते हैं। यदि आपको वापस लौटना है तो मूल फ़ाइल का बैकअप रखें।

**Q: How do I obtain a license for Aspose.PSD for Java?**  
A: लाइसेंस [Aspose website](https://purchase.aspose.com/buy) से खरीदें। यदि आप मूल्यांकन कर रहे हैं, तो सीमित अवधि के लिए एक [temporary license](https://purchase.aspose.com/temporary-license/) का अनुरोध कर सकते हैं।

**Q: Can I highlight multiple layers at once in a PSD file?**  
A: बिल्कुल। `im.getLayers()` पर लूप करें और आवश्यकतानुसार प्रत्येक लेयर पर `setSheetColorHighlight()` कॉल करें।

---

**अंतिम अद्यतन:** 2026-04-03  
**परीक्षण किया गया:** Aspose.PSD 24.11 for Java  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}