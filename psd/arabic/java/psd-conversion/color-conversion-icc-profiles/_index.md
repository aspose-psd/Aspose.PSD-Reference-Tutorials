---
date: 2026-03-21
description: تعلم كيفية استخدام ملفات تعريف ICC لتحويل ملفات تعريف الألوان، وتطبيق
  إعدادات ملف تعريف ICC، وتعيين ملف تعريف RGB عند إنشاء صور PSD باستخدام Aspose.PSD
  للغة Java.
linktitle: Color Conversion using ICC Profiles
second_title: Aspose.PSD Java API
title: كيفية استخدام ملفات تعريف ICC لتحويل الألوان في Aspose.PSD
url: /ar/java/psd-conversion/color-conversion-icc-profiles/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية استخدام ملفات تعريف ICC لتحويل الألوان في Aspose.PSD

## مقدمة
إذا كنت تبحث عن **how to use icc** ملفات التعريف لضمان ألوان دقيقة عبر الأجهزة، فقد وصلت إلى المكان الصحيح. في هذا البرنامج التعليمي سنستعرض تحويل ملف تعريف اللون، تطبيق ملف تعريف ICC، وتعيين ملف تعريف RGB أثناء **creating a PSD image** باستخدام Aspose.PSD for Java. سواءً كنت تبني خط أنابيب معالجة دفعات أو محرر صورة واحد، فإن الخطوات أدناه ستوفر لك أساسًا قويًا وجاهزًا للإنتاج.

## إجابات سريعة
- **What is the primary purpose of an ICC profile?** يحدد كيفية تفسير الألوان على جهاز معين أو مساحة ألوان.  
- **Which class represents a PSD image in Aspose.PSD?** `PsdImage`.  
- **Can I change both RGB and CMYK profiles?** نعم – استخدم `setRgbColorProfile` و `setCmykColorProfile`.  
- **Do I need a license for development?** النسخة التجريبية المجانية تكفي للاختبار؛ يلزم وجود ترخيص للإنتاج.  
- **What output format supports YCCK?** JPEG مع `JpegCompressionColorMode.Ycck`.

## ما هو تحويل اللون باستخدام ICC؟
ملفات تعريف ICC (International Color Consortium) هي مجموعات بيانات معيارية تصف خصائص الألوان للأجهزة (الشاشات، الطابعات، الماسحات). من خلال **convert color profile** من مساحة إلى أخرى، تضمن أن المظهر البصري يبقى ثابتًا، بغض النظر عن مكان عرض الصورة.

## لماذا نستخدم ملفات تعريف ICC مع Aspose.PSD؟
- **Accurate color reproduction** – أساسي للعلامة التجارية وتدفقات عمل الطباعة.  
- **Cross‑platform consistency** – الصورة نفسها تبدو متطابقة على Windows و macOS و الأجهزة المحمولة.  
- **Built‑in API support** – Aspose.PSD يتيح لك **apply icc profile** و **set rgb profile** ببضع أسطر من Java.

## المتطلبات المسبقة
قبل البدء، تأكد من توفر ما يلي:

