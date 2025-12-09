---
date: 2025-12-06
description: Apprenez à faire pivoter une image de 270 degrés avec Aspose.PSD pour
  Java. Ce guide montre comment faire pivoter des fichiers PSD, retourner des images
  et convertir des PSD en JPEG.
linktitle: Rotate Image 270 Degrees
second_title: Aspose.PSD Java API
title: Comment faire pivoter une image de 270 degrés avec Aspose.PSD pour Java
url: /fr/java/advanced-image-manipulation/rotate-image/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Faire pivoter une image de 270 degrés avec Aspose.PSD pour Java

## Introduction

Dans ce **tutoriel de traitement d'images java**, vous découvrirez comment **faire pivoter une image de 270 degrés** rapidement et de manière fiable à l'aide d'Aspose.PSD pour Java. Que vous construisiez un outil de retouche photo, automatisiez des conversions par lots, ou que vous ayez simplement besoin de réorienter un calque PSD, la bibliothèque rend la tâche indolore. Nous aborderons également le retournement d'images et la conversion du PSD pivoté en JPEG, afin que vous disposiez d'un flux de travail complet de bout en bout.

## Réponses rapides
- **Quelle bibliothèque gère la rotation ?** Aspose.PSD pour Java  
- **Quel angle de rotation l'exemple utilise‑t‑il ?** 270 degrés  
- **Puis‑je également retourner l'image ?** Oui – utilisez les options `RotateFlipType` comme `Rotate90FlipX`  
- **Comment enregistrer le résultat ?** Dans l'exemple, nous enregistrons en JPEG avec `JpegOptions`  
- **Ai‑je besoin d'une licence pour la production ?** Une licence Aspose.PSD valide est requise pour un usage commercial  

## Qu’est‑ce que « faire pivoter une image de 270 degrés » ?
Faire pivoter une image de 270 degrés signifie tourner la photo de trois quarts de tour complet dans le sens des aiguilles d'une montre (ou de 90 degrés dans le sens inverse). Dans de nombreux scénarios de retouche graphique, cette orientation correspond à la mise en page portrait originale après une série de transformations.

## Pourquoi utiliser Aspose.PSD pour cette tâche ?
- **Prise en charge complète du PSD** – fonctionne avec les calques, masques et objets d'ajustement.  
- **Pas besoin de Photoshop natif** – s'exécute sur n'importe quel runtime Java.  
- **API simple** – un seul appel de méthode (`rotateFlip`) gère la rotation et le retournement.  
- **Conversion de format facile** – exportation directe vers JPEG, PNG ou autres formats courants.

## Prérequis

Avant de commencer, assurez‑vous d'avoir :

- **Bibliothèque Aspose.PSD pour Java** installée. Vous pouvez la télécharger et consulter la référence complète de l'API [ici](https://reference.aspose.com/psd/java/).  
- Un environnement de développement Java (JDK 8 ou supérieur).  
- Un fichier PSD d'exemple que vous souhaitez faire pivoter. Mettez à jour la variable `sourceFile` dans le code avec le chemin correct vers votre fichier.

## Importer les packages

Commencez par importer les classes nécessaires du package Aspose.PSD :

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Comment faire pivoter un PSD – Étape 1 : charger l’image

Créez une instance `Image` qui pointe vers votre fichier PSD source :

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## Comment faire pivoter un PSD – Étape 2 : faire pivoter l’image de 270 degrés

Utilisez la méthode `rotateFlip` avec `RotateFlipType.Rotate270FlipNone` pour obtenir une rotation de 270 degrés sans aucun retournement :

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

> **Astuce :** Si vous devez également retourner l'image horizontalement ou verticalement, choisissez un autre `RotateFlipType` tel que `Rotate90FlipX` ou `Rotate180FlipY`.

## Comment faire pivoter un PSD – Étape 3 : convertir le PSD en JPEG et enregistrer

Après la rotation, vous pouvez **convertir le PSD en JPEG** (ou tout autre format pris en charge) en utilisant la classe d'options appropriée :

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

Le fichier `RotatedImage_out.jpg` contient maintenant le contenu PSD original pivoté de 270 degrés et enregistré en JPEG.

## Problèmes courants et solutions

| Problème | Solution |
|----------|----------|
| **L'image apparaît à l'envers** | Vérifiez que vous avez utilisé `Rotate270FlipNone`. Pour une rotation de 90 degrés dans le sens horaire, utilisez `Rotate90FlipNone`. |
| **Le fichier de sortie est corrompu** | Assurez‑vous que le dossier de destination existe et que vous disposez des droits d'écriture. |
| **Exception de licence** | Installez une licence Aspose.PSD temporaire ou permanente avant de charger l'image en production. |

## Questions fréquentes

**Q : Aspose.PSD est‑il compatible avec différents formats d'image ?**  
R : Oui, Aspose.PSD prend en charge PSD, JPEG, PNG, BMP, GIF et de nombreux autres formats raster.

**Q : Puis‑je appliquer des rotations personnalisées, pas seulement les retournements prédéfinis ?**  
R : Absolument ! Bien que `RotateFlipType` propose des angles courants, vous pouvez combiner plusieurs appels ou utiliser des matrices de transformation pour des angles arbitraires.

**Q : Comment convertir le PSD pivoté vers un autre format, comme PNG ?**  
R : Remplacez `JpegOptions` par `PngOptions` (ou la classe d'options appropriée) dans la méthode `save`.

**Q : Où puis‑je trouver une assistance supplémentaire ?**  
R : Pour de l'aide communautaire, visitez le [Forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

**Q : Existe‑t‑il un essai gratuit ?**  
R : Oui, vous pouvez explorer Aspose.PSD avec un [essai gratuit](https://releases.aspose.com/).

**Q : Comment obtenir une licence temporaire ?**  
R : Si vous avez besoin d'une licence temporaire, vous pouvez en obtenir une [ici](https://purchase.aspose.com/temporary-license/).

## Conclusion

Vous avez maintenant appris comment **faire pivoter une image de 270 degrés** avec Aspose.PSD pour Java, retourner les images si nécessaire, et exporter le résultat en JPEG. Ce flux de travail simple peut être intégré à des pipelines de traitement d'images basés sur Java plus vastes, vous offrant un contrôle complet sur la manipulation des PSD sans dépendre de Photoshop.

---

**Dernière mise à jour :** 2025-12-06  
**Testé avec :** Aspose.PSD pour Java 24.12  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}