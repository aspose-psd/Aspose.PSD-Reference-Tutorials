---
date: 2026-02-20
description: Apprenez comment convertir un PSD en PNG tout en définissant le mode
  couleur du PSD en niveaux de gris 16 bits à l’aide d’Aspose.PSD pour Java. Guide
  étape par étape avec des exemples de code.
linktitle: Convert PSD to PNG – 16-bit Grayscale – Java
second_title: Aspose.PSD Java API
title: Comment convertir un PSD en PNG avec le mode couleur niveaux de gris 16 bits
  en Java
url: /fr/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

_BLOCK_0}} not code fences. Should keep them unchanged.

We need to translate text inside code blocks? The placeholders are not actual code, but we shouldn't translate them. So just leave as is.

We need to translate table content.

Let's produce final content.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir PSD en PNG avec le mode couleur gris 16 bits en Java

## Introduction
Lorsque vous vous plongez dans le monde du design graphique et de la manipulation d’images, savoir **comment convertir PSD en PNG** est comme disposer d’une arme secrète. Utiliser un mode gris 16 bits ajoute une profondeur et une richesse tonale incroyables, faisant ressortir vos images. Dans ce tutoriel, nous allons parcourir comment **définir le mode couleur du PSD** en gris 16 bits puis **exporter le PSD en PNG** à l’aide d’Aspose.PSD pour Java. Prêt à améliorer votre flux de travail d’image ? C’est parti.

## Réponses rapides
- **Que signifie « convertir PSD en PNG » ?** Charger un PSD, éventuellement changer son mode couleur, puis l’enregistrer en fichier PNG.  
- **Quelle classe Aspose gère la conversion ?** `PsdImage` pour le chargement et `PngOptions` pour l’enregistrement.  
- **Ai‑je besoin d’une licence spéciale ?** Une version d’essai suffit pour les tests ; une licence payante est requise en production.  
- **Puis‑je conserver la profondeur de 16 bits dans le PNG ?** Oui, en utilisant `PngColorType.GrayscaleWithAlpha`.  
- **Quels IDE sont supportés ?** Tous les IDE Java – IntelliJ IDEA, Eclipse, VS Code, etc.

## Pourquoi convertir PSD en PNG avec le gris 16 bits ?
* **Conserver le détail tonal :** le gris 16 bits stocke 65 536 nuances de gris, bien plus que les 256 nuances d’une image 8 bits.  
* **Large compatibilité :** le PNG est largement supporté sur les navigateurs, les applications mobiles et les outils de bureau, tout en conservant des données de haute qualité.  
* **Flux de travail sans perte :** la conversion avec Aspose.PSD garantit l’absence d’artéfacts de compression indésirables, idéal pour l’archivage ou un traitement ultérieur.

## Prérequis
Avant de commencer, assurons‑nous que tout est prêt pour tirer le meilleur parti de ce tutoriel. Voici ce dont vous aurez besoin :

