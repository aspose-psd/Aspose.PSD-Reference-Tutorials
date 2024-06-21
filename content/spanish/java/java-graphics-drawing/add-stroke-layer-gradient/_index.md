---
title: Cómo agregar degradado de capa de trazo en Java
linktitle: Cómo agregar degradado de capa de trazo en Java
second_title: API de Java Aspose.PSD
description: Aprenda a agregar y personalizar gradientes de capa de trazo en archivos PSD usando Aspose.PSD para Java con este completo tutorial paso a paso.
type: docs
weight: 10
url: /es/java/java-graphics-drawing/add-stroke-layer-gradient/
---
## Introducción
¿Alguna vez te has preguntado cómo agregar un degradado de capa de trazo a tus imágenes usando Java? Bueno, ¡estás en el lugar correcto! Hoy nos sumergimos en el mundo de Aspose.PSD para Java, una potente biblioteca que le ayuda a manipular archivos PSD con facilidad. Ya seas un desarrollador principiante o experimentado, esta guía paso a paso te guiará a través del proceso de agregar un degradado de capa de trazo a tus archivos PSD. Así que ¡abróchate el cinturón y prepárate para mejorar tus habilidades de edición gráfica!
## Requisitos previos
Antes de comenzar, hay algunas cosas que debes tener en cuenta. Asegúrate de tener lo siguiente:
1.  Kit de desarrollo de Java (JDK): asegúrese de tener JDK instalado en su sistema. Puedes descargarlo desde[sitio web de oráculo](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.PSD para la biblioteca Java: puede descargarlo desde[Página de descarga de Aspose.PSD](https://releases.aspose.com/psd/java/).
3. Un entorno de desarrollo integrado (IDE): cualquier IDE como IntelliJ IDEA, Eclipse o NetBeans funcionará.
4.  Una licencia válida: puede obtener una[licencia temporal](https://purchase.aspose.com/temporary-license/) si no tienes uno completo.
## Importar paquetes
Primero lo primero, importemos los paquetes necesarios. Estos nos permitirán utilizar las clases y métodos necesarios para manipular el archivo PSD.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```
Ahora, dividamos el ejemplo en varios pasos para una mejor comprensión.
## Paso 1: cargue el archivo PSD
 Primero, necesitamos cargar el archivo PSD que queremos modificar. Usaremos el`PsdLoadOptions` para especificar que queremos cargar los recursos de efectos.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```
## Paso 2: accede al efecto Trazo
A continuación, debemos acceder al efecto de trazo de la capa que nos interesa. Aquí, asumimos que es la tercera capa (índice 2) del archivo PSD.
```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```
## Paso 3: verificar las propiedades del efecto de trazo
Antes de realizar cualquier cambio, verifiquemos las propiedades del efecto de trazo para asegurarnos de que estamos modificando la configuración correcta.
```java
Assert.areEqual(BlendMode.Normal, gradientStroke.getBlendMode());
Assert.areEqual(255, gradientStroke.getOpacity());
Assert.areEqual(true, gradientStroke.isVisible());
GradientFillSettings fillSettings = (GradientFillSettings) gradientStroke.getFillSettings();
Assert.areEqual(Color.getBlack(), fillSettings.getColor());
Assert.areEqual(FillType.Gradient, fillSettings.getFillType());
Assert.areEqual(true, fillSettings.getAlignWithLayer());
Assert.areEqual(GradientType.Linear, fillSettings.getGradientType());
Assert.isTrue(Math.abs(90 - fillSettings.getAngle()) < 0.001, "Angle is incorrect");
Assert.areEqual(false, fillSettings.getDither());
Assert.isTrue(Math.abs(0 - fillSettings.getHorizontalOffset()) < 0.001, "Horizontal offset is incorrect");
Assert.isTrue(Math.abs(0 - fillSettings.getVerticalOffset()) < 0.001, "Vertical offset is incorrect");
Assert.areEqual(false, fillSettings.getReverse());
```
## Paso 4: modificar la configuración del relleno de degradado
Ahora es el momento de modificar la configuración del relleno degradado de acuerdo con nuestros requisitos. Cambiaremos el color, la opacidad, el modo de fusión y otras propiedades.
```java
fillSettings.setColor(Color.getGreen());
gradientStroke.setOpacity((byte) 127);
gradientStroke.setBlendMode(BlendMode.Color);
fillSettings.setAlignWithLayer(false);
fillSettings.setGradientType(GradientType.Radial);
fillSettings.setAngle(45);
fillSettings.setDither(true);
fillSettings.setHorizontalOffset(15);
fillSettings.setVerticalOffset(11);
fillSettings.setReverse(true);
```
## Paso 5: agregar y modificar puntos de color y transparencia
Agreguemos nuevos puntos de color y transparencia y modifiquemos los existentes para lograr el efecto de degradado deseado.
```java
// Agregar nuevo punto de color
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Cambiar ubicación del punto anterior
fillSettings.getColorPoints()[1].setLocation(1899);
// Agregar nuevo punto de transparencia
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Cambiar la ubicación del punto de transparencia anterior
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```
## Paso 6: guarde el archivo PSD modificado
Después de realizar todas las modificaciones necesarias, debemos guardar el archivo PSD.
```java
im.save(exportPath);
```
## Paso 7: verificar las modificaciones
Finalmente, carguemos el archivo PSD guardado y verifiquemos que nuestros cambios se hayan aplicado correctamente.
```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// comprobar puntos de color
Assert.areEqual(3, fillSetting.getColorPoints().length);
IGradientColorPoint point = fillSetting.getColorPoints()[0];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getBlack(), point.getColor());
Assert.areEqual(0, point.getLocation());
point = fillSettings.getColorPoints()[1];
Assert.areEqual(50, point.getMedianPointLocation());
Assert.areEqual(Color.getWhite(), point.getColor());
Assert.areEqual(1899, point.getLocation());
point = fillSettings.getColorPoints()[2];
Assert.areEqual(75, point.getMedianPointLocation());
Assert.areEqual(Color.getGreen(), point.getColor());
Assert.areEqual(4096, point.getLocation());
// Verificar puntos de transparencia
Assert.areEqual(3, fillSettings.getTransparencyPoints().length);
IGradientTransparencyPoint transparencyPoint1 = fillSettings.getTransparencyPoints()[0];
Assert.areEqual(50, transparencyPoint1.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint1.getOpacity());
Assert.areEqual(0, transparencyPoint1.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[1];
Assert.areEqual(50, transparencyPoint.getMedianPointLocation());
Assert.areEqual(100, transparencyPoint.getOpacity());
Assert.areEqual(2411, transparencyPoint.getLocation());
transparencyPoint1 = fillSettings.getTransparencyPoints()[2];
Assert.areEqual(25, transparencyPoint.getMedianPointLocation());
Assert.areEqual(25, transparencyPoint.getOpacity());
Assert.areEqual(4096, transparencyPoint.getLocation());
```
## Conclusión
¡Y ahí lo tienes! Ahora sabe cómo agregar y manipular gradientes de capa de trazo en archivos PSD usando Aspose.PSD para Java. Este tutorial cubrió la carga del archivo PSD, el acceso y la modificación de los efectos de trazo y el guardado de los cambios. Con estas habilidades, puede crear degradados visualmente atractivos y personalizar sus archivos PSD para satisfacer sus necesidades.
## Preguntas frecuentes
### ¿Qué es Aspose.PSD para Java?
Aspose.PSD para Java es una biblioteca que permite a los desarrolladores trabajar con archivos PSD en aplicaciones Java, proporcionando funciones para crear, manipular y convertir archivos PSD.
### ¿Necesito una licencia para usar Aspose.PSD para Java?
 Sí, necesita una licencia válida para utilizar Aspose.PSD para Java. Puedes conseguir un[licencia temporal](https://purchase.aspose.com/temporary-license/) para fines de evaluación.
### ¿Puedo usar Aspose.PSD para Java para crear archivos PSD desde cero?
¡Absolutamente! Aspose.PSD para Java proporciona API integrales para crear y manipular archivos PSD mediante programación.
### ¿Es posible aplicar otros efectos usando Aspose.PSD para Java?
Sí, puedes aplicar varios efectos como sombras, brillos y más usando Aspose.PSD para Java.
### ¿Dónde puedo encontrar la documentación de Aspose.PSD para Java?
 Puedes encontrar la documentación.[aquí](https://reference.aspose.com/psd/java/).