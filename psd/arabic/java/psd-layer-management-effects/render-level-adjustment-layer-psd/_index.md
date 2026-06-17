---
date: 2026-04-05
description: تعلم كيفية تصدير ملفات PSD إلى PNG وتعزيز تباين الصورة بسهولة باستخدام
  Aspose.PSD للغة Java. إتقان طبقات تعديل المستويات مع هذا الدليل خطوة بخطوة.
keywords:
- export psd to png
- how to adjust levels
- batch process psd files
linktitle: تصدير PSD إلى PNG وتطبيق طبقة تعديل المستوى في Java
second_title: Aspose.PSD Java API
title: تصدير PSD إلى PNG وعرض طبقة تعديل المستوى في Java
url: /ar/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير PSD إلى PNG وتطبيق طبقة تعديل المستوى في Java

## مقدمة

هل فتحت ملف PSD ولاحظت أن الألوان باهتة أو التباين غير متوازن؟ يمكنك بسرعة **export PSD to PNG** مع ضبط الصورة باستخدام طبقة تعديل المستويات باستخدام Aspose.PSD for Java. في هذا الدرس سنستعرض العملية بالكامل — من تحميل ملف PSD، تعديل مستوياته، إلى حفظ النتيجة كملف PNG — حتى تتمكن من تعزيز الحيوية وتحضير الأصول الجاهزة للويب في دقائق.

## إجابات سريعة
- **ماذا يعني “export PSD to PNG”؟** It converts a Photoshop document into a lossless PNG image while preserving transparency.  
- **هل يمكنني تعديل المستويات قبل التصدير؟** Yes, Aspose.PSD lets you modify input and output levels programmatically.  
- **هل أحتاج إلى ترخيص؟** A free trial works for development; a commercial license is required for production.  
- **هل المعالجة الدفعية ممكنة؟** Absolutely—you can place the code inside a loop to handle multiple PSD files.  
- **ما نسخة Java المطلوبة؟** Java 8 or newer is recommended.

## ما هو “export PSD إلى PNG”؟
يعني تصدير PSD إلى PNG أخذ ملف Photoshop متعدد الطبقات وتحويله إلى صورة Portable Network Graphics مسطحة. يدعم PNG الضغط غير الضائع وقناة ألفا، مما يجعله مثالياً للرسومات على الويب وعناصر واجهة المستخدم.

## لماذا تعديل المستويات قبل التصدير؟
يسمح تعديل المستويات بالتحكم في الظلال والوسطيات والإضاءات، مما يحسن التباين العام وتوازن الألوان. تضمن هذه الخطوة أن يبدو PNG النهائي مصقلاً دون الحاجة إلى تعديل يدوي في Photoshop.

