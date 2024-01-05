---
title: Cambiar el tamaño de la imagen proporcionalmente con Aspose.PSD para Java
linktitle: Cambiar el tamaño de la imagen proporcionalmente
second_title: API de Java Aspose.PSD
description: Mejore sus aplicaciones Java con Aspose.PSD. Siga nuestra guía para cambiar el tamaño de las imágenes proporcionalmente y sin esfuerzo. Aumente sus capacidades de manejo de imágenes hoy.
type: docs
weight: 17
url: /es/java/advanced-image-manipulation/resize-image-proportionally/
---
## Introducción

Bienvenido a nuestra guía paso a paso sobre cómo cambiar el tamaño de las imágenes proporcionalmente usando Aspose.PSD para Java. Si está buscando mejorar sus aplicaciones Java con capacidades eficientes de cambio de tamaño de imágenes, ha venido al lugar correcto. En este tutorial, lo guiaremos a través del proceso mediante pasos claros y concisos.

## Requisitos previos

Antes de sumergirse en el tutorial, asegúrese de cumplir con los siguientes requisitos previos:

1. Entorno Java: asegúrese de tener Java instalado en su sistema.
2.  Biblioteca Aspose.PSD: descargue e instale la biblioteca Aspose.PSD. Puedes encontrar los recursos necesarios.[aquí](https://releases.aspose.com/psd/java/).

## Importar paquetes

Una vez que haya ordenado los requisitos previos, importe los paquetes necesarios a su proyecto Java. Asegúrese de que se haga referencia correctamente a la biblioteca Aspose.PSD en su proyecto.

```java
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PngOptions;
```

## Paso 1: cargue la imagen

Comience cargando la imagen cuyo tamaño desea cambiar en su aplicación Java.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    image.cacheData();
}
```

## Paso 2: especifique el ancho y el alto

Determine el nuevo ancho y alto de su imagen redimensionada. En este ejemplo, cambiaremos el tamaño de la imagen a la mitad de sus dimensiones originales.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

## Paso 3: guarde la imagen redimensionada

Guarde la imagen redimensionada en la ubicación deseada, especificando las opciones de formato (PNG, en este caso).

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

¡Y ahí lo tienes! Ha cambiado correctamente el tamaño de una imagen proporcionalmente utilizando Aspose.PSD para Java.

## Conclusión

En este tutorial, cubrimos los pasos esenciales para cambiar el tamaño de las imágenes proporcionalmente usando la biblioteca Aspose.PSD para Java. Ahora puede integrar fácilmente esta funcionalidad en sus aplicaciones Java para mejorar el manejo de imágenes.

## Preguntas frecuentes

### P1: ¿Aspose.PSD es compatible con todos los formatos de imagen?

 R1: Aspose.PSD admite varios formatos de imagen, incluidos PSD, PNG, JPEG y más. Comprobar el[documentación](https://reference.aspose.com/psd/java/) para obtener una lista completa.

### P2: ¿Puedo utilizar Aspose.PSD para proyectos comerciales?

 R2: Sí, puedes. Visita el[pagina de compra](https://purchase.aspose.com/buy) para obtener detalles sobre la licencia.

### P3: ¿Hay licencias temporales disponibles para fines de prueba?

 R3: Sí, puedes obtener una licencia temporal[aquí](https://purchase.aspose.com/temporary-license/) Para evaluar.

### P4: ¿Dónde puedo encontrar soporte para Aspose.PSD?

 A4: Visita el[Foro Aspose.PSD](https://forum.aspose.com/c/psd/34) para el apoyo y asistencia de la comunidad.

### P5: ¿Cómo puedo acceder a la documentación de Aspose.PSD?

 A5: consulte la documentación detallada[aquí](https://reference.aspose.com/psd/java/).
`