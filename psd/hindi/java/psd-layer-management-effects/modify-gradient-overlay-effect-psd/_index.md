---
date: 2026-04-05
description: जानेँ कि कैसे ग्रेडिएंट ओवरले जावा को संशोधित करके Aspose.PSD for Java
  का उपयोग करके PSD फ़ाइल में ग्रेडिएंट ओवरले इफ़ेक्ट को संपादित किया जाए और प्रोग्रामेटिकली
  ग्रेडिएंट ओवरले PSD लेयर्स जोड़ी जाएँ।
keywords:
- modify gradient overlay java
- add gradient overlay psd
- Aspose.PSD Java
- PSD layer effects
- gradient overlay effect
linktitle: जावा का उपयोग करके पीएसडी में ग्रेडिएंट ओवरले इफ़ेक्ट को संशोधित करें
second_title: Aspose.PSD Java API
title: ग्रेडिएंट ओवरले जावा को संशोधित करें – जावा का उपयोग करके पीएसडी में ग्रेडिएंट
  ओवरले प्रभाव को संशोधित करें
url: /hi/java/psd-layer-management-effects/modify-gradient-overlay-effect-psd/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ग्रेडिएंट ओवरले जावा संशोधित करें – PSD में ग्रेडिएंट ओवरले प्रभाव को जावा का उपयोग करके संशोधित करें

## परिचय

इस ट्यूटोरियल में आप सीखेंगे कि **modify gradient overlay java** का उपयोग करके Photoshop (PSD) फ़ाइल में ग्रेडिएंट ओवरले प्रभाव को कैसे बदलें, Aspose.PSD for Java का उपयोग करके। चाहे आप दोहरावदार डिज़ाइन कार्यों को स्वचालित कर रहे हों या एक कस्टम इमेज‑प्रोसेसिंग पाइपलाइन बना रहे हों, इस तकनीक में महारत हासिल करने से आप बिना Photoshop खोले ही पेशेवर स्पर्श जोड़ सकते हैं।

