---
date: 2026-03-23
description: Aprende a crear archivos PSD con relleno de degradado usando Java y Aspose.PSD.
  Esta guía muestra cómo editar capas de degradado en PSD, ajustar colores, transparencia
  y otras propiedades de forma programática.
linktitle: Create Gradient Fill PSD with Java – Add Gradient Fill Layer
second_title: Aspose.PSD Java API
title: Crear PSD con relleno de degradado en Java – Añadir capa de relleno de degradado
url: /es/java/psd-image-modification-conversion/add-gradient-fill-layer-psd-files/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Agregar capa de relleno de degradado en archivos PSD con Java

## Introducción

¿Alguna vez has deseado ese toque extra de magia visual para tus archivos PSD y te preguntas **cómo crear un relleno de degradado PSD** con Java? Los degradados le dan profundidad a tus diseños, pero ajustarlos manualmente puede ser tedioso. Con **Aspose.PSD for Java**, puedes editar programáticamente los degradados PSD, cambiar colores, ajustar la transparencia y afinar cada propiedad, ahorrándote tiempo y garantizando consistencia en docenas de archivos.

## Respuestas rápidas
- **¿Qué biblioteca le permite editar degradados PSD en Java?** Aspose.PSD for Java.  
- **¿Qué método carga un archivo PSD?** `Image.load(path)`.  
- **¿Cómo cambia el ángulo del degradado?** `settings.setAngle(double)`.  
- **¿Puede agregar nuevos puntos de color?** Sí—cree objetos `GradientColorPoint` y añádalos a la lista de puntos de color.  
- **¿Necesita una licencia para uso en producción?** Se requiere una licencia comercial; hay una prueba gratuita disponible para evaluación.

## ¿Qué es “crear un relleno de degradado PSD”?
Crear un relleno de degradado PSD significa insertar o modificar programáticamente una capa de relleno basada en degradado dentro de un documento de Photoshop. Esto permite estilizado automatizado, procesamiento por lotes y generación dinámica de imágenes sin abrir Photoshop.

## ¿Por qué usar Aspose.PSD para editar degradados PSD?
- **Compatibilidad total con .PSD** – funciona con todos los tipos de capas, incluidos los objetos inteligentes.  
- **No se requiere Photoshop** – se ejecuta en cualquier servidor o canal de CI.  
- **Control granular** – ajuste ángulo, desplazamientos, tramado, puntos de color y puntos de transparencia mediante una API Java limpia.  

## Requisitos previos

Antes de sumergirse, asegúrese de tener lo siguiente:

- Java Development Kit (JDK):  Una versión estable del JDK es necesaria para ejecutar código Java. Puede descargarla desde el sitio web de Oracle: [Link to Oracle JDK download page]
- Aspose.PSD for Java: Esta poderosa biblioteca le permite trabajar con archivos PSD en sus aplicaciones Java. Descárguela desde el sitio web de Aspose: [Link to Aspose.PSD for Java download] (Prueba gratuita disponible)

## Importar paquetes

Comencemos importando los paquetes esenciales de Aspose.PSD necesarios para trabajar con archivos PSD:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.IGradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.GradientTransparencyPoint;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint;
import com.aspose.psd.imageoptions.PsdOptions;
import java.util.ArrayList;
import java.util.Collections;
import java.util.List;
```

Estas importaciones proporcionan acceso a clases y métodos para cargar, manipular y guardar archivos PSD.

¡Ahora, prepárese para el emocionante viaje de modificar capas de relleno de degradado!

## Cómo crear un relleno de degradado PSD con Java

### Paso 1: Cargar el archivo PSD

Primero, necesitamos cargar el archivo PSD que contiene la capa de relleno de degradado que desea modificar. Use el método `Image.load`, especificando la ruta del archivo:

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ComplexGradientFillLayer.psd";
String outputFile = dataDir + "ComplexGradientFillLayer_output.psd";
PsdImage image = (PsdImage)Image.load(sourceFileName);
```

Este fragmento de código carga el archivo PSD del directorio especificado y lo almacena en la variable `image`.

### Paso 2: Identificar la capa de relleno de degradado

Los archivos PSD pueden contener numerosas capas. Necesitamos aislar la capa específica que contiene el relleno de degradado que queremos editar. Itere a través del arreglo `image.getLayers()` para encontrar la capa deseada:

```java
for (int i = 0; i < image.getLayers().length; i++) {
if (image.getLayers()[i] instanceof FillLayer) {
   FillLayer fillLayer = (FillLayer) image.getLayers()[i];
   // Further checks and modifications will happen here
   break;
}
}
```

Este bucle verifica cada capa. Si una capa es un `FillLayer`, se convierte al tipo `FillLayer` y se almacena en la variable `fillLayer` para procesamiento posterior. Podemos agregar verificaciones adicionales dentro del bucle si tiene criterios específicos para identificar la capa objetivo (p. ej., nombre de la capa).

### Paso 3: Verificar el tipo de relleno de degradado

No todas las capas de relleno utilizan degradados. Este fragmento de código confirma si la capa identificada realmente contiene un relleno de degradado:

```java
if (fillLayer.getFillSettings().getFillType() != FillType.Gradient) {
   throw new Exception("Wrong Fill Layer");
}
```

Si el método `getFillType` no devuelve `FillType.Gradient`, se lanza una excepción, indicando que estamos trabajando con la capa incorrecta.

