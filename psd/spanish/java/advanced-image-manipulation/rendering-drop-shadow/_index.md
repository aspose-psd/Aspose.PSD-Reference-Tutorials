---
date: 2025-12-04
description: Aprenda cómo guardar PSD como PNG y aplicar una sombra paralela de renderizado
  usando Aspose.PSD para Java. Esta guía cubre cómo agregar sombra, convertir PSD
  a PNG y aplicar sombra paralela en Java.
language: es
linktitle: Apply Rendering Drop Shadow
second_title: Aspose.PSD Java API
title: Guardar PSD como PNG y agregar sombra paralela con Aspose.PSD Java
url: /java/advanced-image-manipulation/rendering-drop-shadow/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Guardar PSD como PNG y agregar sombra paralela con Aspose.PSD Java

## Introducción

Si trabajas con archivos de Photoshop en Java, **guardar PSD como PNG** mientras añades una sombra paralela de aspecto profesional es un requisito frecuente. Aspose.PSD hace que esta tarea sea sencilla, permitiéndote **convertir PSD a PNG** y **aplicar sombra paralela Java** en solo unas pocas líneas de código. En este tutorial recorreremos todo el proceso, desde cargar un archivo PSD hasta exportar el PNG final con el efecto de sombra renderizado.

## Respuestas rápidas
- **¿Qué significa “guardar PSD como PNG”?** Convierte un archivo de Photoshop con capas en una imagen PNG plana, preservando la transparencia.  
- **¿Puedo agregar una sombra paralela al convertir?** Sí—Aspose.PSD le permite modificar los efectos de capa antes de la exportación.  
- **¿Necesito una licencia para ejecutar el código?** Una prueba gratuita sirve para evaluación; se requiere una licencia para producción.  
- **¿Qué versión de Java es compatible?** Java 8 o superior.  
- **¿El efecto de sombra paralela es personalizable?** Absolutamente—puede ajustar color, opacidad, distancia, tamaño, ángulo y más.

## Requisitos previos

Antes de comenzar, asegúrate de tener:

