---
title: Faire pivoter une image dans Aspose.PSD pour Java
linktitle: Faire pivoter une image
second_title: API Java Aspose.PSD
description: Explorez la rotation des images en Java sans effort avec Aspose.PSD. Faites pivoter, retournez et enregistrez facilement les fichiers PSD.
type: docs
weight: 19
url: /fr/java/advanced-image-manipulation/rotate-image/
---
## Introduction

Aspose.PSD pour Java fournit un ensemble puissant de fonctionnalités pour travailler avec des images, permettant aux développeurs de manipuler et de traiter efficacement les fichiers PSD. Dans ce didacticiel, nous nous concentrerons sur une tâche spécifique : faire pivoter une image. Que vous créiez une application de retouche photo ou que vous ayez simplement besoin d'ajuster l'orientation d'une image, Aspose.PSD simplifie le processus.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

-  Bibliothèque Aspose.PSD pour Java : assurez-vous d'avoir téléchargé et installé la bibliothèque Aspose.PSD pour Java. Vous pouvez trouver la bibliothèque et la documentation détaillée[ici](https://reference.aspose.com/psd/java/).

- Environnement de développement Java : assurez-vous d'avoir configuré un environnement de développement Java sur votre machine.

-  Exemple de fichier PSD : préparez un exemple de fichier PSD que vous souhaitez faire pivoter. Ajustez le`sourceFile` variable dans l'exemple de code avec le chemin d'accès à votre fichier PSD.

## Importer des packages

Commencez par importer les packages nécessaires pour exploiter les capacités d'Aspose.PSD :

```java
import com.aspose.psd.Image;
import com.aspose.psd.RotateFlipType;

import com.aspose.psd.imageoptions.JpegOptions;
```

## Étape 1 : Charger l'image

 Chargez l'image existante dans une instance du`Image` classe:

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";
Image image = Image.load(sourceFile);
```

## Étape 2 : faire pivoter l'image

 Faites pivoter l'image à l'aide du`rotateFlip` méthode. Dans cet exemple, nous faisons pivoter l'image de 270 degrés :

```java
image.rotateFlip(RotateFlipType.Rotate270FlipNone);
```

## Étape 3 : Enregistrez l'image pivotée

 Enregistrez l'image pivotée à l'aide du`save` et en spécifiant le format de sortie (JPEG, dans ce cas) :

```java
String destName = dataDir + "RotatedImage_out.jpg";
image.save(destName, new JpegOptions());
```

## Conclusion

Félicitations! Vous avez réussi à faire pivoter une image à l’aide d’Aspose.PSD pour Java. Cette bibliothèque simple mais puissante ouvre un monde de possibilités de manipulation d'images dans vos applications Java.

## FAQ

### Q1 : Aspose.PSD est-il compatible avec différents formats d'image ?

A1 : Oui, Aspose.PSD prend en charge divers formats d'image, notamment PSD, JPEG, PNG, etc.

### Q2 : Puis-je appliquer des rotations personnalisées, pas seulement des retournements prédéfinis ?

A2 : Absolument ! Aspose.PSD offre la flexibilité nécessaire pour appliquer des rotations personnalisées afin de répondre à vos besoins spécifiques.

### Q3 : Où puis-je trouver une assistance ou une assistance supplémentaire ?

 A3 : Pour toute question ou problème, visitez le[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pour le soutien de la communauté.

### Q4 : Existe-t-il un essai gratuit ?

 A4 : Oui, vous pouvez explorer Aspose.PSD avec un[essai gratuit](https://releases.aspose.com/).

### Q5 : Comment puis-je obtenir une licence temporaire ?

 A5 : Si vous avez besoin d'un permis temporaire, vous pouvez en obtenir un[ici](https://purchase.aspose.com/temporary-license/).