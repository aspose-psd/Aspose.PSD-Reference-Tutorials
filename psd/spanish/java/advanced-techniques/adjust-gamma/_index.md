---
title: Ajustar la gamma de una imagen con Aspose.PSD para Java
linktitle: Ajustar gamma de una imagen
second_title: API de Java Aspose.PSD
description: Aprenda a ajustar la gamma de la imagen sin esfuerzo usando Aspose.PSD para Java. Siga nuestra guía paso a paso para obtener resultados óptimos.
weight: 23
url: /es/java/advanced-techniques/adjust-gamma/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ajustar la gamma de una imagen con Aspose.PSD para Java

## Introducción

En el ámbito del procesamiento de imágenes, ajustar la gamma de una imagen es un paso crucial para mejorar su atractivo visual. Aspose.PSD para Java ofrece una poderosa solución para que los desarrolladores de Java manipulen sin esfuerzo la gamma de la imagen. En este tutorial, exploraremos cómo ajustar la gamma usando Aspose.PSD, desglosando cada paso para garantizar una implementación perfecta.

## Requisitos previos

Antes de sumergirse en el tutorial, asegúrese de tener configurados los siguientes requisitos previos:

1. Entorno de desarrollo Java: asegúrese de tener un entorno de desarrollo Java instalado en su sistema.
2.  Biblioteca Aspose.PSD: descargue e integre la biblioteca Aspose.PSD en su proyecto Java. Puedes encontrar los recursos necesarios en el[documentación](https://reference.aspose.com/psd/java/).
3. Imagen de muestra: prepare una imagen PSD de muestra que usará para aplicar el ajuste de gamma.

## Importar paquetes

Para iniciar el proceso, importe los paquetes necesarios en su proyecto Java. Esto prepara el escenario para utilizar las funcionalidades de Aspose.PSD sin problemas.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Paso 1: cargue la imagen

 Comience cargando la imagen PSD de muestra en una instancia del`RasterImage` clase. Esta es la base para ajustes gamma posteriores.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Cargue una imagen existente en una instancia de la clase RasterImage
Image image = Image.load(sourceFile);

// Objeto fundido de imagen a imagen rasterizada
RasterImage rasterImage = (RasterImage)image;

// Compruebe si RasterImage está en caché para un mejor rendimiento
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## Paso 2: ajustar gamma

 Ahora, ajuste la gamma de la imagen cargada usando el`adjustGamma` método. Ajuste los valores gamma según sus requisitos.

```java
// Ajustar la gama
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## Paso 3: crear opciones Tiff

 Crear una instancia de`TiffOptions` para la imagen resultante. Configure varias propiedades, como bits por muestra y opciones fotométricas, para adaptar la salida a sus especificaciones.

```java
// Cree una instancia de TiffOptions para la imagen resultante
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## Paso 4: guarde la imagen resultante

 Guarde la imagen manipulada en formato TIFF utilizando el formato previamente definido.`TiffOptions`.

```java
// Guarde la imagen resultante en formato TIFF
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## Conclusión

¡Felicidades! Ha ajustado con éxito la gamma de una imagen usando Aspose.PSD para Java. Este proceso permite a los desarrolladores mejorar la calidad de la imagen sin esfuerzo, contribuyendo a una experiencia de usuario visualmente atractiva.

## Preguntas frecuentes

### P1: ¿Dónde puedo encontrar la documentación de Aspose.PSD?

 A1: Puede acceder a la documentación en[https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/).

### P2: ¿Cómo descargo Aspose.PSD para Java?

 A2: Descargue la biblioteca desde[https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/).

### P3: ¿Dónde puedo comprar Aspose.PSD?

 A3: Visita[https://purchase.aspose.com/buy](https://purchase.aspose.com/buy) para comprar Aspose.PSD.

### P4: ¿Hay una prueba gratuita disponible?

 R4: Sí, puedes explorar una prueba gratuita en[https://releases.aspose.com/](https://releases.aspose.com/).

### P5: ¿Dónde puedo buscar soporte para Aspose.PSD?

 R5: Para obtener ayuda, visite el foro Aspose.PSD en[https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
