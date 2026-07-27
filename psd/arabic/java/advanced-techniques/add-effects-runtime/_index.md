---
date: 2026-07-27
description: استكشف image manipulation في Java باستخدام Aspose.PSD for Java وتعلم
  كيفية إضافة effects أثناء runtime. يوضح لك هذا الدليل خطوة بخطوة كيفية إضافة effects
  إلى الصور.
keywords:
- java image manipulation
- apply layer effects
- add drop shadow
- batch image processing
- apply glow effect
lastmod: 2026-07-27
linktitle: إضافة Effects أثناء Runtime
og_description: معالجة الصور في Java أصبحت سهلة. تعلم كيفية إضافة layer effects، drop
  shadows، و color overlays أثناء runtime باستخدام Aspose.PSD for Java. اتبع الدليل
  خطوة بخطوة.
og_image_alt: 'Developer guide: Adding effects to PSD images in Java with Aspose.PSD'
og_title: معالجة الصور في Java – إضافة Effects أثناء Runtime باستخدام Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-07-27'
  description: Explore java image manipulation with Aspose.PSD for Java and learn
    how to add effects at runtime. This tutorial shows you step‑by‑step how to add
    effects to images.
  headline: Java Image Manipulation – Add Effects at Runtime with Aspose.PSD
  type: TechArticle
