---
date: 2025-12-17
description: Aprende cómo cargar archivos PSD en Java y leer capas PSD mientras se
  admite el recurso Nvrt usando Aspose.PSD.
linktitle: Support Nvrt Resource in PSD Files using Java
second_title: Aspose.PSD Java API
title: Cómo cargar archivos PSD y admitir recursos Nvrt usando Java
url: /es/java/advanced-psd-layer-features-effects/support-nvrt-resource-psd-files/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Soporte del recurso Nvrt en archivos PSD usando Java

## Cómo cargar archivos PSD en Java
Cuando necesitas **cómo cargar psd** archivos programáticamente, Java ofrece un ecosistema robusto—especialmente con la biblioteca Aspose.PSD. Ya sea que estés construyendo un editor gráfico, automatizando flujos de trabajo de diseño, o extrayendo recursos de documentos de Photoshop, dominar el manejo de PSD es esencial. En este tutorial recorreremos la carga de un PSD, la lectura de sus capas y, específicamente, el soporte del recurso Nvrt (Ajuste de Inversión).

## Respuestas rápidas
- **¿Qué biblioteca maneja archivos PSD en Java?** Aspose.PSD for Java  
- **¿Puedo leer capas PSD?** Sí, la API proporciona acceso completo a las estructuras de capas  
- **¿Se requiere una licencia para producción?** Sí, se necesita una licencia comercial  
- **¿Qué versión de JDK es compatible?** Java 8 y superiores  
- **¿Dónde puedo descargar la biblioteca?** Desde la página oficial de descarga de Aspose  

## Requisitos previos
Antes de comenzar a programar, asegúrate de tener lo siguiente:

- **Java Development Kit (JDK)** instalado (se recomienda Java 8+)  
- **Un IDE** como IntelliJ IDEA, Eclipse o VS Code  
- **Aspose.PSD for Java** library – descárgala desde el sitio oficial: [Descargar Aspose.PSD para Java](https://releases.aspose.com/psd/java/)  
- **Conocimientos básicos de Java** (clases, objetos, manejo de excepciones)  

## Importar paquetes
Una vez que tu entorno esté listo, importa las clases necesarias. Estas te dan acceso al manejo de PSD, al recorrido de capas y al recurso Nvrt.

```java
import com.aspose.psd.Image;
import com.aspose.psd.examples.Utils.Assert;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.fileformats.psd.layers.LayerResource;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.InvertAdjustmentLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.NvrtResource;
```

## ¿Por qué leer capas PSD?
Leer capas PSD te permite:

- Extraer recursos individuales (p. ej., íconos, máscaras) para reutilizar  
- Analizar capas de ajuste (como **Nvrt**) para comprender las ediciones de la imagen  
- Automatizar el procesamiento por lotes de archivos de diseño  

## Paso 1: Especifica tu directorio de origen
Establece la carpeta que contiene el PSD con el que deseas trabajar.

```java
String sourceDir = "Your Source Directory";
String inPsdFilePath = sourceDir + "InvertAdjustmentLayer.psd";
```

Reemplaza `"Your Source Directory"` con la ruta real en tu máquina.

## Paso 2: Carga el archivo PSD
Ahora realmente **cómo cargar psd** archivos usando la API de Aspose.

```java
PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);
```

El método `Image.load()` abre el archivo y lo prepara para su inspección.

## Paso 3: Inicializa la variable del recurso Nvrt
Almacenaremos aquí el recurso Nvrt encontrado.

```java
NvrtResource nvrtResource = null;
```

## Paso 4: Busca la capa de ajuste Invert
Itera a través de cada capa, localiza un `InvertAdjustmentLayer` y luego busca el `NvrtResource`.

```java
try {
    for (Layer layer : psdImage.getLayers()) {
        if (layer instanceof InvertAdjustmentLayer) {
            for (LayerResource layerResource : layer.getResources()) {
                if (layerResource instanceof NvrtResource) {
                    // The NvrtResource is found
                    nvrtResource = (NvrtResource)layerResource;
                    break;
                }
            }
        }
    }
} finally {
    psdImage.dispose();
}
```

El bloque `finally` garantiza que la imagen PSD se libere, manteniendo limpio el uso de memoria.

## Paso 5: Verifica el recurso Nvrt
Confirma que el recurso se haya localizado con éxito.

```java
Assert.isNotNull(nvrtResource);
```

Si la aserción pasa, has leído con éxito las capas PSD y extraído el recurso Nvrt.

## Errores comunes y consejos
- **Comprobaciones de null:** Siempre verifica que `psdImage` y los objetos de capa no sean nulos antes de acceder a ellos.  
- **Liberación de recursos:** Olvidar `psdImage.dispose()` puede provocar fugas de memoria en aplicaciones de larga duración.  
- **Problemas con rutas de archivo:** Usa rutas absolutas o asegúrate de que tu directorio de trabajo esté configurado correctamente para evitar `FileNotFoundException`.  

## Conclusión
Ahora sabes **cómo cargar psd** archivos, leer sus capas y extraer el recurso de ajuste Nvrt usando Java y Aspose.PSD. Esta base te permite crear potentes herramientas de automatización gráfica, procesar por lotes recursos de diseño o integrar datos de Photoshop en flujos de trabajo más amplios.

## Preguntas frecuentes

**P: ¿Qué es Aspose.PSD para Java?**  
R: Aspose.PSD para Java es una biblioteca que permite a los desarrolladores crear, editar, convertir y renderizar archivos PSD directamente desde código Java.

**P: ¿Puedo usar Aspose.PSD en productos comerciales?**  
R: Sí, se requiere una licencia comercial para uso en producción. Puedes explorar opciones de compra [aquí](https://purchase.aspose.com/buy).

**P: ¿Dónde puedo encontrar la documentación de Aspose.PSD?**  
R: La documentación completa está disponible aquí: [Documentación de Aspose.PSD](https://reference.aspose.com/psd/java/).

**P: ¿Hay una prueba gratuita disponible?**  
R: ¡Por supuesto! Puedes obtener una prueba gratuita de Aspose.PSD para Java [aquí](https://releases.aspose.com/).

**P: ¿Cómo puedo obtener soporte para Aspose.PSD?**  
R: Puedes hacer preguntas y obtener soporte en el foro de Aspose: [Soporte de Aspose](https://forum.aspose.com/c/psd/34).

---

**Última actualización:** 2025-12-17  
**Probado con:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}