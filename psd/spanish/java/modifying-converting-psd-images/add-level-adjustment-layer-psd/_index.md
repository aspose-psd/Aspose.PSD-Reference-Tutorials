---
date: 2026-03-07
description: Aprende a ajustar los niveles añadiendo una capa de ajuste de niveles
  en archivos PSD usando Aspose.PSD para Java. Domina los ajustes tonales rápidamente.
linktitle: Add Level Adjustment Layer in PSD
second_title: Aspose.PSD Java API
title: Cómo ajustar niveles – Añadir capa de ajuste de nivel en PSD
url: /es/java/modifying-converting-psd-images/add-level-adjustment-layer-psd/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Añadir capa de ajuste de niveles en PSD

## Introducción
Si buscas **cómo ajustar niveles** en tus documentos de Photoshop, la Capa de ajuste de niveles es la herramienta perfecta. Permite afinar sombras, tonos medios y luces sin alterar permanentemente los píxeles originales. En este tutorial veremos cómo añadir una Capa de ajuste de niveles a un archivo PSD usando Aspose.PSD for Java, para que puedas lograr un control tonal de nivel profesional en solo unos pasos.

## Respuestas rápidas
- **¿Qué hace una Capa de ajuste de niveles?** Modifica el rango tonal de una imagen de forma no destructiva.  
- **¿Qué biblioteca se usa?** Aspose.PSD for Java.  
- **¿Necesito una licencia?** Una prueba gratuita funciona para desarrollo; se requiere una licencia para producción.  
- **¿Cuánto tiempo lleva la implementación?** Aproximadamente 10‑15 minutos para un ajuste básico.  
- **¿Puedo ajustar varios canales?** Sí, puedes establecer niveles de entrada/salida para cada canal de color individualmente.

## ¿Qué es una Capa de ajuste de niveles?
Una Capa de ajuste de niveles te permite corregir el equilibrio tonal de una imagen ajustando sombras de entrada, tonos medios y luces, así como los niveles de salida. Como vive en su propia capa, puedes alternar su visibilidad o eliminarla sin afectar el arte subyacente.

## ¿Por qué añadir una Capa de ajuste de niveles con Aspose.PSD?
- **Automatización:** Integra ajustes de niveles en tuberías de procesamiento por lotes.  
- **Multiplataforma:** Funciona en cualquier SO que soporte Java.  
- **Precisión:** Accede a la configuración de cada canal programáticamente para obtener resultados exactos.  

