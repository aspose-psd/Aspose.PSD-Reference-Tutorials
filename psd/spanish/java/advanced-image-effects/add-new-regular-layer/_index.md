---
title: Agregue una nueva capa normal a PSD con Aspose.PSD para Java
linktitle: Agregar una nueva capa normal a PSD
second_title: API de Java Aspose.PSD
description: Aprenda cómo agregar una nueva capa normal a archivos PSD usando Aspose.PSD para Java. Siga nuestra guía paso a paso para una manipulación PSD perfecta.
type: docs
weight: 11
url: /es/java/advanced-image-effects/add-new-regular-layer/
---
## Introducción

Bienvenido a este completo tutorial sobre el uso de Aspose.PSD para Java para agregar una nueva capa normal a un archivo PSD. Aspose.PSD es una poderosa biblioteca Java que permite a los desarrolladores manipular y trabajar con archivos PSD de manera eficiente. En este tutorial, lo guiaremos a través del proceso de agregar una nueva capa normal a un archivo PSD, brindándole pasos detallados y ejemplos de código.

## Requisitos previos

Antes de sumergirse en el tutorial, asegúrese de cumplir con los siguientes requisitos previos:

- Entorno de desarrollo Java: asegúrese de tener un entorno de desarrollo Java configurado en su sistema.
-  Biblioteca Aspose.PSD: descargue e instale la biblioteca Aspose.PSD para Java. Puedes encontrar la biblioteca.[aquí](https://releases.aspose.com/psd/java/).

## Importar paquetes

Para comenzar, importe los paquetes necesarios a su proyecto Java. Estos paquetes son esenciales para trabajar con las funcionalidades de Aspose.PSD. Incluya las siguientes líneas al comienzo de su archivo Java:

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Paso 1: cargar el archivo PSD

Cargue el archivo PSD que desea editar usando el siguiente código:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## Paso 2: preparar matrices de datos y rectángulos

Prepare dos matrices int y dos objetos Rectángulo de la siguiente manera:

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

## Paso 3: inicializar los datos de la capa

Inicialice matrices de datos con un valor predeterminado:

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

## Paso 4: agregue capas regulares

Agregue dos capas regulares a la imagen PSD:

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

## Paso 5: guarde PSD y PNG

Guarde el PSD modificado y un archivo PNG adicional:

```java
im.save(exportPath, new PsdOptions());
im.save(exportPathPng, new PngOptions());
```

¡Felicidades! Ha agregado con éxito una nueva capa normal a un archivo PSD usando Aspose.PSD para Java.

## Conclusión

En este tutorial, cubrimos el proceso de agregar una nueva capa normal a un archivo PSD usando Aspose.PSD para Java. Esta poderosa biblioteca simplifica la manipulación de PSD, haciéndola accesible para los desarrolladores de Java. Experimente con diferentes parámetros y funcionalidades para explorar todo el potencial de Aspose.PSD.

## Preguntas frecuentes

### P1: ¿Aspose.PSD es compatible con Java 8?

R1: Sí, Aspose.PSD es compatible con Java 8 y versiones posteriores.

### P2: ¿Puedo aplicar transformaciones a las capas agregadas?

R2: ¡Absolutamente! Aspose.PSD proporciona una variedad de opciones de transformación para capas.

### P3: ¿Dónde puedo encontrar documentación adicional de Aspose.PSD?

 A3: Puede consultar la documentación.[aquí](https://reference.aspose.com/psd/java/).

### P4: ¿Cómo puedo obtener una licencia temporal para Aspose.PSD?

 A4: Visita[este enlace](https://purchase.aspose.com/temporary-license/) para opciones de licencia temporal.

### P5: ¿Existen foros comunitarios para soporte de Aspose.PSD?

 R5: Sí, puedes encontrar soporte y debates[aquí](https://forum.aspose.com/c/psd/34).