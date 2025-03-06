---
title: जावा का उपयोग करके PSD में ग्रेडिएंट ओवरले प्रभाव संशोधित करें
linktitle: जावा का उपयोग करके PSD में ग्रेडिएंट ओवरले प्रभाव संशोधित करें
second_title: Aspose.PSD जावा एपीआई
description: Aspose.PSD for Java का उपयोग करके PSD फ़ाइल में ग्रेडिएंट ओवरले प्रभाव को संशोधित करना सीखें। अपनी PSD फ़ाइलों को कुशलतापूर्वक स्वचालित और अनुकूलित करने के लिए हमारे गाइड का पालन करें।
weight: 12
url: /hi/java/psd-layer-management-effects/modify-gradient-overlay-effect-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# जावा का उपयोग करके PSD में ग्रेडिएंट ओवरले प्रभाव संशोधित करें

## परिचय

क्या आप जावा के साथ डिजिटल कलाकारी की दुनिया में उतरने के लिए तैयार हैं? यदि आप फ़ोटोशॉप फ़ाइलों (PSD) के साथ काम कर रहे हैं और उन्हें प्रोग्रामेटिक रूप से हेरफेर करना चाहते हैं, तो आपके लिए यह एक बेहतरीन अनुभव है। आज, हम यह पता लगाने जा रहे हैं कि Aspose.PSD for Java का उपयोग करके PSD फ़ाइल में ग्रेडिएंट ओवरले प्रभाव को कैसे संशोधित किया जाए। चाहे आप एक डेवलपर हों जो ग्राफ़िक डिज़ाइन कार्यों को स्वचालित करना चाहते हों या कोई ऐसा व्यक्ति जो इस प्रक्रिया के बारे में उत्सुक हो, यह ट्यूटोरियल आपको चरण दर चरण मार्गदर्शन करेगा। अंत में, आपके पास फ़ोटोशॉप खोले बिना अपनी छवियों में एक पेशेवर स्पर्श जोड़ने का ज्ञान होगा।

## आवश्यक शर्तें

शुरू करने से पहले, आइए सुनिश्चित करें कि आपके पास वह सब कुछ है जिसकी आपको ज़रूरत है। यहाँ एक त्वरित चेकलिस्ट दी गई है:

-  Aspose.PSD for Java लाइब्रेरी: आपको Aspose.PSD for Java लाइब्रेरी की आवश्यकता होगी। यदि आपके पास अभी तक यह नहीं है, तो आप इसे यहाँ से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/psd/java/).
- जावा डेवलपमेंट किट (JDK): सुनिश्चित करें कि आपके मशीन पर JDK 1.8 या बाद का संस्करण स्थापित है।
- एकीकृत विकास वातावरण (IDE): कोई भी जावा IDE, जैसे कि IntelliJ IDEA या Eclipse, पूरी तरह से काम करेगा।
- सैंपल PSD फ़ाइल: एक सैंपल PSD फ़ाइल लें जिसमें एक लेयर हो जहाँ आप ग्रेडिएंट ओवरले लगा सकें। आप अपनी खुद की फ़ाइल का उपयोग कर सकते हैं या वेब से एक टेस्ट PSD डाउनलोड कर सकते हैं।
- जावा का बुनियादी ज्ञान: यद्यपि मैं आपको प्रत्येक चरण में मार्गदर्शन करूंगा, जावा की बुनियादी समझ आपको अधिक आसानी से अनुसरण करने में मदद करेगी।

एक बार जब आप सब कुछ सेट कर लेंगे, तो हम कोड में कूदने के लिए तैयार हैं!

## पैकेज आयात करें

सबसे पहले, आइए सुनिश्चित करें कि हमने सभी आवश्यक पैकेज आयात कर लिए हैं। ये आयात आपको PSD फ़ाइल के साथ काम करने, प्रभाव लागू करने और अपनी संशोधित फ़ाइल को सहेजने में सक्षम करेंगे।

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientType;
import com.aspose.psd.fileformats.psd.layers.layereffects.BlendingOptions;
import com.aspose.psd.fileformats.psd.layers.layereffects.GradientOverlayEffect;
import com.aspose.psd.fileformats.psd.layers.layereffects.ILayerEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## चरण 1: PSD फ़ाइल लोड करें

ग्रेडिएंट ओवरले इफ़ेक्ट को संशोधित करने का पहला चरण PSD फ़ाइल लोड करना है। यहीं पर Aspose.PSD for Java काम आता है। आप फ़ाइल लोड करेंगे, यह सुनिश्चित करते हुए कि किसी भी मौजूदा लेयर इफ़ेक्ट के लिए समर्थन सक्षम है।

