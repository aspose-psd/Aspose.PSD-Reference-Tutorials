---
date: 2026-03-15
description: Aprende a crear archivos PSD, generar la paleta de colores PSD y establecer
  el modo de color PSD usando Aspose.PSD para Java en esta guía paso a paso.
linktitle: Create Indexed PSD Files using Aspose.PSD for Java
second_title: Aspose.PSD Java API
title: Cómo crear archivos PSD usando Aspose.PSD para Java
url: /es/java/modifying-converting-psd-images/create-indexed-psd-files/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cómo crear archivos PSD usando Aspose.PSD para Java

## Introducción
Si alguna vez te has preguntado **cómo crear PSD** de forma programática, estás en el lugar correcto. Aspose.PSD para Java te brinda control total sobre los documentos de Photoshop, permitiéndote generar, editar y guardar archivos PSD sin necesidad de abrir Photoshop. En este tutorial recorreremos la creación de un archivo **PSD indexado**, la configuración del modo de color PSD y la generación de una paleta de colores personalizada, todo con código Java claro y paso a paso. Ya sea que estés construyendo una canalización gráfica, automatizando la creación de recursos o simplemente experimentando, los conceptos aquí te ayudarán a dar vida a tus ideas visuales.

## Respuestas rápidas
- **¿Qué biblioteca necesito?** Aspose.PSD para Java  
- **¿Puedo crear un PSD indexado?** Sí, configurando el modo de color a `Indexed`  
- **¿Necesito tener Photoshop instalado?** No, Aspose.PSD funciona de forma independiente  
- **¿Qué versión de Java se requiere?** JDK 8 o posterior  
- **¿Qué tan grande puede ser el lienzo?** Cualquier tamaño; este ejemplo usa 500 × 500 px  

## ¿Qué es un archivo PSD indexado?
Un PSD indexado almacena los colores en una paleta en lugar de valores de color completos para cada píxel. Esto reduce el tamaño del archivo y es ideal para gráficos con colores limitados, como íconos o recursos de UI. Al generar una paleta personalizada controlas exactamente qué colores aparecen en la imagen final.

## ¿Por qué generar una paleta de colores PSD?
Crear una **paleta de colores PSD** te permite:
- Mantener los tamaños de archivo pequeños para uso web o móvil  
- Garantizar una marca consistente limitando los colores a tu paleta corporativa  
- Acelerar el renderizado en aplicaciones que admiten imágenes indexadas  

## Requisitos previos
Antes de sumergirnos en el código, asegúrate de contar con lo siguiente:

