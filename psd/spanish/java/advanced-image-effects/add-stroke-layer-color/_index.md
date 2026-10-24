---
date: 2026-10-24
description: Aprenda cómo crear stroke layer Java con Aspose.PSD para Java. Esta guía
  paso a paso le muestra cómo agregar un stroke layer, cambiar su color, ajustar la
  opacidad y guardar el PSD.
keywords:
- create stroke layer java
- change stroke color java
- modify stroke opacity
- apply stroke effect
- psd stroke tutorial
lastmod: 2026-10-24
linktitle: Agregar color de Stroke Layer
og_description: Crear stroke layer java usando Aspose.PSD para Java. Siga este tutorial
  conciso para agregar un stroke layer, cambiar su color, ajustar la opacidad y exportar
  el archivo PSD.
og_image_alt: Screenshot of a Java IDE showing Aspose.PSD code that creates and modifies
  a stroke layer in a PSD file
og_title: Crear stroke layer java con Aspose.PSD – Guía rápida
schemas:
- author: Aspose
  dateModified: '2026-10-24'
  description: Learn how to create stroke layer Java with Aspose.PSD for Java. This
    step‑by‑step guide shows you how to add a stroke layer, change its color, adjust
    opacity, and save the PSD.
  headline: How to create stroke layer Java using Aspose.PSD
  type: TechArticle