```java
String sourceDir = "Your Source Directory";
String inPsdFilePath = sourceDir + "psdnet256.psd";

//मौजूदा परत प्रभावों के लिए समर्थन सक्षम करें
PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
psdLoadOptions.setLoadEffectsResource(true);

// PSD फ़ाइल लोड करें
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath, psdLoadOptions);
```

 स्पष्टीकरण: हम फ़ाइल पथ सेट करके और PSD फ़ाइल लोड करके शुरू करते हैं।`PsdLoadOptions` यहाँ ऑब्जेक्ट बहुत ज़रूरी है क्योंकि यह आपको PSD फ़ाइल को उसके सभी मौजूदा लेयर इफ़ेक्ट के साथ लोड करने की अनुमति देता है। यह सुनिश्चित करता है कि आपके द्वारा किए गए कोई भी संशोधन सही लेयर पर सही तरीके से लागू होंगे।

## चरण 2: लक्ष्य परत का पता लगाएँ

अब जब आपने PSD फ़ाइल लोड कर ली है, तो अगला चरण वह विशिष्ट परत ढूँढना है जहाँ आप ग्रेडिएंट ओवरले प्रभाव लागू करना या संशोधित करना चाहते हैं। यह चरण महत्वपूर्ण है क्योंकि फ़ोटोशॉप फ़ाइलों में परतों में विभिन्न प्रकार की सामग्री हो सकती है, और आप यह सुनिश्चित करना चाहते हैं कि आप सही परत को लक्षित कर रहे हैं।

```java
BlendingOptions layerBlendOptions = psdImage.getLayers()[1].getBlendingOptions();
```

स्पष्टीकरण: इस उदाहरण में, हम PSD फ़ाइल में दूसरी परत तक पहुँच रहे हैं (`psdImage.getLayers()[1]` ) द`BlendingOptions` ऑब्जेक्ट आपको लेयर के ब्लेंडिंग विकल्पों तक पहुँच प्रदान करता है, जहाँ ग्रेडिएंट ओवरले जैसे प्रभाव प्रबंधित किए जाते हैं। यदि आपको किसी अलग लेयर के साथ काम करने की आवश्यकता है, तो बस इंडेक्स को समायोजित करें`[1]`उपयुक्त परत संख्या तक.

## चरण 3: मौजूदा ग्रेडिएंट ओवरले प्रभाव की खोज करें

एक बार जब आप लक्ष्य परत की पहचान कर लेते हैं, तो यह जाँचने का समय आ जाता है कि क्या पहले से ही कोई ग्रेडिएंट ओवरले प्रभाव लागू है। अगर है, तो आप इसे संशोधित करेंगे। अगर नहीं है, तो आप एक नया बनाएँगे।

```java
GradientOverlayEffect gradientOverlayEffect = null;
for (ILayerEffect effect : layerBlendOptions.getEffects()) {
    if (effect instanceof GradientOverlayEffect) {
        gradientOverlayEffect = (GradientOverlayEffect) effect;
        break;
    }
}

if (gradientOverlayEffect == null) {
    // यदि यह मौजूद नहीं है तो एक नया GradientOverlayEffect बनाएं
    gradientOverlayEffect = layerBlendOptions.addGradientOverlay();
}
```

 स्पष्टीकरण: कोड का यह ब्लॉक परत पर लागू सभी प्रभावों के माध्यम से लूप करता है, एक खोज करता है`GradientOverlayEffect` . अगर यह एक मिल जाता है, तो बढ़िया! आप इसे संशोधित करने के लिए आगे बढ़ सकते हैं। यदि नहीं, तो आप इसका उपयोग करके एक नया ग्रेडिएंट ओवरले प्रभाव बनाते हैं`addGradientOverlay()` विधि। यह लचीलापन सुनिश्चित करता है कि आपका कोड दोनों परिदृश्यों को संभाल सकता है - मौजूदा प्रभावों को संशोधित करना या नए जोड़ना।

## चरण 4: ग्रेडिएंट ओवरले प्रभाव को संशोधित करें

अब आता है मज़ेदार हिस्सा—ग्रेडिएंट ओवरले इफ़ेक्ट को कस्टमाइज़ करना। यह वह चरण है जहाँ आप रचनात्मक हो सकते हैं, अपारदर्शिता, ब्लेंड मोड, ग्रेडिएंट रंग और बहुत कुछ बदल सकते हैं।

### अपारदर्शिता और मिश्रण मोड सेट करें

```java
gradientOverlayEffect.setOpacity((byte) 200);
gradientOverlayEffect.setBlendMode(BlendMode.Hue);
```

स्पष्टीकरण: यहाँ, हम ग्रेडिएंट ओवरले की अपारदर्शिता को 200 (0 से 255 के पैमाने पर) पर सेट कर रहे हैं और ब्लेंड मोड को बदल रहे हैं`Hue`ब्लेंड मोड यह निर्धारित करता है कि ग्रेडिएंट परत की मौजूदा सामग्री के साथ कैसे इंटरैक्ट करेगा।

### ग्रेडिएंट रंग और सेटिंग अनुकूलित करें

