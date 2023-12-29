---
title: Rotar una imagen en Aspose.PSD para .NET
linktitle: Girar una imagen
second_title: API Aspose.PSD .NET
description: Aprenda a rotar imágenes sin esfuerzo en .NET con Aspose.PSD. Sigue nuestro tutorial paso a paso.
type: docs
weight: 15
url: /es/net/image-manipulation/rotate-image/
---
## Introducción

Si se está sumergiendo en el mundo de la manipulación de imágenes utilizando .NET, Aspose.PSD es su herramienta de referencia para un procesamiento de imágenes eficiente y sin problemas. En este tutorial, nos centraremos en una tarea fundamental: rotar una imagen usando Aspose.PSD para .NET. Siga las instrucciones mientras desglosamos el proceso en pasos simples y prácticos.

## Requisitos previos

Antes de comenzar, asegúrese de tener implementados los siguientes requisitos previos:

-  Aspose.PSD para la biblioteca .NET: descargue e instale la biblioteca desde[Documentación de Aspose.PSD .NET](https://reference.aspose.com/psd/net/).

- Su directorio de documentos: configure un directorio donde se almacenan sus imágenes. Reemplace "Su directorio de documentos" en el fragmento de código con la ruta a este directorio.

## Importar espacios de nombres

Asegúrese de incluir los espacios de nombres necesarios para acceder a la funcionalidad Aspose.PSD. Agregue las siguientes líneas al comienzo de su proyecto .NET:

```csharp
using Aspose.PSD.ImageOptions;
```

## Paso 1: cargue la imagen

```csharp
string sourceFile = dataDir + @"sample.psd";

// Cargue una imagen existente en una instancia de la clase RasterImage
using (Image image = Image.Load(sourceFile))
{
```

## Paso 2: rotar la imagen

```csharp
    // Gira la imagen 270 grados en el sentido de las agujas del reloj.
    image.RotateFlip(RotateFlipType.Rotate270FlipNone);
```

## Paso 3: guarde la imagen girada

```csharp
    // Guarde la imagen girada como un archivo JPEG
    string destName = dataDir + @"RotatingAnImage_out.jpg";
    image.Save(destName, new JpegOptions());
}
```

¡Eso es todo! Con solo unas pocas líneas de código, ha rotado exitosamente una imagen usando Aspose.PSD para .NET.

## Conclusión

En este tutorial, exploramos los conceptos básicos de la rotación de imágenes usando Aspose.PSD para .NET. Aspose.PSD proporciona un sólido conjunto de herramientas para la manipulación de imágenes, lo que la convierte en una biblioteca esencial para los desarrolladores de .NET. Experimente con diferentes rotaciones y explore otras capacidades para mejorar sus flujos de trabajo de procesamiento de imágenes.

## Preguntas frecuentes

### P1: ¿Puedo rotar imágenes en un ángulo personalizado usando Aspose.PSD?

Sí, Aspose.PSD le permite especificar un ángulo personalizado para la rotación. Simplemente reemplace el`RotateFlipType.Rotate270FlipNone` línea con el ángulo de rotación deseado.

### P2: ¿Aspose.PSD es compatible con varios formatos de imagen?

 Absolutamente. Aspose.PSD admite una amplia gama de formatos de imagen, incluidos PSD, JPEG, PNG y más. Comprobar el[documentación](https://reference.aspose.com/psd/net/) para la lista completa.

### P3: ¿Cómo puedo obtener una licencia temporal para Aspose.PSD?

 Visita el[página de licencia temporal](https://purchase.aspose.com/temporary-license/) en el sitio web de Aspose para obtener una licencia temporal con fines de evaluación.

### P4: ¿Dónde puedo encontrar soporte para Aspose.PSD?

 Para cualquier consulta o ayuda, visite el[Foro Aspose.PSD](https://forum.aspose.com/c/psd/34) y conectarse con la comunidad.

### P5: ¿Puedo comprar Aspose.PSD para uso comercial?

 Ciertamente. Explorar el[pagina de compra](https://purchase.aspose.com/buy) para adquirir una licencia adaptada a sus necesidades.