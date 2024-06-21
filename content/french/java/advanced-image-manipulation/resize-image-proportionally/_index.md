---
title: Redimensionner l'image proportionnellement avec Aspose.PSD pour Java
linktitle: Redimensionner l'image proportionnellement
second_title: API Java Aspose.PSD
description: Améliorez vos applications Java avec Aspose.PSD. Suivez notre guide pour redimensionner les images proportionnellement sans effort. Boostez vos capacités de gestion d’images dès aujourd’hui.
type: docs
weight: 17
url: /fr/java/advanced-image-manipulation/resize-image-proportionally/
---
## Introduction

Bienvenue dans notre guide étape par étape sur le redimensionnement proportionnel des images à l'aide d'Aspose.PSD pour Java. Si vous souhaitez améliorer vos applications Java avec des fonctionnalités efficaces de redimensionnement d'image, vous êtes au bon endroit. Dans ce didacticiel, nous vous guiderons tout au long du processus en suivant des étapes claires et concises.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

1. Environnement Java : assurez-vous que Java est installé sur votre système.
2.  Bibliothèque Aspose.PSD : téléchargez et installez la bibliothèque Aspose.PSD. Vous pouvez trouver les ressources nécessaires[ici](https://releases.aspose.com/psd/java/).

## Importer des packages

Une fois vos prérequis triés, importez les packages requis dans votre projet Java. Assurez-vous que la bibliothèque Aspose.PSD est correctement référencée dans votre projet.

```java
import com.aspose.psd.Image;

import com.aspose.psd.imageoptions.PngOptions;
```

## Étape 1 : Charger l'image

Commencez par charger l'image que vous souhaitez redimensionner dans votre application Java.

```java
String dataDir = "Your Document Directory";
String sourceFile = dataDir + "sample.psd";

Image image = Image.load(sourceFile);

if (!image.isCached()) {
    image.cacheData();
}
```

## Étape 2 : Spécifiez la largeur et la hauteur

Déterminez la nouvelle largeur et la hauteur de votre image redimensionnée. Dans cet exemple, nous allons redimensionner l'image à la moitié de ses dimensions d'origine.

```java
int newWidth = image.getWidth() / 2;
image.resizeWidthProportionally(newWidth);

int newHeight = image.getHeight() / 2;
image.resizeHeightProportionally(newHeight);
```

## Étape 3 : Enregistrez l'image redimensionnée

Enregistrez l'image redimensionnée à l'emplacement souhaité, en spécifiant les options de format (PNG, dans ce cas).

```java
String destName = dataDir + "SimpleResizeImageProportionally_out.png";
image.save(destName, new PngOptions());
```

Et voila! Vous avez réussi à redimensionner une image proportionnellement à l'aide d'Aspose.PSD pour Java.

## Conclusion

Dans ce didacticiel, nous avons couvert les étapes essentielles pour redimensionner les images proportionnellement à l'aide de la bibliothèque Aspose.PSD pour Java. Désormais, vous pouvez facilement intégrer cette fonctionnalité dans vos applications Java pour une meilleure gestion des images.

## FAQ

### Q1 : Aspose.PSD est-il compatible avec tous les formats d'image ?

 A1 : Aspose.PSD prend en charge divers formats d'image, notamment PSD, PNG, JPEG, etc. Vérifier la[Documentation](https://reference.aspose.com/psd/java/) pour une liste complète.

### Q2 : Puis-je utiliser Aspose.PSD pour des projets commerciaux ?

 A2 : Oui, vous pouvez. Visiter le[page d'achat](https://purchase.aspose.com/buy) pour les détails de la licence.

### Q3 : Des licences temporaires sont-elles disponibles à des fins de test ?

 A3 : Oui, vous pouvez obtenir une licence temporaire.[ici](https://purchase.aspose.com/temporary-license/) pour évaluation.

### Q4 : Où puis-je trouver de l'assistance pour Aspose.PSD ?

 A4 : Visitez le[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) pour le soutien et l’assistance de la communauté.

### Q5 : Comment puis-je accéder à la documentation Aspose.PSD ?

 A5 : Reportez-vous à la documentation détaillée[ici](https://reference.aspose.com/psd/java/).
`