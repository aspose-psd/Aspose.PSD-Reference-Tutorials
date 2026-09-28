---
date: 2026-09-28
description: Apprenez à exporter un PSD en PNG tout en définissant le mode couleur
  du PSD en gris 16 bits à l'aide d'Aspose.PSD pour Java. Guide étape par étape avec
  des exemples de code.
keywords:
- export psd as png
- how to convert psd to png
- 16-bit grayscale java
lastmod: 2026-09-28
linktitle: Exporter PSD en PNG – Gris 16 bits – Java
og_description: Exportez un PSD en PNG avec le gris 16 bits à l'aide d'Aspose.PSD
  pour Java. Suivez ce tutoriel étape par étape pour préserver 65 536 nuances de gris.
og_image_alt: Guide showing how to export PSD as PNG with 16-bit grayscale using Aspose.PSD
  Java
og_title: Exporter PSD en PNG avec le gris 16 bits en Java – Guide Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  headline: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  type: TechArticle
- description: Learn how to export PSD as PNG while setting PSD color mode to 16-bit
    grayscale using Aspose.PSD for Java. Step‑by‑step guide with code examples.
  name: How to export PSD as PNG with 16‑bit grayscale color mode in Java
  steps:
  - name: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
    text: '**Java Development Kit (JDK)** – Install the latest JDK from [Oracle''s
      site](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).'
  - name: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD for Java library** – Download the JAR from the [Aspose download
      page](https://releases.aspose.com/psd/java/).'
  - name: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
    text: '**An IDE** – IntelliJ IDEA, Eclipse, or Visual Studio Code works perfectly.'
  - name: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
    text: '**Basic Java knowledge** – You should be comfortable creating classes,
      handling exceptions, and working with file paths.'
  - name: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
    text: '**A sample PSD file** – Create one in Adobe Photoshop or grab a free sample
      online.'
  type: HowTo
- questions:
  - answer: It provides 65 536 shades of gray, delivering far more tonal detail than
      the standard 8‑bit (256 shades).
    question: What is 16‑bit grayscale color mode?
  - answer: Absolutely! Aspose.PSD supports RGB, CMYK, Lab, Indexed, and many other
      color modes.
    question: Can I use Aspose.PSD for non‑grayscale images?
  - answer: Yes, you can try a free trial version of Aspose.PSD. Just head to the
      [Aspose download page](https://releases.aspose.com/).
    question: Is there a trial version of Aspose.PSD?
  - answer: Check the official [documentation](https://reference.aspose.com/psd/java/)
      for in‑depth tutorials, API references, and sample projects.
    question: Where can I find more Aspose.PSD examples?
  - answer: You can buy a license by visiting the [Aspose purchase page](https://purchase.aspose.com/buy).
    question: How do I purchase a license for Aspose.PSD?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- convert psd
- Aspose.PSD
- Java image processing
title: Comment exporter un PSD en PNG avec le mode couleur gris 16 bits en Java
url: /fr/java/advanced-psd-layer-features-effects/support-16-bit-grayscale-color-mode-psd/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporter PSD en PNG avec le mode couleur gris 16 bits en Java

## Introduction
Exporter un PSD en PNG tout en conservant le mode couleur gris 16 bits vous offre la profondeur d’une photographie professionnelle et la compatibilité universelle du PNG. Dans ce guide, vous apprendrez à **définir le mode couleur du PSD en gris 16 bits** puis à **exporter le PSD en PNG** en utilisant Aspose.PSD pour Java. Le tutoriel couvre tout, des prérequis au dépannage, afin que vous puissiez intégrer ce flux de travail dans n’importe quel pipeline d’images basé sur Java.

## Réponses rapides
- **Que signifie « exporter PSD en PNG » ?** Charger un PSD, éventuellement changer son mode couleur, puis l’enregistrer en tant que fichier PNG.  
- **Quelle classe Aspose gère la conversion ?** `PsdImage` charge le PSD et `PngOptions` définit les paramètres de sortie PNG.  
- **Ai‑je besoin d’une licence pour la production ?** Oui – une version d’essai fonctionne pour les tests, mais une licence payante est requise pour un usage commercial.  
- **La profondeur de 16 bits peut‑elle être conservée dans le PNG ?** Absolument, en utilisant `PngColorType.GrayscaleWithAlpha`.  
- **Quels IDE sont pris en charge ?** Tout IDE Java – IntelliJ IDEA, Eclipse, VS Code ou NetBeans.

## Qu’est‑ce que l’exportation de PSD en PNG ?
Exporter PSD en PNG est le processus de conversion d’un document Adobe Photoshop (PSD) en un fichier Portable Network Graphics (PNG) tout en préservant les données de pixels et la profondeur de couleur de l’image. Cette conversion est couramment utilisée pour partager des ressources en niveaux de gris de haute qualité sur le web sans perdre de détails tonaux.

## Pourquoi exporter PSD en PNG avec le mode gris 16 bits ?
Exporter en PNG tout en conservant le mode gris 16 bits préserve 65 536 nuances de gris, offrant ainsi beaucoup plus de richesse tonale que les images 8 bits. Le support universel du PNG garantit que les fichiers peuvent être affichés dans les navigateurs, les applications mobiles et les éditeurs de bureau sans perte, tandis que la compression sans perte d’Aspose.PSD assure qu’aucun artefact n’est introduit.

## Prérequis
Avant de commencer, assurez‑vous d’avoir les éléments suivants prêts :

1. **Java Development Kit (JDK)** – Installez le dernier JDK depuis le site de [Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).  
2. **Bibliothèque Aspose.PSD pour Java** – Téléchargez le JAR depuis la [page de téléchargement Aspose](https://releases.aspose.com/psd/java/).  
3. **Un IDE** – IntelliJ IDEA, Eclipse ou Visual Studio Code fonctionnent parfaitement.  
4. **Connaissances de base en Java** – Vous devez être à l’aise avec la création de classes, la gestion des exceptions et la manipulation des chemins de fichiers.  
5. **Un fichier PSD d’exemple** – Créez‑en un dans Adobe Photoshop ou téléchargez un exemple gratuit en ligne.

## Comment exporter PSD en PNG étape par étape

## Comment définir le mode couleur du PSD en gris 16 bits ?
`PsdImage` est la classe Aspose.PSD qui charge et représente un fichier PSD en mémoire.  
`ColorMode` est une énumération qui définit le mode couleur d’une image PSD.  

Chargez le PSD avec `PsdImage`, modifiez son mode couleur à l’aide de la propriété `ColorMode`, puis enregistrez le fichier modifié. Cette opération s’effectue entièrement en mémoire, éliminant le besoin de fichiers intermédiaires et garantissant une conversion rapide et efficace.

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

Ces importations vous donnent accès aux fonctionnalités que vous utiliserez pour manipuler les fichiers PSD, définir le mode couleur et exporter le résultat en PNG.

## Comment définir les répertoires source et de sortie ?
`File` est une classe java.io qui représente un chemin de fichier ou de répertoire sur le système de fichiers.  

Vous devez indiquer au programme où lire le PSD d’origine et où écrire le PNG converti. L’utilisation de chemins absolus ou relatifs fonctionne, mais veillez à les garder cohérents entre les environnements afin d’éviter les erreurs de résolution de chemin.

```java
String sourceDir = "Your Source Directory"; // Change to your source directory
String outputDir = "Your Document Directory"; // Change to your output directory
```

Remplacez les chaînes de caractères factices par les chemins réels sur votre machine.

## Comment encapsuler la logique de conversion dans une méthode réutilisable ?
`convertPsdToPng` est une méthode personnalisée qui encapsule toutes les étapes nécessaires pour convertir un fichier PSD en PNG avec des paramètres optionnels.  

Créer une méthode dédiée vous permet de réutiliser les mêmes étapes de conversion pour plusieurs fichiers ou différents réglages. Passez des paramètres tels que le chemin source, le dossier de destination et le niveau de compression optionnel, rendant le flux de travail flexible et maintenable.

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

## Comment charger le PSD et appliquer le mode gris 16 bits ?
`PsdImage` est la classe Aspose.PSD qui charge un fichier PSD en mémoire.  
`ColorMode.GRAYSCALE_16` est une valeur d’énumération qui définit l’image en gris 16 bits.  
`channelBitsCount` est une propriété qui spécifie le nombre de bits par canal.  

Dans la méthode de conversion, construisez les chemins de fichiers complets, instanciez `PsdImage` et changez son `ColorMode` en `ColorMode.GRAYSCALE_16`. La propriété `channelBitsCount` doit être définie à 16 pour conserver la haute profondeur de bits, garantissant que l’image conserve toutes les informations tonales.

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

## Comment dessiner une bordure subtile sur l’image (étape facultative) ?
`Graphics` est une classe qui fournit des capacités de dessin sur une toile `PsdImage`.  

Vous pouvez éventuellement dessiner un rectangle gris autour de l’image pour rendre la sortie plus visible lors des tests. Cette étape montre comment travailler avec les calques et les objets graphiques, et le rectangle est calculé dynamiquement afin de rester centré quel que soit la taille de l’image.

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

## Comment enregistrer le PSD modifié avec le nouveau mode couleur ?
`PsdOptions` est une classe qui contrôle la façon dont un fichier PSD est enregistré, y compris les paramètres de mode couleur et de profondeur de bits.  

Après le dessin (ou en le sautant), appelez `save` sur l’instance `PsdImage`, en passant un objet `PsdOptions` qui préserve la configuration gris 16 bits. Cela garantit que le PSD enregistré conserve le mode couleur souhaité sans perte de données.

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

## Comment convertir le PSD en PNG tout en conservant la profondeur de 16 bits ?
`PngOptions` est une classe qui définit les paramètres de sortie PNG tels que le type de couleur et le niveau de compression.  
`PngColorType.GrayscaleWithAlpha` est une valeur d’énumération qui stocke les données gris 16 bits avec un canal alpha.  

Chargez le PSD récemment enregistré, configurez `PngOptions` avec `PngColorType.GrayscaleWithAlpha`, puis appelez `save`. Cela conserve les données gris 16 bits dans le fichier PNG, offrant une image sans perte et de haute qualité adaptée à un traitement ou une distribution ultérieurs.

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

Vous avez maintenant réussi à **exporter PSD en PNG** tout en conservant les données gris 16 bits de haute qualité.

## Problèmes courants et solutions
| Problème | Pourquoi cela se produit | Solution |
|----------|--------------------------|----------|
| **Exception « Unsupported color type »** | Tentative d’enregistrement d’un PSD avec une configuration de canal non prise en charge. | Assurez‑vous que `channelBitsCount` correspond à la profondeur réelle (16) et que `channelsCount` est correct pour le gris (1). |
| **Fichier introuvable** | Chemin du répertoire source incorrect. | Vérifiez la chaîne `sourceDir` et confirmez que le fichier PSD existe à cet emplacement. |
| **Le PNG de sortie apparaît noir** | PNG enregistré sans gestion correcte de l’alpha. | Utilisez `PngColorType.GrayscaleWithAlpha` comme indiqué ci‑dessus. |
| **Débordement de mémoire sur de gros PSD** | Chargement du fichier complet en mémoire. | Activez le mode streaming via `PsdImage.load(inputStream, new LoadOptions())` pour traiter les gros fichiers efficacement. |

## Questions fréquemment posées

**Q : Qu’est‑ce que le mode couleur gris 16 bits ?**  
R : Il offre 65 536 nuances de gris, fournissant beaucoup plus de détail tonal que le mode standard 8 bits (256 nuances).

**Q : Puis‑je utiliser Aspose.PSD pour des images non‑gris ?**  
R : Absolument ! Aspose.PSD prend en charge RGB, CMYK, Lab, Indexed et de nombreux autres modes couleur.

**Q : Existe‑t‑il une version d’essai d’Aspose.PSD ?**  
R : Oui, vous pouvez essayer une version d’essai gratuite d’Aspose.PSD. Rendez‑vous simplement sur la [page de téléchargement Aspose](https://releases.aspose.com/).

**Q : Où puis‑je trouver plus d’exemples Aspose.PSD ?**  
R : Consultez la [documentation officielle](https://reference.aspose.com/psd/java/) pour des tutoriels approfondis, des références API et des projets d’exemple.

**Q : Comment acheter une licence pour Aspose.PSD ?**  
R : Vous pouvez acheter une licence en visitant la [page d’achat Aspose](https://purchase.aspose.com/buy).

---

**Dernière mise à jour :** 2026-09-28  
**Testé avec :** Aspose.PSD pour Java 24.12 (dernière version au moment de la rédaction)  
**Auteur :** Aspose

## Tutoriels associés

- [Convert PSD to PNG with Specified Bit Depth Using Aspose.PSD for Java](/psd/java/optimizing-png-files/specify-png-bit-depth/)
- [Export PSD to PNG with Layer Effects using Aspose.PSD for Java](/psd/java/psd-image-modification-conversion/apply-layer-effects-psd-files/)
- [Save PSD as JPEG and Support RGB Color with Aspose.PSD Java](/psd/java/advanced-psd-layer-features-effects/support-rgb-color-psd-files/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}