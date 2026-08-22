---
date: 2026-07-08
description: 'Tutoriel de la bibliothèque Java d''édition d''images : apprenez comment
  rogner une image en Java avec Aspose.PSD for Java, redimensionner, agrandir le canevas
  et convertir un PSD en JPEG.'
keywords:
- java image editing library
- java image processing tutorial
- how to crop image java
lastmod: 2026-07-08
linktitle: Agrandir et rogner les images
og_description: Le tutoriel de la bibliothèque Java d'édition d'images montre comment
  rogner, agrandir le canevas et convertir un PSD en JPEG en quelques minutes avec
  Aspose.PSD for Java.
og_image_alt: 'Guide: Crop and expand images in Java with Aspose.PSD'
og_title: Bibliothèque Java d'édition d'images – Rogner une image avec Aspose.PSD
schemas:
- author: Aspose
  dateModified: '2026-07-08'
  description: 'Java image editing library tutorial: learn how to crop image java
    using Aspose.PSD for Java, resize, expand canvas, and convert PSD to JPEG.'
  headline: Java Image Editing Library – Crop Image with Aspose.PSD
  type: TechArticle
- questions:
  - answer: Aspose.PSD for Java.
    question: What library handles crop image java?
  - answer: A free trial works for testing; a commercial license is required for production.
    question: Do I need a license for development?
  - answer: Yes, using `JpegOptions` together with a cropping rectangle.
    question: Can I convert PSD to JPEG while cropping?
  - answer: Aspose.PSD supports Java 8 and newer versions.
    question: Is Java 8 supported?
  - answer: Typically under 10 minutes for a basic crop operation.
    question: How long does the implementation take?
  type: FAQPage
second_title: Aspose.PSD Java API
tags:
- java image editing
- Aspose.PSD
- image cropping
- PSD to JPEG
title: Bibliothèque Java d'édition d'images – Rogner une image avec Aspose.PSD
url: /fr/java/image-editing/expand-and-crop-images/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Bibliothèque d'édition d'images Java : Recadrer une image Java avec Aspose.PSD

## Introduction

Dans ce tutoriel, vous apprendrez à utiliser une **bibliothèque d'édition d'images Java** — spécifiquement Aspose.PSD pour Java — pour recadrer, agrandir et convertir des fichiers PSD en JPEG. Que vous prépariez des ressources pour un portail web ou automatisiez la génération de miniatures, les étapes ci‑dessous vous offrent un flux de travail reproductible et prêt pour la production que vous pouvez intégrer à tout projet Java 8+.

## Réponses rapides
- **Quelle bibliothèque gère le recadrage d'image Java ?** Aspose.PSD for Java.  
- **Ai-je besoin d'une licence pour le développement ?** Un essai gratuit fonctionne pour les tests ; une licence commerciale est requise pour la production.  
- **Puis-je convertir un PSD en JPEG tout en recadrant ?** Oui, en utilisant `JpegOptions` conjointement avec un rectangle de recadrage.  
- **Java 8 est‑il pris en charge ?** Aspose.PSD prend en charge Java 8 et les versions plus récentes.  
- **Combien de temps prend l'implémentation ?** Typiquement moins de 10 minutes pour une opération de recadrage basique.

## Qu'est-ce que le « recadrage d'image Java » ?

Le recadrage d'image Java consiste à sélectionner une région rectangulaire de l'image source et à supprimer tout ce qui se trouve en dehors de cette région. Avec Aspose.PSD, vous créez un `Rectangle` qui définit la zone, l'appliquez à un `RasterImage`, puis enregistrez le résultat dans n'importe quel format pris en charge tel que JPEG.

## Pourquoi utiliser Aspose.PSD pour le recadrage d'images Java ?

Aspose.PSD fournit une **bibliothèque d'édition d'images Java** qui gère les fichiers PSD nativement, prend en charge plus de 100 fonctionnalités de calque, et peut traiter des images jusqu'à 10 000 × 10 000 pixels tout en maintenant l'utilisation de la mémoire en dessous de 500 Mo. Elle offre également une conversion intégrée vers JPEG, PNG, BMP, et plus, le tout sans nécessiter d'outils externes. Cela rend les pipelines de traitement en masse rapides, fiables et faciles à maintenir.

## Prérequis

