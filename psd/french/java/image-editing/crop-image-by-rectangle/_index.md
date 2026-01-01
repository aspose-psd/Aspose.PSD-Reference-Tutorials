---
date: 2026-01-01
description: Découvrez comment recadrer une image en Java avec Aspose.PSD pour Java.
  Suivez notre guide étape par étape pour charger un fichier PSD, recadrer un rectangle
  d’image et convertir le PSD en JPEG.
linktitle: Crop Image by Rectangle
second_title: Aspose.PSD Java API
title: 'Rogner une image Java : rogner l’image par rectangle avec Aspose.PSD'
url: /fr/java/image-editing/crop-image-by-rectangle/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Recadrer une image Java : Recadrer une image par rectangle avec Aspose.PSD

## Introduction

Manipuler les graphiques est une tâche courante du **java image processing**, et Aspose.PSD for Java vous offre une API propre et haute‑performance pour travailler avec les fichiers PSD. Dans ce tutoriel, vous apprendrez **comment recadrer une image** en utilisant un rectangle, charger un fichier PSD, et enfin convertir le résultat en JPEG — le tout en quelques lignes de code Java.

## Réponses rapides
- **Que signifie “crop image java” ?** Il s'agit de couper une image à un rectangle défini en utilisant du code Java.  
- **Quelle bibliothèque gère l'opération ?** Aspose.PSD for Java provides the necessary classes.  
- **Ai-je besoin d'une licence pour les tests ?** A free trial is available; a license is required for production.  
- **Puis-je convertir le PSD recadré en JPEG ?** Yes—use `JpegOptions` when saving.  
- **Combien de temps prend l'implémentation ?** Usually under 10 minutes for a basic scenario.

## Qu'est-ce que le recadrage d'un rectangle d'image en Java ?

Recadrer un rectangle d'image signifie sélectionner une zone spécifique (définie par X, Y, largeur et hauteur) et supprimer tout ce qui se trouve en dehors de cette zone. Cette opération est courante lorsque vous devez vous concentrer sur une région particulière d'un document PSD plus grand.

## Pourquoi utiliser Aspose.PSD pour cette tâche ?

- **Aucune dépendance externe** – works with pure Java.  
- **Prend en charge PSD, PNG, JPEG et de nombreux autres formats** – you can **convert PSD to JPEG** instantly.  
- **Rendu haute fidélité** – retains layer information and color profiles during the crop.  

## Prérequis

- Java Development Kit (JDK) installé.  
- Bibliothèque Aspose.PSD for Java – téléchargez‑la depuis le [site web](https://releases.aspose.com/psd/java/).  

## Importer les packages

Assurez‑vous d'inclure les packages nécessaires dans votre projet Java afin de tirer parti des capacités d'Aspose.PSD for Java. Ajoutez les déclarations d'importation suivantes au début de votre fichier Java :

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

Maintenant, détaillons le processus en plusieurs étapes pour vous guider dans le recadrage d'une image par un rectangle à l'aide d'Aspose.PSD for Java.

## Étape 1 : Configurer votre répertoire de documents

```java
String dataDir = "Your Document Directory";
```

Remplacez `"Your Document Directory"` par le chemin réel où se trouve votre fichier PSD.

## Étape 2 : Spécifier les fichiers source et destination

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "CroppingByRectangle_out.jpg";
```

Définissez les chemins de votre fichier PSD source et du fichier JPEG de destination.

## Étape 3 : Charger et mettre en cache l'image

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);

if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

Ici nous **chargeons le fichier PSD** dans une instance `RasterImage` et mettons en cache ses données pour améliorer les performances.

## Étape 4 : Créer et définir le rectangle de recadrage

```java
Rectangle rectangle = new Rectangle(20, 20, 20, 20);
```

Créez une instance de la classe `Rectangle` avec la taille souhaitée pour le recadrage. Les paramètres représentent respectivement **X**, **Y**, **largeur** et **hauteur**.

## Étape 5 : Recadrer et enregistrer l'image

```java
rasterImage.crop(rectangle);
rasterImage.save(destName, new JpegOptions());
```

Effectuez l'opération de recadrage en utilisant le rectangle spécifié et **convertissez le PSD en JPEG** en enregistrant le résultat avec `JpegOptions`.

Répétez ces étapes selon les besoins, en ajustant les paramètres en fonction de vos exigences spécifiques.

## Problèmes courants et astuces

- **Rectangle en dehors des limites de l'image** – assurez‑vous que les coordonnées du rectangle sont à l'intérieur des dimensions de l'image source.  
- **Consommation mémoire** – appelez `rasterImage.dispose()` une fois terminé pour libérer les ressources natives.  
- **Contrôle de la qualité** – vous pouvez définir `JpegOptions.setQuality(int)` pour contrôler le niveau de compression du JPEG de sortie.  

## Conclusion

Dans ce tutoriel, nous avons parcouru le processus de **crop image java** par un rectangle à l'aide d'Aspose.PSD for Java. En suivant ces étapes, vous pouvez facilement intégrer des capacités puissantes de manipulation d'images — charger un fichier PSD, recadrer une région spécifique et convertir le résultat en JPEG — dans n'importe quelle application Java.

## FAQ

### Q1 : Puis-je utiliser Aspose.PSD for Java avec d'autres frameworks Java ?

R1 : Oui, Aspose.PSD for Java peut être intégré à divers frameworks Java, offrant une flexibilité dans vos projets de développement.

### Q2 : Existe‑t‑il une version d'essai gratuite d'Aspose.PSD for Java ?

R2 : Oui, vous pouvez accéder à la version d'essai gratuite [ici](https://releases.aspose.com/).

### Q3 : Où puis‑je trouver un support ou une assistance supplémentaires ?

R3 : Consultez le [forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pour le support communautaire et les discussions.

### Q4 : Comment obtenir une licence temporaire pour Aspose.PSD for Java ?

R4 : Vous pouvez obtenir une licence temporaire [ici](https://purchase.aspose.com/temporary-license/).

### Q5 : Quels sont les formats d'image pris en charge pour le recadrage dans Aspose.PSD for Java ?

R5 : Aspose.PSD for Java prend en charge divers formats d'image, notamment PSD, PNG, JPEG, et d'autres.

---

**Dernière mise à jour** : 2026-01-01  
**Testé avec** : Aspose.PSD for Java 24.12  
**Auteur** : Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}