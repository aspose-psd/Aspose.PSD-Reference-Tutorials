---
title: Aplicación del ajuste del balance de color en Aspose.PSD para .NET
linktitle: Aplicar el ajuste del equilibrio de color
second_title: API Aspose.PSD .NET
description: Mejore los colores de las imágenes PSD sin esfuerzo con Aspose.PSD para la función de ajuste del balance de color de .NET. Siga nuestra guía paso a paso para obtener resultados sorprendentes.
type: docs
weight: 14
url: /es/net/image-adjustment/color-balance-adjustment/
---
## Introducción

¡Bienvenido a esta guía completa sobre cómo aplicar el ajuste del equilibrio de color en Aspose.PSD para .NET! Aspose.PSD es una poderosa biblioteca .NET que permite a los desarrolladores trabajar con archivos PSD de manera eficiente. En este tutorial, nos centraremos en la función Ajuste del equilibrio de color, que le permitirá mejorar el equilibrio de color de sus imágenes PSD con facilidad.

## Requisitos previos

Antes de sumergirnos en el tutorial, asegúrese de cumplir con los siguientes requisitos previos:

-  Aspose.PSD para la biblioteca .NET: descargue e instale la biblioteca desde[Sitio web de Aspose.PSD](https://releases.aspose.com/psd/net/).
- Entorno de desarrollo: asegúrese de tener un entorno de desarrollo .NET funcional configurado en su máquina.
- Archivo PSD: tenga listo un archivo PSD al que desee aplicar el ajuste de equilibrio de color.

## Importar espacios de nombres

En su proyecto .NET, incluya los espacios de nombres necesarios para utilizar las funciones de Aspose.PSD. Agregue las siguientes líneas a su código:

```csharp
using Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers;
```

Ahora, dividamos el proceso de ajuste del equilibrio de color en varios pasos:

## Paso 1: cargue el archivo PSD

```csharp
string dataDir = "Your Document Directory";
var filePath = dataDir + "ColorBalance.psd";
var outputPath = dataDir + "ColorBalance_out.psd";

using (var im = (FileFormats.Psd.PsdImage)Image.Load(filePath))
{
    // El código para el ajuste del equilibrio de color se agregará en los siguientes pasos.
}
```

## Paso 2: acceder y ajustar el equilibrio de color

```csharp
foreach (var layer in im.Layers)
{
    var cbLayer = layer as ColorBalanceAdjustmentLayer;
    if (cbLayer != null)
    {
        cbLayer.ShadowsCyanRedBalance = 30;
        cbLayer.ShadowsMagentaGreenBalance = -15;
        cbLayer.ShadowsYellowBlueBalance = 40;
        cbLayer.MidtonesCyanRedBalance = -90;
        cbLayer.MidtonesMagentaGreenBalance = -25;
        cbLayer.MidtonesYellowBlueBalance = 20;
        cbLayer.HighlightsCyanRedBalance = -30;
        cbLayer.HighlightsMagentaGreenBalance = 67;
        cbLayer.HighlightsYellowBlueBalance = -95;
        cbLayer.PreserveLuminosity = true;
    }
}
```

## Paso 3: guarde la imagen ajustada

```csharp
im.Save(outputPath);
```

¡Ahora ha aplicado con éxito el Ajuste del balance de color a su archivo PSD usando Aspose.PSD para .NET!

## Conclusión

¡Felicidades! Ha aprendido cómo mejorar el equilibrio de color de sus imágenes PSD con Aspose.PSD para .NET. Experimente con diferentes valores de equilibrio para lograr los efectos visuales deseados.

## Preguntas frecuentes

### P1: ¿Puedo aplicar el ajuste del equilibrio de color a varias capas?

R1: Sí, puede recorrer todas las capas de su archivo PSD y ajustar el equilibrio de color según sea necesario.

### P2: ¿Aspose.PSD para .NET es adecuado para el procesamiento por lotes de archivos PSD?

R2: ¡Absolutamente! Aspose.PSD proporciona capacidades eficientes de procesamiento por lotes para archivos PSD.

### P3: ¿Cómo puedo obtener una licencia temporal de Aspose.PSD para .NET?

 A3: Visita[Licencia temporal Aspose.PSD](https://purchase.aspose.com/temporary-license/) para una licencia temporal.

### P4: ¿Dónde puedo encontrar más ejemplos y documentación?

 A4: Explora el[Documentación Aspose.PSD](https://reference.aspose.com/psd/net/) para obtener ejemplos y guías detallados.

### P5: ¿Qué opciones de soporte están disponibles para Aspose.PSD para .NET?

 A5: Visita el[Foro Aspose.PSD](https://forum.aspose.com/c/psd/34) para apoyo y debates de la comunidad.
