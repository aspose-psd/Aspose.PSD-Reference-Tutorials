---
title: Recadrer l'image par rectangle dans Aspose.PSD pour Java
linktitle: Recadrer l'image par rectangle
second_title: API Java Aspose.PSD
description: Explorez les capacités de recadrage d'images transparentes en Java avec Aspose.PSD. Suivez notre guide étape par étape pour recadrer des images sans effort à l'aide d'Aspose.PSD pour Java.
type: docs
weight: 15
url: /fr/java/image-editing/crop-image-by-rectangle/
---
## Introduction

Dans le monde du développement Java, la manipulation d'images est une tâche courante et Aspose.PSD pour Java fournit une solution puissante pour le traitement d'images. Dans ce didacticiel, nous vous guiderons tout au long du processus de recadrage d'une image par un rectangle à l'aide d'Aspose.PSD pour Java. Suivez les étapes ci-dessous pour y parvenir facilement.

## Conditions préalables

Avant de vous lancer dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

- Kit de développement Java (JDK) installé sur votre machine.
-  Aspose.PSD pour la bibliothèque Java. Vous pouvez le télécharger depuis le[site web](https://releases.aspose.com/psd/java/).

## Importer des packages

Assurez-vous d'inclure les packages nécessaires dans votre projet Java pour tirer parti des capacités d'Aspose.PSD pour Java. Ajoutez les instructions d'importation suivantes au début de votre fichier Java :

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;
import com.aspose.psd.Rectangle;

import com.aspose.psd.imageoptions.JpegOptions;
```

Maintenant, décomposons le processus en plusieurs étapes pour vous guider dans le recadrage d'une image par un rectangle à l'aide d'Aspose.PSD pour Java.

## Étape 1 : Configurez votre répertoire de documents

```java
String dataDir = "Your Document Directory";
```

 Remplacer`"Your Document Directory"` avec le chemin réel où se trouve votre fichier PSD.

## Étape 2 : Spécifier les fichiers source et de destination

```java
String sourceFile = dataDir + "sample.psd";
String destName = dataDir + "CroppingByRectangle_out.jpg";
```

Définissez les chemins de votre fichier PSD source et du fichier JPEG de destination.

## Étape 3 : charger et mettre en cache l'image

```java
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);

if (!rasterImage.isCached()) {
    rasterImage.cacheData();
}
```

 Chargez l'image PSD dans un`RasterImage` instance et mettre en cache ses données.

## Étape 4 : Créer et définir le rectangle de recadrage

```java
Rectangle rectangle = new Rectangle(20, 20, 20, 20);
```

 Créez une instance du`Rectangle` classe avec la taille souhaitée pour le recadrage.

## Étape 5 : Recadrer et enregistrer l'image

```java
rasterImage.crop(rectangle);
rasterImage.save(destName, new JpegOptions());
```

Effectuez l'opération de recadrage en utilisant le rectangle spécifié et enregistrez les résultats sous forme de fichier JPEG.

Répétez ces étapes si nécessaire, en ajustant les paramètres en fonction de vos besoins spécifiques.

## Conclusion

Dans ce didacticiel, nous avons parcouru le processus de recadrage d'une image par un rectangle à l'aide d'Aspose.PSD pour Java. En suivant ces étapes, vous pouvez facilement intégrer de puissantes fonctionnalités de manipulation d'images dans vos applications Java.

## FAQ

### Q1 : Puis-je utiliser Aspose.PSD pour Java avec d’autres frameworks Java ?

A1 : Oui, Aspose.PSD pour Java peut être intégré à divers frameworks Java, offrant ainsi une flexibilité dans vos projets de développement.

### Q2 : Existe-t-il un essai gratuit disponible pour Aspose.PSD pour Java ?

 A2 : Oui, vous pouvez accéder à la version d'essai gratuite.[ici](https://releases.aspose.com/).

### Q3 : Où puis-je trouver une assistance ou une assistance supplémentaire ?

 A3 : Visitez le[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pour le soutien et les discussions de la communauté.

### Q4 : Comment puis-je obtenir une licence temporaire pour Aspose.PSD pour Java ?

 A4 : Vous pouvez acquérir une licence temporaire.[ici](https://purchase.aspose.com/temporary-license/).

### Q5 : Quels sont les formats d'image pris en charge pour le recadrage dans Aspose.PSD pour Java ?

A5 : Aspose.PSD pour Java prend en charge divers formats d'image, notamment PSD, PNG, JPEG, etc.