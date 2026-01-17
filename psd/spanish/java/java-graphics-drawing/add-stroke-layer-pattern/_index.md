---
date: 2026-01-17
description: Aprende cómo agregar patrones de trazo en Java con Aspose.PSD para Java.
  Sigue esta guía paso a paso para mejorar tus imágenes PSD rápidamente.
linktitle: How to Add Stroke Layer Pattern in Java
second_title: Aspose.PSD Java API
title: Cómo agregar un patrón de trazo en Java usando Aspose.PSD
url: /es/java/java-graphics-drawing/add-stroke-layer-pattern/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo agregar un patrón de trazo Java usando Aspose.PSD

## Introducción
Si necesitas **agregar un patrón de trazo java** a un archivo Photoshop, Aspose.PSD para Java lo hace sorprendentemente sencillo. Ya sea que estés construyendo una herramienta de diseño gráfico, automatizando ediciones por lotes o simplemente experimentando con efectos de capa, este tutorial te guía paso a paso—desde cargar el PSD hasta verificar el nuevo patrón. Vamos a sumergirnos y ver qué rápido puedes mejorar tus imágenes.

## Respuestas rápidas
- **¿Qué biblioteca necesito?** Aspose.PSD para Java  
- **¿Qué versión de Java es compatible?** JDK 8 o posterior  
- **¿Necesito una licencia para pruebas?** Una prueba gratuita funciona para desarrollo; se requiere una licencia para producción  
- **¿Cuánto tiempo lleva la implementación?** Aproximadamente 10‑15 minutos para un trazo de patrón básico  
- **¿Puedo reutilizar el patrón en varias capas?** Sí, solo asigne el mismo `PattResource` a otras capas  

## ¿Qué es agregar un patrón de trazo en Java?
Agregar un patrón de trazo en Java significa aplicar un relleno personalizado (a menudo un mapa de bits repetido) al efecto de trazo de una capa. Esta técnica te permite crear contornos estilizados—piensa en una línea punteada, una textura de ladrillos o un borde gráfico personalizado—directamente dentro de un archivo PSD sin abrir Photoshop.

## ¿Por qué usar Aspose.PSD para agregar un patrón de trazo java?
- **Fidelidad total del PSD** – Todos los efectos de capa, recursos y modos de fusión se conservan.  
- **No se requiere Photoshop nativo** – Funciona en cualquier SO con un JDK.  
- **Control programático** – Automatiza el procesamiento por lotes o intégralo en servicios del lado del servidor.  
- **API rica** – Acceso a recursos globales, rellenos de patrón y modos de fusión en una única interfaz fluida.

## Requisitos previos
- **Java Development Kit (JDK)** – Asegúrate de que JDK 8 o una versión más reciente esté instalada.  
- **Aspose.PSD para Java** – Descarga la biblioteca desde [aquí](https://releases.aspose.com/psd/java/) y agrega el JAR a la ruta de clases de tu proyecto.  
- **IDE** – IntelliJ IDEA, Eclipse o cualquier editor que prefieras.

## Importar paquetes
Primero, importa las clases que necesitarás para manejar archivos PSD, colores, rectángulos y efectos de trazo.

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

## Paso 1: Cargar el archivo PSD
Carga el PSD de origen para que puedas trabajar con sus capas y recursos.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Paso 2: Preparar los nuevos datos del patrón
Crea un patrón simple de 4 × 4 píxeles que se utilizará para el trazo.

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

## Paso 3: Acceder al efecto de trazo
Localiza el efecto de trazo en la capa objetivo (en este ejemplo, la cuarta capa).

```java
StrokeEffect patternStroke = (StrokeEffect)im.getLayers()[3].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Normal, patternStroke.getBlendMode());
Assert.areEqual(255, patternStroke.getOpacity());
Assert.areEqual(true, patternStroke.isVisible());
PatternFillSettings fillSettings = (PatternFillSettings)patternStroke.getFillSettings();
Assert.areEqual(FillType.Pattern, fillSettings.getFillType());
```

## Paso 4: Modificar el efecto de trazo
### Actualizar propiedades del efecto de trazo
Ajusta la opacidad y el modo de fusión para ver el impacto visual del nuevo patrón.

```java
patternStroke.setOpacity((byte)127);
patternStroke.setBlendMode(BlendMode.Color);
```

### Actualizar el recurso de patrón
Reemplaza el recurso de patrón global existente con el que acabas de crear.

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

## Paso 5: Aplicar el nuevo patrón
Vincula el recurso de patrón actualizado al efecto de trazo y guarda el PSD.

```java
((PatternFillSettings)patternStroke.getFillSettings()).setPatternName("$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0");
((PatternFillSettings)patternStroke.getFillSettings()).setPatternId(guid.toString() + "\0");
im.save(exportPath);
```

## Paso 6: Verificar los cambios
Recarga el archivo y confirma que el nuevo patrón, la opacidad y el modo de fusión se hayan aplicado correctamente.

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

## Problemas comunes y soluciones
| Problema | Causa | Solución |
|----------|-------|----------|
| El patrón no aparece | Referencia `PatternId` incorrecta | Asegúrate de que el `PatternId` establecido en `PattResource` coincida con el usado en `PatternFillSettings`. |
| El trazo desaparece después de guardar | Opacidad establecida en 0 o efecto oculto | Verifica que `setOpacity` esté entre 0‑255 y que `isVisible()` devuelva `true`. |
| Colores inesperados | Desajuste del modo de fusión | Usa `BlendMode.Color` (u otro modo) que coincida con la intención de tu diseño. |

## Preguntas frecuentes
### ¿Qué es Aspose.PSD para Java?
Aspose.PSD para Java es una biblioteca que permite a los desarrolladores crear, editar y convertir archivos PSD (Photoshop Document) de forma programática.

### ¿Puedo usar Aspose.PSD para Java en un proyecto comercial?
Sí, puedes usarla en proyectos comerciales. Puedes adquirir una licencia desde [aquí](https://purchase.aspose.com/buy).

### ¿Hay una versión de prueba gratuita disponible para Aspose.PSD para Java?
Sí, puedes descargar una versión de prueba gratuita desde [aquí](https://releases.aspose.com/).

### ¿Cómo puedo obtener soporte para Aspose.PSD para Java?
Puedes obtener soporte en los foros de la comunidad de Aspose [aquí](https://forum.aspose.com/c/psd/34).

### ¿Cuáles son los requisitos del sistema para Aspose.PSD para Java?
Necesitas tener instalado JDK y un IDE para el desarrollo. La biblioteca soporta múltiples sistemas operativos, incluidos Windows, Linux y macOS.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Última actualización:** 2026-01-17  
**Probado con:** Aspose.PSD para Java 24.12 (última versión al momento de escribir)  
**Autor:** Aspose