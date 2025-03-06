---
title: Admite efecto de sombra en Aspose.PSD para Java
linktitle: Soporte de efecto de sombra
second_title: API de Java Aspose.PSD
description: Aprenda a agregar efectos de sombra cautivadores a las imágenes usando Aspose.PSD para Java. Mejore su diseño gráfico con este tutorial paso a paso.
weight: 13
url: /es/java/basic-image-operations/support-shadow-effect/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Admite efecto de sombra en Aspose.PSD para Java

## Introducción

Mejorar imágenes con efectos de sombras es una práctica común en diseño gráfico, agregando profundidad y realismo. Aspose.PSD para Java proporciona un sólido soporte para efectos de sombra, lo que permite a los desarrolladores integrar estos efectos sin esfuerzo en sus aplicaciones Java. En este tutorial, exploraremos cómo admitir efectos de sombra usando Aspose.PSD, paso a paso.

## Requisitos previos

Antes de sumergirse en el tutorial, asegúrese de cumplir con los siguientes requisitos previos:

- Conocimientos básicos de programación Java.
-  Aspose.PSD para Java instalado. Puedes descargarlo[aquí](https://releases.aspose.com/psd/java/).

## Importar paquetes

Asegúrese de haber importado los paquetes necesarios para aprovechar las funcionalidades de Aspose.PSD en su aplicación Java. Utilice el siguiente fragmento de código como guía:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Paso 1: cargue la imagen PSD

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "Shadow.psd";
String psdPathAfterChange = dataDir + "ShadowChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Paso 2: recuperar el efecto de sombra

```java
DropShadowEffect shadowEffect = (DropShadowEffect)(im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

## Paso 3: verificar la configuración predeterminada

```java
Assert.areEqual(Color.getBlack(), shadowEffect.getColor());
Assert.areEqual(255, shadowEffect.getOpacity());
Assert.areEqual(3, shadowEffect.getDistance());
Assert.areEqual(7, shadowEffect.getSize());
Assert.areEqual(true, shadowEffect.getUseGlobalLight());
Assert.areEqual(90, shadowEffect.getAngle());
Assert.areEqual(0, shadowEffect.getSpread());
Assert.areEqual(0, shadowEffect.getNoise());
```

## Paso 4: personaliza el efecto de sombra

```java
shadowEffect.setColor(Color.getGreen());
shadowEffect.setOpacity((byte)128);
shadowEffect.setDistance(11);
shadowEffect.setUseGlobalLight(false);
shadowEffect.setSize(9);
shadowEffect.setAngle(45);
shadowEffect.setSpread(3);
shadowEffect.setNoise(50);
```

## Paso 5: guarde la imagen modificada

```java
im.save(psdPathAfterChange);
```

## Conclusión

Con estos sencillos pasos, puede admitir fácilmente efectos de sombra en Aspose.PSD para Java, mejorando el atractivo visual de sus imágenes.

## Preguntas frecuentes

### P1: ¿Aspose.PSD para Java es adecuado para proyectos de diseño gráfico profesionales?

R1: ¡Absolutamente! Aspose.PSD para Java es una poderosa biblioteca diseñada para tareas profesionales de diseño gráfico.

### P2: ¿Puedo utilizar Aspose.PSD para Java en aplicaciones comerciales?

 R2: Sí, Aspose.PSD para Java es un producto comercial. puedes comprarlo[aquí](https://purchase.aspose.com/buy).

### P3: ¿Hay una prueba gratuita disponible?

 R3: Sí, puedes explorar una versión de prueba gratuita[aquí](https://releases.aspose.com/).

### P4: ¿Dónde puedo encontrar documentación detallada?

 A4: consulte la documentación completa[aquí](https://reference.aspose.com/psd/java/).

### P5: ¿Cómo puedo obtener soporte para Aspose.PSD para Java?

 A5: Únase al foro de la comunidad[aquí](https://forum.aspose.com/c/psd/34) para cualquier consulta de soporte.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
