---
title: जावा के साथ PSD फ़ाइलों में ग्रेडिएंट फिल लेयर जोड़ें
linktitle: जावा के साथ PSD फ़ाइलों में ग्रेडिएंट फिल लेयर जोड़ें
second_title: Aspose.PSD जावा एपीआई
description: Aspose.PSD for Java का उपयोग करके PSD फ़ाइलों में ग्रेडिएंट भरण परतों को संशोधित करें। प्रोग्रामेटिक रूप से रंग, पारदर्शिता और अन्य ग्रेडिएंट गुणों को बदलने का तरीका जानें।
weight: 15
url: /hi/java/psd-image-modification-conversion/add-gradient-fill-layer-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# जावा के साथ PSD फ़ाइलों में ग्रेडिएंट फिल लेयर जोड़ें

## परिचय

क्या आपने कभी अपनी PSD फ़ाइलों के लिए विज़ुअल मैजिक के उस अतिरिक्त स्पर्श की लालसा की है? ग्रेडिएंट आपके डिज़ाइन में गहराई और आयाम जोड़ने का एक शानदार तरीका प्रदान करते हैं। लेकिन क्या होगा यदि आप जावा का उपयोग करके इन ग्रेडिएंट को प्रोग्रामेटिक रूप से हेरफेर करना चाहते हैं? Aspose.PSD बचाव के लिए आता है! यह व्यापक गाइड आपको Aspose.PSD का उपयोग करके PSD फ़ाइलों के भीतर ग्रेडिएंट फिल परतों को संशोधित करने के लिए सशक्त बनाएगी, जो आपको रोमांचक प्रक्रिया के माध्यम से चरण-दर-चरण ले जाएगी।

## आवश्यक शर्तें

इसमें गोता लगाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित चीजें हैं:

-  जावा डेवलपमेंट किट (JDK): जावा कोड चलाने के लिए JDK का एक स्थिर संस्करण आवश्यक है। आप इसे Oracle वेबसाइट से डाउनलोड कर सकते हैं:[Oracle JDK डाउनलोड पृष्ठ का लिंक]
-  Aspose.PSD for Java: यह शक्तिशाली लाइब्रेरी आपको अपने Java अनुप्रयोगों में PSD फ़ाइलों के साथ काम करने की अनुमति देती है। इसे Aspose वेबसाइट से डाउनलोड करें:[जावा डाउनलोड के लिए Aspose.PSD का लिंक] (निःशुल्क परीक्षण उपलब्ध है)

## पैकेज आयात करें

आइए PSD फ़ाइलों के साथ काम करने के लिए आवश्यक आवश्यक Aspose.PSD पैकेजों को आयात करके शुरू करें:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.imageoptions.PsdOptions;
import java.util.ArrayList;
import java.util.Collections;
import java.util.List;
```

ये आयात PSD फ़ाइलों को लोड करने, हेरफेर करने और सहेजने के लिए कक्षाओं और विधियों तक पहुंच प्रदान करते हैं।

अब, ग्रेडिएंट भरण परतों को संशोधित करने की रोमांचक यात्रा के लिए तैयार हो जाइए!

## चरण 1: PSD फ़ाइल लोड करें

 सबसे पहले, हमें उस PSD फ़ाइल को लोड करना होगा जिसमें वह ग्रेडिएंट फ़िल लेयर है जिसे आप संशोधित करना चाहते हैं।`Image.load` विधि, फ़ाइल पथ निर्दिष्ट करना:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ComplexGradientFillLayer.psd";
String outputFile = dataDir + "ComplexGradientFillLayer_output.psd";
PsdImage image = (PsdImage)Image.load(sourceFileName);
```

 यह कोड स्निपेट निर्दिष्ट निर्देशिका से PSD फ़ाइल लोड करता है और इसे संग्रहीत करता है`image` चर।

## चरण 2: ग्रेडिएंट फिल लेयर की पहचान करें

 PSD फ़ाइलों में कई परतें हो सकती हैं। हमें उस विशिष्ट परत को अलग करना होगा जिसमें वह ग्रेडिएंट फ़िल है जिसे हम संपादित करना चाहते हैं।`image.getLayers()` वांछित परत खोजने के लिए सरणी:

