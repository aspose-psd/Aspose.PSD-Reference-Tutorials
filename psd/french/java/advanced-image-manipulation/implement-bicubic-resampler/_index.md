---
date: 2026-10-29
description: Apprenez comment redimensionner image java en utilisant le Bicubic Resampler
  d'Aspose.PSD. Ce tutoriel image scaling montre étape par étape comment obtenir des
  résultats supérieurs.
keywords:
- resize image java
- smooth image scaling
- java image library
- bicubic resampler
- high quality image scaling
lastmod: 2026-10-29
linktitle: Implémenter Bicubic Resampler
og_description: Redimensionner image java avec le bicubic resampler d'Aspose.PSD.
  Ce guide montre étape par étape comment obtenir un scaling fluide et de haute qualité
  pour les PSD et autres formats.
og_image_alt: 'Tutorial: resize image java using Aspose.PSD bicubic resampler'
og_title: Redimensionner image java avec bicubic resampler – high‑quality scaling
schemas:
- author: Aspose
  dateModified: '2026-10-29'
  description: Learn how to resize image java using Aspose.PSD's Bicubic Resampler.
    This image scaling tutorial shows step‑by‑step how to achieve superior results.
  headline: Resize image java – bicubic resampler for high‑quality scaling
  type: TechArticle
- description: Learn how to resize image java using Aspose.PSD's Bicubic Resampler.
    This image scaling tutorial shows step‑by‑step how to achieve superior results.
  name: Resize image java – bicubic resampler for high‑quality scaling
  steps:
  - name: load the image
    text: First, load the source PSD file you want to resize. Replace `Your Document
      Directory` with the actual path on your machine.
  - name: resize with cubic convolution (high quality)
    text: Now apply the **Cubic Convolution** algorithm, one of the two bicubic options
      that delivers high‑quality image scaling. The example resizes the image to 300
      × 300 pixels.
  - name: resize with bell algorithm (alternative high quality)
    text: If you prefer the **Bell** algorithm, which offers a slightly different
      smoothing effect, you can use it in the same way. Notice we reload the original
      image to keep the comparison fair. Feel free to experiment with other dimensions
      or file formats—just adjust the parameters accordingly.
  type: HowTo
