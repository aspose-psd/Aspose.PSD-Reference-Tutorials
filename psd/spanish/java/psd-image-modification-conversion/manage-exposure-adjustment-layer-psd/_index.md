---
date: 2026-03-28
description: 'Aprende cómo crear capas de exposición en Java usando Aspose.PSD para
  Java: guía paso a paso para agregar, modificar y guardar capas de ajuste de exposición
  en archivos PSD.'
linktitle: How to create exposure layer java with Aspose.PSD
second_title: Aspose.PSD Java API
title: Cómo crear una capa de exposición en Java con Aspose.PSD
url: /es/java/psd-image-modification-conversion/manage-exposure-adjustment-layer-psd/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Administrar la capa de ajuste de exposición en PSD usando Java

## Introducción
Cuando se trata de trabajar con archivos de Photoshop de forma programática, aprender a **create exposure layer java** usando Aspose.PSD es un verdadero cambio de juego. La capa de ajuste de exposición le permite afinar el brillo, el desplazamiento y la gamma con solo unas pocas líneas de código. En este tutorial recorreremos cada paso necesario para agregar, modificar y guardar capas de ajuste de exposición dentro de un archivo PSD con Java.

## Respuestas rápidas
- **¿Qué biblioteca?** Aspose.PSD for Java  
- **Tarea principal?** Create exposure layer java and adjust its properties  
- **Tiempo típico de implementación?** 10–15 minutes for a basic script  
- **¿Requisitos?** JDK 11+, an IDE, and the Aspose.PSD JAR  
- **¿Licencia necesaria?** A temporary or full Aspose.PSD license for production use  

## ¿Qué es create exposure layer java?
Crear una capa de exposición en Java significa insertar programáticamente una **Exposure Adjustment Layer** en un documento de Photoshop (PSD). Esta capa se comporta como el ajuste “Exposure” que agregarías manualmente en Photoshop, permitiéndote controlar la exposición, el desplazamiento y la gamma sin rasterizar la imagen.

## ¿Por qué usar Aspose.PSD para esta tarea?
- **No se requiere Photoshop** – trabaje completamente en el servidor o en pipelines CI.  
- **Fidelidad completa de capas** – mantenga todas las capas originales intactas mientras ajusta la exposición.  
- **Multiplataforma** – ejecute en Windows, Linux o macOS con el mismo código Java.  

## Requisitos previos
Antes de embarcarnos en este emocionante viaje de manipular archivos PSD, necesitará tener algunas cosas configuradas en su entorno:

### Entorno Java
1. Java Development Kit (JDK): Asegúrese de que tiene el JDK instalado en su máquina. Si no, descárguelo desde el [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. IDE de su elección: Use cualquier IDE como IntelliJ IDEA, Eclipse, o incluso un editor de texto simple para escribir su código Java.  
3. Aspose.PSD Library: Necesitará la biblioteca Aspose.PSD para Java. Puede descargarla desde la [Aspose release page](https://releases.aspose.com/psd/java/).  
4. Conocimientos básicos de Java: Una comprensión fundamental de la programación Java le será de gran ayuda para entender los conceptos cubiertos en este tutorial.  

Una vez que esté todo listo, podemos sumergirnos en los detalles de agregar, modificar y guardar capas de ajuste de exposición en sus archivos PSD.

## Importar paquetes
Antes de que podamos comenzar a editar nuestros archivos PSD, necesitaremos importar los paquetes necesarios proporcionados por Aspose.PSD. Así es como se hace:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.ExposureLayer;
```
Estas importaciones nos dan acceso a las funcionalidades centrales que necesitamos para manipular archivos PSD.

## Paso 1: Configurar su directorio de documentos
Lo primero, definamos el directorio donde se encuentran sus archivos PSD. Deberá reemplazar `"Your Document Directory"` con la ruta a su directorio local.
```java
String dataDir = "Your Document Directory";
```
Aquí, esencialmente estamos preparando el espacio de trabajo para nuestra aplicación. Es como preparar su estación de trabajo antes de iniciar un proyecto de bricolaje: ¡todo debe estar perfecto!

## Paso 2: Cargar el archivo PSD para editar
Ahora, carguemos el archivo PSD donde queremos ajustar la exposición. Trabajaremos con un archivo de ejemplo llamado `ExposureAdjustmentLayer.psd`. 
```java
String sourceFileName = dataDir + "ExposureAdjustmentLayer.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
¡Este es el momento en que interactuamos con nuestro archivo! Es como abrir un libro y prepararse para sumergirse en sus páginas: cada capa es una historia esperando ser contada.

## Paso 3: Modificar capas de ajuste de exposición existentes
A continuación, recorreremos cada capa en nuestro archivo PSD para comprobar si existe una Exposure Adjustment Layer. ¡Si encontramos una, modificaremos sus propiedades!
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof ExposureLayer) {
        ExposureLayer expLayer = (ExposureLayer) im.getLayers()[i];
        expLayer.setExposure(2);
        expLayer.setOffset(-0.25f);
        expLayer.setGammaCorrection(0.5f);
    }
}
```
Aquí es donde ocurre la magia. Piense en ello como ajustar los diales de una radio antigua para obtener el sonido perfecto; ahora, está afinando los niveles de exposición.

## Paso 4: Guardar el archivo PSD modificado
Una vez que haya ajustado la exposición a su gusto, es hora de guardar el archivo editado. Lo guardaremos como `ExposureAdjustmentLayerChanged.psd`.
```java
String psdPathAfterChange = dataDir + "ExposureAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
Es como asegurar esa receta perfecta que acaba de crear: guardarla garantiza que todo su arduo trabajo no se desperdicie.

