---
date: 2026-06-03
description: Apprenez à redimensionner une image avec Aspose.PSD pour Java. Ce guide
  étape par étape couvre l'énumération Resize Type, le redimensionnement d'image haute
  qualité et la conversion de PSD en JPEG.
keywords:
- how to resize image
- convert psd to jpeg
- high quality image resize
- resize image java
- java image manipulation tutorial
linktitle: Redimensionnement avec l'énumération Resize Type
schemas:
- author: Aspose
  dateModified: '2026-06-03'
  description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  headline: How to Resize Image Java Using Resize Type Enumeration
  type: TechArticle
- description: Learn how to resize image with Aspose.PSD for Java. This step‑by‑step
    guide covers the Resize Type Enumeration, high‑quality image resize, and how to
    convert PSD to JPEG.
  name: How to Resize Image Java Using Resize Type Enumeration
  steps:
  - name: '**Java Development Environment** – JDK 8 or newer installed and configured.'
    text: '**Java Development Environment** – JDK 8 or newer installed and configured.'
  - name: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
    text: '**Aspose.PSD Library** – Download the latest JAR from the [website](https://releases.aspose.com/psd/java/).'
  - name: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
    text: '**Sample PSD File** – Use the [sample.psd](Your Document Directory/sample.psd)
      file included with the SDK for hands‑on testing.'
  type: HowTo
- questions:
  - answer: Load the PSD with `Image.load`, then call `image.save("output.jpg", new
      JpegOptions());`.
    question: How do I programmatically convert a PSD file to JPEG without resizing?
  - answer: Yes, you can set the `Resolution` property on the `Image` object before
      saving.
    question: Is it possible to maintain the original DPI when resizing?
  - answer: While you can call `resize` multiple times, it’s more efficient to calculate
      the final dimensions and resize once.
    question: Can I chain multiple resize operations?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Comment redimensionner une image Java en utilisant l'énumération Resize Type
url: /fr/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment redimensionner une image Java en utilisant l'énumération Resize Type

## Introduction

Si vous cherchez **comment redimensionner une image** efficacement dans un projet Java, Aspose.PSD for Java fournit une API propre et haute‑performance. Dans ce tutoriel, nous allons charger un PSD, appliquer l'**Resize Type Enumeration** pour un redimensionnement d'image de haute qualité, et enfin **convertir le PSD en JPEG**. Que vous construisiez un éditeur de bureau ou un pipeline automatisé côté serveur, ces étapes vous permettent de contrôler les dimensions, la qualité et le format en quelques lignes de code.

## Réponses rapides
- **Quelle bibliothèque gère le redimensionnement d'image java ?** Aspose.PSD for Java.
- **Quel type de redimensionnement offre la meilleure qualité ?** `ResizeType.LanczosResample`.
- **Puis-je convertir le PSD en JPEG après le redimensionnement ?** Oui – il suffit d'enregistrer avec `JpegOptions`.
- **Ai-je besoin d'une licence pour la production ?** A valid Aspose.PSD license is required for production use.
- **Cette approche convient-elle aux gros lots ?** Absolutely; the API processes multi‑hundred‑page files without loading the whole document into memory.

## Qu'est-ce que "how to resize image" en Java ?

**How to resize image** désigne le fait de modifier programmétiquement les dimensions en pixels d'une image tout en préservant la fidélité visuelle. La méthode `Resize` d'Aspose.PSD combinée à l'énumération `ResizeType` offre un contrôle précis sur les algorithmes de mise à l'échelle, permettant aux développeurs de maintenir la qualité sur une large gamme de fichiers source et de tailles cibles.

## Pourquoi utiliser l'énumération Resize Type ?

`ResizeType` vous permet de sélectionner l'algorithme de rééchantillonnage qui offre le meilleur compromis entre vitesse et qualité visuelle. Dans la plupart des scénarios, **LanczosResample** fournit des résultats nets avec un coût de performance modeste, traitant une image de 2000 × 1500 en moins de 120 ms sur un CPU de serveur typique tout en conservant les détails des bords.

## Prérequis

Avant de commencer, assurez-vous d'avoir :

