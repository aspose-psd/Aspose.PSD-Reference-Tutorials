---
date: 2026-01-01
description: Explora cómo recortar imágenes en Java usando Aspose.PSD para Java. Sigue
  nuestra guía paso a paso para cargar un archivo PSD, recortar un rectángulo de la
  imagen y convertir el PSD a JPEG.
linktitle: Crop Image by Rectangle
second_title: Aspose.PSD Java API
title: 'Recortar Imagen Java: Recortar Imagen por Rectángulo con Aspose.PSD'
url: /es/java/image-editing/crop-image-by-rectangle/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Recortar Imagen Java: Recortar Imagen por Rectángulo con Aspose.PSD

## Introducción

Manipular gráficos es una parte rutinaria del **java image processing**, y Aspose.PSD for Java te brinda una API limpia y de alto rendimiento para trabajar con archivos PSD. En este tutorial aprenderás **cómo recortar una imagen** usando un rectángulo, cargar un archivo PSD y, finalmente, convertir el resultado a JPEG, todo con solo unas pocas líneas de código Java.

## Respuestas Rápidas
- **¿Qué significa “crop image java”?** Se refiere a recortar una imagen a un rectángulo definido usando código Java.  
- **¿Qué biblioteca maneja la operación?** Aspose.PSD for Java proporciona las clases necesarias.  
- **¿Necesito una licencia para pruebas?** Hay una versión de prueba gratuita; se requiere una licencia para producción.  
- **¿Puedo convertir el PSD recortado a JPEG?** Sí—usa `JpegOptions` al guardar.  
- **¿Cuánto tiempo lleva la implementación?** Generalmente menos de 10 minutos para un escenario básico.

## ¿Qué es recortar un rectángulo de imagen en Java?

Recortar un rectángulo de imagen significa seleccionar un área específica (definida por X, Y, ancho y alto) y descartar todo lo que está fuera de esa zona. Esta operación es común cuando necesitas enfocarte en una región particular de un documento PSD más grande.

## ¿Por qué usar Aspose.PSD para esta tarea?

- **Sin dependencias externas** – funciona con Java puro.  
- **Soporta PSD, PNG, JPEG y muchos otros formatos** – puedes **convertir PSD a JPEG** al instante.  
- **Renderizado de alta fidelidad** – conserva la información de capas y los perfiles de color durante el recorte.  

## Requisitos Previos

- Java Development Kit (JDK) instalado.  
- Biblioteca Aspose.PSD for Java – descárgala desde el [website](https://releases.aspose.com/psd/java/).  

## Importar Paquetes

Asegúrate de incluir los paquetes necesarios en tu proyecto Java para aprovechar las capacidades de Aspose.PSD for Java. Añade las siguientes declaraciones de importación al comienzo de tu archivo Java:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

Ahora, desglosaremos el proceso en varios pasos para guiarte en el recorte de una imagen por un rectángulo usando Aspose.PSD for Java.

## Paso 1: Configura tu Directorio de Documentos

```java
String dataDir = "Your Document Directory";
```

Reemplaza `"Your Document Directory"` con la ruta real donde se encuentra tu archivo PSD.

## Paso 2: Especifica los Archivos de Origen y Destino

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "CroppingByRectangle_out.jpg";
```

Define las rutas para tu archivo PSD de origen y el archivo JPEG de destino.

## Paso 3: Carga y Almacena en Caché la Imagen

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);

if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

Aquí **cargamos el archivo PSD** en una instancia de `RasterImage` y almacenamos sus datos en caché para mejorar el rendimiento.

## Paso 4: Crea y Define el Rectángulo de Recorte

```java
Rectangle rectangle = new Rectangle(20, 20, 20, 20);
```

Crea una instancia de la clase `Rectangle` con el tamaño deseado para el recorte. Los parámetros representan **X**, **Y**, **ancho** y **alto**, respectivamente.

## Paso 5: Recorta y Guarda la Imagen

```java
rasterImage.crop(rectangle);
rasterImage.save(destName, new JpegOptions());
```

Ejecuta la operación de recorte usando el rectángulo especificado y **convierte PSD a JPEG** guardando el resultado con `JpegOptions`.

Repite estos pasos según sea necesario, ajustando los parámetros de acuerdo a tus requisitos específicos.

## Problemas Comunes y Consejos

- **Rectángulo fuera de los límites de la imagen** – asegúrate de que las coordenadas del rectángulo estén dentro de las dimensiones de la imagen fuente.  
- **Consumo de memoria** – llama a `rasterImage.dispose()` después de terminar para liberar recursos nativos.  
- **Control de calidad** – puedes establecer `JpegOptions.setQuality(int)` para controlar el nivel de compresión del JPEG de salida.

## Conclusión

En este tutorial recorrimos el proceso de **crop image java** por un rectángulo usando Aspose.PSD for Java. Siguiendo estos pasos puedes integrar fácilmente potentes capacidades de manipulación de imágenes—cargar un archivo PSD, recortar una región específica y convertir el resultado a JPEG—en cualquier aplicación Java.

## Preguntas Frecuentes

### P1: ¿Puedo usar Aspose.PSD for Java con otros frameworks Java?

Sí, Aspose.PSD for Java puede integrarse con varios frameworks Java, proporcionando flexibilidad en tus proyectos de desarrollo.

### P2: ¿Hay una versión de prueba gratuita disponible para Aspose.PSD for Java?

Sí, puedes acceder a la versión de prueba gratuita [aquí](https://releases.aspose.com/).

### P3: ¿Dónde puedo encontrar soporte o asistencia adicional?

Visita el [foro de Aspose.PSD](https://forum.aspose.com/c/psd/34) para soporte comunitario y discusiones.

### P4: ¿Cómo obtengo una licencia temporal para Aspose.PSD for Java?

Puedes obtener una licencia temporal [aquí](https://purchase.aspose.com/temporary-license/).

### P5: ¿Cuáles son los formatos de imagen compatibles para recortar en Aspose.PSD for Java?

Aspose.PSD for Java soporta varios formatos de imagen, incluidos PSD, PNG, JPEG y más.

---

**Última actualización:** 2026-01-01  
**Probado con:** Aspose.PSD for Java 24.12  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}