---
title: Capa de ajuste de nivel de renderizado en archivos PSD - Java
linktitle: Capa de ajuste de nivel de renderizado en archivos PSD - Java
second_title: API de Java Aspose.PSD
description: Aprenda cómo mejorar sin esfuerzo el contraste y la vitalidad de la imagen usando Aspose.PSD para Java. Domina las capas de ajuste de niveles con esta guía paso a paso.
weight: 17
url: /es/java/psd-layer-management-effects/render-level-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Capa de ajuste de nivel de renderizado en archivos PSD - Java

## Introducción

¿Alguna vez has abierto un archivo PSD y has descubierto que la imagen carece de contraste o vitalidad? ¡No temáis, guerreros de la edición de imágenes! Aspose.PSD para Java viene al rescate con sus potentes capacidades de manipulación de la capa de ajuste de niveles. Esta guía le proporcionará los conocimientos necesarios para ajustar sus imágenes utilizando niveles en un abrir y cerrar de ojos. 

## Requisitos previos

- Kit de desarrollo de Java (JDK): asegúrese de tener una versión reciente de JDK instalada en su sistema. Puede descargarlo desde el sitio web de Oracle ([https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)).
- Biblioteca Aspose.PSD para Java: descargue la biblioteca Aspose.PSD para Java desde la página de descarga ([https://releases.aspose.com/psd/java/](https://releases.aspose.com/psd/java/)). Necesitará una licencia válida para utilizar todas las funciones, pero hay una prueba gratuita disponible para comenzar ([https://releases.aspose.com/](https://releases.aspose.com/)).

## Importar paquetes

Antes de profundizar en el código, necesitamos importar las clases Aspose.PSD necesarias para interactuar con los archivos PSD. Esto es lo que necesitarás:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
import com.aspose.psd.imageoptions.PngOptions;
```

 El`com.aspose.psd` El paquete proporciona acceso a las funcionalidades de manipulación de PSD, mientras que`com.aspose.psd.imaging.PngOptions` nos permite definir opciones a la hora de guardar la imagen como PNG.

Ahora, embarquémonos en nuestra aventura de ajuste de niveles:

## Paso 1: configurar rutas de archivos:

- Defina variables para su directorio de documentos (`dataDir`), nombre del archivo PSD de origen (`sourceFileName`), nombre del archivo PSD de destino después de la modificación (`psdPathAfterChange`) y la ruta final de exportación PNG (`pngExportPath`). Considere la posibilidad de utilizar nombres descriptivos para mejorar la legibilidad del código.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
String pngExportPath = dataDir + "LevelsAdjustmentLayerChanged.png";
```

## Paso 2: cargar la imagen PSD:

-  Utilice el`Image.load` método para abrir el archivo PSD de origen y almacenarlo en un`PsdImage`objeto (`im`). Aspose.PSD detecta automáticamente el formato del archivo.

```java
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## Paso 3: iteración a través de capas:

- Necesitamos encontrar la capa de ajuste de niveles dentro de su PSD. Aspose proporciona una forma conveniente de iterar a través de todas las capas mediante un bucle.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   // ... (aquí se agregará el código para verificar la capa de niveles)
}
```

## Paso 4: Identificar la capa de niveles:

- Dentro del bucle, compruebe si la capa actual (`im.getLayers()[i]` ) es una instancia de la`LevelsLayer` clase usando el`instanceof` operador. 
-  Si es así, proyecta la capa a un`LevelsLayer` objeto para una mayor manipulación.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   // ... (aquí se agregará el código para ajustar los niveles)
   }
}
```
## Paso 5: Ajuste de niveles (continuación):

-  Ajuste los niveles de salida usando`setOutputShadowLevel` y`setOutputHighlightLevel` para controlar la oscuridad y la claridad de la imagen resultante. Estos valores determinan el rango de niveles de entrada que se asignarán al rango de salida.

```java
for (int i = 0; i < im.getLayers().length; i++) {
   if (im.getLayers()[i] instanceof LevelsLayer) {
	   LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
	   LevelChannel channel = levelsLayer.getChannel(0);

	   // Ajustar los niveles de entrada (0-255):
	   channel.setInputShadowLevel((short) 10); // Oscurecer ligeramente las sombras
	   channel.setInputMidtoneLevel(2.0f);     // Aumentar los medios tonos
	   channel.setInputHighlightLevel((short) 230); // Reducir los reflejos

	   // Ajustar los niveles de salida (0-255):
	   channel.setOutputShadowLevel((short) 20); // Oscurecer aún más las sombras
	   channel.setOutputHighlightLevel((short) 200); //Iluminar reflejos
   }
}
```

## Paso 6: Guardar el PSD modificado:

-  Utilice el`save` método de la`PsdImage` objeto para guardar la imagen modificada en la ruta especificada (`psdPathAfterChange`).

```java
im.save(psdPathAfterChange);
```

## Paso 7: Exportar como PNG (opcional):

-  Si necesita una versión PNG de la imagen ajustada, cree una`PngOptions` objeto y establezca el tipo de color en`TruecolorWithAlpha` . Luego, utiliza el`save` método nuevamente con la ruta de exportación PNG y las opciones.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

¡Y ahí lo tienes! Ha ajustado con éxito la capa de ajuste de niveles en su archivo PSD usando Aspose.PSD para Java. Si comprende estos pasos y experimenta con diferentes valores, podrá mejorar el contraste y la apariencia general de sus imágenes.

## Conclusión

Aspose.PSD para Java le permite tomar el control de su proceso de edición de imágenes. Al dominar la capa de ajuste de niveles, podrás darle nueva vida a tus fotografías y diseños. Recuerde, la práctica hace la perfección, así que no dude en experimentar y explorar todo el potencial de esta poderosa herramienta.
 
## Preguntas frecuentes

### ¿Puedo ajustar canales de color individuales (RGB) por separado? 
Sí, puedes acceder a cada canal de color usando el`getChannel` método de la`LevelsLayer` objeto y modificar sus niveles de forma independiente.

### ¿Cómo manejo múltiples capas de ajuste de niveles en un PSD?
El código recorre todas las capas, por lo que procesará automáticamente cualquier capa de Niveles adicional que se encuentre en la imagen.

### ¿Existen otras formas de ajustar el contraste de la imagen además de los niveles?
¡Absolutamente! Aspose.PSD ofrece varias herramientas de ajuste de imágenes como Curvas, Brillo/Contraste y más.

### ¿Puedo automatizar este proceso para varias imágenes? 
Sí, puede incorporar este código en un script de procesamiento en bucle o por lotes para procesar de manera eficiente varios archivos PSD.

### ¿Dónde puedo encontrar más información y soporte?
Aspose proporciona documentación extensa ([https://reference.aspose.com/psd/java/](https://reference.aspose.com/psd/java/)) y un foro de soporte ([https://forum.aspose.com/c/psd/34](https://forum.aspose.com/c/psd/34)) para cualquier pregunta o problema que pueda surgir.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
