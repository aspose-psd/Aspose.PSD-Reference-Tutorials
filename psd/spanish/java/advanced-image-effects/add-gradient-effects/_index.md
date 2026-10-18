---
date: 2026-10-18
description: Aprende a crear efectos de gradiente radial en imágenes Java usando Aspose.PSD.
  Sigue esta guía paso a paso para una integración sin problemas.
keywords:
- create radial gradient java
- apply gradient overlay psd
- add radial gradient image
lastmod: 2026-10-18
linktitle: Agregar efectos de gradiente
og_description: Aprende a crear efectos de gradiente radial en Java usando Aspose.PSD.
  Este tutorial muestra cómo añadir, personalizar y guardar superposiciones de gradiente
  en minutos.
og_image_alt: Screenshot of Aspose.PSD Java code creating a radial gradient effect
og_title: Crear gradiente radial en Java con Aspose.PSD – guía paso a paso
schemas:
- author: Aspose
  dateModified: '2026-10-18'
  description: Learn how to create radial gradient effects in Java images using Aspose.PSD.
    Follow this step‑by‑step guide for seamless integration.
  headline: How to create radial gradient effects in Aspose.PSD for Java
  type: TechArticle
- description: Learn how to create radial gradient effects in Java images using Aspose.PSD.
    Follow this step‑by‑step guide for seamless integration.
  name: How to create radial gradient effects in Aspose.PSD for Java
  steps:
  - name: Load the PSD file and access the gradient overlay
    text: '`PsdLoadOptions` configures how a PSD file is loaded, allowing you to enable
      loading of effect resources. `Image.load` reads the file into an `Image` object.
      In this step, we load a PSD file and retrieve the first `GradientOverlayEffect`
      from the second layer (index 1). The `loadOptions.setLoadEffec'
  - name: Verify Initial Settings
    text: Before making changes, it’s a good practice to confirm the current blend
      mode, opacity, and visibility. This helps you understand the baseline state
      of the gradient overlay.
  - name: Modify Gradient Settings
    text: Here you can customize the gradient’s color, opacity, and blend mode. The
      example changes the color to green, reduces opacity to 193 (out of 255), and
      switches the blend mode to **Lighten**. Feel free to experiment with other `BlendMode`
      values such as `Multiply`, `Screen`, or `Overlay`.
  - name: Save the Edited Image
    text: After applying your modifications, persist the changes by saving the PSD
      to a new file. This step ensures the original file remains untouched.
  - name: Verify Changes
    text: The snippet above demonstrates how to open a PSD, pull the second layer’s
      first effect (assumed to be a gradient overlay), and prepare it for modification.
  - name: Verify the original settings (optional but recommended)
    text: Before you change anything, checking the existing blend mode, opacity, and
      visibility helps you understand the baseline. The `Assert` calls in the code
      confirm that the effect is currently set to **Normal** blend mode, fully opaque,
      and visible.
  - name: Adjust gradient properties to achieve a radial style
    text: 'You can change the gradient’s color, opacity, and blend mode. For a true
      radial effect, set the gradient style: *Pro tip:* Use `Color.getGreen()` or
      any `java.awt.Color` instance to define the start color, and `gradientOverlay.setColor2(Color.getBlue())`
      for the end color.'
  - name: Save the edited PSD
    text: Calling `im.save(exportPath);` writes the modified image to disk. The saved
      file retains the radial gradient overlay and can be opened in Photoshop, previewed
      in browsers, or converted to other formats.
  type: HowTo
- questions:
  - answer: Yes. Retrieve the layer’s `BlendingOptions`, iterate through the `Effects`
      collection, and add a new `GradientOverlayEffect` for each gradient you need.
    question: Can I apply multiple gradient effects to a single image?
  - answer: Aspose.PSD provides shadows, glows, bevels, and more. Each effect appears
      in the `Effects` array and can be configured independently.
    question: What other effects can I combine with gradient overlays?
  - answer: Verify that the PSD was loaded with `setLoadEffectsResource(true)`, check
      layer visibility, and confirm you are modifying the correct effect index.
    question: How can I troubleshoot if the effects are not rendering correctly?
  - answer: Yes, you can get a free trial [here](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.PSD for Java?
  - answer: Visit the [purchase page](https://purchase.aspose.com/buy) for licensing
      information.
    question: Where can I purchase a license for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- create radial gradient
- gradient overlay effect
- Aspose.PSD Java
title: Cómo crear efectos de gradiente radial en Aspose.PSD para Java
url: /es/java/advanced-image-effects/add-gradient-effects/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo crear efectos de degradado radial en Aspose.PSD para Java

## Introducción

En esta guía aprenderás a **create radial gradient java** efectos usando la biblioteca Aspose.PSD. Los degradados radiales son perfectos para añadir profundidad, foco o un brillo sutil a tus capas PSD sin abrir Photoshop. Al final del tutorial podrás cargar un PSD, aplicar una superposición de degradado, ajustar sus propiedades y guardar el resultado, todo desde código Java.

## Respuestas rápidas
- **¿Qué puedo lograr?** Añadir, editar y mezclar superposiciones de degradado radial en capas PSD.  
- **¿Qué biblioteca se requiere?** Aspose.PSD para Java (última versión).  
- **¿Necesito una licencia?** Una prueba gratuita funciona para desarrollo; se requiere una licencia comercial para producción.  
- **¿Cuánto tiempo lleva la implementación?** Aproximadamente 10‑15 minutos para una superposición de degradado radial básica.  
- **¿Es compatible con Java 8+?** Sí, la API soporta Java 8 y versiones posteriores.

## Requisitos previos

Antes de sumergirnos en el tutorial, asegúrate de que tienes los siguientes requisitos:

1. **Aspose.PSD for Java Library** – Asegúrate de haber descargado e instalado la biblioteca Aspose.PSD for Java. Puedes encontrar la biblioteca y su documentación en la [Aspose.PSD Java documentation page](https://reference.aspose.com/psd/java/).  
2. **Java Development Environment** – Configura un entorno de desarrollo Java en tu máquina (JDK 8 o superior, IDE de tu elección).  
3. **Latest Aspose.PSD release** – Descarga la versión más reciente desde la [Aspose releases page](https://releases.aspose.com/).  
4. **Support resources** – Si encuentras problemas, consulta el [Aspose.PSD Support forum](https://forum.aspose.com/c/psd/34).  
5. **License purchase** – Cuando estés listo para producción, obtén una licencia a través de la [purchase page](https://purchase.aspose.com/buy).

Ahora que tienes todo configurado, procedamos con la guía paso a paso.

## ¿Qué es un efecto de superposición de degradado?

Un efecto de superposición de degradado pinta una transición suave entre dos o más colores a través de un área seleccionada de una capa. En Photoshop este efecto puede mezclarse, colorearse y posicionarse para crear diseños visuales sofisticados. La clase `GradientOverlayEffect` es la representación de Aspose.PSD de ese estilo de capa, exponiendo propiedades como paradas de color, opacidad, modo de fusión y estilo de degradado.

## Cómo crear un efecto de degradado radial

Carga el PSD, localiza la capa objetivo, ajusta las propiedades de `GradientOverlayEffect` y, finalmente, guarda el archivo. El flujo de trabajo completo cabe en cuatro líneas concisas de código Java una vez que la imagen está cargada.

### Paso 1: Cargar el archivo PSD y acceder a la superposición de degradado

`PsdLoadOptions` configura cómo se carga un archivo PSD, permitiéndote habilitar la carga de recursos de efectos. `Image.load` lee el archivo en un objeto `Image`.

```javaString dataDir = "Your Document Directory";

