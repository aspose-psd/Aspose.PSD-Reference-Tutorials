---
date: 2026-01-07
description: Aprende paso a paso técnicas de filtrado para aplicar filtros Mediana
  y Wiener usando Aspose.PSD para Java, y convierte PSD a GIF de manera eficiente.
linktitle: Apply Median and Wiener Filters
second_title: Aspose.PSD Java API
title: 'Filtro paso a paso: aplicar filtros de mediana y Wiener (Java)'
url: /es/java/image-processing/apply-median-wiener-filters/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Filtro paso a paso: aplicar filtros Mediana y Wiener (Java)

## Introducción

Si buscas un flujo de trabajo de **filtro paso a paso** para limpiar imágenes ruidosas en Java, has llegado al lugar correcto. Aspose.PSD para Java facilita la aplicación de los filtros Mediana y Wiener, y además te permite **convertir PSD a GIF** después del procesamiento. En este tutorial recorreremos todo lo que necesitas—desde la configuración de la biblioteca hasta el guardado del resultado filtrado—para que puedas integrar una denoising de imágenes de alta calidad en tus aplicaciones con confianza.

## Respuestas rápidas
- **¿Qué hace el filtro Mediana?** Reduce el ruido de sal y pimienta mientras preserva los bordes.  
- **¿Cuándo debo usar el filtro Wiener?** Para reducción de ruido adaptativa que considera la varianza local de la imagen.  
- **¿Necesito una licencia para ejecutar el código?** Una prueba gratuita funciona para desarrollo; se requiere una licencia comercial para producción.  
- **¿Puedo guardar la salida como GIF?** Sí—Aspose.PSD le permite **convertir PSD a GIF** en un solo paso.  
- **¿Cuánto tiempo lleva la implementación?** Normalmente menos de 10 minutos para una configuración básica.

## ¿Qué es un filtro paso a paso?

Un enfoque de *filtro paso a paso* divide el procesamiento de imágenes en etapas claras y manejables—cargar la imagen, configurar las opciones del filtro, aplicar el filtro y, finalmente, guardar el resultado. Este flujo metódico te ayuda a depurar cada parte, reutilizar código y adaptar el proceso a diferentes formatos de imagen.

## ¿Por qué usar Aspose.PSD para Java?

- **Amplio soporte de formatos** – Maneja PSD, PNG, JPEG, GIF y más.  
- **Sin dependencias externas** – Java puro, fácil de incrustar en cualquier proyecto.  
- **Opciones de filtro integradas** – Mediana, Wiener y otros filtros avanzados están listos de inmediato.  
- **Conversión con un clic** – Exporta directamente a GIF, PNG o JPEG después del procesamiento.

## Requisitos previos

Antes de comenzar, asegúrate de tener:

1. **Biblioteca Aspose.PSD para Java** – Descargue e instale la biblioteca desde [aquí](https://releases.aspose.com/psd/java/).  
2. **Entorno de desarrollo Java** – JDK 8+ y un IDE o herramienta de compilación (Maven/Gradle) configurados en su máquina.

## Importar paquetes

Comience importando las clases necesarias que le dan acceso al manejo de imágenes y a las opciones de filtro.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.MedianFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

## Filtro paso a paso: cómo aplicar el filtro Mediana

### Paso 1: Cargar la imagen

Primero, indique la API al archivo PSD que desea limpiar.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load the source image
Image image = Image.load(sourceFile);
```

### Paso 2: Convertir la imagen a RasterImage

El filtro funciona sobre datos raster, por lo que convertimos el `Image` genérico a un `RasterImage`.

```java
// Cast the image into RasterImage
RasterImage rasterImage = (RasterImage)image;
if (rasterImage == null) {
    return;
}
```

### Paso 3: Crear una instancia de MedianFilterOptions

Configure el tamaño del kernel mediano. Un tamaño de **4** funciona bien para ruido moderado.

```java
// Create an instance of MedianFilterOptions class and set the filter size
MedianFilterOptions options = new MedianFilterOptions(4);
```

### Paso 4: Aplicar el filtro Mediana

Ahora aplique el filtro a todo el contorno de la imagen.

```java
// Apply MedianFilterOptions filter to RasterImage object
rasterImage.filter(image.getBounds(), options);
```

### Paso 5: Guardar la imagen resultante (Convertir PSD a GIF)

Después del filtrado, guardaremos la salida como GIF—demostrando la capacidad de **convertir PSD a GIF**.

```java
String destName = dataDir + "median_test_denoise_out.gif";
// Save the resultant image as a GIF
image.save(destName, new GifOptions());
```

Al seguir estos pasos has aplicado exitosamente un filtro Mediana y exportado la imagen limpiada como GIF.

## Aplicar filtro Wiener (extensión opcional)

Si tu proyecto requiere reducción de ruido adaptativa, puedes reemplazar el filtro Mediana por un filtro Wiener. La estructura del código es idéntica; solo necesitas importar `WienerFilterOptions` e instanciarlo con el radio deseado.

> **Consejo profesional:** Experimenta con diferentes tamaños de kernel para ambos filtros y encuentra el punto óptimo entre eliminación de ruido y preservación de detalles.

## Problemas comunes y solución de problemas

| Síntoma | Causa probable | Solución |
|---------|----------------|----------|
| `ClassCastException` al convertir a `RasterImage` | El archivo de entrada no es un PSD compatible con raster | Verifique que el PSD contenga capas raster o convierta las capas a raster primero |
| El GIF de salida está en blanco | La ruta de destino es incorrecta o la carpeta no tiene permiso de escritura | Asegúrese de que `dataDir` apunte a un directorio existente y con permisos de escritura |
| El filtro parece no tener efecto | El tamaño del kernel es demasiado pequeño para el nivel de ruido | Aumente el tamaño del filtro (p. ej., `new MedianFilterOptions(6)`) |

## Preguntas frecuentes

**Q1: ¿Puedo aplicar estos filtros a imágenes de cualquier formato?**  
A1: Sí, Aspose.PSD soporta una amplia gama de formatos de imagen, lo que lo hace versátil para diversos proyectos.

**Q2: ¿Hay una prueba gratuita disponible para Aspose.PSD para Java?**  
A2: Sí, puedes obtener una prueba gratuita [aquí](https://releases.aspose.com/).

**Q3: ¿Cómo obtengo soporte para Aspose.PSD para Java?**  
A3: Visita el [foro de Aspose.PSD](https://forum.aspose.com/c/psd/34) para soporte comunitario.

**Q4: ¿Dónde puedo encontrar la documentación para Aspose.PSD para Java?**  
A4: Consulta la documentación [aquí](https://reference.aspose.com/psd/java/).

**Q5: ¿Cómo puedo comprar Aspose.PSD para Java?**  
A5: Puedes adquirir el producto [aquí](https://purchase.aspose.com/buy).

## Conclusión

En esta guía demostramos un proceso de **filtro paso a paso** para aplicar filtros Mediana (y opcionalmente Wiener) usando Aspose.PSD para Java, y mostramos cómo **convertir PSD a GIF** después de la denoising. Con estos bloques de construcción puedes integrar pipelines de procesamiento de imágenes robustos en cualquier aplicación Java—ya sea que estés limpiando fotos, preparando recursos para la web o automatizando conversiones por lotes.

---

**Última actualización:** 2026-01-07  
**Probado con:** Aspose.PSD para Java 24.12 (última versión al momento de escribir)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}