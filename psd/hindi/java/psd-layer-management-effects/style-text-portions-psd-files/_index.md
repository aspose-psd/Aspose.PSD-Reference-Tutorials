---
title: जावा का उपयोग करके PSD फ़ाइलों में टेक्स्ट भागों को स्टाइल करें
linktitle: जावा का उपयोग करके PSD फ़ाइलों में टेक्स्ट भागों को स्टाइल करें
second_title: Aspose.PSD जावा एपीआई
description: Aspose.PSD for Java के साथ PSD टेक्स्ट स्टाइलिंग में महारत हासिल करें। टेक्स्ट भागों को आसानी से संशोधित करना, बनाना और स्टाइल करना सीखें। अपने PSD डिज़ाइन को बेहतर बनाएँ।
weight: 22
url: /hi/java/psd-layer-management-effects/style-text-portions-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# जावा का उपयोग करके PSD फ़ाइलों में टेक्स्ट भागों को स्टाइल करें

## परिचय

क्या आपने कभी PSD फ़ाइलों में अपने टेक्स्ट लेयर्स में वह अतिरिक्त आकर्षण जोड़ना चाहा है? Aspose.PSD for Java आपको न केवल टेक्स्ट में हेरफेर करने की शक्ति देता है, बल्कि अविश्वसनीय सटीकता के साथ अलग-अलग हिस्सों को स्टाइल करने की भी शक्ति देता है। यह व्यापक गाइड आपको प्रक्रिया के माध्यम से कदम-दर-कदम ले जाएगा, अपने वातावरण को सेट करने से लेकर अपने PSDs के भीतर आश्चर्यजनक रूप से स्टाइल किए गए टेक्स्ट तत्व बनाने तक।

## आवश्यक शर्तें

इससे पहले कि हम आगे बढ़ें, सुनिश्चित करें कि आपके पास निम्नलिखित चीजें हैं:

- जावा डेवलपमेंट किट (JDK): हम जिस कोड पर चर्चा करेंगे उसे चलाने के लिए आपको अपने सिस्टम पर JDK इंस्टॉल करना होगा। जावा वेबसाइट देखें ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)) डाउनलोड और स्थापना निर्देशों के लिए.
- Aspose.PSD for Java लाइब्रेरी: यह लाइब्रेरी आपको PSD फ़ाइलों के साथ प्रोग्रामेटिक रूप से इंटरैक्ट करने की अनुमति देती है। Aspose वेबसाइट पर जाएँ ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)लाइब्रेरी डाउनलोड करने के लिए। याद रखें, आपको पूरी कार्यक्षमता का उपयोग करने के लिए लाइसेंस की आवश्यकता होगी, लेकिन आरंभ करने के लिए एक निःशुल्क परीक्षण उपलब्ध है।

## पैकेज आयात करें

