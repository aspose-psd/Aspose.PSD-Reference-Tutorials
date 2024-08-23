---
title: Extraer miniatura de PSD en Java
linktitle: Extraer miniatura de PSD en Java
second_title: API de Java Aspose.PSD
description: Aprenda a extraer miniaturas de archivos PSD usando Aspose.PSD para Java. Esta guía paso a paso cubre todo, desde la configuración hasta guardar las imágenes extraídas.
type: docs
weight: 15
url: /es/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
---
## Introducción
En este tutorial, exploraremos cómo extraer miniaturas de archivos PSD usando Aspose.PSD para Java. Las miniaturas pueden resultar útiles para vistas previas rápidas o para crear versiones más pequeñas de imágenes incrustadas en documentos PSD. Profundicemos en los pasos necesarios para lograr esto usando Aspose.PSD.
## Requisitos previos
Antes de comenzar, asegúrese de tener la siguiente configuración:
- Kit de desarrollo de Java (JDK) instalado en su sistema.
-  Aspose.PSD para la biblioteca Java. Puedes descargarlo desde[aquí](https://releases.aspose.com/psd/java/).
- Conocimientos básicos de programación Java.
## Importar paquetes
Para comenzar, incluya el paquete Aspose.PSD necesario en su clase Java:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```
## Paso 1: cargue el archivo PSD
Primero, cargue el archivo PSD que contiene la miniatura que desea extraer.
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
 Reemplazar`"Your_Document_Directory/"` con la ruta del directorio donde se encuentra su archivo PSD, y`"your_file.psd"` con el nombre de su archivo PSD.
## Paso 2: iterar sobre los recursos de imágenes
Recorra los recursos de imágenes para encontrar el recurso de miniaturas.
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Extraer datos en miniatura
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Cree una nueva imagen con los datos de miniatura extraídos
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Guarde la miniatura extraída como un archivo JPEG independiente
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Mensaje de éxito de salida
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Salga del bucle una vez que se encuentre y procese la miniatura
    }
}
```
## Paso 3: guarde la miniatura extraída
Guarde la miniatura extraída como un archivo de imagen independiente (en este caso, como un archivo JPEG).
## Paso 4: Manejo de diferentes tipos de miniaturas
 Si su archivo PSD puede contener varios tipos de miniaturas, como`Thumbnail4Resource`, puede ampliar la lógica para manejar esos casos de manera similar.

## Conclusión
En este tutorial, exploramos cómo extraer miniaturas de archivos PSD usando Aspose.PSD para Java. Si sigue los pasos descritos anteriormente, puede recuperar y guardar de manera eficiente miniaturas incrustadas en sus documentos PSD.

## Preguntas frecuentes
### ¿Qué es Aspose.PSD?
Aspose.PSD es una biblioteca de Java que permite a los desarrolladores trabajar con PSD y otros formatos de archivos de imagen mediante programación.
### ¿Dónde puedo encontrar más documentación sobre Aspose.PSD para Java?
 Puedes consultar el[documentación](https://reference.aspose.com/psd/java/) para referencias detalladas de API y ejemplos.
### ¿Puedo probar Aspose.PSD gratis antes de comprarlo?
 Sí, puedes descargar un[prueba gratuita](https://releases.aspose.com/) evaluar las capacidades de la biblioteca.
### ¿Cómo puedo obtener licencias temporales para Aspose.PSD?
 Las licencias temporales se pueden obtener de[aquí](https://purchase.aspose.com/temporary-license/).
### ¿Aspose.PSD es adecuado para uso comercial?
Sí, Aspose.PSD se puede utilizar para proyectos personales y comerciales según los términos de su licencia.