---
date: 2026-08-01
description: Aprenda cómo ajustar gamma en el procesamiento de imágenes Java con Aspose.PSD,
  convertir PSD a TIFF y corregir imágenes deslavadas en un tutorial conciso.
keywords:
- how to adjust gamma
- fix washed out image
- java image processing
- convert psd to tiff
- server side image processing
lastmod: 2026-08-01
linktitle: Ajustar gamma de una imagen
og_description: Aprenda cómo ajustar gamma en el procesamiento de imágenes Java usando
  Aspose.PSD – una biblioteca rápida del lado del servidor que corrige imágenes deslavadas
  y convierte PSD a TIFF en solo unas pocas líneas de código.
og_image_alt: 'Guide: Adjust gamma in Java images with Aspose.PSD, convert PSD to
  TIFF'
og_title: cómo ajustar gamma – procesamiento Java con Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  headline: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  type: TechArticle
- description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  name: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  steps:
  - name: '**Java Development Environment** – Java 8 or later installed.'
    text: '**Java Development Environment** – Java 8 or later installed.'
  - name: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
  - name: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
    text: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
  type: HowTo
- questions:
  - answer: Yes – the `adjustGamma` method accepts separate float values for red,
      green, and blue channels.
    question: Can I apply different gamma values to each colour channel?
  - answer: Absolutely. You can perform resizing, cropping, or colour corrections
      sequentially on the same `RasterImage` instance.
    question: Is it possible to chain multiple image adjustments before saving?
  - answer: Yes, each layer can be accessed and processed individually.
    question: Does Aspose.PSD support multi‑page PSD files?
  - answer: Aspose.PSD supports PNG, JPEG, BMP, and many other formats via their respective
      options classes.
    question: What format can I export to besides TIFF?
  - answer: Start with a moderate gamma (around 2.0) and preview the result; adjust
      downwards if the image looks too bright.
    question: How do I avoid a washed‑out image after gamma correction?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- adjust gamma
- Aspose.PSD
- Java image processing
- PSD to TIFF
- server side processing
title: Cómo ajustar gamma en el procesamiento de imágenes Java con Aspose.PSD
url: /es/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo ajustar gamma en el procesamiento de imágenes Java con Aspose.PSD

## Introducción

Si estás trabajando en **procesamiento de imágenes Java**, aprender **cómo ajustar gamma** es una técnica fundamental para mejorar el brillo y el contraste sin perder detalle. En este tutorial recorreremos cómo usar **Aspose.PSD for Java** para aplicar corrección gamma a un archivo PSD, **convertir PSD a TIFF**, y evitar una **imagen deslavada**. Verás por qué este enfoque es rápido, fiable y perfecto para pipelines de **procesamiento de imágenes del lado del servidor**.

## Respuestas rápidas
- **¿Qué hace la corrección gamma?** Remapea los valores de luminancia para hacer que las áreas oscuras sean más brillantes o las áreas brillantes más oscuras mientras se preserva el detalle general.  
- **¿Qué biblioteca maneja el procesamiento?** Aspose.PSD for Java proporciona un método dedicado `adjustGamma` para imágenes raster.  
- **¿Puedo convertir PSD a TIFF en el mismo flujo?** Sí – después del ajuste gamma puedes guardar la imagen directamente a TIFF usando `TiffOptions`.  
- **¿Necesito una licencia para desarrollo?** Una prueba gratuita funciona para pruebas; se requiere una licencia comercial para uso en producción.  
- **¿Qué versión de Java es compatible?** Aspose.PSD soporta Java 8 y posteriores.

## Qué es la corrección gamma en Java

La corrección gamma cambia la relación no lineal entre los valores de píxel codificados y el brillo mostrado. Al ajustar la curva gamma puedes **solucionar problemas de imagen deslavada** o realzar detalles en sombras sin sobreexponer los reflejos. Funciona aplicando una función de ley de potencia a cada píxel, lo que aclara los tonos oscuros y comprime los reflejos, resultando en una apariencia visual más natural.

## Por qué usar Aspose.PSD para la corrección gamma

Aspose.PSD es una **biblioteca de procesamiento de imágenes Java** que abstrae las complejidades del formato PSD. Soporta el procesamiento de archivos de hasta 2 GB, maneja más de 50 formatos de imagen diferentes, y ofrece una llamada simple `adjustGamma`, lo que lo hace ideal para **corrección gamma Java** y **convertir PSD a TIFF** en flujos de trabajo.

## Requisitos previos