```java
for (int i = 0; i < image.getLayers().length; i++) {
if (image.getLayers()[i] instanceof FillLayer) {
   FillLayer fillLayer = (FillLayer) image.getLayers()[i];
   // आगे की जाँच और संशोधन यहाँ होंगे
   break;
}
}
```

 यह लूप प्रत्येक परत की जाँच करता है। यदि कोई परत`FillLayer` , इसे डाला जाता है`FillLayer` प्रकार और में संग्रहीत`fillLayer`आगे की प्रक्रिया के लिए चर। यदि आपके पास लक्ष्य परत (जैसे, परत का नाम) की पहचान करने के लिए विशिष्ट मानदंड हैं, तो हम लूप के भीतर अतिरिक्त जाँच जोड़ सकते हैं।

## चरण 3: ग्रेडिएंट भरण प्रकार सत्यापित करें

सभी फिल लेयर ग्रेडिएंट का उपयोग नहीं करते हैं। यह कोड स्निपेट पुष्टि करता है कि पहचानी गई परत में वास्तव में ग्रेडिएंट फिल है या नहीं:

```java
if (fillLayer.getFillSettings().getFillType() != FillType.Gradient) {
   throw new Exception("Wrong Fill Layer");
}
```

 यदि`getFillType` विधि वापस नहीं आती`FillType.Gradient`, एक अपवाद उत्पन्न होता है, जो यह दर्शाता है कि हम गलत परत के साथ काम कर रहे हैं।

## चरण 4: ग्रेडिएंट गुणों तक पहुंचें और उन्हें संशोधित करें

 जादू यहाँ होता है! Aspose.PSD के माध्यम से विभिन्न ग्रेडिएंट भरण गुणों तक पहुँच प्रदान करता है`IGradientFillSettings` इंटरफ़ेस। हम उन्हें आवश्यकतानुसार पुनः प्राप्त और संशोधित कर सकते हैं:

```java
IGradientFillSettings settings = (IGradientFillSettings) fillLayer.getFillSettings();

// गुण संशोधित करें (वांछित मानों से प्रतिस्थापित करें)
settings.setAngle(0.0);  // कोण को 0 डिग्री पर सेट करें
settings.setDither(false);  // डिथरिंग अक्षम करें
settings.setAlignWithLayer(true); // परत के साथ ग्रेडिएंट संरेखित करें
settings.setReverse(true);  // रिवर्स ग्रेडिएंट दिशा
settings.setHorizontalOffset(25);  // क्षैतिज ऑफसेट सेट करें
settings.setVerticalOffset(-15);  // ऊर्ध्वाधर ऑफसेट सेट करें
```

 यह कोड पुनर्प्राप्त करता है`IGradientFillSettings`ऑब्जेक्ट और फिर कोण, डिथरिंग, संरेखण और ऑफसेट जैसे गुणों को संशोधित करता है। आपके द्वारा कल्पना किए गए ग्रेडिएंट प्रभाव को प्राप्त करने के लिए दिए गए मानों को अपनी इच्छित सेटिंग्स से बदलें।

## चरण 5: रंग और पारदर्शिता बिंदुओं में हेरफेर करें

ग्रेडिएंट को स्पेक्ट्रम के साथ रंग और पारदर्शिता बिंदुओं द्वारा परिभाषित किया जाता है। Aspose.PSD आपको सटीक नियंत्रण के लिए इन बिंदुओं को संशोधित करने की अनुमति देता है:

```java
List<IGradientColorPoint> colorPoints = new ArrayList<IGradientColorPoint>();
Collections.addAll(colorPoints, settings.getColorPoints());
List<IGradientTransparencyPoint> transparencyPoints = new ArrayList<IGradientTransparencyPoint>();
Collections.addAll(transparencyPoints, settings.getTransparencyPoints());

// नया रंग बिंदु जोड़ें
GradientColorPoint gr1 = new GradientColorPoint();
gr1.setColor(Color.getViolet());
gr1.setLocation(4096);
gr1.setMedianPointLocation(75);
colorPoints.add(gr1);

// मौजूदा रंग बिंदु को संशोधित करें
colorPoints.get(1).setLocation(3000);

// नया पारदर्शिता बिंदु जोड़ें
GradientTransparencyPoint gr2 = new GradientTransparencyPoint();
gr2.setOpacity(80.0);
gr2.setLocation(4096);
gr2.setMedianPointLocation(25);
transparencyPoints.add(gr2);

// मौजूदा पारदर्शिता बिंदु को संशोधित करें
transparencyPoints.get(2).setLocation(3000);

settings.setColorPoints(colorPoints.toArray(new IGradientColorPoint[0]));
settings.setTransparencyPoints(transparencyPoints.toArray(new IGradientTransparencyPoint[0]));
```

## चरण 6: PSD फ़ाइल को अपडेट करें और सेव करें

एक बार जब आप आवश्यक संशोधन कर लें, तो भरण परत को अपडेट करें और PSD फ़ाइल को सेव करें:

```java
fillLayer.update();
image.save(outputFile, new PsdOptions(image));
```

`fillLayer.update()` विधि ग्रेडिएंट भरण परत पर परिवर्तन लागू करती है, और`image.save` संशोधित PSD फ़ाइल को निर्दिष्ट आउटपुट पथ पर सहेजता है।

## निष्कर्ष

आपने Aspose.PSD for Java का उपयोग करके PSD फ़ाइलों में ग्रेडिएंट फिल लेयर्स को संशोधित करने की कला में सफलतापूर्वक महारत हासिल कर ली है! इन चरणों का पालन करके, आप अपनी रचनात्मकता को उजागर कर सकते हैं और प्रोग्रामेटिक परिशुद्धता के साथ आश्चर्यजनक दृश्य प्रभाव बना सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### क्या मैं ग्रेडिएंट में एकाधिक रंग और पारदर्शिता बिंदु जोड़ सकता हूँ?
बिल्कुल! आप वांछित ग्रेडिएंट प्रभाव प्राप्त करने के लिए जितने आवश्यक हो उतने रंग और पारदर्शिता बिंदु जोड़ सकते हैं। बस नए बिंदु बनाएं और उन्हें संबंधित सूचियों में जोड़ें।

### मैं ग्रेडिएंट से रंग या पारदर्शिता बिंदु कैसे हटाऊं?
 किसी बिंदु को हटाने के लिए, उपयुक्त सूची का उपयोग करें`remove` विधि। उदाहरण के लिए,`colorPoints.remove(index)` निर्दिष्ट सूचकांक पर रंग बिंदु को हटा देगा।

### क्या मैं ग्रेडिएंट का प्रकार (रैखिक, रेडियल, आदि) बदल सकता हूँ?
Aspose.PSD वर्तमान में रैखिक ग्रेडिएंट का समर्थन करता है। जबकि भविष्य के संस्करणों में अन्य ग्रेडिएंट प्रकारों का समर्थन किया जा सकता है, आप रंग और पारदर्शिता बिंदुओं को रचनात्मक रूप से जोड़कर समान प्रभाव प्राप्त कर सकते हैं।

### क्या ग्रेडिएंट संशोधित करने पर प्रदर्शन पर कोई प्रभाव पड़ता है?
प्रदर्शन प्रभाव ग्रेडिएंट की जटिलता और किए गए संशोधनों की संख्या पर निर्भर करता है। अधिकांश व्यावहारिक उपयोग मामलों के लिए, प्रदर्शन स्वीकार्य होना चाहिए। हालाँकि, बड़े पैमाने पर छवि प्रसंस्करण के लिए, दक्षता के लिए अपने कोड को अनुकूलित करने पर विचार करें।

### क्या मैं इस तकनीक को PSD फ़ाइल में एकाधिक ग्रेडिएंट भरण परतों पर लागू कर सकता हूँ?
हां, आप परतों के माध्यम से पुनरावृति कर सकते हैं और अपने मानदंडों को पूरा करने वाले प्रत्येक ग्रेडिएंट भरण परत पर संशोधन लागू कर सकते हैं।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
