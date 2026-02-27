---
date: 2026-02-27
description: Aprende cómo ajustar la gamma en el procesamiento de imágenes en Java
  con Aspose.PSD, convertir PSD a TIFF y corregir imágenes deslavadas en un tutorial
  conciso.
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: Cómo ajustar la gamma en el procesamiento de imágenes Java con Aspose.PSD
url: /es/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo ajustar gamma en el procesamiento de imágenes Java con Aspose.PSD

## Introducción

Si trabajas en **java image processing**, aprender **how to adjust gamma** es una técnica fundamental para mejorar el brillo y el contraste sin perder detalle. En este tutorial recorreremos cómo usar **Aspose.PSD for Java** para aplicar corrección gamma a un archivo PSD, **convert PSD to TIFF**, y evitar una **washed‑out image**. Verás por qué este enfoque es rápido, fiable y perfecto para canalizaciones de imágenes del lado del servidor.

## Respuestas rápidas
- **¿Qué hace la corrección gamma?** Remapea los valores de luminancia para hacer que las áreas oscuras sean más claras o las áreas claras más oscuras mientras preserva el detalle general.  
- **¿Qué biblioteca maneja el procesamiento?** Aspose.PSD for Java proporciona un método dedicado `adjustGamma` para imágenes raster.  
- **¿Puedo convertir PSD a TIFF en el mismo flujo?** Sí – después del ajuste gamma puedes guardar la imagen directamente en TIFF usando `TiffOptions`.  
- **¿Necesito una licencia para desarrollo?** Una prueba gratuita funciona para pruebas; se requiere una licencia comercial para uso en producción.  
- **¿Qué versión de Java es compatible?** Aspose.PSD soporta Java 8 y posteriores.

## Cómo ajustar gamma en el procesamiento de imágenes Java
Ajustar gamma es una parte esencial de cualquier **java image processing tutorial** que trate el brillo o el contraste. A continuación desglosamos los pasos, explicamos por qué cada línea es importante y te mostramos cómo integrar el proceso en tu base de código existente.

## ¿Qué es la corrección gamma en Java?
La corrección gamma cambia la relación no lineal entre los valores de píxel codificados y el brillo mostrado. Al modificar la curva gamma puedes **fix washed out image** problemas o realzar detalles en sombras sin sobreexponer los reflejos.

## ¿Por qué usar Aspose.PSD para la corrección gamma?
Aspose.PSD actúa como una poderosa **java image processing library** que abstrae las complejidades del formato PSD. Maneja perfiles de color, caché y proporciona una llamada simple `adjustGamma`, lo que la hace ideal para **java gamma correction** y flujos de **convert PSD to TIFF**.

## Requisitos previos

1. **Entorno de desarrollo Java** – Java 8 o posterior instalado.  
2. **Biblioteca Aspose.PSD** – Descarga y agrega el JAR a tu proyecto. Consulta la [documentation](https://reference.aspose.com/psd/java/).  
3. **Imagen de muestra** – Un archivo PSD que deseas procesar (p. ej., `sample.psd`).  

## Importar paquetes

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

// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

**Consejo profesional:** Cachéar los datos raster una vez reduce el consumo de memoria cuando aplicas varios ajustes consecutivos.

## Paso 2: Ajustar gamma

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

Puedes pasar valores diferentes para los canales rojo, verde y azul si necesitas ajustes específicos por canal.

## Paso 3: Crear TiffOptions

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

Establecer una muestra de 8 bits (`{8,8,8}`) mantiene el tamaño del archivo TIFF razonable mientras preserva la fidelidad del color.

## Paso 4: Guardar la imagen resultante

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

Después de guardar, puedes enviar el TIFF a sistemas posteriores como servicios de impresión o APIs web.

## Casos de uso comunes

- **Canalizaciones gráficas automatizadas** – Ajustar gamma al vuelo antes de generar miniaturas.  
- **Herramientas de conversión por lotes** – Convertir grandes archivos PSD a TIFF mientras normalizas el brillo.  
- **Servicios web** – Exponer un endpoint que reciba un PSD, aplique corrección gamma y devuelva un TIFF para el cliente.

## Problemas comunes y soluciones

| Problema | Por qué ocurre | Cómo solucionarlo |
|----------|----------------|-------------------|
| **La imagen aparece washed out** | Valor gamma demasiado alto (p. ej., > 2.5) | Reduce el factor gamma a un valor entre 1.8 y 2.2. |
| **`rasterImage.isCached()` devuelve false** | Imagen aún no cargada en memoria | Llama a `rasterImage.cacheData()` antes de ajustar gamma. |
| **El tamaño del archivo TIFF es grande** | Bits por muestra configurados a 16 bits | Usa una muestra de 8 bits (`{8,8,8}`) como se muestra en el ejemplo. |

## Preguntas frecuentes

**P: ¿Puedo aplicar valores gamma diferentes a cada canal de color?**  
R: Sí – el método `adjustGamma` acepta valores float separados para los canales rojo, verde y azul.

**P: ¿Es posible encadenar varios ajustes de imagen antes de guardar?**  
R: Absolutamente. Puedes realizar redimensionado, recorte o correcciones de color secuencialmente sobre la misma instancia `RasterImage`.

**P: ¿Aspose.PSD soporta archivos PSD multipágina?**  
R: Sí, cada capa puede ser accedida y procesada individualmente.

**P: ¿A qué formato puedo exportar además de TIFF?**  
R: Aspose.PSD soporta PNG, JPEG, BMP y muchos otros formatos mediante sus respectivas clases de opciones.

**P: ¿Cómo evito una washed‑out image después de la corrección gamma?**  
R: Comienza con un gamma moderado (alrededor de 2.0) y previsualiza el resultado; disminuye el valor si la imagen parece demasiado brillante.

## Conclusión

¡Felicidades! Has aprendido con éxito **how to adjust gamma** en un flujo de **java image processing**, convertido un PSD a TIFF y evitado problemas comunes como una **washed‑out image**. Este patrón te brinda un control granular sobre el brillo y el contraste, lo que lo hace ideal para canalizaciones gráficas automatizadas, servicios web o utilidades de escritorio.

---

**Última actualización:** 2026-02-27  
**Probado con:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}