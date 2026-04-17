---
date: 2026-03-02
description: تعلم كيفية إضافة ملء عن طريق إنشاء طبقة ملء لونية في ملفات PSD باستخدام
  Java و Aspose.PSD. اتبع دليلنا خطوة بخطوة لتعيين لون طبقة الملء بسرعة.
linktitle: Add Color Fill Layer to PSD Files using Java
second_title: Aspose.PSD Java API
title: 'كيفية إضافة تعبئة: إضافة طبقة تعبئة لونية إلى ملفات PSD باستخدام Java'
url: /ar/java/modifying-converting-psd-images/add-color-fill-layer-psd-files/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إضافة طبقة تعبئة لونية إلى ملفات PSD باستخدام Java

## مقدمة
هل وجدت نفسك تحتاج إلى تعديل ملفات Photoshop برمجياً، ربما لإضافة لمسة من اللون إلى تصميم؟ إذا كنت تتساءل **كيفية إضافة تعبئة** إلى ملف PSD، فأنت في المكان الصحيح. في هذا الدرس سنستعرض كيفية إضافة طبقة تعبئة لونية إلى ملفات PSD (Photoshop Document) باستخدام Java ومكتبة Aspose.PSD. فكر في ملف PSD كقماش رقمي—بحلول النهاية ستعرف كيف تنشئ طبقة تعبئة لونية، وتضبط لون طبقة التعبئة، وتحفظ الملف المحدث ببضع أسطر من الشيفرة فقط.

## إجابات سريعة
- **ما المكتبة المطلوبة؟** Aspose.PSD for Java  
- **ما هو الاستخدام الأساسي؟** إضافة أو تغيير ألوان تعبئة PSD برمجياً  
- **كم يستغرق التنفيذ؟** حوالي 10‑15 دقيقة للسيناريو الأساسي  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تكفي للتقييم؛ يلزم ترخيص تجاري للإنتاج  
- **إصدار Java المدعوم؟** Java 8 وما فوق  

## ما هي طبقة التعبئة اللونية؟
طبقة التعبئة اللونية هي طبقة تغطية صلبة اللون تُوضع فوق الطبقات الأخرى في مستند Photoshop. تُستخدم غالبًا لإضافة لون خلفية، إنشاء أقنعة، أو تغيير سريع للموضوع البصري لتصميم دون تعديل كل بكسل على حدة.

## لماذا نضيف طبقة تعبئة لونية باستخدام الكود؟
- **الأتمتة:** إنشاء أصول علامة تجارية متسقة عبر العديد من الملفات.  
- **المعالجة الدفعية:** تحديث العشرات من ملفات PSD في ثوانٍ بدلاً من يدويًا.  
- **تصاميم ديناميكية:** تغيير الألوان في الوقت الفعلي بناءً على مدخلات المستخدم أو مصادر البيانات.

## المتطلبات المسبقة
قبل أن نغوص في الشيفرة، دعنا نتأكد من أن لديك كل ما تحتاجه:

1. **Java Development Kit (JDK)** – JDK 8 أو أحدث مثبت.  
2. **Aspose.PSD Library** – قم بتنزيل أحدث JAR من صفحة [Aspose Releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA أو Eclipse أو NetBeans أو أي محرر تفضله.  
4. **Basic Java knowledge** – الإلمام بالكائنات، الحلقات، ومعالجة الاستثناءات.

## استيراد الحزم
الآن بعد أن غطينا الأساسيات، لنستورد الفئات الضرورية. هذه الاستيرادات تمنحنا الوصول إلى معالجة PSD وتعديل طبقات التعبئة.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IColorFillSettings;
```

## كيفية إضافة تعبئة – دليل خطوة بخطوة

### الخطوة 1: إعداد بيئتك
حدد مكان وجود ملف PSD المصدر ومكان حفظ الملف المعدل، ثم حمّل المستند.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ColorFillLayer.psd";
String exportPath     = dataDir + "ColorFillLayer_output.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- `dataDir` يشير إلى المجلد الذي يحتوي على ملف PSD الخاص بك.  
- `sourceFileName` هو الملف الأصلي الذي ستقوم بتعديله.  
- `exportPath` هو المكان الذي سيتم كتابة الملف الجديد مع **إضافة طبقة تعبئة لونية** فيه.  

### الخطوة 2: التكرار عبر الطبقات
نحتاج إلى تحديد أي طبقات تعبئة موجودة حتى نتمكن إما من تعديلها أو إنشاء واحدة جديدة.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof FillLayer) {
        FillLayer fillLayer = (FillLayer) im.getLayers()[i];
```

- حلقة `for` تتكرر على كل طبقة في ملف PSD.  
- التحقق `instanceof FillLayer` يضمن أننا نتعامل فقط مع طبقات التعبئة.

### الخطوة 3: التحقق من نوع التعبئة
تأكد من أن الطبقة التي وجدناها هي **طبقة تعبئة لونية** قبل محاولة تغيير لونها.

```java
if (fillLayer.getFillSettings().getFillType() != FillType.Color) {
    throw new Exception("Wrong Fill Layer");
}
```

إذا لم يكن نوع التعبئة هو `FillType.Color`، فإننا نوقف العملية لتجنب تعديل تعبئات التدرج أو النمط عن غير قصد.

### الخطوة 4: تعيين لون التعبئة
هنا نـ **نضبط لون طبقة التعبئة**. المثال يغيّر الطبقة إلى اللون الأحمر، لكن يمكنك استبدال `Color.getRed()` بأي `Color` آخر تحتاجه (مثلاً `Color.getBlue()`، `new Color(255, 165, 0)` للبرتقالي).

```java
IColorFillSettings settings = (IColorFillSettings) fillLayer.getFillSettings();
settings.setColor(Color.getRed());
fillLayer.update();
```

- `settings.setColor(...)` يغيّر لون التعبئة الفعلي.  
- `fillLayer.update()` يجدد الطبقة لتطبيق اللون الجديد.  

### الخطوة 5: حفظ التغييرات
أخيرًا، اكتب ملف PSD المعدل مرة أخرى إلى القرص.

```java
im.save(exportPath);
break;
```

- `break` يوقف الحلقة بعد تحديث أول طبقة تعبئة مطابقة، وهذا عادة ما تريده عندما تحتاج إلى **تغيير لون تعبئة PSD** مرة واحدة.

## المشكلات الشائعة والنصائح
- **لم يتم العثور على FillLayer:** إذا لم يحتوي ملف PSD الخاص بك على طبقة تعبئة، ستحتاج إلى إنشاء واحدة باستخدام `new FillLayer(im)` وإضافتها إلى `im.getLayers()`.  
- **اللون لا يتحديث:** تأكد من استدعاء `fillLayer.update()` بعد تعيين اللون.  
- **الملف غير محفوظ:** تحقق من أن `exportPath` يشير إلى دليل قابل للكتابة وأن لديك صلاحية كتابة الملفات هناك.  

## الأسئلة المتكررة

**س: ما هو Aspose.PSD؟**  
ج: Aspose.PSD هي مكتبة Java قوية تتيح لك إنشاء وتعديل وتحويل ملفات Photoshop PSD دون الحاجة إلى Adobe Photoshop.

**س: هل يمكنني استخدام Aspose.PSD مجانًا؟**  
ج: نعم، نسخة تجريبية مجانية متاحة على صفحة [Aspose Releases page](https://releases.aspose.com/).

**س: ما هي صيغ الملفات التي يمكنني العمل معها بجانب PSD؟**  
ج: Aspose.PSD يدعم PSD، PSB، BMP، JPEG، PNG، GIF، TIFF، والمزيد.

**س: كيف أحصل على الدعم إذا واجهت مشاكل؟**  
ج: يمكنك طرح الأسئلة على [Aspose Support Forum](https://forum.aspose.com/c/psd/34).

**س: أين يمكنني شراء ترخيص كامل؟**  
ج: تُباع التراخيص عبر [Aspose Purchase page](https://purchase.aspose.com/buy).

## الخلاصة
أنت الآن تعرف **كيفية إضافة تعبئة** إلى مستند Photoshop برمجياً باستخدام Java. من خلال إنشاء أو تحديد طبقة تعبئة لونية، ضبط لونها، وحفظ النتيجة، يمكنك أتمتة مهام التصميم المتكررة، توليد أصول ديناميكية، أو دمج تعديل PSD في تطبيقات Java أكبر. جرّب ذلك—جرب ألوانًا مختلفة، أضف طبقات تعبئة متعددة، أو اجمع هذه التقنية مع ميزات Aspose.PSD الأخرى لإنشاء خطوط معالجة صور قوية.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**آخر تحديث:** 2026-03-02  
**تم الاختبار باستخدام:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**المؤلف:** Aspose