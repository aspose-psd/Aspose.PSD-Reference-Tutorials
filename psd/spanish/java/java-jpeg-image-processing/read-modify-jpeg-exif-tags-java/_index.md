---
date: 2026-10-03
description: Aprenda cómo java leer metadatos de imagen y modificar etiquetas JPEG
  EXIF con Aspose.PSD for Java en esta guía paso a paso, perfecta para desarrolladores
  que manejan metadatos de imagen de manera eficiente.
keywords:
- java read image metadata
- read EXIF tags Java
- modify JPEG metadata Java
- Aspose.PSD Java
lastmod: 2026-10-03
linktitle: Leer y modificar etiquetas JPEG EXIF en Java
og_description: Aprenda cómo java leer metadatos de imagen y modificar etiquetas JPEG
  EXIF con Aspose.PSD for Java. Esta guía muestra código paso a paso para extraer
  y actualizar información EXIF.
og_image_alt: Guide showing how to java read image metadata and edit JPEG EXIF tags
  using Aspose.PSD for Java
og_title: Cómo java leer metadatos de imagen y modificar etiquetas JPEG EXIF
schemas:
- author: Aspose
  dateModified: '2026-10-03'
  description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  headline: How to java read image metadata and modify JPEG EXIF tags
  type: TechArticle