1. **Conocimientos básicos de Java** – deberías estar cómodo con clases, métodos y creación de objetos.  
2. **Java Development Kit (JDK) 8+** – instalado y configurado en tu IDE.  
3. **IDE (IntelliJ IDEA, Eclipse, etc.)** – opcional pero muy recomendado para facilitar la depuración.  
4. **Biblioteca Aspose.PSD para Java** – descárgala **[aquí](https://releases.aspose.com/psd/java/)** y agrega el JAR al classpath de tu proyecto.  
5. **Conceptos fundamentales de diseño gráfico** – comprender los modos de color, paletas y formas básicas te ayudará a seguir el tutorial.

## Importar paquetes
Antes de continuar con el código, asegurémonos de que tenemos todos los paquetes necesarios importados en tu aplicación Java. Esto es lo que necesitarás:

```java
import com.aspose.psd.Color;
import com.aspose.psd.Graphics;
import com.aspose.psd.Image;
import com.aspose.psd.Pen;
import com.aspose.psd.Rectangle;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdColorPalette;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.sources.FileCreateSource;
```

Estas importaciones te permitirán trabajar con opciones PSD, colores y manipulación gráfica a través de Aspose.PSD.

Ahora, desglosaremos el código paso a paso para **cómo crear PSD** con un modo de color indexado.

## Paso 1: Configurar el directorio del documento
Primero, define dónde se guardará el PSD generado.

```java
String dataDir = "Your Document Directory";
```

Reemplaza `"Your Document Directory"` con una ruta absoluta o relativa, por ejemplo, `"/Users/YourName/Documents/"`.

## Paso 2: Crear una instancia de PsdOptions
`PsdOptions` contiene todas las configuraciones para el archivo que estás a punto de generar.

```java
PsdOptions createOptions = new PsdOptions();
```

## Paso 3: Establecer propiedades principales de PsdOptions
Aquí especificamos la ubicación de salida, el **modo de color PSD** a `Indexed` y la versión del PSD.

```java
createOptions.setSource(new FileCreateSource(dataDir + "Newsample_out.psd", false));
createOptions.setColorMode(ColorModes.Indexed);
createOptions.setVersion(5);
```

- **Source** – la ruta completa del nuevo archivo.  
- **Color Mode** – `Indexed` indica a Aspose.PSD que use una imagen basada en paleta.  
- **Version** – versión del formato PSD (5 funciona para la mayoría de las versiones modernas de Photoshop).

## Paso 4: Crear una paleta de colores (Generar paleta de colores PSD)
Define los colores que estarán disponibles en la imagen indexada.

```java
Color[] palette = { Color.getRed(), Color.getGreen(), Color.getBlue(), Color.getYellow() };
createOptions.setPalette(new PsdColorPalette(palette));
createOptions.setCompressionMethod(CompressionMethod.RLE);
```

- La matriz `palette` contiene hasta 256 objetos `Color`.  
- `CompressionMethod.RLE` proporciona compresión sin pérdida eficiente para imágenes indexadas.

## Paso 5: Crear el lienzo de la imagen PSD
Ahora creamos un PSD en blanco con las dimensiones que deseamos.

```java
Image psd = Image.create(createOptions, 500, 500);
```

Esto crea un lienzo de 500 × 500 píxeles que utiliza la paleta definida anteriormente.

## Paso 6: Dibujar gráficos en el PSD
Agrega contenido visual; aquí dibujamos una elipse roja simple sobre un fondo blanco.

```java
Graphics graphics = new Graphics(psd);
graphics.clear(Color.getWhite());
graphics.drawEllipse(new Pen(Color.getRed(), 6), new Rectangle(0, 0, 400, 400));
```

- `clear(Color.getWhite())` rellena el fondo de blanco.  
- `drawEllipse` dibuja una elipse roja con un trazo de 6 píxeles.

## Paso 7: Guardar el archivo PSD
Finalmente, persiste la imagen en disco.

```java
psd.save();
```

El archivo `Newsample_out.psd` aparecerá en el directorio que especificaste anteriormente.

## Problemas comunes y consejos
- **Tamaño de la paleta** – Si necesitas más de 4 colores, simplemente añádelos a la matriz `palette` (hasta 256).  
- **Permisos de archivo** – Asegúrate de que el proceso Java tenga acceso de escritura a `dataDir`.  
- **Modo de color incorrecto** – Olvidar `createOptions.setColorMode(ColorModes.Indexed)` producirá un PSD RGB en lugar de uno indexado.  

## Preguntas frecuentes

**P: ¿Qué es Aspose.PSD para Java?**  
R: Aspose.PSD para Java es una biblioteca que permite la manipulación de archivos PSD (Photoshop) de forma programática usando Java.

**P: ¿Puedo usar Aspose.PSD de forma gratuita?**  
R: Sí, puedes acceder a una versión de prueba gratuita de Aspose.PSD **[aquí](https://releases.aspose.com/)**.

**P: ¿Necesito tener Photoshop instalado para trabajar con Aspose.PSD?**  
R: No, puedes crear y manipular archivos PSD sin Photoshop, ya que Aspose.PSD gestiona todas las operaciones de manera independiente.

**P: ¿Cómo obtengo una licencia temporal para Aspose.PSD?**  
R: Puedes solicitar una licencia temporal **[aquí](https://purchase.aspose.com/temporary-license/)**.

**P: ¿Dónde puedo obtener soporte para Aspose.PSD?**  
R: Puedes obtener soporte en el foro de Aspose **[aquí](https://forum.aspose.com/c/psd/34)**.

## Conclusión
Acabas de aprender **cómo crear PSD** con un modo de color indexado, generar una paleta personalizada y añadir gráficos simples, todo usando Aspose.PSD para Java. Con estos bloques de construcción puedes ampliar a dibujos más complejos, gestión de capas y procesamiento por lotes. Para una exploración más profunda, consulta la referencia oficial de la API **[aquí](https://reference.aspose.com/psd/java/)** y sigue experimentando con diferentes paletas y primitivas de dibujo.

---

**Última actualización:** 2026-03-15  
**Probado con:** Aspose.PSD para Java 24.12 (última)  
**Autor:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}