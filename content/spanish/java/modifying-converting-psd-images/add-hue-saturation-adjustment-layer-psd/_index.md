---
title: Agregar capa de ajuste de saturación de tono a PSD
linktitle: Agregar capa de ajuste de saturación de tono a PSD
second_title: API de Java Aspose.PSD
description: Aprenda cómo agregar capas de ajuste de saturación de tono a PSD usando Aspose.PSD para Java en este completo tutorial paso a paso. Mejore su flujo de trabajo de diseño gráfico.
type: docs
weight: 14
url: /es/java/modifying-converting-psd-images/add-hue-saturation-adjustment-layer-psd/
---
## Introducción
Cuando se trata de diseño gráfico, la manipulación del color juega un papel fundamental; específicamente, ajustar el tono, la saturación y la luminosidad puede transformar drásticamente el estado de ánimo y la calidad de cualquier imagen. Una forma eficaz de lograrlo es mediante el uso de capas de ajuste en Photoshop (archivos PSD). Si está buscando mejorar sus archivos PSD mediante programación usando Java, ¡la biblioteca Aspose.PSD está aquí para ayudarlo! Este tutorial lo guiará a través de los pasos para agregar una capa de ajuste de saturación de tono a sus archivos PSD, haciendo que sus flujos de trabajo sean más productivos y eficientes.
En esta guía, cubriremos todo, desde la importación de paquetes necesarios hasta los detalles esenciales de los ejemplos de código.
## Requisitos previos
Antes de pasar al código, asegúrese de tener lo siguiente en su lugar:
1.  Kit de desarrollo de Java (JDK): asegúrese de tener JDK 8 o superior instalado en su máquina. Puedes descargarlo desde el[Descargas del kit de desarrollo Java SE](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Biblioteca Aspose.PSD para Java: necesitará tener la biblioteca Aspose.PSD, que puede[descargar aquí](https://releases.aspose.com/psd/java/). 
3. IDE: un entorno de desarrollo integrado (IDE) adecuado como IntelliJ IDEA o Eclipse para el desarrollo de Java.
4. Conocimientos básicos de Java: la familiaridad con la programación Java es una ventaja, pero no se preocupe; Lo guiaremos a través del código paso a paso.
Ahora que hemos ordenado nuestros requisitos previos, pasemos a la parte divertida: ¡codificar!
## Importar paquetes
Para empezar a trabajar con la biblioteca Aspose.PSD, el primer paso es importar las clases necesarias. Así es como puedes hacerlo en tu archivo Java:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.HueSaturationLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.ColorRangeHsl;
```
Asegúrese de haber agregado las bibliotecas adecuadas a su proyecto para que estas importaciones funcionen sin problemas.
## Paso 1: configure su directorio de documentos
Todo proyecto necesita un punto de partida y el nuestro no es una excepción. Debe especificar un directorio donde se almacenan sus archivos PSD. Esto es crucial para cargar y guardar imágenes correctamente.
```java
String dataDir = "Your Document Directory"; // Actualice esta ruta a su directorio real
```
## Paso 2: cargue un archivo PSD existente
Para manipular un archivo PSD existente, primero debemos cargarlo en nuestro programa. Así es como puedes hacerlo:
```java
String sourceFileName = dataDir + "HueSaturationAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 En este código, actualice`"HueSaturationAdjustmentLayer.psd"` al nombre de su archivo PSD existente que desea editar.
## Paso 3: edita la capa de tono/saturación
A continuación, recorreremos las capas de nuestra imagen PSD cargada para buscar y editar cualquier capa de Tono/Saturación existente. Este paso implica modificar los valores de tono, saturación y luminosidad.
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
- Estamos ajustando el tono a -25, la saturación a -12 y la luminosidad a +67.
-  El`getRange(2)` El método nos permite modificar gamas de colores específicas según lo deseemos.
## Paso 4: guarde el archivo PSD modificado
Después de realizar los ajustes, el siguiente paso es guardar el archivo. Esta es una parte vital de nuestro proceso, ya que garantiza que los cambios que hemos realizado no se pierdan.
```java
String psdPathAfterChange = dataDir + "HueSaturationAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
## Paso 5: agrega una nueva capa de tono/saturación
A continuación, es posible que desees agregar una nueva capa de ajuste de Tono/Saturación a otro archivo PSD. Simplemente siga el mismo enfoque que utilizó anteriormente pero con diferentes archivos PSD.
```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
HueSaturationLayer hueLayerNew = img.addHueSaturationAdjustmentLayer();
```
## Paso 6: Establecer nuevos valores de tono/saturación para la nueva capa
Ahora que ha creado esta nueva capa, aplique los ajustes de tono, saturación y luminosidad deseados como antes.
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
## Paso 7: guarde el archivo PSD actualizado
Finalmente, guarde el archivo PSD con la capa Tono/Saturación agregada para que pueda ver sus cambios.
```java
String psdPathAfterNewLayerChange = dataDir + "PhotoExampleAddedHueSaturation.psd";
img.save(psdPathAfterNewLayerChange);
```
¡Felicidades! Ha manipulado con éxito archivos PSD utilizando Aspose.PSD para Java. Ahora puedes experimentar con diferentes imágenes y modificaciones más profundas, dando vida a tus proyectos de diseño gráfico.
## Conclusión
Trabajar con gráficos mediante programación abre un mundo de posibilidades. El uso de Aspose.PSD para Java para agregar y modificar capas de ajuste de saturación de tono proporciona flexibilidad y eficiencia que pueden optimizar su flujo de trabajo de diseño. Ya sea que esté mejorando fotografías para un proyecto o creando contenido visual sorprendente, dominar estas herramientas puede mejorar enormemente su resultado.
 Siéntase libre de explorar más funcionalidades de Aspose.PSD sumergiéndose en[documentación](https://reference.aspose.com/psd/java/) o considerar enganchar un[licencia temporal](https://purchase.aspose.com/temporary-license/) para probar todo el poder de la biblioteca.
## Preguntas frecuentes
### ¿Qué es una capa de ajuste de saturación de tono?
Una capa de ajuste de saturación de tono le permite modificar las propiedades de color de una imagen sin alterar permanentemente los píxeles originales.
### ¿Necesito tener instalado Photoshop para usar Aspose.PSD?
No, Aspose.PSD es una biblioteca independiente que funciona independientemente de Photoshop.
### ¿Puedo utilizar Aspose.PSD para el procesamiento por lotes?
Sí, puedes automatizar y procesar por lotes varios archivos PSD con Aspose.PSD.
### ¿Aspose.PSD es gratuito?
Aspose.PSD ofrece una prueba gratuita, pero se requiere una licencia para un uso prolongado. Puedes ver precios[aquí](https://purchase.aspose.com/buy).