---
date: 2026-03-02
description: Aprende cómo agregar relleno creando una capa de relleno de color en
  archivos PSD usando Java y Aspose.PSD. Sigue nuestra guía paso a paso para establecer
  rápidamente el color de la capa de relleno.
linktitle: Add Color Fill Layer to PSD Files using Java
second_title: Aspose.PSD Java API
title: 'Cómo agregar relleno: agregar capa de relleno de color a archivos PSD usando
  Java'
url: /es/java/modifying-converting-psd-images/add-color-fill-layer-psd-files/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Añadir capa de relleno de color a archivos PSD usando Java

## Introducción
¿Alguna vez has necesitado manipular archivos de Photoshop de forma programática, tal vez para añadir un toque de color a un diseño? Si te preguntas **cómo añadir relleno** a un PSD, estás en el lugar correcto. En este tutorial recorreremos cómo agregar una capa de relleno de color a archivos PSD (Photoshop Document) usando Java y la biblioteca Aspose.PSD. Piensa en tu PSD como un lienzo digital; al final sabrás crear una capa de relleno de color, establecer el color de la capa de relleno y guardar el archivo actualizado en solo unas pocas líneas de código.

## Respuestas rápidas
- **¿Qué biblioteca se necesita?** Aspose.PSD para Java  
- **Caso de uso principal?** Añadir o cambiar colores de relleno en PSD de forma programática  
- **¿Cuánto tiempo lleva la implementación?** Aproximadamente 10‑15 minutos para un escenario básico  
- **¿Necesito una licencia?** Una prueba gratuita sirve para evaluación; se requiere una licencia comercial para producción  
- **¿Versión de Java compatible?** Java 8 y superiores  

## ¿Qué es una capa de relleno de color?
Una capa de relleno de color es una superposición de color sólido que se sitúa encima de otras capas en un documento de Photoshop. Se usa a menudo para añadir color de fondo, crear máscaras o cambiar rápidamente el tema visual de un diseño sin editar píxeles individuales.

## ¿Por qué añadir una capa de relleno de color con código?
- **Automatización:** Generar activos de marca consistentes en muchos archivos.  
- **Procesamiento por lotes:** Actualizar decenas de PSD en segundos en lugar de hacerlo manualmente.  
- **Diseños dinámicos:** Cambiar colores al instante según la entrada del usuario o fuentes de datos.

## Requisitos previos
Antes de sumergirnos en el código, asegúrate de tener todo lo necesario:

1. **Java Development Kit (JDK)** – JDK 8 o superior instalado.  
2. **Biblioteca Aspose.PSD** – Descarga el JAR más reciente desde la [Aspose Releases page](https://releases.aspose.com/psd/java/).  
3. **IDE** – IntelliJ IDEA, Eclipse, NetBeans o cualquier editor que prefieras.  
4. **Conocimientos básicos de Java** – Familiaridad con objetos, bucles y manejo de excepciones.

## Importar paquetes
Ahora que cubrimos lo básico, importemos las clases necesarias. Estas importaciones nos dan acceso al manejo de PSD y a la manipulación de capas de relleno.

```java
import com.aspose.psd.Color;
import com.aspose.psd.Image;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer;
import com.aspose.psd.fileformats.psd.layers.fillsettings.FillType;
import com.aspose.psd.fileformats.psd.layers.fillsettings.IColorFillSettings;
```

## Cómo añadir relleno – Guía paso a paso

### Paso 1: Configura tu entorno
Define dónde se encuentra tu PSD de origen y dónde se guardará el archivo editado, luego carga el documento.

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "ColorFillLayer.psd";
String exportPath     = dataDir + "ColorFillLayer_output.psd";
PsdImage im = (PsdImage) Image.load(sourceFileName);
```

- `dataDir` apunta a la carpeta que contiene tu PSD.  
- `sourceFileName` es el archivo original que modificarás.  
- `exportPath` es donde se escribirá el nuevo archivo con la **capa de relleno de color añadida**.  

### Paso 2: Recorrer las capas
Necesitamos localizar cualquier capa de relleno existente para poder modificarla o crear una nueva.

```java
for (int i = 0; i < im.getLayers().length; i++) {
    if (im.getLayers()[i] instanceof FillLayer) {
        FillLayer fillLayer = (FillLayer) im.getLayers()[i];
```

- El bucle `for` itera sobre cada capa del PSD.  
- La comprobación `instanceof FillLayer` asegura que solo trabajemos con capas de relleno.

### Paso 3: Verificar el tipo de relleno
Asegúrate de que la capa encontrada sea una **capa de relleno de color** antes de intentar cambiar su color.

```java
if (fillLayer.getFillSettings().getFillType() != FillType.Color) {
    throw new Exception("Wrong Fill Layer");
}
```

Si el tipo de relleno no es `FillType.Color`, abortamos para evitar alterar inadvertidamente rellenos de degradado o patrón.

### Paso 4: Establecer el color de relleno
Aquí es donde **establecemos el color de la capa de relleno**. El ejemplo cambia la capa a rojo, pero puedes reemplazar `Color.getRed()` por cualquier otro `Color` que necesites (p. ej., `Color.getBlue()`, `new Color(255, 165, 0)` para naranja).

```java
IColorFillSettings settings = (IColorFillSettings) fillLayer.getFillSettings();
settings.setColor(Color.getRed());
fillLayer.update();
```

- `settings.setColor(...)` cambia el color real del relleno.  
- `fillLayer.update()` actualiza la capa para que se aplique el nuevo color.  

### Paso 5: Guardar los cambios
Finalmente, escribe el PSD modificado de nuevo en el disco.

```java
im.save(exportPath);
break;
```

- El `break` detiene el bucle después de actualizar la primera capa de relleno coincidente, que es normalmente lo que deseas cuando solo necesitas **cambiar el color de relleno del PSD** una vez.

## Problemas comunes y consejos
- **No se encontró FillLayer:** Si tu PSD no contiene una capa de relleno, deberás crear una usando `new FillLayer(im)` y añadirla a `im.getLayers()`.  
- **El color no se actualiza:** Asegúrate de llamar a `fillLayer.update()` después de establecer el color.  
- **El archivo no se guarda:** Verifica que `exportPath` apunte a un directorio con permisos de escritura y que tengas autorización para escribir archivos allí.  

## Preguntas frecuentes

**P: ¿Qué es Aspose.PSD?**  
R: Aspose.PSD es una robusta biblioteca Java que permite crear, editar y convertir archivos Photoshop PSD sin necesidad de Adobe Photoshop.

**P: ¿Puedo usar Aspose.PSD de forma gratuita?**  
R: Sí, hay una prueba gratuita disponible en la [Aspose Releases page](https://releases.aspose.com/).  

**P: ¿Con qué otros formatos de archivo puedo trabajar además de PSD?**  
R: Aspose.PSD admite PSD, PSB, BMP, JPEG, PNG, GIF, TIFF y más.

**P: ¿Cómo obtengo soporte si tengo problemas?**  
R: Puedes hacer preguntas en el [Aspose Support Forum](https://forum.aspose.com/c/psd/34).  

**P: ¿Dónde puedo comprar una licencia completa?**  
R: Las licencias se venden a través de la [Aspose Purchase page](https://purchase.aspose.com/buy).

## Conclusión
Ahora sabes **cómo añadir relleno** a un documento Photoshop de forma programática con Java. Creando o localizando una capa de relleno de color, estableciendo su color y guardando el resultado, puedes automatizar tareas de diseño repetitivas, generar activos dinámicos o integrar la manipulación de PSD en aplicaciones Java más grandes. Pruébalo: experimenta con diferentes colores, añade múltiples capas de relleno o combina esta técnica con otras funcionalidades de Aspose.PSD para crear potentes flujos de procesamiento de imágenes.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Última actualización:** 2026-03-02  
**Probado con:** Aspose.PSD for Java 24.11 (última versión al momento de escribir)  
**Autor:** Aspose  

---