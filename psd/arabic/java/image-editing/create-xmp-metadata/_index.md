---
date: 2026-01-01
description: تعلم كيفية إنشاء بيانات XMP الوصفية، وإضافة XMP إلى ملفات PSD، وتحديث
  بيانات الصورة الوصفية باستخدام Aspose.PSD للغة Java. اتبع هذا الدليل خطوة بخطوة
  الآن.
linktitle: Create XMP Metadata
second_title: Aspose.PSD Java API
title: إنشاء بيانات XMP الوصفية باستخدام Aspose.PSD للـ Java
url: /ar/java/image-editing/create-xmp-metadata/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إنشاء بيانات XMP الوصفية باستخدام Aspose.PSD للـ Java

## المقدمة

إدارة بيانات التعريف للصور هي متطلب شائع لمطوري Java الذين يعملون مع ملفات Photoshop (PSD). في هذا الدرس ستتعلم **كيفية إنشاء بيانات XMP الوصفية** باستخدام مكتبة Aspose.PSD، إضافة XMP إلى صورة PSD، وتحديث بيانات تعريف الصورة برمجياً. سنستعرض كل خطوة، نشرح لماذا كل جزء مهم، ونقدم لك نصائح عملية يمكنك تطبيقها في المشاريع الحقيقية.

## إجابات سريعة
- **ما هي بيانات XMP الوصفية؟** تنسيق موحد لتضمين معلومات وصفية (المؤلف، الكلمات المفتاحية، إلخ) داخل ملفات الصور.  
- **لماذا نستخدم Aspose.PSD؟** توفر واجهة برمجة تطبيقات pure‑Java لإنشاء وقراءة وتحرير ملفات PSD دون الحاجة إلى Photoshop.  
- **هل يمكنني إضافة XMP إلى PSD موجود؟** نعم – يمكنك تحديث بيانات تعريف الصورة مباشرة باستخدام `setXmpData`.  
- **ما هي الخطوات الرئيسية؟** تحديد حجم الصورة، إنشاء الرأس/الذيل، بناء حزم XMP، إرفاقها، ثم الحفظ.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تكفي للتطوير؛ يتطلب الإنتاج ترخيصًا تجاريًا.

## ما هو “إنشاء بيانات XMP الوصفية” في Java؟

إنشاء بيانات XMP الوصفية يعني بناء حزمة XMP (رأس، جسم، ذيل) التي تصف الصورة ثم تضمين تلك الحزمة في ملف PSD. مكتبة Aspose.PSD تُجرد التفاصيل منخفضة المستوى، مما يتيح لك التركيز على المحتوى الذي تريد تخزينه.

## لماذا نضيف XMP إلى ملفات PSD؟

- **قابلية البحث:** يتيح عمليات بحث قوية في إدارة الأصول بناءً على المؤلف أو العنوان أو العلامات المخصصة.  
- **التوافقية:** يتم التعرف على XMP من قبل منتجات Adobe وLightroom والعديد من أنظمة DAM.  
- **التحكم في الإصدارات:** تخزين تاريخ المعالجة (مثل المدينة، وضع اللون) مباشرة داخل الملف.

## المتطلبات المسبقة

