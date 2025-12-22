---
date: 2025-12-21
description: Aprende a ajustar el contraste de imágenes usando Aspose.PSD para Java,
  una biblioteca líder de manipulación de imágenes en Java, y convierte PSD a TIFF
  de manera eficiente.
linktitle: Adjust Contrast of an Image
second_title: Aspose.PSD Java API
title: Cómo ajustar el contraste de una imagen con Aspose.PSD para Java
url: /es/java/advanced-techniques/adjust-contrast/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo ajustar el contraste de una imagen con Aspose.PSD para Java

## Introducción

Si buscas **cómo ajustar el contraste** en tus proyectos Java, has llegado al lugar correcto. Aspose.PSD para Java es una potente **biblioteca de manipulación de imágenes java** que te permite afinar propiedades de la imagen como contraste, brillo y más. En este tutorial recorreremos paso a paso los pasos exactos para aumentar el contraste de un archivo PSD y luego **convertir PSD a TIFF** para flujos de trabajo posteriores.

## Respuestas rápidas
- **¿Qué significa “ajustar contraste”?** Cambia la diferencia entre los píxeles más oscuros y los más claros, haciendo que los detalles resalten.
- **¿Qué biblioteca lo maneja?** Aspose.PSD para Java – un conjunto de herramientas de procesamiento de imágenes completo.
- **¿Necesito una licencia?** Una licencia temporal funciona para pruebas; se requiere una licencia completa para producción.
- **¿Puedo guardar el resultado como TIFF?** Sí, usaremos `TiffOptions` para exportar la imagen procesada.
- **¿Cuánto tiempo tarda el código en ejecutarse?** Normalmente menos de un segundo para archivos PSD de tamaño estándar.

## ¿Qué es el ajuste de contraste?
El ajuste de contraste modifica el rango tonal de una imagen, amplificando la distinción entre áreas claras y oscuras. Esto es especialmente útil cuando las imágenes se ven planas después de escanearlas o al preparar gráficos para impresión.

## ¿Por qué usar Aspose.PSD para Java?
- **Amplio soporte de formatos** – abre, edita y guarda PSD, TIFF, PNG, JPEG y muchos más.
- **Alto rendimiento** – la caché y las optimizaciones de imágenes rasterizadas reducen el consumo de memoria.
- **API sencilla** – llamadas de método único como `adjustContrast` hacen que el código sea legible.

## Requisitos previos

Antes de comenzar, asegúrate de tener:

- Conocimientos básicos de programación en Java.
- La biblioteca Aspose.PSD para Java instalada. Puedes descargarla [aquí](https://releases.aspose.com/psd/java/).

## Importar paquetes

Agrega los imports necesarios a tu clase Java:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Paso 1: Cargar la imagen

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

Cargamos el archivo PSD de origen (`sample.psd`) en un objeto `Image`, que sirve como punto de entrada para todo el procesamiento posterior.

## Paso 2: Convertir a RasterImage y almacenar en caché los datos

```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

Convertir a `RasterImage` nos brinda acceso a operaciones a nivel de píxel. La caché mejora el rendimiento, especialmente para archivos grandes.

## Cómo ajustar el contraste de una imagen

```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

El método `adjustContrast` recibe un entero que representa el cambio en porcentaje. En este ejemplo aumentamos el contraste en **50 %**.

## Convertir PSD a TIFF usando Aspose.PSD

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Save the resultant image to TIFF format
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

Aquí configuramos `TiffOptions` (bits por muestra, interpretación fotométrica) y escribimos la imagen con contraste mejorado a un archivo TIFF.

## Problemas comunes y soluciones
- **Imagen no almacenada en caché:** Siempre llama a `cacheData()` para PSD grandes y evita `OutOfMemoryError`.
- **Cambio de color inesperado:** Verifica que `setPhotometric` coincida con tu espacio de color objetivo (RGB vs. CMYK).
- **Archivo no encontrado:** Asegúrate de que `dataDir` apunte a la carpeta correcta y que el nombre del archivo esté escrito correctamente.

## Preguntas frecuentes

### Q1: ¿Es Aspose.PSD compatible con diferentes formatos de imagen?

A1: Sí, Aspose.PSD admite varios formatos de imagen, proporcionando flexibilidad en tus proyectos.

### Q2: ¿Cómo puedo obtener una licencia temporal para Aspose.PSD?

A2: Puedes obtener una licencia temporal [aquí](https://purchase.aspose.com/temporary-license/).

### Q3: ¿Dónde puedo encontrar la documentación de Aspose.PSD?

A3: La documentación está disponible [aquí](https://reference.aspose.com/psd/java/).

### Q4: ¿Qué opciones de soporte están disponibles para Aspose.PSD?

A4: Para soporte, visita el [foro de Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Q5: ¿Puedo comprar Aspose.PSD?

A5: Sí, puedes adquirir Aspose.PSD [aquí](https://purchase.aspose.com/buy).

## Conclusión

Ahora sabes **cómo ajustar el contraste** de una imagen PSD usando Aspose.PSD para Java y cómo **convertir PSD a TIFF** para procesamiento adicional. Estos pasos te brindan un control granular sobre la calidad de la imagen mientras mantienes el código limpio y mantenible. Siéntete libre de experimentar con otros métodos de ajuste de imagen como `adjustBrightness` o `adjustGamma` para adaptarlos a tus necesidades específicas.

---

**Última actualización:** 2025-12-21  
**Probado con:** Aspose.PSD para Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}