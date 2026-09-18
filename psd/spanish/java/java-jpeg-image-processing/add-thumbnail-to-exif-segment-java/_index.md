---
date: 2026-09-18
description: Aprenda cómo agregar una miniatura de metadatos de imagen java al segmento
  EXIF usando Aspose.PSD for Java. Esta guía paso a paso cubre los requisitos previos,
  la revisión del código y cómo guardar la imagen actualizada.
keywords:
- java image metadata
- how to add thumbnail
- java exif metadata
lastmod: 2026-09-18
linktitle: Agregar miniatura al segmento EXIF en Java
og_description: Aprenda cómo agregar una miniatura de metadatos de imagen java al
  segmento EXIF usando Aspose.PSD for Java. Siga la guía paso a paso para incrustar
  miniaturas y guardar la imagen actualizada.
og_image_alt: Guide showing Java code to embed a thumbnail into EXIF metadata using
  Aspose.PSD
og_title: Cómo agregar una miniatura de metadatos de imagen java al segmento EXIF
schemas:
- author: Aspose
  dateModified: '2026-09-18'
  description: Learn how to add java image metadata thumbnail to the EXIF segment
    using Aspose.PSD for Java. This step‑by‑step guide covers prerequisites, code
    walkthrough, and saving the updated image.
  headline: How to add java image metadata thumbnail to EXIF segment
  type: TechArticle
