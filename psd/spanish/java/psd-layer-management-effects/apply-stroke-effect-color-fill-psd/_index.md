---
date: 2026-04-03
description: Aprende cómo guardar PSD como PNG con un efecto de trazo y relleno de
  color usando Aspose.PSD para Java. Esta guía paso a paso muestra cómo exportar PSD
  a PNG rápidamente.
keywords:
- save psd as png
- export psd to png
- set stroke color
- apply layer effects
- customize stroke width
linktitle: Guardar PSD como PNG con efecto de trazo – Java
second_title: Aspose.PSD Java API
title: Guardar PSD como PNG con efecto de trazo – Java
url: /es/java/psd-layer-management-effects/apply-stroke-effect-color-fill-psd/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Guardar PSD como PNG con efecto de trazo y relleno de color – Java

## Introducción

En esta guía, aprenderás cómo **guardar PSD como PNG** aplicando un efecto de trazo con un relleno de color usando Aspose.PSD para Java. Ya seas un desarrollador experimentado o estés comenzando, este tutorial paso a paso hará que sea fácil completar la tarea. Cubriremos todo, desde la configuración del entorno hasta la exportación de la imagen final, para que puedas **exportar PSD a PNG** rápidamente en tus propios proyectos.

## Respuestas rápidas
- **¿Qué logra este tutorial?** Muestra cómo guardar un archivo PSD como PNG después de aplicar un efecto de trazo personalizable.  
- **¿Qué biblioteca se utiliza?** Aspose.PSD para Java.  
- **¿Necesito una licencia?** Una prueba gratuita funciona para pruebas; se requiere una licencia para producción.  
- **¿Puedo cambiar el color del trazo?** Sí, puedes establecer cualquier color mediante `ColorFillSettings`.  
- **¿Es posible el procesamiento por lotes?** Absolutamente, envuelve el código en un bucle para procesar múltiples archivos PSD.

## ¿Qué es “guardar PSD como PNG”?
Guardar un PSD como PNG significa convertir el archivo nativo con capas de Photoshop en un formato de imagen plano y apto para la web, preservando la fidelidad visual. Esto es útil cuando necesitas mostrar contenido PSD en sitios web, aplicaciones móviles o cualquier plataforma que no admita archivos PSD directamente.

## ¿Por qué aplicar un efecto de trazo con relleno de color?
Un trazo añade un contorno nítido alrededor del contenido de la capa, haciendo que los gráficos destaquen sobre fondos complejos. Combinarlo con un color de relleno personalizado te permite marcar imágenes, resaltar elementos de UI o crear miniaturas llamativas sin salir de Photoshop.

## Requisitos previos

1. **Java Development Kit (JDK) 8+** – asegúrate de que `java` esté en tu PATH.  
2. **Aspose.PSD para Java** – descarga desde el [sitio web](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse o cualquier editor que prefieras.  
4. **PSD de muestra** – un archivo que ya contenga un efecto de trazo (o añádelo en Photoshop).  
5. **Conocimientos básicos de Java** – escribirás unas pocas líneas de código, pero nada avanzado.

Una vez que tengas todo listo, podemos comenzar a programar.

## Importar paquetes

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

Estas importaciones traen todas las clases necesarias para cargar un PSD, modificar su trazo y guardar tanto los resultados PSD como PNG.

## Cómo guardar PSD como PNG con efecto de trazo

### Paso 1: Cargar el archivo PSD

Primero, indica la carpeta que contiene tu PSD de origen.

```java
String dataDir = "Your Document Directory";
```

Reemplaza `"Your Document Directory"` con la ruta real en tu máquina.

Ahora carga el archivo preservando cualquier recurso de efecto existente:

```java
String sourceFileName = dataDir + "StrokeComplex.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Paso 2: Establecer el color del trazo (y opcionalmente personalizar el ancho)

El bucle a continuación recorre cada capa, toma el primer `StrokeEffect` y cambia su color de relleno. También puedes ajustar `setWidth` o `setPosition` en el objeto `StrokeEffect` si necesitas **personalizar el ancho del trazo**.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    StrokeEffect effect = (StrokeEffect) im.getLayers()[i].getBlendingOptions().getEffects()[0];
    ColorFillSettings settings = (ColorFillSettings) effect.getFillSettings();
    // Set the stroke color – change to any Color you like
    settings.setColor(Color.getDeepPink());
}
```

> **Consejo profesional:** `Color.getDeepPink()` es solo un ejemplo. Usa `new Color(r, g, b)` para valores RGB personalizados.

### Paso 3: Guardar el PSD modificado (opcional)

Si deseas conservar una versión PSD con el trazo actualizado, guárdala así:

```java
String exportPath = dataDir + "StrokeComplexRendering.psd";
im.save(exportPath, new PsdOptions());
```

### Paso 4: Exportar la imagen como PNG (el paso central de “guardar PSD como PNG”)

Finalmente, convierte el PSD editado a un archivo PNG listo para la web:

```java
String exportPathPng = dataDir + "StrokeComplexRendering.png";
PngOptions option = new PngOptions();
option.setColorType(PngColorType.TruecolorWithAlpha);

im.save(exportPathPng, option);
```

El PNG conserva el trazo rosa intenso que configuraste antes, y la opción `TruecolorWithAlpha` asegura que la transparencia se mantenga.

## Problemas comunes y soluciones

| Problema | Razón | Solución |
|----------|-------|----------|
| **`ArrayIndexOutOfBoundsException`** | La capa no tiene efectos o el primer efecto no es un `StrokeEffect`. | Verifica que la capa realmente contenga un trazo o itera a través de `getEffects()` para encontrar el tipo correcto. |
| **El color no cambia** | Es posible que estés editando una copia de la configuración en lugar del original. | Asegúrate de hacer cast directamente a `ColorFillSettings` desde `effect.getFillSettings()`. |
| **El PNG aparece en blanco** | El PSD se cargó sin rasterizar la capa. | Llama a `im.save(..., new PngOptions())` después de todas las modificaciones; evita guardar el `im` original antes de los cambios. |

## Preguntas frecuentes

**P: ¿Puedo aplicar múltiples efectos a una sola capa usando Aspose.PSD para Java?**  
R: Sí, puedes acceder a las opciones de fusión de la capa y añadir tantos efectos como necesites, incluidos sombras, brillos y trazos.

**P: ¿Es posible automatizar el proceso para un lote de archivos PSD?**  
R: Absolutamente. Envuelve la lógica de carga, aplicación de efectos y guardado en un bucle `for‑each` que itere sobre los archivos en un directorio.

**P: ¿Cómo puedo revertir los cambios realizados en un archivo PSD?**  
R: Vuelve a cargar el archivo original antes de guardar cualquier modificación; Aspose.PSD no proporciona una pila de deshacer.

**P: ¿Puedo personalizar el ancho y la posición del trazo?**  
R: Sí. Usa `effect.setWidth(float)` y `effect.setPosition(StrokeEffect.Position)` para controlar el grosor y la ubicación (dentro, fuera o centrado).

**P: ¿La biblioteca Aspose.PSD para Java es gratuita?**  
R: Hay una prueba gratuita disponible para evaluación. La funcionalidad completa requiere una licencia comprada. Consulta las [opciones de compra](https://purchase.aspose.com/buy) para más detalles.

---

**Última actualización:** 2026-04-03  
**Probado con:** Aspose.PSD 24.12 para Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}