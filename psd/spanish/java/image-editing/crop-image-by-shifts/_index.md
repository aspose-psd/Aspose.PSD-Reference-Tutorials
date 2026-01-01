---
date: 2026-01-01
description: Domina el procesamiento de imágenes en Java aprendiendo a recortar imágenes
  con Aspose.PSD para Java. Un tutorial completo para una manipulación de imágenes
  fluida.
linktitle: Crop Image by Shifts
second_title: Aspose.PSD Java API
title: Procesamiento de imágenes Java – Recortar imagen por desplazamientos con Aspose.PSD
url: /es/java/image-editing/crop-image-by-shifts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Procesamiento de Imágenes en Java – Recortar Imagen por Desplazamientos con Aspose.PSD

## Introducción

Si trabajas en **procesamiento de imágenes java**, descubrirás rápidamente que el recorte preciso es un bloque fundamental para cualquier flujo de trabajo gráfico. Ya sea que necesites recortar bordes, eliminar fondos no deseados o preparar recursos para la entrega web, saber **cómo recortar una imagen** programáticamente ahorra innumerables horas manuales. En este tutorial recorreremos el recorte de una imagen raster especificando valores de desplazamiento para cada lado, usando la potente biblioteca **Aspose.PSD for Java**. Al final podrás **usar el método de recorte** con confianza e incluso **optimizar el recorte de imágenes** para un mejor rendimiento.

## Respuestas rápidas
- **¿Qué biblioteca maneja el procesamiento de imágenes java?** Aspose.PSD for Java  
- **¿Qué método recorta una imagen raster?** `RasterImage.crop(left, right, top, bottom)`  
- **¿Necesito almacenar en caché los datos primero?** Sí – el caché mejora la velocidad para archivos PSD grandes  
- **¿Puedo establecer márgenes de recorte personalizados?** Por supuesto – especifica desplazamientos izquierdo, derecho, superior e inferior  
- **¿Qué formatos de salida son compatibles?** JPEG, PNG, BMP y muchos más mediante `ImageOptions`

## ¿Qué es el procesamiento de imágenes java?
El procesamiento de imágenes java se refiere a la manipulación de gráficos bitmap y vectoriales usando APIs basadas en Java. Las tareas incluyen redimensionado, filtrado, conversión de formatos y ajustes de **márgenes de recorte de imagen**, todo lo cual puede automatizarse en aplicaciones del lado del servidor o de escritorio.

## ¿Por qué usar Aspose.PSD para el procesamiento de imágenes java?
Aspose.PSD ofrece una solución puramente Java que entiende archivos PSD compatibles con Photoshop, capas, canales y máscaras. Elimina la necesidad de bibliotecas nativas, funciona multiplataforma y proporciona una API sencilla de **recorte de imagen raster** que se integra limpiamente con proyectos Java existentes.

## Requisitos previos

- **Java Development Kit (JDK)** – descarga la última versión desde [aquí](https://www.oracle.com/java/technologies/javase-downloads.html).  
- **Aspose.PSD for Java Library** – obtén la versión más reciente desde la [página de descarga](https://releases.aspose.com/psd/java/).  
- **Entorno de Desarrollo Integrado (IDE)** – Eclipse, IntelliJ IDEA o cualquier editor que prefieras.

## Importar paquetes

En tu proyecto Java, importa las clases necesarias para iniciar el flujo de trabajo de recorte:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Guía paso a paso

### Paso 1: Cargar la imagen (cómo recortar imagen)

Primero, carga el archivo PSD de origen en una instancia de `RasterImage`. Esto te brinda acceso directo a nivel de píxel.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
```

### Paso 2: Almacenar en caché los datos de la imagen (optimizar recorte de imagen)

Almacenar en caché los datos de la imagen en memoria reduce la sobrecarga de I/O al realizar múltiples operaciones como el recorte.

```java
if (!rasterImage.isCached()) {
  rasterImage.cacheData();
}
```

### Paso 3: Definir los márgenes de recorte (márgenes de recorte de imagen)

Especifica cuántos píxeles deseas recortar de cada lado. Ajusta estos valores para que coincidan con los **márgenes de recorte de imagen** deseados.

```java
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

### Paso 4: Aplicar el recorte (usar método de recorte)

Ahora llama al método `crop` con los valores de desplazamiento. Esta operación de **recorte de imagen raster** modifica el bitmap subyacente.

```java
rasterImage.crop(leftShift, rightShift, topShift, bottomShift);
```

### Paso 5: Guardar los resultados (cómo recortar imagen a un nuevo formato)

Finalmente, escribe la imagen recortada en disco. En este ejemplo elegimos JPEG, pero se puede usar cualquier formato compatible con Aspose.PSD.

```java
String destName = dataDir + "CroppingByShifts_out.jpg";
rasterImage.save(destName, new JpegOptions());
```

¡Felicidades! Has recortado exitosamente una **imagen por desplazamientos** usando Aspose.PSD for Java, una habilidad esencial en cualquier conjunto de herramientas de **procesamiento de imágenes java**.

## Problemas comunes y soluciones

| Problema | Solución |
|----------|----------|
| **`OutOfMemoryError` en archivos PSD grandes** | Asegúrate de llamar a `cacheData()` (Paso 2) y considera aumentar el tamaño del heap de la JVM (`-Xmx`). |
| **Bordes transparentes inesperados** | Verifica que tus valores de desplazamiento reflejen correctamente los márgenes deseados; los valores negativos pueden expandir en lugar de recortar. |
| **Guardado en el formato incorrecto** | Usa la subclase `ImageOptions` apropiada (p. ej., `PngOptions`) al llamar a `save`. |

## Preguntas frecuentes

**P: ¿Aspose.PSD es compatible con todos los formatos de imagen?**  
R: Sí, Aspose.PSD admite una amplia gama de formatos raster y vectoriales, garantizando versatilidad en tus proyectos.

**P: ¿Puedo aplicar múltiples operaciones de recorte a la misma imagen?**  
R: Por supuesto. Puedes llamar a `crop` repetidamente; cada llamada actúa sobre el estado actual de la imagen.

**P: ¿Existe un foro comunitario para soporte de Aspose.PSD?**  
R: Sí, puedes encontrar soporte y participar con la comunidad en el [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**P: ¿Cómo puedo obtener una licencia temporal para Aspose.PSD?**  
R: Visita [aquí](https://purchase.aspose.com/temporary-license/) para obtener una licencia temporal.

**P: ¿Hay proyectos de muestra que muestren funcionalidades de Aspose.PSD?**  
R: Explora la documentación y los ejemplos en la [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).

## Conclusión

En esta guía cubrimos todo lo necesario para **recortar archivos de imagen raster** especificando valores de desplazamiento, una técnica esencial para un **procesamiento de imágenes java** afinado. Ahora tienes una base sólida para integrar el recorte en flujos de trabajo más amplios, ya sea preparando recursos para la web, generando miniaturas o limpiando documentos escaneados.

---

**Última actualización:** 2026-01-01  
**Probado con:** Aspose.PSD 24.11 for Java  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}