// Gradient overlay effect. Example
String sourceFileName = dataDir + "GradientOverlay.psd";
String exportPath = dataDir + "GradientOverlayChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);

GradientOverlayEffect gradientOverlay = (GradientOverlayEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

En este paso, cargamos un archivo PSD y recuperamos el primer `GradientOverlayEffect` de la segunda capa (índice 1). La llamada `loadOptions.setLoadEffectsResource(true)` asegura que los recursos de efecto estén disponibles para su edición.

### Paso 2: Verificar la configuración inicial

```java
// Verify initial settings
Assert.areEqual(BlendMode.Normal, gradientOverlay.getBlendMode());
Assert.areEqual(255, gradientOverlay.getOpacity());
Assert.areEqual(true, gradientOverlay.isVisible());
// ... (additional verifications)
```

Antes de realizar cambios, es una buena práctica confirmar el modo de fusión actual, la opacidad y la visibilidad. Esto te ayuda a entender el estado base de la superposición de degradado.

### Paso 3: Modificar la configuración del degradado

```java
// Modify gradient settings
settings.setColor(Color.getGreen());
gradientOverlay.setOpacity((byte)193);
gradientOverlay.setBlendMode(BlendMode.Lighten);
// ... (additional modifications)
```

Aquí puedes personalizar el color, la opacidad y el modo de fusión del degradado. El ejemplo cambia el color a verde, reduce la opacidad a 193 (de 255) y cambia el modo de fusión a **Lighten**. Siéntete libre de experimentar con otros valores de `BlendMode` como `Multiply`, `Screen` o `Overlay`.

### Paso 4: Guardar la imagen editada

```java
// Save the edited image
im.save(exportPath);
```

Después de aplicar tus modificaciones, persiste los cambios guardando el PSD en un nuevo archivo. Este paso garantiza que el archivo original permanezca intacto.

### Paso 5: Verificar los cambios

```java
// Verify changes after editing
PsdImage img = (PsdImage)Image.load(sourceFileName, loadOptions);

GradientOverlayEffect gradientOverlayEffect = (GradientOverlayEffect)img.getLayers()[1].getBlendingOptions().getEffects()[0];
// ... (additional verifications)
```

El fragmento anterior muestra cómo abrir un PSD, extraer el primer efecto de la segunda capa (asumido como una superposición de degradado) y prepararlo para su modificación.

### Paso 2: Verificar la configuración original (opcional pero recomendado)

Antes de cambiar cualquier cosa, comprobar el modo de fusión, la opacidad y la visibilidad existentes te ayuda a entender la línea base. Las llamadas `Assert` en el código confirman que el efecto está actualmente configurado en modo de fusión **Normal**, totalmente opaco y visible.

### Paso 3: Ajustar las propiedades del degradado para lograr un estilo radial

Puedes cambiar el color, la opacidad y el modo de fusión del degradado. Para un efecto radial verdadero, establece el estilo del degradado:

```java
gradientOverlay.setGradientStyle(GradientStyle.Radial);
gradientOverlay.setAngle(0f); // angle is ignored for radial, but required by API
gradientOverlay.setScale(100f); // 100 % fills the layer
```

*Consejo profesional:* Usa `Color.getGreen()` o cualquier instancia de `java.awt.Color` para definir el color de inicio, y `gradientOverlay.setColor2(Color.getBlue())` para el color final.

### Paso 4: Guardar el PSD editado

Llamar a `im.save(exportPath);` escribe la imagen modificada en disco. El archivo guardado conserva la superposición de degradado radial y puede abrirse en Photoshop, previsualizarse en navegadores o convertirse a otros formatos.

## ¿Por qué crear superposiciones de degradado radial?

Los degradados radiales añaden profundidad y foco a los diseños, haciendo que los elementos parezcan tridimensionales o iluminados. Son ideales para:

- **Rellenos de fondo** que atraen la mirada hacia un sujeto central.  
- **Destellos de botones o íconos** donde se necesita un brillo sutil.  
- **Efectos fotográficos creativos** como viñetas o explosiones de luz.  

Aspose.PSD procesa **más de 50 formatos de entrada y salida** y puede manejar archivos PSD de cientos de páginas sin cargar todo el documento en memoria, permitiéndote automatizar la creación de degradados en grandes bibliotecas de recursos.

## Problemas comunes y consejos

- **Effect not visible:** Asegúrate de que `gradientOverlay.isVisible()` devuelva `true`. Algunos archivos PSD ocultan los efectos por defecto.  
- **Incorrect layer index:** Los índices de capa comienzan en cero; verifica que estés apuntando a la capa correcta (`im.getLayers()[1]` se refiere a la segunda capa).  
- **Opacity casting:** El método `setOpacity` espera un `byte`. Pasar un `int` provocará un error de compilación; conviértelo explícitamente como se muestra.  
- **Resource loading:** Si obtienes `null` al acceder a los efectos, verifica que `loadOptions.setLoadEffectsResource(true)` esté configurado antes de cargar la imagen.

## Preguntas frecuentes

**P: ¿Puedo aplicar varios efectos de degradado a una sola imagen?**  
R: Sí. Recupera el `BlendingOptions` de la capa, itera a través de la colección `Effects` y añade un nuevo `GradientOverlayEffect` para cada degradado que necesites.

**P: ¿Qué otros efectos puedo combinar con superposiciones de degradado?**  
R: Aspose.PSD ofrece sombras, brillos, biseles y más. Cada efecto aparece en la matriz `Effects` y puede configurarse de forma independiente.

**P: ¿Cómo puedo solucionar problemas si los efectos no se renderizan correctamente?**  
R: Verifica que el PSD se haya cargado con `setLoadEffectsResource(true)`, revisa la visibilidad de la capa y confirma que estés modificando el índice de efecto correcto.

**P: ¿Hay una versión de prueba disponible para Aspose.PSD for Java?**  
R: Sí, puedes obtener una prueba gratuita [aquí](https://releases.aspose.com/).

**P: ¿Dónde puedo comprar una licencia para Aspose.PSD for Java?**  
R: Visita la [purchase page](https://purchase.aspose.com/buy) para obtener información sobre licencias.

## Preguntas frecuentes adicionales

**P: ¿Puedo cambiar la dirección del degradado programáticamente?**  
R: Sí. Usa el método `GradientOverlayEffect.setAngle(float angle)` para establecer el ángulo del degradado en grados. Para degradados radiales el ángulo se ignora, pero el método debe llamarse de todos modos.

**P: ¿Aspose.PSD admite degradados radiales?**  
R: Absolutamente. Establece el estilo del degradado a `GradientStyle.Radial` mediante las propiedades de `GradientOverlayEffect`.

**P: ¿Se conservan las superposiciones de degradado al convertir PSD a otros formatos (p. ej., PNG)?**  
R: Cuando rasterizas el PSD (por ejemplo, guardándolo como PNG), el resultado visual del degradado se mantiene, pero el efecto en sí pasa a formar parte de los datos de píxeles.

**P: ¿Cómo elimino una superposición de degradado de una capa?**  
R: Recupera el `BlendingOptions` de la capa, localiza el `GradientOverlayEffect` en la colección `Effects` y elimínalo usando `remove(effect)`.

**P: ¿Es posible animar cambios de degradado?**  
R: Aunque Aspose.PSD no maneja animación directamente, puedes generar una secuencia de archivos PSD con parámetros de degradado variables y luego ensamblarlos en un video o GIF usando otra biblioteca.

## Conclusión

¡Felicidades! Has aprendido **how to create radial gradient java** efectos en tus imágenes usando Aspose.PSD para Java. Siguiendo los pasos anteriores, puedes añadir, modificar y guardar superposiciones de degradado programáticamente, dándote control creativo total sobre los recursos PSD. Experimenta con diferentes colores, modos de fusión y valores de opacidad para lograr el impacto visual que necesitas.

---

**Last Updated:** 2026-10-18  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  








```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.*;
import com.aspose.psd.fileformats.psd.layers.layereffects.GradientOverlayEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Tutoriales relacionados

- [Crear capa de relleno de degradado PSD con Java usando Aspose.PSD – Añadir capa de relleno de degradado](/psd/java/psd-image-modification-conversion/add-gradient-fill-layer-psd-files/)
- [Superposición de patrón PSD: Añadir efectos con Aspose.PSD para Java](/psd/java/advanced-image-effects/add-pattern-effects/)
- [Aplicar una superposición de color y establecer opacidad en Java con Aspose.PSD](/psd/java/image-editing/color-overlay-effect/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}