---
title: Trabajar con la línea de tiempo en Aspose.PSD para .NET
linktitle: Trabajar con línea de tiempo
second_title: API Aspose.PSD .NET
description: Mejore la manipulación de imágenes PSD con Aspose.PSD para la clase .NET Timeline. Controle las propiedades del marco, los estados de las capas y libere posibilidades creativas sin esfuerzo.
weight: 16
url: /es/net/psd-file-manipulation/timeline/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Trabajar con la línea de tiempo en Aspose.PSD para .NET

## Introducción
En el dinámico mundo del diseño gráfico y la manipulación de imágenes, la capacidad de controlar y manipular la línea de tiempo de las imágenes es crucial. Aspose.PSD para .NET proporciona una solución poderosa con su clase Timeline. Esta característica de alto nivel permite a los usuarios realizar cambios en la línea de tiempo de PsdImage, como alterar el retraso de los fotogramas, editar estados de capas en fotogramas específicos y más.
## Requisitos previos
Antes de sumergirse en las interesantes posibilidades que ofrece la clase Timeline, asegúrese de cumplir con los siguientes requisitos previos:
-  Aspose.PSD para la biblioteca .NET: asegúrese de tener instalada la biblioteca Aspose.PSD para .NET. Puedes descargarlo desde el[Aspose.PSD para documentación .NET](https://reference.aspose.com/psd/net/).
-  Directorios de documentos y de salida: defina las rutas de su documento y directorios de salida en el código. Ajustar el`baseDir` y`outputDir` variables de acuerdo a la estructura de su proyecto.
Ahora, exploremos cómo utilizar la clase Timeline paso a paso.
## Importar espacios de nombres
Para comenzar a trabajar con la clase Timeline, importe los espacios de nombres necesarios en su código:
```csharp
using System;
using System.Collections.Generic;
using System.IO;
using Aspose.PSD.FileFormats.Core.Blending;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.Animation;
```
## Paso 1: cargar la imagen PSD
Comience cargando la imagen PSD desde el archivo fuente especificado. Asegúrese de que la ruta del archivo fuente esté configurada correctamente:
```csharp
string sourceFile = Path.Combine(baseDir, "image1219.psd");
using (PsdImage psdImage = (PsdImage)Image.Load(sourceFile))
{
    //Su código para operaciones adicionales va aquí
}
```
## Paso 2: accede a la línea de tiempo
Una vez cargada la imagen PSD, acceda a la línea de tiempo usando el siguiente código:
```csharp
Timeline timeline = psdImage.Timeline;
```
## Paso 3: cambiar el método de eliminación
Manipular el método de eliminación de un marco específico. En este ejemplo, cambiamos el método de eliminación del cuadro 1:
```csharp
timeline.Frames[0].DisposalMethod = FrameDisposalMethod.DoNotDispose;
```
## Paso 4: ajustar el retraso del cuadro
Modifica el retraso de un fotograma en particular. Aquí, cambiamos el retraso del cuadro 2 al 15:
```csharp
timeline.Frames[1].Delay = 15;
```
## Paso 5: editar el estado de la capa
Cambia la opacidad de la 'Capa 1' en un marco específico. En este caso, configuramos la opacidad en 50 en el cuadro 2:
```csharp
LayerState layerState11 = timeline.Frames[1].LayerStates[1];
layerState11.Opacity = 50;
```
## Paso 6: mover capa
Mueva la 'Capa 1' a la esquina inferior izquierda en un marco específico (marco 3 en este ejemplo):
```csharp
LayerState layerState21 = timeline.Frames[2].LayerStates[1];
layerState21.PositionOffset = new Point(-50, 230);
```
## Paso 7: agregar nuevo marco
Añade un nuevo fotograma a la línea de tiempo:
```csharp
List<Frame> frames = new List<Frame>(timeline.Frames);
frames.Add(new Frame());
timeline.Frames = frames.ToArray();
```
## Paso 8: cambiar el modo de fusión
Modifique el modo de fusión de la 'Capa 1' en un fotograma específico (fotograma 4 en este caso):
```csharp
LayerState layerState31 = timeline.Frames[3].LayerStates[1];
layerState31.BlendMode = BlendMode.Dissolve;
```
## Paso 9: guardar cambios
Vuelva a aplicar los cambios a la instancia de PsdImage y guarde la imagen PSD modificada:
```csharp
psdImage.Save(outputPsd);
```
## Paso 10: Limpiar
Finalmente, limpie eliminando el archivo de salida temporal:
```csharp
File.Delete(outputPsd);
```
## Conclusión

En conclusión, la clase Timeline en Aspose.PSD para .NET permite a los desarrolladores tener un control granular sobre la línea de tiempo de las imágenes PSD. A través de una serie de sencillos pasos, puede manipular las propiedades del marco, los estados de las capas y más, abriendo un reino de posibilidades creativas.

## Preguntas frecuentes

### P1: ¿Aspose.PSD para .NET es adecuado para principiantes?

R1: ¡Absolutamente! Aspose.PSD para .NET proporciona una interfaz fácil de usar y documentación completa, lo que lo hace accesible tanto para principiantes como para desarrolladores experimentados.

### P2: ¿Puedo aplicar cambios en la línea de tiempo a imágenes GIF?

A2: La clase Timeline está diseñada específicamente para imágenes PSD. Para la manipulación de GIF, consulte Aspose.GIF para .NET.

### P3: ¿Dónde puedo encontrar soporte adicional o discutir problemas?

 A3: Visita el[Foro Aspose.PSD](https://forum.aspose.com/c/psd/34) para apoyo de la comunidad y discusiones sobre temas.

### P4: ¿Cómo puedo obtener una licencia temporal de Aspose.PSD para .NET?

 A4: Adquirir una licencia temporal[aquí](https://purchase.aspose.com/temporary-license/).

### P5: ¿Cuáles son los beneficios clave de usar Aspose.PSD para .NET?

R5: Aspose.PSD para .NET ofrece capacidades avanzadas de procesamiento de imágenes, manipulación de archivos PSD y renderizado de alto rendimiento.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
