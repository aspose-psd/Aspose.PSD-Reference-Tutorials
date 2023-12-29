---
title: Creando formas elípticas con Aspose.PSD para .NET
linktitle: Creando formas elípticas con Aspose.PSD para .NET
second_title: API Aspose.PSD .NET
description: Aprenda a dibujar formas elípticas en .NET usando Aspose.PSD. Guía paso a paso con ejemplos de código. Crea gráficos impresionantes sin esfuerzo.
type: docs
weight: 13
url: /es/net/psd-drawing-techniques/creating-elliptical-shapes/
---
## Introducción

Bienvenido a nuestra guía completa sobre cómo crear formas elípticas usando Aspose.PSD para .NET. Aspose.PSD es una potente biblioteca .NET que permite a los desarrolladores manipular y convertir archivos de Photoshop sin necesidad de Adobe Photoshop. En este tutorial, lo guiaremos a través del proceso de dibujar formas elípticas usando la biblioteca.

## Requisitos previos

Antes de sumergirnos en el tutorial, asegúrese de cumplir con los siguientes requisitos previos:

-  Aspose.PSD para la biblioteca .NET: asegúrese de tener la biblioteca Aspose.PSD instalada en su proyecto .NET. Puedes descargarlo desde el[Aspose.PSD para documentación .NET](https://reference.aspose.com/psd/net/).

- Entorno .NET: este tutorial asume que tiene conocimientos prácticos del marco .NET.

## Importar espacios de nombres

Para comenzar, importe los espacios de nombres necesarios a su proyecto. Esto garantiza que tenga acceso a las clases y métodos necesarios para dibujar formas elípticas. He aquí un ejemplo:

```csharp
using Aspose.PSD.Brushes;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.ImageOptions;
```

Ahora, dividamos el proceso de creación de formas elípticas en varios pasos:

## Paso 1: configurar el directorio de documentos

```csharp
// La ruta al directorio de documentos.
string dataDir = "Your Document Directory";
```

## Paso 2: crear una instancia de BmpOptions

```csharp
// Cree una instancia de BmpOptions y establezca sus diversas propiedades
string outpath = dataDir + "Ellipse.bmp";
BmpOptions saveOptions = new BmpOptions();
saveOptions.BitsPerPixel = 32;
```

## Paso 3: crea una instancia de imagen

```csharp
// Crear una instancia de imagen
using (Image image = new PsdImage(100, 100))
{
    // Cree e inicialice una instancia de la clase Graphics y la superficie Clear Graphics
    Graphics graphic = new Graphics(image);
    graphic.Clear(Color.Yellow);
```

## Paso 4: dibuja una forma de elipse punteada

```csharp
    // Dibuje una forma de elipse punteada especificando que el objeto Pluma tenga color rojo y un Rectángulo circundante
    graphic.DrawEllipse(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
```

## Paso 5: dibuja una forma de elipse continua

```csharp
    // Dibuje una forma de elipse continua especificando que el objeto Pluma tenga un pincel sólido de color azul y un Rectángulo circundante.
    graphic.DrawEllipse(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    // Exportar imagen a formato de archivo bmp.
    image.Save(outpath, saveOptions);
}
```

## Conclusión

¡Felicidades! Ha creado con éxito formas elípticas utilizando Aspose.PSD para .NET. Este tutorial cubrió los pasos esenciales, desde configurar el entorno hasta dibujar formas de elipse continua y punteada.

## Preguntas frecuentes

### P1: ¿Dónde puedo encontrar la documentación de Aspose.PSD para .NET?

 A1: La documentación está disponible.[aquí](https://reference.aspose.com/psd/net/).

### P2: ¿Cómo descargo Aspose.PSD para .NET?

 A2: Puedes descargarlo desde la página de lanzamiento.[aquí](https://releases.aspose.com/psd/net/).

### P3: ¿Hay una prueba gratuita disponible?

 R3: Sí, puedes acceder a la prueba gratuita[aquí](https://releases.aspose.com/).

### P4: ¿Cómo puedo obtener soporte para Aspose.PSD para .NET?

 A4: Visita el foro de soporte[aquí](https://forum.aspose.com/c/psd/34).

### P5: ¿Necesito una licencia temporal para realizar pruebas?

 R5: Sí, puedes obtener una licencia temporal[aquí](https://purchase.aspose.com/temporary-license/).