1. **Aspose.PSD for Java** – قم بتنزيل أحدث مكتبة من صفحة [releases](https://releases.aspose.com/psd/java/).  
2. **Java Development Environment** – JDK 8+ وبيئتك المتكاملة المفضلة.  
3. **ICC Profiles** – في هذا المثال سنستخدم `eciRGB_v2.icc` (RGB) و `ISOcoated_v2_FullGamut4.icc` (CMYK). يمكنك الحصول عليها من مصادر موثوقة لإدارة الألوان.

## استيراد الحزم
أضف مساحات الأسماء المطلوبة من Aspose.PSD إلى مشروعك. هذه الاستيرادات تمنحك الوصول إلى معالجة الصور، خيارات JPEG، ومصادر التدفق.

```java
import com.aspose.psd.Color;
import com.aspose.psd.fileformats.jpeg.JpegCompressionColorMode;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.JpegOptions;
import com.aspose.psd.sources.StreamSource;
import java.io.File;
import java.io.FileInputStream;
import java.io.FileNotFoundException;
```

## كيفية استخدام ملفات تعريف ICC لتحويل اللون
فيما يلي دليل خطوة بخطوة يوضح **how to convert color** باستخدام ملفات تعريف ICC أثناء **creating a PSD image**.

### الخطوة 1: إنشاء صورة جديدة (Create PSD Image)
أولاً، أنشئ كائن `PsdImage` فارغ. هذا يمنحك لوحة يمكن ملؤها ببيانات البكسل.

```java
String dataDir = "Your Document Directory";
PsdImage image = new PsdImage(500, 500);
```

### الخطوة 2: ملء بيانات الصورة
املأ الصورة بقيم بكسل ARGB الخام. في سيناريو واقعي قد تقوم بتحميل بيانات البكسل من مصدر آخر، لكن هنا نوضح العملية فقط.

```java
int count = image.getWidth() * image.getHeight();
int[] pixels = new int[count];
int r = 0, g = 0, b = 0, channel = 0;
for (int i = 0; i < count; i++) {
    // Fill pixels with color values.
    // ...
}
// Save the newly created pixels.
image.saveArgb32Pixels(image.getBounds(), pixels);
```

### الخطوة 3: حفظ الصورة باستخدام ملفات تعريف ICC الافتراضية
الحفظ في هذه المرحلة يكتب الصورة باستخدام ملفات تعريف الألوان الافتراضية للمكتبة. تساعدك هذه الخطوة على رؤية الفرق بعد تطبيق ملفات تعريف مخصصة لاحقًا.

```java
image.save(dataDir + "Default_profiles.jpg");
```

### الخطوة 4: تحديث ملفات تعريف الألوان (Apply ICC Profile & Set RGB Profile)
حمّل ملفات ICC الخارجية وعيّنها على الصورة. هنا نستخدم **apply icc profile** و **set rgb profile**.

```java
File rgbFile = new File(dataDir + "eciRGB_v2.icc");
FileInputStream rgbInputStream = new FileInputStream(rgbFile);
StreamSource rgbprofile = new StreamSource(rgbInputStream);
File cmykFile = new File(dataDir + "ISOcoated_v2_FullGamut4.icc");
FileInputStream cmykInputStream = new FileInputStream(cmykFile);
StreamSource cmykprofile = new StreamSource(cmykInputStream);
image.setRgbColorProfile(rgbprofile);
image.setCmykColorProfile(cmykprofile);
```

### الخطوة 5: حفظ الصورة باستخدام ملفات تعريف YCCK الجديدة
أخيرًا، صدّر الصورة كملف JPEG باستخدام وضع اللون YCCK، الذي يحترم ملف تعريف CMYK الذي تم تعيينه للتو.

```java
JpegOptions options = new JpegOptions();
options.setColorType(JpegCompressionColorMode.Ycck);
image.save(dataDir + "Ycck_profiles.jpg", options);
```

باتباع هذه الخطوات، تكون قد **converted the color profile** لصورة PSD، **applied ICC profiles**، و **set the RGB profile** للحصول على عرض دقيق.

## المشكلات الشائعة والحلول
| المشكلة | السبب | الحل |
|-------|--------|-----|
| الألوان تبدو باهتة بعد التحويل | تم تعيين ملف تعريف خاطئ أو بيانات ملف التعريف مفقودة | تحقق من أن ملفات ICC تتطابق مع مساحة ألوان الصورة المصدر. |
| `FileNotFoundException` عند تحميل ملفات ICC | مسار `dataDir` غير صحيح | استخدم مسارًا مطلقًا أو تأكد من وضع الملفات في الدليل المحدد. |
| تم حفظ JPEG بدون ألوان YCCK | `JpegOptions` غير مضبوطة على `Ycck` | استدعِ `options.setColorType(JpegCompressionColorMode.Ycck)` قبل الحفظ. |

## الأسئلة المتكررة
**س: هل يمكنني استخدام ملفات تعريف ICC مخصصة مع Aspose.PSD for Java؟**  
**ج:** نعم، ما عليك سوى استبدال ملفات ICC المقدمة بملفاتك الخاصة وتوجيه `StreamSource` إلى الملفات الجديدة.

**س: كيف يمكنني التعامل مع اختلافات الألوان في الصور الناتجة؟**  
**ج:** قم بضبط ملفات ICC بدقة أو استخدم واجهات برمجة تطبيقات تعديل اللون في Aspose.PSD لضبط السطوع، التباين، أو الجاما بعد التحويل.

**س: هل Aspose.PSD مناسب للمعالجة الدفعية للصور؟**  
**ج:** بالتأكيد. يمكنك المرور عبر مجلد من ملفات PSD، تطبيق نفس منطق الملف التعريفي، وحفظ النتائج بكفاءة.

**س: أين يمكنني العثور على المزيد من ملفات تعريف ICC لإدارة الألوان؟**  
**ج:** راجع موقع ICC، صفحة موارد الألوان الخاصة بـ Adobe، أو المكتبات الخاصة بالموردين التي توفر ملفات تعريف مخصصة للأجهزة.

**س: ما هي فوائد استخدام ملفات تعريف ICC في تحويل اللون؟**  
**ج:** تضمن لونًا ثابتًا عبر الأجهزة المختلفة، تبسط أتمتة سير العمل، وتقلل من الجهد اليدوي لمطابقة الألوان.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**آخر تحديث:** 2026-03-21  
**تم الاختبار مع:** Aspose.PSD for Java (latest)  
**المؤلف:** Aspose