- **بيئة تطوير Java:** تثبيت JDK 8 أو أعلى وفهم أساسي للغة Java.  
- **مكتبة Aspose.PSD:** قم بتحميل وإعداد مكتبة Aspose.PSD للـ Java. يمكنك العثور على المكتبة والوثائق التفصيلية [هنا](https://reference.aspose.com/psd/java/).  
- **دليل المستندات الخاص بك:** حدد المكان الذي ستقرأ/تكتب فيه ملفات PSD على نظامك.

## استيراد الحزم

في مشروع Java الخاص بك، استورد الحزم الضرورية للاستفادة من وظائف Aspose.PSD:

```java
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.system.io.MemoryStream;
import com.aspose.psd.xmp.XmpHeaderPi;
import com.aspose.psd.xmp.XmpMeta;
import com.aspose.psd.xmp.XmpPacketWrapper;
import com.aspose.psd.xmp.XmpTrailerPi;
import com.aspose.psd.xmp.schemas.dublincore.DublinCorePackage;
import com.aspose.psd.xmp.schemas.photoshop.ColorMode;
import com.aspose.psd.xmp.schemas.photoshop.PhotoshopPackage;
```

## الخطوة 1: تحديد حجم الصورة

أولاً، حدد أبعاد القماش للصورة PSD الجديدة.

```java
// Specify the size of the image by defining a Rectangle
Rectangle rect = new Rectangle(0, 0, 100, 200);
```

## الخطوة 2: إنشاء صورة جديدة

إنشاء صورة PSD فارغة سنضيف إليها لاحقًا بيانات XMP الوصفية.

```java
// Create a brand new image for sample purposes
PsdImage image = new PsdImage(rect.getWidth(), rect.getHeight());
```

## الخطوة 3: إنشاء رأس XMP

يحتوي الرأس على تعليمات معالجة XML الافتتاحية ومعرف GUID الذي يحدد المستند.

```java
// Create an instance of XMP-Header
XmpHeaderPi xmpHeader = new XmpHeaderPi();
xmpHeader.setGuid("Your Document Directory");
```

## الخطوة 4: إنشاء ذيل XMP

يحدد الذيل نهاية حزمة XMP. ضبط العلامة `true` يكتب تعليمات معالجة الإغلاق.

```java
// Create an instance of Xmp-TrailerPi 
XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## الخطوة 5: إنشاء بيانات XMP الوصفية

أضف سمات عامة مثل المؤلف والوصف إلى كائن بيانات XMP الوصفية الأساسي.

```java
// Create an instance of XMPmeta class to set different attributes
XmpMeta xmpMeta = new XmpMeta();
xmpMeta.addAttribute("Author", "Mr Smith");
xmpMeta.addAttribute("Description", "The fake metadata value");
```

## الخطوة 6: إنشاء غلاف حزمة XMP

غلف الرأس والذيل والبيانات الوصفية الأساسية في حزمة واحدة يمكن إرفاقها بالصورة.

```java
// Create an instance of XmpPacketWrapper that contains all metadata
XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## الخطوة 7: تعيين سمات Photoshop

املأ الحقول الخاصة بـ Photoshop (المدينة، البلد، وضع اللون) التي تتوقعها العديد من أدوات Adobe.

```java
// Create an instance of Photoshop package and set Photoshop attributes
PhotoshopPackage photoshopPackage = new PhotoshopPackage();
photoshopPackage.setCity("London");
photoshopPackage.setCountry("England");
photoshopPackage.setColorMode(ColorMode.Rgb);
```

## الخطوة 8: إضافة حزمة Photoshop إلى بيانات XMP الوصفية

إرفاق حزمة Photoshop بحزمة XMP.

```java
// Add Photoshop package into XMP metadata
xmpData.addPackage(photoshopPackage);
```

## الخطوة 9: تعيين سمات DublinCore

أضف بيانات Dublin Core الوصفية مثل المؤلف، العنوان، وعلامة فيلم مخصصة.

```java
// Create an instance of DublinCore package and set DublinCore attributes
DublinCorePackage dublinCorePackage = new DublinCorePackage();
dublinCorePackage.setAuthor("Charles Bukowski");
dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
dublinCorePackage.addValue("dc:movie", "Barfly");
```

## الخطوة 10: إضافة حزمة DublinCore إلى بيانات XMP الوصفية

دمج حزمة Dublin Core مع حزمة XMP الحالية.

```java
// Add DublinCore Package into XMP metadata
xmpData.addPackage(dublinCorePackage);
```

## الخطوة 11: تحديث بيانات XMP الوصفية في الصورة

الآن قم بتضمين حزمة XMP الكاملة في صورة PSD.

```java
// Update XMP metadata into the image
image.setXmpData(xmpData);
```

## الخطوة 12: حفظ الصورة

أخيرًا، اكتب ملف PSD إلى القرص (أو إلى تدفق الذاكرة) بحيث يتم حفظ البيانات الوصفية.

```java
// Save the image on the disk or in a memory stream
image.save("Your Document Directory" + "create_XMP_Metadata.psd");
```

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|----------------|-----|
| **`NullPointerException` on `setXmpData`** | حزمة XMP لم تُبنى بالكامل (يفتقد الرأس/الذيل). | تأكد من إنشاء `XmpHeaderPi` و `XmpTrailerPi` وإضافة جميع الحزم قبل استدعاء `setXmpData`. |
| **Metadata not visible in Photoshop** | يتوقع Photoshop أن تكون حزمة XMP مغلفة بشكل صحيح. | تحقق من استخدام `XmpTrailerPi(true)` وأن الحزمة تم حفظها مع الصورة. |
| **File path errors** | استخدام مسار نسبي بدون الأذونات المناسبة. | استخدم مسارًا مطلقًا أو تأكد من أن التطبيق يمتلك صلاحية كتابة للمجلد المستهدف. |

## الأسئلة المتكررة

**س: هل Aspose.PSD متوافق مع صيغ صور مختلفة؟**  
ج: نعم، يدعم Aspose.PSD صيغ PSD، PSB، BMP، GIF، JPEG، PNG، TIFF، وأكثر، مما يمنحك مرونة عبر الصيغ.

**س: هل يمكنني تعديل البيانات الوصفية الموجودة باستخدام Aspose.PSD؟**  
ج: بالتأكيد. يمكنك تحميل PSD موجود، استرجاع بيانات XMP الخاصة به باستخدام `getXmpData()`، تعديل الحزمة، ثم حفظها مرة أخرى.

**س: هل هناك أي قيود على حجم الصورة التي يمكن لـ Aspose.PSD التعامل معها؟**  
ج: تم تصميم Aspose.PSD للعمل مع صور كبيرة (حتى عدة جيجابكسل) ويقتصر فقط على الذاكرة المتاحة.

**س: هل هناك نسخة تجريبية متاحة لـ Aspose.PSD؟**  
ج: نعم، يمكنك استكشاف قدرات Aspose.PSD بالحصول على نسخة تجريبية مجانية [هنا](https://releases.aspose.com/).

**س: أين يمكنني الحصول على الدعم للاستفسارات المتعلقة بـ Aspose.PSD؟**  
ج: لأي مساعدة أو استفسارات، زر [منتدى Aspose.PSD](https://forum.aspose.com/c/psd/34).

## الخلاصة

لقد أصبحت الآن متمكنًا من **كيفية إنشاء بيانات XMP الوصفية**، إضافة XMP إلى PSD، وتحديث بيانات تعريف الصورة باستخدام Aspose.PSD للـ Java. تمنحك هذه الخطوات تحكمًا كاملاً في المعلومات الوصفية المدمجة في صورك، مما يجعلها قابلة للبحث وجاهزة لتدفقات العمل اللاحقة. لا تتردد في تجربة مخططات XMP إضافية أو دمج هذا الكود في خطوط معالجة صور أكبر.

---

**آخر تحديث:** 2026-01-01  
**تم الاختبار مع:** Aspose.PSD for Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}