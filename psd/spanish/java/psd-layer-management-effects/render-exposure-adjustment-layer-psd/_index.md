---
date: 2026-04-05
description: Aprende cómo renderizar la capa de ajuste de exposición en archivos PSD
  usando Aspose.PSD para Java. Guía paso a paso con ejemplos de código para modificar
  y agregar capas de exposición.
keywords:
- render exposure adjustment layer
- exposure adjustment layer
- Aspose.PSD Java
linktitle: Renderizar capa de ajuste de exposición en archivos PSD - Java
second_title: Aspose.PSD Java API
title: Renderizar capa de ajuste de exposición en archivos PSD - Java
url: /es/java/psd-layer-management-effects/render-exposure-adjustment-layer-psd/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Renderizar capa de ajuste de exposición en archivos PSD - Java

## Introducción

¿Estás trabajando con archivos PSD de Photoshop y necesitas **render exposure adjustment layer** de forma programática? Ya sea que estés ajustando capas existentes o añadiendo nuevas, Aspose.PSD for Java ofrece una manera potente e intuitiva de manejar estas tareas. En esta guía, recorreremos cómo usar Aspose.PSD for Java para renderizar y modificar capas de ajuste de exposición en archivos PSD. Al final de este tutorial, sabrás cómo ajustar la exposición en capas existentes y añadir nuevas capas de ajuste de exposición a tus archivos PSD. ¡Vamos allá!

## Respuestas rápidas
- **What library is needed?** Aspose.PSD for Java
- **Can I edit an existing exposure layer?** Yes, you can change exposure, offset, and gamma correction.
- **How do I add a new exposure adjustment layer?** Use `addExposureAdjustmentLayer()` on a `PsdImage` instance.
- **Is PNG export supported?** Absolutely – use `PngOptions` to save the result as a PNG.
- **Do I need a license for production?** A commercial license is required for production use; a free trial is available.

## ¿Qué es una capa de ajuste de exposición renderizada?
Una capa de ajuste de exposición es una capa no destructiva de Photoshop que cambia el brillo, el desplazamiento y la gamma de la imagen subyacente. Renderizarla significa aplicar esos ajustes de modo que el resultado visual refleje las modificaciones, lo que luego puedes exportar a formatos como PNG.

## ¿Por qué usar Aspose.PSD for Java para renderizar una capa de ajuste de exposición?
- **Control total** – manipula las propiedades de la capa sin abrir Photoshop.
- **Procesamiento por lotes** – automatiza ajustes en muchos archivos.
- **Multiplataforma** – se ejecuta en cualquier sistema con JDK.
- **Preserva la estructura del PSD** – mantiene las capas editables para futuras modificaciones.

## Requisitos previos

