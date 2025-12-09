---
date: 2025-12-02
description: Aprenda a usar la biblioteca Java de procesamiento de imágenes Aspose.PSD
  para aplicar múltiples capas de ajuste, incluida la capa de ajuste Invertir, para
  una manipulación fluida de archivos PSD.
linktitle: Invert Adjustment Layer
second_title: Aspose.PSD Java API
title: 'Biblioteca Java de procesamiento de imágenes: invertir capa con Aspose.PSD'
url: /es/java/advanced-image-manipulation/invert-adjustment-layer/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Capa de Ajuste Invertir en Aspose.PSD para Java

## Introducción

Si buscas una robusta **image processing java library**, Aspose.PSD for Java es una de las opciones más versátiles del mercado. En este tutorial te mostraremos cómo agregar una **Invert Adjustment Layer** a un archivo PSD, una técnica que puedes combinar con otras capas de ajuste para lograr efectos visuales sofisticados. Ya sea que estés construyendo una herramienta de procesamiento por lotes o un editor de imágenes individual, esta guía te brinda una ruta clara, paso a paso, para completar la tarea rápidamente.

## Respuestas rápidas
- **¿Qué hace la Invert Adjustment Layer?** Invierte todos los valores de color en el área seleccionada, creando un efecto de imagen negativa.  
- **¿Qué biblioteca proporciona esta función?** Aspose.PSD, una biblioteca líder de image processing java library.  
- **¿Puedo combinarla con otros ajustes?** Sí – puedes **apply multiple adjustment layers** como Brillo/Contraste, Tono/Saturación, y más.  
- **¿Necesito una licencia para desarrollo?** Hay una prueba gratuita disponible; se requiere una licencia para uso en producción.  
- **¿Cuánto tiempo lleva la implementación?** Normalmente menos de 10 minutos para un caso de uso básico.

## ¿Qué es la Invert Adjustment Layer?

La Invert Adjustment Layer es una edición no destructiva que invierte los valores RGB de cada píxel que afecta. Debido a que se sitúa encima de la pila de capas, puedes alternar su visibilidad o reordenarla sin alterar permanentemente los datos originales de la imagen.

## ¿Por qué usar Aspose.PSD como tu biblioteca de Image Processing Java?

- **Soporte completo de PSD** – leer, editar y escribir archivos de Photoshop sin necesidad de Photoshop instalado.  
- **Multiplataforma** – funciona en cualquier entorno Java (Java 6+).  
- **Funciones de ajuste avanzadas** – incluye métodos incorporados para muchas ediciones comunes, facilitando **apply multiple adjustment layers** en un solo flujo de trabajo.  
- **Optimizado para rendimiento** – maneja archivos grandes de manera eficiente, lo cual es esencial para el procesamiento por lotes.

## Requisitos previos

Antes de comenzar, asegúrate de tener lo siguiente:

1. **Aspose.PSD Library** – descárgala desde el sitio oficial [here](https://releases.aspose.com/psd/java/).  
2. **Java Development Environment** – JDK 6.0 o posterior instalado y configurado.  

Ahora, sumerjámonos en el código.

## Importar paquetes

Comienza importando las clases necesarias. Estas importaciones te dan acceso a las API centrales de manejo de imágenes y a la funcionalidad específica de PSD.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
```

## Paso 1: Configurar el directorio del documento

Define la carpeta que contiene tu archivo PSD de origen y donde se guardará la salida.

```java
String dataDir = "Your Document Directory";
```

## Paso 2: Cargar el archivo PSD

Carga el archivo de origen en un objeto `PsdImage`. Este objeto representa todo el documento PSD en memoria.

```java
String filePath = dataDir + "InvertStripes_before.psd";
String outputPath = dataDir + "InvertStripes_after.psd";

PsdImage im = (PsdImage)Image.load(filePath);
```

## Paso 3: Añadir la capa de ajuste Invert

Llama al método incorporado para insertar una Invert Adjustment Layer en la parte superior de la pila de capas actual. Luego puedes agregar más capas (p.ej., Brillo, Tono) para **apply multiple adjustment layers**.

```java
im.addInvertAdjustmentLayer();
```

## Paso 4: Guardar la salida

Guarda el PSD modificado en disco. El archivo guardado ahora contiene la Invert Adjustment Layer y puede abrirse en Photoshop o cualquier visor compatible con PSD.

```java
im.save(outputPath);
```

### ¿Qué acaba de suceder?

- El PSD se cargó en memoria.  
- Se añadió una Invert Adjustment Layer como la capa superior.  
- La imagen se guardó, preservando la edición no destructiva.

Ahora has utilizado con éxito Aspose.PSD, una **image processing java library**, para manipular un archivo PSD.

## Problemas comunes y consejos

| Problema | Causa | Solución |
|----------|-------|----------|
| **NullPointerException en `Image.load`** | Ruta de archivo incorrecta o archivo faltante | Verifica `dataDir` y el nombre del archivo; usa rutas absolutas para pruebas |
| **Orden de capas no como se esperaba** | Agregar capas después de las existentes cambia el apilamiento | Usa `im.addInvertAdjustmentLayer()` antes de agregar otros ajustes, o reordena capas mediante `im.getLayers()` |
| **Ralentización del rendimiento en PSD grandes** | Cargar archivos muy grandes en memoria | Considera procesar páginas en fragmentos o aumentar el tamaño del heap de JVM (`-Xmx2g`) |

## Preguntas frecuentes

**Q: ¿Es Aspose.PSD compatible con todas las versiones de Java?**  
A: Aspose.PSD soporta Java 6.0 y versiones posteriores.

**Q: ¿Puedo aplicar múltiples capas de ajuste en una sola operación?**  
A: Sí, puedes apilar varias capas de ajuste — como Invert, Brightness y Hue/Saturation — para lograr efectos complejos.

**Q: ¿Dónde puedo encontrar documentación adicional para Aspose.PSD?**  
A: Consulta la documentación [here](https://reference.aspose.com/psd/java/) para guías completas y referencias de API.

**Q: ¿Hay una prueba gratuita disponible para Aspose.PSD?**  
A: Sí, puedes explorar la prueba gratuita [here](https://releases.aspose.com/).

**Q: ¿Cómo puedo obtener una licencia temporal para Aspose.PSD?**  
A: Puedes obtener una licencia temporal [here](https://purchase.aspose.com/temporary-license/).

---

**Última actualización:** 2025-12-02  
**Probado con:** Aspose.PSD 24.12 para Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}