---
date: 2026-01-01
description: Aprende a crear metadatos XMP, añadir XMP a archivos PSD y actualizar
  los metadatos de imágenes con Aspose.PSD para Java. Sigue esta guía paso a paso
  ahora.
linktitle: Create XMP Metadata
second_title: Aspose.PSD Java API
title: Crear metadatos XMP con Aspose.PSD para Java
url: /es/java/image-editing/create-xmp-metadata/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crear metadatos XMP con Aspose.PSD para Java

## Introducción

Gestionar los metadatos de imágenes es un requisito común para los desarrolladores Java que trabajan con archivos Photoshop (PSD). En este tutorial aprenderá **cómo crear metadatos XMP** usando la biblioteca Aspose.PSD, agregar XMP a una imagen PSD y actualizar los metadatos de la imagen de forma programática. Revisaremos cada paso, explicaremos por qué cada elemento es importante y le daremos consejos prácticos que podrá aplicar en proyectos reales.

## Respuestas rápidas
- **¿Qué es los metadatos XMP?** Un formato estandarizado para incrustar información descriptiva (autor, palabras clave, etc.) dentro de archivos de imagen.  
- **¿Por qué usar Aspose.PSD?** Proporciona una API pura de Java para crear, leer y editar archivos PSD sin Photoshop.  
- **¿Puedo agregar XMP a un PSD existente?** Sí – puede actualizar los metadatos de la imagen al vuelo con `setXmpData`.  
- **¿Cuáles son los pasos principales?** Establecer el tamaño de la imagen, crear encabezado/tráiler, construir paquetes XMP, adjuntarlos y guardar.  
- **¿Necesito una licencia?** Una prueba gratuita funciona para desarrollo; se requiere una licencia comercial para producción.

## Qué significa “crear metadatos XMP” en Java?

Crear metadatos XMP significa construir un paquete XMP (encabezado, cuerpo, tráiler) que describe la imagen y luego incrustar ese paquete en un archivo PSD. La biblioteca Aspose.PSD abstrae los detalles de bajo nivel, permitiéndole centrarse en el contenido que desea almacenar.

## ¿Por qué agregar XMP a archivos PSD?

- **Facilidad de búsqueda:** Permite búsquedas potentes de gestión de activos basadas en autor, título o etiquetas personalizadas.  
- **Interoperabilidad:** XMP es reconocido por productos Adobe, Lightroom y muchos sistemas DAM.  
- **Control de versiones:** Almacena el historial de procesamiento (p.ej., ciudad, modo de color) directamente dentro del archivo.

## Requisitos previos

