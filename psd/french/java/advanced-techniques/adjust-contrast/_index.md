---
date: 2025-12-21
description: Apprenez à ajuster le contraste des images avec Aspose.PSD pour Java,
  une bibliothèque de manipulation d’images Java de premier plan, et convertissez
  les PSD en TIFF efficacement.
linktitle: Adjust Contrast of an Image
second_title: Aspose.PSD Java API
title: Comment ajuster le contraste d’une image avec Aspose.PSD pour Java
url: /fr/java/advanced-techniques/adjust-contrast/
weight: 22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment ajuster le contraste d'une image avec Aspose.PSD pour Java

## Introduction

Si vous cherchez **comment ajuster le contraste** dans vos projets Java, vous êtes au bon endroit. Aspose.PSD pour Java est une puissante **bibliothèque de manipulation d'images java** qui vous permet d'ajuster finement les propriétés d'une image telles que le contraste, la luminosité, et plus encore. Dans ce tutoriel, nous parcourrons les étapes exactes pour augmenter le contraste d'un fichier PSD puis **convertir le PSD en TIFF** pour les flux de travail en aval.

## Quick Answers
- **Que signifie « ajuster le contraste » ?** Cela modifie la différence entre les pixels les plus sombres et les plus clairs, faisant ressortir les détails.
- **Quelle bibliothèque gère cela ?** Aspose.PSD pour Java – une boîte à outils de traitement d'images complète.
- **Ai‑je besoin d'une licence ?** Une licence temporaire suffit pour les tests ; une licence complète est requise pour la production.
- **Puis‑je enregistrer le résultat en TIFF ?** Oui, nous utiliserons `TiffOptions` pour exporter l'image traitée.
- **Combien de temps le code met‑il à s'exécuter ?** Généralement moins d'une seconde pour des fichiers PSD de taille standard.

## Qu'est‑ce que le réglage du contraste ?

Le réglage du contraste modifie la gamme tonale d'une image, amplifiant la distinction entre les zones claires et sombres. Ceci est particulièrement utile lorsque les images semblent plates après numérisation ou lors de la préparation de graphiques pour l'impression.

## Pourquoi utiliser Aspose.PSD pour Java ?
- **Prise en charge riche des formats** – ouvrir, modifier et enregistrer PSD, TIFF, PNG, JPEG et bien d'autres.
- **Haute performance** – la mise en cache et les optimisations d'images raster réduisent la consommation de mémoire.
- **API simple** – des appels à une seule méthode comme `adjustContrast` rendent le code lisible.

## Prerequisites

Avant de commencer, assurez‑vous d'avoir :

- Des connaissances de base en programmation Java.
- La bibliothèque Aspose.PSD pour Java installée. Vous pouvez la télécharger [ici](https://releases.aspose.com/psd/java/).

## Import Packages

Add the required imports to your Java class:

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Étape 1 : Charger l'image

Nous chargeons le fichier PSD source (`sample.psd`) dans un objet `Image`, qui sert de point d'entrée pour tout traitement ultérieur.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

## Étape 2 : Convertir en RasterImage et mettre en cache les données

Le cast en `RasterImage` nous donne accès aux opérations au niveau des pixels. La mise en cache améliore les performances, surtout pour les gros fichiers.

```java
// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached and Cache RasterImage for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## Comment ajuster le contraste d'une image

```java
// Adjust the contrast
rasterImage.adjustContrast(50);
```

La méthode `adjustContrast` prend un entier représentant le pourcentage de variation. Dans cet exemple, nous augmentons le contraste de **50 %**.

## Convertir le PSD en TIFF avec Aspose.PSD

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);

// Save the resultant image to TIFF format
String destName = dataDir + "AdjustContrast_out.tiff";
rasterImage.save(destName, tiffOptions);
```

Ici nous configurons `TiffOptions` (bits par échantillon, interprétation photométrique) et écrivons l'image dont le contraste a été amélioré dans un fichier TIFF.

## Problèmes courants et solutions
- **Image non mise en cache :** Appelez toujours `cacheData()` pour les gros PSD afin d'éviter `OutOfMemoryError`.
- **Déviation de couleur inattendue :** Vérifiez que `setPhotometric` correspond à votre espace couleur cible (RGB vs. CMYK).
- **Fichier introuvable :** Assurez‑vous que `dataDir` pointe vers le bon dossier et que le nom du fichier est correctement orthographié.

## Questions fréquentes

### Q1 : Aspose.PSD est‑il compatible avec différents formats d'image ?
R1 : Oui, Aspose.PSD prend en charge divers formats d'image, offrant une flexibilité dans vos projets.

### Q2 : Comment obtenir une licence temporaire pour Aspose.PSD ?
R2 : Vous pouvez obtenir une licence temporaire [ici](https://purchase.aspose.com/temporary-license/).

### Q3 : Où puis‑je trouver la documentation d'Aspose.PSD ?
R3 : La documentation est disponible [ici](https://reference.aspose.com/psd/java/).

### Q4 : Quelles options de support sont disponibles pour Aspose.PSD ?
R4 : Pour le support, consultez le [forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Q5 : Puis‑je acheter Aspose.PSD ?
R5 : Oui, vous pouvez acheter Aspose.PSD [ici](https://purchase.aspose.com/buy).

## Conclusion

Vous savez maintenant **comment ajuster le contraste** d'une image PSD en utilisant Aspose.PSD pour Java et comment **convertir le PSD en TIFF** pour un traitement ultérieur. Ces étapes vous offrent un contrôle précis sur la qualité de l'image tout en gardant le code propre et maintenable. N'hésitez pas à expérimenter d'autres méthodes d'ajustement d'image telles que `adjustBrightness` ou `adjustGamma` pour répondre à vos besoins spécifiques.

---

**Last Updated:** 2025-12-21  
**Tested With:** Aspose.PSD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}