---
date: 2025-12-17
description: Aprende cómo convertir PSD a PNG mientras configuras el modo de color
  del PSD a escala de grises de 16 bits usando Aspose.PSD para Java. Guía paso a paso
  con ejemplos de código.
linktitle: Convert PSD to PNG – 16-bit Grayscale – Java
second_title: Aspose.PSD Java API
title: Cómo convertir PSD a PNG con modo de color escala de grises de 16 bits en Java
url: /es/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir PSD a PNG con modo de color escala de grises de 16 bits en Java

## Introducción
Cuando te sumerges en el mundo del diseño gráfico y la manipulación de imágenes, entender cómo **convertir PSD a PNG** es como tener un arma secreta. En particular, usar un modo de escala de grises de 16 bits brinda a tus imágenes una profundidad y detalle impresionantes que realmente las hacen destacar. En este tutorial recorreremos cómo **establecer el modo de color del PSD** a escala de grises de 16 bits y luego **exportar el PSD como PNG** usando Aspose.PSD para Java. ¿Listo para elevar tu flujo de trabajo de imágenes? Vamos a comenzar.

## Respuestas rápidas
- **¿Qué implica “convertir PSD a PNG”?** Cargar un PSD, opcionalmente cambiar su modo de color y guardarlo como archivo PNG.  
- **¿Qué clase de Aspose maneja la conversión?** `PsdImage` para cargar y `PngOptions` para guardar.  
- **¿Necesito una licencia especial?** Una versión de prueba funciona para pruebas; se requiere una licencia de pago para producción.  
- **¿Puedo mantener la profundidad de 16 bits en PNG?** Sí, usando `PngColorType.GrayscaleWithAlpha`.  
- **¿Qué IDEs son compatibles?** Cualquier IDE de Java – IntelliJ IDEA, Eclipse, VS Code, etc.

## Requisitos previos
Antes de comenzar, asegurémonos de que tienes todo lo necesario para aprovechar al máximo este tutorial. Esto es lo que necesitarás:

1. **Java Development Kit (JDK)** – Asegúrese de tener la última versión instalada. Puede descargarlo desde [Oracle's site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java Library** – Este es el motor que nos permitirá manipular archivos PSD. Descárguela desde la [Aspose download page](https://releases.aspose.com/psd/java/).  
3. **Un IDE** – IntelliJ IDEA, Eclipse o Visual Studio Code funcionarán sin problemas.  
4. **Conocimientos básicos de Java** – Familiarizarse con la sintaxis de Java hará que los pasos sean más fluidos.  
5. **Un archivo PSD de ejemplo** – Puede crear uno en Adobe Photoshop o descargar una muestra gratuita en línea.

¿Listo? ¡Genial! Importemos los paquetes necesarios y comencemos a programar.

## Importar paquetes
Para iniciar, agregue las importaciones requeridas de Aspose.PSD a su archivo Java:

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

## Paso 1: Definir sus directorios
Primero, configure las carpetas de origen y salida. Esto indica al programa dónde leer el PSD original y dónde escribir los archivos convertidos.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

Reemplace las cadenas de marcador de posición con las rutas reales en su máquina.

## Paso 2: Crear un método para manejar el procesamiento de imágenes
Encapsularemos la lógica de conversión dentro de un método reutilizable. Recibe todos los parámetros que pueda querer ajustar, como modo de color, profundidad de bits y compresión.

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

Este método le permite **establecer el modo de color del PSD** y luego **exportar el PSD como PNG** en un solo flujo.

## Paso 3: Definir rutas de archivo y cargar el PSD
Dentro del método, construya las rutas completas y cargue el PSD original de escala de grises de 16 bits:

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

El `postfix` le ayuda a rastrear la configuración usada para cada archivo exportado.

## Paso 4: Procesar la capa o la imagen completa
Ahora dibujamos sobre una capa específica o sobre la imagen completa. En este ejemplo añadimos un sutil borde gris para que el resultado sea más visible.

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

## Paso 5: Guardar el archivo PSD modificado
Después de dibujar, guardamos el PSD con el modo de color y la profundidad de bits exactos que especificó. Este es el núcleo de **establecer el modo de color del PSD** antes de la conversión.

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

## Paso 6: Convertir el PSD a PNG
Finalmente, cargamos el PSD recién guardado y lo exportamos como PNG. Al usar `PngColorType.GrayscaleWithAlpha` preservamos la profundidad de 16 bits en el archivo PNG.

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

Ahora ha **convertido PSD a PNG** manteniendo los datos de escala de grises de alta calidad de 16 bits.

## Problemas comunes y soluciones
| Problema | Por qué ocurre | Solución |
|----------|----------------|----------|
| **Excepción “Unsupported color type”** | Intentar guardar un PSD con una configuración de canales no compatible. | Asegúrese de que `channelBitsCount` coincida con la profundidad de bits real (16) y que `channelsCount` sea correcto para escala de grises (1). |
| **Archivo no encontrado** | Ruta del directorio de origen incorrecta. | Verifique la cadena `sourceDir` y confirme que el archivo PSD exista. |
| **El PNG de salida aparece negro** | PNG guardado sin manejo del canal alfa. | Use `PngColorType.GrayscaleWithAlpha` como se muestra arriba. |

## Preguntas frecuentes

**P: ¿Qué es el modo de color escala de grises de 16 bits?**  
R: Proporciona 65 536 tonos de gris, ofreciendo mucho más detalle tonal que el modo estándar de 8 bits (256 tonos).

**P: ¿Puedo usar Aspose.PSD para imágenes que no sean escala de grises?**  
R: ¡Absolutamente! Aspose.PSD soporta RGB, CMYK, Lab y muchos otros modos de color.

**P: ¿Existe una versión de prueba de Aspose.PSD?**  
R: Sí, puede probar una versión de prueba gratuita de Aspose.PSD. Simplemente diríjase a la [Aspose download page](https://releases.aspose.com/).

**P: ¿Dónde puedo encontrar más ejemplos de uso de Aspose.PSD?**  
R: Puede consultar la [documentation](https://reference.aspose.com/psd/java/) para obtener ejemplos más detallados y tutoriales.

**P: ¿Cómo compro una licencia para Aspose.PSD?**  
R: Puede comprar una licencia visitando la [Aspose purchase page](https://purchase.aspose.com/buy).

**Última actualización:** 2025-12-17  
**Probado con:** Aspose.PSD for Java 24.12 (última versión al momento de escribir)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}