- description: Learn how to create stroke layer Java with Aspose.PSD for Java. This
    step‑by‑step guide shows you how to add a stroke layer, change its color, adjust
    opacity, and save the PSD.
  name: How to create stroke layer Java using Aspose.PSD
  steps:
  - name: set up your project
    text: Create a new Java project, add the Aspose.PSD JAR to the build path, and
      verify the library loads without errors.
  - name: load the PSD file
    text: Enable loading of effect resources so the stroke information is available.
  - name: access the stroke effect layer
    text: '`StrokeEffect` is Aspose.PSD’s class that represents a vector outline applied
      to a layer. Retrieve the first stroke effect from the second layer (index 1).'
  - name: validate stroke properties
    text: '`ColorFillSettings` holds the color and opacity values for a stroke. Confirm
      the existing properties before making changes to avoid unexpected results.'
  - name: set color and opacity (how to change stroke color)
    text: Here we **change stroke color** to yellow and reduce opacity to 50 % (127
      / 255). `ColorFillSettings` also lets you specify blend mode and size.
  - name: save the modified PSD
    text: Write the updated image back to disk. The new file now contains the modified
      stroke.
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD can be combined with libraries such as Apache Commons
      Imaging or Java2D for extended functionality.
    question: Can I use Aspose.PSD with other Java graphic libraries?
  - answer: Absolutely. The library supports the newest Photoshop specifications and
      over 150 PSD features.
    question: Is Aspose.PSD compatible with the latest PSD file format?
  - answer: Wrap your code in try‑catch blocks and consult the [support forum](https://forum.aspose.com/c/psd/34)
      for detailed troubleshooting examples.
    question: How do I handle exceptions while using Aspose.PSD?
  - answer: Certainly! Grab a [free trial](https://releases.aspose.com/) to explore
      all features.
    question: Can I try Aspose.PSD before purchasing?
  - answer: Obtain a [temporary license](https://purchase.aspose.com/temporary-license/)
      to evaluate the library in your development environment.
    question: Where can I get a temporary license for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- create stroke layer
- Aspose.PSD
- Java image processing
title: Cómo crear stroke layer Java usando Aspose.PSD
url: /es/java/advanced-image-effects/add-stroke-layer-color/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo crear capa de trazo Java usando Aspose.PSD

## Introducción

Si necesitas **crear capa de trazo Java** en un documento Photoshop de forma programática, Aspose.PSD para Java te ofrece un enfoque limpio, basado en código. En este tutorial aprenderás a añadir una nueva capa de trazo, cambiar su color, ajustar la opacidad y guardar el resultado, todo sin lanzar Photoshop. Al final también sabrás cómo editar el trazo de una capa existente, dándote control creativo completo directamente desde tu aplicación Java.

## Respuestas rápidas
- **¿Qué biblioteca se requiere?** Aspose.PSD para Java (última versión).  
- **¿Puedo cambiar el color del trazo?** Sí – usa `ColorFillSettings` para establecer cualquier `Color`.  
- **¿Necesito una licencia?** Una licencia temporal funciona para evaluación; se requiere una licencia completa para producción.  
- **¿Qué versión de Java es compatible?** Java 8 o superior.  
- **¿Cuánto tiempo lleva la implementación?** Normalmente menos de 10 minutos para un cambio básico de trazo.

## ¿Qué es una capa de trazo en un PSD?
Una capa de trazo es un efecto vectorial que dibuja un contorno alrededor del contenido de una capa. Puede personalizarse con color, grosor, opacidad y modo de fusión. Modificar este efecto programáticamente permite automatizar la marca, el procesamiento por lotes o la generación dinámica de gráficos.

## ¿Por qué usar Aspose.PSD para cambiar el color del trazo?
Aspose.PSD soporta **más de 150** características de PSD—including máscaras vectoriales, objetos inteligentes y efectos de capa—mientras procesa archivos de cientos de páginas sin cargar todo el documento en memoria. La biblioteca se ejecuta en cualquier SO con una JVM, ofrece rendimiento de subsegundo para activos típicos y no requiere instalación de Photoshop.

## ¿Cómo crear capa de trazo Java?

Carga el PSD, añade un efecto de trazo, configura su apariencia y guarda el archivo, todo en unas pocas líneas sencillas. La respuesta a continuación te indica exactamente qué hacer antes de sumergirnos en la guía paso a paso.

**Respuesta directa (40‑70 palabras):**  
`PsdImage` representa un documento PSD y proporciona métodos para cargar y guardar archivos. Comienza cargando tu PSD con `PsdImage.load("input.psd", loadOptions)`. Crea un nuevo `StrokeEffect`, establece su `ColorFillSettings` al `Color` deseado, ajusta la opacidad y el tamaño, luego adjunta el efecto a las `BlendingOptions` de la capa objetivo. Finalmente, llama a `psd.save("output.psd", SaveFormat.PSD)`. Esta secuencia crea una capa de trazo en Java con Aspose.PSD.

### Requisitos previos

- **Biblioteca Aspose.PSD** – descárgala desde la [documentación oficial](https://reference.aspose.com/psd/java/).  
- **Java Development Kit (JDK)** – versión 8 o más reciente.  
- **IDE** – Eclipse, IntelliJ IDEA o cualquier editor compatible con Java.

### Importar paquetes

Primero, importa las clases que necesitarás. Esto le da a tu proyecto acceso a la manipulación de PSD y a las API de efectos de trazo.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

### Paso 1: configurar tu proyecto

Crea un nuevo proyecto Java, añade el JAR de Aspose.PSD al path de compilación y verifica que la biblioteca se cargue sin errores.

### Paso 2: cargar el archivo PSD

Habilita la carga de recursos de efectos para que la información del trazo esté disponible.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

### Paso 3: acceder a la capa de efecto de trazo

`StrokeEffect` es la clase de Aspose.PSD que representa un contorno vectorial aplicado a una capa. Recupera el primer efecto de trazo de la segunda capa (índice 1).

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

### Paso 4: validar las propiedades del trazo

`ColorFillSettings` contiene los valores de color y opacidad para un trazo. Confirma las propiedades existentes antes de realizar cambios para evitar resultados inesperados.

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

### Paso 5: establecer color y opacidad (cómo cambiar el color del trazo)

Aquí **cambiamos el color del trazo** a amarillo y reducimos la opacidad al 50 % (127 / 255). `ColorFillSettings` también permite especificar el modo de fusión y el tamaño.

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

### Paso 6: guardar el PSD modificado

Escribe la imagen actualizada de nuevo en disco. El nuevo archivo ahora contiene el trazo modificado.

```java
im.save(exportPath);
```

## ¿Cómo cambiar el color del trazo Java?

`Color` representa un valor de color ARGB. Carga tu PSD, localiza la capa objetivo, actualiza `ColorFillSettings` con un nuevo `Color` y guarda el archivo. Esta operación requiere solo unas pocas líneas de código y se completa en menos de un segundo para activos típicos, lo que la hace rápida y eficiente.

**Respuesta directa (40‑70 palabras):**  
Usa `layer.getEffects().getStrokeEffect()` para obtener el trazo existente, llama a `stroke.getColorFillSettings().setColor(Color.getRed())` (o cualquier `Color` que necesites), opcionalmente ajusta `setOpacity((byte)200)` para una opacidad del 78 %, luego guarda el PSD con `psd.save("output.psd", SaveFormat.PSD)`. El cambio se aplica instantáneamente sin volver a renderizar todo el documento.

## ¿Cómo modificar la opacidad del trazo?

Si solo necesitas ajustar la opacidad manteniendo el color original, cambia el valor de `setOpacity` (0‑255) en `ColorFillSettings`. Por ejemplo, `colorStroke.setOpacity((byte)200);` hará que el trazo sea aproximadamente un 78 % opaco. Ajustar la opacidad te permite crear contornos sutiles o trazos totalmente sólidos, según los requisitos de tu diseño.

**Respuesta directa (40‑70 palabras):**  
Recupera el `StrokeEffect` de la capa deseada, luego llama a `stroke.getColorFillSettings().setOpacity((byte)valorDeseado)`, donde `valorDeseado` varía de 0 (transparente) a 255 (totalmente opaco). Guarda el PSD y la nueva opacidad se reflejará de inmediato. Este enfoque funciona para cualquier trazo existente, sin importar su color original.

## ¿Cómo aplicar el efecto de trazo?

Para añadir un nuevo efecto de trazo a una capa que aún no lo tiene, crea una instancia de `StrokeEffect`, configura su `ColorFillSettings` y adjúntala a las `BlendingOptions` de la capa. Los mismos métodos `setColor` y `setOpacity` se usan para definir la apariencia general.

**Respuesta directa (40‑70 palabras):**  
Instancia `StrokeEffect newStroke = new StrokeEffect(); newStroke.getColorFillSettings().setColor(Color.getBlue()); newStroke.getColorFillSettings().setOpacity((byte)255); layer.getBlendingOptions().setEffect(newStroke);`. Después de adjuntar el efecto, guarda el PSD. Esto agrega una nueva capa de trazo totalmente personalizable a cualquier capa existente en tu documento.

## Casos de uso comunes para cambiar el color del trazo
- **Automatización de marca:** Aplica un color corporativo a logotipos en cientos de activos PSD en una única ejecución por lotes.  
- **Generación dinámica de UI:** Cambia los colores de trazo al instante según los temas seleccionados por el usuario en una herramienta de diseño basada en web.  
- **Preparación previa a la impresión:** Asegura que todos los colores de trazo cumplan con las especificaciones de impresión antes de enviar los archivos a la prensa.

## Errores comunes y consejos

- **Comprobaciones de null** – siempre verifica que `getEffects()` devuelva un arreglo no nulo antes de hacer casting.  
- **Índice de capa** – las capas PSD son indexadas desde cero; asegúrate de apuntar a la capa correcta.  
- **Formato de color** – `Color.getYellow()` es solo un ejemplo; puedes crear colores personalizados con `new Color(r, g, b)`.  
- **Rango de opacidad** – la opacidad es un byte (0–255); los valores superiores a 255 se recortarán.  
- **Carga de recursos** – olvidar `loadOptions.setLoadEffectsResource(true)` resultará en un arreglo de efectos `null`.

## Preguntas frecuentes

**P: ¿Puedo usar Aspose.PSD con otras bibliotecas gráficas de Java?**  
R: Sí, Aspose.PSD puede combinarse con bibliotecas como Apache Commons Imaging o Java2D para funcionalidades ampliadas.

**P: ¿Aspose.PSD es compatible con el último formato de archivo PSD?**  
R: Absolutamente. La biblioteca soporta las especificaciones más recientes de Photoshop y más de 150 características de PSD.

**P: ¿Cómo manejo excepciones al usar Aspose.PSD?**  
R: Envuelve tu código en bloques try‑catch y consulta el [foro de soporte](https://forum.aspose.com/c/psd/34) para ejemplos detallados de solución de problemas.

**P: ¿Puedo probar Aspose.PSD antes de comprar?**  
R: ¡Claro! Obtén una [prueba gratuita](https://releases.aspose.com/) para explorar todas las funciones.

**P: ¿Dónde puedo obtener una licencia temporal para Aspose.PSD?**  
R: Obtén una [licencia temporal](https://purchase.aspose.com/temporary-license/) para evaluar la biblioteca en tu entorno de desarrollo.

---

**Última actualización:** 2026-10-24  
**Probado con:** Aspose.PSD 24.11 para Java  
**Autor:** Aspose

## Tutoriales relacionados

- [Cómo cambiar el color del trazo Java usando Aspose.PSD](/psd/java/advanced-image-effects/add-stroke-layer-color/)
- [Cómo añadir sombra en PSD usando Java – Efectos avanzados de capa](/psd/java/advanced-psd-layer-features-effects/)
- [Superposición de patrón PSD: Añadir efectos con Aspose.PSD para Java](/psd/java/advanced-image-effects/add-pattern-effects/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}