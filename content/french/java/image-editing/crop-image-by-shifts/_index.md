---
title: Recadrer l'image par décalages dans Aspose.PSD pour Java
linktitle: Recadrer l'image par décalages
second_title: API Java Aspose.PSD
description: Maîtrisez le recadrage d'images avec Aspose.PSD pour Java. Un tutoriel complet pour une manipulation transparente des images.
type: docs
weight: 16
url: /fr/java/image-editing/crop-image-by-shifts/
---
## Introduction

Dans le domaine du traitement d'images basé sur Java, Aspose.PSD se distingue comme un outil puissant pour manipuler et améliorer les images avec la plus grande précision. L'une des principales caractéristiques qui distingue Aspose.PSD est sa capacité à effectuer un recadrage d'image de manière transparente. Dans ce didacticiel, nous aborderons l'art du recadrage d'images à l'aide d'Aspose.PSD pour Java. À la fin, vous serez doté des compétences nécessaires pour recadrer sans effort des images selon vos spécifications.

## Conditions préalables

Avant de nous lancer dans cette aventure passionnante, assurons-nous que vous disposez des conditions préalables nécessaires :

### Kit de développement Java (JDK)

 Assurez-vous que la dernière version de JDK est installée sur votre système. Vous pouvez le télécharger depuis[ici](https://www.oracle.com/java/technologies/javase-downloads.html).

### Aspose.PSD pour la bibliothèque Java

 Pour commencer, vous devrez obtenir la bibliothèque Aspose.PSD pour Java. Rendez-vous au[page de téléchargement](https://releases.aspose.com/psd/java/) et récupérez la dernière version.

### Environnement de développement intégré (IDE)

Choisissez votre IDE Java préféré, tel qu'Eclipse ou IntelliJ, pour une expérience de codage fluide.

## Importer des packages

Dans votre projet Java, importez les packages nécessaires pour lancer le processus de recadrage de l'image :

```java
import com.aspose.psd.Image;
import com.aspose.psd.RasterImage;

import com.aspose.psd.imageoptions.JpegOptions;
```

Maintenant, décomposons le processus de recadrage d'une image à l'aide d'Aspose.PSD pour Java en une série d'étapes simples :

## Étape 1 : Charger l'image

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

// Charger une image existante dans une instance de la classe RasterImage
RasterImage rasterImage = (RasterImage)Image.load(sourceFile);
```

## Étape 2 : mettre en cache les données d'image

Avant le recadrage, il est conseillé de mettre en cache les données de l'image pour améliorer les performances :

```java
if (!rasterImage.isCached()) {
  rasterImage.cacheData();
}
```

## Étape 3 : Définir les valeurs de décalage

Spécifiez les valeurs de décalage pour les quatre côtés de l'image :

```java
int leftShift = 10;
int rightShift = 10;
int topShift = 10;
int bottomShift = 10;
```

## Étape 4 : appliquer le recadrage

 En fonction des valeurs de décalage définies, appliquez le recadrage sur l'image à l'aide du`crop` méthode:

```java
rasterImage.crop(leftShift, rightShift, topShift, bottomShift);
```

## Étape 5 : Enregistrez les résultats

Enregistrez l'image recadrée sur le disque au format souhaité, dans ce cas, JPEG :

```java
String destName = dataDir + "CroppingByShifts_out.jpg";
rasterImage.save(destName, new JpegOptions());
```

Félicitations! Vous avez réussi à recadrer une image à l'aide d'Aspose.PSD pour Java.

## Conclusion

Dans ce didacticiel, nous avons exploré les subtilités du recadrage d'images avec Aspose.PSD pour Java. Fort de ces connaissances, vous pouvez désormais intégrer de manière transparente le recadrage d'images dans vos projets Java, ajoutant ainsi une touche de finesse à vos capacités de traitement d'images.

## FAQ

### Q1 : Aspose.PSD est-il compatible avec tous les formats d'image ?

A1 : Oui, Aspose.PSD prend en charge une large gamme de formats d'image, garantissant la polyvalence de vos projets.

### Q2 : Puis-je appliquer plusieurs opérations de recadrage à la même image ?

A2 : Absolument, vous pouvez effectuer plusieurs opérations de recadrage de manière séquentielle sur la même image.

### Q3 : Existe-t-il un forum communautaire pour le support d'Aspose.PSD ?

 A3 : Oui, vous pouvez trouver du soutien et vous engager auprès de la communauté sur[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Q4 : Comment puis-je obtenir une licence temporaire pour Aspose.PSD ?

 A4 : Visite[ici](https://purchase.aspose.com/temporary-license/) pour obtenir un permis temporaire.

### Q5 : Existe-t-il des exemples de projets présentant les fonctionnalités d'Aspose.PSD ?

 A5 : Explorez la documentation et les exemples sur[Aspose.PSD Documentation Java](https://reference.aspose.com/psd/java/).
