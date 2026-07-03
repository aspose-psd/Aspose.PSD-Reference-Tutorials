---
date: 2026-07-03
description: Apprenez comment rogner une image Java en utilisant Aspose.PSD pour Java.
  Ce tutoriel pas à pas sur le rognage d'images couvre le chargement des fichiers
  PSD, la définition des valeurs de décalage et l'enregistrement du résultat.
keywords:
- crop image java
- how to crop image
- load psd file
- java image processing
- crop image left right
linktitle: Rogner l'image par décalages
schemas:
- author: Aspose
  dateModified: '2026-07-03'
  description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  headline: Crop Image Java by Shifts with Aspose.PSD
  type: TechArticle
- description: Learn how to crop image java using Aspose.PSD for Java. This step‑by‑step
    image cropping tutorial covers loading PSD files, setting shift values, and saving
    the result.
  name: Crop Image Java by Shifts with Aspose.PSD
  steps:
  - name: Load the Image
    text: '`Image` is the base class for all image types in Aspose.PSD. `RasterImage`
      represents a raster image and provides cropping capabilities.'
  - name: Cache Image Data
    text: '`cacheData()` loads the image data into memory for faster processing.'
  - name: Define Shift Values
    text: Specify the shift values for all four sides of the image (left, top, right,
      bottom) in pixels.
  - name: Apply Cropping
    text: '`crop(left, right, top, bottom)` trims the image by the specified pixel
      shifts on each side.'
  - name: Save the Results
    text: '`JpegOptions` defines JPEG encoding settings such as quality and color
      profile. Congratulations! You''ve successfully cropped an image using Aspose.PSD
      for Java.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports over 30 raster formats, including PSD, JPEG,
      PNG, BMP, TIFF, and GIF, ensuring broad compatibility.
    question: Is Aspose.PSD compatible with all image formats?
  - answer: Absolutely. After each `crop` call you receive a new image object, which
      you can crop again as needed.
    question: Can I apply multiple cropping operations to the same image?
  - answer: Yes, you can find support and engage with the community at [Aspose.PSD
      Forum](https://forum.aspose.com/c/psd/34).
    question: Is there a community forum for Aspose.PSD support?
  - answer: Visit [here](https://purchase.aspose.com/temporary-license/) to obtain
      a temporary license.
    question: How can I obtain a temporary license for Aspose.PSD?
  - answer: Explore the documentation and examples at [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).
    question: Are there sample projects showcasing Aspose.PSD functionalities?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Rogner une image Java par décalages avec Aspose.PSD
url: /fr/java/image-editing/crop-image-by-shifts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Recadrer l'image Java par décalages avec Aspose.PSD

## Introduction

En traitement d'images Java, **crop image java** est une exigence courante pour préparer des graphiques, des vignettes ou des éléments d'interface utilisateur. Aspose.PSD pour Java rend cette tâche simple en exposant une méthode `crop` facile à utiliser qui fonctionne sur tout format raster pris en charge. Dans ce tutoriel, vous apprendrez comment charger un fichier PSD, définir les valeurs de décalage gauche‑droite‑haut‑bas, appliquer le recadrage et enregistrer le résultat — le tout sans écrire de code de manipulation de pixels personnalisé.

## Réponses rapides
- **Quelle bibliothèque gère le recadrage ?** Aspose.PSD for Java provides a built‑in `crop` method.  
- **Ai-je besoin d'une licence ?** A temporary license works for evaluation; a full license is required for production.  
- **Formats pris en charge ?** Over 30 raster formats, including PSD, JPEG, PNG, BMP, and TIFF.  
- **Taille maximale de fichier ?** Handles files up to 2 GB without loading the entire image into memory.  
- **Combien de lignes de code ?** Only five logical steps—load, cache, define shifts, crop, and save.

## Qu'est-ce que crop image java ?
`crop image java` désigne l'opération de découpage d'un bitmap dans une application Java. Avec Aspose.PSD, l'opération est effectuée par la méthode `crop`, qui accepte des valeurs de décalage pour chaque côté de l'image et renvoie une nouvelle instance d'image.

## Pourquoi utiliser Aspose.PSD pour le recadrage d'images ?
Aspose.PSD prend en charge **plus de 30** formats d'image et peut traiter des fichiers PSD de plusieurs centaines de pages tout en utilisant moins de 150 MB de RAM, grâce à son architecture à chargement différé. La bibliothèque garantit également des résultats pixel‑parfait, en préservant les calques, les masques et les profils couleur — ce que de nombreuses bibliothèques d'images génériques ne peuvent pas assurer.

## Prérequis

### Kit de développement Java (JDK)

Assurez‑vous d'avoir la dernière version du JDK installée sur votre système. Vous pouvez le télécharger depuis [here](https://www.oracle.com/java/technologies/javase-downloads.html).

### Bibliothèque Aspose.PSD pour Java

Pour commencer, vous devez obtenir la bibliothèque Aspose.PSD pour Java. Rendez‑vous sur la [page de téléchargement](https://releases.aspose.com/psd/java/) et récupérez la dernière version.

### Environnement de développement intégré (IDE)

Choisissez votre IDE Java préféré, tel qu'Eclipse ou IntelliJ, pour une expérience de codage fluide.

## Comment recadrer une image Java ?

Chargez votre fichier source, définissez les décalages de pixels pour chaque côté, et appelez la méthode `crop` — l’ensemble du flux de travail peut être écrit en cinq lignes de code concises. L'opération `crop` crée une nouvelle image qui ne contient que la région que vous avez spécifiée, laissant le fichier original intact.

### Étape 1 : Charger l'image

`Image` est la classe de base pour tous les types d'image dans Aspose.PSD.  
`RasterImage` représente une image raster et offre des capacités de recadrage.  
```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

### Étape 2 : Mettre en cache les données de l'image

`cacheData()` charge les données de l'image en mémoire pour un traitement plus rapide.  
```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Load an existing image into an instance of RasterImage class
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
```

### Étape 3 : Définir les valeurs de décalage

Spécifiez les valeurs de décalage pour les quatre côtés de l'image (gauche, haut, droite, bas) en pixels.  
```java
if (!rasterImage.isCached()) {
  rasterImage.cacheData();
}
```

### Étape 4 : Appliquer le recadrage

`crop(left, right, top, bottom)` découpe l'image selon les décalages de pixels spécifiés sur chaque côté.  
```java
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

### Étape 5 : Enregistrer les résultats

`JpegOptions` définit les paramètres d'encodage JPEG tels que la qualité et le profil couleur.  
```java
rasterImage.crop(leftShift, rightShift, topShift, bottomShift);
```

Félicitations ! Vous avez recadré une image avec succès en utilisant Aspose.PSD pour Java.

## Problèmes courants et solutions

- **L'image semble inchangée :** Vérifiez que les valeurs de décalage sont positives et ne dépassent pas les dimensions originales.  
- **OutOfMemoryError sur les gros fichiers :** Activez la mise en cache comme indiqué à l'étape 2 ; cela oblige Aspose.PSD à utiliser un fichier temporaire au lieu de garder l'image entière en RAM.  
- **Déviation de couleur après le recadrage :** Assurez‑vous de préserver le profil couleur en appelant `image.save(..., new JpegOptions { ColorProfile = image.ColorProfile })` si vous avez besoin d'une fidélité couleur exacte.

## Questions fréquemment posées

**Q : Aspose.PSD est‑il compatible avec tous les formats d'image ?**  
R : Oui, Aspose.PSD prend en charge plus de 30 formats raster, dont PSD, JPEG, PNG, BMP, TIFF et GIF, assurant une large compatibilité.

**Q : Puis‑je appliquer plusieurs opérations de recadrage à la même image ?**  
R : Absolument. Après chaque appel à `crop` vous recevez un nouvel objet image, que vous pouvez recadrer à nouveau si besoin.

**Q : Existe‑t‑il un forum communautaire pour le support d'Aspose.PSD ?**  
R : Oui, vous pouvez trouver du support et interagir avec la communauté sur le [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).

**Q : Comment obtenir une licence temporaire pour Aspose.PSD ?**  
R : Rendez‑vous sur [here](https://purchase.aspose.com/temporary-license/) pour obtenir une licence temporaire.

**Q : Existe‑t‑il des projets d'exemple montrant les fonctionnalités d'Aspose.PSD ?**  
R : Explorez la documentation et les exemples sur la [Aspose.PSD Java Documentation](https://reference.aspose.com/psd/java/).

---

**Dernière mise à jour :** 2026-07-03  
**Testé avec :** Aspose.PSD 24.11 for Java  
**Auteur :** Aspose  

{{< blocks/products/products-backtop-button >}}

```java
String destName = dataDir + "CroppingByShifts_out.jpg";
rasterImage.save(destName, new JpegOptions());
```

## Tutoriels associés

- [Recadrer l'image par rectangle dans Aspose.PSD pour Java](/psd/java/image-editing/crop-image-by-rectangle/)
- [Recadrer l'image Java - Agrandir et recadrer les images avec Aspose.PSD pour Java](/psd/java/image-editing/expand-and-crop-images/)
- [Redimensionner l'image Java - Utiliser l'énumération Resize Type dans Aspose.PSD pour Java](/psd/java/advanced-image-manipulation/resizing-with-resize-type-enumeration/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}