---
title: Ampliar y recortar imágenes en Aspose.PSD para .NET
linktitle: Ampliar y recortar imágenes
second_title: API Aspose.PSD .NET
description: Aprenda a expandir y recortar imágenes dinámicamente usando Aspose.PSD para .NET. Siga nuestra guía paso a paso para una manipulación de imágenes perfecta.
type: docs
weight: 13
url: /es/net/image-manipulation/expand-crop-images/
---
## Introducción

Aspose.PSD para .NET es una biblioteca de imágenes completa que permite a los desarrolladores trabajar con varios formatos de imágenes en sus aplicaciones .NET. Una de sus características destacadas es la capacidad de manipular imágenes con facilidad. En este tutorial, nos centraremos en expandir y recortar imágenes, proporcionándole una guía práctica para realizar estas tareas utilizando Aspose.PSD.

## Requisitos previos

Antes de sumergirse en el tutorial, asegúrese de cumplir con los siguientes requisitos previos:

-  Aspose.PSD para la biblioteca .NET: asegúrese de tener instalada la biblioteca Aspose.PSD para .NET. Puedes descargarlo desde el[Aspose.PSD para documentación .NET](https://reference.aspose.com/psd/net/).

- Imagen de muestra: prepare un archivo de imagen de muestra (por ejemplo, "ejemplo1.psd") que usará para el tutorial.

Ahora comencemos con la guía paso a paso.

## Importar espacios de nombres

Comience importando los espacios de nombres necesarios para aprovechar las funcionalidades proporcionadas por Aspose.PSD para .NET. Agregue los siguientes espacios de nombres a su código:

```csharp
using Aspose.PSD.ImageOptions;
```

## Paso 1: configurar el proyecto

 Asegúrese de tener un proyecto configurado con Aspose.PSD para .NET integrado. Si no, sigue las[documentación](https://reference.aspose.com/psd/net/) para ayuda.

## Paso 2: carga la imagen

Cargue la imagen de muestra usando el siguiente código:

```csharp
string dataDir = RunExamples.GetDataDir_DrawingAndFormattingImages();
string sourceFile = dataDir + @"example1.psd";

// Cargar la imagen
using (RasterImage rasterImage = (RasterImage)Image.Load(sourceFile))
{
    // El código adicional para el procesamiento de imágenes irá aquí.
}
```

## Paso 3: almacenar en caché los datos de la imagen

Almacene en caché los datos de la imagen para optimizar el rendimiento:

```csharp
rasterImage.CacheData();
```

## Paso 4: Definir el rectángulo de destino

Cree una instancia de la clase Rectángulo y defina X, Y, Ancho y Alto del rectángulo. Esta será el área a la que se ampliará o recortará la imagen.

```csharp
Rectangle destRect = new Rectangle { X = -200, Y = -200, Width = 300, Height = 300 };
```

## Paso 5: guarde la imagen de salida

Guarde la imagen de salida con las opciones especificadas y el rectángulo de destino:

```csharp
string destName = dataDir + @"jpeg_out.jpg";
rasterImage.Save(destName, new JpegOptions(), destRect);
```

## Conclusión

¡Felicidades! Ha aprendido con éxito cómo expandir y recortar imágenes usando Aspose.PSD para .NET. Esta poderosa biblioteca abre un mundo de posibilidades para la manipulación de imágenes dentro de sus aplicaciones .NET.

## Preguntas frecuentes

### P1: ¿Aspose.PSD puede manejar otros formatos de imagen además de PSD?

R1: Sí, Aspose.PSD admite una amplia gama de formatos de imagen, incluidos JPEG, PNG, GIF y más.

### P2: ¿Dónde puedo encontrar soporte para Aspose.PSD?

 R2: Puede encontrar apoyo e interactuar con la comunidad en[Foro Aspose.PSD](https://forum.aspose.com/c/psd/34).

### P3 ¿Hay una prueba gratuita disponible para Aspose.PSD para .NET?

 R3: Sí, puede explorar las funciones con una prueba gratuita disponible en[Prueba gratuita de Aspose.PSD](https://releases.aspose.com/).

### P4: ¿Cómo obtengo una licencia temporal para Aspose.PSD?

 R4: Puede obtener una licencia temporal de[Licencia temporal Aspose.PSD](https://purchase.aspose.com/temporary-license/).

### P5: ¿Dónde puedo comprar Aspose.PSD para .NET?

 R5: Puedes comprar la biblioteca en el[Página de compra de Aspose.PSD](https://purchase.aspose.com/buy).