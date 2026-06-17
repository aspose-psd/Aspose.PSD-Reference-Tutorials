---
date: 2026-03-23
description: تعلم كيفية حفظ الصورة بصيغة PSD باستخدام Aspose.PSD للغة Java. دليل خطوة
  بخطوة لتعيين وضع اللون في PSD، تحويل البت ماب إلى PSD وتصدير الصور برمجيًا.
linktitle: Export Images to PSD Format with Java
second_title: Aspose.PSD Java API
title: كيفية حفظ الصورة بصيغة PSD باستخدام Java و Aspose.PSD
url: /ar/java/psd-image-modification-conversion/export-images-psd-format/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية حفظ الصورة كملف PSD باستخدام Java و Aspose.PSD

## كيفية حفظ الصورة كملف PSD باستخدام Java

في هذا الدرس، ستتعلم **كيفية حفظ الصورة كملف PSD** باستخدام Java ومكتبة Aspose.PSD. التعامل مع ملفات Photoshop ذات الطبقات هو مهمة يومية للعديد من مطوري التصميم الجرافيكي، ويمكن لأتمتة إنشاء ملفات PSD أن تُسرّع سير العمل بشكل كبير. سنستعرض ضبط وضع اللون في PSD، وإنشاء bitmap، وتحويل هذا الـ bitmap إلى ملف PSD—كل ما تحتاجه للبدء بسرعة. هيا نبدأ!

## إجابات سريعة
- **ما المكتبة التي أحتاجها؟** Aspose.PSD for Java (متاحة للتحميل من الموقع الرسمي).  
- **هل يمكنني ضبط وضع اللون؟** نعم – استخدم `PsdOptions.setColorMode()` لاختيار RGB أو CMYK، إلخ.  
- **هل يدعم تحويل bitmap إلى PSD؟** بالتأكيد؛ أنشئ `PsdImage` من الأبعاد أو من bitmap موجود واحفظه.  
- **هل أحتاج إلى ترخيص للاستخدام الإنتاجي؟** يلزم الحصول على ترخيص تجاري للاستخدام غير التجريبي.  
- **ما نسخة Java المطلوبة؟** Java 8 أو أعلى.

## ما هو “حفظ الصورة كملف PSD”؟

حفظ الصورة كملف PSD يعني تصدير رسم نقطي إلى تنسيق Photoshop الأصلي الطبقي. هذا يسمح للأدوات اللاحقة (Photoshop، GIMP، إلخ) بالحفاظ على الطبقات والقنوات وقابلية التحرير. باستخدام Aspose.PSD يمكنك إنشاء ملفات PSD برمجياً دون الحاجة إلى فتح Photoshop.

## لماذا نستخدم Aspose.PSD for Java؟

- **تحكم كامل** في وضعيات اللون، الضغط، وتوافق إصدارات Photoshop.  
- **بدون تبعيات خارجية** – Java نقي، مثالي للمعالجة على الخادم.  
- **أداء عالي** – مناسب لمعالجة دفعات من آلاف الصور.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من وجود ما يلي:

