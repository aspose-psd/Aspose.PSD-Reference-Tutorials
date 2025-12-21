---
date: 2025-12-21
description: Aprende cómo realizar procesamiento de imágenes en Java ajustando la
  gamma de la imagen con Aspose.PSD. Guía paso a paso para convertir PSD a TIFF y
  aplicar corrección de gamma.
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: Procesamiento de imágenes en Java – Ajustar gamma con Aspose.PSD
url: /es/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Procesamiento de Imágenes en Java – Ajuste de Gamma con Aspose.PSD

## Introducción

Si trabajas con **procesamiento de imágenes en java**, ajustar la gamma de una imagen es una técnica fundamental para mejorar el brillo y el contraste sin perder detalle. En este tutorial recorreremos cómo usar **Aspose.PSD for Java** para aplicar corrección de gamma a un archivo PSD y luego exportar el resultado como una imagen TIFF. Verás por qué este enfoque es rápido, fiable y perfecto para canalizaciones de imágenes del lado del servidor.

## Respuestas rápidas
- **¿Qué hace la corrección de gamma?** Remapea los valores de luminancia para hacer que las áreas oscuras sean más claras o las áreas claras más oscuras, preservando el detalle general.  
- **¿Qué biblioteca maneja el procesamiento?** Aspose.PSD for Java proporciona un método dedicado `adjustGamma` para imágenes raster.  
- **¿Puedo convertir PSD a TIFF en el mismo flujo?** Sí – después del ajuste de gamma puedes guardar la imagen directamente en TIFF usando `TiffOptions`.  
- **¿Necesito una licencia para desarrollo?** Una prueba gratuita funciona para pruebas; se requiere una licencia comercial para uso en producción.  
- **¿Qué versión de Java es compatible?** Aspose.PSD soporta Java 8 y posteriores.

## ¿Qué es el procesamiento de imágenes en java?

El procesamiento de imágenes en Java se refiere a la manipulación, análisis y transformación de datos visuales mediante bibliotecas Java. Las tareas incluyen redimensionado, filtrado, corrección de color y conversión de formatos, todo lo cual puede automatizarse en aplicaciones de escritorio o web.

## ¿Por qué usar Aspose.PSD para la corrección de gamma?

Aspose.PSD ofrece una API de alto nivel que abstrae la complejidad del formato PSD, permitiéndote centrarte en los ajustes reales de la imagen. Gestiona el almacenamiento en caché, los perfiles de color y proporciona una llamada sencilla `adjustGamma`, lo que lo hace ideal para **corrección de gamma de imágenes** y flujos de trabajo **convertir psd a tiff**.

## Requisitos previos

Antes de sumergirte en el tutorial, asegúrate de tener configurados los siguientes requisitos:

1. **Entorno de desarrollo Java** – Asegúrate de tener un entorno de desarrollo Java instalado en tu sistema.  
2. **Biblioteca Aspose.PSD** – Descarga e integra la biblioteca Aspose.PSD en tu proyecto Java. Puedes encontrar los recursos necesarios en la [documentación](https://reference.aspose.com/psd/java/).  
3. **Imagen de muestra** – Prepara una imagen PSD de muestra que usarás para aplicar el ajuste de gamma.

## Importar paquetes

Para iniciar el proceso, importa los paquetes requeridos en tu proyecto Java. Esto prepara el escenario para utilizar las funcionalidades de Aspose.PSD sin problemas.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Paso 1: Cargar la imagen

Comienza cargando la imagen PSD de muestra en una instancia de la clase `RasterImage`. Esta es la base para los ajustes de gamma posteriores.

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

## Paso 2: Ajustar Gamma

Ahora, ajusta la gamma de la imagen cargada usando el método `adjustGamma`. Afina los valores de gamma según tus requisitos.

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## Paso 3: Crear TiffOptions

Crea una instancia de `TiffOptions` para la imagen resultante. Configura varias propiedades, como bits por muestra y opciones fotométricas, para adaptar la salida a tus especificaciones.

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## Paso 4: Guardar la imagen resultante

Guarda la imagen manipulada en formato TIFF usando los `TiffOptions` definidos previamente.

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## Problemas comunes y soluciones

| Problema | Por qué ocurre | Cómo solucionarlo |
|----------|----------------|-------------------|
| **La imagen se ve deslavada** | Valor de gamma demasiado alto (p. ej., > 2.5) | Reduce el factor gamma a un valor entre 1.8 y 2.2. |
| **`rasterImage.isCached()` devuelve false** | La imagen aún no se ha cargado en memoria | Llama a `rasterImage.cacheData()` antes de ajustar la gamma. |
| **El tamaño del archivo TIFF es grande** | Bits por muestra configurados a 16 bits | Usa una muestra de 8 bits (`{8,8,8}`) como se muestra en el ejemplo. |

## Preguntas frecuentes

**P: ¿Puedo aplicar diferentes valores de gamma a cada canal de color?**  
R: Sí – el método `adjustGamma` acepta valores float separados para los canales rojo, verde y azul.

**P: ¿Es posible encadenar varios ajustes de imagen antes de guardar?**  
R: Absolutamente. Puedes realizar redimensionado, recorte o correcciones de color de forma secuencial en la misma instancia de `RasterImage`.

**P: ¿Aspose.PSD soporta archivos PSD multipágina?**  
R: Sí, cada capa puede accederse y procesarse individualmente.

**P: ¿A qué formato puedo exportar además de TIFF?**  
R: Aspose.PSD soporta PNG, JPEG, BMP y muchos otros formatos mediante sus respectivas clases de opciones.

## Conclusión

¡Felicidades! Has realizado con éxito **procesamiento de imágenes en java** ajustando la gamma de un archivo PSD y exportándolo como una imagen TIFF usando Aspose.PSD for Java. Este flujo de trabajo te brinda un control granular sobre el brillo y el contraste de la imagen, lo que lo hace ideal para canalizaciones gráficas automatizadas, servicios web o utilidades de escritorio.

---

**Última actualización:** 2025-12-21  
**Probado con:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

## Preguntas frecuentes

### P1: ¿Dónde puedo encontrar la documentación de Aspose.PSD?

R1: Puedes acceder a la documentación en [https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/).

### P2: ¿Cómo descargo Aspose.PSD para Java?

R2: Descarga la biblioteca desde [https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/).

### P3: ¿Dónde puedo comprar Aspose.PSD?

R3: Visita [https://purchase.aspose.com/buy](https://purchase.aspose.com/buy) para comprar Aspose.PSD.

### P4: ¿Hay una prueba gratuita disponible?

R4: Sí, puedes explorar una prueba gratuita en [https://releases.aspose.com/](https://releases.aspose.com/).

### P5: ¿Dónde puedo obtener soporte para Aspose.PSD?

R5: Para soporte, visita el foro de Aspose.PSD en [https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34).

---