```java
GradientFillSettings settings = gradientOverlayEffect.getSettings();
settings.setColorPoints(new IGradientColorPoint[]{
        new GradientColorPoint(Color.getGreenYellow(), 0, 50),
        new GradientColorPoint(Color.getBlueViolet(), 4096, 50),
});
settings.setAngle(80);
settings.setScale(150);
settings.setGradientType(GradientType.Linear);
settings.getTransparencyPoints()[0].setOpacity(100);
settings.getTransparencyPoints()[1].setOpacity(100);
```

 स्पष्टीकरण:`GradientFillSettings` ऑब्जेक्ट आपको ग्रेडिएंट की विशिष्टताओं को कॉन्फ़िगर करने की अनुमति देता है। हम ग्रेडिएंट के लिए दो रंग बिंदु सेट कर रहे हैं - शुरुआत में हरा-पीला और अंत में नीला-बैंगनी। ग्रेडिएंट को 150% स्केल और 80-डिग्री कोण के साथ एक रैखिक प्रकार पर सेट किया गया है, जो ग्रेडिएंट की दिशा निर्धारित करता है। इसके अतिरिक्त, हमने प्रत्येक पारदर्शिता बिंदु की अपारदर्शिता को 100% पर सेट करके यह सुनिश्चित किया है कि ग्रेडिएंट पूरी तरह से अपारदर्शी है।

## चरण 5: संशोधित PSD फ़ाइल सहेजें

सभी संशोधनों के बाद, अंतिम चरण आपके काम को सहेजना है। यह सुनिश्चित करता है कि आपके परिवर्तन फ़ाइल में लिखे गए हैं, और आप अपने नए अनुकूलित PSD का उपयोग या साझा कर सकते हैं।

```java
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "psdnet256.psd_output.psd";

psdImage.save(outPsdFilePath);
psdImage.dispose();
```

स्पष्टीकरण: संशोधित PSD फ़ाइल निर्दिष्ट आउटपुट निर्देशिका में एक नए नाम के साथ सहेजी जाती है। अंत में,`dispose()` विधि को किसी भी संसाधन को जारी करने के लिए बुलाया जाता है जिसका उपयोग उपयोगकर्ता द्वारा किया जाता है।`PsdImage` यह सुनिश्चित करने के लिए एक अच्छा अभ्यास है कि आपका एप्लिकेशन कुशलतापूर्वक चलता है और अनावश्यक संसाधनों को धारण नहीं करता है।

## निष्कर्ष

और अब यह हो गया! आपने Aspose.PSD for Java का उपयोग करके PSD फ़ाइल में ग्रेडिएंट ओवरले प्रभाव को सफलतापूर्वक संशोधित कर लिया है। इस ट्यूटोरियल ने आपको PSD फ़ाइल लोड करने से लेकर नया ग्रेडिएंट लगाने और अपने काम को सहेजने तक की पूरी प्रक्रिया से गुज़ारा। इन चरणों का पालन करके, आपने अपने ग्राफ़िक डिज़ाइन कार्यों को प्रोग्रामेटिक रूप से स्वचालित और अनुकूलित करने का एक शक्तिशाली तरीका अनलॉक कर लिया है।

## अक्सर पूछे जाने वाले प्रश्न

### क्या मैं एक ही परत पर एकाधिक ग्रेडिएंट ओवरले लागू कर सकता हूँ?  
 हां, आप नए ग्रेडिएंट ओवरले जोड़कर एक ही परत पर कई ग्रेडिएंट ओवरले लागू कर सकते हैं`GradientOverlayEffect` परत के सम्मिश्रण विकल्पों के लिए उदाहरण।

### क्या किसी परत से ग्रेडिएंट ओवरले प्रभाव को हटाना संभव है?  
बिल्कुल! आप लेयर के ब्लेंडिंग विकल्पों से संबंधित प्रभाव को हटाकर मौजूदा ग्रेडिएंट ओवरले प्रभाव को हटा सकते हैं।

### मैं Java के लिए Aspose.PSD का उपयोग करके अन्य कौन से प्रभाव लागू कर सकता हूं?  
Aspose.PSD for Java आपको विभिन्न प्रभाव लागू करने की अनुमति देता है, जैसे ड्रॉप शैडो, इनर ग्लो, आउटर ग्लो, और बहुत कुछ। आप अपनी ज़रूरतों के हिसाब से हर प्रभाव को कस्टमाइज़ कर सकते हैं।

### मैं PSD फ़ाइल में किए गए परिवर्तनों को कैसे पूर्ववत करूँ?  
अगर आपने अभी तक फ़ाइल को सेव नहीं किया है, तो आप बस मूल PSD फ़ाइल को फिर से लोड कर सकते हैं। अगर आपने इसे पहले ही सेव कर लिया है, तो आपको बैकअप से रिस्टोर करना होगा या प्रोग्रामेटिक रूप से बदलावों को पूर्ववत करना होगा
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
