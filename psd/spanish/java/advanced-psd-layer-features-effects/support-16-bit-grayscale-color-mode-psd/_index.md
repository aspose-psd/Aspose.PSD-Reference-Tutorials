---
date: 2026-09-28
description: Aprenda cómo exportar PSD como PNG mientras establece el modo de color
  PSD a gris de 16‑bits usando Aspose.PSD para Java. Guía paso a paso con ejemplos
  de código.
keywords:
- export psd as png
- how to convert psd to png
- 16-bit grayscale java
lastmod: 2026-09-28
linktitle: Exportar PSD como PNG – Gris de 16‑bits – Java
og_description: Exportar PSD como PNG con gris de 16‑bits usando Aspose.PSD para Java.
  Siga este tutorial paso a paso para preservar 65.536 tonos de gris.
og_image_alt: Guide showing how to export PSD as PNG with 16-bit grayscale using Aspose.PSD
  Java
og_title: Exportar PSD como PNG con gris de 16‑bits en Java – Guía Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  headline: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  type: TechArticle
- description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  name: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  steps:
  - name: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
  - name: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
    text: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
  - name: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
    text: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
  - name: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
    text: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
  type: HowTo
- questions:
  - answer: It provides 65 536 shades of gray, delivering far more tonal detail than
      the standard 8‑bit (256 shades).
    question: What is 16‑bit grayscale color mode?
  - answer: Absolutely! Aspose.PSD supports RGB, CMYK, Lab, Indexed, and many other
      color modes.
    question: Can I use Aspose.PSD for non‑grayscale images?
  - answer: Yes, you can try a free trial version of Aspose.PSD. Just head to the
      [Aspose download page](https://releases.aspose.com/).
    question: Is there a trial version of Aspose.PSD?
  - answer: Check the official [documentation](https://reference.aspose.com/psd/java/)
      for in‑depth tutorials, API references, and sample projects.
    question: Where can I find more Aspose.PSD examples?
  - answer: You can buy a license by visiting the [Aspose purchase page](https://purchase.aspose.com/buy).
    question: How do I purchase a license for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert psd
- Aspose.PSD
- Java image processing
title: Cómo exportar PSD como PNG con modo de color gris de 16‑bits en Java
url: /es/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportar PSD como PNG con modo de color gris de 16‑bit en Java

## Introducción
Exportar PSD como PNG manteniendo un modo de color gris de 16‑bit le brinda la profundidad de una fotografía profesional y la compatibilidad universal de PNG. En esta guía aprenderá cómo **establecer el modo de color del PSD a 16‑bit grayscale** y luego **exportar el PSD como PNG** usando Aspose.PSD para Java. El tutorial cubre todo, desde los requisitos previos hasta la solución de problemas, para que pueda integrar el flujo de trabajo en cualquier canal de imágenes basado en Java.

## Respuestas rápidas
- **¿Qué implica “exportar PSD como PNG”?** Cargar un PSD, opcionalmente cambiar su modo de color y guardarlo como archivo PNG.  
- **¿Qué clase de Aspose maneja la conversión?** `PsdImage` carga el PSD y `PngOptions` define la configuración de salida PNG.  
- **¿Necesito una licencia para producción?** Sí – una versión de prueba funciona para pruebas, pero se requiere una licencia paga para uso comercial.  
- **¿Se puede conservar la profundidad de 16‑bits en PNG?** Absolutamente, usando `PngColorType.GrayscaleWithAlpha`.  
- **¿Qué IDEs son compatibles?** Cualquier IDE de Java – IntelliJ IDEA, Eclipse, VS Code o NetBeans.

## Qué es exportar PSD como PNG
Exportar PSD como PNG es el proceso de convertir un documento de Adobe Photoshop (PSD) en un archivo Portable Network Graphics (PNG) mientras se preservan los datos de píxeles y la profundidad de color de la imagen. Esta conversión se usa comúnmente para compartir recursos en escala de grises de alta calidad en la web sin perder detalle tonal.

## Por qué exportar PSD como PNG con escala de grises de 16‑bit
Exportar a PNG manteniendo la escala de grises de 16‑bit preserva 65 536 tonos de gris, lo que brinda mucha más riqueza tonal que las imágenes de 8‑bit. El soporte universal de PNG garantiza que los archivos se puedan mostrar en navegadores, aplicaciones móviles y editores de escritorio sin pérdida, mientras que la compresión sin pérdidas de Aspose.PSD asegura que no se introduzcan artefactos.

## Requisitos previos
1. **Java Development Kit (JDK)** – Instale el último JDK desde [Oracle's site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java library** – Descargue el JAR desde la [Aspose download page](https://releases.aspose.com/psd/java/).  
3. **An IDE** – IntelliJ IDEA, Eclipse o Visual Studio Code funcionan perfectamente.  
4. **Basic Java knowledge** – Debería sentirse cómodo creando clases, manejando excepciones y trabajando con rutas de archivo.  
5. **A sample PSD file** – Cree uno en Adobe Photoshop o obtenga una muestra gratuita en línea.

## Cómo exportar PSD como PNG paso a paso

## ¿Cómo establecer el modo de color del PSD a 16‑bit grayscale?
PsdImage es la clase de Aspose.PSD que carga y representa un archivo PSD en memoria.  
ColorMode es una enumeración que define el modo de color de una imagen PSD.  

Cargue el PSD con `PsdImage`, cambie su modo de color usando la propiedad `ColorMode` y luego guarde el archivo modificado. Esta operación se ejecuta completamente en memoria, eliminando la necesidad de archivos intermedios y garantizando que la conversión sea rápida y eficiente.

```java
import com.aspose.psd.*;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.system.Enum;
```

Estas importaciones le dan acceso a las funcionalidades que usará para manipular archivos PSD, establecer el modo de color y exportar el resultado como PNG.

## ¿Cómo definir los directorios de origen y salida?
`File` es una clase de java.io que representa una ruta de archivo o directorio en el sistema de archivos.  

Debe indicarle al programa dónde leer el PSD original y dónde escribir el PNG convertido. Usar rutas absolutas o relativas funciona, pero manténgalas consistentes entre entornos para evitar errores de resolución de rutas.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

Reemplace las cadenas de marcador de posición con las rutas reales en su máquina.

## ¿Cómo encapsular la lógica de conversión en un método reutilizable?
`convertPsdToPng` es un método personalizado que encapsula todos los pasos necesarios para convertir un archivo PSD a PNG con configuraciones opcionales.  

Crear un método dedicado le permite reutilizar los mismos pasos de conversión para varios archivos o diferentes configuraciones. Pase parámetros como la ruta de origen, la carpeta de destino y el nivel de compresión opcional, haciendo que el flujo de trabajo sea flexible y mantenible.

```java
class LocalScopeExtension {
    void saveToPsdThenLoadAndSaveToPng(
        String file,
        short colorMode,
        short channelBitsCount,
        short channelsCount,
        short compression,
        int layerNumber) {
```

Este método le permite **establecer el modo de color del PSD** y luego **exportar PSD como PNG** en un solo flujo.

## ¿Cómo cargar el PSD y aplicar el modo de 16‑bit grayscale?
PsdImage es la clase de Aspose.PSD que carga un archivo PSD en memoria.  
ColorMode.GRAYSCALE_16 es un valor de enumeración que establece la imagen a escala de grises de 16‑bit.  
`channelBitsCount` es una propiedad que especifica el número de bits por canal.  

Dentro del método de conversión, construya las rutas completas de los archivos, instancie `PsdImage` y cambie su `ColorMode` a `ColorMode.GRAYSCALE_16`. La propiedad `channelBitsCount` debe establecerse en 16 para mantener la alta profundidad de bits, asegurando que la imagen conserve toda la información tonal.

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

El `postfix` le ayuda a llevar un registro de la configuración utilizada para cada archivo exportado.

## ¿Cómo dibujar un borde sutil en la imagen (paso opcional)?
`Graphics` es una clase que proporciona capacidades de dibujo sobre un lienzo `PsdImage`.  

Opcionalmente, puede dibujar un rectángulo gris alrededor de la imagen para que la salida sea más visible durante las pruebas. Este paso demuestra cómo trabajar con capas y objetos gráficos, y el rectángulo se calcula dinámicamente para que permanezca centrado sin importar el tamaño de la imagen.

```java
try {
    RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;
    // Draw a gray inner border around the perimeter of the layer
    Graphics graphics = new Graphics(raster);
    int width = raster.getWidth();
    int height = raster.getHeight();
    Rectangle rect = new Rectangle(
        width / 3,
        height / 3,
        width - (2 * (width / 3)) - 1,
        height - (2 * (height / 3)) - 1);
    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);
```

El rectángulo se calcula dinámicamente para que permanezca centrado sin importar el tamaño de la imagen.

## ¿Cómo guardar el PSD modificado con el nuevo modo de color?
`PsdOptions` es una clase que controla cómo se guarda un archivo PSD, incluyendo la configuración del modo de color y la profundidad de bits.  

Después de dibujar (o omitir ese paso), llame a `save` en la instancia `PsdImage`, pasando un objeto `PsdOptions` que preserve la configuración de escala de grises de 16‑bit. Esto garantiza que el PSD guardado mantenga el modo de color deseado sin pérdida de datos.

```java
    // Save a copy of PSD with specific characteristics
    PsdOptions psdOptions = new PsdOptions();
    psdOptions.setColorMode(colorMode);
    psdOptions.setChannelBitsCount(channelBitsCount);
    psdOptions.setChannelsCount(channelsCount);
    psdOptions.setCompressionMethod(compression);
    image.save(exportPath, psdOptions);
}
```

## ¿Cómo convertir el PSD a PNG manteniendo la profundidad de 16‑bit?
`PngOptions` es una clase que define la configuración de salida PNG como el tipo de color y el nivel de compresión.  
`PngColorType.GrayscaleWithAlpha` es un valor de enumeración que almacena datos de escala de grises de 16‑bit con un canal alfa.  

Cargue el PSD recién guardado, configure `PngOptions` con `PngColorType.GrayscaleWithAlpha` y llame a `save`. Esto conserva los datos de escala de grises de 16‑bit dentro del archivo PNG, proporcionando una imagen sin pérdidas y de alta calidad adecuada para procesamiento o distribución adicional.

```java
finally {
    image.dispose();
}
// Load the saved PSD
PsdImage image1 = (PsdImage)Image.load(exportPath);
try {
    // Convert the saved PSD to a grayscale PNG image
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);
    image1.save(pngExportPath, pngOptions); // here should be no exception
}
finally {
    image1.dispose();
}
```

Ahora ha exportado exitosamente **PSD como PNG** mientras mantiene los datos de escala de grises de 16‑bit de alta calidad.

## Problemas comunes y soluciones
| Problema | Por qué ocurre | Solución |
|----------|----------------|----------|
| **Excepción “Unsupported color type”** | Intentando guardar un PSD con una configuración de canal no compatible. | Asegúrese de que `channelBitsCount` coincida con la profundidad de bits real (16) y que `channelsCount` sea correcto para escala de grises (1). |
| **Archivo no encontrado** | Ruta del directorio de origen incorrecta. | Verifique la cadena `sourceDir` y confirme que el archivo PSD exista en esa ubicación. |
| **El PNG de salida aparece negro** | PNG guardado sin el manejo adecuado del canal alfa. | Use `PngColorType.GrayscaleWithAlpha` como se muestra arriba. |
| **Desbordamiento de memoria en PSD grandes** | Cargando todo el archivo en memoria. | Habilite el modo de transmisión mediante `PsdImage.load(inputStream, new LoadOptions())` para procesar archivos grandes de manera eficiente. |

## Preguntas frecuentes

**Q: ¿Qué es el modo de color gris de 16‑bit?**  
A: Proporciona 65 536 tonos de gris, ofreciendo mucho más detalle tonal que el estándar de 8‑bit (256 tonos).

**Q: ¿Puedo usar Aspose.PSD para imágenes que no sean en escala de grises?**  
A: ¡Absolutamente! Aspose.PSD soporta RGB, CMYK, Lab, Indexed y muchos otros modos de color.

**Q: ¿Existe una versión de prueba de Aspose.PSD?**  
A: Sí, puede probar una versión de prueba gratuita de Aspose.PSD. Simplemente diríjase a la [Aspose download page](https://releases.aspose.com/).

**Q: ¿Dónde puedo encontrar más ejemplos de Aspose.PSD?**  
A: Consulte la [documentación](https://reference.aspose.com/psd/java/) oficial para tutoriales detallados, referencias de API y proyectos de ejemplo.

**Q: ¿Cómo comprar una licencia para Aspose.PSD?**  
A: Puede adquirir una licencia visitando la [página de compra de Aspose](https://purchase.aspose.com/buy).

**Última actualización:** 2026-09-28  
**Probado con:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Autor:** Aspose

## Tutoriales relacionados

- [Convertir PSD a PNG con profundidad de bits especificada usando Aspose.PSD para Java](/psd/java/optimizing-png-files/specify-png-bit-depth/)
- [Exportar PSD a PNG con efectos de capa usando Aspose.PSD para Java](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [Guardar PSD como JPEG y soportar color RGB con Aspose.PSD Java](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}