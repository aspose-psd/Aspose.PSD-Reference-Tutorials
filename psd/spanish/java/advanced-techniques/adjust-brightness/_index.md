---
date: 2026-09-28
description: Tutorial de procesamiento de imágenes en Java que muestra cómo ajustar
  el brillo de una imagen usando Aspose.PSD para Java. Sigue el código paso a paso
  para cargar, modificar y guardar archivos PSD o TIFF.
keywords:
- java image processing
- aspose psd java
- java image manipulation
- adjust brightness java
lastmod: 2026-09-28
linktitle: Ajustar el brillo de una imagen
og_description: Tutorial de procesamiento de imágenes en Java que muestra cómo ajustar
  el brillo de una imagen usando Aspose.PSD para Java. Sigue el código paso a paso
  para cargar, modificar y guardar archivos PSD o TIFF.
og_image_alt: Guide to adjusting image brightness in Java using Aspose.PSD
og_title: 'Procesamiento de imágenes en Java: ajustar el brillo con Aspose.PSD'
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  headline: 'Java image processing: adjust brightness with Aspose.PSD'
  type: TechArticle
- description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  name: 'Java image processing: adjust brightness with Aspose.PSD'
  steps:
  - name: Load the image
    text: The `RasterImage` class represents a rasterized version of a PSD or TIFF
      file in memory. It provides direct pixel access for color‑correction operations.
      In this step, we load the target image and cast it to a `RasterImage` for further
      processing.
  - name: Adjust brightness
    text: '`adjustBrightness(int value)` changes the lightness of every pixel by the
      specified integer value. Positive numbers brighten the image; negative numbers
      darken it. The method processes the image in‑place, so no additional object
      creation is required. Here, we use the `adjustBrightness` method to mod'
  - name: Set TiffOptions
    text: '`TiffOptions` specifies the encoding parameters for TIFF output, such as
      bits per sample and photometric interpretation. It lets you control how the
      resulting file is encoded. Configure the `TiffOptions` for saving the adjusted
      image. Adjust the `bitsPerSample` and `photometric` properties based on '
  - name: Save the resultant image
    text: Calling `save` writes the processed raster data to a file using the previously
      defined options. The operation is atomic and guarantees that the output file
      is a valid TIFF image. Finally, save the modified image using the specified
      `TiffOptions`.
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD for Java supports JPEG, PNG, BMP, GIF, and many other
      raster formats in addition to PSD and TIFF.
    question: Can I adjust brightness in other image formats besides PSD?
  - answer: Wrap the processing code in a try‑catch block and catch `IOException`
      or `ImageProcessingException` to manage file‑access and raster‑operation errors.
    question: How can I handle errors during the image adjustment process?
  - answer: The method accepts integer values from –255 to +255; values outside this
      range are clamped to the nearest limit.
    question: Is there a limit to the range of brightness adjustment?
  - answer: Yes, a commercial license is required for production use. Purchase a license
      [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD for Java in commercial projects?
  - answer: Yes, you can explore the library with a free trial from [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose psd
- java image manipulation
title: 'Procesamiento de imágenes en Java: ajustar el brillo con Aspose.PSD'
url: /es/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ajustar el brillo de una imagen con Aspose.PSD para Java

## Introducción

En este tutorial de **java image processing** aprenderás cómo ajustar el brillo de una imagen directamente desde código Java. Ajustar el brillo es una tarea frecuente para diseñadores gráficos, fotógrafos y cualquiera que construya pipelines de procesamiento de imágenes. En esta guía de **java image manipulation** recorreremos el flujo de trabajo completo —cargar un PSD/TIFF, aplicar un desplazamiento de brillo y guardar el resultado— usando la biblioteca Aspose.PSD for Java.

## Respuestas rápidas
- **¿Qué biblioteca maneja el brillo?** Aspose.PSD for Java.  
- **¿Qué método cambia el brillo?** `RasterImage.adjustBrightness()`.  
- **¿Puedo trabajar con archivos PSD y TIFF?** Sí, la API soporta ambos formatos y más de 10 tipos de imagen adicionales.  
- **¿Necesito una licencia para producción?** Se requiere una licencia comercial para uso que no sea de evaluación.  
- **¿Cuánto tiempo lleva la implementación?** Normalmente menos de 10 minutos para un ajuste básico.

## ¿Qué es el procesamiento de imágenes en Java?
`Java image processing` se refiere al conjunto de técnicas que permiten leer, transformar y escribir datos de imagen programáticamente usando Java. Ajustar el brillo es una de las operaciones básicas que cambia la luminosidad general de cada píxel, haciendo que las áreas oscuras sean más claras o las áreas claras más oscuras.

## ¿Por qué usar Aspose.PSD para Java?
Aspose.PSD for Java ofrece una solución completa, puramente Java, que soporta una amplia gama de formatos raster y vectoriales, elimina dependencias nativas y ofrece caché de alto rendimiento para archivos grandes. Su extensa API permite a los desarrolladores realizar correcciones de color complejas y ediciones basadas en capas con código mínimo, lo que lo hace ideal tanto para ajustes simples como para pipelines avanzados de procesamiento de imágenes.

- **Soporta más de 10 formatos raster y vectoriales** – PSD, TIFF, JPEG, PNG, BMP, GIF, y más.  
- **Implementación Pure‑Java** – sin DLLs nativas ni dependencias externas, por lo que funciona en cualquier JVM.  
- **Caché de alto rendimiento** – los datos raster pueden almacenarse en caché, permitiendo hasta 2× más rapidez en ediciones repetidas de archivos grandes.  
- **Amplia superficie de API** – más de 150 métodos para corrección de color, manejo de capas, máscaras y composición.

## Requisitos previos

Antes de sumergirte en el tutorial, asegúrate de contar con los siguientes requisitos:

- Aspose.PSD for Java Library: Descarga e instala la biblioteca desde la [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).  
- Java Development Kit (JDK) 8 o superior instalado en tu máquina.  
- Un entorno de desarrollo (IDE) como IntelliJ IDEA, Eclipse o VS Code.

## Importar paquetes

Para comenzar, importa los paquetes necesarios en tu proyecto Java. En este ejemplo, usaremos lo siguiente:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Ahora, desglosaremos el proceso de ajustar el brillo de una imagen en pasos simples:

## ¿Cómo ajustar el brillo usando Aspose.PSD?

Carga tu imagen fuente, aplica un desplazamiento de brillo, configura las opciones de guardado y escribe el resultado en disco —todo en cuatro pasos concisos. Las secciones siguientes proporcionan una guía clara paso a paso que puedes copiar en tu propio proyecto. Este enfoque garantiza que cada operación se realice de manera eficiente y que la imagen final conserve la calidad original mientras refleja el cambio de brillo deseado.

### Paso 1: Cargar la imagen

La clase `RasterImage` representa una versión rasterizada de un archivo PSD o TIFF en memoria. Proporciona acceso directo a los píxeles para operaciones de corrección de color.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage) image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

En este paso, cargamos la imagen objetivo y la convertimos a un `RasterImage` para su posterior procesamiento.

### Paso 2: Ajustar el brillo

`adjustBrightness(int value)` cambia la luminosidad de cada píxel según el valor entero especificado. Los números positivos aclaran la imagen; los negativos la oscurecen. El método procesa la imagen in‑place, por lo que no se requiere crear objetos adicionales.

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

Aquí usamos el método `adjustBrightness` para modificar el brillo de la imagen. En este ejemplo, disminuimos el brillo en 50 unidades, pero puedes personalizar este valor según tus requisitos.

### Paso 3: Configurar TiffOptions

`TiffOptions` especifica los parámetros de codificación para la salida TIFF, como bits por muestra e interpretación fotométrica. Te permite controlar cómo se codifica el archivo resultante.

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

Configura los `TiffOptions` para guardar la imagen ajustada. Ajusta las propiedades `bitsPerSample` y `photometric` según tus necesidades específicas.

### Paso 4: Guardar la imagen resultante

Llamar a `save` escribe los datos raster procesados en un archivo usando las opciones definidas previamente. La operación es atómica y garantiza que el archivo de salida sea una imagen TIFF válida.

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

Finalmente, guarda la imagen modificada usando los `TiffOptions` especificados.

## Problemas comunes y soluciones

| Problema | Razón | Solución |
|----------|-------|----------|
| **`ClassCastException` when casting Image** | El archivo no es una imagen raster (p.ej., un PSD vectorial). | Verifica el formato del archivo fuente o usa `image instanceof RasterImage` antes de hacer cast. |
| **Brightness change has no effect** | La imagen no se almacenó en caché antes del ajuste. | Llama a `rasterImage.cacheData()` como se muestra en el Paso 1. |
| **Saved file appears corrupted** | Configuración incorrecta de `TiffOptions`. | Asegúrate de que `bitsPerSample` coincida con la profundidad de la imagen fuente (usualmente 8 bits por canal). |

## Preguntas frecuentes

**Q:** ¿Puedo ajustar el brillo en otros formatos de imagen además de PSD?  
**A:** Sí, Aspose.PSD for Java soporta JPEG, PNG, BMP, GIF y muchos otros formatos raster además de PSD y TIFF.

**Q:** ¿Cómo puedo manejar errores durante el proceso de ajuste de la imagen?  
**A:** Envuelve el código de procesamiento en un bloque try‑catch y captura `IOException` o `ImageProcessingException` para gestionar errores de acceso a archivos y operaciones raster.

**Q:** ¿Hay un límite en el rango de ajuste de brillo?  
**A:** El método acepta valores enteros de –255 a +255; los valores fuera de este rango se limitan al límite más cercano.

**Q:** ¿Puedo usar Aspose.PSD for Java en proyectos comerciales?  
**A:** Sí, se requiere una licencia comercial para uso en producción. Compra una licencia [here](https://purchase.aspose.com/buy).

**Q:** ¿Hay una prueba gratuita disponible?  
**A:** Sí, puedes explorar la biblioteca con una prueba gratuita desde [here](https://releases.aspose.com/).

**Q:** ¿El método `adjustBrightness` afecta la visibilidad de capas?  
**A:** El método trabaja sobre la imagen compuesta rasterizada, por lo que las capas ocultas se ignoran durante la rasterización, preservando el resultado visual previsto.

**Q:** ¿Puedo encadenar múltiples ajustes (p.ej., contraste, saturación) juntos?  
**A:** Absolutamente. Después de ajustar el brillo, puedes llamar a `adjustContrast`, `adjustSaturation` u otros métodos de corrección de color en la misma instancia de `RasterImage`.

**Última actualización:** 2026-09-28  
**Probado con:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Autor:** Aspose

## Tutoriales relacionados

- [Biblioteca de procesamiento de imágenes Java: Invertir capa usando Aspose.PSD](/psd/java/advanced-image-manipulation/invert-adjustment-layer/)
- [Convertir imagen a escala de grises usando Aspose.PSD para Java](/psd/java/advanced-techniques/grayscale-image/)
- [Cómo rotar una imagen en un ángulo específico con Aspose.PSD para Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}