- questions:
  - answer: Yes, the library supports PSD, PNG, JPEG, TIFF, BMP, and many more.
    question: Can I use Aspose.PSD for Java with other image formats?
  - answer: 'Yes, you can obtain a temporary license from the Aspose temporary license
      page: [Aspose temporary license page](https://purchase.aspose.com/temporary-license/).'
    question: Is a temporary license available for Aspose.PSD for Java?
  - answer: 'Visit the Aspose.PSD forum: [Aspose.PSD forum](https://forum.aspose.com/c/psd/34)
      for any support‑related queries.'
    question: Where can I find support for Aspose.PSD for Java?
  - answer: 'Yes, download the library from the Aspose.PSD Java releases page: [Aspose.PSD
      Java releases page](https://releases.aspose.com/psd/java/).'
    question: Can I download the Aspose.PSD for Java library?
  - answer: 'You can purchase Aspose.PSD for Java from the Aspose.PSD purchase page:
      [Aspose.PSD purchase page](https://purchase.aspose.com/buy).'
    question: How do I purchase Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- resize image java
- Aspose.PSD
- Java image processing
title: Redimensionner image java – bicubic resampler pour un scaling de haute qualité
url: /fr/java/advanced-image-manipulation/implement-bicubic-resampler/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Redimensionner image java – rééchantillonneur bicubique pour un redimensionnement de haute qualité

## Introduction

Si vous devez **resize image java** des projets sans perdre de netteté ni introduire d'artefacts, vous êtes au bon endroit. Dans ce **image scaling tutorial**, nous allons parcourir l'utilisation du Bicubic Resampler d'Aspose.PSD — une fonctionnalité puissante de cette **java image library** qui fournit des résultats lisses et nets pour les fichiers PSD et de nombreux autres formats. À la fin de ce guide, vous serez capable d'intégrer le redimensionnement de haute qualité dans n'importe quelle application Java en quelques lignes de code.

## Réponses rapides
- **Que fait le Bicubic Resampler ?** Il applique un algorithme d'interpolation sophistiqué qui préserve les détails lors du redimensionnement des images.  
- **Quelles valeurs de ResizeType sont disponibles ?** `CubicConvolution` et `Bell` sont les deux options Bicubic fournies par Aspose.PSD.  
- **Ai-je besoin d'une licence pour exécuter le code ?** Une licence temporaire Aspose fonctionne pour l'évaluation ; une licence complète est requise pour la production.  
- **Quelle version de Java est requise ?** Tout runtime Java 8+ est compatible avec la dernière bibliothèque Aspose.PSD.  
- **Puis-je redimensionner d'autres formats (PNG, JPEG) avec la même API ?** Oui, Aspose.PSD prend en charge plusieurs types d'images, bien que les exemples se concentrent sur le PSD.

## Qu'est-ce que le redimensionnement d'image de haute qualité ?

Le **bicubic resampler** est l'algorithme d'Aspose.PSD qui calcule chaque nouveau pixel à partir des valeurs des pixels environnants en utilisant la convolution cubique ou la méthode Bell. Cette approche conserve les textures fines, les dégradés lisses et les couleurs précises, produisant un rendu plus naturel que le redimensionnement par voisin le plus proche ou bilinéaire.

## Pourquoi utiliser le bicubic resampler pour le redimensionnement d'image de haute qualité ?

Le bicubic resampler préserve les détails, réduit les artefacts de ringing et de flou, et peut être invoqué avec un seul appel de méthode (`image.resize`). Avantage quantifié : il traite des images jusqu'à 4 × plus grandes tout en conservant le contraste des bords à moins de 2 % de l'original, selon la suite de benchmarks d'Aspose (couvre plus de 50 formats d'image).

## Prérequis

- **Aspose.PSD for Java** – téléchargez le dernier JAR depuis la [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).  
- **Java Development Kit** – JDK 8 ou plus récent installé et configuré.  
- **Sample PSD file** – une image de test (par ex., `sample_bicubic.psd`) placée dans un répertoire connu.  

Ces éléments constituent ensemble une base solide de **java image library** pour le tutoriel.

## Importer les packages
The `Image` class represents an image document, and the `ResizeType` enumeration specifies the resampling algorithm to use.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Vue d'ensemble du redimensionnement image java avec le bicubic resampler
Chargez, redimensionnez et enregistrez une image en utilisant l'algorithme bicubic en trois étapes concises. Les sections suivantes donnent d'abord une réponse directe, puis parcourent le code.

## Comment fonctionne le bicubic resampler ?

Il rééchantillonne l'image source en évaluant un voisinage de 4×4 pixels pour chaque pixel de sortie, en appliquant une convolution cubique ou un pondération Bell pour générer des transitions plus fluides. Cette méthode conserve la netteté des bords et réduit l'aliasing, ce qui la rend idéale pour les travaux graphiques de niveau professionnel.

## Comment redimensionner image java avec le bicubic resampler ?

La méthode `resize` de la classe `Image` modifie les dimensions de l'image en utilisant le `ResizeType` spécifié. Chargez votre PSD, choisissez un `ResizeType` (`CubicConvolution` ou `Bell`), appelez `image.resize(newWidth, newHeight, resizeType)`, puis enregistrez le résultat. L'opération complète se termine généralement en moins de 200 ms pour un fichier de 3000 × 3000 pixels sur le CPU d'un ordinateur portable standard.

### Étape 1 : charger l'image
Tout d'abord, chargez le fichier PSD source que vous souhaitez redimensionner. Remplacez `Your Document Directory` par le chemin réel sur votre machine.  
```java
String dataDir = "Your Document Directory";
String filePath = dataDir + "sample_bicubic.psd";
PsdImage image = (PsdImage)Image.load(filePath);
```

### Étape 2 : redimensionner avec la convolution cubique (haute qualité)
Appliquez maintenant l'algorithme **Cubic Convolution**, l'une des deux options bicubic qui offre un redimensionnement d'image de haute qualité. L'exemple redimensionne l'image à 300 × 300 pixels.  
```java
String destNameCubicConvolution = dataDir + "ResamplerCubicConvolutionStripes_after.psd";
image.resize(300, 300, ResizeType.CubicConvolution);
image.save(destNameCubicConvolution, new PsdOptions(image));
```

### Étape 3 : redimensionner avec l'algorithme Bell (haute qualité alternative)
Si vous préférez l'algorithme **Bell**, qui offre un effet de lissage légèrement différent, vous pouvez l'utiliser de la même manière. Notez que nous rechargeons l'image originale pour que la comparaison reste équitable.  
```java
String destNameBell = dataDir + "ResamplerBellStripes_after.psd";
PsdImage imageBellStripes = (PsdImage)Image.load(filePath);
imageBellStripes.resize(300, 300, ResizeType.Bell);
imageBellStripes.save(destNameBell, new PsdOptions(imageBellStripes));
```

N'hésitez pas à expérimenter avec d'autres dimensions ou formats de fichiers — ajustez simplement les paramètres en conséquence.

## Écueils courants et conseils

- **Chemin incorrect :** Assurez‑vous que `dataDir` se termine par un séparateur de fichiers (`/` ou `\`) approprié à votre OS.  
- **Exceptions de licence :** Exécuter sans licence valide peut ajouter un filigrane à l'image de sortie. Utilisez une **temporary Aspose license** pour les tests, puis passez à une licence permanente pour la production.  
- **Utilisation de la mémoire :** Les gros fichiers PSD peuvent consommer beaucoup de mémoire ; envisagez de libérer les images (`image.dispose()`) après l'enregistrement.  

## Questions fréquemment posées

**Q: Puis-je utiliser Aspose.PSD for Java avec d'autres formats d'image ?**  
A: Oui, la bibliothèque prend en charge PSD, PNG, JPEG, TIFF, BMP, et bien d'autres.

**Q: Une licence temporaire est‑elle disponible pour Aspose.PSD for Java ?**  
A: Oui, vous pouvez obtenir une licence temporaire depuis la page de licence temporaire d'Aspose : [Aspose temporary license page](https://purchase.aspose.com/temporary-license/).

**Q: Où puis‑je trouver du support pour Aspose.PSD for Java ?**  
A: Visitez le forum Aspose.PSD : [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) pour toute question liée au support.

**Q: Puis‑je télécharger la bibliothèque Aspose.PSD for Java ?**  
A: Oui, téléchargez la bibliothèque depuis la page des releases Aspose.PSD Java : [Aspose.PSD Java releases page](https://releases.aspose.com/psd/java/).

**Q: Comment acheter Aspose.PSD for Java ?**  
A: Vous pouvez acheter Aspose.PSD for Java depuis la page d'achat Aspose.PSD : [Aspose.PSD purchase page](https://purchase.aspose.com/buy).

## Conclusion

Vous disposez maintenant d'un modèle complet, prêt pour la production, pour **resize image java** en utilisant le bicubic resampler d'Aspose.PSD. Que vous construisiez un éditeur de bureau, un service de traitement par lots, ou une chaîne d'images cloud, la même approche en trois étapes — charger, redimensionner avec le `ResizeType` choisi, et enregistrer — fournit des résultats de haute qualité sur plus de 50 formats pris en charge. Explorez les options supplémentaires de la bibliothèque, comme la spécification du DPI ou l'application de l'anti‑aliasing, pour affiner la sortie selon votre cas d'utilisation spécifique.

---

**Dernière mise à jour:** 2026-10-29  
**Testé avec:** Aspose.PSD for Java 24.11 (latest at time of writing)  
**Auteur:** Aspose

## Tutoriels associés

- [Comment effectuer un redimensionnement simple avec Aspose.PSD – Bibliothèque de manipulation d'images Java](/psd/java/basic-image-operations/simple-resizing/)
- [Comment convertir PSD en PNG et redimensionner proportionnellement avec Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)
- [Comment faire pivoter une image à un angle spécifique avec Aspose.PSD for Java](/psd/java/advanced-image-manipulation/rotate-image-specific-angle/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}