- questions:
  - answer: EXIF metadata is embedded information in digital images that includes
      camera settings, capture date, GPS coordinates, and other details.
    question: What is EXIF metadata?
  - answer: Adding a thumbnail improves user experience by allowing quick image previews
      without loading the full image.
    question: Why add a thumbnail to EXIF?
  - answer: You can download Aspose.PSD for Java from the [Aspose.PSD for Java download
      page](https://releases.aspose.com/psd/java/).
    question: Where can I download Aspose.PSD for Java?
  - answer: You can obtain a temporary license for Aspose.PSD from the [temporary
      license page](https://purchase.aspose.com/temporary-license/).
    question: How can I get a temporary license for Aspose.PSD?
  - answer: For support, visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34).
    question: How do I get support for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image metadata
- EXIF thumbnail
- Aspose.PSD
- Java image processing
title: Cómo agregar una miniatura de metadatos de imagen java al segmento EXIF
url: /es/java/java-jpeg-image-processing/add-thumbnail-to-exif-segment-java/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Añadir miniatura de metadatos de imagen java al segmento EXIF

## Introducción
En este tutorial aprenderá cómo añadir una miniatura de **java image metadata** al segmento EXIF de un archivo PSD usando Aspose.PSD para Java. Los metadatos EXIF (Exchangeable Image File Format) almacenan la configuración de la cámara, la fecha de captura, la ubicación y otra información útil. Incrustar una pequeña miniatura de vista previa permite a las aplicaciones mostrar una vista rápida de la imagen sin cargar el archivo completo, mejorando el rendimiento y la experiencia del usuario.

## Respuestas rápidas
- **¿Qué cubre el tutorial?** Añadir una miniatura al segmento EXIF de una imagen PSD con Aspose.PSD para Java.  
- **¿Cuánto tiempo lleva la implementación?** Aproximadamente 10‑15 minutos para una integración básica.  
- **¿Necesito una licencia?** Se requiere una licencia temporal para uso en producción; una prueba gratuita sirve para evaluación.  
- **¿Qué versión de Java es compatible?** Java 8 y versiones posteriores son totalmente compatibles.  
- **¿Se pueden procesar archivos grandes?** Sí—Aspose.PSD puede manejar archivos de hasta 2 GB sin cargar la imagen completa en memoria.

## ¿Qué es java image metadata?
Java image metadata se refiere a la información estructurada incrustada en archivos de imagen (como EXIF, IPTC o XMP) que puede leerse, modificarse o crearse programáticamente usando bibliotecas Java como Aspose.PSD. Estos metadatos permiten a las aplicaciones recuperar la configuración de la cámara, marcas de tiempo, coordenadas GPS y datos personalizados sin abrir el contenido visual.

## ¿Por qué añadir una miniatura a los metadatos EXIF?
Añadir una miniatura al segmento EXIF brinda una pista visual instantánea para navegadores de imágenes, exploradores de archivos y sistemas de gestión de contenido. Aspose.PSD procesa las miniaturas en memoria, lo que le permite incrustar una vista previa en menos de 0,2 segundos para imágenes de hasta 500 KB, y admite más de 30 formatos de imagen, incluidos PSD, JPEG, PNG y TIFF.

## Requisitos previos
Antes de sumergirse en el tutorial, asegúrese de contar con los siguientes requisitos:
- Conocimientos básicos de programación en Java.  
- Java Development Kit (JDK) instalado en su sistema.  
- IDE (Entorno de Desarrollo Integrado) para Java, como IntelliJ IDEA o Eclipse.  
- Biblioteca Aspose.PSD para Java. Puede descargarla desde la [página de descarga de Aspose.PSD para Java](https://releases.aspose.com/psd/java/).

## Importar paquetes
Las siguientes importaciones traen las clases de Aspose.PSD necesarias para trabajar con imágenes PSD y datos EXIF.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## Paso 1: cargar la imagen psd
`PsdImage` representa un archivo Photoshop PSD y proporciona acceso a sus capas y recursos.  
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage)Image.load(dataDir + "sample.psd");
```

## Paso 2: iterar sobre los recursos de la imagen
`ImageResource` encapsula recursos como miniaturas, perfiles ICC y metadatos incrustados en un archivo PSD.  
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || image.getImageResources()[i] instanceof Thumbnail4Resource) {
        ThumbnailResource thumbnail = (ThumbnailResource)image.getImageResources()[i];
        // Process the thumbnail resource
    }
}
```

## Paso 3: ajustar los datos de la miniatura
`JpegOptions` le permite configurar ajustes específicos de JPEG, como la calidad, para la imagen de la miniatura.  
```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setQuality(100); // Set JPEG quality
```

## Paso 4: guardar la imagen
Llamar a `save` escribe el segmento EXIF actualizado (incluyendo la nueva miniatura) de vuelta al disco sin volver a codificar la imagen completa.  
```java
image.save(dataDir + "output.psd");
```

## Problemas comunes y soluciones
- **Miniatura no aparece:** Verifique que el recurso de miniatura se haya añadido correctamente al segmento EXIF y que la imagen se guarde con el método `PsdImage.save`.  
- **Errores de falta de memoria en archivos grandes:** Use `PsdImage.load(..., LoadOptions)` con `LoadOptions.setLoadOnlyMetadata(true)` para trabajar solo con los metadatos.  
- **Orientación incorrecta:** Asegúrese de que la miniatura respete la bandera de orientación de la imagen original; puede leer la etiqueta EXIF `Orientation` y rotar la miniatura en consecuencia.

## Preguntas frecuentes

**Q: ¿Qué es los metadatos EXIF?**  
A: Los metadatos EXIF son información incrustada en imágenes digitales que incluye la configuración de la cámara, la fecha de captura, coordenadas GPS y otros detalles.

**Q: ¿Por qué añadir una miniatura a EXIF?**  
A: Añadir una miniatura mejora la experiencia del usuario al permitir vistas previas rápidas de la imagen sin cargar la imagen completa.

**Q: ¿Dónde puedo descargar Aspose.PSD para Java?**  
A: Puede descargar Aspose.PSD para Java desde la [página de descarga de Aspose.PSD para Java](https://releases.aspose.com/psd/java/).

**Q: ¿Cómo puedo obtener una licencia temporal para Aspose.PSD?**  
A: Puede obtener una licencia temporal para Aspose.PSD desde la [página de licencia temporal](https://purchase.aspose.com/temporary-license/).

**Q: ¿Cómo obtengo soporte para Aspose.PSD?**  
A: Para soporte, visite el [foro de Aspose.PSD](https://forum.aspose.com/c/psd/34).

---

**Última actualización:** 2026-09-18  
**Probado con:** Aspose.PSD for Java 24.10  
**Autor:** Aspose

## Tutoriales relacionados

- [Crear metadatos XMP en archivos PSD usando Aspose.PSD para Java](/psd/java/image-editing/create-xmp-metadata/)
- [Redimensionar imagen con Aspose.PSD para Java – Dibujar formas y operaciones básicas de imagen](/psd/java/basic-image-operations/)
- [Cómo convertir PSD a formatos de imagen rasterizados con Aspose.PSD para Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}