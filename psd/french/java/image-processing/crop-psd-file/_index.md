---
date: 2026-08-17
description: Apprenez à rogner un fichier PSD en Java avec Aspose.PSD for Java – une
  méthode rapide et précise pour couper les documents Photoshop dans vos applications
  Java.
keywords:
- crop psd file java
- aspose.psd java
- java image cropping
lastmod: 2026-08-17
linktitle: Rogner le fichier PSD
og_description: Rogner un fichier PSD en Java en utilisant Aspose.PSD for Java. Ce
  guide vous montre étape par étape comment couper efficacement les fichiers Photoshop,
  avec des explications sans code et des conseils de bonnes pratiques.
og_image_alt: Guide showing how to crop a PSD file in Java using Aspose.PSD
og_title: Rogner un fichier PSD en Java avec Aspose.PSD – rognage d'image rapide
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to crop psd file java with Aspose.PSD for Java – a fast,
    precise way to trim Photoshop documents in your Java applications.
  headline: Crop psd file java using Aspose.PSD
  type: TechArticle
- description: Learn how to crop psd file java with Aspose.PSD for Java – a fast,
    precise way to trim Photoshop documents in your Java applications.
  name: Crop psd file java using Aspose.PSD
  steps:
  - name: set document directory
    text: Replace “Your Document Directory” with the absolute or relative path that
      contains the PSD you want to process.
  - name: load PSD file
    text: The `RasterImage` class is Aspose.PSD’s entry point for raster‑based operations
      on a PSD file. Loading the file creates an in‑memory representation that you
      can manipulate.
  - name: define crop area
    text: '`Rectangle` defines the X and Y coordinates together with width and height
      of the region to keep. This class is part of the standard Java AWT package and
      is used by Aspose.PSD to specify cropping bounds.'
  - name: save cropped PSD
    text: After applying the crop, you can persist the result back to PSD format.
      The library writes only the cropped pixels, keeping the original color mode
      and bit depth.
  - name: save cropped image as PNG
    text: If you need a web‑friendly version, export the cropped raster to PNG. Aspose.PSD
      provides PNG save options that let you control compression level and interlacing.
  type: HowTo
- questions:
  - answer: Aspose.PSD for Java.
    question: What library handles PSD cropping in Java?
  - answer: Two API calls after loading the image.
    question: How many lines of code are required for a basic crop?
  - answer: Yes, using the built‑in PNG save options.
    question: Can I export the cropped area as PNG?
  - answer: A commercial license is needed beyond the trial period.
    question: Is a license required for production use?
  - answer: Java 8 and later, including Java 11, 17, and 21.
    question: What Java versions are supported?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- crop psd
- aspose.psd
- java image processing
title: Rogner un fichier PSD en Java avec Aspose.PSD
url: /fr/java/image-processing/crop-psd-file/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Recadrer un fichier PSD en Java avec Aspose.PSD

## Introduction

Si vous devez recadrer des documents Photoshop de manière programmatique, **crop psd file java** est une tâche courante pour les développeurs Java travaillant avec des pipelines graphiques, des pipelines d'actifs ou des flux de travail de conception automatisés. Aspose.PSD for Java fournit une API dédiée qui vous permet de définir un rectangle et d'extraire la région dont vous avez besoin en quelques lignes de code seulement. Dans ce tutoriel, vous apprendrez pourquoi la bibliothèque est conçue pour un recadrage haute performance, comment configurer votre environnement, et les étapes exactes pour produire des résultats au format PSD et PNG.

## Réponses rapides
- **Quelle bibliothèque gère le recadrage PSD en Java ?** Aspose.PSD for Java.
- **Combien de lignes de code sont nécessaires pour un recadrage de base ?** Deux appels d'API après le chargement de l'image.
- **Puis-je exporter la zone recadrée en PNG ?** Oui, en utilisant les options d'enregistrement PNG intégrées.
- **Une licence est‑elle requise pour une utilisation en production ?** Une licence commerciale est nécessaire au‑delà de la période d'essai.
- **Quelles versions de Java sont prises en charge ?** Java 8 et ultérieures, y compris Java 11, 17 et 21.

## Qu'est-ce que le recadrage de fichier PSD en Java ?

Le recadrage de fichier PSD en Java désigne le processus de découpage programmatique d'une région rectangulaire d'un document Photoshop (.psd) à l'aide de code Java. Avec Aspose.PSD, vous pouvez effectuer cette opération sans lancer Photoshop, ce qui le rend idéal pour les pipelines d'images côté serveur.

## Pourquoi utiliser Aspose.PSD pour Java ?

Aspose.PSD prend en charge **plus de 30 formats d'entrée et de sortie** et peut traiter des fichiers PSD jusqu'à **500 Mo** sans charger l'intégralité du document en mémoire, grâce à son architecture de streaming. La bibliothèque préserve les calques, les masques et les profils colorimétriques, offrant un résultat recadré qui correspond à la sortie native de Photoshop. Cette performance quantifiée vous permet de gérer des travaux par lots sur du matériel standard avec une utilisation de mémoire prévisible.

## Prérequis

