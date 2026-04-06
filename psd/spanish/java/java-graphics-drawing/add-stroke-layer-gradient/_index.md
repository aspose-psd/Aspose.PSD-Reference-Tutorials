---
date: 2026-01-14
description: Aprende cómo crear una capa de trazo degradado y personalizar los degradados
  de trazo en archivos PSD usando Aspose.PSD para Java con este tutorial paso a paso.
linktitle: How to Create Gradient Stroke Layer in Java
second_title: Aspose.PSD Java API
title: Cómo crear una capa de trazo degradado en Java
url: /es/java/java-graphics-drawing/add-stroke-layer-gradient/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo crear una capa de trazo degradado en Java

## Introducción
¿Alguna vez te has preguntado cómo **create gradient stroke layer** en tus archivos PSD usando Java? ¡Estás en el lugar correcto! Hoy nos sumergiremos en Aspose.PSD for Java, una biblioteca potente que te permite manipular archivos PSD sin esfuerzo. Tanto si eres nuevo en la programación gráfica como si deseas afinar diseños existentes, esta guía te mostrará paso a paso cómo añadir y personalizar degradados de trazo.

## Respuestas rápidas
- **¿Cuál es el objetivo principal?** Crear una capa de trazo degradado en un archivo PSD.  
- **¿Qué biblioteca se requiere?** Aspose.PSD for Java.  
- **¿Necesito una licencia?** Sí, se requiere una licencia válida (o temporal) para producción.  
- **¿Qué versión de Java funciona?** Java 8 o superior.  
- **¿Cuánto tiempo lleva la implementación?** Aproximadamente 10‑15 minutos para un trazo degradado básico.

## ¿Qué es una capa de trazo degradado?
Una capa de trazo degradado es un contorno vectorial alrededor de una forma o texto que transita suavemente entre colores. Con Aspose.PSD puedes definir programáticamente los colores, la opacidad, el ángulo y el tipo (lineal, radial, etc.) del trazo.

## ¿Por qué usar Aspose.PSD for Java?
- **Soporte completo de PSD** – leer, editar y escribir archivos PSD sin Photoshop.  
- **API de efectos rica** – acceder a trazo, sombra, resplandor y muchos otros efectos de capa.  
- **Multiplataforma** – funciona en cualquier SO que soporte Java.  
- **Sin dependencias nativas** – Java puro, fácil de integrar en pipelines CI.

## Requisitos previos
1. **Java Development Kit (JDK)** – Instala el JDK más reciente desde [sitio web de Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Aspose.PSD for Java** – Descarga la biblioteca desde la [página de descarga de Aspose.PSD](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse o NetBeans.  
4. **Licencia** – Obtén una [licencia temporal](https://purchase.aspose.com/temporary-license/) si no tienes una completa.

## Importar paquetes
Primero, importa las clases que necesitaremos para cargar el PSD, acceder a los efectos y configurar los rellenos degradados.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
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

Ahora dividamos el proceso en pasos claros.

## Paso 1: Cargar el archivo PSD
Cargamos el PSD de origen y habilitamos los recursos de efecto para que el efecto de trazo esté disponible.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);
PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

## Paso 2: Acceder al efecto de trazo
Suponiendo que el trazo que queremos modificar pertenece a la tercera capa (índice 2), recuperamos su `StrokeEffect`.

```java
StrokeEffect gradientStroke = (StrokeEffect) im.getLayers()[2].getBlendingOptions().getEffects()[0];
```

## Paso 3: Verificar las propiedades del efecto de trazo
Antes de realizar cambios, confirmamos la configuración existente para saber exactamente qué estamos actualizando.

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

## Paso 4: Modificar la configuración del relleno degradado
Aquí cambiamos el color, la opacidad, el modo de fusión y otras propiedades para lograr el aspecto deseado.

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

## Paso 5: Añadir y modificar puntos de color y transparencia
Añadimos nuevos puntos de color y transparencia, y luego ajustamos los existentes para dar forma al degradado.

```java
// Add new color point
GradientColorPoint colorPoint = fillSettings.addColorPoint();
colorPoint.setColor(Color.getGreen());
colorPoint.setLocation(4096);
colorPoint.setMedianPointLocation(75);
// Change location of previous point
fillSettings.getColorPoints()[1].setLocation(1899);
// Add new transparency point
GradientTransparencyPoint transparencyPoint = fillSettings.addTransparencyPoint();
transparencyPoint.setOpacity(25);
transparencyPoint.setMedianPointLocation(25);
transparencyPoint.setLocation(4096);
// Change location of previous transparency point
fillSettings.getTransparencyPoints()[1].setLocation(2411);
```

## Paso 6: Guardar el archivo PSD modificado
Después de todos los ajustes, escribimos el archivo actualizado de nuevo en el disco.

```java
im.save(exportPath);
```

## Paso 7: Verificar las modificaciones
Cargamos el archivo guardado y comprobamos que cada propiedad refleje los cambios aplicados.

```java
PsdImage img = (PsdImage) Image.load(exportPath, loadOptions);
StrokeEffect gradientStrokeEffect = (StrokeEffect) img.getLayers()[2].getBlendingOptions().getEffects()[0];
Assert.areEqual(BlendMode.Color, gradientStrokeEffect.getBlendMode());
Assert.areEqual(127, gradientStrokeEffect.getOpacity());
Assert.areEqual(true, gradientStrokeEffect.isVisible());
GradientFillSettings fillSetting = (GradientFillSettings) gradientStrokeEffect.getFillSettings();
Assert.areEqual(Color.getGreen(), fillSetting.getColor());
Assert.areEqual(FillType.Gradient, fillSetting.getFillType());
// Check color points
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
// Check transparency points
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
Ahora sabes cómo **create gradient stroke layer** en archivos PSD usando Aspose.PSD for Java. Al cargar un PSD, acceder al efecto de trazo, ajustar la configuración del relleno degradado y guardar el resultado, puedes producir gráficos de nivel profesional de forma programática sin abrir Photoshop.

## Preguntas frecuentes
### ¿Qué es Aspose.PSD for Java?
Aspose.PSD for Java es una biblioteca que permite a los desarrolladores trabajar con archivos PSD en aplicaciones Java, ofreciendo funcionalidades para crear, manipular y convertir archivos PSD.

### ¿Necesito una licencia para usar Aspose.PSD for Java?
Sí, necesitas una licencia válida para usar Aspose.PSD for Java. Puedes obtener una [licencia temporal](https://purchase.aspose.com/temporary-license/) para propósitos de evaluación.

### ¿Puedo usar Aspose.PSD for Java para crear archivos PSD desde cero?
¡Absolutamente! Aspose.PSD for Java proporciona APIs completas para crear y manipular archivos PSD de forma programática.

### ¿Es posible aplicar otros efectos usando Aspose.PSD for Java?
Sí, puedes aplicar varios efectos como sombra, resplandor y más usando Aspose.PSD for Java.

### ¿Dónde puedo encontrar la documentación de Aspose.PSD for Java?
Puedes encontrar la documentación [aquí](https://reference.aspose.com/psd/java/).

---

**Última actualización:** 2026-01-14  
**Probado con:** Aspose.PSD for Java 24.11  
**Autor:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
