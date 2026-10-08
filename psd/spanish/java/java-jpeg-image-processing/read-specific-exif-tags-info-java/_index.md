---
date: 2026-10-08
description: Aprenda a leer etiquetas EXIF en Java usando Aspose.PSD para Java (asp)
  con nuestro tutorial paso a paso, y mejore sus capacidades de procesamiento de imágenes.
keywords:
- read exif tags java
- java exif tag extraction
- java image metadata extraction
lastmod: 2026-10-08
linktitle: Leer información de etiquetas EXIF específicas en Java
og_description: Los desarrolladores Java pueden extraer rápidamente metadatos de imágenes
  usando Aspose.PSD. Esta guía le muestra cómo cargar un PSD, localizar recursos de
  miniaturas y imprimir campos clave de EXIF como WhiteBalance y ISO speed.
og_image_alt: Guide showing how to read EXIF tags from PSD files in Java using Aspose.PSD
og_title: Cómo leer etiquetas EXIF en Java con Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-10-08'
  description: Learn how to read EXIF tags in Java using Aspose.PSD for Java (asp)
    with our step‑by‑step tutorial, and boost your image processing capabilities.
  headline: How to read EXIF tags in Java with Aspose.PSD
  type: TechArticle
- description: Learn how to read EXIF tags in Java using Aspose.PSD for Java (asp)
    with our step‑by‑step tutorial, and boost your image processing capabilities.
  name: How to read EXIF tags in Java with Aspose.PSD
  steps:
  - name: 'Java Development Kit (JDK): Ensure you have JDK installed on your machine.
      You can download it from the [Oracle JDK website](https://www.oracle.com/java/technologies/javase-downloads.html).'
    text: 'Java Development Kit (JDK): Ensure you have JDK installed on your machine.
      You can download it from the [Oracle JDK website](https://www.oracle.com/java/technologies/javase-downloads.html).'
  - name: 'Aspose.PSD for Java: Download the library from the [Aspose.PSD for Java
      download page](https://releases.aspose.com/psd/java/).'
    text: 'Aspose.PSD for Java: Download the library from the [Aspose.PSD for Java
      download page](https://releases.aspose.com/psd/java/).'
  - name: 'Integrated Development Environment (IDE): An IDE like IntelliJ IDEA, Eclipse,
      or NetBeans will make coding more convenient.'
    text: 'Integrated Development Environment (IDE): An IDE like IntelliJ IDEA, Eclipse,
      or NetBeans will make coding more convenient.'
  - name: 'PSD file: A PSD file with EXIF data. You can use the sample provided in
      this tutorial or any other PSD file with EXIF tags.'
    text: 'PSD file: A PSD file with EXIF data. You can use the sample provided in
      this tutorial or any other PSD file with EXIF tags.'
  type: HowTo
- questions:
  - answer: Aspose.PSD (asp)
    question: What library reads EXIF data from PSD in Java?
  - answer: WhiteBalance, PixelXDimension, PixelYDimension, ISOSpeed, FocalLength,
      and more.
    question: Which tags can be extracted?
  - answer: Yes, a commercial license is required; a free trial is available.
    question: Do I need a license for production?
  - answer: The same API supports PNG, JPEG, TIFF via Java image metadata extraction.
    question: Can I use this with other image formats?
  - answer: About 10‑15 minutes for a basic read‑only scenario.
    question: How long does implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- read exif tags java
- Aspose.PSD
- java image metadata extraction
- EXIF extraction
- PSD processing
title: Cómo leer etiquetas EXIF en Java con Aspose.PSD
url: /es/java/java-jpeg-image-processing/read-specific-exif-tags-info-java/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Leer información de etiquetas EXIF específicas en Java con Aspose (asp)

## Introducción
Si necesitas **leer etiquetas EXIF en Java**, Aspose.PSD (asp) ofrece una API limpia y pura‑Java que funciona sin Photoshop. En este tutorial aprenderás cómo extraer datos EXIF de una imagen PSD, seleccionar solo las etiquetas que te interesan y mostrarlas en la consola. Cubriremos todo, desde configurar tu entorno de desarrollo hasta extraer metadatos como WhiteBalance, velocidad ISO y distancia focal. ¡Comencemos!

## Respuestas rápidas
- **¿Qué biblioteca lee datos EXIF de PSD en Java?** Aspose.PSD (asp)  
- **¿Qué etiquetas se pueden extraer?** WhiteBalance, PixelXDimension, PixelYDimension, ISOSpeed, FocalLength, y más.  
- **¿Necesito una licencia para producción?** Sí, se requiere una licencia comercial; hay una prueba gratuita disponible.  
- **¿Puedo usar esto con otros formatos de imagen?** La misma API admite PNG, JPEG, TIFF mediante extracción de metadatos de imagen en Java.  
- **¿Cuánto tiempo lleva la implementación?** Aproximadamente 10‑15 minutos para un escenario básico de solo lectura.

## ¿Qué es asp (Aspose.PSD para Java)?
Aspose.PSD for Java es una biblioteca pure‑Java que permite a los desarrolladores trabajar con archivos de Adobe Photoshop (PSD, PSB) sin instalar Photoshop. Proporciona acceso programático a capas, recursos y metadatos, incluidas las etiquetas EXIF, lo que la hace ideal para tareas de **java image metadata extraction**.

## ¿Por qué usar Aspose.PSD (asp) para la extracción de EXIF?
Puedes extraer etiquetas EXIF en Java con solo dos llamadas a métodos, y la biblioteca procesa archivos de hasta 2 GB sin cargar todo el documento en memoria. Soporta **30+ image formats** y preserva los ajustes exactos de la cámara, brindándote resultados determinísticos en entornos Windows, Linux y macOS.

## Requisitos previos
Antes de sumergirnos en el código, hay algunas cosas que deberás tener listas:

1. Java Development Kit (JDK): Asegúrate de que tienes el JDK instalado en tu máquina. Puedes descargarlo desde el [Oracle JDK website](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. Aspose.PSD for Java: Descarga la biblioteca desde la [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).  
3. Integrated Development Environment (IDE): Un IDE como IntelliJ IDEA, Eclipse o NetBeans hará que programar sea más cómodo.  
4. PSD file: Un archivo PSD con datos EXIF. Puedes usar el ejemplo proporcionado en este tutorial o cualquier otro archivo PSD con etiquetas EXIF.

## Importar paquetes
Importa las clases necesarias de Aspose.PSD como Image, PsdImage, ThumbnailResource y JpegExifData para trabajar con archivos PSD.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.exif.JpegExifData;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
```

## Paso 1: cargar la imagen PSD
`Image.load()` carga un archivo y devuelve un objeto Image que representa los datos de la imagen.  
`PsdImage` es la clase Aspose.PSD que proporciona funcionalidad específica de PSD.  
El método `Image.load()` carga cualquier archivo de imagen compatible en memoria, devolviendo un objeto `Image` genérico que puedes convertir (cast) a un tipo específico de PSD.  
```java
String dataDir = "Your Document Directory";
PsdImage image = (PsdImage) Image.load(dataDir + "1280px-Zebras_Serengeti.psd");
```

En este paso, cargamos el archivo PSD usando el método `Image.load()`. La clase `PsdImage` se utiliza para representar la imagen PSD, y convertimos la imagen cargada a esta clase para acceder a funcionalidades específicas de PSD.

## Paso 2: iterar sobre los recursos de la imagen
`PsdImage.getResources()` devuelve una colección de recursos incrustados como miniaturas y datos EXIF.  
La llamada `PsdImage.getResources()` devuelve una colección de todos los recursos incrustados. Al iterar sobre esta colección puedes localizar recursos de miniatura que contienen metadatos EXIF.  
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource || 
        image.getImageResources()[i] instanceof Thumbnail4Resource) {
        // Further processing will be done here
    }
}
```

Recorremos los recursos de la imagen usando un bucle `for`. El objetivo es identificar recursos que sean instancias de `ThumbnailResource` o `Thumbnail4Resource`, ya que son los tipos que contienen los datos EXIF.

## Paso 3: extraer datos EXIF
`ThumbnailResource.getJpegOptions()` proporciona acceso a opciones JPEG, incluidas los metadatos EXIF.  
`JpegExifData` contiene valores individuales de etiquetas EXIF.  
El método `ThumbnailResource.getJpegOptions()` brinda acceso a un objeto `JpegExifData`, que contiene etiquetas EXIF individuales como WhiteBalance, ISOSpeed y FocalLength.  
```java
if (image.getImageResources()[i] instanceof ThumbnailResource) {
    JpegExifData exif = ((ThumbnailResource) image.getImageResources()[i]).getJpegOptions().getExifData();
    if (exif != null) {
        System.out.println("Exif WhiteBalance: " + exif.getWhiteBalance());
        System.out.println("Exif PixelXDimension: " + exif.getPixelXDimension());
        System.out.println("Exif PixelYDimension: " + exif.getPixelYDimension());
        System.out.println("Exif ISOSpeed: " + exif.getISOSpeed());
        System.out.println("Exif FocalLength: " + exif.getFocalLength());
    }
}
```

Usamos una sentencia `if` para comprobar si el recurso es una instancia de `ThumbnailResource`. Si lo es, lo convertimos y obtenemos sus `JpegOptions` para acceder al `ExifData`. Finalmente, imprimimos varias etiquetas EXIF como WhiteBalance, dimensiones de píxeles, ISOSpeed y FocalLength.

## Problemas comunes y consejos
- **Null EXIF data:** Algunos archivos PSD pueden no contener un recurso de miniatura con información EXIF. Siempre verifica que no sea `null` antes de acceder a los valores de las etiquetas.  
- **File path errors:** Usa rutas absolutas o asegúrate de que el directorio de trabajo apunte a la carpeta que contiene tu archivo PSD.  
- **License restrictions:** La prueba gratuita limita la cantidad de páginas que puedes procesar; actualiza a una licencia completa para uso sin restricciones.

## Preguntas frecuentes
### ¿Qué son los datos EXIF?
Los datos EXIF (Exchangeable Image File Format) son metadatos incrustados en archivos de imagen, que contienen información como ajustes de cámara, fecha y hora, y dimensiones de la imagen.

### ¿Puedo editar datos EXIF usando Aspose.PSD?
Sí, Aspose.PSD permite leer y modificar datos EXIF. Puedes actualizar etiquetas y guardar los cambios de nuevo en el archivo de imagen.

### ¿Aspose.PSD para Java es gratuito?
Aspose.PSD ofrece una versión de prueba gratuita que puedes descargar desde la [Aspose.PSD official releases page](https://releases.aspose.com/). Para obtener todas las funciones, necesitas adquirir una licencia.

### ¿Qué otros formatos soporta Aspose.PSD?
Aspose.PSD soporta varios formatos de Adobe Photoshop, incluidos PSD, PSB y más. También ofrece opciones para convertir estos formatos a PNG, JPEG, TIFF, etc.

### ¿Cómo obtengo soporte para Aspose.PSD?
Puedes obtener soporte a través del [forum](https://forum.aspose.com/c/psd/34) de Aspose.PSD.

### ¿Cómo ayuda esto con **java image metadata extraction**?
Al usar el objeto `JpegExifData`, puedes extraer programáticamente cualquier etiqueta EXIF que necesites, lo que lo convierte en una base sólida para tareas más amplias de extracción de metadatos en diferentes formatos de imagen.

---

**Última actualización:** 2026-10-08  
**Probado con:** Aspose.PSD for Java 24.11 (última versión al momento de escribir)  
**Autor:** Aspose

## Tutoriales relacionados

- [Leer y modificar etiquetas Jpeg Exif Java](/psd/java/java-jpeg-image-processing/read-modify-jpeg-exif-tags-java/)
- [Procesamiento de imágenes Jpeg Java](/psd/java/java-jpeg-image-processing/)
- [Cómo rotar una imagen en un ángulo específico con Aspose.PSD para Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}