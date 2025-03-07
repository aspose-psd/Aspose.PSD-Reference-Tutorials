---
title: Agregar efectos de trazo a capas en Aspose.PSD para .NET
linktitle: Agregar efectos de trazo a capas
second_title: API Aspose.PSD .NET
description: Mejore la estética de la imagen con Aspose.PSD para .NET. Aprenda a agregar efectos de trazo paso a paso. Descargue, compre o pruebe la prueba gratuita ahora.
weight: 10
url: /es/net/layer-effects/adding-stroke-effects/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Agregar efectos de trazo a capas en Aspose.PSD para .NET

## Introducción

Bienvenido a este tutorial paso a paso sobre cómo agregar efectos de trazo a capas en Aspose.PSD para .NET. Mejorar el atractivo visual de sus imágenes es muy sencillo con el efecto de trazo, y Aspose.PSD lo hace perfecto para los desarrolladores de .NET. En esta guía, lo guiaremos a través del proceso, brindándole pasos claros y ejemplos para ayudarlo a dominar esta poderosa característica.

## Requisitos previos

Antes de sumergirnos en el tutorial, asegúrese de cumplir con los siguientes requisitos previos:

- Aspose.PSD para .NET: descargue e instale la biblioteca Aspose.PSD desde[sitio web](https://releases.aspose.com/psd/net/).

- Directorio de documentos: prepare un directorio que contenga el documento PSD al que desea aplicar efectos de trazo.

- Directorio de salida: tenga un directorio separado para almacenar las imágenes de salida con efectos de trazo.

- Visual Studio: asegúrese de tener configurado Visual Studio o cualquier otro entorno de desarrollo .NET preferido.

## Importar espacios de nombres

En su proyecto .NET, incluya los espacios de nombres necesarios para aprovechar la funcionalidad Aspose.PSD:

```csharp
using System;
using System.IO;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.FillSettings;
using Aspose.PSD.FileFormats.Psd.Layers.LayerEffects;
using Aspose.PSD.ImageLoadOptions;
using Aspose.PSD.ImageOptions;
```

## Paso 1: cargue el documento PSD

```csharp
string srcFile = Path.Combine(SourceDir, "AddStrokeEffect.psd");
string outputFilePng = Path.Combine(OutputDir, "AddStrokeEffect.png");

using (var psdImage = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    // Su código para cargar el documento PSD va aquí
}
```

## Paso 2: agregar efecto de trazo de color

```csharp
// Agrega relleno de color, en la posición Interior
strokeEffect = psdImage.Layers[1].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Inside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## Paso 3: posición exterior

```csharp
// Agrega relleno de color, en la posición Exterior
strokeEffect = psdImage.Layers[2].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Outside;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

## Paso 4: Posición central

```csharp
// Agrega relleno de color, en la posición Centro
strokeEffect = psdImage.Layers[3].BlendingOptions.AddStroke(FillType.Color);
strokeEffect.Size = 7;
strokeEffect.Position = StrokePosition.Center;
colorFillSettings = strokeEffect.FillSettings as IColorFillSettings;
colorFillSettings.Color = Color.Green;
```

Repita pasos similares para los rellenos de Degradado y Patrón, ajustando la configuración en consecuencia.

## Conclusión

¡Felicidades! Ha aprendido con éxito cómo agregar efectos de trazo a capas usando Aspose.PSD para .NET. Experimente con diferentes configuraciones para lograr el impacto visual deseado en sus imágenes.

## Preguntas frecuentes

### P1: ¿Puedo aplicar efectos de trazo solo a capas específicas?

R1: Sí, puede apuntar a capas específicas ajustando el índice de capa en el código.

### P2: ¿Aspose.PSD es compatible con el último marco .NET?

R2: ¡Absolutamente! Aspose.PSD está diseñado para integrarse perfectamente con los últimos marcos .NET.

### P3: ¿Cómo puedo personalizar el color del trazo?

 A3: Simplemente modifique el`Color` propiedad en el código para lograr el color de trazo deseado.

### P4: ¿Aspose.PSD admite el procesamiento por lotes de varios archivos PSD?

R4: Sí, puedes recorrer varios archivos PSD y aplicar el efecto de trazo usando un enfoque similar.

### P5: ¿Puedo utilizar la versión de prueba antes de comprar Aspose.PSD?

 R5: ¡Por supuesto! Agarra el[prueba gratuita](https://releases.aspose.com/) para explorar las capacidades de Aspose.PSD antes de realizar una compra.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
