---
date: 2026-06-13
description: Apprenez comment redimensionner une image en Java à l'aide d'une bibliothèque
  de manipulation d'images Java. Suivez notre guide étape par étape avec Aspose.PSD
  pour Java pour une manipulation d'images efficace.
keywords:
- java image manipulation library
- how to resize image java
- change image dimensions java
linktitle: Effectuer un redimensionnement simple
schemas:
- author: Aspose
  dateModified: '2026-06-13'
  description: Learn how to resize image Java using a java image manipulation library.
    Follow our step‑by‑step guide with Aspose.PSD for Java for efficient image manipulation.
  headline: Simple Resizing with Aspose.PSD – Java Image Manipulation Library
  type: TechArticle
- description: Learn how to resize image Java using a java image manipulation library.
    Follow our step‑by‑step guide with Aspose.PSD for Java for efficient image manipulation.
  name: Simple Resizing with Aspose.PSD – Java Image Manipulation Library
  steps:
  - name: Set Your Document Directory
    text: Define the folder that contains the source PSD file. Replace the placeholder
      with your actual path.
  - name: Specify Source and Destination Paths
    text: Create full file names for the input PSD and the output JPEG.
  - name: Load the Image
    text: '`Image.load(path)` reads an image file from the given path and returns
      an `Image` instance. Load the PSD into an `Image` object.'
  - name: Resize the Image
    text: '`image.resize(width, height)` changes the image dimensions to the specified
      pixel size. Resize to the desired dimensions (e.g., 300 × 300 pixels).'
  - name: Save the Resized Image
    text: '`image.save(path, options)` writes the image to the specified file using
      the given format options. Export the resized bitmap as a JPEG file. > **Pro
      tip:** Experiment with different width/height values or maintain the aspect
      ratio by calculating one dimension from the other.'
  type: HowTo