- description: Learn how to java read image metadata and modify JPEG EXIF tags with
    Aspose.PSD for Java in this step‑by‑step guide, perfect for developers handling
    image metadata efficiently.
  name: How to java read image metadata and modify JPEG EXIF tags
  steps:
  - name: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – make sure you have JDK 11 or newer. You
      can download it from the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – obtain the latest JAR from the [Aspose
      releases page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any editor you prefer.'
  - name: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
    text: '**Basic Java knowledge** – you should be comfortable with creating projects
      and adding external JARs.'
  type: HowTo
- questions:
  - answer: EXIF (Exchangeable Image File Format) metadata stores camera settings,
      timestamps, GPS coordinates, and other information embedded in JPEG and other
      image files.
    question: What is EXIF data?
  - answer: You can get a free trial from the [Aspose releases page](https://releases.aspose.com/).
    question: Can I use Aspose.PSD for Java for free?
  - answer: Aspose.PSD for Java supports Java SE 7 and above.
    question: Is Aspose.PSD for Java compatible with all versions of Java?
  - answer: Check out the [documentation](https://reference.aspose.com/psd/java/)
      for more details.
    question: Where can I find more documentation on Aspose.PSD for Java?
  - answer: You can get support from the [Aspose PSD support forum](https://forum.aspose.com/c/psd/34/).
    question: How do I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image metadata
- exif tags
- aspose psd
- jpeg metadata
- java tutorial
title: Cómo java leer metadatos de imagen y modificar etiquetas JPEG EXIF
url: /es/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Leer y modificar etiquetas EXIF JPEG en Java

## Introducción
Si necesitas **java read image metadata** de archivos JPEG y cambiarlo programáticamente, has llegado al lugar correcto. En este tutorial recorreremos la extracción y actualización de etiquetas EXIF usando Aspose.PSD for Java. Al final podrás obtener los detalles de la cámara, la orientación y campos personalizados, y luego escribirlos de nuevo en el archivo, todo sin un editor gráfico.

## Respuestas rápidas
- **¿Qué biblioteca maneja JPEG EXIF en Java?** Aspose.PSD for Java.
- **¿Cuántas líneas de código se necesitan para leer EXIF?** Alrededor de tres líneas después de cargar la imagen.
- **¿Puedes modificar etiquetas EXIF?** Sí, puedes cambiar cualquier etiqueta estándar o personalizada y guardar el resultado.
- **¿Formatos de imagen compatibles?** Más de 150 formatos, incluyendo PSD, JPEG, PNG, TIFF y BMP.
- **¿Versión mínima de Java?** Java 7 o superior.

## ¿Por qué usar Aspose.PSD para Java?
Aspose.PSD soporta **150+ formatos de imagen** y puede procesar archivos de hasta **2 GB** sin cargar todo el documento en memoria, brindándote operaciones de metadatos rápidas y de bajo consumo de memoria en colecciones de fotos grandes. También ofrece una API sencilla para leer y escribir datos EXIF, IPTC y XMP, haciendo que el procesamiento por lotes de miles de imágenes sea eficiente y fiable.

## Requisitos previos
1. **Java Development Kit (JDK)** – asegúrate de tener JDK 11 o más reciente. Puedes descargarlo del [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java library** – obtén el último JAR de la [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, o cualquier editor que prefieras.  
4. **Conocimientos básicos de Java** – deberías estar cómodo creando proyectos y añadiendo JARs externos.

## ¿Qué es java read image metadata?
Java read image metadata se refiere al proceso de acceder programáticamente a la información incrustada como EXIF, IPTC y XMP almacenada dentro de archivos de imagen usando código Java. Estos metadatos pueden incluir configuraciones de cámara, marcas de tiempo, coordenadas GPS, avisos de derechos de autor y comentarios de usuario, permitiendo que las aplicaciones organicen, busquen y manipulen imágenes basándose en sus datos descriptivos.

## Importar paquetes
Primero, agrega el JAR de Aspose.PSD al classpath de tu proyecto e importa las clases requeridas.

El paquete `com.aspose.psd` proporciona la API central para cargar imágenes y acceder a sus recursos.

```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## ¿Cómo leer metadatos de imagen de archivos JPEG en Java?
Carga el JPEG con `PsdImage.load("image.jpg")`, localiza el recurso de miniatura que contiene los datos EXIF y luego llama a `ExifData.read()` para obtener un objeto `ExifData` poblado. Este enfoque de un solo paso te brinda acceso completo a todos los campos EXIF estándar y a cualquier etiqueta personalizada que hayas añadido.

## Paso 1: Cargar la imagen PSD
PsdImage es la clase de Aspose.PSD que representa un archivo PSD y proporciona métodos para acceder a sus recursos y metadatos.  
En este paso, cargaremos la imagen PSD de la que queremos leer los datos EXIF. Asegúrate de que tu imagen esté en el directorio correcto.

```java
String dataDir = "Your Document Directory";
PsdImage image = null;
try {
    image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## Paso 2: Iterar sobre los recursos de la imagen
ThumbnailResource representa una imagen en miniatura almacenada en un archivo PSD, a menudo contiene datos EXIF incrustados.  
Una vez que la imagen está cargada, el siguiente paso es iterar sobre sus recursos para encontrar el recurso de miniatura, que típicamente contiene los datos EXIF.

```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        // Proceed to next step
    }
}
```

## Paso 3: Extraer datos EXIF
JpegExifData es la clase que contiene la información EXIF extraída de una imagen JPEG, permitiendo leer y modificar etiquetas individuales.  
Ahora que tenemos el recurso de miniatura, podemos extraer los datos EXIF de él. Los datos EXIF incluyen información valiosa como el nombre del propietario de la cámara, valor de apertura, orientación y más.

```java
JpegExifData exifData = thumbnail.getJpegOptions().getExifData();
if (exifData != null) {
    System.out.println("Camera Owner Name: " + exifData.getCameraOwnerName());
    System.out.println("Aperture Value: " + exifData.getApertureValue());
    System.out.println("Orientation: " + exifData.getOrientation());
    System.out.println("Focal Length: " + exifData.getFocalLength());
    System.out.println("Compression: " + exifData.getCompression());
}
```

## Paso 4: Modificar datos EXIF
Después de leer los datos EXIF, puede que desees modificar algunos de sus campos. Así es como puedes hacerlo:

```java
if (exifData != null) {
    exifData.setCameraOwnerName("New Camera Owner");
    exifData.setApertureValue(3.5);
    exifData.setOrientation(1);
    exifData.setFocalLength(35.0);
    exifData.setCompression(6);
    thumbnail.getJpegOptions().setExifData(exifData);
}
```

## Paso 5: Guardar los cambios
Finalmente, después de modificar los datos EXIF, guarda los cambios en un nuevo archivo PSD.

```java
try {
    image.save(dataDir + "Modified_Zebras_Serengeti.psd");
} catch (IOException e) {
    e.printStackTrace();
}
```

## Problemas comunes y soluciones
- **Recurso de miniatura faltante** – Algunos JPEG almacenan EXIF directamente en el encabezado principal de la imagen. Si el recurso de miniatura está ausente, usa `image.getExifData()` en su lugar.  
- **Archivos grandes causan OutOfMemoryError** – Asegúrate de ejecutar la JVM con suficiente heap (`-Xmx2g`) o procesa la imagen en modo streaming usando `PsdImage.load(inputStream, loadOptions)`.  
- **Tipos de etiqueta no compatibles** – Aspose.PSD soporta todas las etiquetas EXIF estándar; las etiquetas personalizadas pueden requerir manejo manual a nivel de bytes.

## Preguntas frecuentes

**Q: ¿Qué son los datos EXIF?**  
A: Los metadatos EXIF (Exchangeable Image File Format) almacenan configuraciones de cámara, marcas de tiempo, coordenadas GPS y otra información incrustada en archivos JPEG y otros formatos de imagen.

**Q: ¿Puedo usar Aspose.PSD para Java gratis?**  
A: Puedes obtener una prueba gratuita de la [Aspose releases page](https://releases.aspose.com/).

**Q: ¿Es Aspose.PSD para Java compatible con todas las versiones de Java?**  
A: Aspose.PSD para Java soporta Java SE 7 y superiores.

**Q: ¿Dónde puedo encontrar más documentación sobre Aspose.PSD para Java?**  
A: Consulta la [documentation](https://reference.aspose.com/psd/java/) para más detalles.

**Q: ¿Cómo obtengo soporte para Aspose.PSD para Java?**  
A: Puedes obtener soporte del [Aspose PSD support forum](https://forum.aspose.com/c/psd/34/).

## Conclusión
Siguiendo estos pasos puedes **java read image metadata** de cualquier JPEG, ajustar los campos EXIF que necesites y escribir los datos actualizados de vuelta al archivo, todo con unas pocas líneas de código Java limpio. La rica API de Aspose.PSD hace que el manejo de metadatos sea fiable y de alto rendimiento, por lo que puedes integrarla en pipelines de procesamiento por lotes, herramientas de gestión de fotos o cualquier aplicación que necesite trabajar con información de imágenes.

---

**Last Updated:** 2026-10-03  
**Tested With:** Aspose.PSD for Java 24.5  
**Author:** Aspose

## Tutoriales relacionados

- [Leer información de etiquetas EXIF específicas en Java con Aspose (asp)](/psd/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/)
- [Crear metadatos XMP en archivos PSD usando Aspose.PSD para Java](/psd/java/image-editing/create-xmp-metadata/)
- [Redimensionar imagen con Aspose.PSD para Java – Dibujar formas y operaciones básicas de imagen](/psd/java/basic-image-operations/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}