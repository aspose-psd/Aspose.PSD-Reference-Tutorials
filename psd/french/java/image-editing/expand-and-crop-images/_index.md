---
date: 2026-01-07
description: Apprenez à recadrer une image en Java avec Aspose.PSD pour Java. Guide
  étape par étape pour le recadrage d’image, le redimensionnement et la conversion
  de PSD en JPEG.
linktitle: Expand and Crop Images
second_title: Aspose.PSD Java API
title: 'Recadrage d''image Java - agrandir et recadrer les images avec Aspose.PSD
  pour Java'
url: /fr/java/image-editing/expand-and-crop-images/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Crop Image Java : Agrandir et Recadrer des Images avec Aspose.PSD for Java

## Introduction

Dans ce tutoriel, vous découvrirez comment **crop image java** avec la bibliothèque Aspose.PSD. Que vous ayez besoin d'agrandir un canevas, de couper des bords indésirables ou de convertir un fichier PSD en JPEG, les étapes ci‑dessous vous guideront à travers un processus propre et reproductible. Nous couvrirons les prérequis, les instructions d'importation et chaque étape de codage avec des explications claires afin que vous puissiez appliquer la technique à des projets réels.

## Réponses rapides
- **Quelle bibliothèque gère crop image java ?** Aspose.PSD for Java.  
- **Ai‑je besoin d’une licence pour le développement ?** Une version d’essai gratuite suffit pour les tests ; une licence commerciale est requise en production.  
- **Puis‑je convertir un PSD en JPEG tout en recadrant ?** Oui, en utilisant `JpegOptions` conjointement avec un rectangle de recadrage.  
- **Java 8 est‑il supporté ?** Aspose.PSD prend en charge Java 8 et les versions ultérieures.  
- **Combien de temps prend l’implémentation ?** Généralement moins de 10 minutes pour une opération de recadrage basique.

## Qu’est‑ce que “crop image java” ?

Recadrer une image en Java signifie sélectionner une région rectangulaire de l’image source et ignorer le reste. Avec Aspose.PSD, vous pouvez définir cette région à l’aide d’un objet `Rectangle`, puis enregistrer le résultat dans un autre format tel que JPEG.

## Pourquoi utiliser Aspose.PSD for Java pour le recadrage d’images ?

- **Prise en charge complète du PSD** – travaillez directement avec des fichiers PSD à calques sans les convertir au préalable.  
- **Gestion raster haute performance** – utilisation efficace de la mémoire pour les images volumineuses.  
- **Conversion intégrée** – exportez facilement vers JPEG, PNG, BMP, etc., tout en appliquant le recadrage ou l’agrandissement du canevas.  
- **Multiplateforme** – fonctionne sur tout système exécutant Java.

## Prérequis

Avant de commencer, assurez‑vous d’avoir :

1. **Java Development Kit (JDK)** – Java 8 ou version ultérieure installé.  
2. **Aspose.PSD for Java** – téléchargez la bibliothèque depuis le site officiel **[ici](https://releases.aspose.com/psd/java/)**.  

> **Astuce :** Ajoutez le JAR Aspose.PSD à votre classpath ou à vos dépendances Maven/Gradle pour éviter `ClassNotFoundException`.

## Import Packages

Ajoutez les imports nécessaires à votre fichier source Java. Ces classes vous donnent accès au chargement d’image, à la manipulation raster, à la définition de rectangle et aux options d’export JPEG.

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Étape 1 : Définir le Répertoire de Votre Document

Spécifiez le dossier contenant le fichier PSD source. Remplacez le texte de substitution par le chemin réel sur votre machine.

```java
String dataDir = "Your Document Directory";
```

## Étape 2 : Spécifier les Chemins Source et Destination

Définissez où lire le PSD et où écrire le JPEG recadré.

```java
String sourceFile = dataDir + "example1.psd";
String destName = dataDir + "jpeg_out.jpg";
```

## Étape 3 : Charger et Mettre en Cache l’Image

Chargez le PSD dans un objet `RasterImage`. Le cache améliore les performances pour les opérations suivantes comme le recadrage.

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
rasterImage.cacheData();
```

## Étape 4 : Créer le Rectangle de Recadrage

Créez un `Rectangle` qui décrit la région que vous souhaitez conserver. Les coordonnées peuvent être négatives pour **agrandir** le canevas avant le recadrage, ce qui est utile pour ajouter une bordure autour de l’image originale.

```java
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

> **Pourquoi utiliser des coordonnées négatives ?**  
> Des valeurs X/Y négatives déplacent la zone de recadrage vers la gauche/vers le haut, ajoutant ainsi de l’espace vide (agrandissement) autour du contenu original avant le recadrage final.

## Étape 5 : Enregistrer l’Image Recadrée

Enfin, enregistrez l’image résultante à l’aide de `JpegOptions`. Cette étape montre également **convert psd jpeg** tout en appliquant le rectangle de recadrage.

```java
rasterImage.save(destName, new JpegOptions(), destRect);
```

> **Résultat :** `jpeg_out.jpg` contient maintenant une image de 300 × 300 pixels qui a été agrandie de 200 px de chaque côté puis recadrée selon le rectangle défini.

Félicitations ! Vous avez réussi à **java image cropping**, à agrandir le canevas et à convertir un fichier PSD en JPEG—le tout en quelques lignes de code concises.

## Cas d’Utilisation Courants

- **Préparer des actifs pour le web** – recadrer et redimensionner des captures d’écran ou des maquettes avant le téléchargement.  
- **Générer des vignettes** – extraire une région spécifique d’un grand PSD pour des aperçus.  
- **Traitement par lots automatisé** – parcourir un dossier de fichiers PSD, en appliquant le même rectangle de recadrage à chacun.

## Dépannage & Astuces

| Problème | Solution proposée |
|----------|-------------------|
| `OutOfMemoryError` lors du chargement de gros PSD | Appelez `rasterImage.cacheData()` tôt et envisagez d’augmenter la taille du tas JVM (`-Xmx`). |
| La zone recadrée est décalée | Vérifiez les décalages X/Y du rectangle ; rappelez‑vous que les valeurs négatives agrandissent le canevas. |
| Le JPEG de sortie apparaît flou | Ajustez le paramètre de qualité de `JpegOptions` (par ex., `new JpegOptions { Quality = 90 }`). |

## Foire Aux Questions

### Q1 : Aspose.PSD est‑il compatible avec différentes versions de Java ?

R1 : Oui, Aspose.PSD prend en charge plusieurs versions de Java, garantissant la compatibilité avec un large éventail d’environnements de développement.

### Q2 : Puis‑je utiliser Aspose.PSD pour des projets commerciaux ?

R2 : Absolument, Aspose.PSD propose des licences commerciales pour les développeurs, permettant son utilisation tant dans des projets personnels que commerciaux.

### Q3 : Existe‑t‑il des limitations concernant les formats de fichiers image pris en charge ?

R3 : Aspose.PSD supporte divers formats d’image, dont PSD, JPEG, PNG, etc. Consultez la [documentation](https://reference.aspose.com/psd/java/) pour la liste complète.

### Q4 : Comment obtenir du support pour les questions relatives à Aspose.PSD ?

R4 : Visitez le [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pour obtenir de l’aide de la communauté ou de l’équipe de support Aspose.

### Q5 : Une version d’essai gratuite est‑elle disponible ?

R5 : Oui, vous pouvez explorer Aspose.PSD avec une version d’essai gratuite. Téléchargez‑la [ici](https://releases.aspose.com/).

---

**Dernière mise à jour :** 2026-01-07  
**Testé avec :** Aspose.PSD for Java 24.12  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}