---
date: 2026-01-07
description: Aprende cómo recortar imágenes en Java usando Aspose.PSD para Java. Guía
  paso a paso para recortar imágenes, cambiar su tamaño y convertir de PSD a JPEG.
linktitle: Expand and Crop Images
second_title: Aspose.PSD Java API
title: 'Recortar Imagen Java: Expandir y Recortar Imágenes con Aspose.PSD para Java'
url: /es/java/image-editing/expand-and-crop-images/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Recortar Imagen Java: Expandir y Recortar Imágenes con Aspose.PSD para Java

## Introducción

En este tutorial descubrirás cómo **crop image java** con la biblioteca Aspose.PSD. Ya sea que necesites expandir un lienzo, recortar bordes no deseados o convertir un archivo PSD a JPEG, los pasos a continuación te guiarán a través de un proceso limpio y repetible. Cubriremos los requisitos previos, las declaraciones de importación y cada paso de codificación con explicaciones claras para que puedas aplicar la técnica en proyectos del mundo real.

## Respuestas Rápidas
- **¿Qué biblioteca maneja crop image java?** Aspose.PSD for Java.
- **¿Necesito una licencia para desarrollo?** Una prueba gratuita funciona para pruebas; se requiere una licencia comercial para producción.
- **¿Puedo convertir PSD a JPEG mientras recorto?** Sí, usando `JpegOptions` junto con un rectángulo de recorte.
- **¿Se admite Java 8?** Aspose.PSD admite Java 8 y versiones posteriores.
- **¿Cuánto tiempo lleva la implementación?** Normalmente menos de 10 minutos para una operación de recorte básica.

## Qué es “crop image java”?

Recortar una imagen en Java significa seleccionar una región rectangular de la imagen original y descartar el resto. Con Aspose.PSD puedes definir esta región usando un objeto `Rectangle`, y luego guardar el resultado en un formato diferente como JPEG.

## ¿Por qué usar Aspose.PSD para recortar imágenes en Java?

- **Full PSD support** – trabaja directamente con archivos PSD con capas sin convertirlos primero.  
- **High‑performance raster handling** – uso eficiente de memoria para imágenes grandes.  
- **Built‑in conversion** – exporta fácilmente a JPEG, PNG, BMP, etc., mientras aplicas recorte o expansión del lienzo.  
- **Cross‑platform** – funciona en cualquier sistema que ejecute Java.

## Requisitos Previos

Antes de profundizar, asegúrate de tener:

1. **Java Development Kit (JDK)** – Java 8 o posterior instalado.  
2. **Aspose.PSD for Java** – descarga la biblioteca desde el sitio oficial **[here](https://releases.aspose.com/psd/java/)**.  

> **Pro tip:** Añade el JAR de Aspose.PSD al classpath de tu proyecto o a las dependencias de Maven/Gradle para evitar `ClassNotFoundException`.

## Importar Paquetes

Agrega las importaciones necesarias a tu archivo fuente Java. Estas clases te dan acceso a la carga de imágenes, manipulación de raster, definición de rectángulos y opciones de exportación JPEG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Paso 1: Establecer el Directorio del Documento

Especifica la carpeta que contiene el archivo PSD fuente. Reemplaza el marcador de posición con la ruta real en tu máquina.

```java
String dataDir = "Your Document Directory";
```

## Paso 2: Especificar Rutas de Origen y Destino

Define de dónde leer el PSD y dónde escribir el JPEG recortado.

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## Paso 3: Cargar y Cachear la Imagen

Carga el PSD en un objeto `RasterImage`. Cachear mejora el rendimiento para operaciones posteriores como el recorte.

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

## Paso 4: Crear un Rectángulo para el Recorte

Crea un `Rectangle` que describa la región que deseas conservar. Las coordenadas pueden ser negativas para **expandir** el lienzo antes del recorte, lo cual es útil para añadir un borde alrededor de la imagen original.

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

> **¿Por qué usar coordenadas negativas?**  
> Los valores negativos de X/Y desplazan el área de recorte hacia la izquierda/arriba, añadiendo efectivamente espacio vacío (expandiendo) alrededor del contenido original antes del recorte final.

## Paso 5: Guardar la Imagen Recortada

Finalmente, guarda la imagen resultante usando `JpegOptions`. Este paso también muestra **convert psd jpeg** mientras se aplica el rectángulo de recorte.

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

> **Resultado:** `jpeg_out.jpg` ahora contiene una imagen de 300 × 300 píxeles que ha sido expandida 200 px en cada lado y luego recortada al rectángulo definido.

¡Felicidades! Has realizado con éxito **java image cropping**, expandido el lienzo y convertido un archivo PSD a JPEG, todo en unas pocas líneas concisas de código.

## Casos de Uso Comunes

- **Preparing assets for web** – recorta y redimensiona capturas de pantalla o diseños antes de subirlos.  
- **Generating thumbnails** – extrae una región específica de un PSD grande para propósitos de vista previa.  
- **Automated batch processing** – recorre una carpeta de archivos PSD, aplicando el mismo rectángulo de recorte a cada uno.

## Solución de Problemas y Consejos

| Problema | Solución Sugerida |
|----------|-------------------|
| `OutOfMemoryError` al cargar PSDs grandes | Llama a `rasterImage.cacheData()` temprano y considera aumentar el tamaño del heap de la JVM (`-Xmx`). |
| El área recortada está descentrada | Verifica los desplazamientos X/Y del rectángulo; recuerda que los valores negativos expanden el lienzo. |
| El JPEG de salida se ve borroso | Ajusta la configuración de calidad de `JpegOptions` (p.ej., `new JpegOptions { Quality = 90 }`). |

## Preguntas Frecuentes

### P1: ¿Es Aspose.PSD compatible con diferentes versiones de Java?

R1: Sí, Aspose.PSD admite varias versiones de Java, garantizando compatibilidad con una amplia gama de entornos de desarrollo.

### P2: ¿Puedo usar Aspose.PSD para proyectos comerciales?

R2: Absolutamente, Aspose.PSD ofrece licencias comerciales para desarrolladores, permitiendo su uso tanto en proyectos personales como comerciales.

### P3: ¿Hay limitaciones en los formatos de archivo de imagen soportados?

R3: Aspose.PSD soporta una variedad de formatos de archivo de imagen, incluyendo PSD, JPEG, PNG y más. Consulta la [documentation](https://reference.aspose.com/psd/java/) para obtener una lista completa.

### P4: ¿Cómo puedo obtener soporte para consultas relacionadas con Aspose.PSD?

R4: Visita el [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) para buscar ayuda de la comunidad o del equipo de soporte de Aspose.

### P5: ¿Hay una prueba gratuita disponible?

R5: Sí, puedes explorar Aspose.PSD con una prueba gratuita. Descárgala [here](https://releases.aspose.com/).

---

**Última actualización:** 2026-01-07  
**Probado con:** Aspose.PSD for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}