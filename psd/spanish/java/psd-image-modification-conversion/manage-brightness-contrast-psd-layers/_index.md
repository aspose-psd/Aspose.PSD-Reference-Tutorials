---
date: 2026-03-28
description: Aprende a ajustar el brillo en PSD con Java usando Aspose.PSD para Java,
  incluyendo cómo cambiar el brillo y el contraste de una capa PSD. Ideal para desarrolladores
  y diseñadores gráficos.
linktitle: Adjust Brightness PSD Java – Manage Brightness & Contrast
second_title: Aspose.PSD Java API
title: Ajustar brillo PSD Java – Gestionar brillo y contraste
url: /es/java/psd-image-modification-conversion/manage-brightness-contrast-psd-layers/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ajustar Brillo PSD Java – Gestionar Brillo y Contraste

## Introducción

¿Eres un diseñador gráfico o un desarrollador que trabaja frecuentemente con archivos PSD (Photoshop Document)? ¿Necesitas **adjust brightness psd java** rápida y confiablemente sin salir de tu entorno Java? En este tutorial, te mostraremos exactamente cómo cambiar el brillo y contraste de capas PSD usando la biblioteca Aspose.PSD para Java. Saldrás con un fragmento de código reutilizable que puede integrarse en cualquier canal de procesamiento de imágenes automatizado. ¡Arremanguémonos y comencemos!

## Respuestas rápidas
- **¿Qué biblioteca necesito?** Aspose.PSD for Java  
- **¿Puedo cambiar varias capas a la vez?** Yes – iterate through all `BrightnessContrastLayer` objects.  
- **¿Qué versión de Java se requiere?** JDK 8 or higher.  
- **¿Necesito una licencia para producción?** Yes, a commercial license is required for non‑evaluation use.  
- **¿El código es compatible con proyectos Maven/Gradle?** Absolutely – just add the Aspose.PSD dependency.

## ¿Qué es “adjust brightness psd java”?

## ¿Por qué ajustar brillo y contraste en capas PSD?

- **Speed up batch processing** – perfect for large design libraries.  
- **Maintain layer structure** – only the targeted adjustment layers are altered, preserving masks and effects.  
- **Integrate into CI/CD pipelines** – generate preview images or thumbnails automatically.

## Requisitos previos

Antes de embarcarnos en este emocionante viaje de manipular archivos PSD con Java, es esencial asegurarse de que tienes todo lo necesario configurado correctamente. Aquí tienes lo que necesitarás para completar con éxito este tutorial:

1. **Java Development Kit (JDK)** – Asegúrate de tener JDK 8 o superior instalado en tu máquina. Puedes descargarlo desde [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk8-downloads.html).