1. **Entorno de desarrollo Java** – Java 8 o posterior instalado.  
2. **Biblioteca Aspose.PSD** – Descarga y agrega el JAR a tu proyecto. Consulta la [documentación](https://reference.aspose.com/psd/java/) oficial.  
3. **Imagen de ejemplo** – Un archivo PSD que deseas procesar (p.ej., `sample.psd`).  

## Importar paquetes

Antes de comenzar, importa los espacios de nombres esenciales que te dan acceso al manejo raster y a las opciones de formato de archivo.

## Paso 1: Cargar la imagen

La clase `RasterImage` representa los datos de píxel rasterizados de una capa PSD en memoria. Cargar la imagen una vez y almacenarla en caché reduce el consumo de memoria para ajustes posteriores.

## Paso 2: Ajustar gamma

Carga tu PSD con `new RasterImage("sample.psd")` y llama a `rasterImage.adjustGamma(2.0f)` — esa única línea aplica un gamma de 2.0 en todos los canales de color, aclarando sombras mientras mantiene los reflejos intactos. Puedes pasar valores separados para rojo, verde y azul si se requieren ajustes específicos por canal.

## Paso 3: Crear TiffOptions

`TiffOptions` te permite controlar la compresión, bits por muestra y otras configuraciones específicas de TIFF. Configurar una muestra de 8 bits (`{8,8,8}`) mantiene el tamaño del archivo TIFF razonable mientras preserva la fidelidad del color.

## Paso 4: Guardar la imagen resultante

Llama a `rasterImage.save("output.tif", tiffOptions)` para escribir la imagen procesada en disco. Después de guardar, puedes enviar el TIFF a sistemas posteriores como servicios de impresión o APIs web.

## Casos de uso comunes

- **Flujos de trabajo de gráficos automatizados** – Ajustar gamma al vuelo antes de generar miniaturas.  
- **Herramientas de conversión por lotes** – Convertir grandes archivos PSD a TIFF mientras se normaliza el brillo.  
- **Servicios web** – Exponer un endpoint que reciba un PSD, aplique corrección gamma y devuelva un TIFF para el consumo del cliente.

## Problemas comunes y soluciones

| Problema | Por qué ocurre | Cómo arreglar |
|----------|----------------|---------------|
| **La imagen aparece deslavada** | Valor de gamma demasiado alto (p.ej., > 2.5) | Reducir el factor gamma a un valor entre 1.8 y 2.2. |
| **`rasterImage.isCached()` devuelve false** | Imagen aún no cargada en memoria | Llamar a `rasterImage.cacheData()` antes de ajustar gamma. |
| **El tamaño del archivo TIFF es grande** | Bits por muestra configurados a 16‑bit | Usar una muestra de 8‑bit (`{8,8,8}`) como se muestra en el ejemplo. |

## Preguntas frecuentes

**P: ¿Puedo aplicar diferentes valores gamma a cada canal de color?**  
R: Sí – el método `adjustGamma` acepta valores float separados para los canales rojo, verde y azul.

**P: ¿Es posible encadenar múltiples ajustes de imagen antes de guardar?**  
R: Absolutamente. Puedes realizar redimensionado, recorte o correcciones de color secuencialmente en la misma instancia `RasterImage`.

**P: ¿Aspose.PSD soporta archivos PSD multipágina?**  
R: Sí, cada capa puede ser accedida y procesada individualmente.

**P: ¿A qué formato puedo exportar además de TIFF?**  
R: Aspose.PSD soporta PNG, JPEG, BMP y muchos otros formatos a través de sus respectivas clases de opciones.

**P: ¿Cómo evito una imagen deslavada después de la corrección gamma?**  
R: Comienza con un gamma moderado (alrededor de 2.0) y previsualiza el resultado; reduce el valor si la imagen parece demasiado brillante.

## Conclusión

¡Felicidades! Has aprendido con éxito **cómo ajustar gamma** en un flujo de trabajo de **procesamiento de imágenes Java**, convertido un PSD a TIFF y evitado problemas comunes como una **imagen deslavada**. Este patrón te brinda un control fino sobre el brillo y el contraste, haciéndolo ideal para flujos de trabajo de gráficos automatizados, servicios web o utilidades de escritorio.

---

**Última actualización:** 2026-08-01  
**Probado con:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriales relacionados

- [Tutorial de procesamiento de imágenes Java - Ajustar brillo de una imagen con Aspose.PSD para Java](/psd/java/advanced-techniques/adjust-brightness/)
- [Cómo convertir PSD a TIFF y ajustar contraste con Aspose.PSD para Java](/psd/java/advanced-techniques/adjust-contrast/)
- [Convertir PSD a imagen en Java – Aplicar capas de ajuste con Aspose.PSD](/psd/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);

// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```