## Requisitos previos
1. Java Development Kit (JDK). Si no lo tienes, descárgalo desde el [sitio web de Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) o usa OpenJDK.  
2. Biblioteca Aspose.PSD for Java – obtén el JAR más reciente desde este [enlace de descarga](https://releases.aspose.com/psd/java/).  
3. Conocimientos básicos de programación en Java.  
4. Un IDE como IntelliJ IDEA, Eclipse o NetBeans con el JAR de Aspose.PSD añadido al classpath del proyecto.

## Importar paquetes
Antes de comenzar a escribir nuestro código, necesitamos importar los paquetes necesarios de la biblioteca Aspose.PSD. Así es como puedes hacerlo:
```java
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.adjustmentlayers.LevelsLayer;
import com.aspose.psd.fileformats.psd.layers.layerresources.LevelChannel;
```
Estas importaciones nos dan acceso a clases para cargar archivos PSD, trabajar con capas de ajuste de niveles y manipular la configuración de canales individuales.

## Cómo ajustar niveles en un archivo PSD
A continuación se muestra una guía paso a paso que te indica exactamente **cómo ajustar niveles** programáticamente.

### Paso 1: Configurar rutas de archivo
Define dónde se encuentra el PSD de origen y dónde se guardará el archivo editado.
```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "LevelsAdjustmentLayer.psd";
String psdPathAfterChange = dataDir + "LevelsAdjustmentLayerChanged.psd";
```
Reemplaza `"Your Document Directory"` con la carpeta real en tu máquina.

### Paso 2: Cargar el archivo PSD
Crea una instancia de `PsdImage` a partir del archivo de origen.
```java
PsdImage im = (PsdImage) Image.load(sourceFileName);
```
Ahora tienes acceso completo a todas las capas dentro del PSD.

### Paso 3: Recorrer las capas
Encuentra la Capa de ajuste de niveles que deseas modificar.
```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof LevelsLayer) {
        LevelsLayer levelsLayer = (LevelsLayer) im.getLayers()[i];
        // Further manipulation will go here...
    }
}
```
La verificación `instanceof LevelsLayer` garantiza que solo trabajemos con capas de ajuste de niveles.

### Paso 4: Ajustar la configuración del canal de niveles
Ajusta los valores de entrada y salida para el canal seleccionado.
```java
LevelChannel channel = levelsLayer.getChannel(0);
channel.setInputMidtoneLevel(2.0f);
channel.setInputShadowLevel((short) 10);
channel.setInputHighlightLevel((short) 230);
channel.setOutputShadowLevel((short) 20);
channel.setOutputHighlightLevel((short) 200);
```
- **Nivel medio de entrada:** Desplaza el rango de tonos medios.  
- **Nivel de sombra de entrada:** Oscurece o aclara las sombras.  
- **Nivel de resaltado de entrada:** Controla las partes más brillantes.  
- **Niveles de sombra/resaltado de salida:** Definen el rango de salida final.

Siéntete libre de experimentar con diferentes valores para ver cómo afectan a la imagen.

### Paso 5: Guardar el archivo PSD modificado
Guarda tus cambios en un nuevo archivo.
```java
im.save(psdPathAfterChange);
```
Encontrarás el PSD actualizado en la ubicación que especificaste en `psdPathAfterChange`.

## Problemas comunes y soluciones
- **Archivo no encontrado:** Verifica que `dataDir` apunte a la carpeta correcta y que el PSD de origen exista.  
- **ClassCastException:** Asegúrate de que el archivo que cargas sea realmente un PSD; otros formatos requieren clases diferentes.  
- **Errores de licencia:** Usa una licencia válida de Aspose.PSD para compilaciones de producción; la versión de prueba funciona para desarrollo.

## Conclusión
Ahora sabes **cómo ajustar niveles** añadiendo y configurando una Capa de ajuste de niveles en un archivo PSD con Aspose.PSD for Java. Esta técnica te brinda un control preciso sobre el equilibrio tonal mientras mantienes tu flujo de trabajo totalmente automatizado. Sigue experimentando con diferentes valores de canal y explora el procesamiento por lotes para aplicar los mismos ajustes a múltiples imágenes.

## Preguntas frecuentes

**P: ¿Qué es una Capa de ajuste de niveles?**  
R: Es una capa no destructiva que te permite modificar el rango tonal (sombras, tonos medios, luces) de una imagen.

**P: ¿Puedo usar Aspose.PSD sin comprar una licencia?**  
R: Sí, puedes evaluar la biblioteca con una prueba gratuita, pero se requiere una licencia para despliegues comerciales.

**P: ¿Dónde puedo encontrar la documentación de Aspose.PSD?**  
R: Puedes encontrar la documentación [aquí](https://reference.aspose.com/psd/java/).

**P: ¿Existe soporte comunitario para los productos Aspose?**  
R: ¡Absolutamente! Puedes hacer preguntas y obtener ayuda en el [foro de Aspose](https://forum.aspose.com/c/psd/34).

**P: ¿Cómo puedo obtener una licencia temporal para Aspose.PSD?**  
R: Puedes solicitar una licencia temporal [aquí](https://purchase.aspose.com/temporary-license/).

---

**Última actualización:** 2026-03-07  
**Probado con:** Aspose.PSD última versión (Java)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}