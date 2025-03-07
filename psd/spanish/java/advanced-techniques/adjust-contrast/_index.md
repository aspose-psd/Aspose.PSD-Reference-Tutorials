---
title: Ajustar el contraste de una imagen con Aspose.PSD para Java
linktitle: Ajustar el contraste de una imagen
second_title: API de Java Aspose.PSD
description: Explore el mundo del ajuste de contraste de imágenes en Java con Aspose.PSD. Siga nuestra guía paso a paso para una manipulación de imágenes perfecta.
weight: 22
url: /es/java/advanced-techniques/adjust-contrast/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ajustar el contraste de una imagen con Aspose.PSD para Java

## Introducción

En el ámbito del procesamiento de imágenes con Java, Aspose.PSD destaca como una poderosa herramienta. Entre sus innumerables funciones, el ajuste del contraste de la imagen es un requisito común. Este tutorial lo guiará a través del proceso de ajustar el contraste de la imagen usando Aspose.PSD para Java. Si eres un desarrollador experimentado o estás empezando, esta guía te ayudará a dominar este aspecto esencial de la manipulación de imágenes.

## Requisitos previos

Antes de sumergirse en el tutorial, asegúrese de cumplir con los siguientes requisitos previos:

- Conocimientos básicos de programación Java.
-  Aspose.PSD para la biblioteca Java instalada. Puedes descargarlo[aquí](https://releases.aspose.com/psd/java/).

## Importar paquetes

Para comenzar, necesita importar los paquetes necesarios a su proyecto Java. Agregue las siguientes líneas a su código:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Paso 1: cargue la imagen

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Cargue una imagen existente en una instancia de la clase RasterImage
Image image = Image.load(sourceFile);
```

 En este paso, cargamos la imagen de muestra ("sample.psd") usando el`Image.load` método.

## Paso 2: Transmitir a RasterImage y almacenar datos en caché

```java
// Objeto fundido de imagen a imagen rasterizada
RasterImage rasterImage = (RasterImage)image;

// Compruebe si RasterImage está almacenado en caché y Cache RasterImage para obtener un mejor rendimiento
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 Aquí, lanzamos el genérico.`Image` objetar a un`RasterImage` para un procesamiento específico. El almacenamiento en caché de los datos de la imagen mejora el rendimiento.

## Paso 3: ajustar el contraste

```java
// Ajustar el contraste
rasterImage.adjustContrast(50);
```

 El`adjustContrast`El método se utiliza para modificar el contraste de la imagen. En este ejemplo, el contraste aumenta en un 50%.

## Paso 4: cree TiffOptions y guarde

```java
// Cree una instancia de TiffOptions para la imagen resultante
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Guarde la imagen resultante en formato TIFF
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

 Aquí configuramos`TiffOptions` para la imagen de salida, especificando el formato y otras propiedades. Luego, la imagen final se guarda en un archivo TIFF.

## Conclusión

¡Felicidades! Ha ajustado con éxito el contraste de una imagen utilizando Aspose.PSD para Java. Este tutorial cubrió los pasos esenciales, desde importar paquetes hasta guardar la imagen procesada.

## Preguntas frecuentes

### P1: ¿Aspose.PSD es compatible con diferentes formatos de imagen?

R1: Sí, Aspose.PSD admite varios formatos de imagen, lo que brinda flexibilidad en sus proyectos.

### P2: ¿Cómo puedo obtener una licencia temporal para Aspose.PSD?

 A2: Puede obtener una licencia temporal[aquí](https://purchase.aspose.com/temporary-license/).

### P3: ¿Dónde puedo encontrar la documentación de Aspose.PSD?

A3: La documentación está disponible.[aquí](https://reference.aspose.com/psd/java/).

### P4: ¿Qué opciones de soporte están disponibles para Aspose.PSD?

 R4: Para obtener ayuda, visite el[Foro Aspose.PSD](https://forum.aspose.com/c/psd/34).

### P5: ¿Puedo comprar Aspose.PSD?

 R5: Sí, puedes comprar Aspose.PSD[aquí](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
