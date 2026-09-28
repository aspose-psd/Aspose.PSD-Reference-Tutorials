---
date: 2026-09-28
description: Le tutoriel de traitement d'images Java montre comment ajuster la luminosité
  d'une image en utilisant Aspose.PSD pour Java. Suivez le code étape par étape pour
  charger, modifier et enregistrer des fichiers PSD ou TIFF.
keywords:
- java image processing
- aspose psd java
- java image manipulation
- adjust brightness java
lastmod: 2026-09-28
linktitle: Ajuster la luminosité d'une image
og_description: Le tutoriel de traitement d'images Java montre comment ajuster la
  luminosité d'une image en utilisant Aspose.PSD pour Java. Suivez le code étape par
  étape pour charger, modifier et enregistrer des fichiers PSD ou TIFF.
og_image_alt: Guide to adjusting image brightness in Java using Aspose.PSD
og_title: 'Traitement d''images Java : ajuster la luminosité avec Aspose.PSD'
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  headline: 'Java image processing: adjust brightness with Aspose.PSD'
  type: TechArticle
- description: Java image processing tutorial shows how to adjust brightness of an
    image using Aspose.PSD for Java. Follow step‑by‑step code to load, modify, and
    save PSD or TIFF files.
  name: 'Java image processing: adjust brightness with Aspose.PSD'
  steps:
  - name: Load the image
    text: The `RasterImage` class represents a rasterized version of a PSD or TIFF
      file in memory. It provides direct pixel access for color‑correction operations.
      In this step, we load the target image and cast it to a `RasterImage` for further
      processing.
  - name: Adjust brightness
    text: '`adjustBrightness(int value)` changes the lightness of every pixel by the
      specified integer value. Positive numbers brighten the image; negative numbers
      darken it. The method processes the image in‑place, so no additional object
      creation is required. Here, we use the `adjustBrightness` method to mod'
  - name: Set TiffOptions
    text: '`TiffOptions` specifies the encoding parameters for TIFF output, such as
      bits per sample and photometric interpretation. It lets you control how the
      resulting file is encoded. Configure the `TiffOptions` for saving the adjusted
      image. Adjust the `bitsPerSample` and `photometric` properties based on '
  - name: Save the resultant image
    text: Calling `save` writes the processed raster data to a file using the previously
      defined options. The operation is atomic and guarantees that the output file
      is a valid TIFF image. Finally, save the modified image using the specified
      `TiffOptions`.
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD for Java supports JPEG, PNG, BMP, GIF, and many other
      raster formats in addition to PSD and TIFF.
    question: Can I adjust brightness in other image formats besides PSD?
  - answer: Wrap the processing code in a try‑catch block and catch `IOException`
      or `ImageProcessingException` to manage file‑access and raster‑operation errors.
    question: How can I handle errors during the image adjustment process?
  - answer: The method accepts integer values from –255 to +255; values outside this
      range are clamped to the nearest limit.
    question: Is there a limit to the range of brightness adjustment?
  - answer: Yes, a commercial license is required for production use. Purchase a license
      [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.PSD for Java in commercial projects?
  - answer: Yes, you can explore the library with a free trial from [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image processing
- aspose psd
- java image manipulation
title: 'Traitement d''images Java : ajuster la luminosité avec Aspose.PSD'
url: /fr/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ajuster la luminosité d'une image avec Aspose.PSD pour Java

## Introduction

Dans ce tutoriel **java image processing**, vous apprendrez comment ajuster la luminosité d'une image directement depuis du code Java. Modifier la luminosité est une tâche fréquente pour les graphistes, les photographes et toute personne construisant des pipelines de traitement d'images. Dans ce guide **java image manipulation**, nous parcourrons le flux complet — chargement d'un PSD/TIFF, application d'un décalage de luminosité et enregistrement du résultat — en utilisant la bibliothèque Aspose.PSD pour Java.

## Réponses rapides

- **Quelle bibliothèque gère la luminosité ?** Aspose.PSD for Java.  
- **Quelle méthode modifie la luminosité ?** `RasterImage.adjustBrightness()`.  
- **Puis-je travailler avec des fichiers PSD et TIFF ?** Oui, l'API prend en charge les deux formats ainsi que plus de 10 types d'images supplémentaires.  
- **Ai-je besoin d'une licence pour la production ?** Une licence commerciale est requise pour une utilisation non‑évaluation.  
- **Combien de temps prend l'implémentation ?** Typiquement moins de 10 minutes pour un ajustement de base.

## Qu'est‑ce que le java image processing ?

`Java image processing` désigne l'ensemble des techniques qui vous permettent de lire, transformer et écrire des données d'image de manière programmatique en utilisant Java. Ajuster la luminosité est l'une des opérations fondamentales qui modifie la clarté globale de chaque pixel, rendant les zones sombres plus claires ou les zones claires plus sombres.

## Pourquoi utiliser Aspose.PSD pour Java ?

Aspose.PSD pour Java offre une solution complète, pure‑Java, qui prend en charge un large éventail de formats raster et vectoriels, élimine les dépendances natives et propose une mise en cache haute performance pour les gros fichiers. Son API étendue permet aux développeurs d'effectuer des corrections de couleur complexes et des modifications basées sur les calques avec un code minimal, ce qui le rend idéal tant pour les ajustements simples que pour les pipelines de traitement d'images avancés.

- **Prend en charge plus de 10 formats raster et vectoriels** – PSD, TIFF, JPEG, PNG, BMP, GIF, et plus.  
- **Implémentation pure‑Java** – aucune DLL native ni dépendance externe, ce qui fonctionne sur n'importe quelle JVM.  
- **Mise en cache haute performance** – les données raster peuvent être mises en cache, permettant des éditions répétées jusqu'à 2× plus rapides sur de gros fichiers.  
- **Large surface d'API** – plus de 150 méthodes pour la correction des couleurs, la gestion des calques, les masques et le compositing.

## Prérequis

Avant de plonger dans le tutoriel, assurez‑vous de disposer des prérequis suivants :

- Bibliothèque Aspose.PSD pour Java : téléchargez et installez la bibliothèque depuis la [documentation Aspose.PSD pour Java](https://reference.aspose.com/psd/java/).  
- Kit de développement Java (JDK) 8 ou supérieur installé sur votre machine.  
- Un environnement de développement (IDE) tel qu'IntelliJ IDEA, Eclipse ou VS Code.

## Importer les packages

Pour commencer, importez les packages nécessaires dans votre projet Java. Dans cet exemple, nous utiliserons les suivants :

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Maintenant, décomposons le processus d'ajustement de la luminosité d'une image en étapes simples :

## Comment ajuster la luminosité avec Aspose.PSD ?

Chargez votre image source, appliquez un décalage de luminosité, configurez les options d'enregistrement et écrivez le résultat sur le disque—le tout en quatre étapes concises. Les sections suivantes offrent un guide clair, étape par étape, que vous pouvez copier dans votre propre projet. Cette approche garantit que chaque opération est effectuée efficacement et que l'image finale conserve la qualité originale tout en reflétant le changement de luminosité souhaité.

### Étape 1 : Charger l'image

La classe `RasterImage` représente une version rasterisée d'un fichier PSD ou TIFF en mémoire. Elle fournit un accès direct aux pixels pour les opérations de correction des couleurs.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "AdjustBrightness_out.tiff";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage) image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

Dans cette étape, nous chargeons l'image cible et la convertissons en `RasterImage` pour un traitement ultérieur.

### Étape 2 : Ajuster la luminosité

`adjustBrightness(int value)` modifie la clarté de chaque pixel selon la valeur entière spécifiée. Les nombres positifs éclaircissent l'image ; les nombres négatifs l'assombrissent. La méthode traite l'image en place, aucune création d'objet supplémentaire n'est requise.

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

Ici, nous utilisons la méthode `adjustBrightness` pour modifier la luminosité de l'image. Dans cet exemple, nous diminuons la luminosité de 50 unités, mais vous pouvez personnaliser cette valeur selon vos besoins.

### Étape 3 : Définir TiffOptions

`TiffOptions` spécifie les paramètres d'encodage pour la sortie TIFF, tels que les bits par échantillon et l'interprétation photométrique. Il vous permet de contrôler la façon dont le fichier résultant est encodé.

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

Configurez les `TiffOptions` pour enregistrer l'image ajustée. Ajustez les propriétés `bitsPerSample` et `photometric` selon vos besoins spécifiques.

### Étape 4 : Enregistrer l'image résultante

Appeler `save` écrit les données raster traitées dans un fichier en utilisant les options définies précédemment. L'opération est atomique et garantit que le fichier de sortie est une image TIFF valide.

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

Enfin, enregistrez l'image modifiée en utilisant les `TiffOptions` spécifiés.

## Problèmes courants et solutions

| Issue | Reason | Solution |
|-------|--------|----------|
| **`ClassCastException` lors du cast d'Image** | Le fichier n'est pas une image raster (par ex., un PSD vectoriel). | Vérifiez le format du fichier source ou utilisez `image instanceof RasterImage` avant le cast. |
| **Le changement de luminosité n'a aucun effet** | L'image n'a pas été mise en cache avant l'ajustement. | Appelez `rasterImage.cacheData()` comme indiqué à l'étape 1. |
| **Le fichier enregistré apparaît corrompu** | Configuration incorrecte de `TiffOptions`. | Assurez‑vous que `bitsPerSample` correspond à la profondeur de l'image source (généralement 8 bits par canal). |

## Questions fréquemment posées

**Q : Puis‑je ajuster la luminosité dans d'autres formats d'image que le PSD ?**  
R : Oui, Aspose.PSD pour Java prend en charge JPEG, PNG, BMP, GIF et de nombreux autres formats raster en plus du PSD et du TIFF.

**Q : Comment gérer les erreurs pendant le processus d'ajustement de l'image ?**  
R : Enveloppez le code de traitement dans un bloc try‑catch et capturez `IOException` ou `ImageProcessingException` pour gérer les erreurs d'accès aux fichiers et d'opérations raster.

**Q : Existe‑t‑il une limite à la plage d'ajustement de la luminosité ?**  
R : La méthode accepte des valeurs entières de –255 à +255 ; les valeurs hors de cette plage sont limitées au bord le plus proche.

**Q : Puis‑je utiliser Aspose.PSD pour Java dans des projets commerciaux ?**  
R : Oui, une licence commerciale est requise pour une utilisation en production. Achetez une licence [ici](https://purchase.aspose.com/buy).

**Q : Une version d'essai gratuite est‑elle disponible ?**  
R : Oui, vous pouvez explorer la bibliothèque avec une version d'essai gratuite depuis [ici](https://releases.aspose.com/).

**Q : La méthode `adjustBrightness` affecte‑t‑elle la visibilité des calques ?**  
R : La méthode agit sur l'image composite rasterisée, ainsi les calques masqués sont ignorés lors de la rasterisation, préservant le résultat visuel souhaité.

**Q : Puis‑je chaîner plusieurs ajustements (par ex., contraste, saturation) ?**  
R : Absolument. Après avoir ajusté la luminosité, vous pouvez appeler `adjustContrast`, `adjustSaturation` ou d'autres méthodes de correction des couleurs sur la même instance de `RasterImage`.

---

**Dernière mise à jour :** 2026-09-28  
**Testé avec :** Aspose.PSD pour Java 24.12 (dernière version au moment de la rédaction)  
**Auteur :** Aspose

## Tutoriels associés

- [Bibliothèque de traitement d'image Java : Inverser le calque avec Aspose.PSD](/psd/java/advanced-image-manipulation/invert-adjustment-layer/)
- [Convertir l'image en niveaux de gris avec Aspose.PSD pour Java](/psd/java/advanced-techniques/grayscale-image/)
- [Comment faire pivoter une image à un angle spécifique avec Aspose.PSD pour Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}