## त्वरित उत्तर
- **मुझे कौन सी लाइब्रेरी चाहिए?** Aspose.PSD for Java (download **[here](https://releases.aspose.com/psd/java/)**).  
- **कौन सा Java संस्करण आवश्यक है?** JDK 1.8 or later.  
- **क्या मैं किसी भी लेयर पर ग्रेडिएंट ओवरले जोड़ सकता हूँ?** Yes – just target the desired layer index.  
- **क्या उत्पादन के लिए लाइसेंस आवश्यक है?** Yes, a commercial license is needed for non‑evaluation use.  
- **इम्प्लीमेंटेशन में कितना समय लगता है?** Roughly 10‑15 minutes for a basic setup.

## “modify gradient overlay java” क्या है?

Java में ग्रेडिएंट ओवरले को संशोधित करना मतलब प्रोग्रामेटिक रूप से PSD लेयर के ऊपर स्थित दृश्य ग्रेडिएंट को समायोजित करना है। इससे आप रंग, अपारदर्शिता, ब्लेंड मोड, कोण, और स्केल को Photoshop में मैन्युअल संपादन के बिना बदल सकते हैं।

## ग्रेडिएंट ओवरले PSD लेयर्स जोड़ने के लिए Aspose.PSD क्यों उपयोग करें?

- **ऑटोमेशन:** बैच जॉब में दर्जनों PSD फ़ाइलों को प्रोसेस करें।  
- **सटीकता:** अपारदर्शिता, कोण, और रंग स्टॉप्स के लिए सटीक संख्यात्मक मान सेट करें।  
- **क्रॉस‑प्लेटफ़ॉर्म:** वही कोड Windows, Linux, या macOS पर चलाएँ।  
- **Photoshop की आवश्यकता नहीं:** सर्वर‑साइड रेंडरिंग या CI पाइपलाइन के लिए आदर्श।

## आवश्यकताएँ

- Aspose.PSD for Java लाइब्रेरी – ऊपर दिए लिंक से डाउनलोड करें।  
- Java Development Kit (JDK) 1.8+ स्थापित हो।  
- IntelliJ IDEA या Eclipse जैसे IDE।  
- एक नमूना PSD फ़ाइल जिसमें कम से कम एक लेयर हो जिसे आप **संपादित करना चाहते हैं**।  
- Java सिंटैक्स की बुनियादी परिचितता।

एक बार जब आप चेकलिस्ट की पुष्टि कर लें, हम कोड में डुबकी लगा सकते हैं।

## पैकेज आयात करें

पहले, उन क्लासों को इम्पोर्ट करें जो हमें PSD हैंडलिंग, लेयर इफ़ेक्ट्स, और ग्रेडिएंट सेटिंग्स तक पहुँच प्रदान करती हैं।

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

## ग्रेडिएंट ओवरले जावा संशोधित करने के चरण 1: PSD फ़ाइल लोड करें

`PsdLoadOptions` के साथ फ़ाइल लोड करने से मौजूदा सभी इफ़ेक्ट्स संरक्षित रहते हैं।

```java
String sourceDir = "Your Source Directory";
String inPsdFilePath = sourceDir + "psdnet256.psd";

// Enable support for existing layer effects
PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
psdLoadOptions.setLoadEffectsResource(true);

// Load the PSD file
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath, psdLoadOptions);
```

## ग्रेडिएंट ओवरले PSD जोड़ने के चरण 2: लक्ष्य लेयर खोजें

उस लेयर की पहचान करें जिसे आप संपादित करना चाहते हैं। इस उदाहरण में हम दूसरे लेयर (`[1]`) के साथ काम करेंगे।

```java
BlendingOptions layerBlendOptions = psdImage.getLayers()[1].getBlendingOptions();
```

## चरण 3: मौजूदा ग्रेडिएंट ओवरले प्रभाव खोजें

हम या तो मौजूदा इफ़ेक्ट को प्राप्त करते हैं या यदि वह मौजूद नहीं है तो नया बनाते हैं।

```java
GradientOverlayEffect gradientOverlayEffect = null;
for (ILayerEffect effect : layerBlendOptions.getEffects()) {
    if (effect instanceof GradientOverlayEffect) {
        gradientOverlayEffect = (GradientOverlayEffect) effect;
        break;
    }
}

if (gradientOverlayEffect == null) {
    // Create a new GradientOverlayEffect if it doesn't exist
    gradientOverlayEffect = layerBlendOptions.addGradientOverlay();
}
```

## चरण 4: ग्रेडिएंट ओवरले प्रभाव संशोधित करें

### अपारदर्शिता और ब्लेंड मोड सेट करें

```java
gradientOverlayEffect.setOpacity((byte) 200);
gradientOverlayEffect.setBlendMode(BlendMode.Hue);
```

### ग्रेडिएंट रंग और सेटिंग्स को अनुकूलित करें

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

## चरण 5: संशोधित PSD फ़ाइल सहेजें

अंत में, बदलावों को नई फ़ाइल में लिखें और संसाधनों को साफ़ करें।

```java
String outputDir = "Your Document Directory";
String outPsdFilePath = outputDir + "psdnet256.psd_output.psd";

psdImage.save(outPsdFilePath);
psdImage.dispose();
```

## सामान्य समस्याएँ और समाधान

- **सहेजने के बाद इफ़ेक्ट दिखाई नहीं दे रहा है:** सुनिश्चित करें कि लेयर इंडेक्स सही है और ब्लेंड मोड ऐसा नहीं है जो ग्रेडिएंट को छिपा दे (जैसे, `Normal` 0 % अपारदर्शिता के साथ)।  
- **रंग बिंदु उल्टे दिख रहे हैं:** `GradientColorPoint` ऑब्जेक्ट्स का क्रम शुरू‑से‑अंत को परिभाषित करता है; यदि ग्रेडिएंट दिशा अपेक्षा के विपरीत है तो उन्हें बदलें।  
- **लोड करने पर अपवाद:** सुनिश्चित करें कि `psdLoadOptions.setLoadEffectsResource(true)` कॉल किया गया है; अन्यथा मौजूदा इफ़ेक्ट्स को अनदेखा किया जा सकता है, जिससे `null` रेफ़रेंसेज़ मिलेंगी।

## अक्सर पूछे जाने वाले प्रश्न

### क्या मैं एक ही लेयर पर कई ग्रेडिएंट ओवरले लागू कर सकता हूँ?
हाँ, आप लेयर के ब्लेंडिंग विकल्पों में नए `GradientOverlayEffect` इंस्टेंस जोड़कर एक ही लेयर पर कई ग्रेडिएंट ओवरले लागू कर सकते हैं।

### क्या लेयर से ग्रेडिएंट ओवरले प्रभाव हटाना संभव है?
बिल्कुल! आप लेयर के ब्लेंडिंग विकल्पों से संबंधित इफ़ेक्ट को हटाकर मौजूदा ग्रेडिएंट ओवरले प्रभाव को हटा सकते हैं।

### Aspose.PSD for Java का उपयोग करके मैं कौन से अन्य प्रभाव लागू कर सकता हूँ?
Aspose.PSD for Java आपको विभिन्न प्रभाव लागू करने की अनुमति देता है, जैसे ड्रॉप शैडो, इनर ग्लो, आउटर ग्लो, आदि। आप प्रत्येक प्रभाव को अपनी आवश्यकता के अनुसार कस्टमाइज़ कर सकते हैं।

### मैं PSD फ़ाइल में किए गए बदलावों को कैसे वापस ले सकता हूँ?
यदि आपने फ़ाइल अभी तक सहेजी नहीं है, तो आप मूल PSD फ़ाइल को पुनः लोड कर सकते हैं। यदि आपने पहले ही सहेज ली है, तो आपको बैकअप से पुनर्स्थापित करना होगा या प्रोग्रामेटिक रूप से बदलावों को वापस करना होगा।

## अक्सर पूछे जाने वाले प्रश्न

**प्रश्न:** क्या यह उन PSD फ़ाइलों के साथ काम करता है जिनमें स्मार्ट ऑब्जेक्ट्स होते हैं?  
**उत्तर:** हाँ, लेकिन स्मार्ट ऑब्जेक्ट्स को सामान्य लेयर्स की तरह माना जाता है; ग्रेडिएंट ओवरले रास्टराइज़्ड प्रतिनिधित्व को प्रभावित करेगा।

**प्रश्न:** क्या मैं विभिन्न ब्लेंड मोड्स के साथ कई ग्रेडिएंट ओवरले को चेन कर सकता हूँ?  
**उत्तर:** बिल्कुल। प्रत्येक `GradientOverlayEffect` का अपना ब्लेंड मोड हो सकता है, जिससे जटिल विज़ुअल कंपोज़िशन संभव होते हैं।

**प्रश्न:** क्या संशोधित करने से पहले वर्तमान ग्रेडिएंट सेटिंग्स पढ़ने का कोई तरीका है?  
**उत्तर:** हाँ। मौजूदा `GradientFillSettings` को प्राप्त करने और उसकी प्रॉपर्टीज़ जांचने के लिए `gradientOverlayEffect.getSettings()` का उपयोग करें।

**प्रश्न:** क्या संशोधित PSD Photoshop के साथ संगतता बनाए रखेगा?  
**उत्तर:** सहेजी गई फ़ाइल PSD स्पेसिफिकेशन का पालन करती है, इसलिए Photoshop इसे बिना किसी समस्या के खोल देगा और नया या संपादित ग्रेडिएंट ओवरले संरक्षित रहेगा।

**प्रश्न:** क्या विकास बिल्ड्स के लिए मुझे व्यावसायिक लाइसेंस चाहिए?  
**उत्तर:** परीक्षण के लिए एक मुफ्त इवैल्यूएशन लाइसेंस पर्याप्त है, लेकिन उत्पादन डिप्लॉयमेंट के लिए खरीदा हुआ लाइसेंस आवश्यक है।

**अंतिम अपडेट:** 2026-04-05  
**परीक्षण किया गया:** Aspose.PSD for Java 24.11  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}