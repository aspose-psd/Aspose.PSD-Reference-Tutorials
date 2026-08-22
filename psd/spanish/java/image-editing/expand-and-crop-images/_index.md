---
date: 2026-07-08
description: 'Tutorial de la biblioteca de edición de imágenes Java: aprenda cómo
  recortar una imagen en Java usando Aspose.PSD para Java, redimensionar, expandir
  el lienzo y convertir PSD a JPEG.'
keywords:
- java image editing library
- java image processing tutorial
- how to crop image java
lastmod: 2026-07-08
linktitle: Expandir y recortar imágenes
og_description: El tutorial de la biblioteca de edición de imágenes Java muestra cómo
  recortar, expandir el lienzo y convertir PSD a JPEG usando Aspose.PSD para Java
  en minutos.
og_image_alt: 'Guide: Crop and expand images in Java with Aspose.PSD'
og_title: Biblioteca de edición de imágenes Java – Recortar imagen con Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-07-08'
  description: 'Java image editing library tutorial: learn how to crop image java
    using Aspose.PSD for Java, resize, expand canvas, and convert PSD to JPEG.'
  headline: Java Image Editing Library – Crop Image with Aspose.PSD
  type: TechArticle
- questions:
  - answer: Aspose.PSD for Java.
    question: What library handles crop image java?
  - answer: A free trial works for testing; a commercial license is required for production.
    question: Do I need a license for development?
  - answer: Yes, using `JpegOptions` together with a cropping rectangle.
    question: Can I convert PSD to JPEG while cropping?
  - answer: Aspose.PSD supports Java 8 and newer versions.
    question: Is Java 8 supported?
  - answer: Typically under 10 minutes for a basic crop operation.
    question: How long does the implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image editing
- Aspose.PSD
- image cropping
- PSD to JPEG
title: Biblioteca de edición de imágenes Java – Recortar imagen con Aspose.PSD
url: /es/java/image-editing/expand-and-crop-images/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Biblioteca de edición de imágenes Java: Recortar imagen Java con Aspose.PSD

## Introducción

En este tutorial aprenderá a usar una **biblioteca de edición de imágenes Java** —específicamente Aspose.PSD para Java— para recortar, expandir y convertir archivos PSD a JPEG. Ya sea que esté preparando recursos para un portal web o automatizando la generación de miniaturas, los pasos a continuación le ofrecen un flujo de trabajo repetible y listo para producción que puede integrar en cualquier proyecto Java 8+.

## Respuestas rápidas
- **¿Qué biblioteca maneja recortar imagen java?** Aspose.PSD for Java.  
- **¿Necesito una licencia para desarrollo?** Una prueba gratuita funciona para pruebas; se requiere una licencia comercial para producción.  
- **¿Puedo convertir PSD a JPEG mientras recorto?** Sí, usando `JpegOptions` junto con un rectángulo de recorte.  
- **¿Se admite Java 8?** Aspose.PSD admite Java 8 y versiones posteriores.  
- **¿Cuánto tiempo lleva la implementación?** Normalmente menos de 10 minutos para una operación básica de recorte.

## ¿Qué es “recortar imagen java”?

Recortar imagen java significa seleccionar una región rectangular de la imagen fuente y descartar todo lo que está fuera de esa región. Con Aspose.PSD, crea un `Rectangle` que define el área, lo aplica a un `RasterImage` y luego guarda el resultado en cualquier formato compatible, como JPEG.

## ¿Por qué usar Aspose.PSD para recorte de imágenes Java?

Aspose.PSD proporciona una **biblioteca de edición de imágenes Java** que maneja archivos PSD de forma nativa, soporta más de 100 características de capas y puede procesar imágenes de hasta 10 000 × 10 000 píxeles manteniendo el uso de memoria por debajo de 500 MB. También ofrece conversión incorporada a JPEG, PNG, BMP y más, todo sin necesidad de herramientas externas. Esto hace que los pipelines de procesamiento masivo sean rápidos, fiables y fáciles de mantener.

## Requisitos previos

