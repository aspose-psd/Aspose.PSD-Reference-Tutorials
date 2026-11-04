---
date: 2026-11-04
description: Aprenda cómo usar Aspose.PSD para Java para aplicar una invert adjustment
  layer, procesar por lotes imágenes PSD y crear archivos PSD de imagen negativa.
keywords:
- how to use aspose
- batch process psd images
- create negative image psd
- image processing java library
- apply multiple adjustment layers
lastmod: 2026-11-04
linktitle: Invert Adjustment Layer
og_description: Cómo usar Aspose.PSD para Java para agregar una invert adjustment
  layer, procesar por lotes imágenes PSD y crear un PSD de imagen negativa. Siga la
  guía paso a paso.
og_image_alt: Screenshot showing Aspose.PSD Java code adding an invert adjustment
  layer
og_title: Cómo usar Aspose.PSD para agregar una invert adjustment layer en Java
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to use Aspose.PSD for Java to apply an invert adjustment
    layer, batch process PSD images, and create negative image PSD files.
  headline: How to use Aspose.PSD to add an invert adjustment layer in Java
  type: TechArticle
- questions:
  - answer: Yes, it supports Java 6.0 and later, including Java 8, 11, and 17.
    question: Is Aspose.PSD compatible with all Java versions?
  - answer: Absolutely. After adding the invert layer you can call `addBrightnessAdjustmentLayer()`,
      `addHueSaturationAdjustmentLayer()`, etc., to stack effects.
    question: Can I apply multiple adjustment layers in a single operation?
  - answer: The complete documentation is available [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).
    question: Where can I find the full API reference?
  - answer: Yes, you can download a trial version [Aspose.PSD trial download](https://releases.aspose.com/).
    question: Is there a free trial for Aspose.PSD?
  - answer: Request a temporary license [temporary license request page](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license for testing?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- aspose psd
- java image processing
- invert adjustment layer
- batch psd processing
title: Cómo usar Aspose.PSD para agregar una invert adjustment layer en Java
url: /es/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo usar Aspose.PSD para agregar una capa de ajuste de inversión en Java

## Introducción

Si buscas una **biblioteca de procesamiento de imágenes java** robusta, Aspose.PSD para Java es una de las opciones más versátiles del mercado. En este tutorial verás **cómo usar Aspose** para insertar una **Capa de Ajuste de Inversión** en un archivo PSD, combinarla con otros ajustes e incluso ejecutar la operación en docenas de archivos. Ya sea que estés construyendo una herramienta de procesamiento por lotes, un servicio de imágenes del lado del servidor o un editor de imágenes individual, los pasos a continuación te llevarán desde el PSD de origen hasta una imagen negativa totalmente editable en minutos.

## Respuestas rápidas
- **¿Qué hace la Capa de Ajuste de Inversión?** Invierte cada valor RGB en el área seleccionada, convirtiendo la imagen en un negativo fotográfico.  
- **¿Qué biblioteca proporciona esta función?** Aspose.PSD, una **biblioteca de procesamiento de imágenes java** líder.  
- **¿Puedo combinarla con otros ajustes?** Sí, puedes **aplicar múltiples capas de ajuste** como Brillo/Contraste, Tono/Saturación y más.  
- **¿Necesito una licencia para desarrollo?** Hay una prueba gratuita disponible; se requiere una licencia para uso en producción.  
- **¿Cuánto tiempo lleva la implementación?** Normalmente menos de 10 minutos para un caso de uso básico.

## ¿Qué es la Capa de Ajuste de Inversión?

La Capa de Ajuste de Inversión es una edición no destructiva que revierte los valores de color de cada píxel que afecta. Como se sitúa encima de la pila de capas, puedes alternar su visibilidad o reordenarla sin alterar permanentemente los datos originales de la imagen. Esta es la forma más rápida de **crear archivos PSD de imagen negativa** o lograr un aspecto clásico de negativo de película.

## ¿Por qué usar Aspose.PSD como tu biblioteca de procesamiento de imágenes java?

Aspose.PSD soporta **más de 200 características PSD**, puede leer y escribir archivos de Photoshop sin requerir Photoshop, y procesa documentos de cientos de páginas usando menos de 500 MB de memoria heap. Se ejecuta en cualquier entorno Java (Java 6+), lo que lo hace ideal para **procesamiento por lotes de imágenes psd** en servidores Windows, Linux o macOS.

## Requisitos previos

Antes de comenzar, asegúrate de tener:

1. **Aspose.PSD para Java** – descarga el último JAR desde el sitio oficial [Aspose.PSD for Java download page](https://releases.aspose.com/psd/java/).  
2. **Java Development Kit** – JDK 6.0 o posterior instalado y configurado en tu `PATH`.  

Ahora estás listo para escribir el código.

## Importar paquetes

La clase `PsdImage` representa un documento completo de Photoshop en memoria, mientras que las clases de capa de ajuste viven en el paquete `com.aspose.psd.layers.adjustments`.

La clase `PsdImage` es el objeto de nivel superior de Aspose.PSD que encapsula la estructura y los datos de píxeles de un archivo PSD. Importa los espacios de nombres y luego podrás cargar, editar y guardar archivos PSD.

## Paso 1: configurar el directorio del documento

Define la carpeta que contiene tu archivo PSD de origen y donde se guardará la salida. Usar rutas absolutas evita `NullPointerException` cuando cambia el directorio de trabajo.

## Paso 2: cargar el archivo PSD

Carga el archivo de origen en un objeto `PsdImage`. Este objeto mantiene toda la jerarquía de capas en memoria, permitiendo ediciones no destructivas.

El método estático `load` de la clase `PsdImage` lee el encabezado del archivo, valida el formato y construye una representación en memoria lista para manipular.

## Paso 3: agregar capa de ajuste de inversión

Llama al método incorporado para insertar una Capa de Ajuste de Inversión en la parte superior de la pila de capas actual. Luego puedes añadir más capas (p. ej., Brillo, Tono) para **aplicar múltiples capas de ajuste** en un solo flujo de trabajo.

`addInvertAdjustmentLayer()` agrega una Capa de Ajuste de Inversión a la colección de capas del PSD.

## Paso 4: guardar la salida

Persistir el PSD modificado en disco.  

`save()` escribe el archivo PSD, incluidas todas las capas y metadatos, en la ruta especificada.

El guardado utiliza el mismo método `save` que escribe el documento completo, incluidas todas las capas de ajuste, máscaras y metadatos, en el formato especificado.

### ¿Qué acaba de suceder?

El archivo PSD se cargó en un objeto `PsdImage`, se creó y añadió una `InvertAdjustmentLayer` como la capa superior, y el documento se guardó. Esta secuencia preserva los datos originales de la imagen mientras agrega un efecto de inversión no destructivo que puede activarse o reordenarse más tarde.

Has usado con éxito Aspose.PSD, una **biblioteca de procesamiento de imágenes java**, para manipular un archivo PSD.

## ¿Cómo procesar por lotes imágenes PSD con ajuste de inversión?

Carga cada archivo dentro de un bucle `for`, aplica los mismos pasos y llama a `save` en cada iteración. Como Aspose.PSD procesa los archivos de forma streaming, puedes manejar **cientos de PSD** manteniendo el uso de memoria bajo 300 MB reutilizando la misma instancia de `PsdImage`.

## ¿Cómo convertir un PSD a una imagen negativa?

Añade la Capa de Ajuste de Inversión como el elemento superior y guarda el documento; esa operación equivale a **convertir PSD a negativo**. Luego puedes desactivar o eliminar la capa para volver a la apariencia original sin volver a cargar el archivo de origen.

## Problemas comunes y consejos

| Problema | Causa | Solución |
|----------|-------|----------|
| **NullPointerException en `Image.load`** | Ruta de archivo incorrecta o archivo faltante | Verifica `dataDir` y el nombre del archivo; usa rutas absolutas para pruebas |
| **Orden de capas no es el esperado** | Añadir capas después de las existentes cambia la superposición | Inserta la capa de inversión antes de otros ajustes, o reordena mediante `psdImage.getLayers().move()` |
| **Ralentización del rendimiento en PSD grandes** | Cargar archivos muy grandes en memoria | Incrementa el heap de JVM (`-Xmx2g`) o procesa archivos en fragmentos usando `psdImage.getPages().get(0).getResources().setMemoryOptimized(true)` |

## Preguntas frecuentes

**P: ¿Aspose.PSD es compatible con todas las versiones de Java?**  
R: Sí, soporta Java 6.0 y posteriores, incluyendo Java 8, 11 y 17.

**P: ¿Puedo aplicar múltiples capas de ajuste en una sola operación?**  
R: Absolutamente. Después de añadir la capa de inversión puedes llamar a `addBrightnessAdjustmentLayer()`, `addHueSaturationAdjustmentLayer()`, etc., para apilar efectos.

**P: ¿Dónde puedo encontrar la referencia completa de la API?**  
R: La documentación completa está disponible [Aspose.PSD Java API reference](https://reference.aspose.com/psd/java/).

**P: ¿Hay una prueba gratuita para Aspose.PSD?**  
R: Sí, puedes descargar una versión de prueba [Aspose.PSD trial download](https://releases.aspose.com/).

**P: ¿Cómo obtengo una licencia temporal para pruebas?**  
R: Solicita una licencia temporal [temporary license request page](https://purchase.aspose.com/temporary-license/).

---

**Última actualización:** 2026-11-04  
**Probado con:** Aspose.PSD 24.12 para Java  
**Autor:** Aspose  









```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

```java
String dataDir = "Your Document Directory";
```

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

```java
im.addInvertAdjustmentLayer();
```

```java
im.save(outputPath);
```

## Tutoriales relacionados

- [Add Level Adjustment Layer to PSD Files with Aspose.PSD for Java](/psd/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/)
- [How to Add Adjustment Layer – Channel Mixer in PSD (Java)](/psd/java/modifying-converting-psd-images/add-channel-mixer-adjustment-layer-psd/)
- [How to Edit PSD - Add Curves Adjustment Layer Using Java](/psd/java/modifying-converting-psd-images/add-curves-adjustment-layer-psd/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}