- **Environnement de développement Java** – JDK 8 ou version supérieure installé et configuré.
- **Aspose.PSD for Java** – téléchargez le dernier JAR et la documentation [Aspose.PSD for Java documentation](https://reference.aspose.com/psd/java/).
- **Fichier PSD d'exemple** – placez un fichier .psd dans le répertoire de votre projet afin que le code puisse le localiser.

## Comment recadrer un fichier PSD en Java ?

Chargez le fichier source, définissez le rectangle que vous souhaitez conserver, appliquez le recadrage, puis enregistrez le résultat dans les formats souhaités. L'ensemble du flux de travail ne nécessite que cinq étapes simples, chacune illustrée avec un espace réservé où vous insérerez votre propre code.

### Étape 1 : définir le répertoire du document

Remplacez « Your Document Directory » par le chemin absolu ou relatif contenant le PSD que vous souhaitez traiter.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.png.PngColorType;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
import com.aspose.psd.xmp.types.complex.colorant.ColorType;
```

### Étape 2 : charger le fichier PSD

La classe `RasterImage` est le point d'entrée d'Aspose.PSD pour les opérations raster sur un fichier PSD. Le chargement du fichier crée une représentation en mémoire que vous pouvez manipuler.

```java
String dataDir = "Your Document Directory";
```

### Étape 3 : définir la zone de recadrage

`Rectangle` définit les coordonnées X et Y ainsi que la largeur et la hauteur de la région à conserver. Cette classe fait partie du package Java AWT standard et est utilisée par Aspose.PSD pour spécifier les limites du recadrage.

```java
String sourceFileName = dataDir + "1.psd";
RasterImage image = (RasterImage)Image.load(sourceFileName);
```

### Étape 4 : enregistrer le PSD recadré

Après avoir appliqué le recadrage, vous pouvez enregistrer le résultat au format PSD. La bibliothèque écrit uniquement les pixels recadrés, en conservant le mode couleur et la profondeur de bits d'origine.

```java
image.crop(new Rectangle(10, 30, 100, 100));
```

### Étape 5 : enregistrer l'image recadrée au format PNG

Si vous avez besoin d'une version adaptée au web, exportez le raster recadré au format PNG. Aspose.PSD propose des options d'enregistrement PNG qui vous permettent de contrôler le niveau de compression et l'entrelacement.

```java
String exportPathPsd = dataDir + "CropTest.psd";
image.save(exportPathPsd, new PsdOptions());
```

## Problèmes courants et solutions

- **Coordonnées du rectangle incorrectes** – Assurez‑vous que les valeurs X/Y commencent à 0 pour le coin supérieur gauche ; des valeurs négatives déclencheront une `ArgumentException`.
- **Pics de mémoire sur les gros fichiers** – Utilisez l'option `loadOptions.setLoadOnlyVisibleLayers(true)` pour réduire la mémoire lorsque vous n'avez pas besoin des calques cachés.
- **Perte du profil couleur** – Conservez le profil ICC original en appelant `image.getColorProfile()` avant le recadrage et en le réassignant après l'opération.

## Questions fréquemment posées

### Q1 : puis‑je utiliser Aspose.PSD pour Java pour recadrer des images dans d'autres formats ?

R1 : Aspose.PSD cible principalement les fichiers PSD, mais il prend également en charge BMP, GIF, JPEG, PNG, TIFF et plusieurs autres formats raster pour l'entrée et la sortie.

### Q2 : Aspose.PSD pour Java est‑il adapté au traitement d'images à grande échelle ?

R2 : Oui. L'architecture de streaming de la bibliothèque traite des fichiers PSD de plusieurs centaines de pages avec une empreinte mémoire inférieure à 100 Mo, ce qui la rend idéale pour les travaux par lots.

### Q3 : existe‑t‑il des considérations de licence pour l'utilisation d'Aspose.PSD pour Java ?

R3 : Une licence commerciale est requise pour les déploiements en production. Les détails sont disponibles sur la [page d'achat d'Aspose.PSD pour Java](https://purchase.aspose.com/buy).

### Q4 : comment obtenir du support pour les problèmes liés à Aspose.PSD pour Java ?

R4 : Consultez le [forum Aspose.PSD pour Java](https://forum.aspose.com/c/psd/34) pour poser des questions, partager des extraits de code et recevoir de l'aide de la communauté et des ingénieurs produit.

### Q5 : puis‑je essayer Aspose.PSD pour Java avant d'acheter ?

R5 : Oui, un essai gratuit pleinement fonctionnel peut être téléchargé [Aspose.PSD free trial download](https://releases.aspose.com/).

{{< blocks/products/products-backtop-button >}}

```java
String exportPathPng = dataDir + "CropTest.png";
PngOptions options = new PngOptions();
options.setColorType(PngColorType.TruecolorWithAlpha);
image.save(exportPathPng, options);
```

## Tutoriels associés

- [Recadrer une image par rectangle avec Aspose.PSD pour Java](/psd/java/image-editing/crop-image-by-rectangle/)
- [Recadrer une image par décalages avec Aspose.PSD pour Java](/psd/java/image-editing/crop-image-by-shifts/)
- [Comment faire pivoter une image en Java avec Aspose.PSD](/psd/java/advanced-image-manipulation/rotate-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}