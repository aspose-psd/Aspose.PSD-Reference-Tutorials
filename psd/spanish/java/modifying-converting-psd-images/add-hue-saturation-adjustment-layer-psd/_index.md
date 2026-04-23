---
date: 2026-03-13
description: Aprende cómo agregar una capa de tono y saturación a archivos PSD usando
  Aspose.PSD para Java. Esta guía también muestra cómo procesar archivos PSD por lotes
  y crear una capa de ajuste de tono de forma programática.
linktitle: Add Hue Saturation Layer to PSD
second_title: Aspose.PSD Java API
title: Agregar capa de tono y saturación a PSD con Aspose.PSD para Java
url: /es/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
weight: 14
---

 placeholders, shortcodes.

Check headings: keep same number of #.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Agregar capa Hue Saturation a PSD

## Introduction
Cuando se trata de diseño gráfico, la manipulación del color juega un papel fundamental—específicamente, ajustar el tono, la saturación y la luminosidad puede transformar drásticamente el ambiente y la calidad de cualquier imagen. Una forma eficaz de lograr esto es mediante el uso de capas de ajuste en Photoshop (archivos PSD). Si buscas **add hue saturation layer** de forma programática usando Java, la biblioteca Aspose.PSD está aquí para ayudar. Este tutorial te guiará paso a paso para agregar una Hue Saturation Adjustment Layer a tus archivos PSD, haciendo que tu flujo de trabajo sea más productivo y eficiente.

## Quick Answers
- **¿Qué biblioteca te permite agregar una capa hue saturation en Java?** Aspose.PSD for Java.  
- **¿Necesito tener Photoshop instalado?** No, la biblioteca funciona de forma independiente de Photoshop.  
- **¿Puedo procesar por lotes archivos PSD con este método?** Sí—una vez que automatices los pasos, puedes aplicarlos a muchos archivos.  
- **¿Qué versión de Java se requiere?** JDK 8 o posterior.  
- **¿Se necesita una licencia para uso en producción?** Sí, se requiere una licencia comercial después del período de prueba.

## What is an “add hue saturation layer” operation?
Una operación **add hue saturation layer** crea una capa de ajuste no destructiva que te permite modificar los valores de tono, saturación y luminosidad sin alterar los datos de píxeles originales. Esto es ideal para afinar colores en toda una composición o en rangos de color específicos.

## Why use Aspose.PSD for Java?
- **Sin dependencia de Photoshop** – funciona en cualquier plataforma que ejecute Java.  
- **Fidelidad total de PSD** – preserva toda la información de capas, máscaras y efectos.  
- **Listo para procesamiento por lotes** – puedes iterar sobre carpetas y aplicar el mismo ajuste a decenas de archivos.  
- **Enfocado en rendimiento** – optimizado para documentos grandes y automatización del lado del servidor.

## Prerequisites
Antes de sumergirnos en el código, asegúrate de tener lo siguiente:

