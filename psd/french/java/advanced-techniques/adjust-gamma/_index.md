---
date: 2025-12-21
description: Apprenez à effectuer le traitement d'images Java en ajustant le gamma
  de l'image avec Aspose.PSD. Guide étape par étape pour convertir un PSD en TIFF
  et appliquer la correction gamma.
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: Traitement d'images Java – Ajuster le gamma avec Aspose.PSD
url: /fr/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Traitement d'images Java – Ajuster le gamma avec Aspose.PSD

## Introduction

Si vous travaillez sur le **traitement d'images Java**, ajuster le gamma d’une image est une technique fondamentale pour améliorer la luminosité et le contraste sans perdre de détails. Dans ce tutoriel, nous allons voir comment utiliser **Aspose.PSD for Java** pour appliquer une correction gamma à un fichier PSD puis exporter le résultat au format TIFF. Vous verrez pourquoi cette approche est rapide, fiable et parfaite pour les pipelines d’images côté serveur.

## Réponses rapides
- **Que fait la correction gamma ?** Elle remappe les valeurs de luminance pour rendre les zones sombres plus claires ou les zones claires plus sombres tout en préservant les détails globaux.  
- **Quelle bibliothèque gère le traitement ?** Aspose.PSD for Java fournit une méthode dédiée `adjustGamma` pour les images raster.  
- **Puis‑je convertir le PSD en TIFF dans le même flux ?** Oui – après l’ajustement du gamma, vous pouvez enregistrer l’image directement en TIFF avec `TiffOptions`.  
- **Ai‑je besoin d’une licence pour le développement ?** Une version d’essai gratuite suffit pour les tests ; une licence commerciale est requise pour la production.  
- **Quelle version de Java est prise en charge ?** Aspose.PSD prend en charge Java 8 et les versions ultérieures.

## Qu’est‑ce que le traitement d’images Java ?

Le traitement d’images Java désigne la manipulation, l’analyse et la transformation de données visuelles à l’aide de bibliothèques Java. Les tâches incluent le redimensionnement, le filtrage, la correction des couleurs et la conversion de formats — le tout pouvant être automatisé dans des applications de bureau ou web.

## Pourquoi utiliser Aspose.PSD pour la correction gamma ?

Aspose.PSD propose une API de haut niveau qui masque la complexité du format PSD, vous permettant de vous concentrer sur les ajustements d’image réels. Elle gère le cache, les profils colorimétriques et offre un appel simple `adjustGamma`, ce qui la rend idéale pour les **corrections gamma d’image** et les flux **convertir psd en tiff**.

## Prérequis

Avant de commencer le tutoriel, assurez‑vous d’avoir les prérequis suivants :

1. **Environnement de développement Java** – Vérifiez que vous avez un environnement de développement Java installé sur votre système.  
2. **Bibliothèque Aspose.PSD** – Téléchargez et intégrez la bibliothèque Aspose.PSD dans votre projet Java. Vous trouverez les ressources nécessaires dans la [documentation](https://reference.aspose.com/psd/java/).  
3. **Image d’exemple** – Préparez une image PSD d’exemple que vous utiliserez pour appliquer l’ajustement gamma.

## Importer les packages

Pour lancer le processus, importez les packages requis dans votre projet Java. Cela prépare le terrain pour utiliser les fonctionnalités d’Aspose.PSD de manière fluide.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Étape 1 : Charger l’image

Commencez par charger l’image PSD d’exemple dans une instance de la classe `RasterImage`. C’est la base pour les ajustements gamma ultérieurs.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);

// Cast object of Image to RasterImage
RasterImage rasterImage = (RasterImage)image;

// Check if RasterImage is cached for better performance
if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

## Étape 2 : Ajuster le gamma

Maintenant, ajustez le gamma de l’image chargée à l’aide de la méthode `adjustGamma`. Affinez les valeurs de gamma selon vos besoins.

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

## Étape 3 : Créer les TiffOptions

Créez une instance de `TiffOptions` pour l’image résultante. Définissez diverses propriétés, telles que les bits par échantillon et les options photométriques, afin d’adapter la sortie à vos spécifications.

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

## Étape 4 : Enregistrer l’image résultante

Enregistrez l’image manipulée au format TIFF en utilisant les `TiffOptions` définies précédemment.

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

## Problèmes courants et solutions

| Problème | Pourquoi cela se produit | Comment résoudre |
|----------|--------------------------|------------------|
| **L’image apparaît délavée** | Valeur gamma trop élevée (par ex. > 2,5) | Réduisez le facteur gamma à une valeur entre 1,8 et 2,2. |
| **`rasterImage.isCached()` renvoie false** | L’image n’est pas encore chargée en mémoire | Appelez `rasterImage.cacheData()` avant d’ajuster le gamma. |
| **La taille du fichier TIFF est importante** | Bits par échantillon définis à 16 bits | Utilisez un échantillon 8 bits (`{8,8,8}`) comme indiqué dans l’exemple. |

## Questions fréquentes

**Q : Puis‑je appliquer des valeurs gamma différentes à chaque canal couleur ?**  
R : Oui – la méthode `adjustGamma` accepte des valeurs flottantes séparées pour les canaux rouge, vert et bleu.

**Q : Est‑il possible de chaîner plusieurs ajustements d’image avant l’enregistrement ?**  
R : Absolument. Vous pouvez effectuer le redimensionnement, le recadrage ou les corrections de couleur séquentiellement sur la même instance `RasterImage`.

**Q : Aspose.PSD prend‑il en charge les fichiers PSD multipages ?**  
R : Oui, chaque calque peut être accédé et traité individuellement.

**Q : Vers quels formats puis‑je exporter en plus du TIFF ?**  
R : Aspose.PSD prend en charge PNG, JPEG, BMP et de nombreux autres formats via leurs classes d’options respectives.

## Conclusion

Félicitations ! Vous avez réussi à effectuer du **traitement d’images Java** en ajustant le gamma d’un fichier PSD et en l’exportant au format TIFF à l’aide d’Aspose.PSD for Java. Ce flux de travail vous offre un contrôle granulaire sur la luminosité et le contraste de l’image, ce qui le rend idéal pour les pipelines graphiques automatisés, les services web ou les utilitaires de bureau.

---

**Dernière mise à jour :** 2025-12-21  
**Testé avec :** Aspose.PSD 24.11 for Java  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