- questions:
  - answer: Absolutely. The `resize(width, height)` method lets you define any pixel
      size you need.
    question: Can I resize images to specific dimensions using Aspose.PSD for Java?
  - answer: Yes. Besides PSD, the library supports JPEG, PNG, BMP, TIFF, and many
      more.
    question: Is Aspose.PSD for Java compatible with different image formats?
  - answer: Refer to the [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/)
      for a full API reference.
    question: Where can I find additional documentation for Aspose.PSD for Java?
  - answer: Certainly! Download the [free trial version](https://releases.aspose.com/)
      to explore all features.
    question: Can I try Aspose.PSD for Java before purchasing?
  - answer: Visit the [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) to ask
      questions and share experiences with the community.
    question: How can I get support for Aspose.PSD for Java?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Redimensionnement simple avec Aspose.PSD – Bibliothèque Java de manipulation
  d'images
url: /fr/java/basic-image-operations/simple-resizing/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Redimensionnement simple avec Aspose.PSD – Bibliothèque Java de manipulation d'images

## Introduction

Si vous êtes développeur Java à la recherche d’une **java image manipulation library** fiable, vous êtes au bon endroit. Dans ce tutoriel, nous allons parcourir **how to resize image java** projets en utilisant Aspose.PSD for Java – une bibliothèque puissante qui rend le traitement d’images rapide et simple. À la fin de ce guide, vous disposerez d’un exemple clair, prêt pour la production, que vous pourrez intégrer à n’importe quelle application Java.

## Réponses rapides
- **Quelle bibliothèque est utilisée ?** Aspose.PSD for Java, une **java image manipulation library** de premier plan.  
- **Puis-je redimensionner n’importe quel PSD ?** Oui – la bibliothèque prend en charge PSD, JPEG, PNG, et plus encore.  
- **Comment spécifier la taille ?** Appelez `image.resize(width, height)` avec les dimensions en pixels souhaitées.  
- **Ai-je besoin d’une licence ?** Un essai gratuit fonctionne pour le développement ; une licence est requise pour la production.  
- **Quelle version de Java est requise ?** Java 8 ou supérieur.

## Qu’est‑ce qu’une Java Image Manipulation Library ?

Une **java image manipulation library** est un ensemble d’APIs Java qui vous permettent de modifier programmétiquement des graphiques raster — redimensionnement, recadrage, conversion de format et gestion des calques — sans outils externes. Aspose.PSD offre ces capacités pour les PSD et de nombreux autres formats, en exposant une API orientée objet claire pour les développeurs.

## Pourquoi utiliser Aspose.PSD pour un redimensionnement simple ?

Aspose.PSD fournit des algorithmes **optimisés pour la performance** qui peuvent traiter des fichiers contenant plus de 500 calques en moins d’une seconde sur un serveur type, et il fonctionne entièrement en Java — aucune DLL native ou binaire externe. La bibliothèque prend en charge **plus de 30 formats d’image** (y compris PSD, JPEG, PNG, TIFF, BMP, GIF) et peut gérer des fichiers de plus de 200 Mo sans charger le document complet en mémoire, ce qui la rend idéale pour les pipelines serveur à haut débit.

## Prérequis

1. **Java Development Kit (JDK)** – téléchargez la dernière version depuis le [site Java](https://www.oracle.com/java/).  
2. **Aspose.PSD for Java** – obtenez la bibliothèque depuis la [page de téléchargement Aspose.PSD for Java](https://releases.aspose.com/psd/java/).  

Disposer de ces éléments assure une configuration fluide pour l’exemple de redimensionnement.

## Importation des packages

La classe `Image` et les options d’exportation associées sont requises pour charger et enregistrer des fichiers.

`Image` est la classe principale représentant une image qui peut être chargée, modifiée et enregistrée.

`JpegOptions` spécifie les paramètres pour enregistrer une image au format JPEG.

Ces importations vous donnent accès à la classe de base `Image` et aux options d’exportation JPEG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.imageoptions.JpegOptions;
```

## Guide étape par étape

### Étape 1 : Définir le répertoire du document

Définissez le dossier contenant le fichier PSD source. Remplacez le texte de substitution par votre chemin réel.

```java
String dataDir = "Your Document Directory";
```

### Étape 2 : Spécifier les chemins source et destination

Créez les noms de fichiers complets pour le PSD d’entrée et le JPEG de sortie.

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "SimpleResizing_out.jpg";
```

### Étape 3 : Charger l’image

`Image.load(path)` lit un fichier image depuis le chemin indiqué et renvoie une instance `Image`.

Chargez le PSD dans un objet `Image`.

```java
Image image = Image.load(sourceFile);
```

### Étape 4 : Redimensionner l’image

`image.resize(width, height)` modifie les dimensions de l’image à la taille en pixels spécifiée.

Redimensionnez aux dimensions souhaitées (par ex., 300 × 300 pixels).

```java
image.resize(300, 300);
```

### Étape 5 : Enregistrer l’image redimensionnée

`image.save(path, options)` écrit l’image dans le fichier spécifié en utilisant les options de format données.

Exportez le bitmap redimensionné en tant que fichier JPEG.

```java
image.save(destName, new JpegOptions());
```

> **Astuce :** Expérimentez avec différentes valeurs de largeur/hauteur ou conservez le ratio d’aspect en calculant une dimension à partir de l’autre.

## Comment changer les dimensions d’une image en Java ?

Utilisez la méthode `resize(width, height)` sur l’instance `Image`, en passant les valeurs exactes en pixels dont vous avez besoin. Par exemple, `image.resize(800, 600)` produira une sortie de 800 × 600 pixels tout en préservant la profondeur de couleur et les métadonnées. Si vous souhaitez conserver le ratio d’aspect original, calculez la seconde dimension en fonction du ratio largeur‑hauteur original avant d’appeler `resize`.

## Problèmes courants et solutions

| Problème | Raison | Solution |
|----------|--------|----------|
| **`OutOfMemoryError`** | Les fichiers PSD très volumineux peuvent dépasser la mémoire du tas JVM. | Augmentez la taille du tas JVM (`-Xmx2g`) ou traitez les images par morceaux. |
| **Unsupported format** | Tentative de charger un fichier non‑PSD sans les options appropriées. | Utilisez la surcharge appropriée de `Image.load` ou convertissez d’abord le fichier. |
| **Distorted output** | Ratio d’aspect incorrect. | Calculez la hauteur en fonction du ratio d’aspect original ou utilisez `image.resizeProportionally`. |

## Questions fréquentes

**Q : Puis‑je redimensionner des images à des dimensions spécifiques en utilisant Aspose.PSD for Java ?**  
A : Absolument. La méthode `resize(width, height)` vous permet de définir n’importe quelle taille en pixels dont vous avez besoin.

**Q : Aspose.PSD for Java est‑il compatible avec différents formats d’image ?**  
A : Oui. En plus du PSD, la bibliothèque prend en charge JPEG, PNG, BMP, TIFF, et bien d’autres.

**Q : Où puis‑je trouver une documentation supplémentaire pour Aspose.PSD for Java ?**  
A : Reportez‑vous à la [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/) pour une référence API complète.

**Q : Puis‑je essayer Aspose.PSD for Java avant d’acheter ?**  
A : Bien sûr ! Téléchargez la [free trial version](https://releases.aspose.com/) pour explorer toutes les fonctionnalités.

**Q : Comment puis‑je obtenir du support pour Aspose.PSD for Java ?**  
A : Visitez le [Aspose.PSD forum](https://forum.aspose.com/c/psd/34) pour poser des questions et partager des expériences avec la communauté.

## Conclusion

Dans ce tutoriel, nous avons démontré comment une **java image manipulation library** comme Aspose.PSD rend les tâches **how to resize image java** sans effort. En suivant les étapes concises ci‑dessus, vous pouvez intégrer le redimensionnement d’images dans n’importe quelle application Java, garantissant des résultats rapides et fiables sans outils externes.

---

**Last Updated:** 2026-06-13  
**Tested With:** Aspose.PSD for Java 24.12 (latest)  
**Author:** Aspose

## Tutoriels associés

- [Redimensionner une image Java - Utilisation de l’énumération Resize Type dans Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)
- [Mise à l’échelle d’image de haute qualité avec le Bicubic Resampler dans Aspose.PSD for Java](/psd/java/advanced-image-manipulation/implement-bicubic-resampler/)
- [Comment convertir PSD en PNG et redimensionner proportionnellement avec Aspose.PSD for Java](/psd/java/advanced-image-manipulation/resize-image-proportionally/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}