## المتطلبات المسبقة
- **Java Development Kit (JDK)** – قم بتنزيل أحدث نسخة من موقع Oracle ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)).  
- **Aspose.PSD for Java Library** – احصل عليها من صفحة التحميل الرسمية ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)). نسخة تجريبية مجانية متاحة ([https://releases.aspose.com/](https://releases.aspose.com/)).  

## استيراد الحزم
قبل الغوص في الكود، استورد الفئات التي تمنحنا إمكانية التعامل مع PSD وتصدير PNG:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

## دليل خطوة بخطوة

### الخطوة 1: تعريف مسارات الملفات (كيفية أتمتة معالجة PSD)
حدد متغيرات واضحة وواصفة لمسار ملف PSD المصدر، وملف PSD المعدل، وموقع تصدير PNG النهائي.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

### الخطوة 2: تحميل صورة PSD
استخدم `Image.load` لقراءة ملف PSD إلى كائن `PsdImage`. يكتشف Aspose.PSD الصيغة تلقائيًا.

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### الخطوة 3: التكرار عبر الطبقات (كيفية تعديل المستويات)
قم بالتكرار عبر كل طبقة للعثور على طبقة تعديل المستويات.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (code to check for Levels Layer will be added here)
}
```

### الخطوة 4: تحديد طبقة المستويات
تحقق من كل طبقة باستخدام `instanceof LevelsLayer`. عند العثور عليها، قم بالتحويل (cast) لتتمكن من تعديل خصائصها.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (code to adjust levels will be added here)
   }
}
```

### الخطوة 5: ضبط المستويات بدقة (كيفية تعديل المستويات)
قم بضبط مستويات الإدخال والإخراج للقناة الأولى (عادةً القناة المركبة). هذه القيم أمثلة؛ لا تتردد في التجربة.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // Adjust Input Levels (0‑255):
	   channel.setInputShadowLevel((short) 10); // Darken shadows slightly
	   channel.setInputMidtoneLevel(2.0f);     // Increase midtones
	   channel.setInputHighlightLevel((short) 230); // Reduce highlights

	   // Adjust Output Levels (0‑255):
	   channel.setOutputShadowLevel((short) 20); // Darken shadows further
	   channel.setOutputHighlightLevel((short) 200); // Brighten highlights
   }
}
```

### الخطوة 6: حفظ ملف PSD المعدل (كيفية أتمتة PSD)
احفظ التغييرات مرة أخرى في ملف PSD جديد.

```java
im.save(psdPathAfterChange);
```

### الخطوة 7: تصدير كـ PNG (Export PSD to PNG)
إذا كنت بحاجة إلى نسخة PNG، قم بتكوين `PngOptions` واحفظ الصورة.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

## حالات الاستخدام الشائعة
- **تحضير أصول الويب:** تحويل نماذج PSD المقدمة من المصمم إلى PNG جاهزة للمتصفحات.  
- **المعالجة الدفعية:** أتمتة تحويل العشرات من ملفات PSD في خط أنابيب CI.  
- **إنشاء صور ديناميكي:** تعديل المستويات في الوقت الفعلي بناءً على مدخلات المستخدم قبل التصدير.

## استكشاف الأخطاء وإصلاحها ونصائح
- **خطأ Null pointer عند الوصول إلى الطبقات:** تأكد من أن ملف PSD يحتوي فعليًا على طبقة تعديل المستويات؛ وإلا أضف فحصًا للـ null.  
- **ألوان غير متوقعة بعد التصدير:** تحقق من أن نوع لون PNG مضبوط على `TruecolorWithAlpha` للحفاظ على الشفافية.  
- **الأداء مع العديد من الملفات:** أعد استخدام نفس كائن `PsdImage` عند معالجة دفعة لتقليل استهلاك الذاكرة.

## الأسئلة المتكررة

**س: هل يمكنني تعديل قنوات اللون الفردية (RGB) بشكل منفصل؟**  
A: نعم. استخدم `levelsLayer.getChannel(index)` حيث `index` = 0 (أحمر)، 1 (أخضر)، 2 (أزرق) لتعديل كل قناة على حدة.

**س: كيف أتعامل مع طبقات تعديل مستويات متعددة في ملف PSD واحد؟**  
A: تقوم الحلقة بمعالجة كل طبقة؛ كل `LevelsLayer` يتم العثور عليها سيتم تعديلها وفقًا للكود داخل كتلة `if`.

**س: هل هناك طرق أخرى لتحسين التباين غير المستويات؟**  
A: يقدم Aspose.PSD أيضًا تعديلات المنحنيات (Curves)، السطوع/التباين (Brightness/Contrast)، وتساوي التوزيع (Histogram Equalization).

**س: هل يمكنني أتمتة ذلك لمجلد من ملفات PSD؟**  
A: ضع سير العمل بالكامل داخل حلقة `File[] files = new File(dataDir).listFiles((d, name) -> name.endsWith(".psd"));` ومعالجة كل ملف على التوالي.

**س: أين يمكنني العثور على مزيد من الوثائق والدعم؟**  
A: زر المرجع الرسمي ([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) ومنتدى المجتمع ([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)).

## الخلاصة
من خلال إتقان سير عمل **export PSD to PNG** وتعلم **كيفية تعديل المستويات** برمجيًا، تحصل على تحكم كامل في جودة الصورة دون مغادرة بيئة Java الخاصة بك. سواء كنت تحضر أصولًا للويب، أو تُؤتمت خط أنابيب التصميم، أو تبني معالجًا دفعيًا، فإن Aspose.PSD for Java يجعل المهمة بسيطة وموثوقة.

---

**آخر تحديث:** 2026-04-05  
**تم الاختبار مع:** Aspose.PSD 24.11 for Java  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}