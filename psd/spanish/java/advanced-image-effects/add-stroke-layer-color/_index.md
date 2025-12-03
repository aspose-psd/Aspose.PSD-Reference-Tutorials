---
date: 2025-11-30
description: Aprende a agregar trazo y cambiar el color del trazo en PSD usando Aspose.PSD
  para Java. Sigue esta guía paso a paso para modificar el color y la opacidad de
  la capa de trazo.
language: es
linktitle: Add Stroke Layer Color
second_title: Aspose.PSD Java API
title: Cómo agregar color de capa de trazo en Aspose.PSD para Java
url: /java/advanced-image-effects/add-stroke-layer-color/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo agregar color de capa de trazo en Aspose.PSD para Java

## Introducción

Si necesitas **cómo agregar trazo** a un documento de Photoshop de forma programática, Aspose.PSD para Java lo hace sencillo. En este tutorial recorreremos cómo agregar un color de capa de trazo, ajustar su opacidad y guardar el resultado. Al final también verás cómo **cambiar el color del trazo** (o *cambiar el color del trazo PSD*) para cualquier capa existente, dándote control creativo total desde tu código Java.

## Respuestas rápidas
- **¿Qué biblioteca se requiere?** Aspose.PSD para Java (última versión).  
- **¿Puedo cambiar el color del trazo?** Sí – usa `ColorFillSettings` para establecer cualquier `Color`.  
- **¿Necesito una licencia?** Una licencia temporal funciona para evaluación; se requiere una licencia completa para producción.  
- **¿Qué versión de Java es compatible?** Java 8 o superior.  
- **¿Cuánto tiempo lleva la implementación?** Normalmente menos de 10 minutos para un cambio básico de trazo.

## ¿Qué es una capa de trazo en un PSD?
Una capa de trazo es un efecto vectorial que dibuja un contorno alrededor del contenido de una capa. Puede personalizarse con color, grosor, opacidad y modo de fusión. Modificar este efecto programáticamente permite branding automatizado, procesamiento por lotes o generación dinámica de gráficos.

## ¿Por qué usar Aspose.PSD para cambiar el color del trazo?
- **No se requiere Photoshop** – trabaja completamente en Java.  
- **Cumplimiento total de la especificación PSD** – todas las funciones modernas de PSD son compatibles.  
- **Alto rendimiento** – procesa archivos grandes rápidamente.  
- **Multiplataforma** – se ejecuta en cualquier SO con una JVM.

## Requisitos previos

- **Biblioteca Aspose.PSD** – descárgala desde la [documentación oficial](https://reference.aspose.com/psd/java/).  
- **Java Development Kit (JDK)** – versión 8 o más reciente.  
- **IDE** – Eclipse, IntelliJ IDEA, o cualquier editor compatible con Java.

## Importar paquetes

Primero, importa las clases que necesitarás. Esto le da a tu proyecto acceso a la manipulación de PSD y a las API de efectos de trazo.

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

## Paso 1: Configura tu proyecto

Crea un nuevo proyecto Java, agrega el JAR de Aspose.PSD a la ruta de compilación y verifica que la biblioteca se cargue sin errores.

## Paso 2: Carga el archivo PSD

Habilita la carga de recursos de efectos para que la información del trazo esté disponible.

```java
String dataDir = "Your Document Directory";

String sourceFileName = dataDir + "Stroke.psd";
String exportPath = dataDir + "StrokeGradientChanged.psd";

PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage)Image.load(sourceFileName, loadOptions);
```

## Paso 3: Accede a la capa de efecto de trazo

Recupera el primer efecto de trazo de la segunda capa (índice 1).

```java
StrokeEffect colorStroke = (StrokeEffect)im.getLayers()[1].getBlendingOptions().getEffects()[0];
```

## Paso 4: Validar propiedades del trazo

Confirma las propiedades existentes antes de realizar cambios. Esto ayuda a evitar resultados inesperados.

```java
Assert.areEqual(BlendMode.Normal, colorStroke.getBlendMode());
Assert.areEqual(255, colorStroke.getOpacity());
Assert.areEqual(true, colorStroke.isVisible());
```

## Paso 5: Establecer color y opacidad (Cómo cambiar el color del trazo)

Aquí **cambiamos el color del trazo PSD** a amarillo y reducimos la opacidad al 50 % (127 / 255).

```java
ColorFillSettings fillSettings = (ColorFillSettings)colorStroke.getFillSettings();
fillSettings.setColor(Color.getYellow());

colorStroke.setOpacity((byte)127);
```

## Paso 6: Guardar el PSD modificado

Escribe la imagen actualizada de nuevo en disco. El nuevo archivo ahora contiene el trazo modificado.

```java
im.save(exportPath);
```

## Problemas comunes y consejos

- **Comprobaciones de null** – siempre verifica que `getEffects()` devuelva un arreglo no nulo antes de hacer casting.  
- **Índice de capa** – las capas PSD son indexadas desde cero; asegúrate de apuntar a la capa correcta.  
- **Formato de color** – `Color.getYellow()` es solo un ejemplo; puedes crear colores personalizados con `new Color(r, g, b)`.  
- **Rango de opacidad** – la opacidad es un byte (0–255); los valores superiores a 255 serán limitados.

## Conclusión

Ahora has aprendido **cómo agregar trazo** a un archivo PSD y **cómo cambiar el color del trazo** usando Aspose.PSD para Java. Experimenta con diferentes colores, modos de fusión y opacidades para lograr el estilo visual exacto que tu proyecto necesita.

## Preguntas frecuentes

**P: ¿Puedo usar Aspose.PSD con otras bibliotecas gráficas de Java?**  
R: Sí, Aspose.PSD puede combinarse con bibliotecas como Apache Commons Imaging o Java2D para funcionalidades ampliadas.

**P: ¿Aspose.PSD es compatible con el último formato de archivo PSD?**  
R: Absolutamente. La biblioteca se actualiza regularmente para soportar las especificaciones más recientes de Photoshop.

**P: ¿Cómo manejo excepciones al usar Aspose.PSD?**  
R: Consulta el [foro de soporte](https://forum.aspose.com/c/psd/34) para obtener solución de problemas detallada y ejemplos de código de manejo de errores.

**P: ¿Puedo probar Aspose.PSD antes de comprar?**  
R: ¡Claro! Obtén una [prueba gratuita](https://releases.aspose.com/) para explorar todas las funciones.

**P: ¿Dónde puedo obtener una licencia temporal para Aspose.PSD?**  
R: Obtén una [licencia temporal](https://purchase.aspose.com/temporary-license/) para evaluar la biblioteca en tu entorno de desarrollo.

---

**Última actualización:** 2025-11-30  
**Probado con:** Aspose.PSD 24.11 para Java  
**Autor:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
