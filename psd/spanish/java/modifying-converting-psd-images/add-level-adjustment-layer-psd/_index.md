---
title: Agregar capa de ajuste de nivel en PSD
linktitle: Agregar capa de ajuste de nivel en PSD
second_title: API de Java Aspose.PSD
description: Aprenda cómo agregar efectivamente una capa de ajuste de nivel en sus archivos PSD usando Aspose.PSD para Java. Mejore sus habilidades de edición de imágenes.
weight: 16
url: /es/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Agregar capa de ajuste de nivel en PSD

## Introducción
Cuando se trata de edición de imágenes, administrar niveles puede marcar una gran diferencia en la vitalidad y claridad de tus fotos. Una herramienta útil en el arsenal de Photoshop es la "Capa de ajuste de nivel", que le permite modificar el rango tonal y el equilibrio de color de sus imágenes. En esta guía, le explicaremos cómo implementar una capa de ajuste de nivel en un archivo PSD usando Aspose.PSD para Java. Entonces, toma tu IDE de Java.
## Requisitos previos
Antes de lanzarse al mundo de los ajustes de nivel, deberá configurar algunas cosas para garantizar un viaje sin problemas:
1.  Kit de desarrollo de Java (JDK): asegúrese de tener el JDK instalado en su máquina. Si no lo tienes, puedes conseguirlo desde el[sitio web de oráculo](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) o utilizar OpenJDK.
2.  Biblioteca Aspose.PSD para Java: para manipular archivos PSD, deberá descargar la biblioteca Aspose.PSD. Puede obtener la última versión de este[enlace de descarga](https://releases.aspose.com/psd/java/) y asegúrese de haber incluido el JAR en la biblioteca de su proyecto.
3. Conocimientos básicos de Java: será útil tener una comprensión fundamental de la programación Java, ya que profundizaremos en fragmentos de código a lo largo de este tutorial.
4. Configuración de IDE: puede utilizar cualquier IDE de Java que prefiera, como IntelliJ IDEA, Eclipse o NetBeans, para escribir y ejecutar su código. Solo asegúrese de haber configurado su proyecto Java y agregado la biblioteca Aspose.PSD.

## Importar paquetes
Antes de comenzar a escribir nuestro código, necesitamos importar los paquetes necesarios de la biblioteca Aspose.PSD. Así es como puedes hacerlo:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
Al importar estos paquetes tendremos acceso a las clases necesarias para cargar, modificar y guardar nuestros archivos PSD.

Ahora, dividamos el proceso en pasos digeribles. Continúe mientras avanzamos en la carga de un archivo PSD, ajustando los niveles y luego guardando los cambios. 
## Paso 1: configure las rutas de sus archivos
El primer paso es definir dónde se encuentra nuestro archivo PSD y dónde queremos guardar la salida modificada. Puede personalizar la ruta del directorio para adaptarla a sus necesidades.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
 Aquí, reemplace`"Your Document Directory"`con la ruta real en su sistema donde está almacenado su archivo PSD. Esto prepara el escenario para todo lo que haremos a continuación.
## Paso 2: cargue el archivo PSD
 Ahora, carguemos el archivo PSD usando el`PsdImage` clase. Este paso es fundamental ya que nos permite acceder y manipular las capas.
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
 cuando llamas`Image.load()` , leerá el archivo PSD y creará una instancia de`PsdImage` con el que puedes trabajar.
## Paso 3: iterar a través de las capas
Como queremos ajustar una capa de ajuste de nivel, necesitaremos recorrer cada capa en nuestro archivo PSD. Esto nos ayuda a encontrar la capa específica que queremos modificar.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // Aquí habrá más manipulación...
    }
}
```
 En este bucle,`instanceof LevelsLayer` comprueba si la capa actual es una capa de ajuste de niveles. Si es así, podemos proceder a modificar sus propiedades.
## Paso 4: ajuste la configuración del canal de nivel
Una vez que identificamos la capa correcta, podemos modificar sus niveles de entrada y salida. ¡Aquí es donde ocurre la magia! Ajuste diferentes parámetros para ver cómo afectan a la imagen.
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
Esto es lo que hace cada parámetro:
- Nivel de tonos medios de entrada: ajusta los tonos medios.
- Nivel de sombra de entrada: modifica las áreas más oscuras de la imagen.
- Nivel de resaltado de entrada: altera las áreas brillantes de la imagen.
- Nivel de sombra de salida: establece cómo aparecerán las sombras oscuras.
- Nivel de resaltado de salida: establece cómo aparecerán los resaltados claros.
¡Siéntete libre de experimentar con diferentes valores!
## Paso 5: guarde el archivo PSD modificado
Ahora que hemos realizado nuestros ajustes, es hora de guardar el archivo PSD modificado. Este paso es crucial para garantizar que sus cambios se apliquen y almacenen.
```java
im.save(psdPathAfterChange);
```
 Ahora puede encontrar su archivo PSD ajustado en el lugar especificado`psdPathAfterChange`. 
## Conclusión
¡Acabas de aprender cómo agregar una capa de ajuste de nivel a un archivo PSD usando Aspose.PSD para Java! Si sigue esta guía, podrá ajustar la calidad tonal de sus imágenes sin esfuerzo, allanando el camino para obtener resultados más vibrantes y visualmente atractivos. Recuerde, la práctica hace la perfección, así que siéntase libre de modificar los ajustes y explorar diferentes archivos PSD para ver los efectos de sus cambios.
## Preguntas frecuentes
### ¿Qué es una capa de ajuste de nivel?
Una capa de ajuste de nivel le permite corregir el rango tonal de sus imágenes, equilibrando sombras, medios tonos y luces.
### ¿Puedo usar Aspose.PSD sin realizar una compra?
¡Sí! Aspose ofrece una prueba gratuita para probar la biblioteca antes de comprarla.
### ¿Dónde puedo encontrar documentación para Aspose.PSD?
 Puedes encontrar la documentación.[aquí](https://reference.aspose.com/psd/java/).
### ¿Existe algún soporte comunitario para los productos Aspose?
 ¡Absolutamente! Puede hacer preguntas y obtener ayuda en el[asponer foro](https://forum.aspose.com/c/psd/34).
### ¿Cómo puedo obtener una licencia temporal para Aspose.PSD?
 Puedes solicitar una licencia temporal[aquí](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