- description: Explore java image manipulation with Aspose.PSD for Java and learn
    how to add effects at runtime. This tutorial shows you step‑by‑step how to add
    effects to images.
  name: Java Image Manipulation – Add Effects at Runtime with Aspose.PSD
  steps:
  - name: '**Java Development Kit (JDK)** – Ensure that you have Java installed on
      your system. You can download the latest JDK from [here](https://www.oracle.com/java/technologies/javase-downloads.html).'
    text: '**Java Development Kit (JDK)** – Ensure that you have Java installed on
      your system. You can download the latest JDK from [here](https://www.oracle.com/java/technologies/javase-downloads.html).'
  - name: '**Aspose.PSD for Java Library** – You need to have the Aspose.PSD for Java
      library. If you haven''t already, download it from the [Aspose.PSD Java documentation](https://reference.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java Library** – You need to have the Aspose.PSD for Java
      library. If you haven''t already, download it from the [Aspose.PSD Java documentation](https://reference.aspose.com/psd/java/).'
  - name: '**Document Directory** – Set up a directory for your documents, and remember
      the path. In the provided example, the directory is referred to as `Your Document
      Directory`.'
    text: '**Document Directory** – Set up a directory for your documents, and remember
      the path. In the provided example, the directory is referred to as `Your Document
      Directory`.'
  type: HowTo
- questions:
  - answer: Yes, you can chain calls such as `addDropShadow()`, `addInnerGlow()`,
      etc., on the same layer’s blending options.
    question: Can I apply multiple effects to a single layer?
  - answer: Yes, Aspose.PSD supports PSD, BMP, JPEG, PNG, TIFF, and more, allowing
      you to convert between formats after manipulation.
    question: Is Aspose.PSD compatible with various image formats?
  - answer: You can obtain a temporary license from [here](https://purchase.aspose.com/temporary-license/).
    question: How can I get a temporary license for Aspose.PSD for Java?
  - answer: Visit the Aspose.PSD [support forum](https://forum.aspose.com/c/psd/34)
      to get help and connect with the community.
    question: Where can I seek assistance for any issues or queries related to Aspose.PSD?
  - answer: Yes, you can explore the free trial version [here](https://releases.aspose.com/).
    question: Is there a free trial available for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image manipulation
- Aspose.PSD
- Java graphics processing
- layer effects
title: معالجة الصور في Java – إضافة Effects أثناء Runtime باستخدام Aspose.PSD
url: /ar/java/advanced-techniques/add-effects-runtime/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تلاعب الصور في Java – إضافة تأثيرات في وقت التشغيل باستخدام Aspose.PSD

## مقدمة

تلاعب الصور في Java هو طلب شائع عندما تحتاج إلى تحسين الرسومات برمجياً، إنشاء صور مصغرة، أو تطبيق تراكبات العلامة التجارية. مع **Aspose.PSD for Java**، مكتبة تدعم أكثر من 50 تنسيق ملف ويمكنها معالجة ملفات PSD مئات الصفحات دون تحميل المستند بالكامل في الذاكرة، يمكنك **إضافة تأثيرات في وقت التشغيل** ببضع أسطر من الشيفرة فقط. يشرح هذا الدرس سير العمل بالكامل، يوضح لماذا كل خطوة مهمة، ويشارك نصائح عملية لتتمكن من بدء استخدام تأثيرات الطبقة فوراً.

## إجابات سريعة
- **ما المكتبة التي تساعد في تلاعب الصور في Java؟** Aspose.PSD for Java.  
- **هل يمكنني إضافة تأثيرات في وقت التشغيل؟** نعم—استخدم API تأثيرات الطبقة لتطبيق تراكبات لونية، ظلال، توهجات، وأكثر.  
- **هل أحتاج إلى ترخيص للتطوير؟** ترخيص مؤقت يعمل للاختبار؛ ترخيص كامل مطلوب للإنتاج.  
- **ما نسخة JDK المطلوبة؟** أي JDK حديث (8+).  
- **أين يمكنني تنزيل نسخة تجريبية مجانية؟** من صفحة تنزيل Aspose.PSD (الرابط في المتطلبات المسبقة).  

## ما هو تلاعب الصور في Java؟

تلاعب الصور في Java هو الإنشاء أو التحرير أو تحسين الرسومات النقطية برمجياً باستخدام مكتبات Java. يشمل ذلك مهام مثل تغيير الحجم، الترشيح، دمج الطبقات، وتطبيق التأثيرات البصرية—وهي قدرات توفرها Aspose.PSD لملفات PSD بأسلوب Photoshop مع الحفاظ على الطبقات، الأقنعة، وبيانات التعديل.

## لماذا تستخدم Aspose.PSD لتلاعب الصور في Java؟

يمكنك إضافة أو تعديل أو إزالة تأثيرات الطبقة فوراً دون الحاجة لتثبيت Photoshop، وتقوم المكتبة بمعالجة ملفات تصل إلى 200 ميغابايت مع الحفاظ على استهلاك الذاكرة أقل من 150 ميغابايت. تدعم **أكثر من 50 تنسيق إدخال وإخراج** (بما في ذلك PSD، BMP، JPEG، PNG، TIFF) وتعمل على أي نظام تشغيل يدعم Java 8 أو أعلى، مما يمنحك مرونة حقيقية عبر المنصات.

## لماذا هذا مهم للمطورين؟

إضافة تأثيرات في وقت التشغيل تتيح لك بناء محركات رسومية ديناميكية تُخصص الصور حسب طلب المستخدم، توليد صور مصغرة مصقولة بظلال، أو إنشاء علامات مائية في الوقت الفعلي—كل ذلك دون الحاجة إلى عمل يدوي في Photoshop. هذه القدرة تقلل وقت التطوير حتى 70 % للتطبيقات التي تعتمد على الصور وتلغي الحاجة إلى أدوات تصميم خارجية مكلفة.

## حالات الاستخدام الشائعة
| حالة الاستخدام | الفائدة |
|----------|---------|
| **محتوى يولده المستخدم** | تطبيق ألوان العلامة التجارية أو التراكبات فوراً. |
| **إنشاء صور مصغرة تلقائيًا** | إضافة ظلال أو توهجات للحصول على مظهر مصقول. |
| **سمات واجهة مستخدم ديناميكية** | تبديل تأثيرات الطبقة بناءً على تفضيلات المستخدم. |
| **خطوط معالجة دفعة** | تحسين مجموعات الصور الكبيرة برمجياً. |

## المتطلبات المسبقة

قبل الخوض في الدرس، تأكد من توفر المتطلبات التالية:

1. **Java Development Kit (JDK)** – تأكد من تثبيت Java على نظامك. يمكنك تنزيل أحدث JDK من [here](https://www.oracle.com/java/technologies/javase-downloads.html).

2. **Aspose.PSD for Java Library** – تحتاج إلى مكتبة Aspose.PSD for Java. إذا لم تقم بذلك بعد، قم بتنزيلها من [Aspose.PSD Java documentation](https://reference.aspose.com/psd/java/).

3. **Document Directory** – أنشئ دليلًا لمستنداتك، وتذكر المسار. في المثال المقدم، يُشار إلى الدليل باسم `Your Document Directory`.

## استيراد الحزم

الاستيرادات التالية تجلب الفئات الأساسية من Aspose.PSD اللازمة لتلاعب الصور.  
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.layereffects.ColorOverlayEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## الخطوة 1: تحميل صورة PSD

`PsImage` هي الفئة الأساسية المستخدمة لتحميل ملف PSD إلى الذاكرة للمعالجة.  
```java
String sourceFileName = "Your Document Directory/ThreeRegularLayers.psd";
String exportPath = "Your Document Directory/ThreeRegularLayersChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## الخطوة 2: إضافة تأثير تراكب اللون

`ColorOverlayEffect` يحدد تراكب لون يمكن تطبيقه على خيارات المزج للطبقة.  
```java
ColorOverlayEffect effect = im.getLayers()[1].getBlendingOptions().addColorOverlay();
effect.setColor(Color.getGreen());
effect.setOpacity((byte)128);
effect.setBlendMode(BlendMode.Normal);
```

## الخطوة 3: حفظ الصورة المعدلة

طريقة `save` تكتب ملف PSD المعدل أو الصورة المصدرة إلى مسار الملف المحدد.  
```java
im.save(exportPath);
```

تهانينا! لقد نجحت في إضافة تأثيرات في وقت التشغيل باستخدام Aspose.PSD for Java، وهي تقنية أساسية في تلاعب الصور الحديثة في Java.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|-----|
| **التأثير غير مرئي** | تم حذف `loadOptions.setLoadEffectsResource(true)` | تأكد من ضبط العلامة قبل تحميل PSD. |
| **الشفافية تبدو خاطئة** | استخدام `byte` موقع بقيم >127 | قم بالتحويل إلى `(byte)128` كما هو موضح، أو استخدم int غير موقع وقسم على 255. |
| **فهرس الطبقة خارج النطاق** | رقم طبقة خاطئ | تحقق من ترتيب الطبقات باستخدام `im.getLayers().length` أو افحص PSD في Photoshop. |

## الأسئلة المتكررة

**س: هل يمكنني تطبيق تأثيرات متعددة على طبقة واحدة؟**  
ج: نعم، يمكنك ربط الاستدعاءات مثل `addDropShadow()`, `addInnerGlow()`, إلخ، على خيارات المزج لنفس الطبقة.

**س: هل Aspose.PSD متوافق مع صيغ صور مختلفة؟**  
ج: نعم، يدعم Aspose.PSD صيغ PSD، BMP، JPEG، PNG، TIFF، وأكثر، مما يتيح لك التحويل بين الصيغ بعد التلاعب.

**س: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD for Java؟**  
ج: يمكنك الحصول على ترخيص مؤقت من [here](https://purchase.aspose.com/temporary-license/).

**س: أين يمكنني طلب المساعدة لأي مشكلات أو استفسارات تتعلق بـ Aspose.PSD؟**  
ج: زر منتدى دعم Aspose.PSD [support forum](https://forum.aspose.com/c/psd/34) للحصول على المساعدة والتواصل مع المجتمع.

**س: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.PSD for Java؟**  
ج: نعم، يمكنك استكشاف النسخة التجريبية المجانية [here](https://releases.aspose.com/).

---

**آخر تحديث:** 2026-07-27  
**تم الاختبار مع:** Aspose.PSD for Java 24.11  
**المؤلف:** Aspose

## دروس ذات صلة

- [كيفية تطبيق تأثيرات التدرج في Aspose.PSD for Java](/psd/java/advanced-image-effects/add-gradient-effects/)
- [إضافة تأثيرات تراكب النمط في Aspose.PSD for Java](/psd/java/advanced-image-effects/add-pattern-effects/)
- [كيفية إضافة ظل داخلي PSD Java – تأثيرات الطبقة المتقدمة](/psd/java/advanced-psd-layer-features-effects/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}