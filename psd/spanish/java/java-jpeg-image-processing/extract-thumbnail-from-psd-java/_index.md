---
date: 2026-01-25
description: Aprende cómo extraer la miniatura de archivos PSD usando Aspose.PSD para
  Java. Sigue esta guía paso a paso para cargar, extraer y guardar miniaturas rápidamente.
linktitle: Extract Thumbnail from PSD in Java
second_title: Aspose.PSD Java API
title: Extraer miniatura de PSD en Java
url: /es/java/java-jpeg-image-processing/extract-thumbnail-from-psd-java/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Extraer miniatura de PSD en Java

## Introducción
En este tutorial, aprenderás **cómo extraer miniatura de PSD** usando la biblioteca Aspose.PSD para Java. Las miniaturas son pequeñas imágenes de vista previa incrustadas dentro de los documentos PSD, y extraerlas puede ayudarte a generar vistas previas rápidas, crear galerías de imágenes o reducir el almacenamiento cuando solo necesitas una representación pequeña de la obra original. Repasaremos todo, desde la configuración del proyecto hasta guardar la miniatura extraída como un archivo de imagen estándar.

## Respuestas rápidas
- **¿Qué cubre este tutorial?** Extracción y guardado de una imagen miniatura de un archivo PSD con Aspose.PSD para Java.  
- **¿Qué biblioteca se requiere?** Aspose.PSD para Java (descargable desde el sitio oficial de Aspose).  
- **¿Necesito una licencia?** Se requiere una licencia temporal o completa para uso en producción; hay disponible una prueba gratuita.  
- **¿Qué formato de salida se usa?** El ejemplo guarda la miniatura como un archivo JPEG, pero se puede elegir cualquier formato compatible.  
- **¿Cuánto tiempo lleva la implementación?** Aproximadamente 5‑10 minutos para un desarrollador familiarizado con conceptos básicos de Java.

## ¿Qué es “extraer miniatura de PSD”?
Extraer una miniatura de un PSD significa leer la pequeña imagen de vista previa que Photoshop almacena dentro de la sección de recursos del archivo. Esta vista previa suele ser una versión de baja resolución del lienzo completo, lo que la hace ideal para una carga rápida en navegadores de archivos o galerías web.

## ¿Por qué extraer miniaturas con Aspose.PSD?
- **Velocidad:** No es necesario abrir el PSD completo en un editor gráfico; la miniatura ya está incrustada.  
- **Automatización:** Perfecto para el procesamiento por lotes de grandes bibliotecas de imágenes.  
- **Multiplataforma:** Funciona en cualquier SO que soporte Java, sin requerir Photoshop.  
- **Flexibilidad de formato:** Convierte la miniatura a JPEG, PNG o cualquier formato compatible con Aspose.PSD.