1. **Java Development Kit (JDK)** – Java 8 o posterior instalado.  
2. **Aspose.PSD for Java** – descargue la biblioteca del sitio oficial **[aquí](https://releases.aspose.com/psd/java/)**.  

> **Consejo profesional:** Añada el JAR de Aspose.PSD al classpath de su proyecto o a las dependencias de Maven/Gradle para evitar `ClassNotFoundException`.

## Importar paquetes

Añada las importaciones necesarias a su archivo fuente Java. Estas clases le dan acceso a la carga de imágenes, manipulación raster, definición de rectángulos y opciones de exportación JPEG.

## ¿Cómo recortar imagen Java usando Aspose.PSD?

Cargue el PSD fuente con `RasterImage`, defina un `Rectangle` que describa el área de recorte (las coordenadas negativas pueden expandir el lienzo) y finalmente guarde el resultado con `JpegOptions`. Este flujo de tres pasos maneja tanto el recorte como la conversión de formato en una sola pasada, eliminando la necesidad de archivos intermedios.

## Paso 1: Establezca el directorio de su documento

Especifique la carpeta que contiene el archivo PSD fuente. Reemplace el marcador de posición con la ruta real en su máquina.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Paso 2: Especifique las rutas de origen y destino

Defina de dónde leer el PSD y dónde escribir el JPEG recortado.

```java
String dataDir = "Your Document Directory";
```

## Paso 3: Cargar y almacenar en caché la imagen

`RasterImage` representa una versión rasterizada de un archivo PSD en memoria.  
Cargue el PSD en un objeto `RasterImage`. El almacenamiento en caché mejora el rendimiento para operaciones posteriores como el recorte.

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## Paso 4: Crear un rectángulo para recortar

`Rectangle` define las coordenadas X, Y y el ancho/alto de la región de recorte.  
Cree un `Rectangle` que describa la región que desea conservar. Las coordenadas pueden ser negativas para **expandir** el lienzo antes del recorte, lo cual es útil para añadir un borde alrededor de la imagen original.

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

> **¿Por qué usar coordenadas negativas?**  
> Los valores negativos de X/Y desplazan el área de recorte hacia la izquierda/arriba, añadiendo efectivamente espacio vacío (expansión) alrededor del contenido original antes del recorte final.

## Paso 5: Guardar la imagen recortada

`JpegOptions` especifica la configuración para la salida JPEG, como calidad y compresión.  
Finalmente, guarde la imagen resultante usando `JpegOptions`. Este paso también muestra **convertir psd a jpeg** mientras se aplica el rectángulo de recorte.

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

> **Resultado:** `jpeg_out.jpg` ahora contiene una imagen de 300 × 300 píxeles que ha sido expandida 200 px en cada lado y luego recortada al rectángulo definido.

¡Felicidades! Ha realizado con éxito **recorte de imágenes Java**, expandido el lienzo y convertido un archivo PSD a JPEG, todo en unas pocas líneas concisas de código.

## Casos de uso comunes

- **Preparar recursos para la web** – recorte y redimensione capturas de pantalla o diseños antes de subirlos.  
- **Generar miniaturas** – extraiga una región específica de un PSD grande para propósitos de vista previa.  
- **Procesamiento por lotes automatizado** – recorra una carpeta de archivos PSD, aplicando el mismo rectángulo de recorte a cada uno.

## Solución de problemas y consejos

| Problema | Solución sugerida |
|----------|-------------------|
| `OutOfMemoryError` al cargar PSDs grandes | Llamar a `rasterImage.cacheData()` temprano y considerar aumentar el tamaño del heap de JVM (`-Xmx`). |
| El área recortada está descentrada | Verifique los desplazamientos X/Y del rectángulo; recuerde que los valores negativos expanden el lienzo. |
| El JPEG de salida se ve borroso | Ajuste la configuración de calidad de `JpegOptions` (p. ej., `new JpegOptions { Quality = 90 }`). |

## Preguntas frecuentes

### Q1: ¿Es Aspose.PSD compatible con diferentes versiones de Java?

R1: Sí, Aspose.PSD admite Java 8, 11, 17 y versiones más recientes, garantizando una amplia compatibilidad en entornos de desarrollo.

### Q2: ¿Puedo usar Aspose.PSD para proyectos comerciales?

R2: Absolutamente, Aspose.PSD ofrece licencias comerciales para desarrolladores, permitiendo su uso tanto en aplicaciones personales como comerciales.

### Q3: ¿Hay limitaciones en los formatos de archivo de imagen soportados?

R3: Aspose.PSD soporta más de 30 formatos de imagen, incluidos PSD, JPEG, PNG, BMP, TIFF y más. Consulte la [documentación](https://reference.aspose.com/psd/java/) para obtener una lista completa.

### Q4: ¿Cómo puedo obtener soporte para consultas relacionadas con Aspose.PSD?

R4: Visite el [foro de Aspose.PSD](https://forum.aspose.com/c/psd/34) para buscar ayuda de la comunidad o del equipo de soporte de Aspose.

### Q5: ¿Hay una prueba gratuita disponible?

R5: Sí, puede explorar Aspose.PSD con una prueba gratuita. Descárguela [aquí](https://releases.aspose.com/).

---

**Última actualización:** 2026-07-08  
**Probado con:** Aspose.PSD for Java 24.12  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

## Tutoriales relacionados

- [Redimensionamiento simple con Aspose.PSD – Biblioteca de manipulación de imágenes Java](/psd/java/basic-image-operations/simple-resizing/)
- [Cómo rotar una imagen 270 grados con Aspose.PSD para Java](/psd/java/advanced-image-manipulation/rotate-image/)
- [Cómo ajustar gamma en procesamiento de imágenes Java con Aspose.PSD](/psd/java/advanced-techniques/adjust-gamma/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}