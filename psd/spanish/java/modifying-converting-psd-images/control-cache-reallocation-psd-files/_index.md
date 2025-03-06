---
title: Controlar la reasignación de caché en archivos PSD
linktitle: Controlar la reasignación de caché en archivos PSD
second_title: API de Java Aspose.PSD
description: Administre la reasignación de caché en archivos PSD usando Aspose.PSD para Java. Aprenda cómo optimizar la memoria y el manejo de archivos de manera eficiente, ideal para desarrolladores.
weight: 22
url: /es/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Controlar la reasignación de caché en archivos PSD

## Introducción
Cuando se trabaja con imágenes y archivos de Photoshop mediante programación, la eficiencia es un factor clave. Aspose.PSD para Java ofrece funciones sólidas para administrar y manipular archivos PSD sin problemas. Uno de los aspectos fundamentales para optimizar el rendimiento es controlar la reasignación de caché. La administración de caché ayuda a mantener el equilibrio entre el uso de la memoria y el disco, lo que garantiza que su aplicación se ejecute sin problemas, sin fallas ni desaceleraciones inesperadas. 
## Requisitos previos
Antes de pasar a la parte de codificación, hay algunas cosas que debes asegurar para que todo funcione sin problemas:
1. Kit de desarrollo de Java (JDK): asegúrese de tener JDK instalado en su máquina. Puedes descargarlo desde[sitio web de oráculo](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.PSD para Java: debe descargar la biblioteca Aspose.PSD. Puedes encontrar la última versión.[aquí](https://releases.aspose.com/psd/java/).
3. Configuración de IDE: un entorno de desarrollo integrado (IDE) como IntelliJ IDEA o Eclipse le facilitará la gestión de su código.
4. Comprensión básica de Java: la familiaridad con la programación Java le ayudará a comprender mejor los conceptos y fragmentos de código.
5.  Licencia Aspose (opcional): si desea eliminar marcas de agua y obtener funcionalidad completa, considere comprar una licencia[aquí](https://purchase.aspose.com/buy) o probar la prueba gratuita[aquí](https://releases.aspose.com/).
## Importar paquetes
Antes de comenzar a escribir el código, asegurémonos de haber importado los paquetes necesarios. A continuación se muestra una breve lista de lo que debe incluir al principio de su archivo Java:
```java
import com.aspose.psd.Cache;
import com.aspose.psd.CacheType;
import com.aspose.psd.Color;
import com.aspose.psd.ColorPalette;
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.imageoptions.GifOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.StreamSource;
import com.aspose.psd.system.io.MemoryStream;
```
## Paso 1: configurar su directorio de datos
Lo primero es lo primero: deberá configurar un directorio donde desea que se almacenen sus archivos de caché. Esto es esencial para gestionar la caché de forma eficaz.
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- String dataDir: define el directorio para la caché de documentos.
- Cache.setCacheFolder(dataDir): este método establece la carpeta de caché en el directorio especificado. Cualquier caché creado por Aspose ahora se almacenará aquí en lugar del directorio temporal predeterminado.
## Paso 2: configurar la caché en el disco
A continuación, especificaremos que queremos que nuestro caché se almacene solo en el disco. Esto es particularmente útil si su aplicación utiliza archivos grandes y desea asegurarse de que la memoria permanezca libre.
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- Cache.setCacheType(CacheType.CacheOnDiskOnly): esta opción garantiza que el caché no se mantenga en la memoria, lo que resulta beneficioso para manejar archivos PSD de gran tamaño sin consumir demasiada RAM.
## Paso 3: Configurar el tamaño máximo de disco y memoria caché
Ahora, restrinjamos el tamaño de nuestra caché. Esto es crucial porque el caché ilimitado puede provocar problemas de rendimiento.
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1 gigabyte
Cache.setMaxMemoryForCache(1073741824); // 1 gigabyte
```

- Cache.setMaxDiskSpaceForCache(1073741824): esto establece un límite de 1 GB para el caché en el disco. Puedes ajustar este tamaño dependiendo de tus necesidades.
- Cache.setMaxMemoryForCache(1073741824): de manera similar, esto limita el caché en memoria, lo que garantiza que su aplicación no utilice memoria excesiva.
## Paso 4: Administrar la estrategia de reasignación de caché
Administrar cómo se reasigna la memoria caché es esencial para mantener el rendimiento. Así es como puedes configurarlo.
```java
Cache.setExactReallocateOnly(false);
```

- Cache.setExactReallocateOnly(false): cuando se establece en false, esto permite a Aspose administrar la reasignación de caché de manera más flexible, lo que puede conducir a un mejor rendimiento.
## Paso 5: Verifique el tamaño de caché asignado
Este paso consiste en monitorear cuántos bytes están asignados actualmente para el caché en la memoria o en el disco. Implementemos eso:
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- long l1: almacena el recuento de bytes asignados en el disco.
- long l2: almacena el recuento de bytes asignados en la memoria. 
Puede verificar estos valores en cualquier momento para asegurarse de que su aplicación administre el uso de la memoria y el disco como se esperaba.
## Paso 6: crear una imagen PSD
Ahora que tenemos nuestras configuraciones de caché configuradas, creemos una imagen PSD simple.
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- Opciones de PsdOptions: este objeto le permite especificar opciones al crear una imagen de Photoshop.
- Color[] color: una matriz que contiene los colores que se utilizarán en la paleta de imágenes.
## Paso 7: guardar datos de píxeles en la imagen
Ahora, completemos nuestra imagen con datos de píxeles y guárdela.
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- Color[] píxeles: es una matriz de objetos de color. Aquí lo estamos llenando con píxeles blancos.
- image.savePixels(image.getBounds(), pixels): este método guarda los datos de píxeles en la imagen. Actualiza la imagen con los colores que hemos definido.
## Paso 8: Monitorear el caché asignado después de la creación de la imagen
Después de crear la imagen, es una buena práctica comprobar nuevamente cuántos bytes están asignados para el caché.
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- long diskBytes: captura la asignación actual en el disco después de la creación de la imagen.
- long MemoryBytes: captura la asignación actual en la memoria. 
Este paso le ayudará a determinar cuánto caché se consume después de sus operaciones.
## Paso 9: verifique la eliminación adecuada
Por último, es crucial asegurarse de que todos los objetos Aspose.PSD se eliminen correctamente para evitar pérdidas de memoria.
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- l1 y l2: Estas variables te ayudarán a comprobar la asignación final. Si no son cero, indica que algunos objetos no se han eliminado correctamente.
## Conclusión
Controlar la reasignación de caché en Aspose.PSD para Java puede marcar una diferencia significativa en el rendimiento de su aplicación. Si sigue los pasos descritos anteriormente, puede administrar eficazmente el caché, minimizar el uso de memoria y crear hermosos archivos PSD de manera eficiente. Adopte estas técnicas y observe cómo sus aplicaciones prosperan con un rendimiento óptimo.
## Preguntas frecuentes
### ¿Qué es Aspose.PSD?
Aspose.PSD es una biblioteca para que los desarrolladores de .NET y Java creen, manipulen y conviertan archivos de Photoshop (PSD) mediante programación.
### ¿Cómo verifico el tamaño de la caché asignada?
 Utilice métodos como`Cache.getAllocatedDiskBytesCount()` y`Cache.getAllocatedMemoryBytesCount()` para monitorear el uso actual de la caché.
### ¿Puedo configurar un directorio personalizado para el caché?
 Sí, puede especificar un directorio diferente usando`Cache.setCacheFolder("Your Directory Path")`.
### ¿Aspose.PSD es de uso gratuito?
Aspose.PSD es una biblioteca paga, pero puedes comenzar con una prueba gratuita disponible en su[sitio web](https://releases.aspose.com/).
### ¿Qué pasa si no me deshago de los objetos?
No deshacerse de los objetos puede provocar pérdidas de memoria, lo que hace que su aplicación utilice más recursos de los necesarios.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
