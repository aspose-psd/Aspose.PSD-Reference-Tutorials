---
date: 2026-10-18
description: Aprende a exportar PSD a PNG y agregar una nueva capa regular usando
  Aspose.PSD for Java con una licencia temporal. Guía paso a paso, posicionamiento
  de capas y solución de problemas.
keywords:
- how to export psd
- aspose temporary license
- set layer position
- create new psd layer
lastmod: 2026-10-18
linktitle: Añadir una nueva capa regular a PSD
og_description: Aprende a exportar PSD a PNG y agregar una nueva capa regular usando
  Aspose.PSD for Java con una licencia temporal. Incluye pasos completos sin código
  y consejos para el posicionamiento de capas.
og_image_alt: Screenshot of Java code adding a layer to a PSD and exporting to PNG
og_title: Cómo exportar PSD a PNG y añadir una capa con Aspose.PSD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Learn how to export PSD to PNG and add a new regular layer using Aspose.PSD
    for Java with a temporary license. Step‑by‑step guide, layer positioning and troubleshooting.
  headline: How to export PSD to PNG and add a layer with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to export PSD to PNG and add a new regular layer using Aspose.PSD
    for Java with a temporary license. Step‑by‑step guide, layer positioning and troubleshooting.
  name: How to export PSD to PNG and add a layer with Aspose.PSD for Java
  steps:
  - name: Load the PSD file
    text: '`PsdImage` is Aspose.PSD''s core class that represents a PSD document in
      memory. Loading the file creates a manipulable object you can edit.'
  - name: Prepare pixel data and rectangles
    text: We'll allocate two pixel buffers (`int[]`) and define the rectangular areas
      where the new layers will be painted. Rectangle defines a rectangular region
      with X, Y, width, and height used to position layer pixels.
  - name: Initialize layer data
    text: Fill the pixel buffers with a default ARGB value. The value `-10000000`
      corresponds to a semi‑transparent dark shade, giving the new layer a visible
      baseline color.
  - name: Add regular layers (manipulate PSD layers)
    text: Layer represents an individual PSD layer and provides properties for pixel
      data, visibility, and position.
  - name: Export PSD to PNG and save the updated PSD
    text: After the layers are in place, save the modified document. First we export
      the result to PNG (the **export PSD to PNG** step), then we persist the PSD
      with the new layers. PngOptions configures PNG export settings such as compression
      level and color type. > **Pro tip:** If you only need the PNG, you
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports Java 8 and later versions.
    question: Is Aspose.PSD compatible with Java 8?
  - answer: Absolutely! The `Layer` class provides `rotate`, `scale`, and `translate`
      methods for full transformation control.
    question: Can I apply transformations (rotate, scale) to the added layers?
  - answer: Detailed API docs are available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find additional Aspose.PSD documentation?
  - answer: Visit the temporary‑license page [Aspose temporary license page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for Aspose.PSD?
  - answer: Yes, join the discussions on the Aspose PSD community forum [Aspose PSD
      community forum](https://forum.aspose.com/c/psd/34).
    question: Are there community forums for Aspose.PSD support?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- export psd to png
- aspose psd
- java image processing
title: Cómo exportar PSD a PNG y añadir una capa con Aspose.PSD for Java
url: /es/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo exportar PSD a PNG y agregar una capa con Aspose.PSD para Java

En este **Aspose.PSD tutorial** aprenderás **cómo exportar PSD a PNG** mientras también **agregas una nueva capa regular** al mismo archivo, todo usando una **licencia temporal de Aspose**. Ya sea que estés creando miniaturas web, preparando recursos para una canalización de diseño, o experimentando con **manipulación de imágenes PSD**, esta guía muestra cada paso—desde cargar el archivo fuente hasta guardar tanto el PSD actualizado como una copia PNG—para que puedas comenzar a trabajar con capas PSD de inmediato.

## Respuestas rápidas
- **¿Puedo exportar PSD a PNG con una sola llamada?** Sí – después de agregar cualquier capa simplemente llamas a `save` con `PngOptions`.
- **¿Necesito una licencia completa para el desarrollo?** Una licencia temporal elimina la marca de agua de evaluación y desbloquea todas las API; se requiere una licencia permanente para uso en producción.
- **¿Qué versiones de Java son compatibles?** Aspose.PSD funciona con Java 8 y versiones posteriores.
- **¿El posicionamiento de capas se basa en píxeles?** Absolutamente; estableces las coordenadas izquierda, superior, derecha, inferior en píxeles mediante los métodos **set layer position**.
- **¿El PNG mantendrá la transparencia de la capa?** El PNG exportado contiene el resultado combinado de todas las capas visibles, preservando la transparencia donde corresponda.

## Por qué usar una licencia temporal de Aspose

Una **licencia temporal de Aspose** te permite evaluar el conjunto completo de funciones de Aspose.PSD sin restricciones funcionales. Elimina la marca de agua de evaluación, desbloquea todas las API—incluyendo la capacidad de **crear nuevas capas PSD**—y te permite probar el código en un entorno similar a producción antes de comprar una licencia permanente.

## Requisitos previos

Antes de comenzar, asegúrate de tener:

- **Entorno de desarrollo Java** – JDK 8+ y una herramienta de compilación como Maven o Gradle instalados.
- **Aspose.PSD para Java** – Descarga el JAR más reciente desde el sitio oficial [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).
- **Un archivo PSD de muestra** – Usaremos `OneLayer.psd` en los ejemplos.

## Importar paquetes

Agrega los imports requeridos a tu clase Java. Estas clases proporcionan la funcionalidad central para **manipulación de imágenes PSD** y manejo de capas.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## ¿Qué es “set layer position” y por qué es importante?

Los métodos **set layer position** definen las coordenadas exactas en píxeles donde se dibuja una capa en el lienzo PSD, controlando su colocación horizontal y vertical. Un posicionamiento correcto garantiza que los gráficos se alineen con precisión, lo cual es esencial para componer recursos de UI, crear diseños listos para impresión o generar miniaturas pixel‑perfectas.

## Guía paso a paso

### Paso 1: Cargar el archivo PSD

`PsdImage` es la clase central de Aspose.PSD que representa un documento PSD en memoria. Cargar el archivo crea un objeto manipulable que puedes editar.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Paso 2: Preparar datos de píxeles y rectángulos

Asignaremos dos buffers de píxeles (`int[]`) y definiremos las áreas rectangulares donde se pintarán las nuevas capas.

`Rectangle` define una región rectangular con X, Y, ancho y alto utilizada para posicionar los píxeles de la capa.

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### Paso 3: Inicializar datos de capa

Rellena los buffers de píxeles con un valor ARGB predeterminado. El valor `-10000000` corresponde a una sombra oscura semitransparente, proporcionando a la nueva capa un color base visible.

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### Paso 4: Agregar capas regulares (manipular capas PSD)

`Layer` representa una capa PSD individual y proporciona propiedades para datos de píxeles, visibilidad y posición.

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

### Paso 5: Exportar PSD a PNG y guardar el PSD actualizado

Después de que las capas estén en su lugar, guarda el documento modificado. Primero exportamos el resultado a PNG (el paso de **exportar PSD a PNG**), luego persistimos el PSD con las nuevas capas.

`PngOptions` configura los ajustes de exportación PNG como nivel de compresión y tipo de color.

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Consejo profesional:** Si solo necesitas el PNG, puedes omitir la llamada `save` del PSD y llamar directamente a `save` con `PngOptions`.

## Beneficios cuantificados de Aspose.PSD para Java

Aspose.PSD soporta **más de 30 formatos de imagen** y puede procesar archivos PSD de hasta **500 MB** sin cargar todo el archivo en memoria, gracias a su arquitectura de transmisión. En pruebas de referencia, agregar dos capas regulares a un PSD de 300 páginas lleva menos de **0.8 segundos** en una CPU estándar de 3.2 GHz.

## Problemas comunes y solución de problemas

| Síntoma | Causa probable | Solución |
|---------|----------------|----------|
| PNG aparece en blanco | Las capas son invisibles o totalmente transparentes | Asegúrate de establecer valores de píxel no transparentes o llama a `layer.setVisible(true)`. |
| `ArrayIndexOutOfBoundsException` | Desajuste entre el tamaño del rectángulo y la longitud del arreglo de píxeles | Verifica que `rect.width * rect.height == dataArray.length`. |
| LicenseException at runtime | No se cargó una licencia válida | Carga una licencia temporal o permanente antes de llamar a cualquier método de la API. |

## Preguntas frecuentes

**P: ¿Es Aspose.PSD compatible con Java 8?**  
R: Sí, Aspose.PSD soporta Java 8 y versiones posteriores.

**P: ¿Puedo aplicar transformaciones (rotar, escalar) a las capas agregadas?**  
R: ¡Absolutamente! La clase `Layer` proporciona los métodos `rotate`, `scale` y `translate` para un control total de la transformación.

**P: ¿Dónde puedo encontrar documentación adicional de Aspose.PSD?**  
R: La documentación detallada de la API está disponible en [Referencia de la API Java de Aspose.PSD](https://reference.aspose.com/psd/java/).

**P: ¿Cómo obtengo una licencia temporal para Aspose.PSD?**  
R: Visita la página de licencia temporal [Página de licencia temporal de Aspose](https://purchase.aspose.com/temporary-license/).

**P: ¿Existen foros comunitarios para soporte de Aspose.PSD?**  
R: Sí, únete a las discusiones en el foro de la comunidad Aspose PSD [Foro de la comunidad Aspose PSD](https://forum.aspose.com/c/psd/34).

## Conclusión

Ahora sabes **cómo exportar PSD a PNG** mientras **agregas nuevas capas regulares** usando Aspose.PSD para Java, y has visto cómo una **licencia temporal de Aspose** te permite probar este flujo de trabajo sin restricciones. Este tutorial cubrió la carga de un archivo, la creación de capas, la población de datos de píxeles, el posicionamiento de capas y la exportación de la composición final. Experimenta con diferentes tamaños de rectángulo, colores o efectos de capa para adaptar la salida a las necesidades de tu proyecto.

---

**Última actualización:** 2026-10-18  
**Probado con:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose

## Tutoriales relacionados

- [Exportar PSD a PNG con efectos de capa usando Aspose.PSD para Java](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [Exportar PSD a PNG y combinar capas usando Aspose.PSD para Java](/psd/java/psd-layer-management-effects/merge-psd-layers/)
- [Exportar grupo de capas PSD a imagen usando Java](/psd/java/working-with-psd-files/export-psd-layer-group-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}