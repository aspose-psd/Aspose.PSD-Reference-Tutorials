---
date: 2025-12-19
description: Aprende a ajustar el brillo de una imagen usando Aspose.PSD para Java.
  Este tutorial de manipulación de imágenes en Java ofrece una guía paso a paso.
linktitle: Adjust Brightness of an Image
second_title: Aspose.PSD Java API
title: Cómo ajustar el brillo de una imagen con Aspose.PSD para Java
url: /es/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ajustar el Brillo de una Imagen con Aspose.PSD para Java

## Introducción

Si necesitas **aprender cómo ajustar el brillo** de una imagen directamente desde código Java, estás en el lugar correcto. Ajustar el brillo es una tarea frecuente para diseñadores gráficos, fotógrafos y cualquier persona que construya pipelines de procesamiento de imágenes. En este **tutorial de manipulación de imágenes en java** recorreremos el flujo de trabajo completo—cargar un PSD/TIFF, aplicar un desplazamiento de brillo y guardar el resultado—usando la biblioteca Aspose.PSD para Java.

## Respuestas Rápidas
- **¿Qué biblioteca maneja el brillo?** Aspose.PSD for Java  
- **¿Qué método cambia el brillo?** `RasterImage.adjustBrightness()`  
- **¿Puedo trabajar con archivos PSD y TIFF?** Sí, la API soporta ambos formatos.  
- **¿Necesito una licencia para producción?** Se requiere una licencia comercial para uso que no sea de evaluación.  
- **¿Cuánto tiempo lleva la implementación?** Normalmente menos de 10 minutos para un ajuste básico.

## ¿Qué es el Ajuste de Brillo de Imagen?

El ajuste de brillo de imagen cambia la luminosidad general de cada píxel en una imagen. Aumentar el brillo hace que las áreas oscuras se vuelvan más claras, mientras que disminuirlo oscurece toda la foto. Esta operación es útil para corregir fotos subexpuestas, preparar recursos para impresión o crear efectos visuales en aplicaciones.

## ¿Por qué usar Aspose.PSD para Java?

- **Soporte completo de formatos** – PSD, TIFF, JPEG, PNG y más.  
- **Sin dependencias nativas externas** – puro Java, fácil de integrar.  
- **Caché de alto rendimiento** – los datos raster pueden almacenarse en caché para operaciones repetidas más rápidas.  
- **API rica** – métodos para corrección de color, capas, máscaras y otras ediciones avanzadas.

## Requisitos Previos

Antes de sumergirte en el tutorial, asegúrate de contar con los siguientes requisitos:

- Biblioteca Aspose.PSD para Java: Descarga e instala la biblioteca desde la [documentación de Aspose.PSD para Java](https://reference.aspose.com/psd/java/).

## Importar Paquetes

Para comenzar, importa los paquetes necesarios en tu proyecto Java. En este ejemplo, usaremos lo siguiente:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Ahora, desglosaremos el proceso de ajustar el brillo de una imagen en pasos simples:

## Cómo Ajustar el Brillo Usando Aspose.PSD

### Paso 1: Cargar la Imagen

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage) image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

En este paso, cargamos la imagen objetivo y la convertimos a un `RasterImage` para su posterior procesamiento.

### Paso 2: Ajustar el Brillo

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

Aquí, usamos el método `adjustBrightness` para modificar el brillo de la imagen. En este ejemplo, disminuimos el brillo en 50 unidades, pero puedes personalizar este valor según tus requisitos.

### Paso 3: Configurar TiffOptions

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

Configura los `TiffOptions` para guardar la imagen ajustada. Ajusta las propiedades `bitsPerSample` y `photometric` según tus necesidades específicas.

### Paso 4: Guardar la Imagen Resultante

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

Finalmente, guarda la imagen modificada usando los `TiffOptions` especificados.

## Problemas Comunes y Soluciones

| Problema | Razón | Solución |
|----------|-------|----------|
| **`ClassCastException` al convertir Image** | El archivo no es una imagen raster (p.ej., un PSD vectorial). | Verifica el formato del archivo fuente o usa `image instanceof RasterImage` antes de convertir. |
| **El cambio de brillo no tiene efecto** | La imagen no se almacenó en caché antes del ajuste. | Llama a `rasterImage.cacheData()` como se muestra en el Paso 1. |
| **El archivo guardado parece corrupto** | Configuración incorrecta de `TiffOptions`. | Asegúrate de que `bitsPerSample` coincida con la profundidad de la imagen fuente (usualmente 8 bits por canal). |

## Preguntas Frecuentes

### Q1: ¿Puedo ajustar el brillo en otros formatos de imagen además de PSD?

**A1:** Sí, Aspose.PSD para Java soporta varios formatos de imagen como JPEG, PNG y TIFF.

### Q2: ¿Cómo puedo manejar errores durante el proceso de ajuste de la imagen?

**A2:** Puedes implementar manejo de errores usando bloques try‑catch para gestionar excepciones que puedan ocurrir.

### Q3: ¿Existe un límite para el rango de ajuste de brillo?

**A3:** El rango de ajuste depende del contenido y formato de la imagen, pero Aspose.PSD brinda flexibilidad en la personalización.

### Q4: ¿Puedo usar Aspose.PSD para Java en proyectos comerciales?

**A4:** Sí, Aspose.PSD para Java es una biblioteca comercial, y puedes obtener una licencia desde [aquí](https://purchase.aspose.com/buy).

### Q5: ¿Hay una prueba gratuita disponible para Aspose.PSD para Java?

**A5:** Sí, puedes explorar la biblioteca con una prueba gratuita desde [aquí](https://releases.aspose.com/).

### Q6: ¿El método `adjustBrightness` afecta la visibilidad de capas?

**A6:** El método actúa sobre la imagen compuesta rasterizada, por lo que la visibilidad de capas se respeta durante la rasterización.

### Q7: ¿Puedo encadenar múltiples ajustes (p.ej., contraste, saturación) juntos?

**A7:** Absolutamente. Después de ajustar el brillo, puedes llamar a `adjustContrast`, `adjustSaturation`, etc., en la misma instancia de `RasterImage`.

---

**Última actualización:** 2025-12-19  
**Probado con:** Aspose.PSD for Java 24.12 (última disponible al momento de escribir)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}