---
date: 2026-03-13
description: Aprende a crear proyectos Java de imágenes PSD mientras gestionas la
  reasignación de caché con Aspose.PSD para Java. Optimiza el uso de memoria y disco
  de manera eficiente.
linktitle: Create PSD Image Java – Control Cache Reallocation
second_title: Aspose.PSD Java API
title: Crear imagen PSD en Java – Control de la reasignación de caché
url: /es/java/modifying-converting-psd-images/control-cache-reallocation-psd-files/
weight: 22
---

_X}} unchanged.

Also keep markdown formatting.

Now write final answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Controlar la reasignación de caché en archivos PSD

## Introducción
Si necesitas **create PSD image java** proyectos de manera eficiente, controlar la reasignación de caché es esencial. Cuando trabajas con imágenes y archivos de Photoshop de forma programática, la eficiencia es un factor clave. Aspose.PSD for Java ofrece funciones robustas para gestionar y manipular archivos PSD sin problemas. Uno de los aspectos fundamentales para optimizar el rendimiento es controlar la reasignación de caché. La gestión de caché ayuda a mantener el equilibrio entre el uso de memoria y disco, garantizando que tu aplicación se ejecute sin interrupciones, sin bloqueos inesperados ni ralentizaciones.

## Respuestas rápidas
- **¿Qué hace la reasignación de caché?** Equilibra el uso de memoria y disco mientras se procesan archivos PSD grandes.  
- **¿Qué tipo de caché es mejor para imágenes grandes?** `CacheOnDiskOnly` mantiene la memoria libre almacenando la caché en disco.  
- **¿Cuánto espacio en disco puedo asignar?** Hasta 1 GB (o cualquier tamaño que establezcas con `setMaxDiskSpaceForCache`).  
- **¿Necesito una licencia para usar estas funciones?** Una licencia elimina las limitaciones de la versión de prueba; consulta la página de compra de Aspose.  
- **¿Puedo monitorizar el uso de caché en tiempo de ejecución?** Sí, usa `Cache.getAllocatedDiskBytesCount()` y `Cache.getAllocatedMemoryBytesCount()`.

## ¿Por qué controlar la reasignación de caché?
Gestionar la caché es crucial cuando **create PSD image java** aplicaciones que manejan archivos de alta resolución o con múltiples capas. Una configuración adecuada de la caché previene errores de falta de memoria, reduce las pausas del recolector de basura y brinda un rendimiento predecible en servidores o aplicaciones de escritorio.