एक बार जब आप सब कुछ सेट कर लें, तो अपना पसंदीदा Java IDE खोलें और कोडिंग शुरू करें। पहला कदम Aspose.PSD for Java से आवश्यक पैकेज आयात करना है:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.TextLayer;
import com.aspose.psd.fileformats.psd.layers.text.IText;
import com.aspose.psd.fileformats.psd.layers.text.ITextParagraph;
import com.aspose.psd.fileformats.psd.layers.text.ITextPortion;
import com.aspose.psd.fileformats.psd.layers.text.ITextStyle;
import com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline;
import com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps;
```

ये आयात हमें PSD फ़ाइलों के साथ काम करने के लिए आवश्यक कक्षाओं और कार्यात्मकताओं तक पहुंच प्रदान करते हैं।

अब, चलिए असली जादू की ओर बढ़ते हैं! PSD फ़ाइल में टेक्स्ट के हिस्सों को स्टाइल करने के लिए यहाँ कुछ चरणों का विवरण दिया गया है:

## चरण 1: PSD फ़ाइल लोड करें

सबसे पहले, हमें PSD फ़ाइल लोड करनी होगी जिसमें वे टेक्स्ट लेयर्स हों जिन्हें हम संशोधित करना चाहते हैं। इसे करने का तरीका इस प्रकार है:

```java
String sourceDir = "yourSourceDirectory";
String inPsdFilePath = sourceDir + "text212.psd";

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);
```

यह कोड स्निपेट आपके स्रोत PSD फ़ाइल का पथ परिभाषित करता है (`inPsdFilePath` ) और फिर का उपयोग करता है`Image.load` फ़ाइल को लोड करने की विधि`PsdImage` वस्तु।

## चरण 2: टेक्स्ट परतों तक पहुँचना

PSD फ़ाइलों में विभिन्न प्रकार की परतें हो सकती हैं। विशेष रूप से टेक्स्ट के साथ काम करने के लिए, हमें टेक्स्ट लेयर ऑब्जेक्ट तक पहुँचने की आवश्यकता है। यहाँ बताया गया है कि कैसे:

```java
TextLayer textLayer = (TextLayer)psdImage.getLayers()[1];
```

यह कोड मानता है कि आप पहली परत में पाठ को संशोधित करना चाहते हैं (`psdImage.getLayers()[1]`) याद रखें, PSD फ़ाइल में परत क्रम भिन्न हो सकता है, इसलिए यदि आपकी पाठ परत किसी भिन्न स्थिति पर है तो सूचकांक को तदनुसार समायोजित करें।

## चरण 3: टेक्स्ट डेटा के साथ काम करना

`TextLayer` ऑब्जेक्ट में टेक्स्ट कंटेंट और उसके फ़ॉर्मेटिंग के बारे में सारी जानकारी होती है। हम इस जानकारी को इसके ज़रिए एक्सेस कर सकते हैं`getTextData` तरीका:

```java
IText textData = textLayer.getTextData();
```

`IText`वस्तु (`textData`) परत की पाठ्य सामग्री का प्रतिनिधित्व करता है। यह पाठ और उसकी शैली में हेरफेर करने के लिए कार्यक्षमता प्रदान करता है।

## चरण 4: डिफ़ॉल्ट शैलियाँ परिभाषित करना (वैकल्पिक)

हालाँकि यह पूरी तरह से आवश्यक नहीं है, लेकिन टेक्स्ट और पैराग्राफ़ के लिए डिफ़ॉल्ट स्टाइल परिभाषित करने से आपका वर्कफ़्लो सुव्यवस्थित हो सकता है। यह आपको एक बेसलाइन स्टाइल सेट करने की अनुमति देता है जिसे आप विशिष्ट भागों के लिए आसानी से ओवरराइड कर सकते हैं:

```java
ITextStyle defaultStyle = textData.producePortion().getStyle();
defaultStyle.setFillColor(Color.getDimGray());
defaultStyle.setFontSize(51);

ITextParagraph defaultParagraph = textData.producePortion().getParagraph();
```

 यह कोड एक नया कोड बनाता है`ITextStyle`वस्तु (`defaultStyle` ) और इसके गुणधर्म जैसे कि भरण रंग और फ़ॉन्ट आकार सेट करता है। इसी तरह, एक नया`ITextParagraph`वस्तु (`defaultParagraph`) डिफ़ॉल्ट पैराग्राफ़ सेटिंग्स को परिभाषित करने के लिए बनाया गया है।

## चरण 5: मौजूदा पाठ भागों को स्टाइल करना

मान लीजिए कि आप लेयर के अंदर मौजूद टेक्स्ट के किसी खास हिस्से पर स्ट्राइकथ्रू इफ़ेक्ट जोड़ना चाहते हैं। इसे पाने का तरीका इस प्रकार है:

```java
textData.getItems()[1].getStyle().setStrikethrough(true);
```

यह कोड दूसरे पाठ भाग को पुनः प्राप्त करता है (`textData.getItems()[1]` ) और इसके`strikethrough`संपत्ति को`true` आप इसी तरह अन्य भागों तक पहुँच सकते हैं और द्वारा प्रदान की गई विभिन्न विधियों का उपयोग करके उनकी शैलियों को संशोधित कर सकते हैं`ITextStyle` इंटरफ़ेस.

## चरण 6: शैलियों के साथ नए पाठ भाग बनाना

क्या आप शुरू से ही विशिष्ट शैलियों के साथ कुछ नए टेक्स्ट तत्व जोड़ना चाहते हैं? Aspose.PSD for Java आपको ऐसा करने की सुविधा देता है!

```java
String[] newTextStrings = {"E=mc2", "Bold", "Italic", "Lowercasetext"};
ITextPortion[] newTextPortions = textData.producePortions(newTextStrings, defaultStyle, defaultParagraph);
```

यह कोड स्ट्रिंग्स की एक सरणी बनाता है (`newTextStrings` ) जिसमें नए भागों के लिए पाठ सामग्री शामिल है। फिर, यह उपयोग करता है`textData.producePortions` एक सरणी बनाने के लिए`ITextPortion` वस्तुओं, को लागू करना`defaultStyle` और`defaultParagraph` प्रत्येक भाग के लिए.

## चरण 7: नए पाठ भागों को अनुकूलित करना

एक बार जब आपके पास नए पाठ भाग आ जाएं, तो आप अलग-अलग भागों पर विशिष्ट शैलियाँ लागू कर सकते हैं:

```java
newTextPortions[0].getStyle().setUnderline(true); // "E=mc2" के लिए रेखांकित करें
newTextPortions[1].getStyle().setFauxBold(true); // बोल्ड के लिए "बोल्ड"
newTextPortions[2].getStyle().setFauxItalic(true); // इटैलिक के लिए "इटैलिक"
newTextPortions[3].getStyle().setFontCaps(FontCaps.SmallCaps); //"लोअरकेसटेक्स्ट" के लिए छोटे अक्षर
```

यहाँ, हम पहले तीन नए टेक्स्ट भागों की शैलियों को अनुकूलित कर रहे हैं। आप अपनी आवश्यकताओं के आधार पर विभिन्न स्टाइलिंग विकल्प लागू कर सकते हैं।

## चरण 8: परत में नए पाठ भाग जोड़ना

नए पाठ भागों को अनुकूलित करने के बाद, आपको उन्हें पाठ परत में जोड़ना होगा:

```java
for (ITextPortion newTextPortion : newTextPortions) {
    textData.addPortion(newTextPortion);
}
```

 यह कोड निम्न के माध्यम से पुनरावृत्त होता है`newTextPortions` सरणी और प्रत्येक भाग को जोड़ता है`textData` वस्तु।

## चरण 9: परत पर परिवर्तन लागू करना

PSD परत में पाठ डेटा में किए गए संशोधनों को प्रतिबिंबित करने के लिए, आपको परत को अपडेट करना होगा:

```java
textData.updateLayerData();
```

 यह कॉल अपडेट करता है`textLayer` इसमें किये गए परिवर्तनों के साथ`textData`.

## चरण 10: संशोधित PSD फ़ाइल को सहेजना

अंत में, संशोधित PSD फ़ाइल को नए स्थान पर सहेजें:

```java
String outputDir = "yourOutputDirectory";
String outPsdFilePath = outputDir + "Output_text212.psd";