2. **Aspose.PSD for Java Library** – Para trabajar con archivos PSD, necesitarás la biblioteca Aspose.PSD. Puedes descargar la última versión desde la [release page](https://releases.aspose.com/psd/java/).

3. **IDE of Your Choice** – Un Entorno de Desarrollo Integrado (IDE) como IntelliJ IDEA, Eclipse o NetBeans es preferido para escribir y ejecutar tu código Java.

4. **Basic Knowledge of Java** – Familiaridad con la programación Java te ayudará a entender los fragmentos de código con los que trabajaremos.

Una vez que tengas estos requisitos en su lugar, estamos listos para continuar. ¡Ahora, toma tu editor de código favorito y pongámonos a programar!

## Importar paquetes

El primer paso en nuestro viaje de codificación es importar los paquetes necesarios. Antes de poder utilizar las funcionalidades proporcionadas por Aspose.PSD, deberás asegurarte de que la biblioteca esté en tu classpath. Así es como puedes hacerlo:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.BrightnessContrastLayer;
```

Al completar estos pasos, estás preparando el escenario para trabajar con archivos PSD de manera eficaz.

Ahora que tenemos todo configurado, es hora de entrar en el meollo del tutorial: ajustar brillo y contraste en capas PSD. Desglosaremos este proceso en pasos claros para que puedas seguirlo fácilmente.

## Paso 1: Definir el directorio de su documento

Comienza definiendo el directorio donde se encuentran tus archivos PSD. Este paso ayuda a organizar tus archivos de manera eficiente.

```java
String dataDir = "Your Document Directory";
```

Reemplaza `"Your Document Directory"` con la ruta real a tu directorio de archivos PSD.

## Paso 2: Especificar los nombres de archivo de origen y destino

A continuación, debes especificar el nombre del archivo fuente de tu PSD y el archivo de destino donde se guardará el PSD editado.

```java
String sourceFileName = dataDir + "BrightnessContrastModern.psd";
String psdPathAfterChange = dataDir + "BrightnessContrastModernChanged.psd";
```

En este ejemplo, asumimos que tienes un archivo PSD llamado `BrightnessContrastModern.psd` en tu directorio.

## Paso 3: Cargar el archivo PSD

Ahora es momento de cargar el archivo PSD en tu aplicación para poder manipularlo.

```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

Esta línea de código crea una instancia de `PsdImage` que representa tu archivo PSD. Con esto, ahora puedes acceder a todas las capas del PSD.

## Paso 4: Recorrer capas

El siguiente paso implica iterar a través de cada capa de tu archivo PSD para encontrar y manipular los ajustes de brillo y contraste.

```java
for(int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof BrightnessContrastLayer) {
        BrightnessContrastLayer brightnessContrastLayer = (BrightnessContrastLayer)im.getLayers()[i];
```

El bucle `for` recorre cada capa del PSD. Estamos verificando si una capa es una instancia de `BrightnessContrastLayer`. Esto es esencial para asegurarse de que solo intentes cambiar el brillo de la capa PSD en las capas correctas.

## Paso 5: Ajustar brillo y contraste

Dentro del bucle, ahora puedes establecer el brillo y contraste para cada `BrightnessContrastLayer`.

```java
        brightnessContrastLayer.setBrightness(50);
        brightnessContrastLayer.setContrast(50);
    }
}
```

En este ejemplo, establecemos brillo y contraste en `50`. Puedes ajustar estos valores según tus requisitos. Un número mayor incrementa brillo/contraste, mientras que un número menor lo disminuye.

## Paso 6: Guardar los cambios

El paso final es guardar tus cambios en el archivo PSD. Deberás escribir la imagen modificada de vuelta al destino especificado.

```java
im.save(psdPathAfterChange);
```

Esta línea de código guarda el archivo PSD editado con tus nuevos ajustes de brillo y contraste.

## Problemas comunes y soluciones
| Problema | Por qué ocurre | Solución |
|----------|----------------|----------|
| **No `BrightnessContrastLayer` found** | The PSD may use a different adjustment type (e.g., Levels). | Verify the layer type or convert the adjustment to a `BrightnessContrastLayer`. |
| **Saved file looks corrupted** | Missing license or using an outdated Aspose.PSD version. | Apply a valid license and ensure you’re using the latest library release. |
| **Values out of range** | Brightness/Contrast values must be between -100 and 100. | Clamp values before calling `setBrightness`/`setContrast`. |

## Preguntas frecuentes

**Q: What is Aspose.PSD for Java?**  
A: Aspose.PSD for Java is a library that allows developers to manipulate PSD files programmatically, enabling automation of Photoshop‑related tasks.

**Q: Can I adjust multiple layers' brightness and contrast at once?**  
A: Yes, the approach used in this tutorial iterates through all layers in the PSD, allowing you to adjust multiple `BrightnessContrastLayer` instances.

**Q: How do I get a temporary license for Aspose.PSD?**  
A: You can obtain a temporary license by visiting the [temporary license page](https://purchase.aspose.com/temporary-license/).

**Q: Is there a free trial available for Aspose.PSD?**  
A: Yes, you can download a free trial version of Aspose.PSD from the [release page](https://releases.aspose.com/).

**Q: Where can I find additional support for Aspose.PSD?**  
A: You can get support for Aspose.PSD on their [support forum](https://forum.aspose.com/c/psd/34).

---

**Última actualización:** 2026-03-28  
**Probado con:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}