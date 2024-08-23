---
title: जावा का उपयोग करके PSD में कर्व्स एडजस्टमेंट लेयर जोड़ें
linktitle: जावा का उपयोग करके PSD में कर्व्स एडजस्टमेंट लेयर जोड़ें
second_title: Aspose.PSD जावा एपीआई
description: इस विस्तृत ट्यूटोरियल में Aspose.PSD for Java का उपयोग करके PSD फ़ाइल में कर्व्स एडजस्टमेंट लेयर जोड़ना सीखें। अपनी छवियों को आसानी से बेहतर बनाएँ।
type: docs
weight: 11
url: /hi/java/modifying-converting-psd-images/add-curves-adjustment-layer-psd/
---
## परिचय
क्या आपने कभी PSD प्रारूप में छवियों में हेरफेर करने की कोशिश करते समय खुद को अटका हुआ पाया है? चाहे आप एक नवोदित ग्राफिक डिजाइनर हों या एक अनुभवी पेशेवर, फ़ोटोशॉप फ़ाइलों के साथ काम करना कभी-कभी भूलभुलैया में नेविगेट करने जैसा महसूस हो सकता है। सौभाग्य से, एक उपकरण है जो इस प्रक्रिया को सरल बनाता है - जावा के लिए Aspose.PSD। इस ट्यूटोरियल में, हम Aspose.PSD का उपयोग करके PSD फ़ाइल में कर्व्स एडजस्टमेंट लेयर जोड़ने के तरीके पर गहराई से चर्चा करेंगे, जिससे आपकी छवि संपादन कार्य आसान और अधिक कुशल हो जाएंगे। चरण-दर-चरण मार्गदर्शन के साथ, आप पारंपरिक रूप से छवि हेरफेर से जुड़ी जटिलताओं में फंसने के बिना एक पेशेवर की तरह अपनी छवियों को बेहतर बनाने में सक्षम होंगे।
## आवश्यक शर्तें
इससे पहले कि हम कोड में उतरें, आइए सुनिश्चित करें कि आप पूरी तरह से तैयार हैं। यहां वे पूर्वापेक्षाएँ दी गई हैं जिनकी आपको आवश्यकता होगी:
1. जावा डेवलपमेंट किट (JDK): आपको अपने कंप्यूटर पर JDK इंस्टॉल करना होगा। सुनिश्चित करें कि यह सबसे अच्छी संगतता के लिए नवीनतम संस्करण है।
2. Aspose.PSD for Java लाइब्रेरी: PSD फ़ाइलों में हेरफेर करने के लिए, आपको अपने प्रोजेक्ट में Aspose.PSD लाइब्रेरी को डाउनलोड करके शामिल करना होगा। आप इसे प्राप्त कर सकते हैं[यहाँ](https://releases.aspose.com/psd/java/).
3. आईडीई: अपना कोड लिखने के लिए किसी भी जावा आईडीई जैसे कि इंटेलीज आईडीईए, एक्लिप्स, या यहां तक कि एक साधारण टेक्स्ट एडिटर का उपयोग करें।
4. जावा की बुनियादी समझ: जावा प्रोग्रामिंग से परिचित होने से आपको इसे आसानी से समझने में मदद मिलेगी।
सब कुछ समझ में आ गया? बहुत बढ़िया! चलिए मज़ेदार भाग में आते हैं।
## पैकेज आयात करना
सबसे पहले, आपको आवश्यक पैकेज आयात करने होंगे। ऐसा करने का तरीका इस प्रकार है:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.CurvesLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager;
import com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager;
```
इन पैकेजों को आयात करके, आप अपने जावा एप्लिकेशन को उन क्लासों के बारे में बता रहे हैं जिनकी उसे PSD फाइलों में हेरफेर करने और विशेष रूप से कर्व्स एडजस्टमेंट परतों के साथ काम करने के लिए आवश्यकता है।
अब जब हमने सब कुछ सेट कर लिया है, तो आइए कोड को तोड़ें और देखें कि चरण दर चरण Curves Adjustment लेयर कैसे जोड़ें।
## चरण 1: अपनी डेटा निर्देशिका निर्धारित करें
पहला कदम यह निर्धारित करना है कि आपकी PSD फ़ाइलें कहाँ संग्रहीत की जाएँगी। सब कुछ व्यवस्थित रखने के लिए एक निर्देशिका सेट करें।
```java
String dataDir = "Your Document Directory"; // इस पथ को अपडेट करें
```
 के बारे में सोचें`dataDir`अपने कार्यस्थल के रूप में; यह वह जगह है जहाँ सारा जादू होता है! सुनिश्चित करें कि आप इसे बदलें`Your Document Directory` वास्तविक पथ के साथ जहां आपकी PSD फ़ाइलें हैं या स्थित होंगी।
## चरण 2: अपनी PSD फ़ाइल लोड करें
इसके बाद, आपको वह PSD फ़ाइल लोड करनी होगी जिसे आप संपादित करना चाहते हैं। यह निम्न कोड का उपयोग करके किया जाता है:
```java
String sourceFileName = dataDir + "CurvesAdjustmentLayer";
String psdPathAfterChange = dataDir + "CurvesAdjustmentLayerChanged";
```
 इस कोड स्निपेट में,`sourceFileName` मूल PSD फ़ाइल की ओर इशारा करता है, जबकि`psdPathAfterChange` वह जगह है जहाँ आप अपनी संशोधित फ़ाइल को सहेजेंगे। जोड़ना न भूलें`.psd` बाद में कोड में.
## चरण 3: परतों पर पुनरावृत्ति करें
अब समय है अपनी PSD फ़ाइल की परतों में खुदाई करने का। हम कर्व्स एडजस्टमेंट परतों की तलाश में प्रत्येक परत के माध्यम से लूप करेंगे।
```java
for (int j = 1; j < 2; j++) {
    String fileName = sourceFileName + ".psd";
    PsdImage im = (PsdImage) Image.load(fileName);
    
    for(int k = 0; k < im.getLayers().length; k++) {
        if (im.getLayers()[k] instanceof CurvesLayer) {
            // कर्व्स लेयर प्रोसेसिंग यहाँ होगी
        }
    }
}
```
यहां जो कुछ हो रहा है उसका विवरण दिया गया है:
-  हम PSD फ़ाइल को एक में लोड करके शुरू करते हैं`PsdImage` ऑब्जेक्ट का नाम`im`.
-  इसके बाद, हम छवि में सभी परतों के माध्यम से लूप करते हैं`im.getLayers().length` . इससे हमें प्रत्येक परत तक पहुंच मिलती है, जिससे हम यह जांच सकते हैं कि क्या यह एक है`CurvesLayer`.
## चरण 4: कर्व्स लेयर को संशोधित करें
 लूप के अंदर जो जाँच करता है`CurvesLayer`आप वक्रों को संशोधित करने के लिए तर्क जोड़ेंगे। यहाँ बताया गया है कि आप ऐसा कैसे करेंगे:
```java
if (curvesLayer.isDiscreteManagerUsed()) {
    CurvesDiscreteManager manager = (CurvesDiscreteManager) curvesLayer.getCurvesManager();
    for (int i = 10; i < 50; i++) {
        manager.setValueInPosition(0, (byte) i, (byte) (15 + (i * 2)));
    }
} else {
    CurvesContinuousManager manager = (CurvesContinuousManager) curvesLayer.getCurvesManager();
    manager.addCurvePoint((byte) 0, (byte) 50, (byte) 100);
    manager.addCurvePoint((byte) 0, (byte) 150, (byte) 130);
}
```
इस खंड में:
- हम जाँचते हैं कि वक्र परत असतत प्रबंधक का उपयोग करती है या सतत प्रबंधक का।
- यदि यह असतत प्रबंधक है, तो हम प्रत्येक पद के लिए 10 से 49 तक नए मान निर्धारित करते हैं।
- इसके विपरीत, सतत प्रबंधक के साथ, हम आवश्यकतानुसार वक्रों को समायोजित करने के लिए वक्र बिंदु जोड़ते हैं।
## चरण 5: संशोधित PSD को सहेजें
समायोजन करने के बाद, अंतिम चरण संशोधित PSD फ़ाइल को सहेजना है।
```java
im.save(psdPathAfterChange + Integer.toString(j) + ".psd");
```
 यह लाइन समायोजित PSD को आपके द्वारा पहले परिभाषित पथ में सहेजती है। हर बार जब आप संशोधित करते हैं, तो यह लूप काउंटर के आधार पर एक अलग प्रत्यय के साथ एक नई फ़ाइल बनाएगा`j`.
## निष्कर्ष
बधाई हो! आपने सफलतापूर्वक सीख लिया है कि Aspose.PSD for Java का उपयोग करके PSD फ़ाइल में कर्व्स एडजस्टमेंट लेयर कैसे जोड़ें। बस कुछ ही चरणों के साथ, आप अपनी छवियों को बेहतर बना सकते हैं और अपनी ज़रूरतों के अनुसार उनमें बदलाव कर सकते हैं। इस लाइब्रेरी द्वारा प्रदान की गई लचीलापन इसे PSD फ़ाइलों के साथ काम करने वाले किसी भी व्यक्ति के लिए एक अमूल्य उपकरण बनाती है। अब आगे बढ़ें और अलग-अलग कर्व्स के साथ प्रयोग करें, और अपनी रचनात्मकता को प्रवाहित होने दें।
## अक्सर पूछे जाने वाले प्रश्न
### Aspose.PSD क्या है?
Aspose.PSD जावा सहित विभिन्न प्रोग्रामिंग भाषाओं में फ़ोटोशॉप PSD फ़ाइलों के प्रसंस्करण के लिए एक लाइब्रेरी है।
### क्या मैं Aspose.PSD का निःशुल्क उपयोग कर सकता हूँ?
 हां, Aspose एक निःशुल्क परीक्षण प्रदान करता है जिसे आप खरीदने से पहले देख सकते हैं।[निःशुल्क परीक्षण डाउनलोड](https://releases.aspose.com/) जोड़ना।
### क्या फ़ोटोशॉप स्थापित करना आवश्यक है?
नहीं, Aspose.PSD के साथ काम करने के लिए आपको अपनी मशीन पर फ़ोटोशॉप स्थापित करने की आवश्यकता नहीं है।
### क्या मैं कर्व्स एडजस्टमेंट परतों के अलावा अन्य परतों में भी बदलाव कर सकता हूँ?
बिल्कुल! Aspose.PSD PSD फ़ाइलों में विभिन्न परत प्रकारों के हेरफेर की अनुमति देता है।
### मुझे अधिक दस्तावेज कहां मिल सकते हैं?
 विस्तृत दस्तावेज़ीकरण के लिए, कृपया देखें[Aspose.PSD for Java दस्तावेज़](https://reference.aspose.com/psd/java/).