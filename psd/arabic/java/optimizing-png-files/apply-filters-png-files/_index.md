---
date: 2026-03-15
description: تعلم كيفية تصفية صور PNG باستخدام Aspose.PSD للـ Java. يغطي هذا الدليل
  خطوة بخطوة تحسين PNG في Java وتحويل PSD إلى PNG مع أنواع الفلاتر.
linktitle: How to Filter PNG Files in Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: كيفية تصفية ملفات PNG في Aspose.PSD للـ Java
url: /ar/java/optimizing-png-files/apply-filters-png-files/
weight: 10
---

 >}}

Make sure no extra spaces.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تصفية ملفات PNG في Aspose.PSD للـ Java

## المقدمة
إذا كنت تتساءل **how to filter PNG** أثناء العمل مع Java، فقد وصلت إلى المكان الصحيح. في هذا الدرس سنستعرض تطبيق أنواع فلاتر PNG باستخدام Aspose.PSD للـ Java، وهي مكتبة تساعدك أيضًا على **convert PSD to PNG** وإجراء **java png optimization**. في النهاية ستتمكن من ضبط الضغط بدقة، تحسين الجودة البصرية، ودمج العملية في أي مشروع Java.

## إجابات سريعة
- **ما المكتبة التي تدعم تصفية PNG في Java؟** Aspose.PSD للـ Java.  
- **أي فلتر يعطي أفضل ضغط لمعظم الصور؟** فلتر Paeth (المستخدم في هذا المثال).  
- **هل أحتاج إلى ترخيص لتشغيل الكود؟** نسخة تجريبية مجانية تكفي للتقييم؛ الترخيص مطلوب للإنتاج.  
- **هل يمكنني تحويل PSD إلى PNG في نفس سير العمل؟** نعم – حمّل ملف PSD واحفظه كـ PNG مع الفلتر المطلوب.  
- **ما إصدار Java المطلوب؟** Java 8 أو أحدث.

## ما هو “how to filter png” عمليًا؟
تصفية ملف PNG تعني اختيار خوارزمية تمهيدية تُجهّز بيانات البكسل قبل الضغط. نوع الفلتر يؤثر على حجم الملف ومدى حفظ الألوان بعد حفظ PNG. توفر لك Aspose.PSD تحكمًا مباشرًا في هذه الخطوة عبر طريقة `PngOptions.setFilterType`.

## لماذا تستخدم Aspose.PSD للـ Java لتحسين PNG؟
- **دعم كامل لـ PSD:** افتح، عدّل، وصدر طبقات PSD دون فقدان الدقة.  
- **اختيار الفلتر مدمج:** اختر من بين Paeth، Sub، Up، Average، أو None.  
- **متعدد المنصات:** يعمل على Windows، Linux، و macOS مع أي JDK قياسي.  
- **بدون تبعيات أصلية خارجية:** تنفيذ Java نقي يبسط عملية النشر.