## Cómo editar el degradado PSD usando Aspose.PSD

### Paso 4: Acceder y modificar las propiedades del degradado

¡La magia ocurre aquí! Aspose.PSD brinda acceso a varias propiedades de relleno de degradado a través de la interfaz `IGradientFillSettings`. Podemos obtenerlas y modificarlas según sea necesario:

```java
IGradientFillSettings settings = (IGradientFillSettings) fillLayer.getFillSettings();

// Modify properties (replace with desired values)
settings.setAngle(0.0);  // Set angle to 0 degrees
settings.setDither(false);  // Disable dithering
settings.setAlignWithLayer(true); // Align gradient with layer
settings.setReverse(true);  // Reverse gradient direction
settings.setHorizontalOffset(25);  // Set horizontal offset
settings.setVerticalOffset(-15);  // Set vertical offset
```

Este código recupera el objeto `IGradientFillSettings` y luego modifica propiedades como ángulo, tramado, alineación y desplazamientos. Reemplace los valores proporcionados con la configuración deseada para lograr el efecto de degradado que imagina.

### Paso 5: Manipular puntos de color y de transparencia

Los degradados se definen mediante puntos de color y de transparencia a lo largo de un espectro. Aspose.PSD le permite modificar estos puntos para un control preciso:

```java
List<IGradientColorPoint> colorPoints = new ArrayList<IGradientColorPoint>();
Collections.addAll(colorPoints, settings.getColorPoints());
List<IGradientTransparencyPoint> transparencyPoints = new ArrayList<IGradientTransparencyPoint>();
Collections.addAll(transparencyPoints, settings.getTransparencyPoints());

// Add a new color point
GradientColorPoint gr1 = new GradientColorPoint();
gr1.setColor(Color.getViolet());
gr1.setLocation(4096);
gr1.setMedianPointLocation(75);
colorPoints.add(gr1);

// Modify an existing color point
colorPoints.get(1).setLocation(3000);

// Add a new transparency point
GradientTransparencyPoint gr2 = new GradientTransparencyPoint();
gr2.setOpacity(80.0);
gr2.setLocation(4096);
gr2.setMedianPointLocation(25);
transparencyPoints.add(gr2);

// Modify an existing transparency point
transparencyPoints.get(2).setLocation(3000);

settings.setColorPoints(colorPoints.toArray(new IGradientColorPoint[0]));
settings.setTransparencyPoints(transparencyPoints.toArray(new IGradientTransparencyPoint[0]));
```

### Paso 6: Actualizar y guardar el archivo PSD

Una vez que haya realizado las modificaciones necesarias, actualice la capa de relleno y guarde el archivo PSD:

```java
fillLayer.update();
image.save(outputFile, new PsdOptions(image));
```

El método `fillLayer.update()` aplica los cambios a la capa de relleno de degradado, y `image.save` guarda el archivo PSD modificado en la ruta de salida especificada.

## Problemas comunes y soluciones

- **Excepción “Wrong Fill Layer”** – Asegúrese de que está apuntando a un `FillLayer` que realmente utiliza un degradado. Verifique el nombre o índice de la capa antes de convertir.  
- **Los puntos de color no reflejan los cambios** – Después de modificar la lista de puntos, siempre llame a `settings.setColorPoints(...)` y `settings.setTransparencyPoints(...)` para enviar las actualizaciones a la capa.  
- **Rendimiento en PSD grandes** – Si procesa muchos archivos, reutilice la misma instancia de `PsdOptions` y cierre las imágenes rápidamente con `image.dispose()` para liberar memoria.

## Preguntas frecuentes

**P: ¿Puedo agregar múltiples puntos de color y de transparencia a un degradado?**  
R: ¡Absolutamente! Puede agregar tantos puntos de color y de transparencia como necesite para lograr el efecto de degradado deseado. Simplemente cree nuevos puntos y añádalos a las listas correspondientes.

**P: ¿Cómo elimino un punto de color o de transparencia de un degradado?**  
R: Use el método `remove` de la lista, por ejemplo, `colorPoints.remove(index)`, para borrar el punto no deseado antes de llamar a `setColorPoints`.

**P: ¿Puedo cambiar el tipo de degradado (lineal, radial, etc.)?**  
R: Aspose.PSD actualmente soporta degradados lineales. Futuras versiones pueden agregar más tipos, pero puede simular otros efectos manipulando los puntos de color y de transparencia.

**P: ¿Hay un impacto en el rendimiento al modificar degradados?**  
R: El impacto depende de la complejidad del degradado y del número de modificaciones. Para casos de uso típicos la sobrecarga es mínima, pero el procesamiento por lotes de archivos grandes puede beneficiarse de ajustes en la gestión de memoria.

**P: ¿Puedo aplicar esta técnica a múltiples capas de relleno de degradado en un archivo PSD?**  
R: Sí. Itere a través de `image.getLayers()`, verifique cada `FillLayer` para `FillType.Gradient` y aplique las mismas modificaciones según sea necesario.

**P: ¿Necesito una licencia comercial para uso en producción?**  
R: Se requiere una licencia válida de Aspose.PSD para implementaciones en producción. Hay una prueba gratuita disponible para propósitos de evaluación.

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**Última actualización:** 2026-03-23  
**Probado con:** Aspose.PSD for Java 24.11 (latest)  
**Autor:** Aspose