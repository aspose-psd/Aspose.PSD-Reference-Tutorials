---
date: 2026-03-21
description: تعلم كيفية تصدير الصور باستخدام Aspose.PSD للـ Java، وتحويل ملفات PSD
  إلى صور نقطية، وحذف الملفات المؤقتة في بيئة متعددة الخيوط. عزّز الأداء واحرص على
  نظافة مساحة عملك.
linktitle: Export Images in Multi‑Threaded Environment
second_title: Aspose.PSD Java API
title: كيفية حذف الملفات المؤقتة أثناء تصدير الصور في بيئة متعددة الخيوط – Aspose.PSD
  للـ Java
url: /ar/java/psd-conversion/export-images-multi-thread/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# دليل تصدير الصور متعدد الخيوط – Aspose.PSD للـ Java  

هل ترغب في **حذف الملفات المؤقتة** مع تحسين قدرات تطبيق Java الخاص بك على تصدير الصور في بيئة متعددة الخيوط؟ تجعل لك Aspose.PSD للـ Java عملية **تحويل PSD إلى raster** سهلة، وتعمل مع **save pixels java**، وتحافظ على نظافة نظام الملفات. في هذا الدرس سنرشدك خلال مثال كامل جاهز للإنتاج يوضح كيفية تصدير الصور، إدارة الخيوط بأمان، وحذف أي ملفات متبقية تلقائيًا.

## إجابات سريعة
- **هل يمكن لـ Aspose.PSD حذف الملفات المؤقتة تلقائيًا؟** نعم – يمكنك إزالتها برمجيًا بعد المعالجة.  
- **هل يدعم معالجة الصور المتعددة الخيوط؟** بالتأكيد؛ المكتبة آمنة للاستخدام من عدة خيوط في عمليات التصدير المتزامنة.  
- **ما هي الطريقة التي تحفظ بيانات البكسل في Java؟** `savePixels` على كائن `RasterImage`.  
- **هل أحتاج إلى ترخيص للاستخدام في الإنتاج؟** يلزم وجود ترخيص صالح لـ Aspose.PSD؛ يتوفر إصدار تجريبي مجاني.  
- **ما إصدارات Java المتوافقة؟** Java 1.7 وما بعدها.

## ما المقصود بـ “حذف الملفات المؤقتة” في سياق تصدير الصور؟
عند تصدير الصور من ملف PSD، غالبًا ما تُنشئ ملفات وسيطة (مثل نسخ من ملف PSD الأصلي، بيانات raster مؤقتة). حذف هذه الملفات المؤقتة يمنع فوضى القرص، يقلل من تكاليف التخزين، ويتجنب إعادة استخدام البيانات القديمة عن طريق الخطأ.

## لماذا نستخدم Aspose.PSD لمعالجة الصور المتعددة الخيوط؟
- **أداء عالي:** معالجة عدة ملفات PSD بالتوازي دون عنق زجاجة.  
- **أمان الخيوط:** تم تصميم واجهات برمجة التطبيقات الأساسية للعمل بشكل صحيح عند الوصول إليها من خيوط متعددة.  
- **مجموعة ميزات غنية:** تحويل مباشر من PSD إلى صيغ raster، تعديل الطبقات، و**save pixels java** مع تحكم دقيق.  
- **تنظيف مدمج:** أنت من يقرر متى وكيف يتم حذف الملفات المؤقتة، مما يمنحك سيطرة كاملة على إدارة الموارد.

