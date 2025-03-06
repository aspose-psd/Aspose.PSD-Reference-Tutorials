---
title: Ajouter une nouvelle couche régulière au PSD avec Aspose.PSD pour Java
linktitle: Ajouter un nouveau calque régulier au PSD
second_title: API Java Aspose.PSD
description: Découvrez comment ajouter une nouvelle couche régulière aux fichiers PSD à l'aide d'Aspose.PSD pour Java. Suivez notre guide étape par étape pour une manipulation transparente du PSD.
weight: 11
url: /fr/java/advanced-image-effects/add-new-regular-layer/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ajouter une nouvelle couche régulière au PSD avec Aspose.PSD pour Java

## Introduction

Bienvenue dans ce didacticiel complet sur l'utilisation d'Aspose.PSD pour Java pour ajouter une nouvelle couche régulière à un fichier PSD. Aspose.PSD est une puissante bibliothèque Java qui permet aux développeurs de manipuler et de travailler efficacement avec les fichiers PSD. Dans ce didacticiel, nous vous guiderons tout au long du processus d'ajout d'une nouvelle couche régulière à un fichier PSD, en vous fournissant des étapes détaillées et des exemples de code.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

- Environnement de développement Java : assurez-vous qu'un environnement de développement Java est configuré sur votre système.
-  Bibliothèque Aspose.PSD : téléchargez et installez la bibliothèque Aspose.PSD pour Java. Vous pouvez trouver la bibliothèque[ici](https://releases.aspose.com/psd/java/).

## Importer des packages

Pour commencer, importez les packages nécessaires dans votre projet Java. Ces packages sont essentiels pour travailler avec les fonctionnalités Aspose.PSD. Incluez les lignes suivantes au début de votre fichier Java :

```java
import com.aspose.psd.Image;
import com.aspose.psd.Rectangle;

import com.aspose.psd.fileformats.psd.PsdImage;
import com.aspose.psd.fileformats.psd.layers.Layer;
import com.aspose.psd.imageoptions.PngOptions;
import com.aspose.psd.imageoptions.PsdOptions;
```

## Étape 1 : Charger le fichier PSD

Chargez le fichier PSD que vous souhaitez modifier en utilisant le code suivant :

```java
String dataDir = "Your Document Directory";
String sourceFileName = dataDir + "OneLayer.psd";
PsdImage im = (PsdImage)Image.load(sourceFileName);
```

## Étape 2 : préparer les tableaux de données et les rectangles

Préparez deux tableaux int et deux objets Rectangle comme suit :

```java
int[] data1 = new int[2500];
int[] data2 = new int[2500];
Rectangle rect1 = new Rectangle(0, 0, 50, 50);
Rectangle rect2 = new Rectangle(0, 0, 100, 25);
```

## Étape 3 : initialiser les données de couche

Initialisez les tableaux de données avec une valeur par défaut :

```java
for (int i = 0; i < 2500; i++) {
    data1[i] = -10000000;
    data2[i] = -10000000;
}
```

## Étape 4 : Ajouter des calques réguliers

Ajoutez deux calques réguliers à l'image PSD :

```java
Layer layer1 = im.addRegularLayer();
layer1.setLeft(25);
layer1.setTop(25);
layer1.setRight(75);
layer1.setBottom(75);
layer1.saveArgb32Pixels(rect1, data1);

Layer layer2 = im.addRegularLayer();
layer2.setLeft(25);
layer2.setTop(150);
layer2.setRight(1255);
layer2.setBottom(175);
layer2.saveArgb32Pixels(rect2, data2);
```

## Étape 5 : Enregistrer le PSD et le PNG

Enregistrez le PSD modifié et un fichier PNG supplémentaire :

```java
im.save(exportPath, new PsdOptions());
im.save(exportPathPng, new PngOptions());
```

Félicitations! Vous avez ajouté avec succès une nouvelle couche régulière à un fichier PSD à l'aide d'Aspose.PSD pour Java.

## Conclusion

Dans ce didacticiel, nous avons couvert le processus d'ajout d'une nouvelle couche régulière à un fichier PSD à l'aide d'Aspose.PSD pour Java. Cette puissante bibliothèque simplifie la manipulation des PSD, la rendant accessible aux développeurs Java. Expérimentez avec différents paramètres et fonctionnalités pour explorer tout le potentiel d’Aspose.PSD.

## FAQ

### Q1 : Aspose.PSD est-il compatible avec Java 8 ?

A1 : Oui, Aspose.PSD prend en charge Java 8 et les versions ultérieures.

### Q2 : Puis-je appliquer des transformations aux calques ajoutés ?

A2 : Absolument ! Aspose.PSD fournit une gamme d'options de transformation pour les calques.

### Q3 : Où puis-je trouver de la documentation supplémentaire sur Aspose.PSD ?

 A3 : Vous pouvez vous référer à la documentation[ici](https://reference.aspose.com/psd/java/).

### Q4 : Comment puis-je obtenir une licence temporaire pour Aspose.PSD ?

 A4 : Visite[ce lien](https://purchase.aspose.com/temporary-license/) pour les options de licence temporaire.

### Q5 : Existe-t-il des forums communautaires pour le support d'Aspose.PSD ?

 A5 : Oui, vous pouvez trouver du soutien et des discussions[ici](https://forum.aspose.com/c/psd/34).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