## Paso 5: Añadir una nueva capa de ajuste de exposición
Ahora que hemos modificado una existente, añadamos una nueva Exposure Adjustment Layer a otro archivo PSD, `PhotoExample.psd`. 
```java
sourceFileName = dataDir + "PhotoExample.psd";
PsdImage img = (PsdImage) Image.load(sourceFileName);
```
Al igual que elegir otro lienzo para pintar, ¡estamos preparando otro documento PSD!

## Paso 6: Configurar la nueva capa de exposición
Crearemos y configuraremos la nueva Exposure Layer con los ajustes deseados.
```java
ExposureLayer newlayer = img.addExposureAdjustmentLayer(10, -0.25f, 2f);
```
Esto es similar a aplicar una nueva capa de pintura a su obra maestra: realza y rejuvenece la imagen, añadiendo profundidad y carácter.

## Paso 7: Guardar el nuevo archivo PSD
Finalmente, guardemos nuestra imagen recién editada como `PhotoExampleAddedExposure.psd`.
```java
String psdPathAfterChange = dataDir + "PhotoExampleAddedExposure.psd";
img.save(psdPathAfterChange);
```
Y así, hemos concluido otro proyecto, listo para mostrar nuestra nueva creación!

## Conclusión
Gestionar capas de ajuste de exposición en archivos PSD usando Aspose.PSD para Java no solo es eficiente; es empoderador. Puede modificar capas existentes o incluso añadir nuevas, asegurando que su visión creativa brille. Siguiendo los pasos descritos arriba, podrá manipular sus imágenes de manera eficaz con solo unas pocas líneas de código.

A medida que continúe explorando las posibilidades de gestión y manipulación de imágenes con Aspose, recuerde que cada ajuste es un paso hacia la creación de la imagen perfecta.

## Preguntas frecuentes

**Q: ¿Qué es Aspose.PSD para Java?**  
A: Aspose.PSD for Java es una biblioteca que le permite trabajar con archivos de Photoshop de forma programática, habilitando funciones como manipulación de capas, renderizado y conversión.

**Q: ¿Puedo usar Aspose.PSD en una aplicación web?**  
A: Sí, Aspose.PSD puede integrarse en aplicaciones web, permitiendo la manipulación de imágenes del lado del servidor.

**Q: ¿Necesito una licencia para usar Aspose.PSD?**  
A: Sí, aunque hay una prueba gratuita disponible, se requiere una licencia válida para uso prolongado. Puede obtener una licencia temporal [aquí](https://purchase.aspose.com/temporary-license/).

**Q: ¿Cómo puedo obtener soporte para Aspose.PSD?**  
A: Puede acceder al soporte de la comunidad en los foros de Aspose [aquí](https://forum.aspose.com/c/psd/34).

**Q: ¿Hay un proyecto de ejemplo disponible para comenzar?**  
A: Sí, puede encontrar proyectos de ejemplo y documentación en la [Aspose.PSD Reference page](https://reference.aspose.com/psd/java/).

---

**Última actualización:** 2026-03-28  
**Probado con:** Aspose.PSD for Java 24.12 (latest)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}