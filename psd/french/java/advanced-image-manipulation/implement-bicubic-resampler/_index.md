---
date: 2025-12-01
description: Apprenez comment obtenir un redimensionnement d'image de haute qualité
  en Java avec le Bicubic Resampler d'Aspose.PSD. Suivez notre guide étape par étape
  pour des résultats supérieurs.
language: fr
linktitle: Implement Bicubic Resampler
second_title: Aspose.PSD Java API
title: Mise à l’échelle d’images haute qualité avec le rééchantillonneur bicubique
  dans Aspose.PSD pour Java
url: /java/advanced-image-manipulation/implement-bicubic-resampler/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Redimensionnement d'images de haute qualité avec le rééchantillonneur bicubique dans Aspose.PSD pour Java

## Introduction

Le redimensionnement d'images de haute qualité est une exigence fréquente lorsque vous devez redimensionner des graphiques sans sacrifier la fidélité visuelle. Aspose.PSD pour Java propose un **Bicubic Resampler** qui offre des résultats lisses et nets pour les fichiers PSD et autres formats pris en charge. Dans ce tutoriel, vous apprendrez exactement comment implémenter le rééchantillonneur bicubique, étape par étape, afin d'apporter le redimensionnement d'images de haute qualité à vos applications Java dès aujourd'hui.

## Réponses rapides
- **Que fait le Bicubic Resampler ?** Il applique un algorithme d'interpolation sophistiqué qui préserve les détails lors du redimensionnement des images.  
- **Quelles valeurs ResizeType sont disponibles ?** `CubicConvolution` et `Bell` sont les deux options Bicubic fournies par Aspose.PSD.  
- **Ai-je besoin d'une licence pour exécuter le code ?** Une licence temporaire fonctionne pour l'évaluation ; une licence complète est requise pour la production.  
- **Quelle version de Java est requise ?** Tout runtime Java 8+ est compatible avec la dernière bibliothèque Aspose.PSD.  
- **Puis-je redimensionner d'autres formats (PNG, JPEG) avec la même API ?** Oui, Aspose.PSD prend en charge plusieurs types d'images, bien que les exemples se concentrent sur le PSD.

## Qu'est-ce que le redimensionnement d'images de haute qualité ?

Le redimensionnement d'images de haute qualité désigne le redimensionnement d'une image tout en conservant des bords nets, des dégradés lisses et une représentation précise des couleurs. Le Bicubic Resampler y parvient en tenant compte des valeurs des pixels environnants (en utilisant la convolution cubique ou l'algorithme Bell) pour calculer chaque nouveau pixel, ce qui donne un aspect plus naturel comparé aux méthodes du plus proche voisin ou bilinéaire.

## Pourquoi utiliser le Bicubic Resampler pour le redimensionnement d'images de haute qualité ?

- **Préserve les détails** : Les textures fines et les tracés restent nets même après des changements de taille importants.  
- **Réduit les artefacts** : minimise les effets de halo et le flou qui apparaissent souvent avec des algorithmes plus simples.  
- **Intégration facile** : un appel de méthode en une ligne (`image.resize`) vous permet de changer d'algorithme sans réécrire le code.  

## Prérequis

Avant de commencer, assurez-vous d'avoir :

- **Aspose.PSD for Java** – téléchargez le JAR le plus récent depuis la [documentation Aspose.PSD pour Java](https://reference.aspose.com/psd/java/).  
- **Java Development Kit** – JDK 8 ou supérieur installé et configuré.  
- **Fichier PSD d'exemple** – une image de test (par ex., `sample_bicubic.psd`) placée dans un répertoire connu.

## Importer les packages

Ajoutez les imports requis à votre classe Java. Ceux-ci importent les classes principales d'Aspose.PSD ainsi que l'énumération `ResizeType`.

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Étape 1 : charger l'image

Tout d'abord, chargez le fichier PSD source que vous souhaitez redimensionner. Remplacez `Your Document Directory` par le chemin réel sur votre machine.

```java
String dataDir = "Your Document Directory";
String filePath = dataDir + "sample_bicubic.psd";
PsdImage image = (PsdImage)Image.load(filePath);
```

## Étape 2 : redimensionner avec la convolution cubique (haute qualité)

Appliquez maintenant l'algorithme **Cubic Convolution**, l'une des deux options bicubiques qui offrent un redimensionnement d'image de haute qualité. L'exemple redimensionne l'image à 300 × 300 pixels.

```java
String destNameCubicConvolution = dataDir + "ResamplerCubicConvolutionStripes_after.psd";
image.resize(300, 300, ResizeType.CubicConvolution);
image.save(destNameCubicConvolution, new PsdOptions(image));
```

## Étape 3 : redimensionner avec l'algorithme Bell (alternative haute qualité)

Si vous préférez l'algorithme **Bell**, qui offre un effet de lissage légèrement différent, vous pouvez l'utiliser de la même manière. Notez que nous rechargeons l'image originale pour que la comparaison reste équitable.

```java
String destNameBell = dataDir + "ResamplerBellStripes_after.psd";
PsdImage imageBellStripes = (PsdImage)Image.load(filePath);
imageBellStripes.resize(300, 300, ResizeType.Bell);
imageBellStripes.save(destNameBell, new PsdOptions(imageBellStripes));
```

N'hésitez pas à expérimenter d'autres dimensions ou formats de fichiers — il suffit d'ajuster les paramètres en conséquence.

## Pièges courants et astuces

- **Chemin incorrect** : assurez‑vous que `dataDir` se termine par un séparateur de fichiers (`/` ou `\`) approprié à votre système d'exploitation.  
- **Exceptions de licence** : exécuter le code sans licence valide peut ajouter un filigrane à l'image de sortie.  
- **Utilisation de la mémoire** : les gros fichiers PSD peuvent consommer beaucoup de mémoire ; envisagez de libérer les images (`image.dispose()`) après l'enregistrement.  

## Questions fréquemment posées

**Q : Puis‑je utiliser Aspose.PSD pour Java avec d'autres formats d'image ?**  
A : Oui, la bibliothèque prend en charge PSD, PNG, JPEG, TIFF, BMP, et bien d'autres.

**Q : Une licence temporaire est‑elle disponible pour Aspose.PSD pour Java ?**  
A : Oui, vous pouvez obtenir une licence temporaire [ici](https://purchase.aspose.com/temporary-license/).

**Q : Où puis‑je trouver du support pour Aspose.PSD pour Java ?**  
A : Visitez le forum Aspose.PSD [ici](https://forum.aspose.com/c/psd/34) pour toute question liée au support.

**Q : Puis‑je télécharger la bibliothèque Aspose.PSD pour Java ?**  
A : Oui, téléchargez la bibliothèque depuis la page des versions [ici](https://releases.aspose.com/psd/java/).

**Q : Comment acheter Aspose.PSD pour Java ?**  
A : Vous pouvez acheter Aspose.PSD pour Java depuis la page d'achat [ici](https://purchase.aspose.com/buy).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Dernière mise à jour** : 2025-12-01  
**Testé avec** : Aspose.PSD for Java 24.11 (dernière version au moment de la rédaction)  
**Auteur** : Aspose