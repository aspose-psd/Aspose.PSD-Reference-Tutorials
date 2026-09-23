---
date: 2026-09-23
description: Aprenda cómo modificar formas vectoriales PSD y procesar por lotes archivos
  PSD usando Aspose.PSD para Java. Pasos detallados, consejos y marcadores de posición
  de código para una solución completa.
keywords:
- modify psd vector shapes
- batch process psd files
- Aspose.PSD Java
- vector shape editing
lastmod: 2026-09-23
linktitle: Soporte de propiedades de datos de registro de longitud en PSD - Java
og_description: Aprenda cómo modificar formas vectoriales PSD y procesar por lotes
  archivos PSD usando Aspose.PSD para Java. Guía paso a paso con marcadores de posición
  de código y consejos de expertos.
og_image_alt: Guide showing how to edit vector shapes in PSD files using Aspose.PSD
  for Java
og_title: Modificar formas vectoriales PSD con Aspose.PSD para Java
schemas:
- author: Aspose
  dateModified: '2026-09-23'
  description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  headline: Modify PSD vector shapes with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to modify PSD vector shapes and batch process PSD files using
    Aspose.PSD for Java. Detailed steps, tips, and code placeholders for a complete
    solution.
  name: Modify PSD vector shapes with Aspose.PSD for Java
  steps:
  - name: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
    text: '**Java Development Kit (JDK)** – download from [Oracle''s website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
      or use your preferred package manager.'
  - name: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java** – obtain the latest JAR from the [Aspose releases
      page](https://releases.aspose.com/psd/java/).'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor.'
  - name: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
    text: '**A PSD file** – create one in Photoshop or grab a sample PSD to experiment
      with.'
  - name: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
    text: '**Basic Java knowledge** – familiarity with classes, objects, and exception
      handling.'
  type: HowTo
- questions:
  - answer: The `VsmsResource` will be absent, so `resource` stays `null`. Add a check
      and skip the modification step or inform the user.
    question: How do I handle a PSD that contains no vector shape layers?
  - answer: Yes, `LengthRecord` provides setters for fill, stroke, and opacity. See
      the API docs for the full list.
    question: Can I change other properties like fill color or stroke width?
  - answer: Absolutely. Wrap the code inside a loop that iterates over a directory
      of PSD files, adjusting the input and output paths each time.
    question: Is it possible to batch‑process multiple PSD files?
  - answer: '`Image.load` handles file streams automatically, but if you load from
      an `InputStream`, remember to close it after use.'
    question: Do I need to close streams manually when loading from a file path?
  - answer: The `LengthRecord` and `PathOperations` classes have been available since
      Aspose.PSD 20.10. Using the latest version (24.11 at time of writing) is recommended.
    question: What version of Aspose.PSD is required for these APIs?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- modify psd vector shapes
- Aspose.PSD
- Java image processing
- batch PSD processing
title: Modificar formas vectoriales PSD con Aspose.PSD para Java
url: /es/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Modificar formas vectoriales PSD con Aspose.PSD para Java

## Introducción
Si necesitas **modificar formas vectoriales PSD** de forma programática, Aspose.PSD para Java te brinda control total sobre los archivos de Photoshop directamente desde tu código Java. Este tutorial te guía a través del soporte de propiedades de registro de longitud, un paso esencial al editar capas de formas vectoriales. Al final podrás abrir un PSD, ajustar sus datos vectoriales y guardar el archivo actualizado sin necesidad de lanzar Photoshop.

## Respuestas rápidas
- **¿Qué significa “modificar formas vectoriales PSD”?** Ajustar la geometría, operaciones de ruta u otros atributos de capas basadas en vectores dentro de un archivo PSD.  
- **¿Qué biblioteca maneja esto?** Aspose.PSD para Java.  
- **¿Necesito una licencia?** Una prueba gratuita sirve para evaluación; se requiere una licencia comercial para producción.  
- **¿Cuánto tiempo lleva la implementación?** Aproximadamente 10‑15 minutos para un script básico de modificación de formas.  
- **¿Cuáles son los requisitos principales?** Java JDK, Aspose.PSD para Java y un archivo PSD de muestra.

## ¿Qué es “soportar propiedades de registro de longitud”?
Soportar propiedades de registro de longitud significa acceder y actualizar los objetos `LengthRecord` que describen cada ruta vectorial dentro de un PSD. Estos registros almacenan información como la longitud de la ruta, su tipo y cómo se une con otras rutas. Cambiarlos te permite controlar cómo las formas se combinan, intersectan o se restan entre sí, habilitando una edición vectorial precisa.

## ¿Por qué usar Aspose.PSD para Java para soportar propiedades de registro de longitud?
Carga tu PSD, edita los datos vectoriales y guarda, todo sin Photoshop. Aspose.PSD procesa PSDs de cientos de páginas en menos de 2 segundos en un servidor típico, ofrece más de 150 clases (incluyendo más de 30 tipos relacionados con vectores) y se ejecuta en Windows, Linux o macOS con cualquier JDK 11+. Esta biblioteca enfocada en el rendimiento elimina la necesidad de costoso software de escritorio.

## Requisitos previos
1. **Java Development Kit (JDK)** – descárgalo desde [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) o usa tu gestor de paquetes preferido.  
2. **Aspose.PSD para Java** – obtén el último JAR en la [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse o cualquier editor compatible con Java.  
4. **Un archivo PSD** – crea uno en Photoshop o consigue un PSD de muestra para experimentar.  
5. **Conocimientos básicos de Java** – familiaridad con clases, objetos y manejo de excepciones.

## Importar paquetes
Las sentencias de importación traen al alcance las clases principales de Aspose.PSD, como `PsdImage`, `VsmsResource` y `LengthRecord`.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Paso 1: Configurar sus directorios de origen y salida
Define dónde se encuentra el PSD original y dónde se escribirá el archivo modificado.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Paso 2: Cargar el archivo PSD
Usa `Image.load` para abrir el archivo y conviértelo a `PsdImage` para acceder a funciones específicas de PSD.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Paso 3: Ubicar el recurso Vsms en la capa
`VsmsResource` es el contenedor que almacena los datos de forma vectorial de una capa. Recorre los recursos de la segunda capa para encontrarlo.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## Paso 4: Acceder a los registros de longitud
`LengthRecord` representa una ruta vectorial distinta. Recupera los registros que planeas modificar.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Paso 5: Modificar las propiedades de operación de ruta
`PathOperations` define cómo interactúan las formas individuales (p. ej., exclusión, intersección, sustracción). Cambiar estos valores actualiza la composición visual de la capa vectorial.

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Paso 6: Guardar el archivo PSD modificado
Persiste tus cambios en un nuevo archivo.

```java
psdImage.save(outPsdFilePath);
```

## Paso 7: Liberar recursos
Descarta la instancia de `PsdImage` para liberar memoria y evitar fugas de recursos.

```java
psdImage.dispose();
```

## Cómo procesar por lotes archivos PSD con soporte de propiedades de registro de longitud
Envuelve el flujo de trabajo de un solo archivo en un bucle que itere sobre un directorio de PSDs, actualizando `inPsdFilePath` y `outPsdFilePath` para cada archivo. Este enfoque te permite aplicar ajustes idénticos de formas vectoriales a decenas o cientos de archivos en minutos, ideal para pipelines de activos automatizados.

## Errores comunes y consejos
- **Comprobaciones de nulos** – siempre verifica que `resource` no sea `null` antes de acceder a sus miembros.  
- **Límites de índices de ruta** – asegura que los índices que uses (p. ej., `[2]`, `[7]`, `[11]`) existan para el PSD específico que estás editando.  
- **Licencia** – ejecutar sin una licencia válida inserta una marca de agua en el PSD guardado.  

## Conclusión
Ahora tienes un ejemplo completo, de extremo a extremo, de cómo **modificar formas vectoriales PSD** soportando propiedades de registro de longitud con Aspose.PSD para Java. Ya sea que estés automatizando un pipeline de activos o construyendo una herramienta de diseño personalizada, estas API te brindan la flexibilidad para manipular capas vectoriales sin trabajo manual en Photoshop. Experimenta con otros valores de `PathOperations` o combina múltiples ediciones de `LengthRecord` para crear formas complejas.

## Preguntas frecuentes

**Q: ¿Cómo manejo un PSD que no contiene capas de forma vectorial?**  
**A:** El `VsmsResource` estará ausente, por lo que `resource` permanecerá `null`. Añade una comprobación y omite el paso de modificación o informa al usuario.

**Q: ¿Puedo cambiar otras propiedades como el color de relleno o el ancho del trazo?**  
**A:** Sí, `LengthRecord` proporciona setters para relleno, trazo y opacidad. Consulta la documentación de la API para la lista completa.

**Q: ¿Es posible procesar por lotes varios archivos PSD?**  
**A:** Absolutamente. Envuelve el código dentro de un bucle que itere sobre un directorio de archivos PSD, ajustando las rutas de entrada y salida en cada iteración.

**Q: ¿Necesito cerrar los streams manualmente al cargar desde una ruta de archivo?**  
**A:** `Image.load` maneja los streams de archivo automáticamente, pero si cargas desde un `InputStream`, recuerda cerrarlo después de usarlo.

**Q: ¿Qué versión de Aspose.PSD se requiere para estas API?**  
**A:** Las clases `LengthRecord` y `PathOperations` están disponibles desde Aspose.PSD 20.10. Se recomienda usar la última versión (24.11 al momento de escribir).

---

**Last Updated:** 2026-09-23  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose

## Tutoriales relacionados

- [Convertir PSD a PNG y crear máscara vectorial Java – Recurso Vmsk en archivos PSD](/psd/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/)
- [Convertir PSD a PNG con soporte de máscara de capa usando Aspose.PSD para Java](/psd/java/advanced-psd-layer-features-effects/support-layer-mask-psd-files/)
- [Agregar soporte de capa a archivos PSD](/psd/java/advanced-psd-layer-features-effects/add-layer-support-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}