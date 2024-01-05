---
title: Girar una imagen en Aspose.PSD para Java
linktitle: Girar una imagen
second_title: API de Java Aspose.PSD
description: Explore la rotación de imágenes en Java sin esfuerzo con Aspose.PSD. Gire, voltee y guarde archivos PSD fácilmente.
type: docs
weight: 19
url: /es/java/advanced-image-manipulation/rotate-image/
---
## Introducción

Aspose.PSD para Java proporciona un potente conjunto de funciones para trabajar con imágenes, lo que permite a los desarrolladores manipular y procesar archivos PSD de manera eficiente. En este tutorial, nos centraremos en una tarea específica: rotar una imagen. Ya sea que esté creando una aplicación de edición de fotografías o simplemente necesite ajustar la orientación de una imagen, Aspose.PSD simplifica el proceso.

## Requisitos previos

Antes de sumergirse en el tutorial, asegúrese de cumplir con los siguientes requisitos previos:

-  Biblioteca Aspose.PSD para Java: asegúrese de haber descargado e instalado la biblioteca Aspose.PSD para Java. Puede encontrar la biblioteca y la documentación detallada.[aquí](https://reference.aspose.com/psd/java/).

- Entorno de desarrollo Java: asegúrese de tener un entorno de desarrollo Java configurado en su máquina.

-  Archivo PSD de muestra: prepare un archivo PSD de muestra que desee rotar. Ajustar el`sourceFile` variable en el código de ejemplo con la ruta a su archivo PSD.

## Importar paquetes

Comience importando los paquetes necesarios para aprovechar las capacidades de Aspose.PSD:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Paso 1: cargue la imagen

 Cargue la imagen existente en una instancia del`Image` clase:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## Paso 2: rotar la imagen

 Gire la imagen usando el`rotateFlip` método. En este ejemplo, rotamos la imagen 270 grados:

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

## Paso 3: guarde la imagen girada

 Guarde la imagen rotada usando el`save` método y especificando el formato de salida (JPEG, en este caso):

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

## Conclusión

¡Felicidades! Has rotado con éxito una imagen usando Aspose.PSD para Java. Esta biblioteca simple pero poderosa abre un mundo de posibilidades para la manipulación de imágenes en sus aplicaciones Java.

## Preguntas frecuentes

### P1: ¿Aspose.PSD es compatible con diferentes formatos de imagen?

R1: Sí, Aspose.PSD admite varios formatos de imagen, incluidos PSD, JPEG, PNG y más.

### P2: ¿Puedo aplicar rotaciones personalizadas, no solo giros predefinidos?

R2: ¡Absolutamente! Aspose.PSD proporciona flexibilidad para aplicar rotaciones personalizadas para cumplir con sus requisitos específicos.

### P3: ¿Dónde puedo encontrar soporte o asistencia adicional?

 R3: Para cualquier consulta o problema, visite el[Foro Aspose.PSD](https://forum.aspose.com/c/psd/34) para el apoyo de la comunidad.

### P4: ¿Hay una prueba gratuita disponible?

 R4: Sí, puedes explorar Aspose.PSD con un[prueba gratis](https://releases.aspose.com/).

### P5: ¿Cómo obtengo una licencia temporal?

 R5: Si necesita una licencia temporal, puede obtener una[aquí](https://purchase.aspose.com/temporary-license/).