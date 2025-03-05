---
title: Redimensionner les images proportionnellement dans Aspose.PSD pour .NET
linktitle: Redimensionner les images proportionnellement
second_title: API Aspose.PSD.NET
description: Explorez le redimensionnement transparent des images avec Aspose.PSD pour .NET. Téléchargez la bibliothèque, suivez notre tutoriel et améliorez vos capacités de traitement d'image.
type: docs
weight: 14
url: /fr/net/image-manipulation/resize-images-proportionally/
---
Dans le domaine de la manipulation d'images, Aspose.PSD pour .NET se distingue comme une boîte à outils puissante, offrant aux développeurs la possibilité de redimensionner facilement les images proportionnellement. Dans ce guide étape par étape, nous vous guiderons tout au long du processus de redimensionnement des images à l'aide d'Aspose.PSD pour .NET, garantissant ainsi que vos images conservent parfaitement leurs proportions.

## Introduction

Le redimensionnement proportionnel des images est une tâche courante dans de nombreuses applications, et Aspose.PSD pour .NET simplifie ce processus pour les développeurs. Que vous travailliez sur une application Web, un logiciel de bureau ou une application mobile, comprendre comment redimensionner les images tout en préservant leurs proportions est crucial pour maintenir l'attrait visuel et la cohérence.

## Conditions préalables

Avant de plonger dans la magie du redimensionnement avec Aspose.PSD pour .NET, assurez-vous d'avoir les conditions préalables suivantes en place :

1.  Bibliothèque Aspose.PSD pour .NET : assurez-vous que la bibliothèque Aspose.PSD pour .NET est installée. Vous pouvez le télécharger depuis le[Aspose.PSD pour les versions .NET](https://releases.aspose.com/psd/net/) page.

2. Répertoire de documents : créez un répertoire pour stocker vos documents et remplacez "Votre répertoire de documents" dans le code fourni par le chemin réel de ce répertoire.

Maintenant que vous avez configuré les conditions préalables, passons au guide étape par étape.

## Importer des espaces de noms

```csharp
using Aspose.PSD.ImageOptions;
```

Importez les espaces de noms nécessaires pour accéder aux classes et méthodes requises.

## Étape 1 : Charger l'image

```csharp
// Le chemin d'accès au répertoire des documents.
string dataDir = "Your Document Directory";

string sourceFile = dataDir + @"sample.psd";

// Charger une image existante dans une instance de la classe RasterImage
using (Image image = Image.Load(sourceFile))
{
	if (!image.IsCached)
	{
		image.CacheData();
	}
	// Le reste des étapes va ici
}
```

 Chargez l'image source à l'aide du`Image.Load` méthode.

## Étape 2 : Spécifiez la largeur et la hauteur

```csharp
// Spécification de la largeur et de la hauteur
int newWidth = image.Width / 2;
image.ResizeWidthProportionally(newWidth);

int newHeight = image.Height / 2;
image.ResizeHeightProportionally(newHeight);
```

Déterminez la nouvelle largeur et la nouvelle hauteur de l'image redimensionnée. Dans cet exemple, la largeur et la hauteur sont réduites de moitié, mais vous pouvez ajuster ces valeurs en fonction de vos besoins.

## Étape 3 : Enregistrez l'image redimensionnée

```csharp
string destName = dataDir + @"SimpleResizeImageProportionally_out.png";

image.Save(destName, new PngOptions());
```

 Enregistrez l'image redimensionnée à l'aide du`Save` méthode avec les options spécifiées. Dans ce cas, nous l'enregistrons sous forme de fichier PNG.

## Conclusion

Le redimensionnement proportionnel des images dans Aspose.PSD pour .NET est un processus simple qui ajoute de la valeur à votre flux de travail de traitement d'image. Ce guide vous a doté des connaissances nécessaires pour intégrer de manière transparente cette fonctionnalité dans vos applications.

## FAQ

### Q1 : Puis-je redimensionner les images à des dimensions spécifiques ?

A1 : Oui, vous pouvez personnaliser la nouvelle largeur et hauteur selon vos besoins dans le code.

### Q2 : Aspose.PSD pour .NET est-il adapté au redimensionnement d'images par lots ?

A2 : Absolument ! Vous pouvez intégrer ces étapes dans une boucle pour traiter par lots plusieurs images.

### Q3 : Existe-t-il d'autres fonctionnalités de manipulation d'images dans Aspose.PSD pour .NET ?

A3 : Oui, Aspose.PSD pour .NET offre un large éventail de fonctionnalités, notamment le recadrage, la rotation et l'application de filtres aux images.

### Q4 : Existe-t-il un essai gratuit disponible pour Aspose.PSD pour .NET ?

 A4 : Oui, vous pouvez explorer les capacités d'Aspose.PSD pour .NET avec un essai gratuit. Visite[ici](https://releases.aspose.com/) pour commencer.

### Q5 : Où puis-je trouver du support pour Aspose.PSD pour .NET ?

 A5 : Visitez le[Aspose.PSD pour le forum .NET](https://forum.aspose.com/c/psd/34) pour le soutien et les discussions de la communauté.