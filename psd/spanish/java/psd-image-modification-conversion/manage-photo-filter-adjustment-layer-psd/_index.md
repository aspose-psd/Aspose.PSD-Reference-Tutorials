---
date: 2026-03-28
description: Aprende cómo crear una capa de filtro fotográfico y añadir capas de ajuste
  en archivos PSD usando Aspose.PSD para Java. Sigue esta guía para editar y agregar
  filtros sin esfuerzo.
linktitle: How to Create Photo Filter Layer in PSD Using Java
second_title: Aspose.PSD Java API
title: Cómo crear una capa de filtro fotográfico en PSD usando Java
url: /es/java/psd-image-modification-conversion/manage-photo-filter-adjustment-layer-psd/
weight: 24
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Administrar capa de ajuste de filtro fotográfico en PSD - Java

## Introducción
Si eres un desarrollador Java que busca **crear capas de filtro fotográfico** dentro de archivos PSD, has llegado al lugar correcto. En este tutorial recorreremos el uso de Aspose.PSD para Java para editar capas de ajuste de filtro fotográfico existentes y añadir nuevas. Al final, sabrás exactamente cómo **crear una capa de filtro fotográfico**, ajustar sus propiedades e incluso **añadir archivos PSD de capa de ajuste** de forma programática, acelerando tu flujo de trabajo de diseño gráfico.

## Respuestas rápidas
- **¿Qué biblioteca maneja capas PSD en Java?** Aspose.PSD for Java  
- **¿Puedo editar una capa de filtro fotográfico existente?** Sí – carga el PSD, localiza el `PhotoFilterLayer` y luego modifica sus propiedades.  
- **¿Cómo añado una nueva capa de filtro?** Usa `addPhotoFilterLayer(Color)` en una instancia de `PsdImage`.  
- **¿Necesito una licencia para producción?** Se requiere una licencia comercial; hay una versión de prueba gratuita disponible.  
- **¿Qué versión de Java es compatible?** JDK 8 o superior (se recomienda JDK 11).  

## ¿Qué es una capa de ajuste de filtro fotográfico?
Una capa de ajuste de filtro fotográfico es un efecto no destructivo que tiñe toda la imagen con un color elegido, similar a aplicar un filtro fotográfico. Vive en su propia capa, lo que permite ajustar el color, la densidad y la luminosidad sin alterar los píxeles originales.

## ¿Por qué usar Aspose.PSD para crear una capa de filtro fotográfico?
- **Control total** sobre la estructura PSD sin Adobe Photoshop.  
- **Multiplataforma** la API Java funciona en Windows, Linux y macOS.  
- **Sin interop COM** – Java puro, ideal para procesamiento del lado del servidor.  
- **Compatible con PSD versión 1‑8**, preservando efectos de capa y máscaras.