## Requisitos previos
Antes de comenzar, asegúrate de tener lo siguiente configurado:
- Java Development Kit (JDK) instalado en tu sistema.  
- Biblioteca Aspose.PSD para Java. Puedes descargarla desde [aquí](https://releases.aspose.com/psd/java/).  
- Conocimientos básicos de programación en Java.

## Importar paquetes
Para comenzar, incluye el paquete necesario de Aspose.PSD en tu clase Java:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.resources.Thumbnail4Resource;
import com.aspose.psd.fileformats.psd.resources.ThumbnailResource;
import com.aspose.psd.imageoptions.JpegOptions;
```

## Cómo extraer miniatura de PSD usando Aspose.PSD para Java
A continuación se muestra la guía paso a paso. Cada paso incluye una breve explicación seguida del código exacto que necesitas copiar.

### Paso 1: Cargar el archivo PSD
Primero, carga el archivo PSD que contiene la miniatura que deseas extraer.
```java
String dataDir = "Your_Document_Directory/";
PsdImage image = (PsdImage)Image.load(dataDir + "your_file.psd");
```
Reemplaza `"Your_Directory/"` con la ruta del directorio donde se encuentra tu archivo PSD, y `"your_file.psd"` con el nombre de tu archivo PSD.

### Paso 2: Iterar sobre los recursos de imagen
Itera a través de los recursos de imagen para encontrar el recurso de miniatura.
```java
for (int i = 0; i < image.getImageResources().length; i++) {
    if (image.getImageResources()[i] instanceof ThumbnailResource) {
        ThumbnailResource thumbnail = (ThumbnailResource) image.getImageResources()[i];
        
        // Extract thumbnail data
        int[] data = thumbnail.getThumbnailArgb32Data();
        
        // Create a new image with the extracted thumbnail data
        PsdImage extractedThumbnailImage = new PsdImage(thumbnail.getWidth(), thumbnail.getHeight());
        extractedThumbnailImage.saveArgb32Pixels(extractedThumbnailImage.getBounds(), data);
        
        // Save the extracted thumbnail as a separate JPEG file
        extractedThumbnailImage.save(dataDir + "extracted_thumbnail.jpg", new JpegOptions());
        
        // Output success message
        System.out.println("Thumbnail extracted and saved successfully.");
        
        break; // Exit the loop once thumbnail is found and processed
    }
}
```

### Paso 3: Guardar la miniatura extraída
El código en el paso anterior ya guarda la miniatura como un archivo JPEG llamado `extracted_thumbnail.jpg` en el mismo directorio. Puedes cambiar el nombre del archivo o el formato ajustando los parámetros del método `save`.

### Paso 4: Manejo de diferentes tipos de miniaturas
Si tu archivo PSD puede contener varios tipos de miniaturas, como `Thumbnail4Resource`, puedes ampliar la lógica para manejar esos casos de forma similar. Simplemente agrega una verificación `instanceof Thumbnail4Resource` dentro del bucle y procésala usando el mismo patrón.

## Problemas comunes y soluciones
- **No se encontró miniatura:** No todos los archivos PSD contienen un recurso de miniatura. Verifica el archivo fuente en Photoshop (Archivo → Exportar → Miniatura) o usa un PSD diferente que incluya una vista previa.  
- **Error de formato de imagen no compatible:** Asegúrate de estar usando una versión reciente de Aspose.PSD que soporte el formato objetivo.  
- **Errores de permiso al guardar:** Confirma que la aplicación tenga acceso de escritura al directorio de salida.

## Preguntas frecuentes

**P: ¿Qué es Aspose.PSD?**  
R: Aspose.PSD es una biblioteca Java que permite a los desarrolladores trabajar con archivos PSD y otros formatos de imagen de forma programática.

**P: ¿Dónde puedo encontrar más documentación sobre Aspose.PSD para Java?**  
R: Puedes consultar la [documentación](https://reference.aspose.com/psd/java/) para referencias detalladas de la API y ejemplos.

**P: ¿Puedo probar Aspose.PSD gratis antes de comprar?**  
R: Sí, puedes descargar una [prueba gratuita](https://releases.aspose.com/) para evaluar las capacidades de la biblioteca.

**P: ¿Cómo puedo obtener licencias temporales para Aspose.PSD?**  
R: Las licencias temporales pueden obtenerse desde [aquí](https://purchase.aspose.com/temporary-license/).

**P: ¿Es Aspose.PSD adecuado para uso comercial?**  
R: Sí, Aspose.PSD puede usarse tanto en proyectos personales como comerciales bajo sus términos de licencia.

## Conclusión
En este tutorial, exploramos cómo **extraer miniatura de PSD** usando Aspose.PSD para Java. Siguiendo los pasos descritos arriba, puedes recuperar y guardar de manera eficiente las miniaturas incrustadas en tus documentos PSD, lo que permite vistas previas más rápidas y flujos de trabajo de imágenes simplificados.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Última actualización:** 2026-01-25  
**Probado con:** Aspose.PSD for Java (latest release)  
**Autor:** Aspose