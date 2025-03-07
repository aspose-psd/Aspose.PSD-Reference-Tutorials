---
title: كيفية إضافة نمط طبقة السكتة الدماغية في جافا
linktitle: كيفية إضافة نمط طبقة السكتة الدماغية في جافا
second_title: Aspose.PSD جافا API
description: تعرف على كيفية إضافة نمط طبقة الحد إلى ملفات PSD باستخدام Aspose.PSD لـ Java. اتبع هذا الدليل خطوة بخطوة لتحسين صورك بسهولة.
weight: 11
url: /ar/java/java-graphics-drawing/add-stroke-layer-pattern/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية إضافة نمط طبقة السكتة الدماغية في جافا

## مقدمة
قد تبدو إضافة نمط طبقة حد إلى صورة في Java مهمة شاقة، ولكن مع Aspose.PSD لـ Java، أصبح الأمر أسهل مما تعتقد. سواء كنت تصمم رسومات أو تعمل على تطبيقات تحرير الصور، سيرشدك هذا الدليل خلال العملية خطوة بخطوة. هل أنت مستعد للبدء؟ دعونا الغوص في!
## المتطلبات الأساسية
قبل البدء، ستحتاج إلى بعض الأشياء:
- Java Development Kit (JDK): تأكد من تثبيت JDK على نظامك.
-  Aspose.PSD لـ Java: قم بتنزيل المكتبة من[هنا](https://releases.aspose.com/psd/java/) وإدراجه في مشروعك.
- بيئة تطوير متكاملة (IDE): استخدم بيئة التطوير المتكاملة (IDE) المفضلة لديك مثل IntelliJ IDEA أو Eclipse.
## حزم الاستيراد
أول الأشياء أولاً، تحتاج إلى استيراد الحزم الضرورية إلى مشروع Java الخاص بك. هذه الحزم ضرورية للعمل مع Aspose.PSD.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```
## الخطوة 1: قم بتحميل ملف PSD
الخطوة الأولى في إضافة نمط طبقة الحد هي تحميل ملف PSD الذي تريد تحريره.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
من خلال تحميل ملف PSD، يمكنك الآن الوصول إلى طبقاته وتأثيراته ومعالجتها.
## الخطوة 2: إعداد بيانات النمط الجديد
بعد ذلك، تحتاج إلى إعداد بيانات النمط الجديد التي ستطبقها على طبقة الحد.
```java
int[] newPattern = new int[]
{
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
    Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
};
Rectangle newPatternBounds = new Rectangle(0, 0, 4, 4);
UUID guid = UUID.randomUUID();
```
سيتم استخدام بيانات النمط هذه لإنشاء تأثير الحد الجديد.
## الخطوة 3: الوصول إلى تأثير السكتة الدماغية
لتعديل تأثير السكتة الدماغية، تحتاج إلى الوصول إلى الطبقة المحددة وخيارات المزج الخاصة بها.
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
وهذا يضمن أنك تعمل مع الطبقة والتأثير الصحيحين.
## الخطوة 4: تعديل تأثير السكتة الدماغية
الآن، دعونا نعدل تأثير الحد باستخدام بيانات النمط الجديد.
### تحديث خصائص تأثير السكتة الدماغية
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
### قم بتحديث مورد النمط
```java
PattResource resource;
for (int i = 0; i < im.getGlobalLayerResources().length; i++)
{
    if (im.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource = (PattResource)im.getGlobalLayerResources()[i];
        resource.setPatternId(guid.toString());
        resource.setName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
        resource.setPattern(newPattern, newPatternBounds);
    }
}
```
يقوم مقتطف الكود هذا بتحديث مورد النمط ببيانات النمط الجديد.
## الخطوة 5: تطبيق النمط الجديد
أخيرًا، قم بتطبيق النمط الجديد على تأثير السكتة الدماغية واحفظ التغييرات.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
وهذا يضمن تطبيق النمط الجديد بشكل صحيح وحفظ الملف مع التغييرات.
## الخطوة 6: التحقق من التغييرات
للتأكد من أن كل شيء يعمل بشكل صحيح، قم بتحميل الملف مرة أخرى وتحقق من التغييرات.
```java
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
PattResource resource1 = null;
for (int i = 0; i < img.getGlobalLayerResources().length; i++)
{
    if (img.getGlobalLayerResources()[i] instanceof PattResource)
    {
        resource1 = (PattResource)img.getGlobalLayerResources()[i];
    }
}
try
{
    Assert.areEqual(newPattern, resource1.getPatternData());
    Assert.areEqual(newPatternBounds, new Rectangle(0, 0, resource1.getWidth(), resource1.getHeight()));
    Assert.areEqual(guid.toString(), resource1.getPatternId());
    Assert.areEqual(BlendMode.Color, patternStrokeEffect.getBlendMode());
    Assert.areEqual(127, patternStrokeEffect.getOpacity());
    Assert.areEqual(true, patternStrokeEffect.isVisible());
    PatternFillSettings fillSettings1 = (PatternFillSettings)patternStrokeEffect.getFillSettings();
    Assert.areEqual(FillType.Pattern, fillSettings1.getFillType());
}
catch (Exception e)
{
    System.out.println(e.getMessage());
}
```
تتحقق هذه الخطوة من أن بيانات النمط قد تم تطبيقها بشكل صحيح على تأثير الحد.
## خاتمة
وهنا لديك! لقد نجحت في إضافة نمط طبقة الحد إلى ملف PSD باستخدام Aspose.PSD لـ Java. باتباع هذه الخطوات، يمكنك تخصيص صورك وتحسينها بسهولة. ترميز سعيد!
## الأسئلة الشائعة
### ما هو Aspose.PSD لجافا؟
Aspose.PSD for Java هي مكتبة تتيح للمطورين إنشاء ملفات PSD (مستندات Photoshop) وتحريرها وتحويلها برمجيًا.
### هل يمكنني استخدام Aspose.PSD لـ Java في مشروع تجاري؟
 نعم يمكنك استخدامه في المشاريع التجارية. يمكنك شراء ترخيص من[هنا](https://purchase.aspose.com/buy).
### هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.PSD لـ Java؟
 نعم، يمكنك تنزيل نسخة تجريبية مجانية من[هنا](https://releases.aspose.com/).
### كيف يمكنني الحصول على الدعم لـ Aspose.PSD لـ Java؟
 يمكنك الحصول على الدعم من منتديات مجتمع Aspose[هنا](https://forum.aspose.com/c/psd/34).
### ما هي متطلبات النظام لـ Aspose.PSD لـ Java؟
تحتاج إلى تثبيت JDK وIDE للتطوير. تدعم المكتبة أنظمة تشغيل متعددة بما في ذلك Windows وLinux وmacOS.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
