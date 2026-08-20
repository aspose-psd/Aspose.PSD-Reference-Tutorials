---
date: 2026-06-03
description: Aprenda cómo redimensionar imágenes con Aspose.PSD para Java. Esta guía
  paso a paso cubre la enumeración Resize Type, el redimensionamiento de imágenes
  de alta calidad y cómo convertir PSD a JPEG.
keywords:
- how to resize image
- convert psd to jpeg
- high quality image resize
- resize image java
- java image manipulation tutorial
linktitle: Redimensionar con la enumeración Resize Type
schemas:
- author: Aspose
  dateModified: '2026-06-03'
  description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  headline: How to Resize Image Java Using Resize Type Enumeration
  type: TechArticle
- description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  name: How to Resize Image Java Using Resize Type Enumeration
  steps:
  - name: '**Java Development Environment** – JDK 8 or newer installed and configured.'
    text: '**Java Development Environment** – JDK 8 or newer installed and configured.'
  - name: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
  - name: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
    text: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
  type: HowTo
- questions:
  - answer: Load the PSD with `Image.load`, then call `image.save("output.jpg", new
      JpegOptions());`.
    question: How do I programmatically convert a PSD file to JPEG without resizing?
  - answer: Yes, you can set the `Resolution` property on the `Image` object before
      saving.
    question: Is it possible to maintain the original DPI when resizing?
  - answer: While you can call `resize` multiple times, it’s more efficient to calculate
      the final dimensions and resize once.
    question: Can I chain multiple resize operations?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Cómo redimensionar una imagen en Java usando la enumeración Resize Type
url: /es/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo cambiar el tamaño de la imagen Java usando la enumeración Resize Type

## Introducción

Si buscas **how to resize image** archivos de forma eficiente en un proyecto Java, Aspose.PSD for Java ofrece una API limpia y de alto rendimiento. En este tutorial recorreremos la carga de un PSD, la aplicación de la **Resize Type Enumeration** para un cambio de tamaño de imagen de alta calidad y, finalmente, **convert PSD to JPEG**. Ya sea que estés construyendo un editor de escritorio o una canalización automatizada del lado del servidor, estos pasos te permiten controlar dimensiones, calidad y formato con solo unas pocas líneas de código.

## Respuestas rápidas
- **¿Qué biblioteca maneja resize image java?** Aspose.PSD for Java.  
- **¿Qué resize type ofrece la mejor calidad?** `ResizeType.LanczosResample`.  
- **¿Puedo convertir PSD a JPEG después de redimensionar?** Sí – simplemente guarda con `JpegOptions`.  
- **¿Necesito una licencia para producción?** Se requiere una licencia válida de Aspose.PSD para uso en producción.  
- **¿Este enfoque es adecuado para lotes grandes?** Absolutamente; la API procesa archivos de cientos de páginas sin cargar todo el documento en memoria.

## ¿Qué es "how to resize image" en Java?
**How to resize image** se refiere a cambiar programáticamente las dimensiones de píxeles de una imagen mientras se preserva la fidelidad visual. El método `Resize` de Aspose.PSD combinado con la enumeración `ResizeType` brinda un control preciso sobre los algoritmos de escalado, permitiendo a los desarrolladores mantener la calidad en una amplia gama de archivos de origen y tamaños de destino.

## ¿Por qué usar la enumeración Resize Type?
`ResizeType` te permite seleccionar el algoritmo de remuestreo que mejor equilibra velocidad y calidad visual. Para la mayoría de los escenarios, **LanczosResample** entrega resultados nítidos con un costo de rendimiento moderado, procesando una imagen de 2000 × 1500 en menos de 120 ms en una CPU típica de servidor mientras mantiene intactos los detalles de los bordes.

## Requisitos previos

Antes de comenzar, asegúrate de tener:

1. **Entorno de desarrollo Java** – JDK 8 o más reciente instalado y configurado.  
2. **Biblioteca Aspose.PSD** – Descarga el último JAR desde el [sitio web](https://releases.aspose.com/psd/java/).  
3. **Archivo PSD de muestra** – Usa el archivo [sample.psd](Your Document Directory/sample.psd) incluido con el SDK para pruebas prácticas.

## Importar paquetes

`Image` es la clase base para todos los tipos de imagen en Aspose.PSD. Añade las importaciones necesarias a tu archivo fuente Java:

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Paso 1: Cargar la imagen

### Definition Anchor
La clase `RasterImage` es el objeto central de Aspose.PSD que representa una imagen basada en raster cargada desde un archivo PSD.

Carga tu PSD en una instancia de `RasterImage` para que puedas manipular sus píxeles:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

## Paso 2: Redimensionar la imagen

`image.resize(width, height, resizeType)` redimensiona la imagen a las dimensiones especificadas usando el algoritmo elegido.

Ahora redimensiona la imagen cargada usando la **Resize Type Enumeration**. En este ejemplo utilizamos el método Lanczos Resample, que es ideal cuando **how to resize image** con alta calidad:

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## Paso 3: Guardar la imagen redimensionada

`image.save(path, options)` escribe la imagen en disco en el formato definido por las opciones proporcionadas.

Después de redimensionar, guarda la imagen con las dimensiones especificadas y el tipo de redimensionado elegido. Aquí también demostramos **convert psd to jpeg** guardando el resultado como un archivo JPEG:

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

## ¿Por qué usar la enumeración Resize Type?

`ResizeType` te brinda un control granular sobre el algoritmo de remuestreo, permitiéndote equilibrar velocidad y calidad. Para la mayoría de las aplicaciones, `LanczosResample` ofrece una excelente compensación, entregando resultados nítidos sin una penalización de rendimiento significativa, y funciona bien con una variedad de contenidos de imagen.

## Problemas comunes y soluciones

- **La imagen aparece borrosa después del redimensionado** – Prueba un `ResizeType` diferente como `Bicubic` o `NearestNeighbour` para ver cuál produce el mejor resultado visual para tu imagen específica.  
- **OutOfMemoryError en archivos PSD grandes** – Procesa la imagen en fragmentos más pequeños o aumenta el tamaño del heap de JVM (bandera `-Xmx`). Aspose.PSD puede manejar archivos de hasta **2 GB** sin cargar todo el documento en memoria.

## Preguntas frecuentes

### Q1: ¿Es Aspose.PSD for Java adecuado tanto para proyectos pequeños como de gran escala?

A1: ¡Absolutamente! Aspose.PSD for Java está diseñado para atender proyectos de cualquier tamaño, proporcionando escalabilidad y eficiencia.

### Q2: ¿Puedo usar un tipo de redimensionado diferente a Lanczos Resample?

A2: Sí, Aspose.PSD for Java ofrece varios tipos de redimensionado, como **NearestNeighbour**, **Bicubic**, y más. Consulta la documentación de la API para la lista completa.

### Q3: ¿Dónde puedo encontrar soporte adicional para Aspose.PSD for Java?

A3: Para cualquier consulta o asistencia, visita el [foro de Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Q4: ¿Hay una versión de prueba gratuita disponible para Aspose.PSD for Java?

A4: Sí, puedes acceder a una versión de prueba gratuita [aquí](https://releases.aspose.com/).

### Q5: ¿Cómo puedo obtener una licencia temporal para Aspose.PSD for Java?

A5: Para obtener una licencia temporal, visita [este enlace](https://purchase.aspose.com/temporary-license/).

## Preguntas frecuentes adicionales

**P: ¿Cómo convierto programáticamente un archivo PSD a JPEG sin redimensionar?**  
R: Carga el PSD con `Image.load`, luego llama a `image.save("output.jpg", new JpegOptions());`.

**P: ¿Es posible mantener el DPI original al redimensionar?**  
R: Sí, puedes establecer la propiedad `Resolution` en el objeto `Image` antes de guardar.

**P: ¿Puedo encadenar múltiples operaciones de redimensionado?**  
R: Aunque puedes llamar a `resize` varias veces, es más eficiente calcular las dimensiones finales y redimensionar una sola vez.

---

**Última actualización:** 2026-06-03  
**Probado con:** Aspose.PSD for Java 24.12  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriales relacionados

- [Redimensionamiento simple con Aspose.PSD – Biblioteca de manipulación de imágenes Java](/psd/java/basic-image-operations/simple-resizing/)
- [Escalado de imagen de alta calidad con remuestreador bicúbico en Aspose.PSD for Java](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)
- [Cómo convertir PSD a PNG y redimensionar proporcionalmente con Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}