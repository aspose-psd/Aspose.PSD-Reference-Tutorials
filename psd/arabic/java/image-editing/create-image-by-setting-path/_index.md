---
date: 2026-01-01
description: تعلم كيفية إنشاء صور PSD في Java باستخدام Aspose.PSD. يوضح هذا الدليل
  كيفية تعيين المسار وإنشاء مستند فوتوشوب في Java مع كود خطوة بخطوة.
linktitle: Create Image by Setting Path
second_title: Aspose.PSD Java API
title: كيفية إنشاء ملف PSD – إنشاء صورة بتحديد المسار في Aspose.PSD للغة Java
url: /ar/java/image-editing/create-image-by-setting-path/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية إنشاء PSD – إنشاء صورة عن طريق تعيين المسار في Aspose.PSD للـ Java

## المقدمة

مرحبًا بك في هذا الدليل خطوة بخطوة حول **how to create PSD** باستخدام Aspose.PSD للـ Java. سنرشدك إلى تعيين مسار الملف، وتكوين الخيارات، وإنشاء مستند Photoshop برمجيًا. في النهاية، ستفهم كيفية **java create photoshop document** التي يمكن تعديلها لاحقًا أو دمجها في تطبيقاتك.

## إجابات سريعة
- **What does Aspose.PSD do?** يوفر API نقي للـ Java لقراءة وتحرير وإنشاء ملفات Photoshop (PSD) دون الحاجة إلى تثبيت Photoshop.  
- **Can I set a custom output path?** نعم – استخدم `FileCreateSource` لتحديد الموقع الدقيق واسم الملف.  
- **Which compression methods are supported?** RLE، ZIP، و RAW؛ هذا المثال يستخدم RLE للضغط غير الفاقد.  
- **Do I need a license for development?** نسخة تجريبية مجانية تعمل للاختبار؛ يلزم الحصول على ترخيص تجاري للإنتاج.  
- **What Java versions are supported?** Aspose.PSD يعمل مع Java 8 وما بعده.

## ما هو “how to create PSD”؟

إنشاء ملف PSD يعني توليد صورة متوافقة مع Photoshop تحتفظ بالطبقات والقنوات والبيانات الخاصة بـ Photoshop. Aspose.PSD يبسط تنسيق الملف المعقد، مما يتيح لك التركيز على منطق عملك.

## لماذا نستخدم Java لـ **java create photoshop document**؟

- **Cross‑platform** – Java يعمل في أي مكان، لذا يعمل توليد PSD الخاص بك على Windows أو Linux أو macOS.  
- **No Photoshop dependency** – إنشاء أو تعديل ملفات PSD دون تثبيت Adobe Photoshop.  
- **Full control** – تعيين الضغط، وضع اللون، الأبعاد، وأكثر من ذلك عبر نموذج كائن نظيف.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من أن لديك:

- معرفة أساسية ببرمجة Java.  
- مكتبة Aspose.PSD للـ Java مثبتة. يمكنك تنزيلها [هنا](https://releases.aspose.com/psd/java/).

## استيراد الحزم

ابدأ باستيراد الحزم اللازمة إلى مشروع Java الخاص بك:

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

## الخطوة 1: كيفية تعيين المسار لمجلد المستند

قم بإعداد المسار لمجلد المستند حيث سيتم إنشاء الصورة.

```java
String dataDir = "Your Document Directory";
```

## الخطوة 2: تحديد اسم ملف الإخراج

حدد اسم ملف الإخراج، بما في ذلك مجلد المستند.

```java
String desName = dataDir + "CreatingAnImageBySettingPath_out.psd";
```

## الخطوة 3: تكوين PsdOptions

أنشئ مثيلًا من `PsdOptions` وقم بتكوين خصائصه، مثل طريقة الضغط.

```java
PsdOptions psdOptions = new PsdOptions();
psdOptions.setCompressionMethod(CompressionMethod.RLE);
```

## الخطوة 4: تعيين خاصية Source

حدد خاصية المصدر لمثيل `PsdOptions`، مع تحديد ملف الإخراج وما إذا كان مؤقتًا.

```java
psdOptions.setSource(new FileCreateSource(desName, false));
```

## الخطوة 5: إنشاء الصورة

أنشئ مثيلًا من `Image` واستدعِ طريقة `create` بتمرير كائن `PsdOptions` وأبعاد الصورة.

```java
Image image = Image.create(psdOptions, 500, 500);
```

## الخطوة 6: حفظ الصورة

احفظ الصورة التي تم إنشاؤها.

```java
image.save();
```

كرر هذه الخطوات، وستكون قد أنشأت صورة بنجاح باستخدام Aspose.PSD للـ Java عن طريق تعيين المسار.

## المشكلات الشائعة والنصائح

- **Invalid directory** – تأكد من أن `dataDir` ينتهي بفاصل الملفات المناسب (`/` أو `\\`).  
- **Permission errors** – شغّل تطبيقك بصلاحيات كتابة للمجلد المستهدف.  
- **License not set** – إذا تلقيت استثناء ترخيص، قم بتحميل ترخيص Aspose.PSD قبل إنشاء الصورة.

## الخاتمة

في هذا الدليل غطينا ملفات **how to create PSD** باستخدام Aspose.PSD للـ Java، وأظهرنا **how to set path**، وعرضنا تدفقًا كاملاً لإنشاء مستند Photoshop. يتيح هذا النهج لمطوري Java دمج إنشاء PSD مباشرة في سير عملهم، سواء للتقارير الآلية، الرسومات الديناميكية، أو المعالجة الدُفعية.

## الأسئلة الشائعة

### س1: هل Aspose.PSD متوافق مع بيئات تطوير Java المختلفة؟

A1: نعم، Aspose.PSD يعمل بسلاسة مع مختلف بيئات التطوير المتكاملة (IDEs) للـ Java.

### س2: هل يمكنني استخدام Aspose.PSD للمشاريع التجارية؟

A2: نعم، يمكنك استخدام Aspose.PSD للمشاريع الشخصية والتجارية على حد سواء. راجع [صفحة الشراء](https://purchase.aspose.com/buy) للحصول على تفاصيل الترخيص.

### س3: كيف يمكنني الحصول على دعم Aspose.PSD؟

A3: زر [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) للحصول على دعم المجتمع والنقاشات.

### س4: هل هناك نسخة تجريبية مجانية متاحة؟

A4: نعم، يمكنك الوصول إلى النسخة التجريبية المجانية [هنا](https://releases.aspose.com/).

### س5: هل أحتاج إلى ترخيص مؤقت للاختبار؟

A5: يمكنك الحصول على ترخيص مؤقت لأغراض الاختبار [هنا](https://purchase.aspose.com/temporary-license/).

**س: هل يمكنني تغيير أبعاد الصورة بعد الإنشاء؟**  
**ج: نعم، يمكنك تغيير حجم الصورة باستخدام `image.resize(width, height)` قبل الحفظ.**

**س: ما هي أوضاع الألوان المدعومة؟**  
**ج: يدعم Aspose.PSD أوضاع اللون RGB، CMYK، Grayscale، و Indexed.**

---

**Last Updated:** 2026-01-01  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}