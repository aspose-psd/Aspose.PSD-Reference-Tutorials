---
date: 2025-12-18
description: Aprenda a crear una máscara vectorial (recurso Vmsk) en archivos PSD
  usando Aspose.PSD para Java. Este tutorial paso a paso le muestra cómo agregar una
  máscara vectorial, convertir PSD a PNG y más.
linktitle: Create Vector Mask (Vmsk Resource) in PSD Files with Java
second_title: Aspose.PSD Java API
title: Crear máscara vectorial (recurso Vmsk) en archivos PSD con Java
url: /es/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crear máscara vectorial (recurso Vmsk) en archivos PSD con Java

## Introducción
Si necesitas **crear máscara vectorial** (Vmsk) recursos dentro de archivos Photoshop (PSD), Aspose.PSD para Java te ofrece una forma limpia y programática de hacerlo. Ya sea que estés construyendo una herramienta de automatización de diseño o añadiendo soporte de máscara personalizada a una canalización gráfica existente, este tutorial te guía paso a paso: cargar un PSD, leer el recurso Vmsk, ajustar sus propiedades y guardar el resultado. Al final, estarás cómodo manejando máscaras vectoriales, convirtiendo PSD a PNG y ampliando el archivo con datos vectoriales adicionales.

## Respuestas rápidas
- **¿Qué es un recurso Vmsk?** Es el dato de máscara vectorial almacenado dentro de un archivo PSD, que define formas vectoriales complejas para una capa.  
- **¿Qué biblioteca lo soporta?** Aspose.PSD para Java proporciona acceso completo de lectura/escritura a los recursos Vmsk.  
- **¿Necesito una licencia?** Hay una prueba gratuita disponible; se requiere una licencia comercial para uso en producción.  
- **¿Puedo convertir el PSD editado a PNG?** Sí, una vez guardado, puedes cargar el PSD y exportarlo a PNG con la misma API.  
- **¿Hay soporte para Maven?** Absolutamente; Aspose.PSD puede añadirse como una dependencia Maven (ver la palabra clave “aspose psd maven”).

## ¿Qué es una máscara vectorial (recurso Vmsk)?
Una máscara vectorial (Vmsk) es una máscara no basada en píxeles que utiliza curvas Bézier y registros de ruta para definir regiones transparentes y opacas en una capa. Al ser vectorial, se escala sin pérdida de calidad, lo que la hace perfecta para gráficos de alta resolución.

## ¿Por qué crear una máscara vectorial con Aspose.PSD?
- **Automatización:** Añade o modifica máscaras programáticamente sin abrir Photoshop.  
- **Consistencia:** Garantiza que cada PSD que generes siga las mismas reglas de máscara.  
- **Multiplataforma:** Funciona en cualquier SO que soporte Java.  
- **Integración:** Combínalo con otras APIs de Aspose (p. ej., convertir PSD → PNG) para flujos de trabajo de extremo a extremo.

## Requisitos previos
Antes de sumergirnos en el código, asegúrate de contar con lo siguiente:

### Qué necesitas
- **Java Development Kit (JDK):** Asegúrate de tener el JDK instalado en tu máquina. Si no, puedes descargarlo del [sitio web de Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).
- **Aspose.PSD para Java:** Esta es una biblioteca potente para gestionar archivos PSD. Puedes descargarla desde la [página de lanzamientos de Aspose](https://releases.aspose.com/psd/java/). Para quienes quieran probar antes de comprar, también puedes iniciar con la [prueba gratuita](https://releases.aspose.com/).
- **Un IDE:** Cualquier IDE para Java (como IntelliJ IDEA, Eclipse, etc.) funcionará para este proyecto.

### Configurando su espacio de trabajo
1. **Crear un nuevo proyecto Java** – Abre tu IDE preferido y comienza un proyecto nuevo.  
2. **Agregar la biblioteca Aspose** – Después de descargar el JAR de Aspose, añádelo a la ruta de compilación de tu proyecto para que puedas acceder a todas las clases relacionadas con PSD.

Con el entorno listo, pasemos a la implementación real.

## Cómo crear una máscara vectorial en archivos PSD con Java
A continuación tienes una guía paso a paso. Los bloques de código permanecen sin cambios respecto al tutorial original; solo hemos añadido texto explicativo para que cada paso quede perfectamente claro.

## Importar paquetes
Antes de poder trabajar con archivos PSD, necesitamos importar las clases necesarias de la biblioteca Aspose.PSD.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Point;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.VmskResource;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.BezierKnotRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.InitialFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.LengthRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.PathFillRuleRecord;
import com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathType;
```

Ahora que hemos preparado el escenario, repasemos cada operación.

## Paso 1: Cargar su archivo PSD
Lo primero que debes hacer es cargar tu archivo PSD. Aquí es donde comienza toda la magia.

```java
String dataDir = "Your Document Directory"; // Update this path
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- Establecemos `dataDir` al directorio de tu archivo PSD.  
- Creamos una cadena para `sourceFileName`, combinando el directorio con el nombre del archivo PSD.  
- Finalmente, cargamos el archivo PSD en un objeto `PsdImage` usando `Image.load()`.

## Paso 2: Recuperar el recurso Vmsk
Ahora que tenemos la imagen PSD cargada, vamos a obtener el recurso Vmsk.

```java
VmskResource resource = getVmskResource(im);
```

- Llamamos al método `getVmskResource()` que se encarga de buscar y recuperar el recurso Vmsk de la imagen.

## Paso 3: Validar las propiedades del recurso Vmsk
Antes de proceder con modificaciones, es esencial validar que nuestro recurso Vmsk esté en el estado esperado.

```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- Aquí verificamos varias propiedades del recurso Vmsk. Queremos asegurarnos de que no esté deshabilitado, invertido o no vinculado, y que tenga el número correcto de rutas.

## Paso 4: Acceder a cada ruta y validar
Profundicemos un poco más e inspeccionemos las rutas dentro del recurso Vmsk.

```java
PathFillRuleRecord pathFillRule = (PathFillRuleRecord) resource.getPaths()[0];
InitialFillRuleRecord initialFillRule = (InitialFillRuleRecord) resource.getPaths()[1];
LengthRecord subpathLength = (LengthRecord) resource.getPaths()[2];
if (pathFillRule.getType() != VectorPathType.PathFillRuleRecord ||
	initialFillRule.getType() != VectorPathType.InitialFillRuleRecord ||
	initialFillRule.isFillStartsWithAllPixels() != false ||
	subpathLength.getType() != VectorPathType.ClosedSubpathLengthRecord ||
	subpathLength.isClosed() != true) {
	throw new RuntimeException("VmskResource paths were read wrong");
}
```

- Extraemos tres registros de ruta específicos y validamos sus tipos y propiedades para asegurarnos de que cumplen con nuestros criterios.

## Paso 5: Editar el recurso Vmsk
¡Ahora entramos en la parte de modificación! Puedes ajustar las propiedades del recurso Vmsk según sea necesario.

```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- En este bloque, alternamos varias propiedades del recurso Vmsk. Al establecerlas en `true`, podemos controlar cómo se comporta la máscara en el archivo PSD.

## Paso 6: Modificar los puntos de nudos Bézier
Los nudos Bézier son críticos para las rutas vectoriales. Cambiemos algunos valores aquí.

```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

- Accedemos a rutas específicas de `BezierKnotRecord` y cambiamos sus puntos para potencialmente remodelar la máscara vectorial.

## Paso 7: Guardar el archivo PSD modificado
Una vez completadas todas las ediciones, es hora de guardar el archivo PSD modificado.

```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

- Definimos la ruta para el PSD exportado y luego llamamos a `im.save()` para escribir los cambios en este nuevo archivo.

## Paso 8: Limpiar los recursos
Finalmente, debemos asegurarnos de disponer correctamente de la imagen para liberar recursos.

```java
im.dispose();
```

- Siempre es una buena práctica liberar cualquier recurso una vez que hayas terminado. Esto ayuda a evitar fugas de memoria en tus aplicaciones.

## Conclusión
¡Felicidades! Acabas de recorrer un proceso detallado de **creación de máscara vectorial** (Vmsk) en archivos PSD usando Aspose.PSD para Java. Desde cargar la imagen, recuperar y validar el recurso Vmsk, editar sus propiedades, hasta guardar tu PSD modificado, ahora tienes una base sólida para automatizar flujos de trabajo de máscaras vectoriales. Usa estas técnicas para enriquecer tus canalizaciones de diseño, integrarlas con otras APIs de Aspose (como convertir PSD a PNG) o crear herramientas gráficas personalizadas.

## Preguntas frecuentes
**P: ¿Cómo añado una nueva máscara vectorial a una capa existente?**  
R: Crea un `VmskResource`, puebla con los registros de ruta necesarios (p. ej., `BezierKnotRecord`) y adjúntalo a la colección de recursos de la capa.

**P: ¿Puedo convertir el PSD editado directamente a PNG sin abrir Photoshop?**  
R: Sí, después de guardar el PSD, cárgalo nuevamente con `Image.load()` y llama a `im.save("output.png")` especificando el formato PNG.

**P: ¿Existe una forma de automatizar esto en una canalización CI/CD?**  
R: Absolutamente. Como el proceso es puro Java, puedes incorporarlo en builds de Maven/Gradle, contenedores Docker o cualquier sistema CI que soporte Java.

**P: ¿Qué versiones de Aspose.PSD son compatibles con Java 11+?**  
R: Todas las versiones recientes (2024‑2025) soportan Java 8 y superiores, incluyendo Java 11, 17 y versiones LTS más nuevas.

**P: ¿Necesito una licencia para compilaciones de desarrollo?**  
R: Una licencia de evaluación gratuita funciona para desarrollo y pruebas. Para despliegues en producción, se requiere una licencia comercial.

---

**Last Updated:** 2025-12-18  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