- **Entorno de desarrollo Java:** JDK 8 o superior instalado y una comprensión básica de Java.  
- **Biblioteca Aspose.PSD:** Descargue y configure la biblioteca Aspose.PSD para Java. Puede encontrar la biblioteca y la documentación detallada [aquí](https://reference.aspose.com/psd/java/).  
- **Su directorio de documentos:** Decida dónde leerá/escribirá los archivos PSD en su sistema.

## Importar paquetes

En su proyecto Java, importe los paquetes necesarios para aprovechar las funcionalidades de Aspose.PSD:

```java
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.system.io.MemoryStream;
import com.aspose.psd.xmp.XmpHeaderPi;
import com.aspose.psd.xmp.XmpMeta;
import com.aspose.psd.xmp.XmpPacketWrapper;
import com.aspose.psd.xmp.XmpTrailerPi;
import com.aspose.psd.xmp.schemas.dublincore.DublinCorePackage;
import com.aspose.psd.xmp.schemas.photoshop.ColorMode;
import com.aspose.psd.xmp.schemas.photoshop.PhotoshopPackage;
```

## Paso 1: Especificar el tamaño de la imagen

Primero, defina las dimensiones del lienzo para la nueva imagen PSD.

```java
// Specify the size of the image by defining a Rectangle
Rectangle rect = new Rectangle(0, 0, 100, 200);
```

## Paso 2: Crear una nueva imagen

Cree una imagen PSD en blanco que luego enriqueceremos con metadatos XMP.

```java
// Create a brand new image for sample purposes
PsdImage image = new PsdImage(rect.getWidth(), rect.getHeight());
```

## Paso 3: Crear el encabezado XMP

El encabezado contiene la instrucción de procesamiento XML de apertura y un GUID que identifica el documento.

```java
// Create an instance of XMP-Header
XmpHeaderPi xmpHeader = new XmpHeaderPi();
xmpHeader.setGuid("Your Document Directory");
```

## Paso 4: Crear el tráiler XMP

El tráiler marca el final del paquete XMP. Establecer la bandera `true` escribe la instrucción de procesamiento de cierre.

```java
// Create an instance of Xmp-TrailerPi 
XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## Paso 5: Crear metadatos XMP

Agregue atributos genéricos como autor y descripción al objeto central de metadatos XMP.

```java
// Create an instance of XMPmeta class to set different attributes
XmpMeta xmpMeta = new XmpMeta();
xmpMeta.addAttribute("Author", "Mr Smith");
xmpMeta.addAttribute("Description", "The fake metadata value");
```

## Paso 6: Crear el contenedor del paquete XMP

Envuelva el encabezado, el tráiler y los metadatos centrales en un solo paquete que pueda adjuntarse a la imagen.

```java
// Create an instance of XmpPacketWrapper that contains all metadata
XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## Paso 7: Establecer atributos de Photoshop

Complete los campos específicos de Photoshop (ciudad, país, modo de color) que muchas herramientas de Adobe esperan.

```java
// Create an instance of Photoshop package and set Photoshop attributes
PhotoshopPackage photoshopPackage = new PhotoshopPackage();
photoshopPackage.setCity("London");
photoshopPackage.setCountry("England");
photoshopPackage.setColorMode(ColorMode.Rgb);
```

## Paso 8: Añadir el paquete Photoshop a los metadatos XMP

Adjunte el paquete Photoshop al paquete XMP.

```java
// Add Photoshop package into XMP metadata
xmpData.addPackage(photoshopPackage);
```

## Paso 9: Establecer atributos DublinCore

Agregue metadatos Dublin Core como autor, título y una etiqueta personalizada de película.

```java
// Create an instance of DublinCore package and set DublinCore attributes
DublinCorePackage dublinCorePackage = new DublinCorePackage();
dublinCorePackage.setAuthor("Charles Bukowski");
dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
dublinCorePackage.addValue("dc:movie", "Barfly");
```

## Paso 10: Añadir el paquete DublinCore a los metadatos XMP

Combine el paquete Dublin Core con el paquete XMP existente.

```java
// Add DublinCore Package into XMP metadata
xmpData.addPackage(dublinCorePackage);
```

## Paso 11: Actualizar los metadatos XMP en la imagen

Ahora incruste el paquete XMP completo en la imagen PSD.

```java
// Update XMP metadata into the image
image.setXmpData(xmpData);
```

## Paso 12: Guardar la imagen

Finalmente, escriba el archivo PSD en disco (o en un flujo de memoria) para que los metadatos se persistan.

```java
// Save the image on the disk or in a memory stream
image.save("Your Document Directory" + "create_XMP_Metadata.psd");
```

## Problemas comunes y soluciones

| Problema | Por qué ocurre | Solución |
|----------|----------------|----------|
| **`NullPointerException` en `setXmpData`** | El paquete XMP no se construyó completamente (faltaba encabezado/tráiler). | Asegúrese de crear `XmpHeaderPi`, `XmpTrailerPi` y agregar todos los paquetes antes de llamar a `setXmpData`. |
| **Los metadatos no son visibles en Photoshop** | Photoshop espera que el paquete XMP esté envuelto correctamente. | Verifique que se use `XmpTrailerPi(true)` y que el paquete se guarde con la imagen. |
| **Errores de ruta de archivo** | Uso de una ruta relativa sin los permisos adecuados. | Use una ruta absoluta o asegúrese de que la aplicación tenga acceso de escritura a la carpeta de destino. |

## Preguntas frecuentes

**P: ¿Es Aspose.PSD compatible con diferentes formatos de imagen?**  
R: Sí, Aspose.PSD soporta PSD, PSB, BMP, GIF, JPEG, PNG, TIFF y más, brindándole flexibilidad entre formatos.

**P: ¿Puedo manipular metadatos existentes usando Aspose.PSD?**  
R: Absolutamente. Puede cargar un PSD existente, obtener sus datos XMP con `getXmpData()`, modificar el paquete y guardarlo nuevamente.

**P: ¿Hay limitaciones en el tamaño de imagen que Aspose.PSD puede manejar?**  
R: Aspose.PSD está diseñado para trabajar con imágenes grandes (hasta varios gigapíxeles), limitadas solo por la memoria disponible.

**P: ¿Existe una versión de prueba disponible para Aspose.PSD?**  
R: Sí, puede explorar las capacidades de Aspose.PSD obteniendo una prueba gratuita [aquí](https://releases.aspose.com/).

**P: ¿Dónde puedo buscar soporte para consultas relacionadas con Aspose.PSD?**  
R: Para cualquier ayuda o consulta, visite el [foro de Aspose.PSD](https://forum.aspose.com/c/psd/34).

## Conclusión

Ahora ha dominado **cómo crear metadatos XMP**, agregar XMP a un PSD y actualizar los metadatos de la imagen usando Aspose.PSD para Java. Estos pasos le brindan control total sobre la información descriptiva incrustada en sus imágenes, haciéndolas buscables, buscables y listas para flujos de trabajo posteriores. Siéntase libre de experimentar con esquemas XMP adicionales o integrar este código en pipelines de procesamiento de imágenes más grandes.

---

**Última actualización:** 2026-01-01  
**Probado con:** Aspose.PSD for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}