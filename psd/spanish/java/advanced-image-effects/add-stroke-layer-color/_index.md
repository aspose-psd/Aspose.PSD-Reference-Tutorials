---
title: Agregar color de capa de trazo en Aspose.PSD para Java
linktitle: Agregar color de capa de trazo
second_title: API de Java Aspose.PSD
description: Explore el poder de Aspose.PSD para Java con nuestra guía paso a paso sobre cómo agregar color de capa de trazo. Mejora tus diseños gráficos sin esfuerzo.
type: docs
weight: 14
url: /es/java/advanced-image-effects/add-stroke-layer-color/
---
## Introducción

Libere el potencial del diseño gráfico de su aplicación Java con Aspose.PSD. En este tutorial, profundizaremos en el fascinante mundo de agregar color a la capa de trazo usando Aspose.PSD para Java. Mejore sus gráficos con trazos que resaltan, creando diseños visualmente atractivos sin esfuerzo.

## Requisitos previos

Antes de embarcarse en este viaje creativo, asegúrese de cumplir con los siguientes requisitos previos:

-  Biblioteca Aspose.PSD: descargue y configure la biblioteca Aspose.PSD siguiendo las instrucciones[documentación](https://reference.aspose.com/psd/java/).

- Kit de desarrollo de Java (JDK): asegúrese de tener Java instalado en su sistema.

- Entorno de desarrollo integrado (IDE): elija un IDE de su preferencia; Eclipse o IntelliJ son opciones populares.

## Importar paquetes

Comencemos importando los paquetes necesarios para que suceda la magia de Aspose.PSD.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;


import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.BlendMode;
import com.aspose.psd.fileformats.psd.layers.fillsettings.ColorFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
```

## Paso 1: configura tu proyecto

Comience creando un nuevo proyecto Java en su IDE preferido. Asegúrese de que la biblioteca Aspose.PSD esté agregada a su proyecto.

## Paso 2: cargar el archivo PSD

Cargue el archivo PSD usando Aspose.PSD, permitiendo la carga de recursos de efectos.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Paso 3: acceder a la capa de trazo

Acceda a la capa de efecto de trazo dentro del archivo PSD.

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## Paso 4: validar las propiedades del trazo

Asegúrese de que las propiedades del trazo sean las esperadas.

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

## Paso 5: establecer el color y la opacidad

Modifica el color y la opacidad de la capa del trazo.

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

## Paso 6: guarde el PSD modificado

Guarde el archivo PSD modificado con el color de capa de trazo recién agregado.

```java
im.save(exportPath);
```

## Conclusión

¡Felicidades! Ha agregado con éxito el color de la capa de trazo a su archivo PSD usando Aspose.PSD para Java. Experimente con diferentes colores y configuraciones para darle vida a sus diseños gráficos.

## Preguntas frecuentes

### P1: ¿Puedo utilizar Aspose.PSD con otras bibliotecas gráficas de Java?

R1: Sí, Aspose.PSD se puede integrar con otras bibliotecas gráficas de Java para mejorar su funcionalidad.

### P2: ¿Aspose.PSD es compatible con el último formato de archivo PSD?

R2: ¡Absolutamente! Aspose.PSD se mantiene al día con las últimas especificaciones de formato de archivo PSD, lo que garantiza la compatibilidad.

### P3: ¿Cómo manejo las excepciones mientras uso Aspose.PSD?

 A3: Consulte el[foro de soporte](https://forum.aspose.com/c/psd/34) para obtener ayuda en el manejo de excepciones y solución de problemas.

### P4: ¿Puedo probar Aspose.PSD antes de comprarlo?

 R4: ¡Por supuesto! Coge un[prueba gratuita](https://releases.aspose.com/) para explorar las características de Aspose.PSD antes de comprometerse.

### P5: ¿Dónde puedo obtener una licencia temporal para Aspose.PSD?

 R5: Obtener un[licencia temporal](https://purchase.aspose.com/temporary-license/) para que Aspose.PSD evalúe sus capacidades en sus proyectos.