1. **معرفة أساسية بـ Java** – يجب أن تكون مرتاحًا مع تجميع وتشغيل برامج Java.  
2. **مكتبة Aspose.PSD for Java** – يمكنك [تحميلها من هنا](https://releases.aspose.com/psd/java/).  
3. **مجموعة تطوير Java (JDK)** – JDK 8 أو أحدث مثبت على جهازك.  
4. **IDE أو محرر نصوص** – IntelliJ IDEA، Eclipse، VS Code، أو أي محرر تفضله.  
5. **فهم مفاهيم الصورة** – وضعيات اللون، الضغط، وأساسيات الـ bitmap مفيدة لكن ليست إلزامية.

هل لديك كل شيء؟ رائع، لننتقل إلى التالي.

## استيراد الحزم

أولاً، استورد الفئات التي سنحتاجها من مكتبة Aspose.PSD:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Pen;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
```

توفر هذه الاستيرادات لنا الوصول إلى أدوات الرسم، معالجة الألوان، وخيارات PSD الخاصة.

## الخطوة 1: تهيئة دليل المستند الخاص بك

حدد المكان الذي سيُحفظ فيه ملف PSD المُولد:

```java
String dataDir = "Your Document Directory";
```

استبدل `"Your Document Directory"` بمسار مطلق مثل `"C:/Images/"` أو مسار نسبي داخل مشروعك.

## الخطوة 2: إنشاء صورة جديدة (تحويل Bitmap إلى PSD)

الآن نقوم بإنشاء bitmap فارغ سنقوم لاحقًا **بتحويل bitmap إلى PSD** عن طريق حفظه باستخدام خيارات PSD:

```java
PsdImage bmpImage = new PsdImage(300, 300);
```

يمكنك تعديل `300, 300` لتتناسب مع الأبعاد التي تحتاجها.

## الخطوة 3: ملء بيانات الصورة

أضف بعض الرسومات إلى الـ bitmap حتى لا يكون الـ PSD الناتج مجرد لوحة فارغة:

```java
Graphics graphics = new Graphics(bmpImage);
graphics.clear(Color.getWhite());
Pen pen = new Pen(Color.getBrown());
graphics.drawRectangle(pen, bmpImage.getBounds());
```

- `graphics.clear(Color.getWhite())` يملأ كامل اللوحة باللون الأبيض.  
- القلم البني يرسم مستطيلًا يحد حدود الصورة.

## الخطوة 4: ضبط خيارات PSD (ضبط وضع لون PSD)

هنا نقوم بتكوين طريقة حفظ الملف. هذا هو المكان الذي **نضبط فيه وضع لون PSD** إلى RGB، نختار الضغط، ونحدد إصدار Photoshop:

```java
PsdOptions psdOptions = new PsdOptions();
psdOptions.setColorMode(ColorModes.Rgb);
psdOptions.setCompressionMethod(CompressionMethod.Raw);
psdOptions.setVersion(4);
```

- `ColorModes.Rgb` – الأكثر شيوعًا للرسومات على الويب والشاشات.  
- `CompressionMethod.Raw` – يخزن بيانات البكسل بدون ضغط للحصول على أقصى جودة.  
- `setVersion(4)` – يحفظ الملف بتنسيق Photoshop 4.0، وهو متوافق على نطاق واسع.

## الخطوة 5: حفظ الصورة

أخيرًا، صدّر الـ bitmap كملف PSD—هذه هي العملية الأساسية **لحفظ الصورة كملف PSD**:

```java
bmpImage.save(dataDir + "ExportImageToPSD_output.psd", psdOptions);
```

سيظهر الملف `ExportImageToPSD_output.psd` في الدليل الذي حددته.

## حالات الاستخدام الشائعة

- **إنشاء تقارير تلقائي** حيث تحتاج المخططات إلى أن تكون قابلة للتحرير في Photoshop.  
- **تحويل دفعي** لأصول PNG/JPEG إلى PSD للمصممين الذين يحتاجون إلى طبقات.  
- **تركيب الصور على الخادم** لخدمات الويب التي تقدم قوالب PSD للعملاء.

## المشكلات الشائعة والحلول

| Issue | Solution |
|-------|----------|
| **خطأ ملف غير موجود** عند الحفظ | تحقق من أن `dataDir` ينتهي بفاصل مسار (`/` أو `\\`) وأن المجلد موجود. |
| **صورة فارغة** بعد الحفظ | تأكد من أنك استدعيت `graphics.clear()` ورسمت شيئًا قبل الحفظ. |
| **وضع لون غير مدعوم** | استخدم `ColorModes.Cmyk` إذا كنت بحاجة إلى إخراج CMYK؛ وتذكر تعديل الرسومات وفقًا لذلك. |
| **LicenseException** أثناء التشغيل | قم بتثبيت ترخيص Aspose.PSD صالح أو شغّل في وضع التجربة (قد يظهر علامة مائية للتقييم). |

## الأسئلة المتكررة

**س: ما هو Aspose.PSD for Java؟**  
ج: Aspose.PSD for Java هو API قوي يتيح للمطورين إنشاء وتحرير وتحويل وعرض ملفات Photoshop PSD دون الحاجة إلى استخدام Adobe Photoshop.

**س: هل يمكنني تعديل ملف PSD موجود؟**  
ج: نعم، يمكنك فتح ملف PSD موجود باستخدام `new PsdImage("input.psd")`، إجراء التعديلات، ثم حفظه مرة أخرى.

**س: هل يتوفر نسخة تجريبية مجانية؟**  
ج: بالتأكيد! يمكنك تحميل نسخة تجريبية مجانية من Aspose.PSD [هنا](https://releases.aspose.com/).

**س: أين يمكنني العثور على مزيد من الوثائق؟**  
ج: يمكنك الاطلاع على الوثائق الشاملة [هنا](https://reference.aspose.com/psd/java/) لتتعرف أكثر على استخدام Aspose.PSD.

**س: كيف يمكنني الحصول على الدعم إذا واجهت مشاكل؟**  
ج: للحصول على الدعم، يمكنك زيارة [منتدى Aspose](https://forum.aspose.com/c/psd/34).

## الخلاصة

أنت الآن تعرف كيفية **حفظ الصورة كملف PSD** باستخدام Java، وكيفية **ضبط وضع لون PSD**، وكيفية **تحويل bitmap إلى PSD** باستخدام Aspose.PSD. يمنحك هذا النهج تحكمًا برمجيًا كاملاً في ملفات Photoshop، مما يفتح الأبواب أمام خطوط تصميم آلية، وتوليد صور ديناميكي، وتكامل سلس مع تطبيقات Java الحالية. جرب وضعيات لون مختلفة، أحجام، وعمليات رسم لتخصيص ملفات PSD وفق احتياجاتك الدقيقة.

---

**Last Updated:** 2026-03-23  
**Tested With:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}