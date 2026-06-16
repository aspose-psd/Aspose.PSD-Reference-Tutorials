---
date: 2026-05-19
description: Apprenez comment convert PSD to JPEG et rotate image 270 degrés en utilisant
  Aspose.PSD for Java. Ce guide montre comment rotate les fichiers PSD, flip les images,
  et convert PSD to JPEG.
keywords:
- convert psd to jpeg
- how to rotate psd
- flip image java
- rotate psd layer
- rotate image without photoshop
linktitle: Rotate Image 270 degrés
schemas:
- author: Aspose
  dateModified: '2026-05-19'
  description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  headline: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  type: TechArticle
- description: Learn how to convert PSD to JPEG and rotate image 270 degrees using
    Aspose.PSD for Java. This guide shows how to rotate PSD files, flip images, and
    convert PSD to JPEG.
  name: Convert PSD to JPEG & Rotate 270° with Aspose.PSD for Java
  steps:
  - name: Load the PSD File
    text: '`Image` is Aspose.PSD''s core class that represents a single PSD document
      in memory. Instantiating it reads only the header information, keeping memory
      usage low.'
  - name: Rotate the Image 270 Degrees
    text: '`rotateFlip` performs the specified rotation and optional flip on the image.
      `RotateFlipType.Rotate270FlipNone` rotates the canvas 270 degrees clockwise
      while leaving the image orientation unchanged. > **Pro tip:** If you also need
      to flip the image horizontally or vertically, choose a different `Ro'
  - name: Convert PSD to JPEG and Save
    text: '`JpegOptions` defines JPEG‑specific parameters such as compression quality.
      The `save` method writes the transformed image to disk in the desired format.
      The file `RotatedImage_out.jpg` now contains the original PSD content rotated
      270 degrees and saved as a JPEG.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.PSD supports PSD, JPEG, PNG, BMP, GIF, TIFF, and many other
      raster formats.
    question: Is Aspose.PSD compatible with different image formats?
  - answer: Absolutely! While `RotateFlipType` provides common angles, you can chain
      multiple calls or use transformation matrices for arbitrary angles.
    question: Can I apply custom rotations, not just predefined flips?
  - answer: Replace `JpegOptions` with `PngOptions` (or the appropriate options class)
      in the `save` method.
    question: How do I convert the rotated PSD to another format, such as PNG?
  - answer: For community help, visit the [Aspose.PSD Forum](https://forum.aspose.com/c/psd/34).
    question: Where can I find additional support or assistance?
  - answer: Yes, you can explore Aspose.PSD with a [free trial](https://releases.aspose.com/).
    question: Is there a free trial available?
  type: FAQPage
second_title: Aspose.PSD Java API
title: Convert PSD to JPEG & Rotate 270° avec Aspose.PSD for Java
url: /fr/java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir PSD en JPEG et faire pivoter l'image de 270 degrés avec Aspose.PSD pour Java

## Introduction

Dans ce **tutoriel de traitement d'images Java**, vous apprendrez comment **convertir un PSD en JPEG** tout en faisant pivoter l'image de 270 degrés à l'aide d'Aspose.PSD pour Java. Que vous construisiez une chaîne de traitement par lots, un éditeur web ou un utilitaire de bureau, la bibliothèque vous permet de manipuler les calques PSD sans Photoshop. Nous aborderons également le retournement optionnel et montrerons le flux complet de bout en bout, du chargement d'un fichier PSD à l'enregistrement d'un JPEG.

## Réponses rapides
- **Quelle bibliothèque gère la rotation ?** Aspose.PSD pour Java  
- **Quel angle de rotation l'exemple utilise‑t‑il ?** 270 degrés  
- **Puis‑je également retourner l'image ?** Oui – utilisez les options `RotateFlipType` comme `Rotate90FlipX`  
- **Comment enregistrer le résultat ?** Dans l'exemple nous enregistrons au format JPEG avec `JpegOptions`  
- **Ai‑je besoin d'une licence pour la production ?** Une licence Aspose.PSD valide est requise pour un usage commercial  

## Qu’est‑ce que « faire pivoter l'image de 270 degrés » ?
Faire pivoter une image de 270 degrés signifie tourner la photo de trois quarts de tour complet dans le sens des aiguilles d'une montre (ou de 90 degrés dans le sens inverse). Cette orientation restaure souvent la mise en page portrait d'origine après des transformations antérieures, et elle est couramment utilisée lorsque les images ont été capturées en mode paysage mais doivent être affichées en portrait. Le résultat est une image correctement orientée sans perte de qualité.

## Pourquoi utiliser Aspose.PSD pour cette tâche ?
Aspose.PSD prend en charge **plus de 50 formats d’entrée et de sortie** — y compris PSD, JPEG, PNG, BMP, GIF et TIFF — et peut traiter des fichiers jusqu’à **2 Go** sans charger le document complet en mémoire. L’API fonctionne sur n’importe quel runtime Java (JDK 8+), ne nécessite aucune installation native de Photoshop, et fournit un appel unique `rotateFlip` qui gère à la fois la rotation et le retournement en une étape.

## Prérequis

Avant de commencer, assurez‑vous d’avoir :

- La bibliothèque **Aspose.PSD pour Java** installée. Vous pouvez la télécharger et consulter la référence complète de l’API [ici](https://reference.aspose.com/psd/java/).  
- Un environnement de développement Java (JDK 8 ou supérieur).  
- Un fichier PSD d’exemple que vous souhaitez faire pivoter. Mettez à jour la variable `sourceFile` dans le code avec le chemin correct vers votre fichier.

## Importer les packages

Les classes `Image`, `RotateFlipType` et `JpegOptions` sont nécessaires pour charger, transformer et enregistrer le fichier.  
`Image` est la classe principale représentant un document PSD en mémoire.  
`RotateFlipType` énumère les opérations de rotation et de retournement prises en charge.  
`JpegOptions` configure les paramètres de sortie JPEG tels que la qualité.  

```java
```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```
```

## Comment convertir PSD en JPEG après rotation ?

Chargez le PSD source, appliquez une rotation de 270 degrés, puis enregistrez‑le immédiatement en JPEG. Ce flux en trois étapes s’exécute en moins d’une seconde pour des images typiques de 10 MP sur un CPU moderne, ce qui le rend idéal pour des travaux par lots à haut débit. En ne traitant que les données d’image nécessaires, la consommation mémoire reste faible, et le JPEG résultant conserve la fidélité visuelle tout en réduisant la taille du fichier.

### Étape 1 : Charger le fichier PSD

`Image` est la classe principale d’Aspose.PSD qui représente un document PSD unique en mémoire. Son instanciation ne lit que les informations d’en‑tête, ce qui maintient une utilisation mémoire basse.

```java
```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```
```

### Étape 2 : Faire pivoter l'image de 270 degrés

`rotateFlip` exécute la rotation spécifiée ainsi que le retournement optionnel sur l’image. `RotateFlipType.Rotate270FlipNone` fait pivoter le canevas de 270 degrés dans le sens horaire tout en laissant l’orientation de l’image inchangée.

```java
```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```
```

> **Astuce :** Si vous devez également retourner l'image horizontalement ou verticalement, choisissez un autre `RotateFlipType` tel que `Rotate90FlipX` ou `Rotate180FlipY`.

### Étape 3 : Convertir PSD en JPEG et enregistrer

`JpegOptions` définit les paramètres spécifiques au JPEG comme la qualité de compression. La méthode `save` écrit l’image transformée sur le disque dans le format souhaité.

```java
```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```
```

Le fichier `RotatedImage_out.jpg` contient maintenant le contenu PSD original pivoté de 270 degrés et enregistré au format JPEG.

## Problèmes courants et solutions

| Problème | Solution |
|----------|----------|
| **L'image apparaît à l'envers** | Vérifiez que vous avez utilisé `Rotate270FlipNone`. Pour une rotation de 90 degrés dans le sens horaire, utilisez `Rotate90FlipNone`. |
| **Le fichier de sortie est corrompu** | Assurez‑vous que le dossier de destination existe et que vous avez les permissions d’écriture. |
| **Exception de licence** | Installez une licence Aspose.PSD temporaire ou permanente avant de charger l’image en production. |

## Questions fréquemment posées

**Q : Aspose.PSD est‑il compatible avec différents formats d’image ?**  
R : Oui, Aspose.PSD prend en charge PSD, JPEG, PNG, BMP, GIF, TIFF et de nombreux autres formats raster.

**Q : Puis‑je appliquer des rotations personnalisées, pas seulement les retournements prédéfinis ?**  
R : Absolument ! Bien que `RotateFlipType` propose les angles courants, vous pouvez chaîner plusieurs appels ou utiliser des matrices de transformation pour des angles arbitraires.

**Q : Comment convertir le PSD pivoté vers un autre format, comme PNG ?**  
R : Remplacez `JpegOptions` par `PngOptions` (ou la classe d’options appropriée) dans la méthode `save`.

**Q : Où puis‑je trouver un support ou une assistance supplémentaire ?**  
R : Pour de l’aide communautaire, visitez le [Forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

**Q : Existe‑t‑il un essai gratuit ?**  
R : Oui, vous pouvez explorer Aspose.PSD avec un [essai gratuit](https://releases.aspose.com/).

**Q : Comment obtenir une licence temporaire ?**  
R : Si vous avez besoin d’une licence temporaire, vous pouvez en obtenir une [ici](https://purchase.aspose.com/temporary-license/).

---

**Dernière mise à jour :** 2026-05-19  
**Testé avec :** Aspose.PSD pour Java 24.12  
**Auteur :** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriels associés

- [Convertir PSD en formats d’images raster avec Aspose.PSD pour Java](/psd/java/advanced-techniques/convert-psd-to-raster-formats/)
- [Convertir PSD en PNG et faire pivoter les calques dans les fichiers PSD avec Java](/psd/java/advanced-psd-layer-features-effects/rotate-layers-psd-files/)
- [Comment faire pivoter une image en Java avec Aspose.PSD](/psd/java/advanced-image-manipulation/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}