---
date: 2025-12-17
description: Apprenez à convertir un PSD en PNG tout en définissant le mode couleur
  du PSD en niveaux de gris 16 bits à l’aide d’Aspose.PSD pour Java. Guide étape par
  étape avec des exemples de code.
linktitle: Convert PSD to PNG – 16-bit Grayscale – Java
second_title: Aspose.PSD Java API
title: Comment convertir un PSD en PNG avec le mode couleur niveaux de gris 16 bits
  en Java
url: /fr/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir PSD en PNG avec le mode couleur gris 16 bits en Java

## Introduction
Lorsque vous vous plongez dans le monde du design graphique et de la manipulation d’images, comprendre comment **convertir PSD en PNG** revient à posséder une arme secrète. En particulier, l’utilisation d’un mode gris 16 bits confère à vos images une profondeur et des détails époustouflants qui les font vraiment ressortir. Dans ce tutoriel, nous allons vous montrer comment **définir le mode couleur du PSD** en gris 16 bits, puis **exporter le PSD en PNG** à l’aide d’Aspose.PSD pour Java. Prêt à améliorer votre flux de travail d’image ? C’est parti.

## Quick Answers
- **Que comprend “convertir PSD en PNG” ?** Chargement d’un PSD, modification éventuelle de son mode couleur, puis sauvegarde en fichier PNG.  
- **Quelle classe Aspose gère la conversion ?** `PsdImage` pour le chargement et `PngOptions` pour la sauvegarde.  
- **Ai‑je besoin d’une licence spéciale ?** Une version d’essai suffit pour les tests ; une licence payante est requise en production.  
- **Puis‑je conserver la profondeur 16 bits dans le PNG ?** Oui, en utilisant `PngColorType.GrayscaleWithAlpha`.  
- **Quels IDE sont supportés ?** Tout IDE Java – IntelliJ IDEA, Eclipse, VS Code, etc.

## Prerequisites
Avant de commencer, assurons‑nous que vous avez tout ce qu’il faut pour tirer le meilleur parti de ce tutoriel. Voici ce dont vous aurez besoin :

