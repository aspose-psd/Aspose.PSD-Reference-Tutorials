---
title: Admite recursos Vmsk en archivos PSD con Java
linktitle: Admite recursos Vmsk en archivos PSD con Java
second_title: API de Java Aspose.PSD
description: Administre sin esfuerzo los recursos de Vmsk en archivos PSD usando Aspose.PSD para Java. Un tutorial completo paso a paso ideal tanto para desarrolladores como para diseñadores.
weight: 23
url: /es/java/advanced-psd-layer-features-effects/support-vmsk-resource-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Admite recursos Vmsk en archivos PSD con Java

## Introducción
Cuando se trata de trabajar con archivos PSD (Documento de Photoshop), administrar los recursos es crucial, especialmente cuando se integran funciones especiales como el recurso Vmsk (Máscara vectorial). Los recursos de Vmsk pueden empoderar a los diseñadores agregando formas vectoriales complejas, permitiéndoles crear gráficos impresionantes sin esfuerzo. En esta guía, adoptaremos un enfoque práctico para mostrarle cómo admitir recursos de Vmsk en archivos PSD usando Aspose.PSD para Java. Ya sea que sea un desarrollador que busca mejorar su aplicación o un diseñador que busca automatización, este tutorial lo guiará a través del proceso paso a paso, haciéndolo fácil de seguir e implementar.
## Requisitos previos
Antes de profundizar en los jugosos detalles del manejo de los recursos de Vmsk, asegurémonos de que tiene todo listo para una experiencia perfecta.
### Lo que necesitas
-  Kit de desarrollo de Java (JDK): asegúrese de tener JDK instalado en su máquina. Si no, puedes descargarlo desde[sitio web de oráculo](https://www.oracle.com/java/technologies/javase-downloads.html).
- Biblioteca Aspose.PSD para Java: esta es una poderosa biblioteca para administrar archivos PSD. Puedes descargarlo desde el[Página de lanzamiento de Aspose](https://releases.aspose.com/psd/java/) . Para aquellos que quieran probar antes de comprar, también pueden comenzar con el[prueba gratuita](https://releases.aspose.com/).
- Un IDE: cualquier IDE para Java (como IntelliJ IDEA, Eclipse, etc.) funcionará para este proyecto.
### Configurando su espacio de trabajo
1. Cree un nuevo proyecto Java: inicie su IDE preferido y cree un nuevo proyecto Java. Este es su campo de juego para trabajar con el código.
2. Agregue la biblioteca Aspose: después de descargar la biblioteca Aspose, agregue el archivo jar a las bibliotecas de su proyecto. Este paso es crucial ya que nos permite utilizar todas esas características interesantes de Aspose.PSD.
Con estos requisitos previos implementados, está listo para comenzar a crear, modificar y administrar archivos PSD con recursos de Vmsk. ¡Vayamos directamente a la programación!
## Importar paquetes
Antes de poder trabajar con archivos PSD, debemos importar los paquetes necesarios. Esta es la columna vertebral de nuestro código y nos da acceso a varias clases y métodos que ofrece la biblioteca Aspose.PSD.
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
Ahora que hemos preparado el escenario, ¡es hora de actuar! En esta sección, dividiremos el código en pasos manejables. Estos pasos lo guiarán a través de la lectura de un archivo PSD, el manejo del recurso Vmsk e incluso su edición.
## Paso 1: cargue su archivo PSD
Lo primero que debes hacer es cargar tu archivo PSD. Aquí es donde comienza toda la magia.
```java
String dataDir = "Your Document Directory"; // Actualizar esta ruta
String sourceFileName = dataDir + "Rectangle.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

-  fijamos el`dataDir` al directorio de su archivo PSD. 
-  Creamos una cadena para el`sourceFileName`, combinando el directorio con el nombre del archivo PSD.
-  Finalmente, cargamos el archivo PSD en un`PsdImage` objeto usando`Image.load()`.
## Paso 2: recuperar el recurso Vmsk
Ahora que tenemos nuestra imagen PSD cargada, busquemos el recurso Vmsk.
```java
VmskResource resource = getVmskResource(im);
```

-  llamamos al`getVmskResource()` Método que maneja la búsqueda y recuperación del recurso Vmsk de la imagen.
## Paso 3: Validar las propiedades del recurso Vmsk
Antes de proceder con las modificaciones, es fundamental validar que nuestro recurso Vmsk se encuentre en el estado esperado.
```java
if (resource.isDisabled() != false ||
	resource.isInverted() != false ||
	resource.isNotLinked() != false ||
	resource.getPaths().length != 7) {
	throw new RuntimeException("VmskResource was read wrong");
}
```

- Aquí, comprobamos varias propiedades del recurso Vmsk. Queremos asegurarnos de que no esté deshabilitado, invertido o no vinculado, y que tenga la cantidad correcta de rutas.
## Paso 4: acceda a cada ruta y valide
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

- Estamos extrayendo tres registros de ruta específicos y validando sus tipos y propiedades para garantizar que cumplan con nuestros criterios.
## Paso 5: edite el recurso Vmsk
¡Ahora entramos en la parte de modificación! Puede modificar las propiedades del recurso Vmsk según sea necesario.
```java
resource.setDisabled(true);
resource.setInverted(true);
resource.setNotLinked(true);
```

- En este bloque, alternaremos varias propiedades del recurso Vmsk. Al configurarlos en verdadero, podemos controlar cómo se comporta la máscara en el archivo PSD.
## Paso 6: modificar los puntos del nudo Bézier
Los nudos Bézier son críticos para las rutas vectoriales. Cambiemos algunos valores aquí.
```java
BezierKnotRecord bezierKnot = (BezierKnotRecord) resource.getPaths()[3];
bezierKnot.getPoints()[0] = new Point(0, 0);
bezierKnot = (BezierKnotRecord) resource.getPaths()[4];
bezierKnot.getPoints()[0] = new Point(8039797, 10905190);
```

-  Estamos accediendo a específicos`BezierKnotRecord` rutas y cambiando sus puntos para remodelar potencialmente la máscara vectorial.
## Paso 7: guarde el archivo PSD modificado
Una vez completadas todas las ediciones, es hora de guardar el archivo PSD modificado. 
```java
String exportPath = dataDir + "Rectangle_changed.psd";
im.save(exportPath);
```

-  Establecemos la ruta para el archivo PSD exportado y luego llamamos`im.save()` para escribir los cambios en este nuevo archivo.
## Paso 8: Limpiar recursos
Finalmente, debemos asegurarnos de desechar correctamente la imagen para liberar recursos.
```java
im.dispose();
```

- Siempre es una buena práctica deshacerse de los recursos una vez que haya terminado. Esto ayuda a evitar pérdidas de memoria en sus aplicaciones.
## Conclusión
¡Felicidades! Acaba de pasar por un proceso detallado de compatibilidad con recursos de Vmsk en archivos PSD utilizando Aspose.PSD para Java. Desde cargar la imagen, recuperar y validar el recurso Vmsk, editar sus propiedades y luego guardar su PSD modificado, ha cubierto lo esencial. Con estas habilidades, puede administrar y utilizar de manera eficiente varios recursos dentro de archivos PSD, mejorando sus proyectos de diseño gráfico o scripts de automatización.
## Preguntas frecuentes
### ¿Qué es un recurso Vmsk?
Un recurso Vmsk es una máscara vectorial en un archivo PSD que permite formas vectoriales complejas y funciones de edición.
### ¿Puedo usar Aspose.PSD en un proyecto Maven?
Sí, puedes incluir Aspose.PSD como una dependencia en tu proyecto Maven usando sus coordenadas del repositorio.
### ¿En qué formato puedo guardar mis archivos PSD modificados?
Puede guardarlos como archivos PSD o exportarlos a otros formatos como PNG, JPEG, etc.
### ¿Hay una prueba gratuita disponible para Aspose.PSD?
 Sí, puede acceder a una prueba gratuita de Aspose.PSD para probar sus funciones. Visita el[enlace de prueba gratuito](https://releases.aspose.com/).
### ¿Cómo puedo obtener soporte para Aspose.PSD?
 Puedes unirte al[asponer foro](https://forum.aspose.com/c/psd/34)para obtener soporte y ayuda para la solución de problemas.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