1. **Java Development Kit (JDK)** – Assurez‑vous d’avoir la dernière version installée. Vous pouvez la télécharger depuis le [site d’Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Bibliothèque Aspose.PSD pour Java** – C’est le moteur qui nous permettra de manipuler les fichiers PSD. Téléchargez‑la depuis la [page de téléchargement Aspose](https://releases.aspose.com/psd/java/).  
3. **Un IDE** – IntelliJ IDEA, Eclipse ou Visual Studio Code conviendront parfaitement.  
4. **Connaissances de base en Java** – Une familiarité avec la syntaxe Java rendra les étapes plus fluides.  
5. **Un fichier PSD d’exemple** – Créez‑en un dans Adobe Photoshop ou téléchargez un exemple gratuit en ligne.

Prêt ? Super ! Importons les packages nécessaires et commençons à coder.

## Importer les packages
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

## Étape 1 : Définir vos répertoires
Tout d’abord, configurez les dossiers source et de sortie. Cela indique au programme où lire le PSD original et où écrire les fichiers convertis.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

Remplacez les chaînes de caractères factices par les chemins réels sur votre machine.

## Étape 2 : Créer une méthode pour gérer le traitement d’image
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

Cette méthode vous permet de **définir le mode couleur du PSD** puis **d’exporter le PSD en PNG** en un seul flux.

## Étape 3 : Définir les chemins de fichiers et charger le PSD
À l’intérieur de la méthode, construisez les chemins complets et chargez le PSD gris 16 bits original :

```java
String filePath = sourceDir + file + ".psd";
String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +
                 channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);
String exportPath = outputDir + file + postfix + ".psd";
String pngExportPath = outputDir + file + postfix + ".png";
// Load a predefined 16-bit grayscale PSD
PsdImage image = (PsdImage)Image.load(filePath);
```

Le `postfix` vous aide à suivre les réglages utilisés pour chaque fichier exporté.

## Étape 4 : Traiter le calque ou l’image complète
Nous allons maintenant soit dessiner sur un calque spécifique, soit sur l’image entière. Dans cet exemple, nous ajoutons une bordure grise subtile pour rendre le résultat plus visible.

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

## Étape 5 : Enregistrer le fichier PSD modifié
Après le dessin, nous enregistrons le PSD avec le mode couleur et la profondeur de bits exacts que vous avez spécifiés. C’est le cœur du **définir le mode couleur du PSD** avant la conversion.

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

## Étape 6 : Convertir le PSD en PNG
Enfin, nous chargeons le PSD fraîchement enregistré et l’exportons en PNG. En utilisant `PngColorType.GrayscaleWithAlpha`, nous conservons la profondeur de 16 bits dans le fichier PNG.

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

Vous avez maintenant **converti PSD en PNG** tout en conservant les données gris 16 bits de haute qualité.

## Problèmes courants et solutions
| Problème | Pourquoi cela se produit | Solution |
|----------|--------------------------|----------|
| **Exception « Unsupported color type »** | Tentative d’enregistrement d’un PSD avec une configuration de canaux non prise en charge. | Assurez‑vous que `channelBitsCount` correspond à la profondeur réelle (16) et que `channelsCount` est correct pour le gris (1). |
| **Fichier introuvable** | Chemin du répertoire source incorrect. | Vérifiez la chaîne `sourceDir` et assurez‑vous que le fichier PSD existe. |
| **Le PNG de sortie apparaît noir** | PNG enregistré sans gestion du canal alpha. | Utilisez `PngColorType.GrayscaleWithAlpha` comme indiqué ci‑dessus. |

## Questions fréquentes

**Q : Qu’est‑ce que le mode couleur gris 16 bits ?**  
R : Il offre 65 536 nuances de gris, fournissant beaucoup plus de détail tonal que le mode standard 8 bits (256 nuances).

**Q : Puis‑je utiliser Aspose.PSD pour des images non‑gris ?**  
R : Absolument ! Aspose.PSD supporte RGB, CMYK, Lab et de nombreux autres modes couleur.

**Q : Existe‑t‑il une version d’essai d’Aspose.PSD ?**  
R : Oui, vous pouvez essayer une version d’essai gratuite d’Aspose.PSD. Rendez‑vous simplement sur la [page de téléchargement Aspose](https://releases.aspose.com/).

**Q : Où puis‑je trouver plus d’exemples d’utilisation d’Aspose.PSD ?**  
R : Consultez la [documentation](https://reference.aspose.com/psd/java/) pour des exemples plus approfondis et des tutoriels.

**Q : Comment acheter une licence pour Aspose.PSD ?**  
R : Vous pouvez acheter une licence en visitant la [page d’achat Aspose](https://purchase.aspose.com/buy).

---

**Dernière mise à jour :** 2026-02-20  
**Testé avec :** Aspose.PSD pour Java 24.12 (dernière version au moment de la rédaction)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}