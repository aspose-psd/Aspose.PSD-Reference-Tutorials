---
title: Agrandissement et recadrage d'images dans Aspose.PSD pour .NET
linktitle: Agrandissement et recadrage des images
second_title: API Aspose.PSD.NET
description: Découvrez comment agrandir et recadrer dynamiquement des images à l'aide d'Aspose.PSD pour .NET. Suivez notre guide étape par étape pour une manipulation transparente des images.
type: docs
weight: 13
url: /fr/net/image-manipulation/expand-crop-images/
---
## Introduction

Aspose.PSD pour .NET est une bibliothèque d'imagerie complète qui permet aux développeurs de travailler avec différents formats d'image dans leurs applications .NET. L'une de ses fonctionnalités les plus remarquables est la capacité de manipuler facilement les images. Dans ce didacticiel, nous nous concentrerons sur l'agrandissement et le recadrage des images, en vous fournissant un guide pratique pour réaliser ces tâches à l'aide d'Aspose.PSD.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

-  Bibliothèque Aspose.PSD pour .NET : assurez-vous que la bibliothèque Aspose.PSD pour .NET est installée. Vous pouvez le télécharger depuis le[Aspose.PSD pour la documentation .NET](https://reference.aspose.com/psd/net/).

- Exemple d'image : préparez un exemple de fichier image (par exemple, "example1.psd") que vous utiliserez pour le didacticiel.

Commençons maintenant par le guide étape par étape.

## Importer des espaces de noms

Commencez par importer les espaces de noms nécessaires pour exploiter les fonctionnalités fournies par Aspose.PSD pour .NET. Ajoutez les espaces de noms suivants à votre code :

```csharp
using Aspose.PSD.ImageOptions;
```

## Étape 1 : configurer le projet

 Assurez-vous d’avoir un projet configuré avec Aspose.PSD pour .NET intégré. Sinon, suivez les[Documentation](https://reference.aspose.com/psd/net/) à titre indicatif.

## Étape 2 : Charger l'image

Chargez l'exemple d'image à l'aide du code suivant :

```csharp
string dataDir = RunExamples.GetDataDir_DrawingAndFormattingImages();
string sourceFile = dataDir + @"example1.psd";

// Charger l'image
using (RasterImage rasterImage = (RasterImage)Image.Load(sourceFile))
{
    // Le code supplémentaire pour le traitement de l'image ira ici
}
```

## Étape 3 : mettre en cache les données d'image

Mettez en cache les données d'image pour optimiser les performances :

```csharp
rasterImage.CacheData();
```

## Étape 4 : Définir le rectangle de destination

Créez une instance de la classe Rectangle et définissez les X, Y, la largeur et la hauteur du rectangle. Ce sera la zone dans laquelle l'image sera agrandie ou recadrée.

```csharp
Rectangle destRect = new Rectangle { X = -200, Y = -200, Width = 300, Height = 300 };
```

## Étape 5 : Enregistrez l'image de sortie

Enregistrez l'image de sortie avec les options spécifiées et le rectangle de destination :

```csharp
string destName = dataDir + @"jpeg_out.jpg";
rasterImage.Save(destName, new JpegOptions(), destRect);
```

## Conclusion

Toutes nos félicitations! Vous avez appris avec succès comment agrandir et recadrer des images à l'aide d'Aspose.PSD pour .NET. Cette puissante bibliothèque ouvre un monde de possibilités de manipulation d'images au sein de vos applications .NET.

## FAQ

### Q1 : Aspose.PSD peut-il gérer d'autres formats d'image que PSD ?

R1 : Oui, Aspose.PSD prend en charge un large éventail de formats d'image, notamment JPEG, PNG, GIF, etc.

### Q2 : Où puis-je trouver de l'assistance pour Aspose.PSD ?

 A2 : Vous pouvez trouver du soutien et interagir avec la communauté sur[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34).

### Q3 Existe-t-il un essai gratuit disponible pour Aspose.PSD pour .NET ?

 A3 : Oui, vous pouvez explorer les fonctionnalités avec un essai gratuit disponible sur[Aspose.PSD Essai gratuit](https://releases.aspose.com/).

### Q4 : Comment puis-je obtenir une licence temporaire pour Aspose.PSD ?

 A4 : Vous pouvez obtenir une licence temporaire auprès de[Aspose.PSD Licence temporaire](https://purchase.aspose.com/temporary-license/).

### Q5 : Où puis-je acheter Aspose.PSD pour .NET ?

 A5 : Vous pouvez acheter la bibliothèque au[Page d'achat Aspose.PSD](https://purchase.aspose.com/buy).