1. **Java Development Kit (JDK):** Asegúrate de tener instalado JDK 8 o superior en tu máquina. Puedes descargarlo desde el [Java SE Development Kit Downloads](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Aspose.PSD for Java Library:** Necesitarás la biblioteca Aspose.PSD, que puedes [descargar aquí](https://releases.aspose.com/psd/java/).  
3. **IDE:** Un Entorno de Desarrollo Integrado (IDE) adecuado como IntelliJ IDEA o Eclipse para desarrollo Java.  
4. **Conocimientos básicos de Java:** Familiaridad con la programación en Java es una ventaja, pero no te preocupes—te guiaremos línea por línea.

Ahora que tenemos los requisitos listos, ¡pasemos a la parte divertida—¡programar!

## Import Packages
Para comenzar a trabajar con la biblioteca Aspose.PSD, el primer paso es importar las clases necesarias. Así es como puedes hacerlo en tu archivo Java:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```

Asegúrate de haber añadido las bibliotecas apropiadas a tu proyecto para que estas importaciones funcionen sin problemas.

## Step 1: Set Up Your Document Directory
Todo proyecto necesita un punto de partida, y el nuestro no es una excepción. Debes especificar un directorio donde se almacenan tus archivos PSD. Esto es crucial para cargar y guardar imágenes correctamente.

```java
String dataDir = "Your Document Directory"; // Update this path to your actual directory
```

## Step 2: Load an Existing PSD File
Para manipular un archivo PSD existente, primero debemos cargarlo en nuestro programa. Así es como puedes hacerlo:

```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

En este código, actualiza `"HueSaturationAdjustmentLayer.psd"` con el nombre de tu archivo PSD existente que deseas editar.

## Step 3: Edit the Hue/Saturation Layer
A continuación, iteraremos sobre las capas de nuestra imagen PSD cargada para encontrar y editar cualquier capa Hue/Saturation existente. Este paso implica modificar los valores de tono, saturación y luminosidad.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof HueSaturationLayer) {
        HueSaturationLayer hueLayer = (HueSaturationLayer) im.getLayers()[i];
        hueLayer.setHue((short) -25);
        hueLayer.setSaturation((short) -12);
        hueLayer.setLightness((short) 67);
        ColorRangeHsl colorRange = hueLayer.getRange(2);
        colorRange.setHue((short) -40);
        colorRange.setSaturation((short) 50);
        colorRange.setLightness((short) -20);
        colorRange.setMostLeftBorder((short) 300);
    }
}
```

En este ejemplo:  
- Ajustamos el tono a **-25**, la saturación a **-12** y la luminosidad a **+67**.  
- El método `getRange(2)` nos permite ajustar rangos de color específicos según lo deseado.

## Step 4: Save the Modified PSD File
Después de realizar los ajustes, el siguiente paso es guardar el archivo. Esta es una parte vital de nuestro proceso, asegurando que los cambios realizados no se pierdan.

```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```

## Step 5: Add a New Hue/Saturation Layer
Si necesitas **create hue adjustment layer** desde cero, puedes añadir una capa de ajuste Hue/Saturation completamente nueva a otro archivo PSD. Sigue el mismo patrón de carga pero usa el método `addHueSaturationAdjustmentLayer()`.

```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```

## Step 6: Set New Hue/Saturation Values for the New Layer
Ahora que has creado esta nueva capa, aplica los ajustes deseados de tono, saturación y luminosidad como antes.

```java
hueLayerNew.setHue((short) -25);
hueLayerNew.setSaturation((short) -12);
hueLayerNew.setLightness((short) 67);
ColorRangeHsl newColorRange = hueLayerNew.getRange(2);
newColorRange.setHue((short) -160);
newColorRange.setSaturation((short) 100);
newColorRange.setLightness((short) 20);
newColorRange.setMostLeftBorder((short) 300);
```

## Step 7: Save the Updated PSD File
Finalmente, guarda el archivo PSD con la capa Hue/Saturation añadida para que puedas ver tus cambios.

```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```

¡Felicidades! Has manipulado con éxito archivos PSD usando Aspose.PSD for Java. Ahora puedes experimentar con diferentes imágenes y alteraciones más profundas, dando vida a tus proyectos de diseño gráfico.

## How to batch process PSD files with hue adjustments
Dado que el código anterior es totalmente scriptable, puedes envolver toda la secuencia en un bucle que itere sobre cada archivo `.psd` en una carpeta. Esto te permite **batch process psd files** y aplicar los mismos ajustes de tono, saturación y luminosidad en una sola ejecución—perfecto para actualizaciones de marca a gran escala.

## Common Issues and Solutions
- **NullPointerException al cargar un archivo:** Verifica que `dataDir` termine con el separador de archivos apropiado (`/` o `\`) y que el nombre del archivo sea correcto.  
- **Valores de ajuste fuera de rango:** El tono, la saturación y la luminosidad aceptan valores de -255 a 255. Mantén tus números dentro de este rango.  
- **Capa no encontrada:** Si el PSD no tiene capa Hue/Saturation, la verificación `instanceof` omitirá el bloque. Usa `addHueSaturationAdjustmentLayer()` para crear una primero.

## Frequently Asked Questions

**Q: What is a Hue Saturation Adjustment Layer?**  
A: Permite modificar las propiedades de color de una imagen sin alterar permanentemente los píxeles originales.

**Q: Do I need Photoshop installed to use Aspose.PSD?**  
A: No, Aspose.PSD es una biblioteca independiente que funciona sin Photoshop.

**Q: Can I use Aspose.PSD for batch processing?**  
A: Sí, puedes automatizar y procesar por lotes varios archivos PSD con Aspose.PSD.

**Q: Is Aspose.PSD free?**  
A: Aspose.PSD ofrece una prueba gratuita, pero se requiere una licencia para uso a largo plazo. Puedes ver los precios [here](https://purchase.aspose.com/buy).

## Conclusion
Trabajar con gráficos de forma programática abre un mundo de posibilidades. Usar Aspose.PSD for Java para **add hue saturation layer** y para **create hue adjustment layer** brinda flexibilidad y eficiencia que pueden optimizar tu flujo de trabajo de diseño. Ya sea que estés mejorando fotos para un proyecto o creando contenido visual impresionante, dominar estas herramientas puede mejorar enormemente tu producción.

Siéntete libre de explorar más funcionalidades de Aspose.PSD sumergiéndote en la [documentation](https://reference.aspose.com/psd/java/) o considera obtener una [temporary license](https://purchase.aspose.com/temporary-license/) para probar todo el potencial de la biblioteca.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

---