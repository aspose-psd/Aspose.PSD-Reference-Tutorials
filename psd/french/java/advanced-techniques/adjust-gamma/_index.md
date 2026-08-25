---
date: 2026-08-01
description: Apprenez comment ajuster le gamma dans le traitement d'images Java avec
  Aspose.PSD, convertir les PSD en TIFF et corriger les images délavées dans un tutoriel
  concis.
keywords:
- how to adjust gamma
- fix washed out image
- java image processing
- convert psd to tiff
- server side image processing
lastmod: 2026-08-01
linktitle: Ajuster le gamma d'une image
og_description: Apprenez comment ajuster le gamma dans le traitement d'images Java
  avec Aspose.PSD – une bibliothèque rapide côté serveur qui corrige les images délavées
  et convertit les PSD en TIFF en quelques lignes de code.
og_image_alt: 'Guide: Adjust gamma in Java images with Aspose.PSD, convert PSD to
  TIFF'
og_title: comment ajuster le gamma – traitement Java avec Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-08-01'
  description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  headline: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  type: TechArticle
- description: Learn how to adjust gamma in Java image processing with Aspose.PSD,
    convert PSD to TIFF, and fix washed‑out images in a concise tutorial.
  name: How to Adjust Gamma in Java Image Processing with Aspose.PSD
  steps:
  - name: '**Java Development Environment** – Java 8 or later installed.'
    text: '**Java Development Environment** – Java 8 or later installed.'
  - name: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download and add the JAR to your project. See
      the official [documentation](https://reference.aspose.com/psd/java/).'
  - name: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
    text: '**Sample Image** – A PSD file you want to process (e.g., `sample.psd`).'
  type: HowTo
- questions:
  - answer: Yes – the `adjustGamma` method accepts separate float values for red,
      green, and blue channels.
    question: Can I apply different gamma values to each colour channel?
  - answer: Absolutely. You can perform resizing, cropping, or colour corrections
      sequentially on the same `RasterImage` instance.
    question: Is it possible to chain multiple image adjustments before saving?
  - answer: Yes, each layer can be accessed and processed individually.
    question: Does Aspose.PSD support multi‑page PSD files?
  - answer: Aspose.PSD supports PNG, JPEG, BMP, and many other formats via their respective
      options classes.
    question: What format can I export to besides TIFF?
  - answer: Start with a moderate gamma (around 2.0) and preview the result; adjust
      downwards if the image looks too bright.
    question: How do I avoid a washed‑out image after gamma correction?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- adjust gamma
- Aspose.PSD
- Java image processing
- PSD to TIFF
- server side processing
title: Comment ajuster le gamma dans le traitement d'images Java avec Aspose.PSD
url: /fr/java/advanced-techniques/adjust-gamma/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment ajuster le gamma dans le traitement d'images Java avec Aspose.PSD

## Introduction

Si vous travaillez sur le **traitement d'images Java**, apprendre **comment ajuster le gamma** est une technique fondamentale pour améliorer la luminosité et le contraste sans perdre de détails. Dans ce tutoriel, nous allons vous montrer comment utiliser **Aspose.PSD for Java** pour appliquer une correction gamma à un fichier PSD, **convertir le PSD en TIFF**, et éviter une **image délavée**. Vous verrez pourquoi cette approche est rapide, fiable et parfaite pour les pipelines de **traitement d'images côté serveur**.

## Réponses rapides
- **À quoi sert la correction gamma ?** Elle remappe les valeurs de luminance pour rendre les zones sombres plus claires ou les zones claires plus sombres tout en préservant les détails globaux.  
- **Quelle bibliothèque gère le traitement ?** Aspose.PSD for Java fournit une méthode dédiée `adjustGamma` pour les images raster.  
- **Puis-je convertir le PSD en TIFF dans le même flux ?** Oui – après l'ajustement du gamma, vous pouvez enregistrer l'image directement en TIFF en utilisant `TiffOptions`.  
- **Ai-je besoin d'une licence pour le développement ?** Un essai gratuit suffit pour les tests ; une licence commerciale est requise pour une utilisation en production.  
- **Quelle version de Java est prise en charge ?** Aspose.PSD prend en charge Java 8 et les versions ultérieures.

## Qu'est-ce que la correction gamma en Java ?

La correction gamma modifie la relation non linéaire entre les valeurs de pixels codées et la luminosité affichée. En ajustant la courbe gamma, vous pouvez **corriger les problèmes d'image délavée** ou améliorer les détails dans les ombres sans surexposer les hautes lumières. Elle fonctionne en appliquant une fonction de loi de puissance à chaque pixel, ce qui éclaircit les tons sombres et compresse les hautes lumières, donnant ainsi une apparence visuelle plus naturelle.

## Pourquoi utiliser Aspose.PSD pour la correction gamma ?

Aspose.PSD est une **bibliothèque de traitement d'images Java** qui masque les complexités du format PSD. Elle prend en charge le traitement de fichiers jusqu'à 2 Go, gère plus de 50 formats d'image différents, et offre un appel simple `adjustGamma`, ce qui la rend idéale pour les flux de travail de **correction gamma Java** et de **conversion PSD en TIFF**.

## Prérequis

1. **Environnement de développement Java** – Java 8 ou version ultérieure installé.  
2. **Bibliothèque Aspose.PSD** – Téléchargez et ajoutez le JAR à votre projet. Voir la [documentation](https://reference.aspose.com/psd/java/) officielle.  
3. **Image d'exemple** – Un fichier PSD que vous souhaitez traiter (par ex., `sample.psd`).  

## Importer les packages

Avant de commencer, importez les espaces de noms essentiels qui vous donnent accès à la gestion raster et aux options de format de fichier.

## Étape 1 : Charger l'image

La classe `RasterImage` représente les données de pixels rasterisées d'un calque PSD en mémoire. Charger l'image une fois et la mettre en cache réduit la consommation de mémoire pour les ajustements ultérieurs.

## Étape 2 : Ajuster le gamma

Chargez votre PSD avec `new RasterImage("sample.psd")` et appelez `rasterImage.adjustGamma(2.0f)` — cette ligne unique applique un gamma de 2,0 à tous les canaux de couleur, éclaircissant les ombres tout en conservant les hautes lumières intactes. Vous pouvez fournir des valeurs séparées pour le rouge, le vert et le bleu si des ajustements spécifiques aux canaux sont nécessaires.

## Étape 3 : Créer TiffOptions

`TiffOptions` vous permet de contrôler la compression, les bits par échantillon et d'autres paramètres spécifiques au TIFF. Définir un échantillon de 8 bits (`{8,8,8}`) maintient la taille du fichier TIFF raisonnable tout en préservant la fidélité des couleurs.

## Étape 4 : Enregistrer l'image résultante

Appelez `rasterImage.save("output.tif", tiffOptions)` pour écrire l'image traitée sur le disque. Après l'enregistrement, vous pouvez transmettre le TIFF aux systèmes en aval tels que les services d'impression ou les API web.

## Cas d'utilisation courants

- **Pipelines graphiques automatisés** – Ajuster le gamma à la volée avant de générer des miniatures.  
- **Outils de conversion par lots** – Convertir de grandes archives PSD en TIFF tout en normalisant la luminosité.  
- **Services web** – Exposer un point de terminaison qui reçoit un PSD, applique la correction gamma et renvoie un TIFF pour la consommation du client.

## Problèmes courants et solutions

| Problème | Pourquoi cela se produit | Comment corriger |
|----------|--------------------------|------------------|
| **L'image apparaît délavée** | Valeur gamma trop élevée (p. ex., > 2,5) | Réduisez le facteur gamma à une valeur entre 1,8 et 2,2. |
| **`rasterImage.isCached()` renvoie false** | L'image n'est pas encore chargée en mémoire | Appelez `rasterImage.cacheData()` avant d'ajuster le gamma. |
| **La taille du fichier TIFF est grande** | Bits par échantillon définis à 16 bits | Utilisez un échantillon de 8 bits (`{8,8,8}`) comme indiqué dans l'exemple. |

## Questions fréquemment posées

**Q: Puis-je appliquer des valeurs gamma différentes à chaque canal de couleur ?**  
A: Oui – la méthode `adjustGamma` accepte des valeurs float séparées pour les canaux rouge, vert et bleu.

**Q: Est-il possible d'enchaîner plusieurs ajustements d'image avant l'enregistrement ?**  
A: Absolument. Vous pouvez effectuer le redimensionnement, le recadrage ou les corrections de couleur séquentiellement sur la même instance `RasterImage`.

**Q: Aspose.PSD prend‑il en charge les fichiers PSD multi‑pages ?**  
A: Oui, chaque calque peut être accédé et traité individuellement.

**Q: Vers quel format puis‑je exporter en plus du TIFF ?**  
A: Aspose.PSD prend en charge PNG, JPEG, BMP et de nombreux autres formats via leurs classes d'options respectives.

**Q: Comment éviter une image délavée après la correction gamma ?**  
A: Commencez avec un gamma modéré (environ 2,0) et prévisualisez le résultat ; réduisez-le si l'image apparaît trop claire.

## Conclusion

Félicitations ! Vous avez appris avec succès **comment ajuster le gamma** dans un flux de **traitement d'images Java**, converti un PSD en TIFF et évité les pièges courants tels qu'une **image délavée**. Ce modèle vous offre un contrôle fin de la luminosité et du contraste, ce qui le rend idéal pour les pipelines graphiques automatisés, les services web ou les utilitaires de bureau.

---

**Dernière mise à jour:** 2026-08-01  
**Testé avec:** Aspose.PSD 24.11 for Java  
**Auteur:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriels associés

- [Tutoriel de traitement d'images Java - Ajuster la luminosité d'une image avec Aspose.PSD for Java](/psd/java/advanced-techniques/adjust-brightness/)
- [Comment convertir le PSD en TIFF et ajuster le contraste avec Aspose.PSD for Java](/psd/java/advanced-techniques/adjust-contrast/)
- [Convertir le PSD en image en Java – Appliquer des calques d'ajustement avec Aspose.PSD](/psd/java/advanced-psd-layer-features-effects/apply-adjustment-layers-psd-files/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

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

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```