## المتطلبات المسبقة
1. **Java Development Kit (JDK) 8+** – تأكد من أن `java -version` يُظهر 1.8 أو أعلى.  
2. **IDE (IntelliJ IDEA، Eclipse، أو VS Code)** – أي بيئة تشعر بالراحة معها.  
3. **مكتبة Aspose.PSD للـ Java** – حمّلها من [هنا](https://releases.aspose.com/psd/java/).  
4. **معرفة أساسية بـ Java** – إلمام بالصفوف، الطرق، وملفات الإدخال/الإخراج.

## استيراد الحزم
أولاً، استورد الفئات المطلوبة من Aspose.PSD إلى ملف Java الخاص بك:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngFilterType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
```

> **نصيحة احترافية:** أضف ملف JAR الخاص بـ Aspose.PSD إلى مسار بناء المشروع أو إلى تبعيات Maven/Gradle حتى يتم حل الاستيرادات دون أخطاء.

## الخطوة 1: إعداد دليل المستند
عرّف المجلد الذي يحتوي على ملف PSD المصدر وأين سيتم حفظ PNG المصفّى.

```java
String dataDir = "Your Document Directory"; // Adjust this path
```

استبدل `"Your Document Directory"` بالمسار المطلق أو النسبي على جهازك.

## الخطوة 2: تحميل صورة PSD
افتح ملف PSD الذي تريد معالجته. التحويل إلى `PsdImage` يمنحك إمكانيات خاصة بـ PSD.

```java
PsdImage psdImage = (PsdImage) Image.load(dataDir + "sample.psd");
```

إذا كان الملف مفقودًا، فإن `Image.load` يرمي استثناءً – تأكد من صحة المسار.

## الخطوة 3: إنشاء خيارات PNG (تحسين PNG في Java)
قم بتكوين إعدادات تصدير PNG، بما في ذلك نوع الفلتر الذي يجيب مباشرةً على **how to filter png**.

```java
PngOptions options = new PngOptions();
options.setFilterType(PngFilterType.Paeth);
```

يمكنك تجربة أنواع فلاتر أخرى (`Sub`، `Up`، `Average`، `None`) لترى كيف تؤثر على الحجم والجودة. توضح هذه الخطوة أيضًا **java png optimization** لأن الفلتر المختار يؤثر على كفاءة الضغط.

## الخطوة 4: حفظ صورة PNG
أخيرًا، اكتب الصورة المعالجة إلى القرص باستخدام الخيارات التي حددتها.

```java
psdImage.save(dataDir + "ApplyFilterMethod_out.png", options);
```

الملف الناتج، `ApplyFilterMethod_out.png`، سيكون PNG مُصفّى جاهز للاستخدام على الويب أو سطح المكتب.

## المشكلات الشائعة والحلول
| العَرَض | السبب المحتمل | الحل |
|---------|--------------|-----|
| `FileNotFoundException` | مسار `dataDir` غير صحيح | تحقق من أن سلسلة الدليل تنتهي بفاصل (`/` أو `\\`). |
| لا يُلاحظ تأثير الفلتر | استخدام `PngFilterType.None` | غيّر إلى `Paeth` أو نوع فلتر آخر. |
| خطأ نفاد الذاكرة على ملفات PSD الكبيرة | تحميل ملف ضخم دون تدفق | استخدم `PsdImage` مع `loadOptions` لتقليل استهلاك الذاكرة. |

## الأسئلة المتكررة

**س: ما هو Aspose.PSD للـ Java؟**  
ج: Aspose.PSD للـ Java هو API قوي يتيح للمطورين قراءة، تعديل، وتحويل ملفات PSD، تطبيق الفلاتر، وإجراء تحسينات على الصور دون الحاجة إلى Adobe Photoshop.

**س: كيف يمكنني تحميل Aspose.PSD للـ Java؟**  
ج: يمكنك تحميله من صفحة إصدارات Aspose [هنا](https://releases.aspose.com/psd/java/).

**س: هل يمكنني تجربة Aspose.PSD مجانًا؟**  
ج: نعم، نسخة تجريبية مجانية متاحة [هنا](https://releases.aspose.com/).

**س: ما أنواع الفلاتر التي يمكنني تطبيقها على صور PNG؟**  
ج: يدعم Aspose.PSD الفلاتر Paeth، Sub، Up، Average، وNone. اختر الأنسب لتحقيق التوازن بين الحجم والوضوح البصري.

**س: أين يمكنني العثور على دعم لمشكلات Aspose.PSD؟**  
ج: يمكنك الحصول على المساعدة والدعم بزيارة منتدى Aspose [هنا](https://forum.aspose.com/c/psd/34).

## الخاتمة
أنت الآن تعرف **how to filter PNG** باستخدام Aspose.PSD للـ Java، وكيفية **convert PSD to PNG**، وكيفية إجراء **java png optimization** باستخدام أنواع الفلاتر المختلفة. جرّب الفلاتر المتنوعة، دمج هذا سير العمل في خط معالجة الصور الخاص بك، واستمتع بملفات PNG أصغر جودةً وعالية الدقة.

---

**آخر تحديث:** 2026-03-15  
**تم الاختبار مع:** Aspose.PSD للـ Java 24.10  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}