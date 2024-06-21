---
title: Cómo agregar un patrón de capa de trazo en Java
linktitle: Cómo agregar un patrón de capa de trazo en Java
second_title: API de Java Aspose.PSD
description: Aprenda a agregar un patrón de capa de trazo a archivos PSD usando Aspose.PSD para Java. Siga esta guía paso a paso para mejorar sus imágenes fácilmente.
type: docs
weight: 11
url: /es/java/java-graphics-drawing/add-stroke-layer-pattern/
---
## Introducción
Agregar un patrón de capa de trazo a una imagen en Java puede parecer una tarea desalentadora, pero con Aspose.PSD para Java, es más fácil de lo que piensa. Ya sea que esté diseñando gráficos o trabajando en aplicaciones de edición de fotografías, esta guía lo guiará a través del proceso paso a paso. ¿Listo para comenzar? ¡Vamos a sumergirnos!
## Requisitos previos
Antes de comenzar, necesitará algunas cosas:
- Kit de desarrollo de Java (JDK): asegúrese de tener JDK instalado en su sistema.
-  Aspose.PSD para Java: descargue la biblioteca desde[aquí](https://releases.aspose.com/psd/java/) e inclúyelo en tu proyecto.
- Un IDE: utilice su entorno de desarrollo integrado (IDE) favorito, como IntelliJ IDEA o Eclipse.
## Importar paquetes
Lo primero es lo primero: debe importar los paquetes necesarios a su proyecto Java. Estos paquetes son esenciales para trabajar con Aspose.PSD.
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.examples.Utils.Utils;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.fileformats.psd.layers.layerresources.PattResource;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import java.util.UUID;
```
## Paso 1: cargue el archivo PSD
El primer paso para agregar un patrón de capa de trazo es cargar el archivo PSD que desea editar.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
Al cargar el archivo PSD, ahora puede acceder y manipular sus capas y efectos.
## Paso 2: preparar nuevos datos de patrón
continuación, debe preparar los nuevos datos del patrón que aplicará a la capa de trazo.
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
Estos datos de patrón se utilizarán para crear el nuevo efecto de trazo.
## Paso 3: accede al efecto Trazo
Para modificar el efecto de trazo, debe acceder a la capa específica y sus opciones de fusión.
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
Esto garantiza que está trabajando con la capa y el efecto correctos.
## Paso 4: modificar el efecto del trazo
Ahora, modifiquemos el efecto del trazo con los nuevos datos del patrón.
### Actualizar propiedades del efecto de trazo
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
### Actualizar el recurso de patrón
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
Este fragmento de código actualiza el recurso de patrón con los datos del nuevo patrón.
## Paso 5: aplique el nuevo patrón
Finalmente, aplique el nuevo patrón al efecto de trazo y guarde los cambios.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
Esto garantiza que el nuevo patrón se aplique correctamente y que el archivo se guarde con los cambios.
## Paso 6: verificar los cambios
Para asegurarse de que todo funcionó correctamente, cargue el archivo nuevamente y verifique los cambios.
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
Este paso verifica que los datos del patrón se hayan aplicado correctamente al efecto de trazo.
## Conclusión
¡Y ahí lo tienes! Ha agregado con éxito un patrón de capa de trazo a un archivo PSD usando Aspose.PSD para Java. Siguiendo estos pasos, podrá personalizar y mejorar sus imágenes con facilidad. ¡Feliz codificación!
## Preguntas frecuentes
### ¿Qué es Aspose.PSD para Java?
Aspose.PSD para Java es una biblioteca que permite a los desarrolladores crear, editar y convertir archivos PSD (Documentos de Photoshop) mediante programación.
### ¿Puedo utilizar Aspose.PSD para Java en un proyecto comercial?
 Sí, puedes usarlo en proyectos comerciales. Puede adquirir una licencia en[aquí](https://purchase.aspose.com/buy).
### ¿Hay una prueba gratuita disponible para Aspose.PSD para Java?
 Sí, puedes descargar una versión de prueba gratuita desde[aquí](https://releases.aspose.com/).
### ¿Cómo puedo obtener soporte para Aspose.PSD para Java?
 Puede obtener soporte en los foros de la comunidad Aspose.[aquí](https://forum.aspose.com/c/psd/34).
### ¿Cuáles son los requisitos del sistema para Aspose.PSD para Java?
Necesita JDK instalado y un IDE para el desarrollo. La biblioteca admite múltiples sistemas operativos, incluidos Windows, Linux y macOS.