psdImage.save(outPsdFilePath);
```

 यह कोड आउटपुट फ़ाइल पथ बनाता है और सहेजता है`psdImage` निर्दिष्ट स्थान पर आपत्ति करें।

## निष्कर्ष

और अब आपका काम हो गया! आपने Aspose.PSD for Java का उपयोग करके PSD फ़ाइल में टेक्स्ट भागों को सफलतापूर्वक स्टाइल किया है। इन चरणों का पालन करके और उपलब्ध विभिन्न स्टाइलिंग विकल्पों की खोज करके, आप अपने PSDs में आकर्षक और अनुकूलित टेक्स्ट तत्व बना सकते हैं।

याद रखें, यह सिर्फ़ एक शुरुआती बिंदु है। Aspose.PSD for Java टेक्स्ट हेरफेर के लिए कई तरह की कार्यक्षमता प्रदान करता है, जिसमें उन्नत फ़ॉर्मेटिंग, पैराग्राफ़ नियंत्रण और बहुत कुछ शामिल है। वांछित परिणाम प्राप्त करने के लिए प्रयोग करें और अपनी रचनात्मकता को उजागर करें!

## अक्सर पूछे जाने वाले प्रश्न

### क्या मैं किसी विशिष्ट पाठ भाग का फ़ॉन्ट बदल सकता हूँ?
 हां, आप इसका उपयोग करके पाठ भाग का फ़ॉन्ट बदल सकते हैं`setFontName` की विधि`ITextStyle` वस्तु।

### मैं किसी पैराग्राफ में टेक्स्ट संरेखण कैसे समायोजित कर सकता हूँ?
`ITextParagraph` ऑब्जेक्ट जैसे गुण प्रदान करता है`setAlignment` पैराग्राफ़ के भीतर पाठ संरेखण को नियंत्रित करने के लिए.

### क्या पाठ के वर्ण अन्तराल को संशोधित करना संभव है?
 हां, आप इसका उपयोग करके वर्ण अंतरण को समायोजित कर सकते हैं`setCharacterSpacing` की विधि`ITextStyle` वस्तु।

### क्या मैं एक ही पाठ के विभिन्न भागों पर अलग-अलग शैलियाँ लागू कर सकता हूँ?
यद्यपि यह सीधे तौर पर समर्थित नहीं है, फिर भी आप एक ही समग्र भाग के भीतर अनेक पाठ भाग बनाकर समान प्रभाव प्राप्त कर सकते हैं।

### क्या पाठ के भागों या अक्षरों की संख्या पर कोई सीमाएं हैं?
व्यावहारिक सीमाएँ सिस्टम संसाधनों और PSD फ़ाइल की जटिलता पर निर्भर करती हैं। हालाँकि, Aspose.PSD for Java को बड़ी PSD फ़ाइलों को कुशलतापूर्वक संभालने के लिए डिज़ाइन किया गया है।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
