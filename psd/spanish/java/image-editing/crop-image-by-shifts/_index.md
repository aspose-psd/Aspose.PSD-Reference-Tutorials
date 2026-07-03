---
date: 2026-07-03
description: Aprenda cómo recortar una imagen Java usando Aspose.PSD para Java. Este
  tutorial paso a paso de recorte de imágenes cubre la carga de archivos PSD, la configuración
  de valores de desplazamiento y el guardado del resultado.
keywords:
- crop image java
- how to crop image
- load psd file
- java image processing
- crop image left right
linktitle: Recortar imagen por desplazamientos
schemas:
- author: Aspose
  dateModified: '2026-07-03'
  description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  headline: Crop Image Java by Shifts with Aspose.PSD
  type: TechArticle
- description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  name: Crop Image Java by Shifts with Aspose.PSD
  steps:
  - name: Load the Image
    text: '`Image` is the base class for all image types in Aspose.PSD. `RasterImage`
      represents a raster image and provides cropping capabilities.'
  - name: Cache Image Data
    text: '`cacheData()` loads the image data into memory for faster processing.'
  - name: Define Shift Values
    text: Specify the shift values for all four sides of the image (left, top, right,
      bottom) in pixels.
  - name: Apply Cropping
    text: '`crop(left, right, top, bottom)` trims the image by the specified pixel
      shifts on each side.'
  - name: Save the Results
    text: '`JpegOptions` defines JPEG encoding settings such as quality and color
      profile. Congratulations! You''ve successfully cropped an image using Aspose.PSD
      for Java.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports over 30 raster formats, including PSD, JPEG,
      PNG, BMP, TIFF, and GIF, ensuring broad compatibility.
    question: Is Aspose.PSD compatible with all image formats?
  - answer: Absolutely. After each `crop` call you receive a new image object, which
      you can crop again as needed.
    question: Can I apply multiple cropping operations to the same image?
  - answer: Yes, you can find support and engage with the community at [Aspose.PSD
      Forum](https://forum.aspose.com/c/psd/34).
    question: Is there a community forum for Aspose.PSD support?
  - answer: Visit [here](https://purchase.aspose.com/temporary-license/) to obtain
      a temporary license.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Explore the documentation and examples at [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).
    question: Are there sample projects showcasing Aspose.PSD functionalities?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Recortar imagen Java por desplazamientos con Aspose.PSD
url: /es/java/image-editing/crop-image-by-shifts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Recortar Imagen Java por Desplazamientos con Aspose.PSD

## Introducción

En el procesamiento de imágenes en Java, **crop image java** es un requisito común para preparar gráficos, miniaturas o recursos de UI. Aspose.PSD for Java hace que esta tarea sea sencilla al exponer un método `crop` simple que funciona con cualquier formato raster compatible. En este tutorial aprenderá cómo cargar un archivo PSD, definir los valores de desplazamiento izquierda‑derecha‑arriba‑abajo, aplicar el recorte y guardar el resultado, todo sin escribir código personalizado de manipulación de píxeles.

## Respuestas Rápidas
- **¿Qué biblioteca maneja el recorte?** Aspose.PSD for Java proporciona un método `crop` incorporado.  
- **¿Necesito una licencia?** Una licencia temporal funciona para evaluación; se requiere una licencia completa para producción.  
- **¿Formatos compatibles?** Más de 30 formatos raster, incluidos PSD, JPEG, PNG, BMP y TIFF.  
- **¿Tamaño máximo de archivo?** Maneja archivos de hasta 2 GB sin cargar la imagen completa en memoria.  
- **¿Cuántas líneas de código?** Solo cinco pasos lógicos: cargar, almacenar en caché, definir desplazamientos, recortar y guardar.

## ¿Qué es crop image java?
`crop image java` se refiere a la operación de recortar un mapa de bits en una aplicación Java. Usando Aspose.PSD, la operación se realiza mediante el método `crop`, que acepta valores de desplazamiento para cada lado de la imagen y devuelve una nueva instancia de imagen.

## ¿Por qué usar Aspose.PSD para recortar imágenes?
Aspose.PSD soporta **30+** formatos de imagen y puede procesar archivos PSD de cientos de páginas mientras usa menos de 150 MB de RAM, gracias a su arquitectura de carga diferida. La biblioteca también garantiza resultados píxel‑perfectos, preservando capas, máscaras y perfiles de color, algo que muchas bibliotecas de imágenes genéricas no pueden asegurar.

## Requisitos Previos

### Java Development Kit (JDK)

Asegúrese de tener la última versión del JDK instalada en su sistema. Puede descargarla desde [aquí](https://www.oracle.com/java/technologies/javase-downloads.html).

### Aspose.PSD for Java Library

Para comenzar, necesitará obtener la biblioteca Aspose.PSD for Java. Diríjase a la [página de descarga](https://releases.aspose.com/psd/java/) y obtenga la última versión.

### Integrated Development Environment (IDE)

Elija su IDE Java favorito, como Eclipse o IntelliJ, para una experiencia de codificación fluida.

## ¿Cómo recortar imagen java?

Cargue su archivo fuente, defina los desplazamientos de píxeles para cada lado y llame al método `crop`; todo este flujo de trabajo se puede escribir en cinco líneas concisas de código. La operación `crop` crea una nueva imagen que contiene solo la región especificada, dejando el archivo original intacto.

### Paso 1: Cargar la Imagen

`Image` es la clase base para todos los tipos de imagen en Aspose.PSD.  
`RasterImage` representa una imagen raster y proporciona capacidades de recorte.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

### Paso 2: Almacenar en caché los datos de la imagen

`cacheData()` carga los datos de la imagen en memoria para un procesamiento más rápido.  
```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
```

### Paso 3: Definir valores de desplazamiento

Especifique los valores de desplazamiento para los cuatro lados de la imagen (izquierda, arriba, derecha, abajo) en píxeles.  
```java
if (!rasterImage.isCached()) {
  rasterImage.cacheData();
}
```

### Paso 4: Aplicar recorte

`crop(left, right, top, bottom)` recorta la imagen según los desplazamientos de píxeles especificados en cada lado.  
```java
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

### Paso 5: Guardar los resultados

`JpegOptions` define la configuración de codificación JPEG, como calidad y perfil de color.  
```java
rasterImage.crop(leftShift, rightShift, topShift, bottomShift);
```

¡Felicidades! Ha recortado una imagen con éxito usando Aspose.PSD for Java.

## Problemas Comunes y Soluciones

- **La imagen parece sin cambios:** Verifique que los valores de desplazamiento sean positivos y no excedan las dimensiones originales.  
- **OutOfMemoryError en archivos grandes:** Habilite el almacenamiento en caché como se muestra en el Paso 2; esto obliga a Aspose.PSD a usar un archivo temporal en lugar de mantener toda la imagen en RAM.  
- **Desplazamiento de color después del recorte:** Asegúrese de preservar el perfil de color llamando a `image.save(..., new JpegOptions { ColorProfile = image.ColorProfile })` si necesita una fidelidad de color exacta.

## Preguntas Frecuentes

**Q: ¿Es Aspose.PSD compatible con todos los formatos de imagen?**  
A: Sí, Aspose.PSD soporta más de 30 formatos raster, incluidos PSD, JPEG, PNG, BMP, TIFF y GIF, garantizando una amplia compatibilidad.

**Q: ¿Puedo aplicar múltiples operaciones de recorte a la misma imagen?**  
A: Absolutamente. Después de cada llamada a `crop` recibe un nuevo objeto de imagen, que puede recortar nuevamente según sea necesario.

**Q: ¿Existe un foro comunitario para soporte de Aspose.PSD?**  
A: Sí, puede encontrar soporte y participar con la comunidad en [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**Q: ¿Cómo puedo obtener una licencia temporal para Aspose.PSD?**  
A: Visite [aquí](https://purchase.aspose.com/temporary-license/) para obtener una licencia temporal.

**Q: ¿Hay proyectos de ejemplo que muestren funcionalidades de Aspose.PSD?**  
A: Explore la documentación y ejemplos en [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).

---

**Última actualización:** 2026-07-03  
**Probado con:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
String destName = dataDir + "CroppingByShifts_out.jpg";
rasterImage.save(destName, new JpegOptions());
```

## Tutoriales Relacionados

- [Recortar Imagen por Rectángulo en Aspose.PSD para Java](/psd/java/image-editing/crop-image-by-rectangle/)
- [Recortar Imagen Java - Expandir y Recortar Imágenes con Aspose.PSD para Java](/psd/java/image-editing/expand-and-crop-images/)
- [Redimensionar Imagen Java - Usando la Enumeración Resize Type en Aspose.PSD para Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}