---
date: 2026-02-20
description: Aprenda cómo admitir propiedades de registro de longitud y procesar por
  lotes archivos PSD usando Aspose.PSD para Java. Guía paso a paso con ejemplos de
  código.
linktitle: Support Length Record Data Properties in PSD - Java
second_title: Aspose.PSD Java API
title: Soporte de propiedades de registro de longitud – Modificar formas vectoriales
  PSD (Java)
url: /es/java/advanced-psd-layer-features-effects/support-length-record-data-properties-psd/
weight: 14
---

Record` and `PathOperations` classes are available since Aspose.PSD 20.10. Using the latest version is recommended.

Translate.

Then the footer:

**Last Updated:** 2026-02-20  
**Tested With:** Aspose.PSD for Java 24.11  
**Author:** Aspose  

Translate labels but keep dates.

Then closing shortcodes unchanged.

Also include backtop button shortcode unchanged.

Now produce final content.

Let's craft Spanish translation.

Be careful to keep markdown formatting.

Proceed.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Soporte de Propiedades de Registro de Longitud – Modificar Formas Vectoriales PSD (Java)

## Introducción
Si necesitas **modificar formas vectoriales PSD** de forma programática, la biblioteca Aspose.PSD for Java te brinda control total sobre los archivos de Photoshop directamente desde tu código Java. En este tutorial repasaremos todo lo que necesitas saber para **soportar propiedades de registro de longitud**, un paso esencial cuando deseas editar capas de formas vectoriales. Al final, podrás abrir un PSD, ajustar sus propiedades de forma vectorial y guardar el archivo actualizado sin salir de tu IDE. ¡Vamos allá!

## Respuestas Rápidas
- **¿Qué significa “modificar formas vectoriales PSD”?** Ajustar la geometría, operaciones de ruta u otras propiedades de capas basadas en vectores dentro de un archivo PSD.  
- **¿Qué biblioteca gestiona esto?** Aspose.PSD for Java.  
- **¿Necesito una licencia?** Una prueba gratuita sirve para evaluación; se requiere una licencia comercial para producción.  
- **¿Cuánto tiempo lleva la implementación?** Aproximadamente 10‑15 minutos para un script básico de modificación de formas.  
- **¿Cuáles son los requisitos principales?** Java JDK, Aspose.PSD for Java y un archivo PSD de ejemplo.

## ¿Qué significa “soportar propiedades de registro de longitud”?
Soportar propiedades de registro de longitud implica acceder y actualizar los objetos `LengthRecord` que describen cada ruta vectorial dentro de un PSD. Cambiar estos registros te permite controlar cómo las formas se combinan, intersectan o se restan entre sí.

## ¿Por qué usar Aspose.PSD for Java para soportar propiedades de registro de longitud?
- **No se requiere Photoshop** – trabaja directamente con archivos PSD en cualquier servidor.  
- **API rica** – accede a capas, recursos y datos vectoriales con clases fuertemente tipadas.  
- **Multiplataforma** – se ejecuta en Windows, Linux o macOS con cualquier JDK.  
- **Enfocado en rendimiento** – manejo eficiente de memoria y operaciones de guardado rápidas.  

## Requisitos previos
1. **Java Development Kit (JDK)** – descárgalo desde [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) o usa tu gestor de paquetes preferido.  
2. **Aspose.PSD for Java** – obtén el JAR más reciente desde la [Aspose releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse o cualquier editor compatible con Java.  
4. **Un archivo PSD** – crea uno en Photoshop o consigue un PSD de muestra para experimentar.  
5. **Conocimientos básicos de Java** – familiaridad con clases, objetos y manejo de excepciones.

## Importar paquetes
Primero, importa las clases que necesitarás para trabajar con archivos PSD y recursos de formas vectoriales.

```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VsmsResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathOperations;
```

## Paso 1: Configura tus directorios de origen y salida
Define dónde se encuentra el PSD original y dónde deseas guardar el archivo modificado.

```java
String sourceDir = "Your Source Directory";
String outputDir = "Your Document Directory";
String inPsdFilePath = sourceDir + "PathOperationsShape.psd";
String outPsdFilePath = outputDir + "out_PathOperationsShape.psd";
```

## Paso 2: Carga el archivo PSD
Utiliza `Image.load` para abrir el archivo y conviértelo a `PsdImage` para acceder a funciones específicas de PSD.

```java
PsdImage psdImage = (PsdImage) Image.load(inPsdFilePath);
```

## Paso 3: Ubica el recurso Vsms en la capa
Los datos de la forma vectorial se encuentran dentro de un `VsmsResource`. Recorre los recursos de la segunda capa para encontrarlo.

```java
VsmsResource resource = null;
for (LayerResource layerResource : psdImage.getLayers()[1].getResources()) {
    if (layerResource instanceof VsmsResource) {
        resource = (VsmsResource) layerResource;
        break;
    }
}
```

## Paso 4: Accede a los registros de longitud
Cada `LengthRecord` representa una ruta vectorial distinta. Obtén los que pretendes modificar.

```java
LengthRecord lengthRecord0 = (LengthRecord) resource.getPaths()[2];
LengthRecord lengthRecord1 = (LengthRecord) resource.getPaths()[7];
LengthRecord lengthRecord2 = (LengthRecord) resource.getPaths()[11];
```

## Paso 5: Modifica las propiedades de operación de ruta
Ahora puedes **modificar formas vectoriales PSD** cambiando sus `PathOperations`. Esto determina cómo interactúan las formas (p. ej., exclusión, intersección, sustracción).

```java
lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);
lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);
lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);
```

## Paso 6: Guarda el archivo PSD modificado
Persiste tus cambios en un nuevo archivo.

```java
psdImage.save(outPsdFilePath);
```

## Paso 7: Libera los recursos
Descarta el `PsdImage` para liberar memoria.

```java
psdImage.dispose();
```

## Cómo procesar por lotes archivos PSD con soporte de propiedades de registro de longitud
Si necesitas aplicar los mismos ajustes de forma vectorial a muchos PSD, envuelve el código anterior en un bucle que recorra un directorio de archivos. Actualiza `inPsdFilePath` y `outPsdFilePath` en cada iteración, y podrás **procesar por lotes archivos PSD** de manera eficiente.

## Problemas comunes y consejos
- **Comprobaciones de nulos** – siempre verifica que `resource` no sea `null` antes de acceder a rutas.  
- **Límites de índices de ruta** – asegúrate de que los índices que usas (`[2]`, `[7]`, `[11]`) existan en el PSD específico que estás editando.  
- **Licencia** – ejecutar sin una licencia válida incrustará una marca de agua en el PSD guardado.  

## Conclusión
Ahora tienes un ejemplo completo, de extremo a extremo, de cómo **modificar formas vectoriales PSD** soportando propiedades de registro de longitud con Aspose.PSD for Java. Ya sea que estés automatizando pipelines de activos o construyendo una herramienta de diseño personalizada, estas API te brindan la flexibilidad para manipular capas vectoriales sin trabajo manual en Photoshop. Explora más experimentando con otras `PathOperations` o combinando múltiples ediciones de `LengthRecord` para formas complejas.

## Preguntas frecuentes

**P: ¿Cómo manejo un PSD que no contiene capas de forma vectorial?**  
R: El `VsmsResource` estará ausente, por lo que `resource` permanecerá `null`. Añade una comprobación y omite el paso de modificación o informa al usuario.

**P: ¿Puedo cambiar otras propiedades como el color de relleno o el grosor del trazo?**  
R: Sí, `LengthRecord` ofrece setters adicionales para relleno, trazo y opacidad. Consulta la documentación de la API para obtener todos los detalles.

**P: ¿Es posible procesar por lotes varios archivos PSD?**  
R: Absolutamente. Envuelve el código dentro de un bucle que itere sobre un directorio de archivos PSD, ajustando las rutas de entrada y salida en cada ejecución.

**P: ¿Necesito cerrar los streams manualmente al cargar desde una ruta de archivo?**  
R: El método `Image.load` gestiona los streams de archivo internamente, pero si cargas desde un `InputStream`, recuerda cerrarlo después de usarlo.

**P: ¿Qué versión de Aspose.PSD se requiere para estas API?**  
R: Las clases `LengthRecord` y `PathOperations` están disponibles desde Aspose.PSD 20.10. Se recomienda usar la versión más reciente.

**Última actualización:** 2026-02-20  
**Probado con:** Aspose.PSD for Java 24.11  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}