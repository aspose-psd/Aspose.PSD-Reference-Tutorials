---
title: Rotation d'une image dans Aspose.PSD pour .NET
linktitle: Rotation d'une image
second_title: API Aspose.PSD.NET
description: Apprenez à faire pivoter des images sans effort dans .NET avec Aspose.PSD. Suivez notre tutoriel étape par étape.
type: docs
weight: 15
url: /fr/net/image-manipulation/rotate-image/
---
## Introduction

Si vous plongez dans le monde de la manipulation d'images à l'aide de .NET, Aspose.PSD est votre outil incontournable pour un traitement d'image transparent et efficace. Dans ce didacticiel, nous nous concentrerons sur une tâche fondamentale : faire pivoter une image à l'aide d'Aspose.PSD pour .NET. Suivez-nous pendant que nous décomposons le processus en étapes simples et réalisables.

## Conditions préalables

Avant de commencer, assurez-vous que les conditions préalables suivantes sont remplies :

-  Aspose.PSD pour la bibliothèque .NET : téléchargez et installez la bibliothèque à partir du[Documentation Aspose.PSD .NET](https://reference.aspose.com/psd/net/).

- Votre répertoire de documents : configurez un répertoire dans lequel vos images sont stockées. Remplacez « Votre répertoire de documents » dans l'extrait de code par le chemin d'accès à ce répertoire.

## Importer des espaces de noms

Assurez-vous d'inclure les espaces de noms nécessaires pour accéder à la fonctionnalité Aspose.PSD. Ajoutez les lignes suivantes au début de votre projet .NET :

```csharp
using Aspose.PSD.ImageOptions;
```

## Étape 1 : Charger l'image

```csharp
string sourceFile = dataDir + @"sample.psd";

// Charger une image existante dans une instance de la classe RasterImage
using (Image image = Image.Load(sourceFile))
{
```

## Étape 2 : faire pivoter l'image

```csharp
    // Faites pivoter l'image de 270 degrés dans le sens des aiguilles d'une montre
    image.RotateFlip(RotateFlipType.Rotate270FlipNone);
```

## Étape 3 : Enregistrez l'image pivotée

```csharp
    // Enregistrez l'image pivotée sous forme de fichier JPEG
    string destName = dataDir + @"RotatingAnImage_out.jpg";
    image.Save(destName, new JpegOptions());
}
```

C'est ça! Avec seulement quelques lignes de code, vous avez réussi à faire pivoter une image à l’aide d’Aspose.PSD pour .NET.

## Conclusion

Dans ce didacticiel, nous avons exploré les bases de la rotation d'images à l'aide d'Aspose.PSD pour .NET. Aspose.PSD fournit un ensemble robuste d'outils pour la manipulation d'images, ce qui en fait une bibliothèque essentielle pour les développeurs .NET. Expérimentez différentes rotations et explorez d’autres fonctionnalités pour améliorer vos flux de travail de traitement d’images.

## FAQ

### Q1 : Puis-je faire pivoter les images selon un angle personnalisé à l’aide d’Aspose.PSD ?

 Oui, Aspose.PSD vous permet de spécifier un angle de rotation personnalisé. Remplacez simplement le`RotateFlipType.Rotate270FlipNone` alignez-vous avec l’angle de rotation souhaité.

### Q2 : Aspose.PSD est-il compatible avec différents formats d’image ?

 Absolument. Aspose.PSD prend en charge une large gamme de formats d'image, notamment PSD, JPEG, PNG, etc. Vérifier la[Documentation](https://reference.aspose.com/psd/net/) pour la liste complète.

### Q3 : Comment puis-je obtenir une licence temporaire pour Aspose.PSD ?

 Visiter le[page de licence temporaire](https://purchase.aspose.com/temporary-license/) sur le site Aspose pour obtenir une licence temporaire à des fins d'évaluation.

### Q4 : Où puis-je trouver de l'assistance pour Aspose.PSD ?

 Pour toute question ou assistance, visitez le[Forum Aspose.PSD](https://forum.aspose.com/c/psd/34) et connectez-vous avec la communauté.

### Q5 : Puis-je acheter Aspose.PSD pour un usage commercial ?

 Certainement. Explore le[page d'achat](https://purchase.aspose.com/buy) pour acquérir une licence adaptée à vos besoins.