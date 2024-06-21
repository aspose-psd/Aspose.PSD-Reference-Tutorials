---
title: Implementación del ajuste gamma en Aspose.PSD para .NET
linktitle: Implementación del ajuste gamma
second_title: API Aspose.PSD .NET
description: Explore el poder de Aspose.PSD para .NET con nuestra guía paso a paso sobre cómo implementar el ajuste gamma. Ajuste el brillo y el contraste de la imagen sin esfuerzo.
type: docs
weight: 12
url: /es/net/image-adjustment/gamma-adjustment/
---
## Introducción

¡Bienvenido a esta guía completa sobre la implementación del ajuste gamma en Aspose.PSD para .NET! El ajuste gamma es una técnica de procesamiento de imágenes crucial que le permite ajustar el brillo y el contraste de una imagen. En este tutorial, lo guiaremos a través del proceso utilizando la poderosa biblioteca Aspose.PSD para .NET.

## Requisitos previos

Antes de sumergirse en la implementación, asegúrese de cumplir con los siguientes requisitos previos:

-  Biblioteca Aspose.PSD para .NET: asegúrese de tener instalada la biblioteca Aspose.PSD para .NET. Puedes descargarlo[aquí](https://releases.aspose.com/psd/net/).

- .NET Framework: este tutorial asume que tiene conocimientos básicos del desarrollo de .NET y que tiene instalado .NET Framework.

- Entorno de desarrollo integrado (IDE): elija su IDE preferido para el desarrollo .NET, como Visual Studio.

## Importar espacios de nombres

En su proyecto .NET, comience importando los espacios de nombres necesarios para trabajar con Aspose.PSD:

```csharp
using Aspose.PSD.FileFormats.Tiff.Enums;
using Aspose.PSD.ImageOptions;
```

## Paso 1: configura tu proyecto

Cree un nuevo proyecto .NET en el IDE elegido. Asegúrese de agregar referencias a la biblioteca Aspose.PSD.

## Paso 2: definir el directorio de documentos

```csharp
string dataDir = "Your Document Directory";
```

## Paso 3: cargue la imagen

```csharp
string sourceFile = dataDir + @"sample.psd";
using (var image = Image.Load(sourceFile))
{
    // Se realizarán pasos adicionales dentro de este bloque de uso.
}
```

## Paso 4: Transmitir a RasterImage y almacenar datos en caché

```csharp
RasterImage rasterImage = (RasterImage)image;
if (!rasterImage.IsCached)
{
    rasterImage.CacheData();
}
```

## Paso 5: ajustar gamma

```csharp
rasterImage.AdjustGamma(2.2f, 2.2f, 2.2f);
```

## Paso 6: cree TiffOptions y guarde

```csharp
string destName = dataDir + @"AdjustGamma_out.tiff";
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.BitsPerSample = new ushort[] { 8, 8, 8 };
tiffOptions.Photometric = TiffPhotometrics.Rgb;
rasterImage.Save(destName, tiffOptions);
```

## Conclusión

¡Felicidades! Ha implementado con éxito el ajuste de gamma utilizando Aspose.PSD para .NET. Esta poderosa biblioteca proporciona capacidades sólidas para el procesamiento de imágenes, lo que la convierte en una herramienta valiosa para los desarrolladores de .NET.

## Preguntas frecuentes

### P1: ¿Dónde puedo encontrar la documentación de Aspose.PSD?

 A1: Puede consultar la documentación.[aquí](https://reference.aspose.com/psd/net/).

### P2: ¿Cómo descargo Aspose.PSD para .NET?

 A2: Puedes descargar la biblioteca.[aquí](https://releases.aspose.com/psd/net/).

### P3: ¿Hay una prueba gratuita disponible?

 R3: Sí, puedes obtener una prueba gratuita.[aquí](https://releases.aspose.com/).

### P4: ¿Dónde puedo obtener soporte para Aspose.PSD?

 R4: Puedes visitar el foro de soporte.[aquí](https://forum.aspose.com/c/psd/34).

### P5: ¿Necesito una licencia temporal?

 R5: Si es necesario, puede obtener una licencia temporal.[aquí](https://purchase.aspose.com/temporary-license/).