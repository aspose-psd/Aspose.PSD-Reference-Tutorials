---
date: 2025-12-08
description: Aprende a convertir PSD a PNG y a redimensionar imágenes proporcionalmente
  en Java usando Aspose.PSD. Este tutorial paso a paso cubre el almacenamiento en
  caché de imágenes, el redimensionado y la guardado como PNG.
linktitle: Convert PSD to PNG & Resize Proportionally
second_title: Aspose.PSD Java API
title: Cómo convertir PSD a PNG y redimensionar proporcionalmente con Aspose.PSD para
  Java
url: /es/java/advanced-image-manipulation/resize-image-proportionally/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo convertir PSD a PNG y cambiar el tamaño proporcionalmente con Aspose.PSD para Java

## Introducción

Si necesitas **convertir PSD a PNG** manteniendo la proporción original, has llegado al lugar correcto. En este tutorial recorreremos un **tutorial completo de Aspose.PSD** que muestra **cómo cambiar el tamaño de la imagen** de forma proporcional en Java, almacenar en caché la imagen para un rendimiento óptimo y, finalmente, guardar el resultado como PNG. Al final podrás integrar este flujo de trabajo en cualquier canal de procesamiento de imágenes basado en Java.

## Respuestas rápidas
- **¿Aspose.PSD puede convertir PSD a PNG?** Sí, simplemente carga el PSD y guárdalo con `PngOptions`.
- **¿La biblioteca admite el cambio de tamaño proporcional?** Absolutamente; usa `resizeWidthProportionally` y `resizeHeightProportionally`.
- **¿Necesito almacenar la imagen en caché primero?** El caché (`image.cacheData()`) mejora el rendimiento para archivos PSD grandes.
- **¿Qué versión de Java se requiere?** Java 8 o superior es totalmente compatible.
- **¿Se necesita una licencia para producción?** Sí, una licencia comercial elimina las marcas de agua de evaluación.

## ¿Qué es “convertir PSD a PNG” y por qué es importante?

Convertir un documento de Photoshop (PSD) a un archivo portable network graphics (PNG) te permite compartir diseños con capas en un formato ligero y amigable para la web. PNG conserva la transparencia y la calidad sin pérdidas, lo que lo hace ideal para recursos de UI, miniaturas o cualquier escenario donde la fidelidad de la imagen sea crucial.

## ¿Por qué cambiar el tamaño de la imagen proporcionalmente en Java?

Cambiar el **tamaño de la imagen** sin distorsionar su relación de aspecto garantiza que los gráficos se vean naturales en diferentes pantallas. La API `Aspose.PSD` proporciona métodos dedicados para el escalado proporcional, que calculan automáticamente la altura o anchura coincidente, ahorrándote errores de cálculo manual.

## Requisitos previos

Antes de sumergirnos en el código, asegúrate de contar con:

1. **Java Development Kit (JDK)** – Java 8 o posterior instalado.
2. **Aspose.PSD para Java** – descarga el último JAR desde el sitio oficial [here](https://releases.aspose.com/psd/java/).
3. Un archivo PSD de ejemplo (`sample.psd`) colocado en un directorio al que puedas referenciar desde tu proyecto.

## Importar paquetes

Agrega las importaciones necesarias a tu clase Java. Estas clases te dan acceso a la carga de imágenes, caché, cambio de tamaño y opciones de salida PNG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.PngOptions;
```

## Paso 1: Cargar la imagen PSD

Primero, carga el archivo PSD de origen. Si el archivo es grande, almacenar en caché los datos de la imagen reduce el consumo de memoria cuando realices operaciones posteriores.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    // Image caching java – improves performance for large files
    image.cacheData();
}
```

## Paso 2: Cambiar el tamaño de la imagen proporcionalmente (Java)

Ahora decide las nuevas dimensiones. En este ejemplo reducimos la imagen a **la mitad** de su tamaño original mientras preservamos la relación de aspecto. Puedes ajustar la anchura o altura objetivo según sea necesario.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

> **Consejo profesional:** Usa `resizeWidthProportionally` *o* `resizeHeightProportionally`; la biblioteca calcula automáticamente la otra dimensión para mantener la proporcionalidad de la imagen.

## Paso 3: Guardar la imagen redimensionada como PNG

Finalmente, exporta la imagen redimensionada al formato PNG. Este paso completa el flujo de **convertir PSD a PNG**.

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

Cuando el código se ejecute, encontrarás un archivo PNG que es la mitad del tamaño del PSD original, con la misma calidad visual y sin distorsión.

## Problemas comunes y soluciones

| Problema | Causa | Solución |
|----------|-------|----------|
| **OutOfMemoryError** | PSD grande no almacenado en caché | Llama a `image.cacheData()` antes de cambiar el tamaño |
| **Salida PNG en blanco** | Ruta de archivo incorrecta | Verifica `dataDir` y los permisos de escritura |
| **La relación de aspecto se ve incorrecta** | Uso simultáneo de anchura y altura manualmente | Usa los métodos proporcionales provistos por Aspose.PSD |

## Preguntas frecuentes

**P: ¿Aspose.PSD es compatible con todos los formatos de imagen?**  
R: Aspose.PSD soporta PSD, PNG, JPEG, BMP, GIF y muchos más. Consulta la lista completa en la [documentación](https://reference.aspose.com/psd/java/).

**P: ¿Puedo usar Aspose.PSD en proyectos comerciales?**  
R: Sí. Compra una licencia comercial en la [tienda de Aspose](https://purchase.aspose.com/buy).

**P: ¿Existen licencias temporales para pruebas?**  
R: Absolutamente – solicita una licencia temporal [here](https://purchase.aspose.com/temporary-license/) para propósitos de evaluación.

**P: ¿Dónde puedo encontrar soporte de la comunidad?**  
R: El [foro de Aspose.PSD](https://forum.aspose.com/c/psd/34) es un excelente lugar para hacer preguntas y compartir soluciones.

**P: ¿Cómo accedo a la referencia completa de la API?**  
R: La documentación detallada de la API está disponible [here](https://reference.aspose.com/psd/java/).

## Conclusión

Ahora sabes cómo **convertir PSD a PNG**, cambiar el tamaño de la imagen proporcionalmente y manejar el caché de manera eficiente usando Aspose.PSD para Java. Incorpora estos pasos en tus propias aplicaciones para ofrecer un procesamiento de imágenes rápido y de alta calidad sin depender de instalaciones nativas de Photoshop.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Última actualización:** 2025-12-08  
**Probado con:** Aspose.PSD 24.12 para Java  
**Autor:** Aspose