- **Entorno de desarrollo Java** – JDK 8 o más reciente instalado.  
- **Biblioteca Aspose.PSD** – Descargue el último JAR desde el sitio oficial [aquí](https://releases.aspose.com/psd/java/).  
- **Un archivo PSD** – Un archivo que contiene al menos una capa que desea realzar con una sombra.  

## ¿Cómo guardar PSD como PNG con una sombra paralela en Java?

A continuación tienes una guía paso a paso. Cada paso incluye una breve explicación seguida del código exacto que debes copiar.

### Paso 1: Importar los paquetes necesarios

Comenzamos importando las clases que proporcionan la carga de imágenes, el manejo de efectos y la capacidad de exportar a PNG.

```java
import com.aspose.psd.Image;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.layereffects.DropShadowEffect;
import com.aspose.psd.imageloadoptions.PsdLoadOptions;
import com.aspose.psd.Color;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
```

### Paso 2: Definir el directorio del documento

Establece la carpeta donde vivirán tu PSD de origen y el PNG resultante.

```java
String dataDir = "Your Document Directory";
```

### Paso 3: Establecer rutas de archivo PSD y PNG

Especifica las rutas completas para el PSD de entrada y el PNG de salida.

```java
String sourceFileName = dataDir + "Shadow.psd";
String pngExportPath = dataDir + "Shadowchanged1.png";
```

### Paso 4: Cargar el archivo PSD con efectos habilitados

Habilitar **loadEffectsResource** garantiza que los efectos de capa (como sombras) estén disponibles para su manipulación.

```java
PsdLoadOptions loadOptions = new PsdLoadOptions();
loadOptions.setLoadEffectsResource(true);

PsdImage im = (PsdImage) Image.load(sourceFileName, loadOptions);
```

### Paso 5: Acceder al efecto de sombra paralela

Aquí obtenemos el primer efecto aplicado a la segunda capa (índice 1). Aquí es donde leeremos o modificaremos los parámetros de la sombra.

```java
DropShadowEffect shadowEffect = (DropShadowEffect) (im.getLayers()[1].getBlendingOptions().getEffects()[0]);
```

### Paso 6: Validar las propiedades del efecto de sombra (Opcional pero útil)

Comprobar las propiedades existentes te ayuda a decidir si necesitas cambiar algo. Las aserciones a continuación confirman los valores predeterminados.

```java
Assert.areEqual(Color.getBlack(), shadowEffect.getColor());
Assert.areEqual(255, shadowEffect.getOpacity());
Assert.areEqual(3, shadowEffect.getDistance());
Assert.areEqual(7, shadowEffect.getSize());
Assert.areEqual(true, shadowEffect.getUseGlobalLight());
Assert.areEqual(90, shadowEffect.getAngle());
Assert.areEqual(0, shadowEffect.getSpread());
Assert.areEqual(0, shadowEffect.getNoise());
```

> **Consejo profesional:** Si desea **cómo agregar sombra** con configuraciones personalizadas, modifique las propiedades en `shadowEffect` antes de guardar (p.ej., `shadowEffect.setColor(Color.getRed());`).

### Paso 7: Guardar la imagen modificada como PNG

Finalmente, exportamos el PSD (con la sombra renderizada) a un archivo PNG. La opción `TruecolorWithAlpha` preserva la transparencia.

```java
PngOptions saveOptions = new PngOptions();
saveOptions.setColorType(PngColorType.TruecolorWithAlpha);
im.save(pngExportPath, saveOptions);
```

Y eso es todo: un flujo de trabajo completo para **convertir PSD a PNG** que también **aplica sombra paralela java** en una sola pasada.

## ¿Por qué usar Aspose.PSD para esta tarea?

- **No se requiere Photoshop nativo** – Funciona en cualquier plataforma que soporte Java.  
- **Fidelidad total del PSD** – Toda la información de capas, máscaras y efectos se preserva.  
- **Control fino** – Ajuste cada parámetro de la sombra paralela antes de la exportación.  
- **Alto rendimiento** – Optimizado para archivos grandes y procesamiento por lotes.

## Problemas comunes y solución de problemas

| Síntoma | Causa probable | Solución |
|---------|----------------|----------|
| `NullPointerException` on `shadowEffect` | La capa objetivo no tiene efectos o el índice es incorrecto. | Verifique el índice de la capa (`im.getLayers()[i]`) y asegúrese de que exista un efecto. |
| Exported PNG is blank | Opciones PNG no configuradas correctamente o la imagen no se guardó. | Use `PngColorType.TruecolorWithAlpha` y confirme que la ruta de `im.save()` sea escribible. |
| Shadow color is not visible | Opacidad de la sombra establecida en 0 o el color coincide con el fondo. | Establezca `shadowEffect.setOpacity(255);` y elija un color contrastante. |

## Preguntas frecuentes

**Q: ¿Puedo aplicar sombras paralelas a varias capas a la vez?**  
A: Sí. Recorra `im.getLayers()` y modifique el `DropShadowEffect` de cada capa según sea necesario.

**Q: ¿Qué hace el parámetro ‘Spread’?**  
A: Controla cuán abruptamente la sombra pasa de totalmente opaca a transparente. Un spread mayor crea un borde más duro.

**Q: ¿Aspose.PSD es compatible con todas las versiones de Photoshop?**  
A: Soporta una amplia gama de versiones de PSD, desde lanzamientos tempranos hasta los últimos archivos de Photoshop CC.

**Q: ¿Cómo puedo obtener ayuda si tengo problemas?**  
A: Visite el [foro de Aspose.PSD](https://forum.aspose.com/c/psd/34) para soporte comunitario y asistencia oficial.

**Q: ¿Puedo probar Aspose.PSD antes de comprar?**  
A: Por supuesto. Descargue una prueba gratuita desde el [sitio web de Aspose](https://releases.aspose.com/).

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

**Última actualización:** 2025-12-04  
**Probado con:** Aspose.PSD 24.12 for Java  
**Autor:** Aspose  

---