---
date: 2025-12-19
description: Apprenez à ajuster la luminosité d’une image en utilisant Aspose.PSD
  pour Java. Ce tutoriel de manipulation d’images Java fournit un guide étape par
  étape.
linktitle: Adjust Brightness of an Image
second_title: Aspose.PSD Java API
title: Comment ajuster la luminosité d’une image avec Aspose.PSD pour Java
url: /fr/java/advanced-techniques/adjust-brightness/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ajuster la luminosité d'une image avec Aspose.PSD pour Java

## Introduction

Si vous devez **apprendre comment ajuster la luminosité** d’une image directement depuis du code Java, vous êtes au bon endroit. Le réglage de la luminosité est une tâche fréquente pour les graphistes, les photographes et toute personne construisant des pipelines de traitement d’images. Dans ce **tutoriel de manipulation d’images en Java** nous parcourrons le flux complet : chargement d’un PSD/TIFF, application d’un décalage de luminosité, puis sauvegarde du résultat — le tout avec la bibliothèque Aspose.PSD pour Java.

## Réponses rapides
- **Quelle bibliothèque gère la luminosité ?** Aspose.PSD pour Java  
- **Quelle méthode modifie la luminosité ?** `RasterImage.adjustBrightness()`  
- **Puis‑je travailler avec des fichiers PSD et TIFF ?** Oui, l’API prend en charge les deux formats.  
- **Ai‑je besoin d’une licence pour la production ?** Une licence commerciale est requise pour un usage autre que l’évaluation.  
- **Combien de temps prend l’implémentation ?** Généralement moins de 10 minutes pour un réglage de base.

## Qu’est‑ce que le réglage de la luminosité d’une image ?

Le réglage de la luminosité d’une image modifie la clarté globale de chaque pixel. Augmenter la luminosité rend les zones sombres plus claires, tandis que la diminuer assombrit l’ensemble de l’image. Cette opération est utile pour corriger des photos sous‑exposées, préparer des actifs pour l’impression ou créer des effets visuels dans des applications.

## Pourquoi utiliser Aspose.PSD pour Java ?

- **Prise en charge complète des formats** – PSD, TIFF, JPEG, PNG, et plus encore.  
- **Aucune dépendance native externe** – pur Java, facile à intégrer.  
- **Cache haute performance** – les données raster peuvent être mises en cache pour des opérations répétées plus rapides.  
- **API riche** – méthodes pour la correction des couleurs, les calques, les masques et d’autres éditions avancées.

## Prérequis

Avant de commencer le tutoriel, assurez‑vous de disposer des prérequis suivants :

- Bibliothèque Aspose.PSD pour Java : téléchargez et installez la bibliothèque depuis la [documentation Aspose.PSD pour Java](https://reference.aspose.com/psd/java/).

## Importer les packages

Pour commencer, importez les packages nécessaires dans votre projet Java. Dans cet exemple, nous utiliserons les suivants :

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.psd.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.psd.imageoptions.TiffOptions;
```

Décomposons maintenant le processus d’ajustement de la luminosité d’une image en étapes simples :

## Comment ajuster la luminosité avec Aspose.PSD

### Étape 1 : Charger l’image

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

À cette étape, nous chargeons l’image cible et la convertissons en `RasterImage` pour le traitement ultérieur.

### Étape 2 : Ajuster la luminosité

```java
// Adjust the brightness
rasterImage.adjustBrightness(-50);
```

Ici, nous utilisons la méthode `adjustBrightness` pour modifier la luminosité de l’image. Dans cet exemple, nous diminuons la luminosité de 50 unités, mais vous pouvez personnaliser cette valeur selon vos besoins.

### Étape 3 : Définir les TiffOptions

```java
int[] ushort = {8, 8, 8};
// Create an instance of TiffOptions for the resultant image
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setBitsPerSample(ushort);
tiffOptions.setPhotometric(TiffPhotometrics.Rgb);
```

Configurez les `TiffOptions` pour enregistrer l’image ajustée. Ajustez les propriétés `bitsPerSample` et `photometric` en fonction de vos exigences spécifiques.

### Étape 4 : Enregistrer l’image résultante

```java
// Save the resultant image
rasterImage.save(destName, tiffOptions);
```

Enfin, enregistrez l’image modifiée en utilisant les `TiffOptions` spécifiées.

## Problèmes courants et solutions

| Problème | Raison | Solution |
|----------|--------|----------|
| **`ClassCastException` lors du cast d’Image** | Le fichier n’est pas une image raster (par ex., un PSD vectoriel). | Vérifiez le format du fichier source ou utilisez `image instanceof RasterImage` avant le cast. |
| **Le changement de luminosité n’a aucun effet** | L’image n’a pas été mise en cache avant l’ajustement. | Appelez `rasterImage.cacheData()` comme indiqué à l’Étape 1. |
| **Le fichier enregistré apparaît corrompu** | Configuration incorrecte des `TiffOptions`. | Assurez‑vous que `bitsPerSample` correspond à la profondeur de l’image source (généralement 8 bits par canal). |

## Foire aux questions

### Q1 : Puis‑je ajuster la luminosité dans d’autres formats d’image que le PSD ?

R1 : Oui, Aspose.PSD pour Java prend en charge divers formats d’image comme JPEG, PNG et TIFF.

### Q2 : Comment gérer les erreurs pendant le processus d’ajustement d’image ?

R2 : Vous pouvez implémenter la gestion des erreurs avec des blocs try‑catch pour gérer les exceptions éventuelles.

### Q3 : Existe‑t‑il une limite à la plage d’ajustement de la luminosité ?

R3 : La plage d’ajustement dépend du contenu et du format de l’image, mais Aspose.PSD offre une grande flexibilité de personnalisation.

### Q4 : Puis‑je utiliser Aspose.PSD pour Java dans des projets commerciaux ?

R4 : Oui, Aspose.PSD pour Java est une bibliothèque commerciale, et vous pouvez obtenir une licence [ici](https://purchase.aspose.com/buy).

### Q5 : Une version d’essai gratuite est‑elle disponible pour Aspose.PSD pour Java ?

R5 : Oui, vous pouvez explorer la bibliothèque avec une version d’essai gratuite [ici](https://releases.aspose.com/).

### Q6 : La méthode `adjustBrightness` affecte‑t‑elle la visibilité des calques ?

R6 : La méthode agit sur l’image composite rasterisée, donc la visibilité des calques est respectée lors de la rasterisation.

### Q7 : Puis‑je chaîner plusieurs ajustements (par ex., contraste, saturation) ?

R7 : Absolument. Après avoir ajusté la luminosité, vous pouvez appeler `adjustContrast`, `adjustSaturation`, etc., sur la même instance `RasterImage`.

---

**Dernière mise à jour :** 2025-12-19  
**Testé avec :** Aspose.PSD pour Java 24.12 (dernière version au moment de la rédaction)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}