1. **Java Development Kit (JDK)** – Assurez‑vous d’avoir la dernière version installée. Vous pouvez le télécharger depuis [Oracle's site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Aspose.PSD for Java Library** – C’est le moteur qui nous permettra de manipuler les fichiers PSD. Procurez‑vous-le depuis la [page de téléchargement Aspose](https://releases.aspose.com/psd/java/).  
3. **Un IDE** – IntelliJ IDEA, Eclipse ou Visual Studio Code fonctionneront parfaitement.  
4. **Connaissances de base en Java** – Une familiarité avec la syntaxe Java rendra les étapes plus fluides.  
5. **Un fichier PSD d’exemple** – Créez‑en un dans Adobe Photoshop ou téléchargez un exemple gratuit en ligne.

Prêt ? Super ! Importons les packages nécessaires et commençons à coder.

## Import Packages
Pour démarrer, ajoutez les imports Aspose.PSD requis à votre fichier Java :

```java
import com.aspose.psd.*;
import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.fileformats.psd.ColorModes;
import com.aspose.psd.fileformats.psd.CompressionMethod;
import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.system.Enum;
```

Ces imports vous donnent accès aux fonctionnalités nécessaires pour manipuler les fichiers PSD, définir le mode couleur et exporter le résultat en PNG.

## Step 1: Define Your Directories
Tout d’abord, configurez les dossiers source et de sortie. Cela indique au programme où lire le PSD original et où écrire les fichiers convertis.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

Remplacez les chaînes de caractères factices par les chemins réels sur votre machine.

## Step 2: Create a Method to Handle Image Processing
Nous allons encapsuler la logique de conversion dans une méthode réutilisable. Elle reçoit tous les paramètres que vous pourriez vouloir ajuster, tels que le mode couleur, la profondeur de bits et la compression.

```java
class LocalScopeExtension {
    void saveToPsdThenLoadAndSaveToPng(
        String file,
        short colorMode,
        short channelBitsCount,
        short channelsCount,
        short compression,
        int layerNumber) {
```

Cette méthode vous permet de **définir le mode couleur du PSD** puis de **exporter le PSD en PNG** en un seul flux.

## Step 3: Define File Paths and Load the PSD
À l’intérieur de la méthode, construisez les chemins de fichiers complets et chargez le PSD gris 16 bits original :

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

Le `postfix` vous aide à suivre les paramètres utilisés pour chaque fichier exporté.

## Step 4: Process the Layer or Full Image
Nous dessinons maintenant soit sur un calque spécifique, soit sur l’image entière. Dans cet exemple, nous ajoutons une fine bordure grise pour rendre le résultat plus visible.

```java
try {
    RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;
    // Draw a gray inner border around the perimeter of the layer
    Graphics graphics = new Graphics(raster);
    int width = raster.getWidth();
    int height = raster.getHeight();
    Rectangle rect = new Rectangle(
        width / 3,
        height / 3,
        width - (2 * (width / 3)) - 1,
        height - (2 * (height / 3)) - 1);
    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);
```

Le rectangle est calculé dynamiquement afin de rester centré quel que soit la taille de l’image.

## Step 5: Save the Modified PSD File
Après le dessin, nous sauvegardons le PSD avec le mode couleur et la profondeur de bits exacts que vous avez spécifiés. C’est le cœur du **définir le mode couleur du PSD** avant la conversion.

```java
    // Save a copy of PSD with specific characteristics
    PsdOptions psdOptions = new PsdOptions();
    psdOptions.setColorMode(colorMode);
    psdOptions.setChannelBitsCount(channelBitsCount);
    psdOptions.setChannelsCount(channelsCount);
    psdOptions.setCompressionMethod(compression);
    image.save(exportPath, psdOptions);
}
```

## Step 6: Convert the PSD to PNG
Enfin, nous chargeons le PSD fraîchement sauvegardé et l’exportons en PNG. En utilisant `PngColorType.GrayscaleWithAlpha`, nous préservons la profondeur 16 bits dans le fichier PNG.

```java
finally {
    image.dispose();
}
// Load the saved PSD
PsdImage image1 = (PsdImage)Image.load(exportPath);
try {
    // Convert the saved PSD to a grayscale PNG image
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);
    image1.save(pngExportPath, pngOptions); // here should be no exception
}
finally {
    image1.dispose();
}
```

Vous avez maintenant **converti le PSD en PNG** tout en conservant les données gris 16 bits de haute qualité.

## Common Issues and Solutions
| Issue | Why It Happens | Fix |
|-------|----------------|-----|
| **Exception “Unsupported color type”** | Tentative de sauvegarder un PSD avec une configuration de canaux non prise en charge. | Assurez‑vous que `channelBitsCount` correspond à la profondeur réelle (16) et que `channelsCount` est correct pour le gris (1). |
| **File not found** | Chemin du répertoire source incorrect. | Vérifiez la chaîne `sourceDir` et assurez‑vous que le fichier PSD existe. |
| **Output PNG appears black** | PNG sauvegardé sans prise en charge du canal alpha. | Utilisez `PngColorType.GrayscaleWithAlpha` comme indiqué ci‑dessus. |

## Frequently Asked Questions

**Q : Qu’est‑ce que le mode couleur gris 16 bits ?**  
R : Il offre 65 536 nuances de gris, fournissant beaucoup plus de détails tonaux que le mode standard 8 bits (256 nuances).

**Q : Puis‑je utiliser Aspose.PSD pour des images non‑grises ?**  
R : Absolument ! Aspose.PSD prend en charge RGB, CMYK, Lab et de nombreux autres modes couleur.

**Q : Existe‑t‑il une version d’essai d’Aspose.PSD ?**  
R : Oui, vous pouvez essayer une version d’essai gratuite d’Aspose.PSD. Rendez‑vous simplement sur la [page de téléchargement Aspose](https://releases.aspose.com/).

**Q : Où puis‑je trouver plus d’exemples d’utilisation d’Aspose.PSD ?**  
R : Consultez la [documentation](https://reference.aspose.com/psd/java/) pour des exemples plus détaillés et des tutoriels.

**Q : Comment acheter une licence pour Aspose.PSD ?**  
R : Vous pouvez acheter une licence en visitant la [page d’achat Aspose](https://purchase.aspose.com/buy).

---

**Last Updated:** 2025-12-17  
**Tested With:** Aspose.PSD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}