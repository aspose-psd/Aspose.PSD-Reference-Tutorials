---
date: 2026-01-07
description: Apprenez pas à pas les techniques de filtrage pour appliquer les filtres
  médian et Wiener avec Aspose.PSD pour Java, et convertissez efficacement les PSD
  en GIF.
linktitle: Apply Median and Wiener Filters
second_title: Aspose.PSD Java API
title: 'Filtre étape par étape : appliquer les filtres médian et de Wiener (Java)'
url: /fr/java/image-processing/apply-median-wiener-filters/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Filtre étape par étape : appliquer les filtres médian et Wiener (Java)

## Introduction

Si vous recherchez un **step by step filter** pour nettoyer des images bruitées en Java, vous êtes au bon endroit. Aspose.PSD for Java simplifie l’application des filtres Median et Wiener, et vous permet même de **convertir PSD en GIF** après le traitement. Dans ce tutoriel, nous passerons en revue tout ce dont vous avez besoin — de l’installation de la bibliothèque à l’enregistrement du résultat filtré—afin que vous puissiez intégrer un débruitage d’image de haute qualité dans vos applications en toute confiance.

## Réponses rapides
- **Que fait le filtre médian ?** Il réduit le bruit sel‑et‑poivre tout en préservant les contours.  
- **Quand devrais‑je utiliser le filtre Wiener ?** Pour une réduction de bruit adaptative qui prend en compte la variance locale de l’image.  
- **Ai‑je besoin d’une licence pour exécuter le code ?** Un essai gratuit suffit pour le développement ; une licence commerciale est requise pour la production.  
- **Puis‑je enregistrer la sortie au format GIF ?** Oui—Aspose.PSD vous permet de **convertir PSD en GIF** en une seule étape.  
- **Combien de temps prend l’implémentation ?** Généralement moins de 10 minutes pour une configuration de base.

## Qu’est‑ce qu’un filtre étape par étape ?

Une approche *step by step filter* découpe le traitement d’image en étapes claires et gérables — chargement de l’image, configuration des options du filtre, application du filtre, puis enregistrement du résultat. Ce flux méthodique vous aide à déboguer chaque partie, à réutiliser le code et à adapter le processus à différents formats d’image.

## Pourquoi utiliser Aspose.PSD pour Java ?

- **Large prise en charge des formats** – Gère PSD, PNG, JPEG, GIF, etc.  
- **Aucune dépendance externe** – Java pur, facile à intégrer dans n’importe quel projet.  
- **Options de filtres intégrées** – Median, Wiener et d’autres filtres avancés sont prêts à l’emploi.  
- **Conversion en un clic** – Exportation directe vers GIF, PNG ou JPEG après traitement.

## Prérequis

1. **Aspose.PSD for Java Library** – Téléchargez et installez la bibliothèque depuis [here](https://releases.aspose.com/psd/java/).  
2. **Environnement de développement Java** – JDK 8+ et un IDE ou un outil de construction (Maven/Gradle) configurés sur votre machine.

## Importer les packages

Commencez par importer les classes nécessaires qui vous donnent accès à la gestion d’image et aux options de filtre.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imagefilters.filteroptions.MedianFilterOptions;
import com.aspose.psd.imageoptions.GifOptions;
```

## Filtre étape par étape : comment appliquer le filtre médian

### Étape 1 : charger l’image

Tout d’abord, indiquez l’API vers le fichier PSD que vous souhaitez nettoyer.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load the source image
Image image = Image.load(sourceFile);
```

### Étape 2 : convertir l’image en RasterImage

Le filtre agit sur les données raster, nous convertissons donc l’`Image` générique en `RasterImage`.

```java
// Cast the image into RasterImage
RasterImage rasterImage = (RasterImage)image;
if (rasterImage == null) {
    return;
}
```

### Étape 3 : créer une instance de MedianFilterOptions

Configurez la taille du noyau médian. Une taille de **4** fonctionne bien pour un bruit modéré.

```java
// Create an instance of MedianFilterOptions class and set the filter size
MedianFilterOptions options = new MedianFilterOptions(4);
```

### Étape 4 : appliquer le filtre médian

Appliquez maintenant le filtre à l’ensemble des limites de l’image.

```java
// Apply MedianFilterOptions filter to RasterImage object
rasterImage.filter(image.getBounds(), options);
```

### Étape 5 : enregistrer l’image résultante (convertir PSD en GIF)

Après le filtrage, nous enregistrons le résultat au format GIF—démontrant la capacité de **convertir PSD en GIF**.

```java
String destName = dataDir + "median_test_denoise_out.gif";
// Save the resultant image as a GIF
image.save(destName, new GifOptions());
```

En suivant ces étapes, vous avez appliqué avec succès un filtre médian et exporté l’image nettoyée au format GIF.

## Application du filtre Wiener (extension optionnelle)

Si votre projet nécessite une réduction de bruit adaptative, vous pouvez remplacer le filtre médian par un filtre Wiener. La structure du code reste identique ; il suffit d’importer `WienerFilterOptions` et de l’instancier avec le rayon souhaité.

> **Pro tip** : Expérimentez avec différentes tailles de noyau pour les deux filtres afin de trouver le compromis optimal entre suppression du bruit et préservation des détails.

## Problèmes courants et dépannage

| Symptôme | Cause probable | Solution |
|----------|----------------|----------|
| `ClassCastException` lors de la conversion en `RasterImage` | Le fichier d’entrée n’est pas un PSD compatible raster | Vérifiez que le PSD contient des calques raster ou convertissez les calques en raster d’abord |
| Le GIF de sortie est vide | Le chemin de destination est incorrect ou le dossier n’a pas les droits d’écriture | Assurez‑vous que `dataDir` pointe vers un répertoire existant et accessible en écriture |
| Le filtre ne semble pas avoir d’effet | La taille du noyau est trop petite pour le niveau de bruit | Augmentez la taille du filtre (par ex., `new MedianFilterOptions(6)`) |

## Questions fréquentes

**Q1 : Puis‑je appliquer ces filtres à des images de n’importe quel format ?**  
R1 : Oui, Aspose.PSD prend en charge un large éventail de formats d’image, ce qui le rend polyvalent pour divers projets.

**Q2 : Existe‑t‑il un essai gratuit pour Aspose.PSD for Java ?**  
R2 : Oui, vous pouvez obtenir un essai gratuit [here](https://releases.aspose.com/).

**Q3 : Comment obtenir du support pour Aspose.PSD for Java ?**  
R3 : Visitez le [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pour le support communautaire.

**Q4 : Où trouver la documentation d’Aspose.PSD for Java ?**  
R4 : Consultez la documentation [here](https://reference.aspose.com/psd/java/).

**Q5 : Comment acheter Aspose.PSD for Java ?**  
R5 : Vous pouvez acheter le produit [here](https://purchase.aspose.com/buy).

## Conclusion

Dans ce guide, nous avons démontré un processus **step by step filter** pour appliquer les filtres Median (et éventuellement Wiener) avec Aspose.PSD for Java, et nous avons montré comment **convertir PSD en GIF** après le débruitage. Avec ces blocs de construction, vous pouvez intégrer des pipelines de traitement d’image robustes dans n’importe quelle application Java—que vous nettoyiez des photos, prépariez des actifs pour le web ou automatisiez des conversions par lots.

---

**Dernière mise à jour** : 2026-01-07  
**Testé avec** : Aspose.PSD for Java 24.12 (dernière version au moment de la rédaction)  
**Auteur** : Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}