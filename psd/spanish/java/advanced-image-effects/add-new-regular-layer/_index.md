---
date: 2026-04-08
description: Aprende cómo exportar PSD a PNG y crear una nueva capa PSD con Aspose.PSD
  para Java usando una licencia temporal de Aspose. Este tutorial paso a paso cubre
  la manipulación de imágenes PSD y cómo establecer la posición de la capa.
keywords:
- aspose temporary license
- set layer position
- psd image manipulation
- create new psd layer
linktitle: Agregar una nueva capa regular al PSD
second_title: Aspose.PSD Java API
title: Exportar PSD a PNG y agregar una nueva capa regular usando Aspose.PSD para
  Java – licencia temporal de Aspose
url: /es/java/advanced-image-effects/add-new-regular-layer/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportar PSD a PNG y Añadir una Nueva Capa Regular usando Aspose.PSD para Java

## Introducción

En este **aspose psd tutorial** descubrirás cómo **exportar PSD a PNG** mientras también **creas una nueva capa regular** dentro del mismo archivo, **usando una licencia temporal de aspose** para desarrollo. Ya sea que necesites generar miniaturas listas para la web, preparar recursos para una cadena de diseño, o simplemente experimentar con **psd image manipulation**, Aspose.PSD para Java te brinda control total programático. Recorreremos cada paso—desde cargar el archivo fuente hasta guardar tanto el PSD actualizado como una copia PNG—para que puedas comenzar a manipular capas PSD de inmediato.

## Respuestas rápidas
- **¿Puedo exportar PSD a PNG con una sola llamada?** Sí, después de añadir capas puedes llamar a `save` con `PngOptions`.
- **¿Necesito una licencia para desarrollo?** Una licencia temporal funciona para pruebas; se requiere una licencia completa para producción.
- **¿Qué versión de Java es compatible?** Aspose.PSD funciona con Java 8 y versiones posteriores.
- **¿El posicionamiento de capas se basa en píxeles?** Sí, estableces las coordenadas left, top, right y bottom en píxeles usando los métodos **set layer position**.
- **¿El PNG conservará la transparencia de las capas?** El PNG contendrá el resultado combinado de todas las capas visibles.

## ¿Por qué usar una licencia temporal de aspose?

Una **aspose temporary license** te permite evaluar el conjunto completo de funciones de Aspose.PSD sin restricciones funcionales. Elimina la marca de agua de evaluación, desbloquea todas las API—incluyendo la capacidad de **create new psd layer** objects—y te permite probar tu código en un entorno similar a producción antes de comprar una licencia permanente.

## Requisitos previos

- **Java Development Environment** – JDK 8+ y una herramienta de compilación (Maven/Gradle) instalada.
- **Aspose.PSD for Java** – Descarga el último JAR desde el sitio oficial [aquí](https://releases.aspose.com/psd/java/).
- **A sample PSD file** – Usaremos `OneLayer.psd` en los ejemplos.

## Importar paquetes

Agrega los imports necesarios a tu clase Java. Estas clases proporcionan la funcionalidad central para **psd image manipulation** y la gestión de capas.

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## ¿Qué es “set layer position” y por qué es importante?

Cuando añades una nueva capa, necesitas definir dónde aparece en el lienzo. Los métodos `setLeft`, `setTop`, `setRight` y `setBottom` **set layer position** en coordenadas de píxeles. Un posicionamiento correcto garantiza que tus gráficos se alineen exactamente donde los esperas, lo cual es crucial para tareas como componer recursos de UI o preparar archivos listos para impresión.

## Guía paso a paso

### Paso 1: Cargar el archivo PSD

Primero, carga el PSD existente que deseas modificar. Esto te proporciona un objeto `PsdImage` con el que puedes trabajar.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

### Paso 2: Preparar datos de píxeles y rectángulos

Crearemos dos buffers de píxeles (`int[]`) y definiremos las áreas rectangulares donde se pintarán las nuevas capas. Esta es la base para **creating a new psd layer**.

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

### Paso 3: Inicializar datos de capa

Rellena los buffers de píxeles con un valor ARGB predeterminado. El valor `-10000000` corresponde a un tono oscuro semitransparente.

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

### Paso 4: Añadir capas regulares (Manipular capas PSD)

Ahora **add regular layers** a la imagen PSD y **set layer position** usando las propiedades left, top, right y bottom. Esto demuestra cómo **manipulate PSD layers** programáticamente.

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

### Paso 5: Exportar PSD a PNG y guardar el PSD actualizado

Una vez que las capas están en su lugar, guarda el documento modificado. Primero exportamos el resultado a PNG (el paso **export psd to png**), luego guardamos el PSD con las nuevas capas.

```java
String exportPath = dataDir + "Updated.psd";
String exportPathPng = dataDir + "Updated.png";

im.save(exportPath, new PsdOptions());          // Save the updated PSD
im.save(exportPathPng, new PngOptions());       // Export PSD to PNG
```

> **Consejo profesional:** Si solo necesitas el PNG, puedes omitir la llamada `save` del PSD y directamente invocar `save` con `PngOptions`.

## Problemas comunes y solución de problemas

| Síntoma | Causa probable | Solución |
|---------|----------------|----------|
| PNG aparece en blanco | Las capas son invisibles o totalmente transparentes | Asegúrate de establecer valores de píxel no transparentes o llama a `layer.setVisible(true)`. |
| `ArrayIndexOutOfBoundsException` | Incompatibilidad entre el tamaño del rectángulo y la longitud del arreglo de píxeles | Verifica que `rect.width * rect.height == dataArray.length`. |
| LicenseException en tiempo de ejecución | No se cargó una licencia válida | Carga una licencia temporal o permanente antes de llamar a cualquier método de la API. |

## Preguntas frecuentes

**Q: ¿Es Aspose.PSD compatible con Java 8?**  
A: Sí, Aspose.PSD soporta Java 8 y versiones posteriores.

**Q: ¿Puedo aplicar transformaciones (rotar, escalar) a las capas añadidas?**  
A: ¡Absolutamente! La clase `Layer` proporciona métodos como `rotate`, `scale` y `translate` para un control total de la transformación.

**Q: ¿Dónde puedo encontrar documentación adicional de Aspose.PSD?**  
A: La documentación detallada de la API está disponible [aquí](https://reference.aspose.com/psd/java/).

**Q: ¿Cómo obtengo una licencia temporal para Aspose.PSD?**  
A: Visita la página de licencia temporal [aquí](https://purchase.aspose.com/temporary-license/).

**Q: ¿Existen foros comunitarios para soporte de Aspose.PSD?**  
A: Sí, únete a las discusiones en los foros de Aspose [aquí](https://forum.aspose.com/c/psd/34).

## Conclusión

Ahora has aprendido cómo **exportar PSD a PNG** mientras **añades nuevas capas regulares** usando Aspose.PSD para Java, y has visto cómo una **aspose temporary license** te permite probar este flujo de trabajo sin restricciones. Este tutorial muestra las capacidades centrales de **psd image manipulation**: cargar un archivo, crear capas, rellenar datos de píxeles y exportar la composición final. Siéntete libre de experimentar con diferentes tamaños de rectángulo, colores de píxeles o efectos de capa para adaptar la salida a las necesidades de tu proyecto.

---

**Última actualización:** 2026-04-08  
**Probado con:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}