## Requisitos previos
Antes de pasar a la parte de codificación, hay algunas cosas que debes asegurar para que todo funcione sin problemas:
1. **Java Development Kit (JDK):** Asegúrate de tener el JDK instalado en tu máquina. Puedes descargarlo desde [sitio web de Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java:** Necesitas descargar la biblioteca Aspose.PSD. Puedes encontrar la última versión [aquí](https://releases.aspose.com/psd/java/).  
3. **Configuración del IDE:** Un Entorno de Desarrollo Integrado (IDE) como IntelliJ IDEA o Eclipse facilitará la gestión de tu código.  
4. **Conocimientos básicos de Java:** Familiarizarte con la programación en Java te ayudará a comprender mejor los conceptos y fragmentos de código.  
5. **Licencia de Aspose (Opcional):** Si deseas eliminar marcas de agua y obtener la funcionalidad completa, considera comprar una licencia [aquí](https://purchase.aspose.com/buy) o probar la versión de prueba gratuita [aquí](https://releases.aspose.com/).

## Importar paquetes
Antes de comenzar a escribir el código, asegurémonos de que tenemos los paquetes necesarios importados. A continuación se muestra una breve lista de lo que debes incluir al inicio de tu archivo Java:
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

## Cómo crear PSD Image Java con control de caché
A continuación se presenta una guía paso a paso que vincula la configuración de la caché directamente al proceso de creación de una imagen PSD en Java.

### Paso 1: Configurar tu directorio de datos
Lo primero es establecer un directorio donde se almacenarán los archivos de caché. Esto es esencial para gestionar la caché de manera eficaz.
```java
String dataDir = "Your Document Directory";
Cache.setCacheFolder(dataDir);
```

- `String dataDir`: Define el directorio para la caché de tu documento.  
- `Cache.setCacheFolder(dataDir)`: Este método establece la carpeta de caché en el directorio especificado. Cualquier caché creada por Aspose se almacenará aquí en lugar del directorio temporal predeterminado.

### Paso 2: Configurar la caché en disco
A continuación, especificaremos que queremos que la caché se almacene solo en disco. Esto es particularmente útil si tu aplicación maneja archivos grandes y deseas que la memoria permanezca libre.
```java
Cache.setCacheType(CacheType.CacheOnDiskOnly);
```

- `Cache.setCacheType(CacheType.CacheOnDiskOnly)`: Esta opción garantiza que la caché no se mantenga en memoria, lo que resulta beneficioso para manejar archivos PSD grandes sin consumir demasiada RAM.

### Paso 3: Establecer el tamaño máximo de caché en disco y en memoria
Ahora, restrinjamos los tamaños de la caché. Esto es crucial porque una caché ilimitada puede provocar problemas de rendimiento.
```java
Cache.setMaxDiskSpaceForCache(1073741824); // 1 gigabyte
Cache.setMaxMemoryForCache(1073741824); // 1 gigabyte
```

- `Cache.setMaxDiskSpaceForCache(1073741824)`: Establece un límite de 1 GB para la caché en disco. Puedes ajustar este tamaño según tus necesidades.  
- `Cache.setMaxMemoryForCache(1073741824)`: De forma similar, limita la caché en memoria, asegurando que tu aplicación no use una cantidad excesiva de memoria.

### Paso 4: Gestionar la estrategia de reasignación de caché
Gestionar cómo se reasigna la caché es esencial para mantener el rendimiento. Así es como puedes configurarlo.
```java
Cache.setExactReallocateOnly(false);
```

- `Cache.setExactReallocateOnly(false)`: Cuando se establece en `false`, permite que Aspose gestione la reasignación de caché de forma más flexible, lo que puede traducirse en un mejor rendimiento.

### Paso 5: Verificar el tamaño de caché asignado
Este paso consiste en monitorizar cuántos bytes están actualmente asignados a la caché en memoria o en disco. Implementémoslo:
```java
long l1 = Cache.getAllocatedDiskBytesCount();
long l2 = Cache.getAllocatedMemoryBytesCount();
```

- `long l1`: Almacena el recuento de bytes asignados en el disco.  
- `long l2`: Almacena el recuento de bytes asignados en memoria.  
Puedes comprobar estos valores en cualquier momento para asegurarte de que tu aplicación gestiona la memoria y el uso de disco como se espera.

### Paso 6: Crear una imagen PSD
Ahora que tenemos nuestras configuraciones de caché listas, creemos una imagen PSD sencilla.
```java
PsdOptions options = new PsdOptions();
Color[] color = { Color.getRed(), Color.getBlue(), Color.getBlack(), Color.getWhite() };
options.setPalette(new ColorPalette(color));
options.setSource(new StreamSource(new ByteArrayInputStream(new byte[0])));
RasterImage image = (RasterImage) Image.create(options, 100, 100);
```

- `PsdOptions options`: Este objeto permite especificar opciones al crear una imagen de Photoshop.  
- `Color[] color`: Una matriz que contiene los colores que se usarán en la paleta de la imagen.

### Paso 7: Guardar datos de píxeles en la imagen
Ahora, rellenemos nuestra imagen con datos de píxeles y guardémosla.
```java
Color[] pixels = new Color[10000];
for (int i = 0; i < pixels.length; i++) {
    pixels[i] = Color.getWhite();
}
image.savePixels(image.getBounds(), pixels);
```

- `Color[] pixels`: Es una matriz de objetos de color. Aquí la llenamos con píxeles blancos.  
- `image.savePixels(image.getBounds(), pixels)`: Este método guarda los datos de píxeles en la imagen. Actualiza la imagen con los colores que hemos definido.

### Paso 8: Monitorizar la caché asignada después de crear la imagen
Después de crear la imagen, es una buena práctica volver a comprobar cuántos bytes están asignados a la caché.
```java
long diskBytes = Cache.getAllocatedDiskBytesCount();
long memoryBytes = Cache.getAllocatedMemoryBytesCount();
```

- `long diskBytes`: Captura la asignación actual en disco después de la creación de la imagen.  
- `long memoryBytes`: Captura la asignación actual en memoria.  
Este paso te ayudará a determinar cuánta caché se está consumiendo tras tus operaciones.

### Paso 9: Verificar la eliminación adecuada
Por último, es fundamental asegurarse de que todos los objetos de Aspose.PSD se hayan eliminado correctamente para evitar fugas de memoria.
```java
l1 = Cache.getAllocatedDiskBytesCount();
l2 = Cache.getAllocatedMemoryBytesCount();
```

- `l1` y `l2`: Estas variables te ayudarán a comprobar la asignación final. Si no son cero, indica que algunos objetos no se han eliminado adecuadamente.

## Problemas comunes y soluciones
- **Carpeta de caché no creada** – Verifica que la aplicación tenga permisos de escritura para la ruta que pasaste a `Cache.setCacheFolder`.  
- **Errores de falta de memoria** – Asegúrate de que `Cache.setCacheType(CacheType.CacheOnDiskOnly)` esté aplicado antes de cargar archivos PSD grandes.  
- **Tamaño de caché inesperado** – Utiliza los métodos `Cache.getAllocated*BytesCount()` después de cada operación importante para rastrear el crecimiento.

## Preguntas frecuentes

**P: ¿Qué es Aspose.PSD?**  
R: Aspose.PSD es una biblioteca para desarrolladores .NET y Java que permite crear, manipular y convertir archivos Photoshop (PSD) de forma programática.

**P: ¿Cómo puedo comprobar el tamaño de caché asignado?**  
R: Usa métodos como `Cache.getAllocatedDiskBytesCount()` y `Cache.getAllocatedMemoryBytesCount()` para monitorizar el uso actual de la caché.

**P: ¿Puedo establecer un directorio personalizado para la caché?**  
R: Sí, puedes especificar un directorio diferente usando `Cache.setCacheFolder("Your Directory Path")`.

**P: ¿Aspose.PSD es gratuito?**  
R: Aspose.PSD es una biblioteca de pago, pero puedes comenzar con una prueba gratuita disponible en su [sitio web](https://releases.aspose.com/).

**P: ¿Qué ocurre si no elimino los objetos?**  
R: No eliminar los objetos puede provocar fugas de memoria, haciendo que tu aplicación use más recursos de los necesarios.

## Conclusión
Controlar la reasignación de caché mientras **create PSD image java** aplicaciones puede marcar una diferencia significativa en el rendimiento. Siguiendo los pasos anteriores, gestionarás la caché de manera eficiente, minimizarás el consumo de memoria y generarás archivos PSD de alta calidad con Aspose.PSD for Java. Aplica estas técnicas y tus proyectos funcionarán de forma más fluida y escalable.

---

**Última actualización:** 2026-03-13  
**Probado con:** Aspose.PSD for Java (última versión)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}