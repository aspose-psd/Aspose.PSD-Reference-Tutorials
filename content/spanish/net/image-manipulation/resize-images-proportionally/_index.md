---
title: Cambiar el tamaño de las imágenes proporcionalmente en Aspose.PSD para .NET
linktitle: Cambiar el tamaño de las imágenes proporcionalmente
second_title: API Aspose.PSD .NET
description: Explore el cambio de tamaño de imágenes sin problemas con Aspose.PSD para .NET. Descargue la biblioteca, siga nuestro tutorial y mejore sus capacidades de procesamiento de imágenes.
type: docs
weight: 14
url: /es/net/image-manipulation/resize-images-proportionally/
---
En el ámbito de la manipulación de imágenes, Aspose.PSD para .NET se destaca como un poderoso conjunto de herramientas que brinda a los desarrolladores la capacidad de cambiar el tamaño de las imágenes proporcionalmente con facilidad. En esta guía paso a paso, lo guiaremos a través del proceso de cambiar el tamaño de las imágenes usando Aspose.PSD para .NET, asegurando que sus imágenes mantengan sus proporciones sin problemas.

## Introducción

Cambiar el tamaño de las imágenes proporcionalmente es una tarea común en muchas aplicaciones y Aspose.PSD para .NET simplifica este proceso para los desarrolladores. Ya sea que esté trabajando en una aplicación web, software de escritorio o aplicación móvil, comprender cómo cambiar el tamaño de las imágenes conservando su relación de aspecto es crucial para mantener el atractivo visual y la coherencia.

## Requisitos previos

Antes de sumergirse en la magia del cambio de tamaño con Aspose.PSD para .NET, asegúrese de cumplir con los siguientes requisitos previos:

1.  Aspose.PSD para la biblioteca .NET: asegúrese de tener instalada la biblioteca Aspose.PSD para .NET. Puedes descargarlo desde el[Aspose.PSD para versiones .NET](https://releases.aspose.com/psd/net/) página.

2. Directorio de documentos: cree un directorio para almacenar sus documentos y reemplace "Su directorio de documentos" en el código proporcionado con la ruta real a este directorio.

Ahora que ha configurado los requisitos previos, pasemos a la guía paso a paso.

## Importar espacios de nombres

```csharp
using Aspose.PSD.ImageOptions;
```

Importe los espacios de nombres necesarios para acceder a las clases y métodos necesarios.

## Paso 1: cargue la imagen

```csharp
// La ruta al directorio de documentos.
string dataDir = "Your Document Directory";

string sourceFile = dataDir + @"sample.psd";

// Cargue una imagen existente en una instancia de la clase RasterImage
using (Image image = Image.Load(sourceFile))
{
	if (!image.IsCached)
	{
		image.CacheData();
	}
	// El resto de los pasos van aquí.
}
```

 Cargue la imagen de origen usando el`Image.Load` método.

## Paso 2: especifique el ancho y el alto

```csharp
// Especificación de ancho y alto
int newWidth = image.Width / 2;
image.ResizeWidthProportionally(newWidth);

int newHeight = image.Height / 2;
image.ResizeHeightProportionally(newHeight);
```

Determine el nuevo ancho y alto de la imagen redimensionada. En este ejemplo, el ancho y el alto se reducen a la mitad, pero puede ajustar estos valores según sus requisitos.

## Paso 3: guarde la imagen redimensionada

```csharp
string destName = dataDir + @"SimpleResizeImageProportionally_out.png";

image.Save(destName, new PngOptions());
```

 Guarde la imagen redimensionada usando el`Save` método con opciones especificadas. En este caso, lo guardaremos como un archivo PNG.

## Conclusión

Cambiar el tamaño de las imágenes proporcionalmente en Aspose.PSD para .NET es un proceso sencillo que agrega valor a su flujo de trabajo de procesamiento de imágenes. Esta guía le ha proporcionado los conocimientos necesarios para integrar perfectamente esta funcionalidad en sus aplicaciones.

## Preguntas frecuentes

### P1: ¿Puedo cambiar el tamaño de las imágenes a dimensiones específicas?

R1: Sí, puede personalizar el nuevo ancho y alto según sus requisitos en el código.

### P2: ¿Aspose.PSD para .NET es adecuado para cambiar el tamaño de imágenes por lotes?

R2: ¡Absolutamente! Puede incorporar estos pasos en un bucle para procesar por lotes varias imágenes.

### P3: ¿Existen otras funciones de manipulación de imágenes en Aspose.PSD para .NET?

R3: Sí, Aspose.PSD para .NET ofrece una amplia gama de funciones, que incluyen recortar, rotar y aplicar filtros a las imágenes.

### P4: ¿Hay una prueba gratuita disponible para Aspose.PSD para .NET?

 R4: Sí, puede explorar las capacidades de Aspose.PSD para .NET con una prueba gratuita. Visita[aquí](https://releases.aspose.com/) para empezar.

### P5: ¿Dónde puedo encontrar soporte para Aspose.PSD para .NET?

 A5: Visita el[Aspose.PSD para el foro .NET](https://forum.aspose.com/c/psd/34) para apoyo y debates de la comunidad.