## Requisitos previos
### Software esencial
1. Java Development Kit (JDK): Asegúrate de tener una versión compatible del JDK instalada en tu máquina. Puedes descargarla desde [Oracle's website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
2. Aspose.PSD for Java: Para manipular archivos PSD, necesitarás la biblioteca Aspose.PSD. Puedes descargarla desde la [Aspose releases page](https://releases.aspose.com/psd/java/). No olvides consultar la [Aspose documentation](https://reference.aspose.com/psd/java/) para más detalles.
3. IDE (Entorno de Desarrollo Integrado): Un buen IDE como IntelliJ IDEA o Eclipse hará que tu experiencia de codificación sea más fluida.

### Comprender los conceptos básicos
Familiaridad con la programación Java y una comprensión básica de cómo funcionan los archivos PSD será beneficiosa. Si eres nuevo en el uso de bibliotecas en Java, es una buena idea acostumbrarte a importar y utilizar frameworks.

## Importar paquetes
Para comenzar, necesitamos importar las clases necesarias de la biblioteca Aspose.PSD. Aquí tienes una simple declaración de importación que necesitarás al inicio de tu archivo Java:
```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.PhotoFilterLayer;
```
Simplemente pega esto al inicio de tu archivo Java, ¡y estarás listo para comenzar a trabajar con imágenes PSD!

## Editar capa de filtro fotográfico existente
### Paso 1: Configurar el directorio de datos
Primero, necesitas definir el directorio donde se almacenan tus archivos PSD. Reemplaza `"Your Document Directory"` con la ruta real. Así es como organizas todo:
```java
String dataDir = "Your Document Directory";
```

### Paso 2: Cargar su archivo PSD
Ahora, carguemos el archivo PSD que deseas editar. Asegúrate de que `PhotoFilterAdjustmentLayer.psd` exista en el directorio especificado.
```java
String sourceFileName = dataDir + "PhotoFilterAdjustmentLayer.psd";
```

### Paso 3: Inicializar el objeto de imagen
Usando la funcionalidad incorporada de Aspose, cargamos la imagen en nuestro proyecto:
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

### Paso 4: Recorrer las capas
A continuación, examinaremos las capas dentro del archivo PSD. Nuestro objetivo es localizar el `PhotoFilterLayer`:
```java
for(int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof PhotoFilterLayer) {
        PhotoFilterLayer photoLayer = (PhotoFilterLayer) im.getLayers()[i];
        // Make changes to the layer
    }
}
```

### Paso 5: Personalizar la capa de filtro fotográfico
¡Aquí es donde ocurre la magia! Puedes modificar el `Color` y la `Density`. Por ejemplo, podemos establecer el color a un rojo vibrante y ajustar la densidad:
```java
photoLayer.setColor(Color.fromArgb(255, 60, 60));
photoLayer.setDensity(78);
photoLayer.setPreserveLuminosity(false);
```

### Paso 6: Guardar el archivo PSD editado
Finalmente, guarda los cambios para crear un nuevo archivo PSD con tus ajustes:
```java
String psdPathAfterChange = dataDir + "PhotoFilterAdjustmentLayerChanged.psd";
im.save(psdPathAfterChange);
```
Acabas de editar una capa de ajuste de filtro fotográfico en un archivo PSD.

## Añadir una nueva capa de filtro fotográfico
### Paso 1: Configurar la ruta del directorio
Como antes, comenzamos definiendo nuestro directorio de datos:
```java
String dataDir = "Your Document Directory";
```

### Paso 2: Cargar el archivo fuente
Para este ejemplo, carguemos un archivo PSD diferente donde queremos **añadir capa de ajuste PSD**:
```java
String sourceFileName = dataDir + "PhotoExample.psd";
```

### Paso 3: Inicializar nuevamente el objeto de imagen
Debemos crear una nueva instancia de `PsdImage`, así que cargamos el archivo:
```java
PsdImage img = (PsdImage) Image.load(sourceFileName);
```

### Paso 4: Añadir una capa de filtro fotográfico
Ahora, podemos añadir una nueva capa de filtro fotográfico con un color personalizado. Así se hace:
```java
PhotoFilterLayer layer = img.addPhotoFilterLayer(Color.fromArgb(25, 255, 35));
```

### Paso 5: Guardar el nuevo archivo PSD
Una vez más, es momento de guardar nuestros cambios. Aquí está la línea para hacerlo:
```java
String psdPathAfterChange = dataDir + "PhotoExampleAddedPhotoFilter.psd";
img.save(psdPathAfterChange);
```
Has añadido con éxito una nueva capa de filtro fotográfico a tu archivo PSD.

## Problemas comunes y soluciones
- **`ClassCastException` al cargar la imagen** – Asegúrate de que el archivo que cargas sea un PSD; otros formatos requieren clases diferentes.  
- **Los valores de color aparecen incorrectos** – Usa `Color.fromArgb(alpha, red, green, blue)` donde cada componente está entre 0‑255.  
- **Capa no encontrada** – Verifica que el PSD fuente realmente contenga un `PhotoFilterLayer`. Usa `im.getLayers().length` para depurar.

## Preguntas frecuentes
### ¿Qué es Aspose.PSD?
Aspose.PSD es una biblioteca .NET y Java para crear, editar y convertir archivos PSD.

### ¿Puedo probar Aspose.PSD gratis?
Sí, Aspose ofrece una versión de prueba gratuita. Échale un vistazo [aquí](https://releases.aspose.com/).

### ¿Dónde puedo encontrar la documentación?
Puedes encontrar la documentación completa en la [página de referencia de Aspose](https://reference.aspose.com/psd/java/).

### ¿Cómo puedo comprar Aspose.PSD?
Puedes comprar el software desde [este enlace](https://purchase.aspose.com/buy).

### ¿Hay soporte disponible para Aspose.PSD?
¡Absolutamente! Puedes obtener soporte a través del foro de soporte de Aspose [aquí](https://forum.aspose.com/c/psd/34).

**Última actualización:** 2026-03-28  
**Probado con:** Aspose.PSD for Java 24.11 (latest as of 2026)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}