1. **Java Development Kit (JDK)** – al menos JDK 8.
2. **Aspose.PSD for Java** – descárgalo desde [aquí](https://releases.aspose.com/psd/java/).
3. **Conocimientos básicos de Java** – deberías estar cómodo con la sintaxis estándar de Java.
4. **IDE o editor de texto** – IntelliJ IDEA, Eclipse, VS Code, o cualquier editor que prefieras.

## Importar paquetes

Primero, importa las clases necesarias de Aspose.PSD:

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.ExposureLayer;
import com.aspose.psd.imageoptions.PngOptions;
```

## Cómo renderizar una capa de ajuste de exposición – Guía paso a paso

### Paso 1: Cargar el archivo PSD

```java
String dataDir = "Your Document Directory";  // Define your document directory
String sourceFileName = dataDir + "ExposureAdjustmentLayer.psd";  // Source PSD file path

PsdImage im = (PsdImage) Image.load(sourceFileName);  // Load the PSD file
```

Reemplaza `"Your Document Directory"` con la carpeta que contiene tus archivos PSD. El método `Image.load()` devuelve un objeto `PsdImage` que te brinda acceso completo a las capas del documento.

### Paso 2: Editar una capa de ajuste de exposición existente

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof ExposureLayer) {
        ExposureLayer expLayer = (ExposureLayer) im.getLayers()[i];
        expLayer.setExposure(2);  // Adjust the exposure level
        expLayer.setOffset(-0.25f);  // Set the offset
        expLayer.setGammaCorrection(0.5f);  // Adjust the gamma correction
    }
}
```

El bucle recorre cada capa, encuentra cualquier `ExposureLayer` y actualiza sus tres parámetros clave. Este es el núcleo de **rendering the exposure adjustment layer** con tus valores personalizados.

### Paso 3: Guardar el archivo PSD modificado

```java
String psdPathAfterChange = dataDir + "ExposureAdjustmentLayerChanged.psd";  // Path to save the modified PSD file

im.save(psdPathAfterChange);  // Save the changes to the PSD file
```

El PSD modificado conserva todas las capas originales, pero el ajuste de exposición ahora refleja la nueva configuración.

### Paso 4: Exportar el resultado como PNG

```java
String pngExportPath = dataDir + "ExposureAdjustmentLayerChanged.png";  // Path to save the PNG file

PngOptions saveOptions = new PngOptions();  // Create PNG options
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);  // Set color type to Truecolor with Alpha

im.save(pngExportPath, saveOptions);  // Save as PNG
```

Usar `PngOptions` con `TruecolorWithAlpha` garantiza que el PNG exportado mantenga la profundidad de color completa y cualquier transparencia del PSD.

### Paso 5: Añadir una nueva capa de ajuste de exposición

Si necesitas **add a new exposure adjustment layer** a un documento existente, usa el siguiente código:

```java
String sourceFileName = dataDir + "PhotoExample.psd";  // Source PSD file path

PsdImage img = (PsdImage) Image.load(sourceFileName);  // Load the PSD file

ExposureLayer newLayer = img.addExposureAdjustmentLayer(2, -0.25f, 2f);  // Add new exposure adjustment layer

String psdPathAfterChange = dataDir + "PhotoExampleAddedExposure.psd";  // Path to save the modified PSD file
String pngExportPath = dataDir + "PhotoExampleAddedExposure.png";  // Path to save the PNG file

img.save(psdPathAfterChange);  // Save the changes to the PSD file

PngOptions options = new PngOptions();  // Create PNG options
options.setColorType(PngColorType.TruecolorWithAlpha);  // Set color type to Truecolor with Alpha

img.save(pngExportPath, options);  // Save as PNG
```

El método `addExposureAdjustmentLayer` crea una nueva capa de ajuste con los valores de exposición, desplazamiento y gamma especificados, y luego puedes renderizarla y exportarla como antes.

## Problemas comunes y consejos

- **Layer not found** – Asegúrate de que el PSD realmente contenga un `ExposureLayer`. Usa `instanceof ExposureLayer` como se muestra para evitar `ClassCastException`.
- **File path errors** – Utiliza rutas absolutas o verifica que `dataDir` termine con un separador de archivo (`/` o `\`).
- **License exception** – Ejecutar sin una licencia válida añadirá una marca de agua al resultado. Registra tu licencia al inicio del código (`License license = new License(); license.setLicense("Aspose.PSD.lic");`).

## Preguntas frecuentes

### ¿Qué es Aspose.PSD for Java?

Aspose.PSD for Java es una biblioteca que permite crear, editar y convertir archivos PSD de forma programática usando Java. Proporciona una funcionalidad completa para trabajar con documentos de Photoshop.

### ¿Puedo usar Aspose.PSD for Java para manipular otros tipos de capas?

Sí, Aspose.PSD for Java soporta varios tipos de capas, incluidas capas de texto, capas de ajuste y capas de imagen, lo que permite una manipulación extensa de los archivos PSD.

### ¿Cómo empiezo con Aspose.PSD for Java?

Puedes comenzar descargando la biblioteca desde el [sitio web](https://releases.aspose.com/psd/java/) y consultando la [documentación](https://reference.aspose.com/psd/java/) para guías y ejemplos detallados.

### ¿Hay una versión de prueba gratuita disponible para Aspose.PSD for Java?

Sí, hay una versión de prueba gratuita. Puedes descargarla [aquí](https://releases.aspose.com/).

### ¿Cómo puedo obtener soporte para Aspose.PSD for Java?

Para soporte, puedes visitar el [foro de soporte de Aspose](https://forum.aspose.com/c/psd/34) donde puedes hacer preguntas y obtener ayuda de la comunidad.

**Preguntas adicionales**

**P: ¿Puedo procesar por lotes varios archivos PSD?**  
R: Absolutamente. Envuelve la lógica de carga, edición y guardado dentro de un bucle que itere sobre una lista de rutas de archivo.

**P: ¿La biblioteca preserva la jerarquía de capas cuando añado una nueva capa de exposición?**  
R: Sí. La nueva capa se añade encima de las capas existentes, manteniendo la jerarquía original.

**P: ¿A qué formatos de imagen puedo exportar además de PNG?**  
R: Aspose.PSD soporta JPEG, BMP, TIFF y varios otros formatos mediante las clases `*Options` correspondientes.

---

**Última actualización:** 2026-04-05  
**Probado con:** Aspose.PSD for Java 24.10  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}