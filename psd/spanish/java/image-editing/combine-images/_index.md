---
date: 2025-12-30
description: Aprende a crear archivos PSD en Java combinando dos imágenes usando Aspose.PSD.
  Sigue nuestra guía paso a paso para fusionar imágenes en un archivo PSD rápidamente.
linktitle: Combine Images
second_title: Aspose.PSD Java API
title: Cómo crear un archivo PSD en Java – Combinar imágenes con Aspose.PSD
url: /es/java/image-editing/combine-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crear archivo PSD en Java – Combinar imágenes usando Aspose.PSD

## Introducción

Si necesitas **crear un archivo PSD en Java** combinando varias imágenes, Aspose.PSD hace el trabajo sencillo. En este tutorial recorreremos el proceso de combinar dos imágenes en un solo lienzo PSD, explicaremos por qué este enfoque es útil y te proporcionaremos código listo para ejecutar. Al final podrás **combinar dos imágenes en Java** y generar un archivo con capas de aspecto profesional.

## Respuestas rápidas
- **¿Qué biblioteca es la mejor para combinar imágenes en PSD?** Aspose.PSD para Java.  
- **¿Cuánto tiempo lleva la implementación?** Aproximadamente 10‑15 minutos para una combinación básica.  
- **¿Necesito una licencia?** Una prueba gratuita funciona para pruebas; se requiere una licencia comercial para producción.  
- **¿Puedo añadir más de dos imágenes?** Sí – repite las llamadas a `drawImage` para cada capa adicional.  
- **¿Qué versión de Java es compatible?** Java 8 y posteriores.

## Requisitos previos

Antes de comenzar, asegúrate de tener lo siguiente:

1. **Biblioteca Aspose.PSD** – descárgala desde [here](https://releases.aspose.com/psd/java/).  
2. **Java Development Kit (JDK)** – se recomienda Java 8+.  
3. **Directorio de documentos** – una carpeta en tu máquina donde se almacenarán las imágenes fuente y el PSD resultante.

## Importar paquetes

Comienza importando las clases necesarias de Aspose.PSD en tu proyecto:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

## Guía paso a paso

### Paso 1: Crear opciones PSD (preparar el archivo)

Primero creamos una instancia de `PsdOptions` que contendrá la configuración de salida.

```java
PsdOptions imageOptions = new PsdOptions();
```

### Paso 2: Establecer FileCreateSource (definir dónde se guardará el PSD)

Asigna un `FileCreateSource` a las opciones, apuntando al archivo de resultado deseado.

```java
imageOptions.setSource(new FileCreateSource(dataDir + "Two_images_result_out.psd", false));
```

### Paso 3: Crear instancia Image (inicializar el tamaño del lienzo)

Crea un objeto `Image` con las opciones y especifica un lienzo de 600 × 600 píxeles.

```java
Image image = Image.create(imageOptions, 600, 600);
```

### Paso 4: Inicializar Graphics y dibujar la primera imagen

Un objeto `Graphics` nos permite pintar en el lienzo. Limpiamos el fondo a blanco y dibujamos la primera imagen fuente en la mitad izquierda.

```java
Graphics graphics = new Graphics(image);
graphics.clear(Color.getWhite());
graphics.drawImage(Image.load(dataDir + "example1.psd"), 0, 0, 300, 600);
```

### Paso 5: Dibujar la segunda imagen (completar la combinación)

Ahora colocamos la segunda imagen en la mitad derecha del mismo lienzo.

```java
graphics.drawImage(Image.load(dataDir + "example2.psd"), 300, 0, 300, 600);
```

### Paso 6: Guardar el archivo PSD resultante

Finalmente, guardamos el lienzo combinado en disco.

```java
image.save();
```

¡Felicidades! Has **combinado imágenes en PSD** exitosamente y creado un archivo PSD en Java.

## ¿Por qué combinar imágenes con Aspose.PSD?

- **Con capas** – cada llamada a `drawImage` agrega una capa separada que puedes editar después.  
- **Flexibilidad de formato** – soporta PSD, PNG, JPEG, BMP y más.  
- **Sin dependencias nativas** – Java puro, funciona en cualquier SO que ejecute el JDK.  

## Problemas comunes y soluciones

| Problema | Causa | Solución |
|----------|-------|----------|
| Error `File not found` al cargar imágenes fuente | Ruta `dataDir` incorrecta | Verifica que `dataDir` apunte a la carpeta que contiene `example1.psd` y `example2.psd`. |
| El PSD de salida está en blanco | `graphics.clear` llamado después de dibujar | Asegúrate de que `graphics.clear(Color.getWhite())` se ejecute **antes** de cualquier llamada a `drawImage`. |
| Excepción de licencia en tiempo de ejecución | Licencia Aspose.PSD faltante o expirada | Aplica una licencia válida usando `License license = new License(); license.setLicense("Aspose.PSD.lic");` antes de cualquier llamada a la API. |

## Preguntas frecuentes

### P1: ¿Aspose.PSD es compatible con todos los formatos de imagen?
R1: Aspose.PSD se centra principalmente en el formato de archivo PSD. Sin embargo, soporta varios otros formatos para entrada y salida.

### P2: ¿Puedo realizar modificaciones adicionales en la imagen combinada?
R2: ¡Claro! Después de combinar imágenes, puedes manipular aún más el PSD resultante usando las amplias funciones de Aspose.PSD.

### P3: ¿Existen requisitos de licencia para usar Aspose.PSD?
R3: Sí, se requiere una licencia válida para uso comercial. Obténla desde [here](https://purchase.aspose.com/buy).

### P4: ¿Hay una prueba gratuita disponible para Aspose.PSD?
R4: Sí, puedes explorar Aspose.PSD con una prueba gratuita [here](https://releases.aspose.com/).

### P5: ¿Dónde puedo encontrar soporte para consultas relacionadas con Aspose.PSD?
R5: Visita el [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) para soporte comunitario y discusiones.

---

**Last Updated:** 2025-12-30  
**Tested With:** Aspose.PSD 24.11 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}