1. **Java Development Kit (JDK)** – Java 8 ou version ultérieure installé.  
2. **Aspose.PSD for Java** – téléchargez la bibliothèque depuis le site officiel **[ici](https://releases.aspose.com/psd/java/)**.  

> **Conseil pro :** ajoutez le JAR Aspose.PSD au classpath de votre projet ou aux dépendances Maven/Gradle pour éviter `ClassNotFoundException`.

## Importer les packages

Ajoutez les imports requis à votre fichier source Java. Ces classes vous donnent accès au chargement d'images, à la manipulation raster, à la définition de rectangles et aux options d'exportation JPEG.

## Comment recadrer une image Java avec Aspose.PSD ?

Chargez le PSD source avec `RasterImage`, définissez un `Rectangle` qui décrit la zone de recadrage (les coordonnées négatives peuvent agrandir le canevas), et enfin enregistrez le résultat avec `JpegOptions`. Ce flux en trois étapes gère à la fois le recadrage et la conversion de format en un seul passage, éliminant le besoin de fichiers intermédiaires.

## Étape 1 : Définir le répertoire de votre document

Spécifiez le dossier contenant le fichier PSD source. Remplacez le texte de substitution par le chemin réel sur votre machine.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Étape 2 : Spécifier les chemins source et destination

Définissez où lire le PSD et où écrire le JPEG recadré.

```java
String dataDir = "Your Document Directory";
```

## Étape 3 : Charger et mettre en cache l'image

`RasterImage` représente une version rasterisée d'un fichier PSD en mémoire.  
Chargez le PSD dans un objet `RasterImage`. La mise en cache améliore les performances pour les opérations ultérieures telles que le recadrage.

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## Étape 4 : Créer un rectangle pour le recadrage

`Rectangle` définit les coordonnées X, Y ainsi que la largeur/hauteur de la région de recadrage.  
Créez un `Rectangle` qui décrit la zone que vous souhaitez conserver. Les coordonnées peuvent être négatives pour **agrandir** le canevas avant le recadrage, ce qui est utile pour ajouter une bordure autour de l'image originale.

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

> **Pourquoi utiliser des coordonnées négatives ?**  
> Les valeurs négatives de X/Y déplacent la zone de recadrage vers la gauche/vers le haut, ajoutant effectivement de l'espace vide (agrandissement) autour du contenu original avant le recadrage final.

## Étape 5 : Enregistrer l'image recadrée

`JpegOptions` spécifie les paramètres de sortie JPEG, tels que la qualité et la compression.  
Enfin, enregistrez l'image résultante en utilisant `JpegOptions`. Cette étape montre également **convertir psd jpeg** tout en appliquant le rectangle de recadrage.

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

> **Résultat :** `jpeg_out.jpg` contient maintenant une image de 300 × 300 pixels qui a été agrandie de 200 px de chaque côté puis recadrée selon le rectangle défini.

Félicitations ! Vous avez réussi le **recadrage d'image Java**, agrandi le canevas et converti un fichier PSD en JPEG — le tout en quelques lignes de code concises.

## Cas d'utilisation courants

- **Préparer des ressources pour le web** – recadrer et redimensionner des captures d'écran ou des maquettes avant le téléchargement.  
- **Générer des miniatures** – extraire une région spécifique d'un grand PSD à des fins de prévisualisation.  
- **Traitement par lots automatisé** – parcourir un dossier de fichiers PSD, en appliquant le même rectangle de recadrage à chacun.

## Dépannage et conseils

| Problème | Solution suggérée |
|-------|----------------|
| `OutOfMemoryError` when loading large PSDs | Call `rasterImage.cacheData()` early and consider increasing the JVM heap size (`-Xmx`). |
| Cropped area is off‑center | Verify the rectangle’s X/Y offsets; remember negative values expand the canvas. |
| Output JPEG looks blurry | Adjust `JpegOptions` quality setting (e.g., `new JpegOptions { Quality = 90 }`). |

## Questions fréquentes

### Q1 : Aspose.PSD est‑il compatible avec différentes versions de Java ?

A1 : Oui, Aspose.PSD prend en charge Java 8, 11, 17 et les versions plus récentes, garantissant une large compatibilité avec les environnements de développement.

### Q2 : Puis‑je utiliser Aspose.PSD pour des projets commerciaux ?

A2 : Absolument, Aspose.PSD propose des licences commerciales pour les développeurs, permettant son utilisation tant dans des applications personnelles que commerciales.

### Q3 : Existe‑t‑il des limitations concernant les formats de fichiers image pris en charge ?

A3 : Aspose.PSD prend en charge plus de 30 formats d'image, dont PSD, JPEG, PNG, BMP, TIFF, et d'autres. Consultez la [documentation](https://reference.aspose.com/psd/java/) pour la liste complète.

### Q4 : Comment obtenir du support pour les questions liées à Aspose.PSD ?

A4 : Visitez le [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pour solliciter l'aide de la communauté ou de l'équipe de support d'Aspose.

### Q5 : Une version d'essai gratuite est‑elle disponible ?

A5 : Oui, vous pouvez explorer Aspose.PSD avec une version d'essai gratuite. Téléchargez‑la [ici](https://releases.aspose.com/).

**Dernière mise à jour :** 2026-07-08  
**Testé avec :** Aspose.PSD for Java 24.12  
**Auteur :** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

## Tutoriels associés

- [Redimensionnement simple avec Aspose.PSD – Bibliothèque de manipulation d'images Java](/psd/java/basic-image-operations/simple-resizing/)
- [Comment faire pivoter une image de 270 degrés avec Aspose.PSD pour Java](/psd/java/advanced-image-manipulation/rotate-image/)
- [Comment ajuster le gamma dans le traitement d'images Java avec Aspose.PSD](/psd/java/advanced-techniques/adjust-gamma/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}