---
title: Recortar imágenes por turnos en Aspose.PSD para .NET
linktitle: Recortar imágenes por turnos
second_title: API Aspose.PSD .NET
description: Aprenda a recortar imágenes sin esfuerzo usando Aspose.PSD para .NET. Siga nuestra guía paso a paso para realizar ajustes de imagen precisos.
type: docs
weight: 12
url: /es/net/image-manipulation/crop-image-shifts/
---
## Introducción

En el ámbito del desarrollo .NET, Aspose.PSD se destaca como un poderoso conjunto de herramientas para tareas de procesamiento de imágenes. Una de sus características destacables es la posibilidad de recortar imágenes con precisión, gracias a la funcionalidad 'Recortar por turnos'. En esta guía paso a paso, lo guiaremos a través del proceso de recortar imágenes sin problemas usando Aspose.PSD para .NET.

## Requisitos previos

Antes de profundizar en el tutorial, asegúrese de cumplir con los siguientes requisitos previos:

-  Aspose.PSD para la biblioteca .NET: asegúrese de tener la biblioteca instalada. Si no, puedes descargarlo desde[página de lanzamiento](https://releases.aspose.com/psd/net/).

- Entorno .NET: asegúrese de tener un entorno de desarrollo .NET configurado en su máquina.

- Imagen de muestra: prepare una imagen de muestra en formato PSD con la que le gustaría trabajar.

## Importar espacios de nombres

Comience importando los espacios de nombres necesarios a su proyecto .NET. Estos espacios de nombres brindan acceso a las clases y métodos de Aspose.PSD necesarios para recortar imágenes.

```csharp
using Aspose.PSD.ImageOptions;
```

## Paso 1: Defina su directorio de documentos

Establezca la ruta al directorio de documentos donde se ubicarán los archivos de origen y de destino.

```csharp
string dataDir = "Your Document Directory";
```

## Paso 2: cargue la imagen de origen

Cargue la imagen PSD que desea recortar. Asegúrese de reemplazar "sample.psd" con el nombre de su archivo fuente.

```csharp
string sourceFile = dataDir + @"sample.psd";
string destName = dataDir + @"CroppingByShifts_out.jpg";
```

## Paso 3: almacenar en caché los datos de la imagen para obtener un mejor rendimiento

Antes de recortar, es recomendable almacenar en caché los datos de la imagen para mejorar el rendimiento.

```csharp
using (RasterImage rasterImage = (RasterImage)Image.Load(sourceFile))
{
    if (!rasterImage.IsCached)
    {
        rasterImage.CacheData();
    }
```

## Paso 4: Definir valores de desplazamiento para recortar

Especifique los valores de desplazamiento para los lados izquierdo, derecho, superior e inferior de la imagen. Ajuste estos valores según sus requisitos de cultivo.

```csharp
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

## Paso 5: aplique el recorte y guarde los resultados

 Utilice el`Crop` método para aplicar los cambios especificados y guardar la imagen recortada en el archivo de destino.

```csharp
rasterImage.Crop(leftShift, rightShift, topShift, bottomShift);
rasterImage.Save(destName, new JpegOptions());
}
```

## Conclusión

¡Felicidades! Ha aprendido con éxito cómo recortar imágenes por turnos usando Aspose.PSD para .NET. Esta potente funcionalidad le proporciona la precisión y el control necesarios para diversas tareas de procesamiento de imágenes.

## Preguntas frecuentes

### P1: ¿Puedo recortar imágenes de diferentes formatos, no solo PSD?

R1: Sí, Aspose.PSD admite varios formatos de imagen, lo que le permite recortar imágenes en formatos como JPEG, PNG y más.

### P2: ¿Existe una versión de prueba disponible antes de comprar Aspose.PSD para .NET?

 R2: ¡Por supuesto! Puede explorar el kit de herramientas con una prueba gratuita disponible[aquí](https://releases.aspose.com/).

### P3: ¿Cómo obtengo una licencia temporal de Aspose.PSD para .NET?

 R3: Puede adquirir una licencia temporal con fines de prueba[aquí](https://purchase.aspose.com/temporary-license/).

### P4: ¿Dónde puedo encontrar soporte adicional y debates relacionados con Aspose.PSD?

 A4: Visita el[Foro Aspose.PSD](https://forum.aspose.com/c/psd/34) por apoyo y debates interesantes.

### P5: ¿Puedo comprar Aspose.PSD para .NET directamente desde el sitio web?

 R5: Sí, puede comprar la biblioteca de forma segura desde[pagina de compra](https://purchase.aspose.com/buy).