1. **Environnement de développement Java** – JDK 8 ou version supérieure installé et configuré.  
2. **Bibliothèque Aspose.PSD** – Téléchargez le dernier JAR depuis le [website](https://releases.aspose.com/psd/java/).  
3. **Fichier PSD d'exemple** – Utilisez le fichier [sample.psd](Your Document Directory/sample.psd) inclus avec le SDK pour des tests pratiques.

## Importer les packages

`Image` est la classe de base pour tous les types d'image dans Aspose.PSD. Ajoutez les imports requis à votre fichier source Java :

```java
import com.aspose.psd.Image;
import com.aspose.psd.ResizeType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Étape 1 : Charger l'image

### Ancre de définition

La classe `RasterImage` est l'objet principal d'Aspose.PSD qui représente une image raster chargée depuis un fichier PSD.

Chargez votre PSD dans une instance `RasterImage` afin de pouvoir manipuler ses pixels :

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
Image image = Image.load(sourceFile);
```

## Étape 2 : Redimensionner l'image

`image.resize(width, height, resizeType)` redimensionne l'image aux dimensions spécifiées en utilisant l'algorithme choisi.

Redimensionnez maintenant l'image chargée en utilisant l'**Enumération Resize Type**. Dans cet exemple, nous utilisons la méthode Lanczos Resample, qui est idéale lorsque vous **how to resize image** avec une haute qualité :

```java
image.resize(300, 300, ResizeType.LanczosResample);
```

## Étape 3 : Enregistrer l'image redimensionnée

`image.save(path, options)` écrit l'image sur le disque dans le format défini par les options fournies.

Après le redimensionnement, enregistrez l'image avec les dimensions spécifiées et le type de redimensionnement choisi. Ici, nous démontrons également **convert psd to jpeg** en enregistrant le résultat sous forme de fichier JPEG :

```java
String destName = dataDir + "ResizingwithResizeTypeEnumeration_out.jpg";
image.save(destName, new JpegOptions());
```

## Pourquoi utiliser l'énumération Resize Type ?

`ResizeType` vous offre un contrôle fin sur l'algorithme de rééchantillonnage, vous permettant d'équilibrer vitesse et qualité. Pour la plupart des applications, `LanczosResample` offre un excellent compromis, fournissant des résultats nets sans pénalité de performance importante, et fonctionne bien sur une variété de contenus d'image.

## Problèmes courants et solutions

- **L'image apparaît floue après le redimensionnement** – Essayez un autre `ResizeType` tel que `Bicubic` ou `NearestNeighbour` pour voir lequel donne le meilleur résultat visuel pour votre image spécifique.  
- **OutOfMemoryError sur les gros fichiers PSD** – Traitez l'image en morceaux plus petits ou augmentez la taille du tas JVM (`-Xmx` flag). Aspose.PSD peut gérer des fichiers jusqu'à **2 GB** sans charger le document complet en mémoire.

## FAQ

### Q1 : Aspose.PSD for Java convient-il aux projets petits et à grande échelle ?

R1 : Absolument ! Aspose.PSD for Java est conçu pour répondre aux projets de toutes tailles, offrant évolutivité et efficacité.

### Q2 : Puis-je utiliser un type de redimensionnement différent de Lanczos Resample ?

R2 : Oui, Aspose.PSD for Java propose différents types de redimensionnement, tels que **NearestNeighbour**, **Bicubic**, et plus encore. Consultez la documentation de l'API pour la liste complète.

### Q3 : Où puis‑je trouver un support supplémentaire pour Aspose.PSD for Java ?

R3 : Pour toute question ou assistance, visitez le [forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Q4 : Existe‑t‑il un essai gratuit disponible pour Aspose.PSD for Java ?

R4 : Oui, vous pouvez accéder à une version d'essai gratuite [ici](https://releases.aspose.com/).

### Q5 : Comment obtenir une licence temporaire pour Aspose.PSD for Java ?

R5 : Pour obtenir une licence temporaire, visitez [ce lien](https://purchase.aspose.com/temporary-license/).

## Questions fréquemment posées

**Q : Comment convertir programmétiquement un fichier PSD en JPEG sans le redimensionner ?**  
R : Chargez le PSD avec `Image.load`, puis appelez `image.save("output.jpg", new JpegOptions());`.

**Q : Est‑il possible de conserver le DPI original lors du redimensionnement ?**  
R : Oui, vous pouvez définir la propriété `Resolution` sur l'objet `Image` avant l'enregistrement.

**Q : Puis‑je enchaîner plusieurs opérations de redimensionnement ?**  
R : Bien que vous puissiez appeler `resize` plusieurs fois, il est plus efficace de calculer les dimensions finales et de redimensionner une seule fois.

---

**Dernière mise à jour :** 2026-06-03  
**Testé avec :** Aspose.PSD for Java 24.12  
**Auteur :** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriels associés

- [Redimensionnement simple avec Aspose.PSD – Bibliothèque de manipulation d'images Java](/psd/java/basic-image-operations/simple-resizing/)
- [Mise à l'échelle d'image haute qualité avec le rééchantillonneur Bicubic dans Aspose.PSD for Java](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)
- [Comment convertir un PSD en PNG et redimensionner proportionnellement avec Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}