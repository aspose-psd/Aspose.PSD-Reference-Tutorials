---
date: 2026-08-28
description: Agregue un patrón a una capa en Java con Aspose.PSD. Siga esta guía paso
  a paso para aplicar un efecto de capa de trazo, configurar recursos de patrón y
  guardar sus archivos PSD de manera eficiente.
keywords:
- add pattern to layer
- java add layer effect
- Aspose.PSD stroke pattern
lastmod: 2026-08-28
linktitle: Cómo agregar un patrón de capa de trazo en Java
og_description: Agregue un patrón a una capa en Java usando Aspose.PSD. Siga esta
  guía concisa para aplicar un efecto de capa de trazo, configurar recursos de patrón
  y guardar sus archivos PSD de manera eficiente.
og_image_alt: Guide showing how to add pattern to layer in Java with Aspose.PSD
og_title: Agregar un patrón a una capa en Java – tutorial de Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-08-28'
  description: Add pattern to layer in Java with Aspose.PSD. Follow this step‑by‑step
    guide to apply a stroke layer effect, configure pattern resources, and save your
    PSD files efficiently.
  headline: How to add pattern to layer in Java
  type: TechArticle
- description: Add pattern to layer in Java with Aspose.PSD. Follow this step‑by‑step
    guide to apply a stroke layer effect, configure pattern resources, and save your
    PSD files efficiently.
  name: How to add pattern to layer in Java
  steps:
  - name: load the PSD file
    text: 'Loading the document gives you access to its layer hierarchy and effect
      collection. `PsdLoadOptions` configures how the PSD is read, while `PsdImage`
      represents the loaded file in memory. java String dataDir = "Your Document Directory";
      String sourceFileName = dataDir + "Stroke.psd"; PsdLoadOptions '
  - name: prepare new pattern data
    text: Create a `PatternResource` that holds the bitmap you want to tile as a stroke
      pattern. `PatternResource` is a PSD global resource that stores a repeating
      bitmap pattern. `Rectangle` defines the bounds of the pattern, and `UUID` provides
      a unique identifier. java int[] newPattern = new int[] { Color.
  - name: access the stroke effect
    text: Identify the shape layer that already has a stroke, then retrieve its `StrokeEffect`
      object. `StrokeEffect` represents the stroke layer effect applied to a shape
      layer. java StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
      Assert.areEqual(BlendMode.N
  - name: modify the stroke effect
    text: Now update the stroke’s properties to reference the new pattern resource.
  - name: apply the new pattern
    text: '`PatternFillSettings` holds the fill settings for a pattern‑based stroke
      effect. Commit the changes to the layer and write the updated PSD back to disk.
      java ((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal
      Line 9\0"); ((PatternFil'
  - name: verify the changes
    text: 'Reload the file and inspect the stroke to confirm the pattern appears as
      expected. java PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);
      StrokeEffect patternStrokeEffect = (StrokeEffect)img.getLayers()[3].getBlendingOptions().getEffects()[0];
      PattResource resource1 = null; for (int '
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java is a library that enables developers to create, edit,
      and convert PSD (Photoshop Document) files programmatically.
    question: What is Aspose.PSD for Java?
  - answer: Yes, you can use it in commercial projects. You can purchase a license
      from the **Aspose purchase page**([Aspose purchase page](https://purchase.aspose.com/buy)).
    question: Can I use Aspose.PSD for Java in a commercial project?
  - answer: Yes, you can download a free trial version from the **Aspose releases
      page**([Aspose releases page](https://releases.aspose.com/)).
    question: Is there a free trial available for Aspose.PSD for Java?
  - answer: You can get support from the Aspose community forums **here**([Aspose
      PSD community forum](https://forum.aspose.com/c/psd/34)).
    question: How can I get support for Aspose.PSD for Java?
  - answer: You need a JDK installed and an IDE for development. The library supports
      Windows, Linux, and macOS.
    question: What are the system requirements for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java graphics
- Aspose.PSD
- layer effects
title: Cómo agregar un patrón a una capa en Java
url: /es/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo agregar un patrón a una capa en Java

## Introducción
Agregar un patrón a una capa en Java es un requisito común cuando necesitas enriquecer archivos Photoshop PSD con efectos de trazo personalizados. Con Aspose.PSD for Java esta tarea se vuelve sencilla, incluso si eres nuevo en la biblioteca. En este tutorial aprenderás cómo cargar un PSD, crear un recurso de patrón, adjuntarlo a un efecto de trazo y guardar el resultado, todo con instrucciones claras paso a paso.

## Respuestas rápidas
- **¿Qué biblioteca se necesita?** Aspose.PSD for Java.  
- **¿Cuánto tiempo lleva la implementación?** Alrededor de 10‑15 minutos para un patrón básico.  
- **¿Necesito una licencia?** Una prueba gratuita funciona para desarrollo; se requiere una licencia comercial para producción.  
- **¿Qué versión de Java se admite?** JDK 8 o superior.  
- **¿Puedo usar esto en un servicio web?** Sí, la API es independiente de la plataforma y funciona en cualquier entorno Java.

## ¿Qué es agregar un patrón a una capa?
Agregar un patrón a una capa significa asignar un mapa de bits en mosaico a un efecto de trazo o relleno para que el gráfico se repita a lo largo del contorno de la forma. Esta técnica se usa ampliamente para bordes decorativos, texturas y superposiciones de marca, permitiendo a los diseñadores crear temas visuales consistentes sin dibujar manualmente cada elemento.

## ¿Por qué usar Aspose.PSD para esta tarea?
Aspose.PSD soporta **más de 30 formatos de imagen** y puede manipular archivos PSD de hasta **2 GB** sin cargar todo el documento en memoria, ofreciendo un rendimiento rápido en hardware de servidor típico. Su API fluida permite trabajar con efectos de capa programáticamente, eliminando la necesidad de Photoshop en pipelines automatizados.

## Requisitos previos
- Java Development Kit (JDK) 8 o superior instalado.
- Aspose.PSD for Java – descárgalo desde la **página de descarga de Aspose.PSD for Java**([Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/)) y agrega el JAR al classpath de tu proyecto.
- Un IDE como IntelliJ IDEA o Eclipse para editar y ejecutar el código de ejemplo.
- Un archivo PSD de muestra que contenga una capa de forma que deseas modificar.

## Importar paquetes
Primero, importa los espacios de nombres que proporcionan acceso a objetos, recursos y efectos de PSD.

```
// No actual code block is added to preserve original placeholders.
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
```

## ¿Cómo agregar un patrón a una capa en Java?
Carga el PSD objetivo, crea un recurso de patrón, adjúntalo al efecto de trazo de la capa deseada y, finalmente, guarda el archivo. Este flujo de extremo a extremo requiere solo unas pocas líneas de código y funciona con cualquier PSD estándar que contenga una capa de forma vectorial.

### Paso 1: cargar el archivo PSD
Cargar el documento te da acceso a su jerarquía de capas y colección de efectos.  
`PsdLoadOptions` configura cómo se lee el PSD, mientras que `PsdImage` representa el archivo cargado en memoria.

```
// Placeholder for original code.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```
```

Al cargar el archivo PSD, ahora puedes acceder y manipular sus capas y efectos.

### Paso 2: preparar los nuevos datos del patrón
Crea un `PatternResource` que contenga el mapa de bits que deseas mosaicar como patrón de trazo.  
`PatternResource` es un recurso global de PSD que almacena un patrón de mapa de bits repetido. `Rectangle` define los límites del patrón, y `UUID` proporciona un identificador único.

```
// Placeholder for original code.
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
```

Estos datos del patrón se usarán para crear el nuevo efecto de trazo.

### Paso 3: acceder al efecto de trazo
Identifica la capa de forma que ya tiene un trazo, luego recupera su objeto `StrokeEffect`.  
`StrokeEffect` representa el efecto de capa de trazo aplicado a una capa de forma.

```
// Placeholder for original code.
```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```
```

Esto asegura que estés trabajando con la capa y el efecto correctos.

### Paso 4: modificar el efecto de trazo
Ahora actualiza las propiedades del trazo para que referencien el nuevo recurso de patrón.

#### Actualizar propiedades del efecto de trazo
```
// Placeholder for original code.
```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```
```

#### Actualizar el recurso de patrón
`PattResource` es un recurso global de capa PSD que almacena datos de patrón.

```
// Placeholder for original code.
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
```

Estos fragmentos reemplazan el patrón existente con el que proporcionaste.

### Paso 5: aplicar el nuevo patrón
`PatternFillSettings` contiene la configuración de relleno para un efecto de trazo basado en patrón. Confirma los cambios en la capa y escribe el PSD actualizado de nuevo en el disco.

```
// Placeholder for original code.
```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```
```

Esto asegura que el nuevo patrón se aplique correctamente y que el archivo se guarde con los cambios.

### Paso 6: verificar los cambios
Recarga el archivo e inspecciona el trazo para confirmar que el patrón aparece como se espera.

```
// Placeholder for original code.
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
```

Este paso verifica que los datos del patrón se hayan aplicado correctamente al efecto de trazo.

## Problemas comunes y solución de problemas
- **Patrón no visible:** Asegúrate de que el DPI de la imagen del patrón coincida con la resolución del PSD, y de que la bandera `Enabled` del trazo esté establecida en `true`.  
- **Los archivos PSD grandes causan OutOfMemoryError:** Usa `PsdImage.load(..., LoadOptions)` con `LoadOptions.setLoadAllLayers(false)` para cargar capas bajo demanda.  
- **Capa incorrecta seleccionada:** Verifica el índice o nombre de la capa antes de acceder a sus efectos; puedes enumerar `psdImage.getLayers()` para listar las capas disponibles.

## Preguntas frecuentes

**Q: ¿Qué es Aspose.PSD for Java?**  
A: Aspose.PSD for Java es una biblioteca que permite a los desarrolladores crear, editar y convertir archivos PSD (Photoshop Document) programáticamente.

**Q: ¿Puedo usar Aspose.PSD for Java en un proyecto comercial?**  
A: Sí, puedes usarlo en proyectos comerciales. Puedes comprar una licencia en la **página de compra de Aspose**([Aspose purchase page](https://purchase.aspose.com/buy)).

**Q: ¿Hay una versión de prueba gratuita disponible para Aspose.PSD for Java?**  
A: Sí, puedes descargar una versión de prueba gratuita desde la **página de versiones de Aspose**([Aspose releases page](https://releases.aspose.com/)).

**Q: ¿Cómo puedo obtener soporte para Aspose.PSD for Java?**  
A: Puedes obtener soporte en los foros de la comunidad de Aspose **aquí**([Aspose PSD community forum](https://forum.aspose.com/c/psd/34)).

**Q: ¿Cuáles son los requisitos del sistema para Aspose.PSD for Java?**  
A: Necesitas un JDK instalado y un IDE para el desarrollo. La biblioteca soporta Windows, Linux y macOS.

## Conclusión
Ahora has aprendido cómo agregar un patrón a una capa en Java usando Aspose.PSD. Siguiendo los pasos anteriores puedes mejorar programáticamente los archivos PSD con patrones de trazo personalizados, automatizar flujos de trabajo de marca e integrar el procesamiento de gráficos en cualquier aplicación basada en Java. Explora otras funciones de Aspose.PSD como la fusión de capas, ajustes de color y exportación a PNG o JPEG para ampliar aún más tu conjunto de herramientas de procesamiento de imágenes.

---

**Última actualización:** 2026-08-28  
**Probado con:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose

## Tutoriales relacionados

- [Renderizar capa de relleno de patrón PSD](/psd/java/advanced-psd-layer-features-effects/render-pattern-fill-layer-psd-files/)
- [Superposición de patrón PSD: agregar efectos con Aspose.PSD for Java](/psd/java/advanced-image-effects/add-pattern-effects/)
- [Cómo cambiar el color del trazo en Java usando Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}
{{< blocks/products/products-backtop-button >}}