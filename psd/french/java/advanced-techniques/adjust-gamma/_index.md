---
date: 2026-02-27
description: Apprenez à ajuster le gamma dans le traitement d'images Java avec Aspose.PSD,
  à convertir les PSD en TIFF et à corriger les images délavées dans un tutoriel concis.
linktitle: Adjust Gamma of an Image
second_title: Aspose.PSD Java API
title: Comment ajuster le gamma dans le traitement d'images Java avec Aspose.PSD
url: /fr/java/advanced-techniques/adjust-gamma/
weight: 23
---

 translation.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment ajuster le gamma en traitement d'images Java avec Aspose.PSD

## Introduction

Si vous travaillez sur le **traitement d'images Java**, apprendre **comment ajuster le gamma** est une technique fondamentale pour améliorer la luminosité et le contraste sans perdre de détails. Dans ce tutoriel, nous allons vous montrer comment utiliser **Aspose.PSD for Java** pour appliquer une correction gamma à un fichier PSD, **convertir le PSD en TIFF**, et éviter une **image délavée**. Vous verrez pourquoi cette approche est rapide, fiable et parfaite pour les pipelines d'images côté serveur.

## Réponses rapides
- **Que fait la correction gamma ?** Elle remappe les valeurs de luminance pour rendre les zones sombres plus claires ou les zones claires plus sombres tout en préservant les détails globaux.  
- **Quelle bibliothèque gère le traitement ?** Aspose.PSD for Java fournit une méthode dédiée `adjustGamma` pour les images raster.  
- **Puis-je convertir le PSD en TIFF dans le même flux ?** Oui – après l'ajustement du gamma, vous pouvez enregistrer l'image directement en TIFF avec `TiffOptions`.  
- **Ai‑je besoin d’une licence pour le développement ?** Une version d'essai gratuite suffit pour les tests ; une licence commerciale est requise pour la production.  
- **Quelle version de Java est prise en charge ?** Aspose.PSD supporte Java 8 et versions ultérieures.

## Comment ajuster le gamma en traitement d'images Java
L'ajustement du gamma est une partie centrale de tout **tutoriel de traitement d'images Java** qui traite de la luminosité ou du contraste. Ci‑dessous, nous détaillons les étapes, expliquons l'importance de chaque ligne et vous montrons comment intégrer le processus dans votre base de code existante.

## Qu'est‑ce que la correction gamma en Java ?
La correction gamma modifie la relation non linéaire entre les valeurs de pixels encodées et la luminosité affichée. En ajustant la courbe gamma, vous pouvez **corriger les problèmes d'image délavée** ou améliorer les détails dans les ombres sans surexposer les hautes lumières.

## Pourquoi utiliser Aspose.PSD pour la correction gamma ?
Aspose.PSD agit comme une puissante **bibliothèque de traitement d'images Java** qui abstrait les complexités du format PSD. Elle gère les profils couleur, la mise en cache, et fournit un appel simple `adjustGamma`, ce qui la rend idéale pour les **corrections gamma Java** et les flux **convertir PSD en TIFF**.

## Prérequis

1. **Environnement de développement Java** – Java 8 ou version ultérieure installé.  
2. **Bibliothèque Aspose.PSD** – Téléchargez et ajoutez le JAR à votre projet. Voir la [documentation officielle](https://reference.aspose.com/psd/java/).  
3. **Image d'exemple** – Un fichier PSD que vous souhaitez traiter (par ex., `sample.psd`).  

## Importer les packages

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

## Étape 1 : Charger l'image

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

**Astuce :** Mettre en cache les données raster une fois réduit les fluctuations de mémoire lorsque vous appliquez plusieurs ajustements successifs.

## Étape 2 : Ajuster le gamma

```java
// Adjust the gamma
rasterImage.adjustGamma(2.2f, 2.2f, 2.2f);
```

Vous pouvez passer des valeurs différentes pour les canaux rouge, vert et bleu si vous avez besoin d'ajustements spécifiques à chaque canal.

## Étape 3 : Créer les TiffOptions

```java
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
int[] ushort = { 8, 8, 8 };
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

Définir un échantillon de 8 bits (`{8,8,8}`) maintient la taille du fichier TIFF raisonnable tout en préservant la fidélité des couleurs.

## Étape 4 : Enregistrer l'image résultante

```java
// Save the resultant image to TIFF format
String destName = dataDir + "AdjustGamma_out.tiff";
rasterImage.save(destName, tiffOptions);
```

Après l’enregistrement, vous pouvez transmettre le TIFF aux systèmes en aval tels que les services d’impression ou les API web.

## Cas d'utilisation courants

- **Pipelines graphiques automatisés** – Ajuster le gamma à la volée avant de générer des miniatures.  
- **Outils de conversion par lots** – Convertir de grandes archives PSD en TIFF tout en normalisant la luminosité.  
- **Services web** – Exposer un point de terminaison qui reçoit un PSD, applique la correction gamma, et renvoie un TIFF au client.

## Problèmes fréquents et solutions

| Problème | Pourquoi cela se produit | Comment résoudre |
|----------|--------------------------|-------------------|
| **L'image apparaît délavée** | Valeur gamma trop élevée (par ex., > 2,5) | Réduisez le facteur gamma à une valeur entre 1,8 et 2,2. |
| **`rasterImage.isCached()` renvoie false** | Image pas encore chargée en mémoire | Appelez `rasterImage.cacheData()` avant d’ajuster le gamma. |
| **La taille du fichier TIFF est importante** | Bits par échantillon définis à 16 bits | Utilisez un échantillon de 8 bits (`{8,8,8}`) comme indiqué dans l’exemple. |

## Foire aux questions

**Q : Puis‑je appliquer des valeurs gamma différentes à chaque canal couleur ?**  
R : Oui – la méthode `adjustGamma` accepte des valeurs flottantes séparées pour les canaux rouge, vert et bleu.

**Q : Est‑il possible de chaîner plusieurs ajustements d'image avant l'enregistrement ?**  
R : Absolument. Vous pouvez effectuer le redimensionnement, le recadrage ou les corrections couleur séquentiellement sur la même instance `RasterImage`.

**Q : Aspose.PSD prend‑il en charge les fichiers PSD multi‑pages ?**  
R : Oui, chaque calque peut être accédé et traité individuellement.

**Q : Vers quels formats puis‑je exporter en plus du TIFF ?**  
R : Aspose.PSD supporte PNG, JPEG, BMP et de nombreux autres formats via leurs classes d’options respectives.

**Q : Comment éviter une image délavée après la correction gamma ?**  
R : Commencez avec un gamma modéré (environ 2,0) et prévisualisez le résultat ; diminuez la valeur si l’image paraît trop claire.

## Conclusion

Félicitations ! Vous avez appris avec succès **comment ajuster le gamma** dans un **workflow de traitement d'images Java**, converti un PSD en TIFF, et évité les pièges courants tels qu’une **image délavée**. Ce modèle vous offre un contrôle fin de la luminosité et du contraste, ce qui le rend idéal pour les pipelines graphiques automatisés, les services web ou les utilitaires de bureau.

---

**Dernière mise à jour :** 2026-02-27  
**Testé avec :** Aspose.PSD 24.11 for Java  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}