## المتطلبات المسبقة
- معرفة أساسية ببرمجة Java.  
- بيئة تطوير Java (JDK 1.7+).  
- مكتبة Aspose.PSD للـ Java محملة ومثبتة. يمكنك العثور على رابط التحميل [هنا](https://releases.aspose.com/psd/java/).

## استيراد الحزم
أضف الاستيرادات المطلوبة إلى فئة Java الخاصة بك. هذه الفئات تمنحك الوصول إلى معالجة الألوان، تعديل صور raster، والتحميل القائم على الـ stream.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.StreamSource;
import com.aspose.psd.system.io.FileStream;
import java.io.File;
import java.io.FileInputStream;
import java.io.FileNotFoundException;
```

## الخطوة 1: إعداد دليل المستندات  
حدد مكان وجود ملفات PSD المصدرية. حفظ المسار في متغير يجعل إعادة الاستخدام عبر الخيوط أمرًا سهلًا.

```java
String dataDir = "Your Document Directory";
```

## الخطوة 2: تحميل صورة PSD  
افتح ملف PSD كـ stream وقم بتكوين `PsdOptions` حتى تعرف Aspose.PSD من أين تقرأ البيانات.

```java
String imageDataPath = dataDir + "sample.psd";
FileInputStream fileStream = new FileInputStream(imageDataPath);
PsdOptions psdOptions = new PsdOptions();
psdOptions.setSource(new StreamSource(fileStream));
```

## الخطوة 3: معالجة الصورة – تحويل PSD إلى Raster وحفظ البكسل  
أنشئ كائن `RasterImage` من خيارات PSD، عدل بعض البكسلات، ثم احفظ بيانات raster مرة أخرى إلى نظام الملفات. هذا يوضح سير عمل **convert psd to raster** و**save pixels java**.

```java
RasterImage image = (RasterImage)Image.create(psdOptions, 10, 10);
Color[] pixels = new Color[4];
for (int i = 0; i < 4; ++i) {
    pixels[i] = Color.fromArgb(40, 30, 20, 10);
}
image.savePixels(new Rectangle(0, 0, 2, 2), pixels);
image.save();
```

## الخطوة 4: التنظيف – حذف الملفات المؤقتة  
بعد انتهاء عملية التصدير، من الممارسات الجيدة حذف أي ملفات مؤقتة تم إنشاؤها (بما في ذلك نسخة PSD الأصلية إذا كانت نسخة). هذا هو جوهر استراتيجيتنا لـ **delete temporary files**.

```java
File f = new File(imageDataPath);
if (f.exists()) {
    f.delete();
}
```

> **نصيحة احترافية:** ضع كود التنظيف داخل كتلة `finally` أو استخدم `try‑with‑resources` في Java لضمان الحذف حتى لو حدث استثناء.

## المشكلات الشائعة والحلول
| المشكلة | السبب | الحل |
|-------|--------|-----|
| `FileNotFoundException` على `FileInputStream` | مسار غير صحيح أو أذونات ملف مفقودة | تحقق من `dataDir` وتأكد من أن التطبيق يمتلك صلاحيات القراءة/الكتابة. |
| الصور لا تُحفظ بشكل صحيح | عدم استدعاء `image.save()` بعد `savePixels` | تأكد من تنفيذ `image.save()` بعد تعديل البكسلات. |
| تبقى الملفات المؤقتة بعد تعطل البرنامج | لم يصل الكود إلى مرحلة التنظيف | استخدم hook للإغلاق أو كتلة `finally` لضمان الحذف. |

## الأسئلة المتكررة

### هل Aspose.PSD متوافق مع جميع إصدارات Java؟
Aspose.PSD متوافق مع Java 1.7 والإصدارات الأحدث.

### هل يمكنني معالجة عدة صور في وقت واحد باستخدام Aspose.PSD؟
نعم، تدعم Aspose.PSD تعدد الخيوط، مما يسمح بمعالجة صور متعددة بشكل متزامن.

### أين يمكنني العثور على وثائق إضافية لـ Aspose.PSD؟
يمكنك الرجوع إلى الوثائق [هنا](https://reference.aspose.com/psd/java/).

### هل يتوفر نسخة تجريبية مجانية لـ Aspose.PSD للـ Java؟
نعم، يمكنك الوصول إلى النسخة التجريبية المجانية [هنا](https://releases.aspose.com/).

### كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.PSD؟
تفضل بزيارة [هذا الرابط](https://purchase.aspose.com/temporary-license/) للحصول على ترخيص مؤقت.

**أسئلة وإجابات إضافية**

**س:** ما هي أفضل طريقة لإدارة مجموعة من خيوط العاملين لتصدير الصور؟  
**ج:** استخدم `java.util.concurrent.ExecutorService` (مثل `Executors.newFixedThreadPool`) لتقديم مهام التصدير ودع الإطار يتولى إدارة دورة حياة الخيوط.

**س:** هل يمكنني التصدير إلى صيغ أخرى غير PSD؟  
**ج:** نعم، يمكن لـ Aspose.PSD حفظ صور raster إلى PNG، JPEG، BMP، والعديد من الصيغ الأخرى عبر فئة `ImageOptions` المناسبة.

**س:** كيف أضمن أمان الخيوط عند مشاركة كائن `RasterImage`؟  
**ج:** لا تشارك نفس كائن `RasterImage` بين الخيوط؛ أنشئ صورة منفصلة لكل مهمة أو قم بمزامنة الوصول إذا كان لا مفر من المشاركة.

## الخاتمة
في هذا الدرس استعرضنا كيفية **حذف الملفات المؤقتة** أثناء تصدير الصور باستخدام Aspose.PSD للـ Java في بيئة **متعددة الخيوط**. تعلمت كيفية **تحويل PSD إلى raster**، تعديل بيانات البكسل باستخدام **save pixels java**، والحفاظ على نظافة مساحة العمل بحذف الملفات المؤقتة برمجيًا. طبّق هذه الأنماط لتعزيز الأداء، تقليل استهلاك التخزين، وبناء خطوط معالجة صور Java قوية وموثوقة.

---

**آخر تحديث:** 2026-03-21  
**تم الاختبار مع:** Aspose.PSD للـ Java 24.12 (أحدث نسخة وقت الكتابة)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}